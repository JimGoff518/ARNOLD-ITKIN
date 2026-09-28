# Thompson Law — Phase 1 Recon Report

**Target:** Thompson Law Injury Lawyers (Ryan "The Lion" Thompson)
**Real URL:** https://1800lionlaw.com
**Recon date:** 2026-05-09 (evening)
**Scope:** 1 homepage + 1 robots.txt + 23 sub-sitemaps + 10 representative pages crawled via Crawl4AI

---

## CRITICAL ALERT — Existing competitive analysis cites the wrong URL

Your prior competitive analysis docs in this workspace list `thompsons.law` as Thompson Law's website **in at least 4 places** ([goff-law-competitive-analysis-ADDENDUM.md:26](../../goff-law-competitive-analysis-ADDENDUM.md), [goff-law-dfw-competitive-analysis-report.md:186](../../goff-law-dfw-competitive-analysis-report.md), `:900`, `:2608`).

**That URL is wrong.** Two domains were tested and neither is Ryan Thompson's PI firm:

| Domain | What it actually is |
|---|---|
| `thompsons.law` | **Thompsons Solicitors UK** — a 1921-founded British personal injury firm with 18 offices across England/Wales/NI. Not a Texas competitor. |
| `thompsonlawtx.com` | **Law Office of Carey Thompson, PC** in Saginaw — does estate planning, probate, SSDI appeals, business law. Not a personal injury firm. |
| **`1800lionlaw.com`** ✅ | **Real Thompson Law** — Ryan L. Thompson, $1.9B settlements, 4 offices (Dallas/Phoenix/LA/Atlanta) |

**Implication:** Any keyword position estimates, traffic numbers (the "25,000/mo organic, 200+ keywords" claim), DA scores ("DA 55"), or PPC spend figures previously attributed to "Thompson Law" via the wrong URL are not reliable. Recommend a SEMrush/Ahrefs re-pull against `1800lionlaw.com` before quoting any of those numbers to the COO.

---

## Footprint at a glance

| Metric | Thompson Law | Goff Law (for context) |
|---|---|---|
| Total static pages | **~1,109** | ~30-40 (est.) |
| Blog posts (est.) | **~891** | ~50 (est.) |
| Total indexable URLs (est.) | **~2,000+** | ~100 |
| State coverage | **TX, CA, AZ, GA + IL launching** | TX only |
| Bilingual content | **Full Spanish duplicate** (~150+ Spanish pages) | None |
| Blog cadence (post-sitemap1 lastmod) | Updated **2026-05-09** (today) | Variable |

**Conclusion:** Thompson Law is **not** a "DFW PI firm." They're a national multi-state PI brand with deep SEO infrastructure. Treating them as a peer-sized DFW competitor underestimates the gap.

---

## Page architecture — they run a programmatic SEO factory

Every Dallas practice-area page follows an **identical template**:

1. H1: `[City] [Practice Area] Lawyers`
2. Identical hero case-result trio: **$3,107,629 / $11,991,670 / $9,187,114** (every page tested)
3. "Receive a Free Case Review" form
4. BBB Accredited badge + awards row
5. Long-form copy (2,500–5,000 words per page)
6. "What Clients Are Saying" testimonial block (same across pages)
7. "Awards and Recognized Results" repeated section
8. Texas Offices map block

**This same skeleton is used across:**
- 23+ Dallas practice-area pages (`/tx/dallas/{practice}-lawyers/`)
- All other Texas city hubs (Fort Worth, Arlington, Houston, Garland, McKinney, Waco, San Antonio, etc.)
- Replicated for California, Arizona, Georgia
- Replicated again in Spanish (`/abogados-de-{practice}-en-{city}/`)

This is **template-based programmatic SEO at industrial scale** — likely 800+ city/practice-area landing pages built from the same component system.

---

## Positioning & messaging stack

### Brand identifiers
- **Tagline:** "No Fee Unless We Win"
- **Trust hammer:** "OVER $1.9 BILLION RECOVERED FOR OUR CLIENTS"
- **Phone branding:** 1-800-LION-LAW (1-800-546-6529)
- **Personality vehicle:** Ryan "The Lion" Thompson — has a separate attorney site at ryanthelionthompson.com
- **Trial credibility:** "Trial-Ready" / "Trial-Tested" appears in headlines

### Promise stack (appears on virtually every page)
1. No fee unless we win
2. Free consultation 24/7
3. Same-day case start (truck pages)
4. No obligation
5. "Free case review" CTA repeated 5–10× per page

### Trust signals (stacked redundantly)
- $1.9B aggregate settlements
- BBB Accredited Business
- "5-Star Reputation" claim
- Awards/honors badges (multiple)
- Client testimonials (same set across pages)
- Specific case results with dollar amounts (e.g. $3.1M, $11.9M, $9.2M trio)

### Phone CTA pattern
Three numbers stack on every page, presumably for call tracking:
- (214) 716-0116 — Dallas
- (817) 873-1639 — Fort Worth/Tarrant
- (713) 322-7750 — Houston

