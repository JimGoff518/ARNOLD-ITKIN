# Angel Reyes & Associates — Phase 2 Deep Recon Report

**Target:** Angel Reyes & Associates (real site: `https://www.reyeslaw.com/`)
**Recon date:** 2026-05-17
**Method:** 7 WebFetch + 4 WebSearch, building on Phase 1 (2026-05-14)
**Brand domain note:** `angelreyeslaw.com` is a parked domain currently for sale via Spaceship ($1,999 BIN). The operating brand domain is `reyeslaw.com`. Brand-variant domain defense gap.

---

## 1. Executive summary (7 things Goff most needs to know)

1. **The "/es/" Spanish site is a native adaptation, NOT a translation.** H1s use colloquial Mexican-Spanish ("¿Accidente de Auto o Camión? Recibe El Dinero Que Mereces"), idiomatic phrasing, and a USA-flag/Mexico-flag language toggle. The /es/dallas/ page is ~3,500-4,000 words with localized H2s, native Spanish FAQs, Spanish-named attorneys featured first, and case results in Spanish. **This is not Google-translated WordPress** — it's a parallel content track. Goff cannot beat this with a Weglot plugin; he needs native Spanish-authored content.

2. **The Case Calculator is their highest-leverage conversion tool, and it's a 3-step funnel with a 15-minute speed-to-lead promise.** The funnel: (Step 1) accident type + fault %, (Step 2) injuries, (Step 3) damages. It outputs an "Attorney-Negotiated Settlement Estimate" and gates fault % at 51% (Texas modified comparative negligence rule). Contact form appears AFTER the estimate, with the explicit promise: *"A case specialist will call you within 15 minutes during business hours."* A Spanish version ("Calculadora de Casos") runs in parallel. **This is the only tool in the DFW competitor set that produces a number BEFORE asking for contact info** — a textbook reciprocity-based conversion design. Goff has no analog.

3. **The site footprint is ~440+ URLs across 7 sitemaps**, with ~250 location/city pages and ~70+ Spanish pages. Page-sitemap1 (~175 URLs) and page-sitemap2 (~170 URLs) are dominated by `[city]/[practice-area]/` permutations — e.g., `/houston/truck-accidents/`, `/dallas/car-accidents/`, `/mckinney-personal-injury-lawyers/`. They're not just running 16 office cities — they have pages for Rosenberg, Rockwall, Port Arthur, Pflugerville, Killeen, Galveston, Marshall, Lufkin, Longview, Laredo, and dozens more. **Reyes is running a programmatic SEO play across all of Texas, not just DFW.**

4. **Intake form is deliberately minimal (4 fields: First/Last/Email/Phone + optional message).** No qualifying questions. No accident-date dropdown. No injury-severity radios. No police-report toggle. This is a pure volume-capture design — they pre-qualify on the phone, not on the form. **Goff's intake form should mirror this minimalism for the same demo; qualifying friction kills working-class first-time-user conversion.**

5. **Speed-to-lead is the headline conversion promise. Two stated SLAs in tension:**
   - Generic contact page: *"one of our attorneys will contact you within 24 hours"*
   - Case Calculator: *"A case specialist will call you within 15 minutes during business hours"*
   The 15-minute promise is reserved for the calculator funnel (their hot leads). The 24-hour promise covers the cold form. **Goff should ship a single tighter promise — "Real attorney on the phone in under 10 minutes, 24/7" — and beat both Reyes SLAs by being attorney-first, not specialist-first.**

6. **Reyes has NO mass-tort presence (confirmed Phase 1; reaffirmed in Phase 2 sitemap audit).** Zero Galaxy Gas, AFFF, Tepezza, Paragard, Suboxone, hair relaxer, AI liability pages found in any sitemap. Page-sitemap3 is heavy on truck-subtype permutations (flatbed, dump, tow, box, tanker, jackknife, underride, garbage, overloaded cargo) — they're going deep on commercial trucking, not on federal MDLs. **Goff's emerging-tort organic moat is still uncontested by Reyes. This is the single biggest unfair advantage Goff has in the DFW market.**

7. **Case Calculator + 31-question FAQ + Spanish parity = a complete conversion stack purpose-built for first-time lawyer users.** The FAQ has 31 questions across 8 categories addressing the exact "I've never hired a lawyer before, what do I do" questions Goff's ICP types into Google. Reyes is winning intent search on educational queries, then converting via calculator + 15-min callback. **Goff's FAQ-page niche stack (from the Alventra prompt subset) maps directly onto Reyes's territory — this is where Goff can compete on intent.**

---

## 2. Website + hero architecture

