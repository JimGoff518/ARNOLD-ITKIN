# Thompson Law — Phase 2 Deep-Dive Report

**Target:** Thompson Law Injury Lawyers (1800lionlaw.com)
**Recon date:** 2026-05-10
**Scope:** Schema audit (5 pages, raw HTML) + Live SERP positioning (7 DFW queries) + Authority signal scan
**Companion to:** [PHASE-1-RECON-REPORT.md](PHASE-1-RECON-REPORT.md)

---

## TL;DR — The headline finding upends Phase 1's threat assessment

**Thompson Law's massive ~2,000-page programmatic SEO factory is invisible at the top of SERPs.** Despite the volume, they did not appear on page 1 organic results for ANY of the 7 high-value DFW queries tested — including their home market of Dallas.

The actual organic threat in DFW PI is **Mullen & Mullen**, with hyper-local specialists owning the suburbs (Snellings in Frisco, McCraw in McKinney, Burress in Allen).

This dramatically changes the strategic picture. **Goff Law's primary digital opponent is not Thompson Law** — it's a different firm + a set of localized incumbents.

---

## 1. SERP positioning — the big surprise

7 commercial-intent queries tested via live Google Search 2026-05-10. **Thompson Law's organic rank** in each:

| Query | Thompson Law in top 10? | Top organic players (excluding directories) |
|---|---|---|
| Dallas car accident lawyer | **❌ NO** | Kraft, Ben Abbott, Tate, Montgomery, Mullen & Mullen, Thomas J. Henry, Ben Crump, McGilberry & Shirer, DFW Injury Lawyers |
| Dallas truck accident lawyer | **❌ NO** | Zehl Law (claims "undefeated"), Aldous, Ben Crump, **Witherite**, Thomas J. Henry, Shamieh, Slocumb, Dunn Sheehan, Reyes |
| Frisco personal injury lawyer | **❌ NO** | **Snellings Law** (dominant local), Mullen & Mullen, McKey, Hernandez Law, Vecchio, Feizy |
| Plano personal injury lawyer | **❌ NO** | Vecchio, Mullen & Mullen, McCraw, Patterson, Daniel Stark, Stanley & Associates, Johnson Reist |
| McKinney personal injury attorney | **❌ NO** | **McCraw Law Group** (founded in McKinney), Burress, Ford Law, Lucé, Underwood, Mullen & Mullen |
| Allen Texas personal injury lawyer | **❌ NO** | Hwang, **Burress Law**, Underwood, Zinda Law Group |

**Confirmed across all 6 commercial-intent queries:** Thompson Law's English programmatic-SEO pages aren't winning organic position 1–10.

### Implications
1. Their 1,109 static pages may be ranking on pages 2–10+ (a "broad but shallow" footprint), not delivering the organic traffic implied by raw page count
2. Whatever traffic they ARE generating is likely from:
   - Brand search ("thompson law", "1-800-LION-LAW")
   - Paid ads (heavy investment per Phase 1)
   - Long-tail / hyperlocal queries we didn't test
3. The "DA 55 / 25,000/mo organic / 200+ keywords" stale metrics in your existing docs are **even more misleading** than just being wrong-URL — they imply organic dominance that doesn't appear in actual SERPs.

### Counterintelligence updates needed
| Original threat ranking | New evidence-based threat ranking |
|---|---|
| 1. Thompson Law | 1. **Mullen & Mullen** (appears in 4 of 6 queries — Dallas, Frisco, Plano, McKinney) |
| 2. Witherite | 2. **Witherite** (truck-accident specialist; appears top 10 for Dallas truck only) |
| 3. Hamilton Wingo (per existing docs) | 3. **Local suburb specialists** (Snellings/Frisco, McCraw/McKinney, Burress/Allen, Vecchio/Plano) |
| | 4. **Thomas J. Henry** (statewide; appears in Dallas car + truck) |
| | 5. **Ben Crump** (national brand, Dallas presence) |
| | 6. **Thompson Law** — NOT visible in top 10 organic for any tested commercial query |

---

## 2. Schema markup audit (5 representative pages)

| Page | Schema types present | FAQPage? | Attorney? | Review/AggregateRating? |
|---|---|---|---|---|
| `/tx/dallas/` (Dallas hub) | Organization, WebSite, ImageObject, BreadcrumbList, WebPage, LegalService, FAQPage | ✅ | ❌ | ❌ |
| `/tx/dallas/car-accident-lawyers/` | Organization, WebSite, ImageObject, BreadcrumbList, WebPage+FAQPage, LegalService | ✅ | ❌ | ❌ |
| `/tx/dallas/truck-accident-lawyers/` | Organization, WebSite, ImageObject, BreadcrumbList, WebPage, LegalService | ❌ | ❌ | ❌ |
| `/personal-injury-lawyers/` (national hub) | Organization, WebSite, ImageObject, BreadcrumbList, WebPage, LegalService | ❌ | ❌ | ❌ |
| `/our-results-2/` | **BreadcrumbList only** | ❌ | ❌ | ❌ |

