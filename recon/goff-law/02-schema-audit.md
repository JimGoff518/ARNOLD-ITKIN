# Goff Law — Schema Markup Audit

**Crawl date:** 2026-05-11
**Pages audited:** 74
**Comparison benchmark:** Thompson Law (1800lionlaw.com), per `recon/thompson-law/PHASE-2-DEEP-DIVE-REPORT.md`. Mullen & Mullen schema audit pending (Phase 2 backlog).

## TL;DR

Goff Law has only the schema that **Yoast SEO auto-generates by default**: BreadcrumbList, WebSite, WebPage, ImageObject (and one Attorney + a few Person blocks on blog authors). The schema types that drive **SERP rich results for law firms** — Organization, LegalService, AggregateRating, FAQPage, Service, Offer — are entirely absent.

This is a **major opportunity gap**. Thompson Law has Organization + LegalService on every page (still misses Attorney + AggregateRating, but at least has firm identity). Goff has neither, which means Google has no structured signal that "this site = a law firm offering Y services in DFW."

## Aggregate schema types found

| Schema type | Pages with it | % of 74 | Should be on Goff? | Verdict |
|---|---|---|---|---|
| `BreadcrumbList` | 74 | 100% | Yes — every page | ✅ Full coverage |
| `WebSite` | 74 | 100% | Yes — homepage (with SearchAction) | ✅ Full coverage |
| `WebPage` | 72 | 97% | Yes — every page | ✅ Near-full coverage |
| `ImageObject` | 22 | 30% | Optional but useful | ⚠️ Sparse |
| `Person` | 6 | 8% | Yes — for blog post authors | ⚠️ Sparse |
| `WebPage+ContactPage` | 2 | 3% | Yes — contact page only | ⚠️ Limited |
| `Attorney` | 1 | 1% | Yes — every attorney bio | ⚠️ Only 1 page |
| `Organization` | 0 | 0% | Yes — sitewide | ❌ **MISSING ENTIRELY** |
| `LegalService` | 0 | 0% | Yes — sitewide (preferred over Organization for law firms) | ❌ **MISSING ENTIRELY** |
| `AggregateRating` | 0 | 0% | Yes — homepage + key landing pages | ❌ **MISSING ENTIRELY** |
| `Review` | 0 | 0% | Yes — paired with AggregateRating | ❌ **MISSING ENTIRELY** |
| `FAQPage` | 0 | 0% | Yes — every practice-area page with FAQs | ❌ **MISSING ENTIRELY** |
| `Service` | 0 | 0% | Yes — each practice-area page | ❌ **MISSING ENTIRELY** |
| `Offer` | 0 | 0% | Yes — homepage + every consult CTA | ❌ **MISSING ENTIRELY** |
| `LocalBusiness` | 0 | 0% | Yes — homepage (with hours + address) | ❌ **MISSING ENTIRELY** |

---

## Critical gaps (in priority order)

### 🚨 P0 — Add immediately (these directly drive SERP rich results)

**1. AggregateRating + Review**

Mullen & Mullen displays "567 reviews / 4.9★" prominently in their site UI (we should verify schema markup in Phase 2 recon). **Goff currently has ZERO review schema and ZERO visible review count on the homepage.** This is the single biggest SERP-feature miss.

- **Action:** Get verified Google Business Profile review count + average rating. Add `AggregateRating` schema to homepage in `<head>`. Add `Review` schema for top 3-5 most recent positive reviews.
- **Impact:** Star ratings appear next to listings in SERP (massive CTR lift), passes Google's E-E-A-T trust signals.
- **Blocker:** Need actual review numbers from Jim before deploying.

**2. Organization / LegalService**

Thompson Law has this on every page. Goff has neither. Without it, Google has no structured signal that this site is a law firm with an address, phone, hours, areas served.

- **Action:** Add sitewide `LegalService` block (preferred over generic Organization for law firms) in homepage `<head>`. Include name, address, phone, areas served (DFW + surrounding cities), founder (Jim Goff), URL, social media accounts.
- **Impact:** Knowledge panel eligibility, attorney rich cards, "near me" local-pack improvements.

**3. FAQPage**

Most Goff practice-area pages have FAQ-shaped content in the body but it's not marked up. Marking it up makes FAQs appear as expandable rich snippets directly in SERP results.

- **Action:** Every practice-area page that has FAQ content (most of them do — verified during URL inventory) gets a `FAQPage` block with 5-8 Q/A pairs lifted from existing copy.
- **Impact:** Expandable FAQ boxes under your SERP listing = more SERP real estate.