### 2.1 Real domain vs. parked domain
| Domain | Status | Implication |
|---|---|---|
| `reyeslaw.com` | Live brand site, WordPress, English+Spanish toggle | Real target |
| `angelreyeslaw.com` | Parked at Spaceship — "Buy Now $1,999" | Brand-protection gap |

### 2.2 English hero (reyeslaw.com)
- **H1:** "Car or Truck Accident?"
- **Subhead:** "Get The Money You Deserve"
- **Hero image:** attorney comforting client (emotional, not aspirational)
- **Primary CTA:** "CONTACT US" → contact form
- **Header phone:** 469-289-1910 (click-to-call, sticky)
- **Above-fold trust signals:** $1 Billion+ Recovered · 30+ Years · 16 Offices · 15,000+ Five-Star Google Reviews
- **Language toggle:** prominent (USA flag / Mexico flag)
- **Footer:** 16 offices, newsletter signup, social (IG, FB, LI, YT, **TikTok**)

### 2.3 Spanish hero (/es/)
- **H1:** "¿Accidente de Auto o Camión?"
- **Subhead:** "Recibe El Dinero Que Mereces"
- **Primary CTA:** "Evalúa tu caso gratis"
- **Phone:** 469-289-1910 labeled "LLAMA HOY" (same number — no separate Spanish line)
- **Trust signals:** "$1 Billion + Recuperado", "AS SEEN ON" media logos, 15,000+ Google reviews
- **Urgency phrases:** "LLAMA HOY", "Consulta gratis 24/7", "Disponible 24/7"

### 2.4 Site architecture map

```
reyeslaw.com/
├── / (homepage, EN)
├── /es/ (homepage, ES)
├── /about-us/, /attorneys/ (~30 attorney bios)
├── /contact-us/
├── /case-calculator/  ← KEY CONVERSION TOOL
├── /faq/ (31 questions, 8 categories)
├── /case-results/
├── /office-locations/
│
├── /[city]/ ← ~50+ city hub pages
├── /[city]/[practice]/ ← ~200+ city×practice combos
├── /[city]/truck-accidents/[truck-subtype]/ ← deep nesting
│
├── /es/[city]/ ← Spanish city hubs
├── /es/[city]/[practice]/ ← Spanish city×practice
├── /es/calculadora-de-casos/
├── /es/abogados/, /es/contactenos/, /es/sobre-nosotros/
├── /es/testimonios-de-clientes-reales/
│
├── /attorneys/[name]/ ← ~30 attorney profile pages
├── /blog/ (active, multiple posts/week)
├── /ultimate-truck-accident-guide-in-texas/ ← pillar
├── /ultimate-car-accident-guide-in-texas/ ← pillar
└── /meta-lp-car-accident-case-calculator/ ← Meta-ads paid LP
```

**Goff equivalent estimate:** ~100 URLs total per Phase 1. Reyes is **4-5x larger** by page count.

### 2.5 Schema / tech
- WordPress (confirmed via asset paths)
- Yoast SEO pattern
- Active publishing cadence — sitemaps updated multiple times per week
- Dedicated `video-sitemap.xml` (YouTube SEO investment)
- Footer includes editorial-standards link (E-E-A-T signal)

---

## 3. Intake + funnel mechanics

### 3.1 Contact form (/contact-us/)
**Just 4 required fields:** First Name, Last Name, Email, Phone.
**Plus:** Optional Message, Terms checkbox, SMS opt-in with STOP language, honeypot anti-bot field, privacy note.

**What's NOT on the form:** No accident date, no injury severity, no police-report Y/N, no fault dropdown, no insurance question, no qualifying disclosures.

**Implication:** They've deliberately removed friction. Pre-qualification happens on the phone with intake staff — not on the web form. This is the right design for a volume-PI working-class demo where any extra field drops conversion 5-10%.

### 3.2 Phone-first architecture
- Header phone is sticky on both EN and ES sites
- Same number (469-289-1910) serves both English and Spanish
- "Available 24/7" / "Disponible 24/7" displayed prominently
- "Walk-ins welcome" + 24-hour open offices (per Phase 1)
- "It's Free to Get Started" / "No Fee Unless We Win" repeated 8+ times on Dallas page

### 3.3 The Case Calculator — their best conversion asset

**3-step progressive funnel:**

| Step | Inputs | Friction reduction |
|---|---|---|
| 1 | Accident type, your fault % | Front-loads the easy question |
| 2 | Injury type, severity, treatment | Pain-point engagement (sunk cost) |
| 3 | Medical bills, lost wages, property damage | Numeric inputs (commitment escalation) |