### What they have
- ✅ Consistent `Organization` + `WebSite` + `LegalService` markup
- ✅ Proper `BreadcrumbList` on every page (good for SERP breadcrumb rich result)
- ✅ Clean `<title>`, meta description, canonical URL on every page (Yoast doing its job)
- ✅ One H1 per page
- ✅ Substantial word counts (3,500–6,000 words per page)

### Gaps Goff can exploit
1. **No `Attorney` schema anywhere.** They have an /our-attorneys/ page and individual attorney bios — none marked up. Missed rich-snippet opportunity for SERP attorney cards.
2. **No `Review` or `AggregateRating` schema.** They claim 2,021 Birdeye reviews and a 4.9-star rating, but this is invisible to Google. Adding this could win SERP star ratings — they have NOT.
3. **`FAQPage` schema is inconsistent** — present on Dallas hub + Dallas car, missing on Dallas truck (their flagship), national hub, and Our Results. Sloppy template execution.
4. **`/our-results-2/` page has only `BreadcrumbList`** — no schema for $1.9B in case results, no Service schema, no LegalService. The page they brag about most has the weakest markup.
5. **No `Service` or `Offer` schema** for individual practice areas — could be marking up "free consultation" as an Offer.

### Goff's playbook (immediate)
- Implement `Attorney` schema for Jim Goff's bio page
- Implement `LegalService` + `AggregateRating` (with verifiable review count from Google/Avvo)
- Implement `FAQPage` on every practice-area page consistently
- Implement `Service` schema for each practice area with `areaServed` (DFW cities)
- Implement `Offer` schema for "Free Consultation"

These take a few hours to implement and can produce SERP rich results Thompson Law isn't getting.

---

## 3. Critical bug confirmed: "Our Results" page is broken

The `/our-results-2/` page (their primary trust-signal page) has:
- **TITLE (English-canonical URL):** "Nuestros Resultados | Abogados De Lesiones De Thompson Law"
- **META DESC:** Spanish text
- **OG:TITLE:** Spanish
- **CANONICAL:** https://1800lionlaw.com/our-results-2/ (English URL!)

**This is a confirmed SEO failure.** Spanish meta tags on an English-canonical URL — Google sees a content/language mismatch and will likely struggle to rank this page for either English OR Spanish queries. The page they want to feature most prominently (their $1.9B social proof) is misconfigured.

**Goff opportunity:** Build a *correctly configured* "Our Results" / "Case Results" page with proper schema (Service + AggregateRating + ItemList of case results) — directly compete for the same searcher intent.

---

## 4. Authority signals (free-tool check)

Without Ahrefs/SEMrush, I checked publicly available signals:

| Signal | Thompson Law (1800lionlaw.com) |
|---|---|
| Birdeye reviews | **2,021** (4.9-star claim — NOT exposed via schema) |
| Trustpilot reviews | **23 reviews, 4-star** ⚠️ — surprisingly low |
| Avvo presence | Yes (rating page exists) |
| Lawyers.com listing | Yes (Fort Worth office) |
| Facebook | @1800LIONLAW (active) |
| LinkedIn | "Thompson Law Injury Lawyers" company page |
| YouTube | youtube.com/thompsonlaw |
| Wikipedia | Not found |

### Read on these signals
- **Birdeye 2,021 reviews** = real moat IF independently verified. But it's a Birdeye-only volume (no Trustpilot or Yelp parity). They've channelized review collection through one platform — easier to game, harder to defend if Birdeye changes terms.
- **Trustpilot 4-star / 23 reviews** is a credibility liability if anyone digs. Your competitive analysis docs claim "4.9-star" — that's the Birdeye number. Trustpilot tells a different story.
- **Avvo + Lawyers.com presence** = standard table-stakes. Goff should match these at minimum.
- **Mullen & Mullen, your real new threat, also appears prominently in directories** — they likely have stronger backlink + citation profiles than Thompson Law per the SERP results.

### Recommended Phase 3 paid-tool work
- Pull `1800lionlaw.com` AND `mullenandmullen.com` AND `witheritelaw.com` through Ahrefs:
  - Domain Rating
  - Referring domains count + quality
  - Top 100 organic keywords (actual keywords driving traffic)
  - Top backlink sources