---

## Practice area inventory

**Volume verticals (heavy investment):**
- Car accidents
- Truck accidents (their flagship — most copy depth, "trial-tested" framing)
- Motorcycle accidents
- Wrongful death
- Pedestrian accidents
- Slip & fall / Premises liability

**Industrial/specialty verticals:**
- Oilfield accidents (Texas-specific differentiator)
- Plant & refinery accidents
- Construction accidents
- Workers' compensation
- Commercial vehicle accidents
- Maritime injury
- Aviation accidents

**Defective product / mass tort verticals:**
- Defective tires (heavy emphasis — case results dominated by tire failure cases)
- Vehicle crashworthiness defects
- Defective seatbelts, airbags, fuel systems
- Defective medical devices
- Dangerous drugs

**Catastrophic injury verticals:**
- Brain injury
- Spinal cord injury
- Paralysis
- Amputation
- Burn injury
- Drowning / pool

**Other:**
- Rideshare (Uber/Lyft)
- Dog bites
- Bicycle accidents
- E-scooter accidents
- Bus / public transportation
- Boat accidents
- Elevator accidents
- Nursing home abuse
- Daycare abuse
- Amusement park accidents
- ATV accidents
- Go-kart / golf cart accidents

**Inferred strategy:** "If a Texan can be injured doing it, we have a landing page for it." Goff cannot match this surface area with $55–100K/mo. Goff must instead **out-rank or out-convert on a defended subset**.

---

## Geographic coverage — the city map

### Texas (English) — 362 URLs under /tx/
**DFW core (full English coverage):** Dallas, Fort Worth, Arlington, Plano, Frisco, McKinney, Garland, Mesquite, Irving, Carrollton, Lewisville, Allen, Richardson, Grand Prairie, Denton

**Outer DFW/North Texas:** Cedar Hill, Balch Springs, DeSoto, Haltom City, Cleburne, Midlothian, Waxahachie, Burleson, Keller, Bedford, Euless, Hurst, Coppell, The Colony, Little Elm, Saginaw, Sachse, Seagoville, Flower Mound

**Other major Texas metros covered:** Houston (+ Sugar Land, Pearland, League City, Baytown, The Woodlands, Conroe, Galveston, Missouri City), San Antonio (+ New Braunfels, Cibolo, Boerne, Canyon Lake, Seguin), Austin (+ Round Rock, Cedar Park, Pflugerville, Bastrop, Kyle, Leander, San Marcos), Waco, Killeen, Temple, Tyler, Longview, Lubbock, Amarillo, Wichita Falls, Midland, Odessa, El Paso, Beaumont, Corpus Christi, McAllen, Edinburg, Mission, Brownsville, Laredo, Abilene, San Angelo

### Other states
- **California** — 221 pages (Sacramento, San Francisco, Santa Clarita, LA + suburbs)
- **Arizona** — 100 pages (Phoenix, Tucson + suburbs)
- **Georgia** — 41 pages (Atlanta primary)
- **Illinois** — 1 page (just starting)

### Spanish-language coverage
~150+ Spanish landing pages following pattern `/abogados-de-{practice}-en-{city}/`. Includes essentially every English DFW city plus Houston, San Antonio, Austin, and even multi-state (LA, Phoenix, Atlanta).

---

## Content depth

Sample page sizes (markdown):
- Dallas hub: 26KB / ~3,500 words
- Dallas car accident: 29KB / ~4,000 words
- Dallas truck accident: **42KB / ~5,500 words** (their longest)
- Dallas motorcycle: 40KB / ~5,200 words
- Dallas wrongful death: 31KB / ~4,000 words
- Our Results page: **53KB / ~7,000 words** (mostly settlement amounts)

**Implication:** These are not thin landing pages. They have invested in long-form, FAQ-heavy, schema-friendly content per page. To outrank them on `[city] [practice] lawyer` queries, Goff's pages need to be at minimum 3,500 words with comparable trust signals.

---

## Strike list — Thompson Law's exploitable weaknesses

Rank-ordered by leverage:

### 1. **The "Our Results" page H1 is in the wrong language**
The page at `/our-results-2/` has H1 = `Nuestros resultados` (Spanish) on what is otherwise an English page (URL is English, content is English). This is a templating error — Yoast/SEO crawlers will see a Spanish title on an English-targeted page. **Quick win: nothing for Goff to do here, but evidence that their template engine is brittle.**

### 2. **Massive near-duplicate content across cities**
The same template skeleton + same case results + same testimonial block + same FAQ frame is used on hundreds of pages. Google's Helpful Content / duplicate content systems can devalue this at scale. **Goff opportunity: build genuinely city-specific content** (real local crash data, real local courts/judges, real DFW neighborhood references) on a smaller set of pages — quality vs. their volume.

### 3. **Multiple H1s on at least one practice page**
Dallas motorcycle has two H1s (`Dallas Motorcycle Accident Lawyer ` and `Thompson Law Guarantee`). Likely an oversight in the WordPress template. **Goff: ensure single, well-formed H1 per page.**

