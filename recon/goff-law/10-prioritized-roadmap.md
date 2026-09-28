# Goff Law — SEO Audit & Prioritized Remediation Roadmap

**Date:** 2026-05-11
**Scope:** Full-site SEO audit + competitor benchmarking + prioritized fix roadmap for gofflawdfw.com
**Method:** See `recon/goff-law/01-09-*.md` artifacts for raw audit data
**Companion to:** Phase 1 + Phase 2 Thompson Law recon (`recon/thompson-law/`), Phase 1 Mullen & Mullen recon (`recon/mullen-mullen/`), Phase 1 UX recon (`recon/goff-law/UX-RECON-PHASE-1.md`)

---

## Executive summary (3 bullets)

1. **🏆 Goff is winning the emerging-litigation niche.** Galaxy Gas SERP shows **4 of top 10 results are Goff pages** (positions ~2, 6, 7, 8). This validates the existing strategy and represents the firm's biggest unfair SEO advantage. Strategic priority: **defend + extend** this template to other mass torts (AFFF, Tepezza, Paragard, AI Liability, Suboxone, hair relaxers).

2. **🚨 The schema gap is the biggest fixable leak.** Goff has only the Yoast-auto-generated schema (BreadcrumbList, WebSite, WebPage). Missing: Organization/LegalService, AggregateRating, FAQPage, Service, Attorney, Offer — every schema type that drives SERP rich results. Industry-wide gap; Goff can leapfrog Thompson Law and Mullen by being the first DFW PI firm to ship a comprehensive schema stack.

3. **❌ Geographic coverage is the biggest strategic gap.** Goff has zero pages for 32 DFW-area cities, including all the wealthy north-DFW suburbs (Plano, Frisco, Allen, McKinney) AND Fort Worth (1M population). Per Phase 2 SERP findings, those suburbs are confirmed low-competition / high-CPC opportunities.

---

## Tier 0 — This week (effort: ~15-20 hours total)

| Item | Effort | Impact | Owner | Source |
|---|---|---|---|---|
| Fix multi-H1 theme bug (affects 48 of 74 pages) | M (1-3 hr) | HIGH | WP dev | `03-meta-tags-audit.md` |
| Deploy sitewide `LegalService` schema (Block 1) | S (1 hr) | HIGH | WP dev | `08-schema-implementation-guide.md` |
| Deploy `AggregateRating` + 3-5 `Review` blocks on homepage | S (2 hr — needs Jim to gather GBP review data) | HIGH | WP dev + Jim | `08-schema-implementation-guide.md` |
| Add Yoast site-wide default `og:image` (covers 52 pages) | S (30 min) | MED-HIGH | WP dev / Jim | `03-meta-tags-audit.md` |
| Write meta descriptions for 8 missing pages | S (30 min) | MED | Content writer or Jim | `03-meta-tags-audit.md` |
| Deploy `Attorney` schema for Jim Goff bio | S (1-2 hr) | MED | WP dev | `08-schema-implementation-guide.md` |
| Deploy `Service` schema to top 5 practice pages | M (2-3 hr) | MED-HIGH | WP dev | `08-schema-implementation-guide.md` |
| Deploy `Offer` schema for free consultation | S (30 min) | LOW-MED | WP dev | `08-schema-implementation-guide.md` |
| Configure W3TC: HTML `Cache-Control` max-age 5min | S (30 min) | MED | WP dev | `04-technical-hygiene.md` |
| Trim 40 oversized meta descriptions to ≤155 chars | M (2 hr) | LOW-MED | Content writer | `03-meta-tags-audit.md` |

**Subtotal:** ~15-20 hours
**Estimated cost:** ~$0 if Jim's existing WP dev is on retainer; otherwise $500-1,500 for a freelance specialist on a one-shot engagement.

**Inputs Jim needs to provide before Tier 0 can ship:**
- [ ] Verified Google Business Profile review count + average rating
- [ ] 3-5 verified reviewer names + texts (for Review schema)
- [ ] Jim Goff bar admission year + law school
- [ ] Office hours
- [ ] Social media URLs (Facebook, LinkedIn, X, YouTube)
- [ ] Logo + office photo URLs

---

## Tier 1 — 30 days (cost: ~$2-5K)