**Output before contact capture:**
- "Attorney-Negotiated Settlement Estimate $0" updating live
- Both economic damages and pain/suffering shown separately
- Gate: if user is 51%+ at fault → "Texas follows the 51% bar rule" message blocks results (turns away unqualified leads + delivers legal education)

**Contact capture AFTER estimate:**
- First, Last, Email, Phone, optional Description
- **Promise: "A case specialist will call you within 15 minutes during business hours"**
- Disclaimer: "This estimate is a starting point — an attorney can evaluate your specific case"

**Why this works on the Goff ICP:**
- Working-class users don't trust "free consultation" alone — they want to know "is my case worth anything?"
- Reciprocity: user receives a number → feels owed → submits contact
- Spanish parallel funnel at `/es/calculadora-de-casos/`
- Meta-ads landing page (`/meta-lp-car-accident-case-calculator/`) confirms paid traffic funnels here

### 3.4 Speed-to-lead SLAs (bifurcated — note the asymmetry)
| Source | Promise |
|---|---|
| Generic contact form | "Attorney will contact you within 24 hours" |
| Case Calculator | "Case specialist will call within 15 minutes during business hours" |

**Read:** Calculator leads are flagged as HOT (already qualified themselves by completing 3 steps) and get human treatment in 15 min. Cold form leads get 24-hour SLA. **Goff opportunity:** a single tight attorney-first SLA on every channel beats their bifurcated promise.

### 3.5 Chat widget
**Not observed in WebFetch.** Inconclusive — Goff should verify in a real browser session.

---

## 4. Paid media observations

### Hard constraints
WebSearch returns organic + AI-summarized results, **not the live Google SERP with paid-ad labels.** Cannot directly observe ad creative, spend, or impression share.

### 4.1 Paid-ad infrastructure signals on their site
- **Meta landing page exists:** `/meta-lp-car-accident-case-calculator/` — explicit confirmation they run paid Meta traffic into the Case Calculator funnel
- **TikTok in social footer** — testing TikTok creative, possibly organic + paid
- **Video sitemap** — suggests YouTube presence, likely with TrueView paid distribution
- **WordPress + Yoast** with aggressive city-pages suggests Google Ads to those landing pages

### 4.2 SERP organic competitive observations

**"car accident lawyer Dallas":** Reyes did NOT appear in top organic results. Likely competing via paid/map pack, not organic head terms.

**"personal injury lawyer Plano Texas":** Mullen owns Plano organic. Reyes's `/plano/` page exists (2,500 words) but isn't winning the SERP for head terms.

**"abogado lesiones personales Plano":** Top organic includes Texas Law Dog, Tate Law, Zinda, McCraw, Fell Law, Los Defensores, abogados.com (Morgan & Morgan). **Reyes did NOT appear here either.** Despite their /es/ investment, they're losing Plano Spanish organic.

**"abogado de accidentes Dallas Reyes" (branded):** They dominate.

### 4.3 Strategic inferences
- Reyes appears to win on **brand + map pack + paid**, NOT on unbranded organic head terms
- Their /es/ content is deep BUT is not winning Spanish head-term SERPs against Texas Law Dog, Zinda, Tate
- **Spanish PI organic is genuinely contested — Reyes is not unbeatable there**

---

## 5. SEO content map + identified gaps

### 5.1 Confirmed content inventory

| Category | Approx. count | Examples |
|---|---|---|
| City landing pages (EN) | ~50 | Dallas, Houston, Austin, FW, Plano, Frisco, McKinney, Arlington, Mesquite, Irving + ~40 secondary TX cities |
| City × practice-area pages (EN) | ~200 | `/houston/truck-accidents/`, `/dallas/car-accidents/`, `/mckinney-personal-injury-lawyers/` |
| Truck-subtype deep pages | ~15+ | flatbed, dump, tow, box, tanker, jackknife, underride, garbage, overloaded cargo |
| Injury-type pages | ~10+ | brain injury, spinal cord, burn, whiplash, paralysis, amputation, broken bones |
| Spanish (/es/) pages | ~70+ | Mirror of EN; native-written, not auto-translated |
| Practice-area hubs | 9 | car, truck, motorcycle, rideshare, bus, pedestrian, bicycle, premises, wrongful death |
| Attorney profile pages | ~30 | Per Phase 1 |
| Pillar guides | 2 | Ultimate Truck Accident Guide TX, Ultimate Car Accident Guide TX |
| FAQ | 1 (~3,000 words, 31 Qs, 8 categories) | See §5.2 |
| Tools | 1 (Case Calculator + Spanish version) | High-converting |
| Blog posts | Active, ~weekly cadence | Sitemap last-modified 2026-05-15 |
| Video pages | Dedicated video-sitemap | YouTube content library |
| Office-locations hub | 1 | Lists all 16 |
| Meta paid LP | 1 | `/meta-lp-car-accident-case-calculator/` |