### 4. **Trailing whitespace and case inconsistencies in headlines**
Multiple H1s end with a trailing space (`Dallas Personal Injury Lawyers `). Minor but evidence of low editorial QA — they're generating pages from templates faster than they're being reviewed.

### 5. **Blog content is broad/informational, not high-intent**
Sampled blog post slugs from post-sitemap1: "which-states-require-a-front-license-plate", "what-is-a-rolling-stop", "can-you-park-next-to-a-fire-hydrant", "is-it-illegal-to-drive-with-interior-car-lights-on". These are top-of-funnel curiosity content — not commercial-intent topics that produce signed clients. **Goff opportunity: skip the curiosity content; build BOFU content (e.g., "How much is a [specific injury] settlement worth in [DFW county]") that wins commercial-intent searches.**

### 6. **No Frisco/Plano/Allen English city pages — only Spanish**
Several high-income, high-traffic-volume DFW suburbs (Plano, Allen, McKinney, Frisco) have **Spanish-language pages but NOT English pages** in the sitemap, OR are covered only via the broad `/tx/dallas/` parent. These are some of the wealthiest, highest-PI-CPC zip codes in the metro.
- Plano-specific English: only `/tx/plano/` parent (no practice-area children visible)
- Frisco-specific English: only Spanish exists (`/abogados-de-accidentes-en-frisco/`)
- McKinney-specific English: limited
- **Goff opportunity: build the dedicated English `[Frisco/Plano/Allen/McKinney] [practice] attorney` page set Thompson Law hasn't built. Lower competition + high-income clients.**

### 7. **The "Lion" persona is a single point of failure**
The brand is heavily anchored on Ryan Thompson personally ("Ryan The Lion"). If anything happens to him (bar discipline, PR incident, leaves the firm), the brand collapses. **Goff angle: position "Jim Goff" as the alternative for clients who want a personal advocate, not a brand mascot.**

### 8. **No specialty for emerging litigation themes**
No dedicated landing pages found for: Galaxy Gas / nitrous oxide injuries, Amazon delivery vehicle litigation, hernia mesh — all of which are areas your existing workspace docs identify as high-opportunity. **Goff is already ahead here** (per your existing GSC ranking pos 6-8 on Galaxy Gas content).

### 9. **They appear to lack schema markup verification**
Need to verify in Phase 2, but the markdown extracts show no FAQ-styled markup blocks. If they're not using FAQ schema, Review schema, Attorney schema — that's a big SERP feature opportunity.

### 10. **Crawl-delay not set in robots.txt**
Their robots.txt allows aggressive crawling (no crawl-delay). Doesn't help Goff directly but tells us they're not bandwidth-constrained — this is an enterprise-hosted site (likely WordPress on managed hosting like WP Engine or similar).

---

## Recommended next moves

### Immediate (this week)
1. **Fix the existing competitive analysis docs** to use `1800lionlaw.com`. Re-pull SEMrush/Ahrefs data against the correct URL before any COO briefing.
2. **Pull ALL pages from `1800lionlaw.com` for full keyword/topic mapping** — Phase 2. We have the URL list (1,109 static pages); a full crawl would take ~30–60 min via Crawl4AI.
3. **Verify Witherite Law Group** — `witheritelaw.com` is the correct Amy Witherite firm (confirmed). Run Phase 1 against them next.

### Phase 2 priorities
1. **Schema audit** — extract structured data from 10 representative pages
2. **Backlink profile** — Ahrefs/Majestic on `1800lionlaw.com`
3. **Live SERP check** — Google `[Dallas car accident lawyer]`, `[Dallas truck accident lawyer]` etc. and observe their ranking + ad positioning
4. **Frisco/Plano/Allen/McKinney English-page gap audit** — confirm via SERP that Goff can win these without a Thompson Law incumbent

### Phase 3 — Strike plan inputs
1. Compare practice-area URL list (1800lionlaw vs. your current site) → topic gaps
2. Compare DFW city coverage → geo gaps
3. Compare blog topic distribution → content gap analysis vs. your DFW Content Marketing Playbook

---

## Files saved (this recon)
- `recon/thompson-law/PHASE-1-RECON-REPORT.md` — this file
- `%TEMP%/lion-home.json` — homepage markdown
- `%TEMP%/lion-sitemap-idx.xml` — sitemap index
- `%TEMP%/lion-page-sitemap{1-11}.xml` — 11 page sitemaps
- `%TEMP%/lion-attorneys-sitemap.xml` — attorneys sitemap
- `%TEMP%/lion-post-sitemap1.xml` — blog post sample sitemap
- `%TEMP%/lion-{dallas-hub,dallas-car,dallas-truck,dallas-moto,dallas-wd,dallas-oilfield,ftworth-hub,results,national-pi,spanish-dallas-pi}.json` — 10 page crawls

(These are in your Windows TEMP — let me know if you want them moved into the workspace permanently.)
