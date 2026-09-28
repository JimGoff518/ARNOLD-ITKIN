# Goff Law DFW — SEO Page-Type Gap Analysis (v2 — 19 firms)

**Date:** 2026-05-17 (v2 expansion)
**Method:** Live URL audit of gofflawdfw.com (176 indexed URLs via Yoast sitemap_index.xml) + page-type inventory of 19 DFW + Texas PI competitors across 36 page types
**v1 → v2 deltas:** Added Hamilton Wingo, Snellings, J. Alexander, Thompson Law (Tier S/A/B benchmarks), Zehl, DFW Injury Lawyers, Hartley Law, Mr. Law, Kastl Law, DFW Injury Lawyer, Ted Lyon, Jay Murray, Shamieh Law, MAA Firm/Anderson Injury Lawyers
**Two moat status changes:** Legal glossary moat BROKEN (Zehl + MAA Anderson). FAQ-page atomization moat PARTIALLY contested (MAA Anderson)

---

## Executive summary — 10 things that matter most

1. **5 must-build parity gaps hold at 19 firms.** Every firm has Attorney bios (19/19), About (17/19 — only Hamilton Wingo and Snellings substitute via bio + nav-grouping), Case Results (19/19), Testimonials (19/19), FAQ (16/19). Goff has zero of these five. **These are still the P0 builds.**

2. **THE BIG ONE — MAA Firm (Anderson Injury Lawyers) is executing Goff's FAQ-page niche stack right now.** MAA has `/dallas-car-accident-attorney/faq/what-to-do-when-injured-in-a-car-accident-in-dallas-tx/`, `.../when-to-hire-a-lawyer/`, `.../who-will-pay-my-medical-bills.../`, plus a Fort Worth FAQ subfolder. This is the EXACT atomized city × practice × FAQ structure Jim's marketing-constraint memo identified as uncontested. **Dallas car-accident FAQ vertical is now contested.** Goff's Spanish FAQ and mass-tort FAQ angles remain 0/19 — those stay uncontested.

3. **Legal glossary moat BROKEN.** Was 0/9. Now **2/19** — Zehl's `/personal-injury-resources/` (18+ definition pages) and MAA Anderson's 27-entry glossary. Goff can still win with bilingual + mass-tort-prefixed glossary entries, but the pure-English glossary play is no longer uncontested.

4. **5 moats remain 0/19 — strongest possible signal.** Insurance-company-NAMED pages (State Farm, GEICO, Allstate, Progressive, USAA), Hospital-NAMED pages (Baylor Plano, Methodist Mansfield, Texas Health, Parkland), Federal MDL bellwether tracker, Non-case-value utility calculators (SOL deadline, comparative negligence), Year-in-review annual report. **All 5 confirmed structurally absent across 19 firms.** Moat thesis validated.

5. **Mass-tort current-MDL moat STRENGTHENED.** 0/19 firms have current pharmaceutical MDL pages (Galaxy Gas, AFFF, Paragard, hair relaxer, Tepezza, Suboxone, PFAS, AI Liability). Ted Lyon has Elmiron (older). Zehl has 2018-2022 mix (Takata, transvaginal mesh). Mullen has older mix (Roundup, Tylenol, Peloton). **Goff's 15+ current-MDL pages are the strongest defensible content position in the entire DFW PI landscape.**

6. **Lead-magnet library is the peer-tier playbook.** Snellings has 17 free guides. McCraw has free books. Hartley has the "free Uber/Lyft safe ride home" program. DFW Injury Lawyer has scholarships. **5 of 19 firms run substantial lead-magnet programs.** Goff has zero. Adding 3-5 lead magnets anchored to mass-tort + Phase 4 cities = peer-tier parity in 4-6 weeks.

7. **Accessibility statement now 3/19 — promote from Tier 3 to Tier 1.** McCraw + Jay Murray + MAA Anderson have them. Trend toward parity. Combined with ADA-lawsuit exposure reduction = ship-this-week tier.

8. **Spanish landscape map: 8 of 19 firms have meaningful ES content** (Reyes gold standard ~70 pages, McCraw full, L&S full, Thompson ~150 pages, Mr. Law full parallel, Shamieh ~115 pages, MAA Anderson ~25 pages, Zehl + DFW Injury Lawyers + DFW Injury Lawyer + Ted Lyon all partial). **The Spanish × mass-tort intersection — Goff's structural moat — remains 0/19.** Build that 4-page sprint.