**Total estimated URLs:** ~440+ across 7 sub-sitemaps.

### 5.2 The 31-question FAQ (their educational SEO play)

31 questions across 8 categories (PI general, Car, Truck, Rideshare, Motorcycle, Car Insurance, Truck Insurance). **All in one mega-page.**

**Goff opportunity:** Per the Alventra prompt subset, Goff's plan is to build a FAQ question-stack niche site. **The Reyes FAQ is NOT optimized as a niche stack** — it's a consolidated mega-page. Goff can outrank them by building **one URL per question** with deep schema markup. The FAQ-pages niche is genuinely available because Reyes consolidated rather than fragmented.

### 5.3 Identified content gaps (Goff opportunities)

| Gap | Reyes status | Goff move |
|---|---|---|
| Galaxy Gas / nitrous oxide | ❌ Zero pages | Defend + expand — uncontested |
| AFFF / firefighting foam | ❌ Zero pages | Federal mass tort — Goff plays, Reyes doesn't |
| Tepezza, Paragard, Suboxone, hair relaxers | ❌ Zero pages | Same |
| AI Liability | ❌ Zero pages | Emerging — first-mover |
| Spanish × mass tort | ❌ Zero | **Highest-value untouched intersection** — stacks 2 of Jim's 4 niche-stack pillars |
| Individual FAQ URLs (one Q = one URL) | ❌ Consolidated mega-page only | Build one URL per high-intent question with FAQPage schema |
| Oilfield / industrial / construction | ❌ Zero | If Goff expands here, no Reyes contest (Lyons & Simmons is the competitor) |
| Federal MDL bellwether tracker pages | ❌ Zero | Goff's mass-tort moat |
| Hospital-named landing pages | ❌ Zero (Plano page names no hospitals) | "Injured at Baylor Scott & White Plano" / "Injured at Methodist Mansfield" pages |
| Neighborhood landing pages within Dallas/Plano | ❌ Plano page names no Legacy / Willow Bend / Collin Creek | Goff can micro-segment |

### 5.4 Where Reyes IS strong (don't try to compete head-to-head)
- City × practice matrix (200+ pages, years of authority)
- 30 attorney profile pages with schema
- Pillar truck/car accident guides (10,000+ word equivalents)
- Active blog cadence (multiple posts/week)
- Video sitemap with YouTube content
- 15,000+ Google reviews (multi-year unmatchable per Phase 1)

---

## 6. Strategic implications for Goff Law DFW

### 6.1 Copy (steal these tactics outright)

1. **Build a 3-step Case Calculator with a 15-minute callback promise.** Single best conversion asset; Goff has no analog. Build EN + ES from day one. Output a settlement estimate range, then capture contact. Add the 51%-fault gate to filter unqualified leads. **Ship before Q4.**
2. **Minimal 4-field intake form everywhere.** First, Last, Email, Phone. Optional Message. SMS opt-in. Honeypot. Nothing else. Kill any existing Goff form that has 6+ fields.
3. **One sticky phone number visible on every page, both EN and ES.** Pick one DID and never let any page render without a sticky click-to-call.
4. **Native Spanish content — not Weglot, not Google Translate.** If Goff plays in /es/ at all, hire a bilingual content writer with Mexican-Spanish PI fluency.
5. **TikTok presence (organic at minimum).** Even one Jim-on-camera short per week is a starter for the 25-55 mobile-first ICP.
6. **Editorial-standards page in footer.** Cheap E-E-A-T signal.

### 6.2 Counter (do the OPPOSITE)

1. **Single tight speed-to-lead promise: "Real attorney on the phone in under 10 minutes, 24/7."** Goff's small team is an ADVANTAGE — Jim or an attorney can answer the phone, not a "case specialist." Lead with that.
2. **Senior-attorney-attention positioning** ("Not a case factory"). Reyes runs 30+ attorneys on volume. Frame as: *"You'll talk to the same attorney every time, not a different paralegal."*
3. **Big-verdict-per-attorney metric.** Reyes's largest case displayed is $30M; average per client is ~$18K. Goff's mass-tort wins will individually exceed Reyes's average. Lead with case-quality, not case-quantity.
4. **Atomize the FAQ.** Build 31+ individual FAQ URLs with FAQPage schema, deep answers (1,200-1,500 words each), internal linking.