### 🟧 P1 — Add in week 2

**4. Service schema**

Each practice area (car accident, truck accident, wrongful death, slip & fall, premises liability, Galaxy Gas, mass tort, etc.) should be a discrete `Service` block with `areaServed` covering DFW cities.

- **Action:** Service schema template applied to each `/legal-services/*` and `/dallas-personal-injury-lawyer/*` page.

**5. Attorney schema**

Currently 1 found across 74 pages. Goff likely has at least Jim Goff's bio that needs proper `Attorney` markup (including barCertification, alumniOf, areasServed).

- **Action:** `Attorney` schema on every attorney bio page.

### 🟨 P2 — Add when convenient

6. **Offer** — Free consultation marked as a discrete Offer.
7. **LocalBusiness** variant — Hours of operation, address, geo coordinates.
8. **VideoObject** if you have video content on landing pages.

---

## Per-page schema inventory (highlights)

All 74 pages have the same Yoast-auto-generated schema set: `[WebPage, ImageObject, BreadcrumbList, WebSite]` with occasional additions:
- 2 contact pages have `ContactPage` variant
- 6 blog posts have author `Person` schema
- Galaxy Gas attorney bio likely has the lone `Attorney` schema (need to verify which page that was on)

**No page has multiple LD-JSON script blocks** (Yoast emits one block per page with a `@graph` array).

The full per-page data is saved at `%TEMP%\goff-schema-data.json` for reference.

---

## Comparison vs competitors

| Schema type | Goff Law | Thompson Law (1800lionlaw) | Mullen & Mullen |
|---|---|---|---|
| `Organization` / `LegalService` | ❌ 0/74 | ✅ Yes, on every page | (Phase 2 backlog) |
| `BreadcrumbList` | ✅ 74/74 | ✅ Every page | (Phase 2 backlog) |
| `WebSite` | ✅ 74/74 | ✅ Yes | (Phase 2 backlog) |
| `WebPage` | ✅ 72/74 | ✅ Yes | (Phase 2 backlog) |
| `Attorney` | ⚠️ 1/74 | ❌ Missing (their gap too) | (Phase 2 backlog) |
| `AggregateRating` / `Review` | ❌ 0/74 | ❌ Missing despite 2,021 Birdeye reviews | (Phase 2 backlog) |
| `FAQPage` | ❌ 0/74 | ⚠️ 2 of 5 pages (inconsistent) | (Phase 2 backlog) |
| `Service` | ❌ 0/74 | ❌ Missing | (Phase 2 backlog) |
| `Offer` | ❌ 0/74 | ❌ Missing | (Phase 2 backlog) |
| `LocalBusiness` | ❌ 0/74 | ❌ Missing | (Phase 2 backlog) |

### Strategic insight

The schema gap is largely **industry-wide** in DFW PI marketing. Goff currently lags Thompson Law by 1-2 critical schema types (Organization/LegalService), but **leapfrogging both Thompson AND Mullen is achievable** by being the first DFW PI firm to ship a comprehensive Attorney + AggregateRating + Service + FAQPage + Offer schema stack.

That gives Goff SERP features competitors do not have — star ratings, expandable FAQ boxes, attorney rich cards, service rich results — all without paid media spend.

---

## Recommendations summary

| Priority | Schema type | Effort | Impact |
|---|---|---|---|
| P0 | AggregateRating + Review (homepage) | S (2hr if Google review data exists) | HIGH — star ratings in SERP |
| P0 | LegalService (sitewide) | S (1hr) | HIGH — firm identity, knowledge panel |
| P0 | FAQPage (every practice page) | M (8hr to write FAQs + add markup) | HIGH — expandable FAQ snippets |
| P1 | Service (each practice area) | M (4-6hr) | MED-HIGH — service-specific rich results |
| P1 | Attorney (each attorney bio) | S (1-2hr per attorney) | MED — attorney rich cards |
| P2 | Offer | S (30min) | LOW-MED |
| P2 | LocalBusiness | S (1hr) | MED — local pack improvement |

**Total P0+P1 schema effort:** ~12-15 hours. Could be split across 2-3 days. Ready-to-paste JSON-LD blocks are produced in Task D1 → `08-schema-implementation-guide.md`.

---

## Raw audit data

The aggregate JSON is saved at `%TEMP%\goff-schema-data.json` for downstream tasks (Task D1 will reference this).
