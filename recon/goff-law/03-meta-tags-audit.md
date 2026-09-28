# Goff Law — Meta Tags & Page Basics Audit

**Crawl date:** 2026-05-11
**Pages audited:** 74

## TL;DR — three findings that matter most

1. **🚨 48 of 74 pages (65%) have MULTIPLE H1 tags.** This is a serious SEO bug — WordPress theme is emitting both the site title AND the page title as `<h1>`. Google guidelines say one H1 per page.
2. **🚨 52 of 74 pages (70%) have NO `og:image`** — social sharing previews on Facebook/LinkedIn/X show no thumbnail. Massive missed organic-social CTR opportunity.
3. **⚠️ Median page word count is 1,455** — vs Thompson Law's 3,500-6,000 word benchmark. Goff is roughly 1/3 as deep per page. 42 pages are under 1,500 words; 3 pages are under 500 words.

---

## Aggregate stats

| Metric | Value | Notes |
|---|---|---|
| Pages audited | 74 | |
| Missing `<title>` | 0 | ✅ |
| Title length out of range (recommend 30-60 chars) | 7 | 5 too long, 2 too short |
| Missing meta description | 8 | ❌ Mostly Dallas-PI subfolder pages |
| Meta desc length > 160 chars (gets truncated) | 40 | ⚠️ More than half |
| Meta desc length < 100 chars (under-utilized) | 0 | ✅ |
| Missing canonical URL | 0 | ✅ Yoast handles this |
| Pages with MULTIPLE H1s | 48 | ❌ **65% of site** |
| Pages with NO H1 | 0 | ✅ |
| No `og:image` | 52 | ❌ **70% of pages** |
| Median word count | 1,455 | ⚠️ Below competitive benchmark |
| Average word count | 1,450 | |
| Word count range | 341 - 2,244 | |
| Pages under 500 words (very thin) | 3 | ❌ |
| Pages under 1,500 words (thin vs competitor benchmark) | 42 | ⚠️ |

---

## Critical issues

### 🚨 P0 — Multi-H1 on 65% of pages

**The bug:** Most Goff pages have **2 or 3 `<h1>` tags** instead of one. WordPress theme is emitting both site title AND page title as `<h1>`.

**H1 count distribution:**
- 1 H1 (correct): 26 pages
- 2 H1s: 44 pages
- 3 H1s: 4 pages

**Sample affected pages:**
- `cedar-hill-personal-injury-lawyer`
- `cedar-hill_car-accident-lawyer`
- `cedar-hill_car-accident-lawyer_rideshare-accident-lawyer`
- (... and 45 more)

**Why it matters:** Google explicitly says one H1 per page. Multiple H1s confuse topical signal and can dilute ranking. SEMrush / Ahrefs flag this as a critical error.

**Action:** WordPress theme audit. Likely the theme is wrapping the site logo/header in `<h1>` while ALSO emitting the page H1 in the content area. Standard fix: change theme so site title becomes `<a>` or `<div>` and only the page-level H1 remains.

**Effort:** S (1-3 hours theme tweak, by your WP dev).
**Impact:** HIGH for SEO clarity.

### 🚨 P0 — 70% of pages lack og:image

**The bug:** 52 of 74 pages have no `og:image` meta tag, meaning Facebook / LinkedIn / X / Slack previews show a blank thumbnail when someone shares the URL.

**Why it matters:** Social-shared links without thumbnails get ~5-10x lower CTR than those with images. This affects organic social referrals AND any time a journalist, lawyer, or potential client shares a Goff page.

**Action:** Two paths:
1. Use Yoast SEO's "Social" tab to set a default share image per page (manual but reliable)
2. Configure Yoast site-wide default share image (fastest fix — covers all pages automatically)

**Effort:** S (30 min for site-wide default; M for per-page customization).
**Impact:** MED-HIGH for organic social CTR.

### 🟧 P1 — 8 pages missing meta description

**Specifically missing:**
- `dallas-personal-injury-lawyer` (the main Dallas hub!)
- `dallas-personal-injury-lawyer/catastrophic-injury`
- `dallas-personal-injury-lawyer/catastrophic-injury/spinal-cord-injury-attorney`
- `dallas-personal-injury-lawyer/medical-malpractice`
- `dallas-personal-injury-lawyer/nursing-home-abuse`
- `dallas-personal-injury-lawyer/premises-liability`
- `dallas_car-accident-lawyer/rideshare-accident-lawyer/dallas-lyft-attorney`
- `dallas_car-accident-lawyer/rideshare-accident-lawyer/uber-accident`