9. **Three steal-worthy ideas this audit surfaced:**
   - **Hartley's "Free Uber/Lyft safe ride home"** — best lead-magnet idea in any recon. Near-zero cost, news-bait, hyperlocal. Clone-and-ship within a week.
   - **DFW Injury Lawyers' `llms-sitemap.xml`** — first firm in any DFW PI dataset to ship an AI-crawler-specific sitemap. Forward-looking 2026 SEO. Trivial to add to Yoast.
   - **Shamieh's drone delivery accident vertical** — emerging-tech tort. Directly stacks with Goff's existing AI Liability page. 4-state coverage including ES.

10. **Site-health issues unchanged from v1 and still critical.** 6 footer 404s on every page. 5 homepage body 404s. WordPress soft-404 problem on `/attorneys`. NO schema.org JSON-LD detected on homepage. Three different URL patterns for city pages. All still leaking traffic right now.

---

## Section 1 — What Goff actually HAS (unchanged from v1)

| Inventory item | Count / detail |
|---|---|
| Total indexed URLs | **176** (Yoast sitemap_index.xml) |
| City silos | 5 — Dallas, Cedar Hill, East Texas, Houston, DeSoto |
| Pages under `/dallas-personal-injury-lawyer/` | ~110 |
| Practice areas with at least one live URL | ~18+ |
| Blog posts | 39 (at `/news/`, paginated) |
| Mass-tort / federal MDL pages | ~15 — Galaxy Gas (3-state geo: TX/NTX/GA), AFFF, Paragard, PFAS, Tepezza, Suboxone, Hair Relaxer, AI Liability, Privacy/Emotional Distress |
| Schema.org JSON-LD on homepage | **Not detected** |
| CMS | WordPress + Yoast SEO + W3 Total Cache + Redis |
| HTML user-facing sitemap | Yes, at `/site-map/` |

## Section 2 — The 5 must-build parity gaps (every competitor has these)

