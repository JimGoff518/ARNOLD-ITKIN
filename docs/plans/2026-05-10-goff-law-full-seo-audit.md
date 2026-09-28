# Goff Law Full SEO Audit & Remediation Roadmap Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Produce a comprehensive SEO audit of `gofflawdfw.com` with a prioritized remediation roadmap. Compare the site against verified competitor data (Thompson Law from prior recon, plus DFW market signals from SERP analysis). Produce ready-to-implement deliverables: drafted JSON-LD schema blocks, on-page optimization checklist, content gap brief, and an executive-ready roadmap suitable for the COO briefing.

**Architecture:** Multi-phase audit pipeline running locally. Each phase produces a markdown artifact under `recon/goff-law/` that feeds the next phase. The Crawl4AI Docker container at `localhost:11235` (already running and registered as MCP `c4ai-sse`) is the primary content extractor. Schema audit uses direct curl with browser User-Agent because Crawl4AI's `/html` endpoint strips `<head>` content (verified bug in Phase 2 work). SERP positioning verified via WebSearch. Final deliverable is a single executive-ready roadmap.

**Tech Stack:**
- Crawl4AI Docker container at `http://localhost:11235` (lifecycle in @reference_crawl4ai_mcp.md)
- `curl` 8.17.0 (Schannel) on Windows for raw HTTP
- Python 3.14.2 (`python -m pip` for pip) for HTML/XML parsing
- WebSearch tool for live SERP verification
- Edit / Write / Read / Grep / Glob for artifact production
- All artifacts saved under `recon/goff-law/`
- All temp files under `%TEMP%\` (Windows: `C:\Users\jim\AppData\Local\Temp\`)

**Important context for the executor (read before starting):**
- The workspace is **NOT** a git repo. Skip all git commit steps. The verification checkpoint is "save artifact + read it back to confirm contents."
- The user is **Jim Goff**, principal of Goff Law PLLC. He IS the client AND the operator. Do not produce "client gift" deliverables.
- Prior recon on Thompson Law lives at `recon/thompson-law/PHASE-1-RECON-REPORT.md` and `PHASE-2-DEEP-DIVE-REPORT.md` — reference these for benchmarks.
- Existing competitive analysis docs (`goff-law-dfw-competitive-analysis-COMPLETE.md`, `-report.md`, `-ADDENDUM.md`) have been corrected for the Thompson Law URL error (2026-05-10) but contain other unverified claims — treat numerically with skepticism.
- Existing keyword research lives in `DFW_Personal_Injury_Keyword_Research.md` and `gsc-data/` (Google Search Console exports).
- DFW competitor real URLs (verified 2026-05-10): Thompson Law = `1800lionlaw.com`, Witherite = `witheritelaw.com`, real organic threat = `mullenandmullen.com`.

---

## Phase A — Setup & Site Discovery

### Task A1: Pre-flight environment check

**Files:**
- Read: none
- Write: none

**Step 1: Verify Crawl4AI container is running**

Run:
```
docker ps --filter "name=crawl4ai" --format "{{.Names}}: {{.Status}}"
```
Expected: `crawl4ai: Up X minutes (healthy)`

If empty/unhealthy, run `docker start crawl4ai` then poll:
```
i=0; until curl -sf -o nul http://localhost:11235/health; do i=$((i+3)); [ $i -ge 60 ] && { echo TIMEOUT; exit 1; }; sleep 3; done; echo "Healthy after ${i}s"
```

**Step 2: Confirm the recon output directory exists**

Run:
```
mkdir -p "$USERPROFILE/OneDrive/Documents/ArnoldItkin/recon/goff-law" && echo "ok"
```
Expected: `ok`

**Step 3: Save artifact checkpoint**

No artifact yet — environment-only step. Note in the executing session that pre-flight passed.

---

### Task A2: Pull gofflawdfw.com robots.txt + sitemap

**Files:**
- Create: `%TEMP%\goff-robots.txt`
- Create: `%TEMP%\goff-sitemap.xml` (or `goff-sitemap-index.xml` if it's an index)

**Step 1: Fetch robots.txt and inspect for sitemap declaration**

Run:
```
curl -sL --max-time 15 -A "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 Chrome/130.0.0.0 Safari/537.36" https://gofflawdfw.com/robots.txt -o "$TEMP/goff-robots.txt" -w "HTTP %{http_code} | %{size_download}b\n"
```
Expected: `HTTP 200 | 50-500b`. Look for a `Sitemap:` line.

If HTTP != 200, try `https://www.gofflawdfw.com/robots.txt` (with www). If still failing, the site may bot-block — note the failure mode and continue with Crawl4AI in Step 3.

**Step 2: Read robots.txt content to find sitemap URL**

Run:
```
cat "$TEMP/goff-robots.txt"
```
Look for: `Sitemap: https://gofflawdfw.com/sitemap.xml` (or `sitemap_index.xml`). Note the URL.

**Step 3: Fetch the sitemap**

Run (substitute the actual sitemap URL discovered above; default if not found):
```
curl -sL --max-time 30 -A "Mozilla/5.0 Chrome/130" https://gofflawdfw.com/sitemap_index.xml -o "$TEMP/goff-sitemap-index.xml" -w "HTTP %{http_code} | %{size_download}b\n"
```
Expected: `HTTP 200 | 500-50000b`. If 404, try `/sitemap.xml`.