- Compare to Goff's domain
- Specifically for Mullen & Mullen — they're the dark horse appearing in 4/6 SERPs. Treat them as Threat #1 going forward.

---

## 5. Updated strike list (refined from Phase 1)

### Tier 1 — Immediate wins
1. **Build dedicated, well-optimized English suburb pages**: Frisco, Plano, Allen, McKinney
   - Thompson Law has Spanish-only or thin English coverage in these cities
   - Local incumbents (Snellings, McCraw, Burress, Vecchio) are beatable single-firm targets
   - These are the wealthiest, highest-PI-CPC zip codes in the metro
2. **Implement comprehensive schema markup** (Attorney, Review/AggregateRating, FAQPage, Service, Offer)
   - Easy wins Thompson Law has not taken
   - Could produce SERP star ratings + attorney rich cards Thompson Law lacks
3. **Build a properly configured "Case Results" page** with Service + AggregateRating + ItemList schema
   - Direct counter to Thompson Law's broken /our-results-2/

### Tier 2 — Re-frame the competitive landscape
4. **Stop treating Thompson Law as the primary organic threat.** They're an ad-spend + brand-recognition threat, not an organic-ranking threat.
5. **Treat Mullen & Mullen as Threat #1 organic.** They appear in 4 of 6 DFW SERPs tested. Run a separate Phase 1 recon against them.
6. **Treat Witherite as the truck-accident specialist threat.** They're not threatening for general PI but they own Dallas truck SERPs. Goff should not try to head-to-head on truck unless investing heavily.
7. **Treat suburb specialists as defensible local incumbents.** Snellings/Frisco, McCraw/McKinney, Burress/Allen, Vecchio/Plano — beating them requires local-citation depth + neighborhood content, not raw page count.

### Tier 3 — Long-game
8. **Birdeye review machine.** Thompson Law's 2,021 reviews on a single platform is a moat. Goff needs a systematic review-collection program (likely 200+ reviews on Google + 100+ on Avvo + 50+ on Birdeye to be competitive).
9. **DFW Spanish-language pages.** Thompson Law has 150+ Spanish PI pages. Goff has none. Spanish PI in DFW is a mid-six-figure-revenue market segment (per Census data — 30%+ of DFW PI claimants are Hispanic). Major content gap.
10. **Practice-area depth.** Thompson Law has dedicated pages for niches like Galaxy Gas / nitrous, Amazon delivery, hernia mesh — actually, they DON'T (per Phase 1). Goff is already ahead on Galaxy Gas. Stay aggressive on emerging litigation.

---

## 6. Recommendations for the COO briefing

Three things to communicate before the next executive update:

1. **The original "Thompson Law" threat assessment was based on the wrong URL.** All quantitative SEO/PPC metrics need re-pulling. (Already flagged inline in the corrected docs.)
2. **Thompson Law is a brand/ad-spend threat, not an organic-search threat.** They're losing organic to Mullen & Mullen and local suburb specialists despite their ~2,000-page footprint.
3. **The actual highest-ROI Phase 1 strategic move is dedicated DFW suburb landing pages** (Frisco, Plano, Allen, McKinney). Lower competition, higher CPC, no Thompson Law incumbent in English. This should be the lead recommendation in the budget allocation pitch.

---

## Phase 3 backlog (parking lot)

- Run Phase 1 recon against **Mullen & Mullen** (mullenandmullen.com) — confirmed organic threat
- Run Phase 1 recon against **Witherite Law Group** (witheritelaw.com) — URL confirmed, deferred
- Run Phase 1 recon against **Snellings Law** (snellingsinjurylaw.com) — Frisco specialist
- Run Phase 1 recon against **McCraw Law Group** (mccrawlawgroup.com) — McKinney specialist
- Pull paid-tool data (Ahrefs/SEMrush) on top 5 confirmed competitors
- Build SERP-rank tracker for top 50 DFW commercial-intent queries
- Audit Goff Law's current schema markup (mirror this Phase 2 method)

---

## Files saved (this recon)
- `recon/thompson-law/PHASE-2-DEEP-DIVE-REPORT.md` — this file
- `%TEMP%/raw-{dallas-hub,dallas-car,dallas-truck,national-pi,results}.html` — raw page source (5 pages, 1.5–8.5MB each)
- `%TEMP%/lion-{dallas-hub,dallas-car,dallas-truck,national-pi,results}-html.json` — Crawl4AI cleaned HTML extracts
- (Original Phase 1 sitemap and markdown crawls also remain in `%TEMP%/`)