| Item | Effort | Impact | Owner | Source |
|---|---|---|---|---|
| Deploy `FAQPage` schema across all practice-area pages (5-8 Q/A each) | L (8-12 hr writing + dev) | HIGH | Content writer + WP dev | `02-schema-audit.md` |
| **Build Frisco landing page hub** (city hub + 5-7 practice pages) | L (1-2 weeks content + dev) | HIGH | Content writer + WP dev | `06-content-gap-analysis.md` |
| **Build Plano landing page hub** | L (same scale) | HIGH | Content writer + WP dev | `06-content-gap-analysis.md` |
| Replicate Galaxy Gas template across AFFF + Tepezza + Paragard verticals (4 geo pages each) | L (1-2 weeks) | HIGH | Content writer | `07-serp-positioning.md` |
| **Build Allen + McKinney landing page hubs** | L | HIGH | Content writer + WP dev | `06-content-gap-analysis.md` |
| Run Phase 1 recon on **Hamilton Wingo** (newly-discovered $8B-settlements firm) | M (2-3 hr automated recon — same method as Mullen) | MED-HIGH (intel gap) | Claude / next session | `07-serp-positioning.md` |
| Pull actual GSC data for queries at pos 11-30 with traffic; identify "just-outside-top-10" wins | S (2 hr — Jim's data, my analysis) | HIGH (low-hanging fruit) | Jim + Claude | `07-serp-positioning.md` |
| Investigate + remediate `DataForSeoBot` block IF Jim subscribes to a SERP tool | S (5 min) | LOW (only if subscribed) | WP dev | `04-technical-hygiene.md` |
| Subscribe to a SERP tool (Ahrefs $129/mo recommended per prior memory) | n/a | HIGH (unlocks competitive intel beyond free WebSearch) | Jim's decision | `reference_serp_monitoring_options.md` |

**Subtotal: ~$2-5K** for content writer + dev time, plus tool subscription (~$129/mo recurring for Ahrefs).

---

## Tier 2 — 90 days (cost: ~$5-15K)

| Item | Effort | Impact | Owner | Source |
|---|---|---|---|---|
| **Build Fort Worth hub** (1M population, zero current coverage) | XL (2-3 weeks) | HIGH | Content writer + WP dev | `06-content-gap-analysis.md` |
| Build Arlington + Irving + Garland pages | L (per city) | MED-HIGH | Content writer | `06-content-gap-analysis.md` |
| Add Workers' Comp / Workplace Injury vertical (Texas-specific opportunity) | L | HIGH | Content writer | `06-content-gap-analysis.md` |
| Add Oilfield + Plant & Refinery + Construction Accident pages | L | MED-HIGH | Content writer | `06-content-gap-analysis.md` |
| Expand thin practice-area pages: Nursing Home Abuse (1→5 pages), Medical Malpractice (1→5 pages) | L | MED | Content writer | `06-content-gap-analysis.md` |
| Run Phase 1 recon on remaining DFW competitors: Witherite, Snellings, McCraw, Burress, Vecchio, Aldous, Lyons & Simmons | M (2-3 hr per firm × 7) | HIGH (closes intel gaps) | Claude / next sessions | `07-serp-positioning.md` |
| Deploy `LocalBusiness` schema variant with hours + geo | S | MED | WP dev | `02-schema-audit.md` |
| Add `Content-Security-Policy` header in report-only mode | M | LOW-MED (security) | Dev | `04-technical-hygiene.md` |
| Begin systematic Google review-collection program (target 100+ reviews in 90 days to match Mullen's 567) | M (process + tools) | MED-HIGH | Operations/intake | `07-serp-positioning.md` |

**Subtotal: ~$5-15K** content + dev time (mostly content production). Fits the $55-100K/mo budget from existing strategy docs.

---

## Tier 3 — 6-12 months (cost: ~$30-60K, fits the $55-100K/mo budget)

| Item | Effort | Impact | Owner | Source |
|---|---|---|---|---|
| **Spanish-language content** — Thompson Law has 150+ Spanish PI pages; Goff has zero. ~30% of DFW PI claimants are Hispanic. | XL (months of writer + translator work) | HIGH | Bilingual content writer | `06-content-gap-analysis.md` |
| **Blog content moat** — current 35 posts is light. Build to 200+ posts over 12 months targeting long-tail commercial queries. | XL (ongoing weekly cadence) | HIGH | Content writer + Claude | `05-content-inventory.md` |
| Build remaining DFW suburb pages (Garland, Mesquite, Grand Prairie, Carrollton, Richardson, Lewisville, Denton, Bedford/Euless/Hurst, Mansfield, Rockwall, etc.) | XL | MED-HIGH | Content writer | `06-content-gap-analysis.md` |
| Add Defective Vehicle / Defective Tire / Crashworthiness vertical (high-value mass tort) | L-XL | MED | Content writer | `06-content-gap-analysis.md` |
| Build comprehensive Goff Galaxy Gas content cluster (5+ supporting blog posts per geo page) | L | MED-HIGH (defend the moat) | Content writer | `07-serp-positioning.md` |
| Backlink building campaign (HARO, guest posts, local citations, legal directories) | XL | HIGH | SEO specialist or agency | All audits |
| Mobile UX optimization based on Phase 1 UX recon recommendations | L | HIGH (60-70% of PI traffic is mobile) | WP dev + designer | `UX-RECON-PHASE-1.md` |
| Hire dedicated SEO specialist or contract with agency for ongoing work | n/a | HIGH | Jim decision | All |

**Subtotal: $30-60K** for content + agency + tool subscriptions. Easily fits the $55-100K/mo budget envelope.

---

## Projected cumulative impact

### 30 days (Tier 0 + early Tier 1)
- Schema rich results begin appearing in Google SERP for Goff: star ratings, FAQ accordions, breadcrumb trail
- Multi-H1 bug fixed (helps Google understand page topic)
- og:image fixed (social sharing CTR improves)
- Frisco + Plano pages launched (new geographic SERP territory)
- Galaxy Gas / mass tort moat extended (4 → 8+ geo pages per tort)
- Expected: modest SERP CTR lift on existing rankings + first page-1 appearances in suburb-specific queries (Frisco PI lawyer, Plano PI lawyer)

### 90 days (Tier 0 + Tier 1 + most Tier 2)
- Fort Worth hub live (1M-pop market becomes Goff-accessible)
- Workers' Comp + Oilfield + Construction Accident verticals filled
- Competitive intelligence gaps closed (Hamilton Wingo + 6 other firms recon'd)
- 100+ Google reviews displayed via AggregateRating schema
- Expected: organic clicks from current ~170/mo grow toward 500-800/mo; first measurable lift in signed cases from new geographic markets

### 12 months (full roadmap)
- Goff is the dominant DFW PI organic player for emerging litigation (Galaxy Gas, Amazon truck, electric scooter, AI liability, mass torts)
- Goff has English coverage of every major DFW suburb
- Goff has 200+ blog posts and a Spanish-language content track
- Per existing executive report: from avg pos 40 → avg pos 5 = **10-20x organic clicks** from the same 42K impression base
- Per existing executive report budget projection: $720K invested → $13.5M revenue potential (18x ROI)

---

## Open questions for the COO briefing

1. **Schema deployment ownership** — Does Jim's current WP dev have schema/JSON-LD experience? If not, plan to bring in a specialist for the Tier 0 schema work (~$1,500 one-shot OR can be done by Schema Pro plugin + 4 hours of admin time).

2. **Review-collection program** — Mullen displays 567 reviews / 4.9★. What's Goff's actual Google Business Profile review count today? If it's <30, the AggregateRating schema is a nice-to-have but the bigger play is a systematic review-collection process (intake follow-up, post-case survey, email automation).

3. **Content production capacity** — Tier 1 + Tier 2 assume access to a content writer who can produce 1,500-3,000 word legal pages at a competent quality. Does Goff have this in-house? Contractor? Or use Bill AI Machine + Jim's review for production?

4. **SERP tool subscription decision** — Per `reference_serp_monitoring_options.md`, Ahrefs Lite at $129/mo is the recommendation. Decision is open from yesterday. Tier 1 work assumes some SERP tool is available — if Jim defers indefinitely, we lose visibility into rankings beyond what free WebSearch shows.

5. **Geographic expansion strategy** — Does Goff want to defend its Cedar Hill + DeSoto strongholds AND expand to north DFW suburbs simultaneously, or pick one expansion at a time?

6. **East Texas + Houston content** — Goff has 25 pages in each region but per audit they're under 1,500 words on average. Deepen them OR deprioritize for DFW focus?

7. **Hamilton Wingo intel gap** — New competitor surfaced in SERP audit with $8B settlements claim. Bigger than Thompson Law. Should we run full Phase 1/2 recon on them next session?

---

## Linked artifacts

- [01-url-inventory.md](01-url-inventory.md) — 176 URLs cataloged
- [02-schema-audit.md](02-schema-audit.md) — Schema gaps identified
- [03-meta-tags-audit.md](03-meta-tags-audit.md) — Meta, H1, og:image issues
- [04-technical-hygiene.md](04-technical-hygiene.md) — Headers, HTTPS, caching
- [05-content-inventory.md](05-content-inventory.md) — Practice areas + locations
- [06-content-gap-analysis.md](06-content-gap-analysis.md) — Gaps vs Thompson Law + suburbs
- [07-serp-positioning.md](07-serp-positioning.md) — Live SERP positions + new competitors
- [08-schema-implementation-guide.md](08-schema-implementation-guide.md) — Ready-to-paste JSON-LD
- [09-on-page-quick-wins.md](09-on-page-quick-wins.md) — This-week effort list
- [UX-RECON-PHASE-1.md](UX-RECON-PHASE-1.md) — Visual UX comparison (from yesterday)
- [HERO-FIX-DRAFT.md](HERO-FIX-DRAFT.md) — Homepage hero redesign spec (from yesterday)

## Companion recon

- `recon/thompson-law/PHASE-1-RECON-REPORT.md` + `PHASE-2-DEEP-DIVE-REPORT.md`
- `recon/mullen-mullen/PHASE-1-RECON-REPORT.md`
- `recon/COMPETITOR-SCOREBOARD.md`
- `recon/dfw-pi-positioning-map.svg`