**Step 4: Verify it's XML, not HTML**

Run:
```
head -c 200 "$TEMP/goff-sitemap-index.xml"
```
Expected starts with: `<?xml version="1.0"...` or `<sitemapindex` or `<urlset`. If it starts with `<!doctype html>`, the request returned a 404 page styled as HTML — try alternative URLs.

**Step 5: Save artifact checkpoint**

Confirm both files exist:
```
ls -la "$TEMP/goff-robots.txt" "$TEMP/goff-sitemap-index.xml"
```
Expected: both files listed with non-zero size.

---

### Task A3: Inventory all gofflawdfw.com URLs from sitemap

**Files:**
- Create: `recon/goff-law/01-url-inventory.md`

**Step 1: Parse the sitemap (handle both index and direct sitemap)**

Run:
```
python << 'PY'
import re, os, urllib.request
tmp = os.environ['TEMP']
with open(os.path.join(tmp,'goff-sitemap-index.xml'), encoding='utf-8') as f:
    xml = f.read()
sitemaps = re.findall(r'<sitemap>\s*<loc>([^<]+)</loc>', xml)
direct_urls = re.findall(r'<url>\s*<loc>([^<]+)</loc>', xml)
print(f'Sub-sitemaps: {len(sitemaps)}')
print(f'Direct URLs: {len(direct_urls)}')
if sitemaps:
    for s in sitemaps: print(f'  SUB: {s}')
elif direct_urls:
    print(f'  First 5 URLs: {direct_urls[:5]}')
PY
```
Expected: Either a list of sub-sitemap URLs (it's an index) OR a count of direct URLs.

**Step 2: Fetch all sub-sitemaps if present**

If sub-sitemaps exist, fetch each with curl and save to `%TEMP%\goff-sub-sitemap-N.xml`. Loop construction:
```
n=1; for url in $(grep -oE '<loc>[^<]+</loc>' "$TEMP/goff-sitemap-index.xml" | sed 's/<[^>]*>//g'); do
  curl -sL --max-time 20 -A "Mozilla/5.0 Chrome/130" "$url" -o "$TEMP/goff-sub-sitemap-${n}.xml" -w "${url}: HTTP %{http_code} | %{size_download}b\n"
  n=$((n+1))
done
```

**Step 3: Aggregate and categorize all URLs**

Run:
```
python << 'PY'
import re, os, glob
from collections import defaultdict
tmp = os.environ['TEMP']
all_urls = set()
files = glob.glob(os.path.join(tmp, 'goff-sub-sitemap-*.xml')) or [os.path.join(tmp,'goff-sitemap-index.xml')]
for fp in files:
    with open(fp, encoding='utf-8') as f:
        all_urls.update(re.findall(r'<loc>([^<]+)</loc>', f.read()))
print(f'TOTAL URLS: {len(all_urls)}')
buckets = defaultdict(list)
for u in all_urls:
    path = u.replace('https://gofflawdfw.com','').replace('https://www.gofflawdfw.com','').rstrip('/')
    parts = [p for p in path.split('/') if p]
    top = parts[0] if parts else 'home'
    buckets[top].append(u)
print()
for section, items in sorted(buckets.items(), key=lambda x:-len(x[1])):
    print(f'  /{section}: {len(items)}')
PY
```
Expected: ~20-200 total URLs (Goff Law per existing docs is much smaller than Thompson Law).

**Step 4: Write the inventory artifact**

Use the Write tool to create `recon/goff-law/01-url-inventory.md` with this structure:
```markdown
# Goff Law — URL Inventory

**Crawl date:** 2026-05-10
**Source:** {sitemap URL used}
**Total URLs:** {count}

## Top-level sections
| Section | URL count |
|---|---|
| /{top1} | {n} |
...

## Full URL list
{flat bullet list of every URL, grouped by section}
```

**Step 5: Verify artifact**

Run:
```
wc -l "recon/goff-law/01-url-inventory.md"
```
Expected: at least 30 lines (grows with URL count).

---

## Phase B — Technical SEO Audit

### Task B1: Crawl every Goff Law page (or top 30 if site has >50)

**Files:**
- Create: `%TEMP%\goff-page-N.json` (one per page, where N is a sanitized slug)
- Create: `%TEMP%\goff-raw-N.html` (one per page, raw HTML for schema audit)

**Step 1: Decide crawl scope**

If total URLs ≤ 50, crawl all. If >50, crawl: homepage + every practice-area page + every attorney bio + top 5 most-linked pages (use the URL inventory). Note the chosen list in a temp file `%TEMP%\goff-crawl-list.txt`.

**Step 2: Crawl each URL through Crawl4AI /md (markdown)**

Loop construction:
```
cd "$TEMP" && cat goff-crawl-list.txt | while read -r url; do
  slug=$(echo "$url" | sed 's|https://[^/]*||;s|/$||;s|/|_|g;s|^_||')
  [ -z "$slug" ] && slug="home"
  curl -s -X POST http://localhost:11235/md \
    -H "Content-Type: application/json" \
    -d "{\"url\": \"${url}\", \"f\": \"fit\"}" \
    -o "goff-page-${slug}.json" \
    -w "${slug}: HTTP %{http_code} | %{size_download}b | %{time_total}s\n" \
    --max-time 90 &
done
wait
echo "---all done---"
```
Expected: each page returns HTTP 200 with 5KB-50KB markdown.

**Step 3: Crawl each URL via direct curl for raw HTML (needed for schema audit)**

Same loop but use direct curl (Crawl4AI strips `<head>`):
```
cd "$TEMP" && cat goff-crawl-list.txt | while read -r url; do
  slug=$(echo "$url" | sed 's|https://[^/]*||;s|/$||;s|/|_|g;s|^_||')
  [ -z "$slug" ] && slug="home"
  curl -sL --max-time 30 -A "Mozilla/5.0 Chrome/130" "$url" -o "goff-raw-${slug}.html" -w "${slug}: HTTP %{http_code} | %{size_download}b\n" &
done
wait
```
Expected: each page returns HTTP 200 with 50KB-500KB raw HTML.

**Step 4: Verify both artifact sets**

Run:
```
ls "$TEMP/goff-page-"*.json | wc -l; ls "$TEMP/goff-raw-"*.html | wc -l
```
Expected: matching counts.

**Step 5: Note any failures**

If any URL returned non-200, log it to `recon/goff-law/00-crawl-failures.md` so the audit doesn't silently miss pages. If failures > 20% of pages, STOP and investigate before proceeding.

---

### Task B2: Audit schema markup across all crawled pages

**Files:**
- Create: `recon/goff-law/02-schema-audit.md`

**Step 1: Run schema extraction script (mirror Phase 2 method)**

Run:
```
python << 'PY'
import json, os, re, glob
from collections import Counter, defaultdict
tmp = os.environ['TEMP']
files = sorted(glob.glob(os.path.join(tmp, 'goff-raw-*.html')))
all_types = Counter()
per_page = {}
for fp in files:
    name = os.path.basename(fp).replace('goff-raw-','').replace('.html','')
    with open(fp, encoding='utf-8', errors='replace') as f:
        html = f.read()
    blocks = re.findall(r'<script[^>]*type=["\']application/ld\+json["\'][^>]*>(.*?)</script>', html, re.DOTALL | re.IGNORECASE)
    types_here = []
    for b in blocks:
        try:
            data = json.loads(b.strip())
            items = data.get('@graph', [data]) if isinstance(data, dict) else data
            if not isinstance(items, list): items = [items]
            for it in items:
                t = it.get('@type','?')
                if isinstance(t, list): t = '+'.join(t)
                types_here.append(t)
                all_types[t] += 1
        except Exception as e:
            pass
    per_page[name] = types_here
    print(f'{name:40s} | LD-JSON blocks: {len(blocks)} | types: {types_here}')
print(f'\n=== AGGREGATE ACROSS {len(files)} PAGES ===')
for t, n in all_types.most_common():
    print(f'  {t}: {n}')
PY
```
Expected output: list of pages with their schema types. If most pages show 0 LD-JSON blocks, that's the headline finding (huge gap to fix).

**Step 2: Cross-reference against the "ideal" schema set for a PI law firm**

Build a comparison table. The ideal set per Phase 2 Thompson Law analysis:
- `Organization` / `LegalService` (firm identity)
- `WebSite` (sitewide search box)
- `BreadcrumbList` (every page)
- `WebPage` (every page)
- `Attorney` (each attorney bio)
- `AggregateRating` + `Review` (homepage + key pages)
- `FAQPage` (every page with FAQs)
- `Service` (each practice-area page)
- `Offer` (free-consultation CTA)
- `LocalBusiness` (variant of LegalService with hours/address)

**Step 3: Write the schema audit artifact**

Use Write to create `recon/goff-law/02-schema-audit.md` with structure:
```markdown
# Goff Law — Schema Markup Audit

**Crawl date:** 2026-05-10
**Pages audited:** {count}
**Comparison benchmark:** Thompson Law (1800lionlaw.com), per recon/thompson-law/PHASE-2-DEEP-DIVE-REPORT.md

## Aggregate schema types found
| Schema type | Pages with it | Should be on (Goff goal) | Gap |
|---|---|---|---|

## Per-page schema inventory
{table: page slug | types present | missing critical types}

## Critical gaps
1. {gap with impact estimate}
...

## Comparison vs Thompson Law
| Schema type | Goff | Thompson Law | Notes |
|---|---|---|---|
```

**Step 4: Verify artifact exists and has expected sections**

Run:
```
grep -c "^##" "recon/goff-law/02-schema-audit.md"
```
Expected: at least 4 H2 sections.

---

### Task B3: Audit meta tags + page-level SEO basics

**Files:**
- Create: `recon/goff-law/03-meta-tags-audit.md`

**Step 1: Extract meta + structural signals from every raw HTML**

Run:
```
python << 'PY'
import os, re, glob, csv, sys
tmp = os.environ['TEMP']
files = sorted(glob.glob(os.path.join(tmp,'goff-raw-*.html')))
rows = []
for fp in files:
    name = os.path.basename(fp).replace('goff-raw-','').replace('.html','')
    with open(fp, encoding='utf-8', errors='replace') as f:
        html = f.read()
    title = re.search(r'<title>(.*?)</title>', html, re.DOTALL)
    desc = re.search(r'<meta[^>]+name=["\']description["\'][^>]+content=["\']([^"\']+)', html, re.IGNORECASE)
    canonical = re.search(r'<link[^>]+rel=["\']canonical["\'][^>]+href=["\']([^"\']+)', html, re.IGNORECASE)
    og_title = re.search(r'<meta[^>]+property=["\']og:title["\'][^>]+content=["\']([^"\']+)', html)
    og_image = re.search(r'<meta[^>]+property=["\']og:image["\'][^>]+content=["\']([^"\']+)', html)
    h1s = re.findall(r'<h1[^>]*>(.*?)</h1>', html, re.DOTALL | re.IGNORECASE)
    h2s = re.findall(r'<h2[^>]*>(.*?)</h2>', html, re.DOTALL | re.IGNORECASE)
    text = re.sub(r'<script[^>]*>.*?</script>|<style[^>]*>.*?</style>|<[^>]+>', ' ', html, flags=re.DOTALL)
    word_count = len(text.split())
    rows.append({
        'page': name,
        'title': (title.group(1).strip() if title else 'MISSING')[:120],
        'title_len': len(title.group(1).strip()) if title else 0,
        'meta_desc': (desc.group(1).strip() if desc else 'MISSING')[:120],
        'desc_len': len(desc.group(1).strip()) if desc else 0,
        'canonical': canonical.group(1) if canonical else 'MISSING',
        'h1_count': len(h1s),
        'h2_count': len(h2s),
        'word_count': word_count,
        'has_og_title': bool(og_title),
        'has_og_image': bool(og_image),
    })

# Write CSV for the artifact
with open(os.path.join(tmp,'goff-meta-audit.csv'), 'w', encoding='utf-8', newline='') as f:
    w = csv.DictWriter(f, fieldnames=rows[0].keys())
    w.writeheader()
    w.writerows(rows)

# Print summary stats
print(f'Pages audited: {len(rows)}')
print(f'Missing title: {sum(1 for r in rows if r["title"]=="MISSING")}')
print(f'Title >60 chars: {sum(1 for r in rows if r["title_len"]>60)}')
print(f'Title <30 chars: {sum(1 for r in rows if 0<r["title_len"]<30)}')
print(f'Missing meta description: {sum(1 for r in rows if r["meta_desc"]=="MISSING")}')
print(f'Meta desc >160 chars: {sum(1 for r in rows if r["desc_len"]>160)}')
print(f'Meta desc <100 chars: {sum(1 for r in rows if 0<r["desc_len"]<100)}')
print(f'Missing canonical: {sum(1 for r in rows if r["canonical"]=="MISSING")}')
print(f'Multiple H1s: {sum(1 for r in rows if r["h1_count"]>1)}')
print(f'No H1: {sum(1 for r in rows if r["h1_count"]==0)}')
print(f'Word count <500: {sum(1 for r in rows if r["word_count"]<500)}')
print(f'Word count <1500: {sum(1 for r in rows if r["word_count"]<1500)}')
print(f'Median word count: {sorted(r["word_count"] for r in rows)[len(rows)//2]}')
PY
```
Expected: a stats summary. Note any "missing" or out-of-bounds counts — these become remediation items.

**Step 2: Read the CSV and write the artifact**

Use Write to create `recon/goff-law/03-meta-tags-audit.md` with:
```markdown
# Goff Law — Meta Tags & Page Basics Audit

**Crawl date:** 2026-05-10

## Aggregate stats
- Pages audited: N
- Missing `<title>`: N
- Title length out of range (recommend 30-60 chars): N
- Missing meta description: N
- Description out of range (recommend 100-160): N
- Missing canonical URL: N
- Pages with multiple H1s: N
- Pages with no H1: N
- Median word count: N
- Pages with word count <500 (thin content): N

## Per-page issues
{table: page | issue | severity | suggested fix}

## Comparison vs Thompson Law benchmarks
- Thompson Law median word count: ~3,500-6,000 (per Phase 2)
- Goff median word count: {N}
- Thompson Law title pattern: "{City} {Practice} Lawyers | {brand}"
- Goff title pattern observed: {summarize}
```

**Step 3: Verify artifact**

Run:
```
ls -la "recon/goff-law/03-meta-tags-audit.md"
```
Expected: file exists, non-zero size.

---

### Task B4: Audit robots.txt + sitemap health + technical hygiene

**Files:**
- Create: `recon/goff-law/04-technical-hygiene.md`

**Step 1: Inspect robots.txt for issues**

Read `%TEMP%\goff-robots.txt`. Check for:
- Crawl-delay (if >5, that's slowing Google)
- Disallow rules that block important paths
- Sitemap declaration present
- User-agent specificity (should be `*` not blocking common bots)

**Step 2: Test HTTPS + canonicalization**

Run all 4 in parallel:
```
for u in http://gofflawdfw.com/ http://www.gofflawdfw.com/ https://gofflawdfw.com/ https://www.gofflawdfw.com/; do
  echo "=== $u ==="
  curl -sIL --max-time 10 -A "Mozilla/5.0 Chrome/130" -o /dev/null -w "Final URL: %{url_effective}\nHTTP: %{http_code}\nRedirects: %{num_redirects}\n" "$u"
done
```
Expected: All 4 should redirect to a single canonical (`https://www.gofflawdfw.com/` or `https://gofflawdfw.com/`).

**Step 3: Check page response headers (caching, security)**

Run:
```
curl -sI -A "Mozilla/5.0 Chrome/130" https://gofflawdfw.com/ | head -20
```
Look for: `cache-control`, `strict-transport-security`, `content-encoding: gzip|br`, `x-frame-options`, `content-security-policy`. Note presence/absence.

**Step 4: Run a basic Lighthouse-style check via free tool**

Run a WebSearch to fetch a free PageSpeed Insights score:
```
WebSearch: site:pagespeed.web.dev gofflawdfw.com
```
If a recent result exists, note it. Otherwise mark "manual check needed via https://pagespeed.web.dev/?url=https%3A%2F%2Fgofflawdfw.com%2F".

**Step 5: Write the artifact**

Use Write to create `recon/goff-law/04-technical-hygiene.md` with sections:
```markdown
# Goff Law — Technical Hygiene Audit

## robots.txt
- Sitemap declaration: {present/missing}
- Crawl-delay: {value or "none"}
- Disallow blocks affecting SEO: {list}

## HTTPS + canonicalization
| URL | Final | Status | Redirects |
|---|---|---|---|

## Response headers
- HSTS: {yes/no}
- Compression: {gzip/br/none}
- Cache-Control: {value}
- Security headers: {list present}

## Performance signals
- PageSpeed Insights: {score or "manual check needed"}
- Core Web Vitals: {pass/fail/unknown}

## Issues found
1. {issue + impact + fix}
...
```

**Step 6: Verify artifact**

Run:
```
test -s "recon/goff-law/04-technical-hygiene.md" && echo ok
```
Expected: `ok`.

---

## Phase C — Content Inventory & Gap Analysis

### Task C1: Inventory practice areas + geographic coverage

**Files:**
- Create: `recon/goff-law/05-content-inventory.md`

**Step 1: Extract practice areas from URL inventory + page content**

Use the URL inventory from Task A3. Look for URL patterns indicating practice areas: `/practice-areas/`, `/services/`, `/personal-injury/`, `/{practice}-lawyer/`, `/{practice}-attorney/`. Aggregate into a list.

Then cross-reference with H1s extracted in Task B3 for any practice-area H1s not surfaced by URL pattern.

**Step 2: Extract geographic coverage**

Look for URL patterns: `/{city}-personal-injury-lawyer/`, `/dallas/`, `/{city}/`, location subfolders. List every DFW city covered.

Compare against the DFW city list from Phase 1 Thompson Law recon (Plano, Frisco, Allen, McKinney, Arlington, Garland, Mesquite, Irving, Carrollton, Lewisville, Richardson, Grand Prairie, Denton, etc.).

**Step 3: Inventory blog cadence**

Find blog URLs in inventory (`/blog/`, `/news/`, dated URLs). Count total posts. If lastmod data is in the sitemap, compute median posting frequency.

**Step 4: Write the artifact**

Use Write to create `recon/goff-law/05-content-inventory.md`:
```markdown
# Goff Law — Content Inventory

## Practice areas covered
| Practice area | URL | Word count | Schema present? |
|---|---|---|---|

## DFW geographic coverage
| City | Has dedicated page? | Page URL | Word count |
|---|---|---|---|
| Dallas | yes | /... | ... |
| Fort Worth | ... | ... | ... |
| Plano | ... | ... | ... |
{include all major DFW cities — mark missing as "NO"}

## Blog
- Total posts: N
- Most recent post: {date}
- Posts in last 90 days: N
- Topical themes (top 5 from titles): ...
```

**Step 5: Verify artifact**

```
grep -c "^##" "recon/goff-law/05-content-inventory.md"
```
Expected: ≥4.

---

### Task C2: Compute content gaps vs Thompson Law + DFW competitor set

**Files:**
- Create: `recon/goff-law/06-content-gap-analysis.md`

**Step 1: Build the gap matrix**

Use Read to load:
- `recon/goff-law/05-content-inventory.md` (Goff's coverage)
- `recon/thompson-law/PHASE-1-RECON-REPORT.md` (Thompson's practice areas + cities)

Build a side-by-side table. For each practice area Thompson has + each DFW city Thompson has, mark Goff as "✅ Has" / "❌ Missing" / "⚠️ Thin (<500 words)".

**Step 2: Identify "low competition + Goff missing" opportunities**

Cross-reference with the SERP findings from Phase 2 Thompson Law recon — specifically the suburb gaps where Thompson Law doesn't rank top 10. These are the highest-ROI build targets.

Suburb gaps confirmed in Phase 2: **Frisco, Plano, Allen, McKinney**.

**Step 3: Cross-reference with existing Goff workspace docs**

Use Read to load:
- `DFW_Personal_Injury_Keyword_Research.md`
- `goff-law-content-calendar-2025-2026.md`
- `goff-law-dfw-domination-content-calendar.md`

Identify any practice area / city already in the calendar but not yet built on the site. Those are "in-flight" — note them differently.

**Step 4: Write the artifact**

Use Write to create `recon/goff-law/06-content-gap-analysis.md`:
```markdown
# Goff Law — Content Gap Analysis

## Practice-area gap matrix
| Practice area | Thompson Law has | Goff has | Status | Recommended action |
|---|---|---|---|---|

## Geographic gap matrix (DFW)
| City | Thompson EN page | Thompson ES page | Goff page | SERP competition (per Phase 2) | Recommended action |
|---|---|---|---|---|---|
| Frisco | thin/none | yes | {N} | LOW (Snellings dominates) | BUILD |
| Plano | thin/none | yes | {N} | LOW-MED (Vecchio leads) | BUILD |
| Allen | thin/none | yes | {N} | LOW (Hwang/Burress) | BUILD |
| McKinney | thin/none | yes | {N} | LOW (McCraw founded there) | BUILD |
{...continue for all DFW cities...}

## In-flight gaps (in calendar, not yet built)
{list with target date if known}

## Top 10 highest-ROI gap fills
1. {item — practice/city, est. effort, est. impact}
...
```

**Step 5: Verify artifact**

```
grep -c "BUILD\|FILL\|IN-FLIGHT" "recon/goff-law/06-content-gap-analysis.md"
```
Expected: ≥10 (gaps identified).

---

### Task C3: Live SERP positioning check for Goff Law

**Files:**
- Create: `recon/goff-law/07-serp-positioning.md`

**Step 1: Run WebSearch for top commercial-intent queries**

For each of these queries, WebSearch and note where Goff Law appears (or doesn't) in the top 20:
1. `Dallas personal injury lawyer`
2. `Fort Worth personal injury lawyer`
3. `Dallas car accident lawyer`
4. `Dallas truck accident lawyer`
5. `Dallas wrongful death lawyer`
6. `Dallas motorcycle accident lawyer`
7. `Dallas oilfield accident lawyer`
8. `Galaxy Gas injury lawyer` (per existing GSC data showing Goff ranks pos 6-8)
9. `Frisco personal injury lawyer`
10. `Plano personal injury lawyer`

**Step 2: For brand-defense queries also check**

11. `Goff Law` (should be #1 — brand search)
12. `Jim Goff attorney Dallas` (should be #1)

**Step 3: Cross-reference with Goff's GSC data**

Use Read to load `gsc-data/` files. Compare GSC-reported positions against live SERP observations. Flag any ≥10-position discrepancies for investigation (could mean Google personalization, recent re-ranking, or stale GSC data).

**Step 4: Write the artifact**

```markdown
# Goff Law — Live SERP Positioning

**Date:** 2026-05-10

## Commercial-intent queries
| Query | Goff position (live) | GSC reported avg pos | Top 5 organic competitors |
|---|---|---|---|

## Brand queries
| Query | Goff position |
|---|---|

## Discrepancies vs GSC
{list}

## Strategic implications
- Where Goff ranks well already (defend)
- Where Goff is just outside top 10 (push for top 10)
- Where Goff is invisible (ground-up build needed)
```

**Step 5: Verify artifact**

```
grep -c "^| " "recon/goff-law/07-serp-positioning.md"
```
Expected: ≥12 table rows (one per query).

---

## Phase D — Schema Implementation Drafts

### Task D1: Draft JSON-LD blocks for the missing schema types

**Files:**
- Create: `recon/goff-law/08-schema-implementation-guide.md`

**Step 1: Identify firm-level inputs needed**

Before drafting, gather these inputs from the existing crawls + workspace docs:
- Full firm legal name (probably "Goff Law PLLC")
- Address (read homepage crawl)
- Phone number(s)
- Email
- Hours of operation
- Founder/managing partner: Jim Goff
- Bar admission(s)
- Aggregate review count + average rating: get from Google Business Profile (manual check needed) — note "PLACEHOLDER" if unknown

**Step 2: Draft Organization + LegalService schema (sitewide, in `<head>`)**

Write the JSON-LD block as a code example in the artifact. Use real values where known, `{PLACEHOLDER: description}` where unknown.

**Step 3: Draft Attorney schema for Jim Goff**

Same — JSON-LD block with placeholders for any unknown fields (bar admissions, education, areas of practice).

**Step 4: Draft AggregateRating schema**

Note the data source requirement: this MUST come from a real review platform (Google Business Profile reviews are the most defensible). Provide the JSON-LD template + flag that Jim must input the real numbers.

**Step 5: Draft Service schema template (one per practice area)**

Provide a parameterized template the dev can replicate per practice page.

**Step 6: Draft FAQPage schema template**

Parameterized template — dev fills in 5-8 questions per page from existing copy.

**Step 7: Draft Offer schema for free consultation**

JSON-LD block for the consultation offer.

**Step 8: Write the implementation guide artifact**

Use Write to create `recon/goff-law/08-schema-implementation-guide.md`:
```markdown
# Goff Law — Schema Markup Implementation Guide

**Method:** Add these JSON-LD blocks to gofflawdfw.com via WordPress (Yoast SEO custom fields, or theme `<head>` injection, or a plugin like Schema Pro / Rank Math).

## Inputs needed from Jim before deploying
- [ ] Verified Google review count + avg rating
- [ ] Verified Avvo rating
- [ ] Bar admission state(s) and admission year
- [ ] Office address(es)
- [ ] Office hours
- [ ] Practice area list (final)

## Block 1: Sitewide Organization + LegalService (homepage `<head>`)
```json
{ ... }
```
**Where to deploy:** homepage `<head>`. **Validation:** https://validator.schema.org/

## Block 2: Attorney schema (each attorney bio page)
```json
{ ... }
```

## Block 3: AggregateRating (homepage + key landing pages)
```json
{ ... }
```

## Block 4: Service schema template (one per practice area)
```json
{ ... }
```

## Block 5: FAQPage schema template
```json
{ ... }
```

## Block 6: Offer schema for free consultation
```json
{ ... }
```

## Deployment checklist
- [ ] Validate each block at validator.schema.org
- [ ] Test in Google Rich Results Test
- [ ] Deploy to staging first if possible
- [ ] Submit updated sitemap to Search Console
- [ ] Re-crawl with this audit method in 30 days to confirm
```

**Step 9: Verify artifact**

```
grep -c '```json' "recon/goff-law/08-schema-implementation-guide.md"
```
Expected: ≥6 JSON blocks.

---

## Phase E — On-Page Optimization Quick Wins

### Task E1: Compile on-page quick-win checklist

**Files:**
- Create: `recon/goff-law/09-on-page-quick-wins.md`

**Step 1: Aggregate the quick-win opportunities from prior audits**

Use Read on:
- `recon/goff-law/02-schema-audit.md` (schema gaps)
- `recon/goff-law/03-meta-tags-audit.md` (meta gaps)
- `recon/goff-law/04-technical-hygiene.md` (technical gaps)
- `recon/goff-law/06-content-gap-analysis.md` (content gaps)

Tag each item by effort (S = <1hr, M = 1-4hr, L = 1-3 days, XL = weeks) and impact (low/med/high).

**Step 2: Build the quick-win table (only S/M items with med/high impact)**

Filter the aggregated list to "S or M effort" + "med or high impact". These are the "do this week" items.

**Step 3: Write the artifact**

```markdown
# Goff Law — On-Page Quick Wins (this week)

## Schema-related (8 hours total)
| Item | Page(s) | Effort | Impact | Source artifact |
|---|---|---|---|---|

## Meta-tag fixes (3 hours total)
| Item | Page(s) | Effort | Impact | Source artifact |
|---|---|---|---|---|

## Technical hygiene fixes (2 hours total)
| Item | Pages | Effort | Impact | Source artifact |
|---|---|---|---|---|

## Total quick-win effort: {sum} hours
## Total quick-win opportunities: {count}
```

**Step 4: Verify artifact**

```
grep -c "^| " "recon/goff-law/09-on-page-quick-wins.md"
```
Expected: ≥10 actionable items.

---

## Phase F — Roadmap Synthesis

### Task F1: Prioritize all remediation items into the executive roadmap

**Files:**
- Create: `recon/goff-law/10-prioritized-roadmap.md`

**Step 1: Aggregate every recommendation from prior artifacts**

Read all 9 prior artifacts and pull every "recommended action" / "fix" / "build" item into a master list with: item description, source artifact, effort estimate, impact estimate, recommended owner (you / web dev / content writer / paid tool subscription).

**Step 2: Tier the items**

- **Tier 0: Immediate (this week)** — All quick wins from `09-on-page-quick-wins.md`
- **Tier 1: 30-day (next month)** — Schema deploy, top 3 suburb pages built (Frisco/Plano/McKinney), AggregateRating activation
- **Tier 2: 90-day (next quarter)** — Remaining suburb pages, content gap fills, Phase 1 recon vs Mullen & Mullen / Witherite / suburb specialists
- **Tier 3: Strategic (6-12 months)** — Spanish-language coverage, blog content moat, review-collection program

**Step 3: For each tier, estimate cost + projected impact**

Pull cost benchmarks from existing workspace doc `goff-law-executive-report-coo.md` ($55K-100K/mo budget context). Allocate Tier 0 → essentially free (Claude + Jim's time). Tier 1 → low ($500-2K dev). Tier 2-3 → real budget allocation.

**Step 4: Write the executive-ready roadmap**

```markdown
# Goff Law — SEO Audit & Prioritized Remediation Roadmap

**Date:** 2026-05-10
**Scope:** Full-site SEO audit + competitor benchmarking + prioritized fix roadmap
**Method:** See `recon/goff-law/01-09-*.md` artifacts for raw audit data
**Companion to:** Phase 1 + Phase 2 Thompson Law recon

## Executive summary (3 bullets)
- {finding 1: biggest issue}
- {finding 2: biggest opportunity}
- {finding 3: biggest competitive insight}

## Tier 0 — This week (effort: {N} hours)
| Item | Effort | Impact | Owner | Source |
|---|---|---|---|---|

## Tier 1 — 30 days (cost: $X)
| Item | Effort | Impact | Owner | Source |
|---|---|---|---|---|

## Tier 2 — 90 days (cost: $X)
| Item | Effort | Impact | Owner | Source |
|---|---|---|---|---|

## Tier 3 — 6-12 months (cost: $X, fits the $55-100K/mo budget)
| Item | Effort | Impact | Owner | Source |
|---|---|---|---|---|

## Projected cumulative impact
- 30 days: {expected SERP movement, schema rich-result wins}
- 90 days: {expected organic traffic lift, suburb visibility}
- 12 months: {expected DFW market share movement}

## Open questions for the COO briefing
1. ...
2. ...

## Linked artifacts
- [URL inventory](01-url-inventory.md)
- [Schema audit](02-schema-audit.md)
- [Meta tags audit](03-meta-tags-audit.md)
- [Technical hygiene](04-technical-hygiene.md)
- [Content inventory](05-content-inventory.md)
- [Content gap analysis](06-content-gap-analysis.md)
- [SERP positioning](07-serp-positioning.md)
- [Schema implementation guide](08-schema-implementation-guide.md)
- [On-page quick wins](09-on-page-quick-wins.md)
```

**Step 5: Verify the roadmap is complete**

```
test -s "recon/goff-law/10-prioritized-roadmap.md" && grep -c "^## Tier" "recon/goff-law/10-prioritized-roadmap.md"
```
Expected: 4 (one for each Tier 0-3).

---

### Task F2: Update workspace memory + index

**Files:**
- Modify: `C:\Users\jim\.claude\projects\c--Users-jim-OneDrive-Documents-ArnoldItkin\memory\MEMORY.md`
- Create: `C:\Users\jim\.claude\projects\c--Users-jim-OneDrive-Documents-ArnoldItkin\memory\reference_goff_law_audit.md`

**Step 1: Write a reference memory file pointing future sessions to the audit**

Use Write to create `memory/reference_goff_law_audit.md`:
```markdown
---
name: Reference — Goff Law SEO audit (2026-05-10)
description: Full audit of gofflawdfw.com with prioritized remediation roadmap; canonical source for "what's wrong with our site and what to do about it"
type: reference
---

The full audit lives at `recon/goff-law/`:
- 01-url-inventory.md
- 02-schema-audit.md
- 03-meta-tags-audit.md
- 04-technical-hygiene.md
- 05-content-inventory.md
- 06-content-gap-analysis.md
- 07-serp-positioning.md
- 08-schema-implementation-guide.md
- 09-on-page-quick-wins.md
- **10-prioritized-roadmap.md** ← executive-ready summary

Re-run the audit method any time via the plan at `docs/plans/2026-05-10-goff-law-full-seo-audit.md`.
```

**Step 2: Add the index entry to MEMORY.md**

Use Edit to append a line to `memory/MEMORY.md`:
```
- [Reference — Goff Law SEO audit (2026-05-10)](reference_goff_law_audit.md) — comprehensive site audit + roadmap at recon/goff-law/10-prioritized-roadmap.md
```

**Step 3: Verify memory is updated**

```
grep -c "goff-law-audit\|Goff Law SEO audit" "C:\Users\jim\.claude\projects\c--Users-jim-OneDrive-Documents-ArnoldItkin\memory\MEMORY.md"
```
Expected: 1.

---

### Task F3: Hand back to Jim with a one-message summary

**Step 1: Print a brief end-of-execution summary to chat**

Tell Jim:
- Total artifacts produced: 10 markdown files in `recon/goff-law/`
- Total findings: N issues identified, M opportunities
- Tier 0 (this week) effort: N hours
- Top 3 next moves
- Whether any input was needed from him (review counts, bar admissions, etc.)

No file write needed for this step — it's a chat message only.

---

## Notes for the executor

### Skills to reference at runtime
- @superpowers:systematic-debugging — if any crawl or audit step produces unexpected results
- @superpowers:verification-before-completion — before claiming Tier 0 fixes are deployed
- @seo-audit — for any deeper technical SEO methodology questions
- @schema-markup — for JSON-LD validation and best practices

### Failure modes to watch for
1. **Goff site bot-blocks Crawl4AI** — fall back to direct curl with browser User-Agent (per the Thompson Law site fix in Phase 1).
2. **Sitemap returns HTML 404 page** — try multiple sitemap URLs (`/sitemap.xml`, `/sitemap_index.xml`, `/sitemap1.xml`, check robots.txt).
3. **Crawl4AI `/html` endpoint strips `<head>`** — known bug. Always use direct curl for raw HTML when auditing schema or meta tags.
4. **Free PageSpeed Insights data unavailable** — note as "manual check required" rather than blocking.
5. **GSC data files are large/binary** — sample with `head` first, don't try to load the whole thing into memory.

### What NOT to do
- Do NOT email anyone, post to Slack, or share artifacts externally.
- Do NOT commit anything (workspace is not a git repo).
- Do NOT modify the live gofflawdfw.com site. Audit-only.
- Do NOT re-run Phase 1/Phase 2 work on Thompson Law — it's already done at `recon/thompson-law/`.
- Do NOT make up numbers. If a metric isn't measurable with available tools, write "MANUAL CHECK NEEDED" and move on.

### Estimated total runtime
- Phase A (setup + discovery): 5-15 min
- Phase B (technical audit): 20-40 min
- Phase C (content audit + SERP): 15-30 min
- Phase D (schema drafts): 15-25 min
- Phase E (quick wins): 10-15 min
- Phase F (synthesis): 15-25 min
- **Total: 80-150 minutes**
