# Goff Law — On-Page Quick Wins (this week)

**Date:** 2026-05-11
**Filtered from:** All Phase B + C audits (schema, meta tags, technical hygiene, content gap, SERP positioning)
**Criteria:** S (under 1 hour) or M (1-4 hours) effort × medium-or-high impact items

## TL;DR

There are **~15 hours of mostly-mechanical work** that would meaningfully improve Goff's SEO foundation. Most can be done by your WordPress dev in a single workday. The biggest single move is fixing the **multi-H1 theme bug** affecting 65% of pages.

---

## Schema-related (12-16 hours total)

| # | Item | Page(s) | Effort | Impact | Source |
|---|---|---|---|---|---|
| 1 | Add sitewide `LegalService` schema (Block 1 from implementation guide) | All pages via `<head>` | S (1 hr) | HIGH | `02-schema-audit.md` |
| 2 | Add `AggregateRating` + 3-5 `Review` blocks on homepage | Homepage only | S (1-2 hr, depends on review data gathering) | HIGH | `02-schema-audit.md` |
| 3 | Add `Attorney` schema for Jim Goff bio page | 1 page | S (1-2 hr) | MED | `02-schema-audit.md` |
| 4 | Add `Service` schema to top 5 practice-area pages (start with car, truck, wrongful death, premises liability, Galaxy Gas) | 5 pages | M (2-3 hr) | MED-HIGH | `08-schema-implementation-guide.md` |
| 5 | Add `FAQPage` schema to top 5 practice pages (lift Q/A from existing content) | 5 pages | M (4-6 hr, mostly Q/A writing) | HIGH | `02-schema-audit.md` |
| 6 | Add `Offer` schema for free consultation | Homepage + /contact | S (30 min) | LOW-MED | `08-schema-implementation-guide.md` |

**Subtotal: 10-15 hours.**

⚠️ **Blockers before deploying schema:**
- Need verified Google review count + average rating from Jim
- Need Jim Goff's bar admission year + law school + photo URL
- Need final office hours
- Need social media URLs (Facebook, LinkedIn, X)

---

## Meta-tag fixes (2-4 hours total)

| # | Item | Page(s) | Effort | Impact | Source |
|---|---|---|---|---|---|
| 7 | Add Yoast site-wide default `og:image` (covers 52 pages missing one) | Yoast settings | S (30 min) | MED-HIGH | `03-meta-tags-audit.md` |
| 8 | Write meta descriptions for 8 pages missing them (including Dallas PI hub) | 8 pages | S (30-45 min) | MED | `03-meta-tags-audit.md` |
| 9 | Trim 40 oversized meta descriptions to ≤155 chars | 40 pages | M (2 hr) | LOW-MED | `03-meta-tags-audit.md` |

**Subtotal: 3-3.5 hours.**

---

## Technical hygiene fixes (1-3 hours total)

| # | Item | Pages | Effort | Impact | Source |
|---|---|---|---|---|---|
| 10 | **🚨 Fix multi-H1 issue** affecting 48 of 74 pages — WordPress theme is wrapping site title in `<h1>` in addition to page H1 | Theme template (likely `header.php`) | M (1-3 hr theme tweak) | **HIGH** | `03-meta-tags-audit.md` |
| 11 | Configure W3 Total Cache to set sensible `Cache-Control: max-age` on HTML (e.g., 5 min) instead of `max-age=0` | Server config | S (30 min) | MED (perf) | `04-technical-hygiene.md` |
| 12 | (If you subscribe to DataForSEO) — Remove `DataForSeoBot Disallow` from robots.txt | robots.txt | S (5 min) | LOW (only relevant if DataForSEO subscribed) | `04-technical-hygiene.md` |

**Subtotal: 1.5-3.5 hours.**

---

## Content micro-fixes (variable effort)

| # | Item | Page(s) | Effort | Impact | Source |
|---|---|---|---|---|---|
| 13 | Expand 3 very-thin (<500 word) pages: `/east-texas/`, `/houston/`, `/legal-services/` | 3 hub pages | L (1-2 days per page, content writer work) | HIGH (these are hub pages for whole sections) | `03-meta-tags-audit.md` |
| 14 | Add 1-2 sentences of LSI-keyword content to single-page mass tort verticals: Nursing Home Abuse, Medical Malpractice, Hair Relaxer, Suboxone, Video Game Addiction | 5 pages | M (3-4 hr writer time) | MED (positions Goff for emerging searches) | `06-content-gap-analysis.md` |

**Subtotal: variable — exclude from "this week" if no writer bandwidth.**

---

## Optional polish (deprioritize if time-constrained)

| # | Item | Effort | Impact |
|---|---|---|---|
| Add Content-Security-Policy header in report-only mode | M-L | LOW-MED (security posture) |
| Add Permissions-Policy header | S | LOW |
| Collapse `http://www` 2-hop redirect to 1 hop | S | LOW |
| Add `loading="lazy"` to below-the-fold images (per UX recon) | M (theme work) | MED (perf + mobile Core Web Vitals) |

---

## Total quick-win effort: ~15-20 hours

**Top 5 in priority order:**
1. **Fix multi-H1 theme bug** (3 hours, HIGH impact, affects 65% of pages)
2. **Deploy sitewide LegalService schema** (1 hour, HIGH impact, sitewide)
3. **Add AggregateRating + 3-5 Reviews** (2 hours assuming you have review data)
4. **Add Yoast default og:image** (30 minutes, affects 70% of pages' social shares)
5. **Add FAQPage schema to top 5 practice pages** (6 hours, drives expandable SERP snippets)

If you only have 1 day of dev time, do #1-#4 first. The FAQPage one (#5) is a content-writer ask, not dev.

---

## Verification after deployment

Re-run this audit (Tasks B2, B3, B4 from `docs/plans/2026-05-10-goff-law-full-seo-audit.md`) 30 days after deploying changes. Expected improvements:

- Schema audit: `LegalService` jumps from 0 to 74 pages. `AggregateRating`, `FAQPage`, `Service`, `Attorney` all present on intended pages.
- Meta audit: multi-H1 count drops from 48 to 0. og:image coverage rises from 22 to 74.
- Technical hygiene: HTML cache-control improved.

---

## Total quick-win opportunities: 14 actionable items (+ 4 optional polish)