### 6.3 Differentiate (own white space)

1. **Spanish × mass tort.** Reyes has Spanish PI. Reyes has NO mass tort. Spanish-language Galaxy Gas, AFFF, Paragard pages = uncontested in DFW and likely in Texas. **Single highest-leverage move** — stacks 2 of Jim's 4 niche-stack pillars.
2. **Mass-tort city pages.** `/dallas/galaxy-gas-lawyer/`, `/plano/afff-lawyer/`, `/houston/paragard-lawyer/` — don't compete with Reyes (zero presence); compete with national MDL aggregators who don't have local credibility.
3. **Hospital-named landing pages.** "Injured at Methodist Mansfield" / "Injured at Texas Health Presbyterian Dallas" — target post-ER search behavior.
4. **Federal MDL bellwether tracker.** Static page Reyes will never build. Goff can be the local DFW source for AFFF / Paragard / Hair Relaxer bellwether status.

### 6.4 Brand defense

- **`angelreyeslaw.com` is for sale at Spaceship for $1,999.** Third-party squatter listing. Goff almost certainly **should not buy this** (cybersquatting exposure), but worth flagging that Reyes hasn't locked down their brand-variant domain. Goff should ensure all his own brand-variants (`gofflawdfw.com`, `gofflawtexas.com`, `gofflawdallas.com`, common misspellings) ARE locked down.

---

## 7. Recommendations for Phase 6

### Tier 1 — ship this month
1. **Build a Case Calculator MVP** (EN first, ES in v2). 3 steps, settlement estimate, 51%-fault gate, then capture First/Last/Email/Phone + 10-min callback promise. **Estimated:** 2 weeks dev + 1 week copy + 1 week QA. Conversion lift target: 2-3x vs baseline.
2. **Atomize Goff's FAQ into one-URL-per-question.** Build 30 dedicated FAQ pages, each 1,200-1,500 words, FAQPage schema. This IS one of Jim's 4 niche-stack pillars.
3. **Strip Goff's intake form to 4 fields + SMS opt-in.** Whatever's there now, kill the qualifying questions.

### Tier 2 — ship next month
4. **Spanish × mass tort content sprint** — 10 Spanish landing pages (`abogado-galaxy-gas-dallas`, `abogado-afff-dallas`, `abogado-paragard-dallas`, `abogado-hair-relaxer-dallas` plus Houston, Plano, FW variants). Native Spanish writer.
5. **TikTok organic test** (8 weeks, ~2 shorts/week). Jim on camera answering one FAQ per video. 16 shorts at zero paid.
6. **Hospital-named landing pages** (5 to start): Baylor Scott & White Plano, Methodist Mansfield, Texas Health Presbyterian Dallas, Medical City Dallas, Parkland.

### Tier 3 — ship Q3
7. **Federal MDL bellwether tracker page** (Galaxy Gas + AFFF + Paragard + Hair Relaxer). Updated monthly.
8. **Editorial-standards / E-E-A-T page** in footer.
9. **Lock down Goff brand-variant domains.** ~$50/year insurance.

### Don't build (yet)
- **Don't build a 50-city × 9-practice page matrix.** Reyes has 4-5 years of authority. Stay in niche stacks.
- **Don't chase Reyes on Google review velocity.** 15K is multi-year unmatchable. Compete on Avvo, Best Lawyers, per-case-result PR instead.
- **Don't build a Spanish duplicate of the entire English site.** Build a Spanish niche site at /es/ focused on mass tort + 10-15 high-value PI pages.

---

## Phase 2 followups (open for Phase 3)

1. Live chat verification (browser session)
2. Real Google SERP scrape with paid-ad inspection (clean Chrome profile in DFW geo)
3. Ahrefs/SEMrush on reyeslaw.com — top organic queries, DA, paid keyword spend, backlinks
4. GBP audit on Reyes Dallas listing — review velocity, response rate, post cadence, photos
5. Audit which of the 16 offices are real vs. virtual/coworking
6. Meta ad library verification for active Reyes campaigns

---

## Sources (live recon, 2026-05-17)

- reyeslaw.com homepage + /es/ + /contact-us/ + /dallas/ + /es/dallas/ + /plano/ + /case-calculator/ + /faq/ + sitemap.xml + page-sitemap1-3.xml
- SERP probes: site:reyeslaw.com, car accident lawyer Dallas, personal injury lawyer Plano Texas, abogado de accidentes Dallas Reyes, abogado lesiones personales Plano
- Phase 1 artifact: `recon/angel-reyes/PHASE-1-RECON-REPORT.md`