**Why it matters:** When meta desc is missing, Google auto-generates one from page content — usually less compelling than a hand-written one. CTR suffers.

**Action:** Write a 120-155 char meta description for each of these 8 pages via Yoast. Should include city + practice area + CTA.

**Effort:** S (15-30 min for all 8).
**Impact:** MED — better SERP click-through.

### 🟧 P1 — 40 pages have descriptions > 160 chars (get truncated in SERP)

Google's SERP descriptions are truncated around 155-160 chars on desktop, 120 chars on mobile. Over half of Goff pages have meta descs that overflow.

**Action:** Audit + rewrite the 40 long descriptions to 120-155 chars. Could be done in batch via Yoast bulk editor or programmatically.

**Effort:** M (2-3 hours).
**Impact:** LOW-MED — reduces truncation, slightly better SERP appearance.

### 🟧 P1 — Thin content on 42 of 74 pages

Pages under 1,500 words. Below the competitive benchmark (Thompson Law's median is 3,500-6,000).

**Especially thin (under 500 words):**
- `east-texas` (location hub)
- `houston` (location hub)
- `legal-services` (services hub)

These three are **HUB pages** — they should be the longest and most comprehensive, not the thinnest. Major opportunity.

**Action:** Content audit + expansion. Hub pages should have 2,500-4,000 words. Practice area pages should have 1,500-3,000 words. Blog posts can be 1,000-2,500 depending on topic.

**Effort:** L (1-3 days per major hub page rewrite, by a content writer).
**Impact:** HIGH — directly affects topical authority and SERP ranking.

---

## Title pattern analysis

Goff uses a consistent format: `{City} {Practice} Lawyer - Goff Law` or `Dallas, TX {Topic} | Subtitle`.

**Examples:**
- "Cedar Hill Personal Injury Lawyer - Goff Law" (45 chars ✓)
- "Cedar Hill Car Accident Lawyer - Goff Law" (42 chars ✓)
- "Cedar Hill Galaxy Gas Lawyer - Goff Law" (39 chars ✓)
- "Dallas, TX Brain Injury Lawsuit | Key Factors to Consider" (57 chars ✓)

**Comparison to Thompson Law:** Thompson uses "{City} {Practice} Lawyers | Free Consultations" or "{City} {Practice} Lawyer – No Fee Unless We Win" — heavier on CTAs in the title itself.

**Suggestion:** Consider adding a CTA hook to Goff titles ("Free Consultation", "Trusted Local Lawyer", "Free Case Review") to match competitor SERP appeal. But not critical — current titles are clean and clear.

---

## Comparison vs Thompson Law benchmark

| Metric | Thompson Law (per Phase 2) | Goff Law (this audit) |
|---|---|---|
| Median word count | 3,500-6,000 | 1,455 ⚠️ |
| Title structure | Consistent | Consistent ✓ |
| Meta desc consistency | Yoast-managed, well-tuned | Yoast-managed but 40 are too long |
| H1 hygiene | 1 per page | 48 pages have 2-3 H1s ❌ |
| og:image | Present | Missing on 70% of pages ❌ |

---

## Recommendations summary

| Priority | Item | Effort | Impact |
|---|---|---|---|
| P0 | Fix multi-H1 issue (WordPress theme) | S (1-3 hr dev) | HIGH |
| P0 | Add Yoast site-wide default og:image | S (30 min) | MED-HIGH |
| P1 | Write meta descriptions for 8 missing pages | S (30 min) | MED |
| P1 | Trim 40 oversized meta descriptions to ≤155 chars | M (2-3 hr) | LOW-MED |
| P1 | Expand thin hub pages (east-texas, houston, legal-services) | L (1-3 days per page) | HIGH |
| P2 | Add CTA hook to title pattern | M (across 74 pages) | LOW |

**Total P0+P1 quick-win effort:** ~5-7 hours of dev/content time (excluding the major hub page rewrites).

---

## Raw audit data

- Full per-page CSV: `%TEMP%\goff-meta-audit.json`
- Summary stats: `%TEMP%\goff-meta-stats.json`