| Gap | Goff state | Coverage across 19 firms | Why P0 |
|---|---|---|---|
| **Attorney bio page** | `/attorneys`, `/jim-goff`, `/team` all 404 | **19/19 firms have at least one** (Reyes ~30, Witherite 45, Anderson MAA 14, Ted Lyon 10, L&S 10, McCraw 11, Snellings 4, Mullen 4, J. Alexander 6, Shamieh 4+, Mr. Law 8, etc.) | Zero E-E-A-T for the named attorney on his own site. **Most-confirmed universal in the dataset.** |
| **About / About Us page** | `/about`, `/about-us` both 404 | 17/19 (Hamilton Wingo and Snellings substitute via attorney-bio + nav-grouping; everyone else has a dedicated page) | Foundation page. Goff is one of 2 firms without it. |
| **Case Results / Verdicts** | `/case-results`, `/results`, `/verdicts-and-settlements` all 404 | **19/19** | Conversion-killer. Every consumer wants to see verdict numbers. |
| **Testimonials / Reviews** | `/testimonials`, `/reviews` both 404 | **19/19** | Social proof. You already have 42 five-star Google reviews — surface them. |
| **FAQ hub page** | `/faq`, `/faqs` both 404 | 16/19 (L&S, J. Alexander, Kastl partial don't have dedicated hubs) | Phase 1 + 1b briefs already cover 18 FAQ pages — just needs the parent URL. **HOWEVER**: MAA Anderson is now executing atomized city × practice × FAQ — Goff should pivot to bilingual + mass-tort FAQ where MAA is absent. |

**Build cost estimate:** Attorney bio + About + Case Results + Testimonials = 4 pages, ~3-5 hrs each = 12-20 hrs Dianne work.

## Section 3 — Moat opportunities (status updated for 19-firm dataset)

| Moat | Status across 19 firms | Goff's unique authority signal | Build priority |
|---|---|---|---|
| **Insurance-company-NAMED pages** ("Suing State Farm in Texas," "How GEICO undervalues claims in DFW") | **0/19 — UNCONTESTED** (multiple firms have generic bad-faith / PIP / UM/UIM content but ZERO name carriers) | **Jim worked DEFENSE for the biggest insurance companies in Texas.** Unique authority no other firm can match. | **P0 — top moat play, validated across 19 firms** |
| **Hospital-NAMED pages** ("Injured at Baylor Plano," "Treated at Methodist Mansfield") | **0/19 — UNCONTESTED** (Jay Murray has "hospital sexual abuse" institutional framing; Mr. Law mentions Parkland/Baylor contextually; nobody has dedicated hospital-named pages) | Hyperlocal post-ER intent capture; Phase 4 v2 brief already has the DFW hospital list mapped | **P0 — hyperlocal moat** |
| **Federal MDL bellwether tracker** | **0/19 — UNCONTESTED** | Stacks with Goff's existing 15+ current-MDL pages | **P1 — content moat** |
| **Non-case-value utility calculators** ("Texas SOL deadline calculator," "comparative negligence calculator," "PIP coverage estimator") | **0/19 — UNCONTESTED** (DFW Injury Lawyer has "what is my case worth" page but no interactive utility calc) | Genuinely useful tools — unlike fake settlement estimators. | **P2 — Trust signal** |
| **Year-in-review / annual report** | **0/19 — UNCONTESTED** | Once-a-year PR + backlinks + E-E-A-T | **P3 — annual cadence** |
| **Legal glossary** | ~~0/9 was uncontested~~ → **NOW 2/19 (Zehl, MAA Anderson)** | Still partially open — bilingual + mass-tort-prefixed glossary terms = 0/19 | **P2 — narrower play than originally scoped. Spanish-first.** |
| **Court / jurisdiction info pages** | 0/19 for true county-specific (Dallas County District Court, Tarrant County, Collin County) — Ted Lyon and MAA have Texas-statute-level pages but none have actual court pages | Hyperlocal authority + ranks for niche court-name queries | **P2** |

## Section 4 — Strategic decision territory (some firms have, some don't)

| Page type | Coverage 19 firms | Goff move |
|---|---|---|
| **Spanish parallel content** | 8/19 — Reyes (~70 pages, gold), Thompson (~150 pages), Mr. Law (full parallel), Shamieh (~115 pages), McCraw (full), L&S (full), MAA Anderson (~25 pages), Zehl (toggle). | **Don't try full ES parity.** Build Spanish × mass-tort niche only — 0/19 firms compete here. 4-page sprint. |
| **Case calculator** | 1/19 — Reyes only | **SKIP per Jim** (defense-industry shortcut, fake numbers). Build utility calculators (SOL, comparative neg) instead. |
| **Pillar guides** | 2/19 — Reyes (Ultimate Truck + Ultimate Car TX), Snellings (17-guide library counts in spirit) | P1 — one pillar per major practice area |
| **Editorial standards / E-E-A-T page** | 1/19 — Reyes only | P1 — cheap E-E-A-T signal |
| **Accessibility statement** | 3/19 — McCraw, Jay Murray, MAA Anderson. **Trending toward parity.** | **PROMOTE TO P1.** ADA lawsuit-exposure reduction alone justifies. Boilerplate template. |
| **HTML user sitemap** | 7/19 — McCraw, L&S, Hamilton Wingo, DFW Injury Lawyers, Mr. Law, Ted Lyon, Goff (`/site-map/`), MAA Anderson | Goff already has. Keep. |
| **Video library / video sitemap** | 11/19 (~58%) — Reyes, McCraw, L&S, Hamilton Wingo, Thompson, DFW Injury Lawyers, Mr. Law, Ted Lyon, Jay Murray, Shamieh, MAA Anderson | Approaching parity. **TikTok organic** is cheaper-equivalent trust signal. |
| **Neighborhood-level pages** | 4/19 — Mullen (14 suburbs), Jay Murray (8 Dallas neighborhoods), MAA Anderson (9 Dallas + Sundance Square FW), Mr. Law (Addison/Balch Springs/Farmers Branch/Sunnyvale as full silos). **Trend rising.** | Goff's Phase 4 v2 (16 suburb pages) competes correctly. Consider sub-Dallas neighborhood layer (Pleasant Grove, South Oak Cliff, Bishop Arts, Deep Ellum) for Q3. |
| **Mass tort / MDL pages** | 4/19 — Mullen (5 older), Ted Lyon (Elmiron + 9 meso pages), Zehl (~13 older MDLs), Mr. Law (hernia mesh listed) — none with current MDL inventory | **Goff already wins here.** 15+ current-MDL pages already live. Single strongest defensible position. |
| **Free guide / lead magnet** | 5/19 — Snellings (17!), McCraw (free book), Hartley (free safe ride home — best idea), DFW Injury Lawyer (scholarship), Jay Murray (jaycares community page) | **Peer-tier playbook.** Build 3-5 lead magnets in Tier 2 anchored on in-lane practice areas + mass-tort. |
| **AI-crawler sitemap (`llms-sitemap.xml`)** | 1/19 — DFW Injury Lawyers only | **Emerging 2026 standard.** Trivial to add via Yoast or manual. P1 future-proof. |
| **Drone delivery accident vertical** | 1/19 — Shamieh (TX + AR + ES) | Emerging tech tort. Stacks with Goff's existing AI Liability page. Worth a 1-page sprint when capacity. |

## Section 5 — Critical site-health issues (unchanged from v1)

Top items damaging Goff's existing SEO right now:

| Issue | Cost | Time to fix |
|---|---|---|
| **6 footer practice-area links return 404** on every page | Bleeding PageRank on 176 pages + visible broken UX | **5 min** — redirect map (full mapping in v1 Section 9) |
| **5 homepage body links 404** | Visible broken anchors | 10 min |
| **WordPress soft-404 problem** — `/attorneys` serves a Galaxy Gas press release | Indexation confusion + duplicate content | 30 min — proper 404 handler + permalink rewrite |
| **3 different URL patterns for city pages coexist** | Splits PageRank | Multi-week migration; or canonical tags as quick win |
| **NO schema.org JSON-LD detected on homepage** | Missing rich-snippet eligibility | 1-2 hrs — LocalBusiness + Attorney + Service schema |
| **NO Privacy Policy, Disclaimer, Accessibility statement** | TX Bar compliance + GDPR/CCPA + ADA exposure | 2-3 hrs total — boilerplate templates |

## Section 6 — Decisions Jim owes (unchanged from v1)

| Decision | What it blocks | Recommendation |
|---|---|---|
| **Case-exclusion contradictions** — Live URLs for medmal, nursing home, premises liability, slip-fall, dog bite | Voice Guide enforcement, Dianne tone, keyword scope | Remove pages OR update case-exclusion memo |
| **Sexual Assault** in homepage body + (broken) footer link | Footer 404 fix; About-page scope | Decide and either build or remove |
| **5-city footprint reality check** — Dallas/Cedar Hill/East Texas/Houston/DeSoto silos but Contact page only lists 1 office | Local SEO + map pack | Audit virtual vs real offices, set canonicals correctly |
| **15 fact-verification flags from briefs** | Dianne drafts | 15-min Jim review |

## Section 7 — Prioritized build list (v2 — revised for 19-firm findings)

### Tier 0 — Ship this week

| # | Task | Time | Why P0 |
|---|---|---|---|
| 1 | **Fix 6 footer 404s** — redirect map | 5 min | Bleeding PageRank on 176 pages |
| 2 | **Fix 5 homepage body 404s** | 10 min | Visible broken links |
| 3 | **Build `/attorneys/jim-goff/` bio page** + `/attorneys/` index | 3-4 hrs | **The single biggest E-E-A-T gap — 19/19 competitors have this** |
| 4 | **Build `/about/` page** with the buried defense-counsel hook promoted (per Homepage Audit) | 3-4 hrs | 17/19 competitors have it |
| 5 | **Build `/practice-areas/` hub** | 2 hrs | Phase 1-5 cross-link target |
| 6 | **Decide on case-exclusion contradictions** | 15 min | Unblocks 4 page-removal/rewrite tasks |
| 7 | **Add Privacy Policy + Disclaimer + Accessibility statement** | 2-3 hrs (boilerplate) | Compliance + legal exposure |
| 8 | **Add Schema.org JSON-LD to homepage** (LocalBusiness + Attorney + Service) | 1-2 hrs | Rich snippet eligibility |

**Tier 0 total: ~16-21 hrs.** Could ship inside 2 weeks if Chelsea + Dianne split.

### Tier 1 — Ship this month

| # | Task | Time |
|---|---|---|
| 9 | **Build `/case-results/` page** (anonymized, Rule 7.02 compliant) | 4-6 hrs |
| 10 | **Build `/testimonials/` page** + GBP review widget | 3-4 hrs |
| 11 | **Ship Phase 1 EN briefs to Dianne** | Dianne-time |
| 12 | **Spanish × mass-tort 4-page sprint** — `/es/abogado-relajante-cabello-dallas/`, `/es/abogado-paragard-iud-dallas/`, `/es/abogado-afff-bomberos-dallas/`, `/es/abogado-galaxy-gas-dallas/`. Native Spanish writer. | ~$300-500/page |
| 13 | **Editorial standards / E-E-A-T page** | 1 hr |
| 14 | **WordPress soft-404 fix** | 30 min - 1 hr |
| 15 | **GBP Review-Gen SOP execution** — backfill 10 closed cases | 1-2 hrs Chelsea + ongoing |
| 16 | **Add `llms-sitemap.xml`** for AI crawlers (emerging 2026 standard) | 15 min — Yoast extension or manual |
| 17 | **Clone Hartley's "Free Safe Ride Home" lead magnet** for DFW. Cheap, news-bait, hyperlocal. | 1 week setup (Uber/Lyft account, intake script, PR plan) |

### Tier 2 — Ship this quarter (moat plays)

| # | Task | Time |
|---|---|---|
| 18 | **Insurance-company-NAMED pages** — 5 to start (State Farm Texas, GEICO Texas, Allstate Texas, Progressive Texas, USAA Texas). **0/19 firms — Jim's defense-counsel background = unique authority.** | ~6-10 hrs Dianne per page |
| 19 | **Hospital-NAMED pages** — 5 to start (Baylor Scott & White Plano, Methodist Mansfield, Texas Health Presbyterian Dallas, Medical City Dallas, Parkland). **0/19 firms.** | ~4-6 hrs Dianne per page |
| 20 | **Federal MDL bellwether tracker** — single live page covering Galaxy Gas + AFFF + Paragard + Hair Relaxer + Tepezza + Suboxone status, updated monthly. **0/19 firms.** | 8-12 hrs initial + 2 hrs/month ongoing |
| 21 | **Lead-magnet library (5 guides)** — Peer-tier playbook (Snellings has 17). Anchor on in-lane practice + mass-tort. E.g., "DFW Truck Accident Insurance Playbook," "Galaxy Gas Settlement Tracker PDF," "Texas SOL Pocket Card," "What to Do After ER Discharge," "Federal MDL Bellwether Quarterly" | 3-5 hrs per guide Dianne + WordPress gated-form plugin |
| 22 | **Bilingual legal glossary** — only 0/19 has the Spanish version. Start with 15-20 most-searched legal terms in Spanish. | 4-5 hrs Spanish writer per 5-term batch |
| 23 | **Pillar guides** — 2-3 (Ultimate DFW Truck Accident Guide, Ultimate DFW Mass Tort Guide). | Dianne 15-20 hrs per pillar |
| 24 | **Drone delivery accident page** (stacks with AI Liability moat — Shamieh just opened this vertical) | 4-6 hrs Dianne |
| 25 | **URL pattern consolidation** (canonical tags or migration) | 1-2 weeks |

### Tier 3 — Ship Q3+

- Court/jurisdiction info pages (Dallas/Tarrant/Collin/Denton)
- Non-case-value utility calculators (SOL, comparative neg, PIP)
- Year-in-review / annual report
- Sub-Dallas neighborhood layer (Pleasant Grove, South Oak Cliff, Bishop Arts, Deep Ellum)
- Video library / TikTok organic test (8 weeks, 2 Jim shorts/week)

---

## Section 8 — Cross-firm matrix (19 firms × 36 page types — full)

**Format:** ✓ = has it / ✗ = missing / ~ = partial. Counts shown for key page types.

### Firms 1-10 (Tier S/A heavy)

| Page type | Reyes | Mullen | Witherite | McCraw | L&S | HamWingo | Snellings | J.Alex | Thompson | Zehl |
|---|---|---|---|---|---|---|---|---|---|---|
| Homepage | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| About | ✓ | ✓ | ✓ | ✓ | ✓ | ✗ | ~ | ✓ | ✓ | ✓ |
| Attorney bios | 30 | 4 | 45 | 11 | 10 | 14 | 4 | 6 | ~15-20 | 17 |
| Why Us | ~ | ✓ | ✓ | ✓ | ✓ | ~ | ✓ | ~ | ✓ | ✓ |
| Practice HUB | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Practice pages | 9+ | 7+ | 6 | 17 | 12+ | 21 | 18 | 16 | 30+ | 25+ |
| Practice × city | 200+ | ✓ | 17 | many | ✓ | ✗ | ✗ | 6 | hundreds | many |
| Standalone cities | 50+ | 5 | ~ | 33+ | 13 | ✗ | 3 | 13 | 60+ TX | 12+ |
| Office hub | ✓ | ✓ | ✓ | ✓ | ✗ | ~ | ✓ | ✓ | ✓ | ~ |
| Spanish | full | ✗ | ✗ | full | full | ✗ | ✗ | ✗ | ~150pg | toggle |
| Bilingual toggle | ✓ | ✗ | ✗ | ✓ | ✓ | ✗ | ✗ | ✗ | ✓ | ✓ |
| Pillar guides | 2 | ✗ | ✗ | ✗ | ✗ | ✗ | 17! | ✗ | ✗ | ✓ |
| Blog/News | ✓ | ✓ | ✓ | ✓ | ✓ | 299 | ✓ | ✓ | 891 | ✓ |
| FAQ | mega | ✓ | ✓ | ✓ | embed | embed | ✓ | ✗ | ~ | atom 80+ |
| Case Results | ✓ | 105 | ✓ | 46 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Testimonials | ✓ | 567 | ✓ | ✓ | ✓ | 24 | ✓ | ✓ | ✓ | ✓ |
| Contact | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Case calc | ✓ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ |
| Lead magnet | ✗ | ✗ | ✗ | ✓ | ✗ | ✗ | **17** | ✗ | ✗ | ~ |
| Legal glossary | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | **✓** |
| Court pages | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ |
| Insurance-named | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ~ | ✗ | ✗ | ✗ |
| Hospital-named | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ |
| Neighborhoods | ✗ | 14 | ✗ | ~ | ✗ | ✗ | ✗ | ✗ | ✗ | 4+ |
| Mass tort/MDL | ✗ | 5 old | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ~13 old |
| MDL tracker | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ |
| Press/Media | ✓ | ✗ | ✓ | ✓ | ✓ | ✓ | ✓ | ✗ | ~ | ✓ |
| Charity | ? | ✓ | ✓ | ✓ | ✗ | ~ | ✓ | ~ | ~ | ~ |
| Careers | ? | ✗ | ✓ | ✓ | ✓ | ✗ | ✓ | ✗ | ~ | ✓ |
| E-E-A-T page | ✓ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ |
| Privacy | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ✓ | ✓ |
| Terms | ✓ | ✗ | ✓ | ✓ | ✗ | ~ | ✗ | ~ | ✓ | ✓ |
| Accessibility | ? | ✗ | ✗ | ✓ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ |
| HTML sitemap | ✗ | ✗ | ✗ | ✓ | ✓ | ✓ | ✗ | ✗ | ~ | ✓ |
| Video library | ✓ | ✗ | ✗ | ✓ | 80+ | 28 | ~ | ✗ | ✓ | ✓ |
| Schema JSON-LD | ✓ | ? | likely | likely | ✓ | ✓ | ~ | ~ | ✓ | ✓ |

### Firms 11-19 (Tier B/C heavy)

| Page type | DFWInjL | Hartley | Mr.Law | Kastl | DFWInjLwr | TedLyon | JayMurray | Shamieh | MAA | **Goff** | **% of 19** |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Homepage | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | 100% |
| About | ✓ | ~ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | **✗** | 89% |
| Attorney bios | 2 | 2 | 8 | ~2-4 | 1 | 10 | 1+ | 4+ | 14 | **✗** | 100% |
| Why Us | ~ | ~ | ✓ | ? | ~ | ✓ | ~ | ~ | ~ | ~ | 79% |
| Practice HUB | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✗ | 95% |
| Practice pages | 10 | 24 | 20 | 10 | 20 | 80+ | 30 | 30 | 25+ | 18 | 100% |
| Practice × city | 80+ | 200+ | ✓ | ? | ✗ | 25+ | ~ | 130+ | 70+ | ~110 | 79% |
| Standalone cities | 6 | 17+ | 22 | 3 | ~ | 10 | 10+ | 18 | 8+ | 5 | 89% |
| Office hub | ✓ | ✓ | ✓ | ~ | ~ | ~ | ✓ | ✓ | ~ | ✗ | 79% |
| Spanish | ~ | ✗ | full | ✗ | ~ | ~ | ~ | full | ~25pg | **✗** | 42% w/full ES |
| Bilingual toggle | ✓ | ✗ | ✓ | ✗ | ✓ | ✓ | ~ | ✓ | ✓ | ✗ | 53% |
| Pillar guides | ✗ | ✗ | ✗ | ? | ✗ | ~ | ✗ | ~ | ~ | ✗ | 16% |
| Blog/News | ✓ | ✓ | ✓ | ? | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | 95% |
| FAQ | ✓ | mega | ~ | ? | ✓ | ✓ | ✓ | ✓ | atomized | ✗ | 84% |
| Case Results | ✓ | ~ | ✓ | ? | ✓ | ✓ | ✓ | ✓ | ✓ | **✗** | 100% |
| Testimonials | ✓ | ✓ | ✓ | ~ | ✓ | ✓ | ✓ | ✓5 | ✓ | **✗** | 100% |
| Contact | ✓ | ✓ | ✓ | ? | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | 100% |
| Case calc | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | 5% |
| Lead magnet | ✗ | ✓ | ✗ | ✗ | ✓ | ~ | ~ | ~ | ✓ | ✗ | 26% |
| **Legal glossary** | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | **27 entries** | ✗ | **11% (was 0%)** |
| Court pages | ✗ | ✗ | ✗ | ✗ | ✗ | ~ | ✗ | ✗ | ~ | ✗ | 0% (true court) |
| Insurance-named | ✗ | ✗ | ✗ | ✗ | ~ | ~ | ~ | ✗ | ~ | ✗ | **0% (named)** |
| Hospital-named | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ~ | ✗ | ✗ | ✗ | **0%** |
| Neighborhoods | ~ | ✗ | ~ | ✗ | ✗ | ✗ | 8 | ✗ | 9 | ~ | 21% |
| Mass tort/MDL | ~ | ✗ | ~ | ✗ | ✗ | 2 | ✗ | ~ | ✗ | **15+ current** | 21% (Goff wins) |
| MDL tracker | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | **0%** |
| Press/Media | ~ | ✗ | ✓ | ~ | ~ | ✓ | ✗ | ✓ | ~ | ~ | 63% |
| Charity | ✗ | ~ | ✗ | ? | ~ | ✗ | ✓ | ✓ | ✓ | ✗ | 53% |
| Careers | ✗ | ✗ | ✗ | ? | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | 26% |
| E-E-A-T page | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ | 5% |
| Privacy | ✓ | ✗ | ✓ | ? | ✓ | ✓ | ✓ | ✓ | ✓ | **✗** | 89% |
| Terms | ✓ | ✓ | ~ | ? | ✓ | ✓ | ✓ | ✗ | ✓ | ✗ | 63% |
| Accessibility | ✗ | ✗ | ✗ | ? | ✗ | ✗ | ✓ | ✗ | ~ | ✗ | **16%** |
| HTML sitemap | ✓ | ~ | ✓ | ? | ✓ | ✓ | ✗ | ✗ | ✓ | ✓ | 47% |
| Video library | ✓ | ~ | ✓ | ? | ✗ | ✓ | ✓ | ✓ | ✓ | ✗ | 58% |
| Schema JSON-LD | likely | likely | likely | likely | ? | likely | likely | likely | likely | **✗** | likely 95%+ |

### Single-firm differentiators worth stealing or noting

| Firm | Differentiator | Steal-worthy? |
|---|---|---|
| **Hartley Law** | `/free-uber-lyft-cab-rides/` lead magnet | **YES — Tier 1 build** |
| **DFW Injury Lawyers** | `llms-sitemap.xml` (AI crawler sitemap) | **YES — Tier 1 (15 min)** |
| **Shamieh Law** | Drone delivery accident vertical (TX + AR + ES) | YES — Tier 2 (stacks with AI Liability) |
| **Snellings** | 17-guide lead-magnet library | YES — peer-tier playbook, Tier 2 |
| **MAA Anderson** | Atomized city × practice × FAQ | Goff was planning this — adjust to bilingual + mass-tort FAQ angles |
| **MAA Anderson** | 27-entry legal glossary | Goff should ship bilingual version (0/19 in Spanish) |
| **Zehl** | Atomized FAQ with 80+ URLs across 12 topic silos | Confirms FAQ atomization ceiling is much higher than v1 planned |
| **Mr. Law** | "Third-Party Crimes" practice page (shootings/assaults/negligent security) | Maybe — narrows lane |
| **Mr. Law** | "Tractor overturn" as separate motor-vehicle category | No — too niche |
| **Ted Lyon** | Pipeline explosion vertical (10 pages) | No — oil-and-gas isn't Goff's lane |
| **Ted Lyon** | Mesothelioma 9-page clinical stack | No — asbestos not in lane |
| **Jay Murray** | `/jaycares/` branded community page | YES — promote Goff's community involvement once decided |
| **Jay Murray** | 8 Dallas neighborhood pages (Bishop Arts, Deep Ellum, etc.) | YES — Q3 sub-Dallas neighborhood expansion |
| **MAA Anderson** | 18 anatomical injury-type pages (back, amputation, broken bones, etc.) | Maybe — clinical content depth |
| **DFW Injury Lawyer** | "What is my case worth" page in top-nav (not interactive calc, just guidance) | Maybe — bridges to utility-calc moat |
| **Mr. Law** | Case Management System as nav item (tech transparency play) | Maybe — Bill AI Machine could be the equivalent |
| **DFW Injury Lawyers** | Clergy abuse mass-litigation specialty | No — Aldous owns sexual abuse |
| **Witherite** | Vanity domain (1800truckwreck.com) | No — Jim handles compliance, but doesn't fit voice |
| **Zehl** | `wpseo_locations-sitemap.xml` + `geo-sitemap.xml` | YES — Yoast Local SEO Pro, ~$99/year, geographic structured-data trust |

## Section 9 — The single Monday move

**Fix the 6 footer 404s. 5 minutes.** Set up redirects:

| Dead URL (footer link) | Live destination |
|---|---|
| `/dallas-sexual-assault-attorney/` | `/dallas-personal-injury-lawyer/sexual-assault-lawyer/` |
| `/hair-relaxer-lawsuits/` | `/dallas-personal-injury-lawyer/product-liability/hair-relaxers/` |
| `/car-accidents/` | `/dallas/car-accident-lawyer/` |
| `/dallas-electric-scooter-accident-attorney/` | `/dallas-personal-injury-lawyer/electric-scooter-accident/` |
| `/truck-accidents/` | `/dallas/truck-accident-lawyer/` |
| `/dallas-brain-injury-attorney/` | `/dallas-personal-injury-lawyer/catastrophic-injury/dallas-brain-injury-attorney/` |

Use Rank Math Redirect / Redirection plugin / .htaccess 301s. Every visitor and every crawler sees a working footer. Highest leverage / lowest effort move on the entire site — unchanged from v1.

---

## Confirmed firm URLs (all 19)

| # | Firm | URL | Tier |
|---|---|---|---|
| 1 | Angel Reyes & Associates | reyeslaw.com | S (Latino DFW volume king) |
| 2 | Mullen & Mullen | mullenandmullen.com | S (29% contingency hook) |
| 3 | Witherite Law Group | witheritelaw.com | A (1-800-CAR-WRECK + trucking) |
| 4 | McCraw Law Group | mccrawlawgroup.com | A (full Spanish + 6 NTX offices) |
| 5 | Lyons & Simmons | lyons-simmons.com | A (catastrophic + $1B since 2023) |
| 6 | Hamilton Wingo | hamiltonwingo.com | S ($7.3B Charter verdict) |
| 7 | Snellings Law | snellingsinjurylaw.com | B (Frisco specialist; 17-guide library) |
| 8 | J. Alexander Law | severeinjurylawyers.com + caraccidentlawyersnow.com | B (sports-partner branding) |
| 9 | Thompson Law | 1800lionlaw.com | A national (60+ TX cities + 4 states + Spanish duplicate) |
| 10 | Zehl & Associates | zehllaw.com | S out-of-DFW (Houston catastrophic) |
| 11 | DFW Injury Lawyers | dfwinjurylawyers.com | B (Kevin Edwards + Peter de la Cerda; clergy abuse) |
| 12 | Hartley Law TX | hartleylawtx.com | C (suburb-saturation SEO with free safe-ride magnet) |
| 13 | Mr. Law | mr.law | A (8 attorneys, TX + IL, full ES parity) |
| 14 | Kastl Law | kastllaw.com | B (Krisi Kastl, women-owned, 20+ yrs, 100+ trials) |
| 15 | DFW Injury Lawyer | dfwinjurylawyer.com | B (Jerry Andrews, solo + Board Cert) |
| 16 | Ted Lyon & Associates | tedlyon.com | A (10 attorneys, 10 TX offices, pipeline/oilfield) |
| 17 | Jay Murray Law | jaymurraylaw.com | B (3 offices + Dallas neighborhoods + branded community) |
| 18 | Shamieh Law | shamiehlaw.com | A (TX+LA+AR, 4 attorneys, drone delivery niche) |
| 19 | MAA Firm / Anderson Injury Lawyers | maafirm.com | A (14 attorneys, 5 offices DFW+Austin, 27-entry glossary + atomized FAQ) |

---

## Sources

- **Goff URL inventory:** Live audit 2026-05-17 via sitemap_index.xml + 30+ targeted URL fetches
- **Competitor inventory (live fetches 2026-05-17):** reyeslaw.com (Phase 2 deep recon), mullenandmullen.com, witheritelaw.com, mccrawlawgroup.com, lyons-simmons.com, hamiltonwingo.com, snellingsinjurylaw.com, severeinjurylawyers.com, 1800lionlaw.com (Phase 1+2 recon, live HTML gated), zehllaw.com, dfwinjurylawyers.com, hartleylawtx.com, mr.law, kastllaw.com (partial — site hardened), dfwinjurylawyer.com, tedlyon.com, jaymurraylaw.com, shamiehlaw.com, maafirm.com
- **Phase 1 recon docs for prior 9 firms** (recon/[firm]/PHASE-1-RECON-REPORT.md) — cross-validation
- **Companion docs:** Voice Guide v1, Homepage Voice Audit, Reyes Phase 2 deep recon + Spanish + reviews
