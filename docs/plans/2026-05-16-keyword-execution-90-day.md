# Goff Law 90-Day Keyword Execution Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan phase-by-phase.

**Goal:** Ship 30-45 organic-only landing pages over 90 days that win uncontested keyword positions and pull DFW PI leads at $0 paid spend.

**Architecture:** Five sequential content stacks executed in a fixed priority order. Each page = one keyword cluster + one published URL on gofflawdfw.com + one schema block + one internal link map update. Sequence is non-negotiable per [feedback-phase-order memory](../../C:/Users/jim/.claude/projects/c--Users-jim-OneDrive-Documents-ArnoldItkin/memory/feedback_phase_order.md) — close each phase fully before starting the next.

**Source data:** `c:\Users\jim\OneDrive\Documents\ArnoldItkin\DFW_Personal_Injury_Keyword_Research.md` (838 lines, 9 sections).

## Phase 0 — Prereqs (parallel, can start immediately)

- **Task 0.1 — Spanish keyword pull:** Generate a 100-200 keyword Spanish-language DFW PI dataset mirroring the English source's structure (head terms, FAQ questions, mass-tort × city). Output: `recon/goff-law/SPANISH-KEYWORDS-2026-05-16.md`. Unblocks Phase 1b.
- **Task 0.2 — TxDOT crash data pull:** Pull TxDOT CRIS data for: I-35 (Dallas County), I-20 (Dallas County), I-30 (Tarrant County), I-635/LBJ. Need: annual crash count, fatality count, top crash sub-types (rear-end, jackknife, etc.) for last 3 years. Output: `recon/goff-law/TXDOT-CORRIDOR-DATA-2026-05-16.md`. Unblocks Phase 2.

## Phase 1b — Spanish FAQ Pages (parallel to Phase 1, days 15-45)

Triggers after Task 0.1 completes. Ship 5-8 Spanish-language FAQ pages mirroring the English Phase 1 patterns. Hreflang tags required. Internal-link the Spanish version from each English FAQ via `<link rel="alternate" hreflang="es-us">`.



**Strategy filter (per memory):**
- NO paid channel work (no Google PPC, no Meta Ads)
- EXCLUDE keyword categories Goff doesn't take: med mal, nursing home, dog bite, workers comp, birth injury, generic slip-fall
- Frame against PEER tier (Snellings, J. Alexander) NOT Tier S (Mullen, Reyes, Hamilton Wingo)
- Mullen & Mullen = the REAL organic threat for everything suburb-related

**Tech stack:** WordPress (existing gofflawdfw.com), Rank Math or Yoast for on-page SEO, schema.org LegalService + FAQPage + LocalBusiness JSON-LD, no new infrastructure.

---

## Phase 1 — FAQ Question Pages (Days 1-30)

**Why first:** Largest aggregate volume at lowest difficulty. 2,500/mo across 10 pages, all rated "Low" competition in the dataset. Fastest organic ranking timeline (45-75 days from publish).

**Volume target:** 10 pages published.

**Files:**
- Create (10): `gofflawdfw.com/faq/[slug]/` — WordPress page in new "Resources > FAQ" parent
- Modify: `gofflawdfw.com/sitemap.xml` (auto via Rank Math)
- Update: internal link map — every existing practice-area page gets 1 link to the most-relevant FAQ page

### Task 1.1: Build FAQ content brief

**Files:**
- Create: `recon/goff-law/FAQ-CONTENT-BRIEF-2026-05-16.md`

**Step 1: Pull the 10 target keywords from source data**

Read source: `c:\Users\jim\OneDrive\Documents\ArnoldItkin\DFW_Personal_Injury_Keyword_Research.md`, Section 5.

Confirmed 10 targets (all Low competition):
1. what to do after a car accident in texas — 480/mo
2. how much is my personal injury case worth — 390/mo
3. how long do i have to file personal injury claim texas — 290/mo
4. how much do personal injury lawyers charge in texas — 280/mo
5. should i hire a personal injury lawyer — 210/mo
6. should i accept first settlement offer — 180/mo
7. what to do if injured at work texas — 170/mo (REFRAMED: H1 = "What To Do If You're Injured at Work in Texas (When It's NOT Workers' Comp)" — covers third-party negligence routes, 1099 cases, employer non-subscribers; stays in Goff's lane)
8. who pays medical bills after car accident texas — 150/mo
9. how much can you sue for pain and suffering in texas — 190/mo
10. when to get a lawyer after car accident — 220/mo

**Step 2: Draft brief structure for each page**

For each: H1 (exact-match question), 1,200-1,800 words, 5-8 H2 sub-questions (pull from People Also Ask), schema FAQPage block, one CTA module, one related-articles module pointing to 2 other FAQ pages.

**Step 3: Commit brief**

Save to `recon/goff-law/FAQ-CONTENT-BRIEF-2026-05-16.md` — show Jim for sign-off before any page is written.

### Task 1.2: Write FAQ page #1 (highest volume — "what to do after a car accident in texas")

**Files:**
- Create: WordPress page `/faq/what-to-do-after-car-accident-in-texas/`
- Create: schema FAQPage JSON-LD in page header

**Step 1: Draft full page copy** (1,500 words target)

Sections:
1. H1: "What To Do After a Car Accident in Texas: Step-by-Step Guide"
2. H2: Immediate steps (call 911, get to safety, photograph scene)
3. H2: What to say to the other driver (and what NOT to say)
4. H2: When to call police vs. exchange info
5. H2: Texas-specific reporting requirements (CR-3 form)
6. H2: First 48 hours: medical care + insurance notification
7. H2: When to call a lawyer (and why timing matters in Texas)
8. CTA module: "Free consultation — DFW only"

**Step 2: Build FAQPage schema**

JSON-LD block with the H1 question + 5-8 sub-questions matched to H2s.

**Step 3: Publish + verify**

Run: rich-results test via search.google.com/test/rich-results
Expected: FAQ rich snippet eligible.

**Step 4: Add internal links**

From these existing pages, add one contextual link to the new FAQ page:
- `/practice-areas/car-accident/`
- `/blog/` index
- Homepage "Resources" footer block

**Step 5: Commit**

Document the publish in `recon/goff-law/FAQ-PUBLISH-LOG.md` with URL, publish date, target keyword, schema verification screenshot link.

### Tasks 1.3 through 1.10: Repeat Task 1.2 pattern for remaining 9 FAQ pages

Same structure. Ship at ~1 page every 2-3 days. Target: all 10 published by Day 28.

### Task 1.11: Phase 1 close-out

**Step 1: Verify all 10 pages indexed**

Run: GSC URL inspection on each. Expected: all 10 in Google's index.

**Step 2: Confirm schema rendering**

Run: rich-results test on each URL. Expected: 10/10 pass FAQPage validation.

**Step 3: Baseline GSC tracking**

Add all 10 URLs to a GSC saved filter "FAQ Phase 1". Note baseline impressions/clicks for Day 30 → Day 90 comparison.

**Step 4: Sign-off**

Update `project_keyword_strategy_2026-05-16.md` — mark Phase 1 complete with publish-log link. Per [feedback-phase-order](../../C:/Users/jim/.claude/projects/c--Users-jim-OneDrive-Documents-ArnoldItkin/memory/feedback_phase_order.md), do NOT start Phase 2 until this checkbox is closed.

---

## Phase 2 — Highway × Truck-Type Long-Tail (Days 31-55)

**Why second:** Matches Jim's federal MDL motor-vehicle lane. Difficulty 15-30. No DFW PI firm currently owns this long-tail. 8-12 pages should rank inside 60 days.

**Volume target:** 8 pages published.

### Task 2.0: TxDOT corridor data (gating prereq)

Must complete before Tasks 2.1+ — pages cite this data. See Phase 0 Task 0.2.

### Task 2.1: Lock the 8 target keywords

Pull from source Section 4 (truck) + Section 6 (highway):
1. fmcsa violation accident lawyer texas — 25/mo, Very Low
2. jackknife truck accident lawyer texas — 40/mo, Low
3. truck driver fatigue accident lawyer — 45/mo, Low
4. overloaded truck accident lawyer dallas — 30/mo, Low
5. i-35 truck accident lawyer dallas — 35/mo, Low
6. i-20 truck accident lawyer dallas — 30/mo, Low
7. i-30 truck accident lawyer fort worth — 25/mo, Low
8. 635 lbj freeway accident lawyer — 45/mo, Low

### Task 2.2 through 2.9: Write each page

Pattern: 1,200-1,800 words, H1 exact-match, includes one DFW-specific case study or accident-data sidebar (pull from TxDOT crash data — flag if Jim wants this scoped separately), Schema = LegalService + FAQPage, internal links to: main truck-accident practice page, the closest geographic FAQ page from Phase 1, one other Phase 2 page.

### Task 2.10: Phase 2 close-out

Same verification ritual as Task 1.11. Mark Phase 2 complete in `project_keyword_strategy_2026-05-16.md` before starting Phase 3.

---

## Phase 3 — Mass-Tort × DFW-City Pages (Days 56-75)

**Why third:** Goff's structural moat. Source dataset has only 80/mo "dallas mass tort lawyer" + 60/mo Fort Worth equivalent — meaning NO competitor is targeting [drug/device] × [DFW city] combinations. This is whitespace.

**Volume target:** 6-10 pages, depending on which current MDLs Jim wants to lead with.

### Task 3.1: Confirm MDL pairings with Jim

**Decision required (BEFORE writing):** Which 3-5 active MDLs should Jim front?

Existing recon points to: AFFF firefighting foam, hernia mesh, hair relaxer, Paragard, Amazon delivery vehicle. See `recon/AFFF-PAGES/`, `recon/PARAGARD-PAGES/`, `recon/HAIR-RELAXER-PAGES/`, `hernia-mesh-litigation-research.md`, `amazon-delivery-vehicle-litigation-research.md`.

DFW-city slots: Dallas, Fort Worth, Plano, Frisco, Arlington, McKinney, Denton, Irving.

Matrix = 5 MDLs × 8 cities = up to 40 pages (programmatic). Phase 3 ships ONLY 6-10 — the highest-priority pairings — and the rest become a Phase 6 programmatic build.

### Task 3.2 through 3.9: Write each page

Pattern: 1,500-2,200 words. Use programmatic-SEO template structure (page header pulls city, MDL summary block is shared partial). Schema = LegalService + LocalBusiness. Each page links to the parent MDL hub + the city-level practice page if one exists.

### Task 3.10: Phase 3 close-out

Same verification ritual. Mark complete.

---

## Phase 4 — Suburb Displacement Pages (Days 76-85)

**Why fourth:** Per [snellings recon memory](../../C:/Users/jim/.claude/projects/c--Users-jim-OneDrive-Documents-ArnoldItkin/memory/reference_snellings_recon.md), Snellings is the most beatable suburb incumbent (Frisco, 4 attorneys, $3.66M largest verdict). Per [mullen recon](../../C:/Users/jim/.claude/projects/c--Users-jim-OneDrive-Documents-ArnoldItkin/memory/reference_mullen_recon.md), Mullen owns Plano/Frisco with a 29% contingency moat — direct attack on Plano/Frisco will be slower; treat as hold-the-line.

**Volume target:** 4 suburb pages (Frisco, McKinney, Denton, Plano).

### Task 4.1 through 4.4: Write each suburb page

Pattern per page:
- H1: "Personal Injury Lawyer in [City], TX"
- Local proof: 1-2 case results from [City] or adjacent area
- 1,500 words minimum
- LocalBusiness schema with NAP for nearest physical Goff presence
- 5+ local landmarks/highway references for entity disambiguation
- Internal links to city-relevant FAQ + city-relevant Phase 2 highway page

Frisco page MUST out-rank Snellings's Frisco page on local-pack signals within 60 days — measurable target.

### Task 4.5: Phase 4 close-out

Mark complete.

---

## Phase 5 — Emerging Tort Flag-Planting (Days 86-90)

**Why fifth:** These are <100/mo each but YoY growth is 30-50%+. Goal is land-grab — own the URL before competition wakes up. 60-90 day ranking timeline is fine because volume is still climbing.

**Volume target:** 4 pages.

### Task 5.1 through 5.4: Write each emerging-tort page

1. e-scooter accident lawyer dallas
2. doordash accident lawyer dallas
3. amazon driver accident lawyer dallas
4. tesla autopilot accident lawyer texas

Same write-publish-schema-link pattern.

### Task 5.5: Phase 5 close-out + 90-day retrospective

**Step 1:** Pull GSC data for all 30+ published pages — impressions, clicks, average position.

**Step 2:** Write `recon/goff-law/KEYWORD-PHASE-RETROSPECTIVE-2026-08-14.md` covering:
- Which pages ranked fastest
- Which keywords over/under-performed volume estimates (per [reference-keyword-research](../../C:/Users/jim/.claude/projects/c--Users-jim-OneDrive-Documents-ArnoldItkin/memory/reference_keyword_research_dfw_pi.md), volumes are estimates only)
- Lead-flow data from those pages (cross-ref Bill AI Machine intake logs)
- Recommend Phase 6 (programmatic mass-tort × city matrix expansion) scope

**Step 3:** Decision point — programmatic build or another curated phase?

---

## Phase Gates

- Phase 1 done = 10 FAQ URLs published, indexed, schema-valid, GSC baseline saved
- Phase 2 done = 8 highway/truck URLs published, indexed, schema-valid
- Phase 3 done = 6-10 MDL×city URLs published, indexed, schema-valid
- Phase 4 done = 4 suburb URLs published, indexed, schema-valid
- Phase 5 done = 4 emerging-tort URLs published + retrospective doc written

Do NOT start the next phase before the prior phase's gate is closed.

## Status log

- **2026-05-16 — Phase 0 closed.** Spanish keyword pull (184 KW) + TxDOT corridor data both shipped to `recon/goff-law/`. Phase 1b + Phase 2 unblocked from data side.
- **2026-05-16 — Phase 1 drafts complete.** All 10 WordPress-ready FAQ pages written to `recon/goff-law/faq-drafts/` (~14,240 words). Mirrored to Bill AI Machine `static/faq-drafts/` and surfaced via new `/faq-drafts` route (action card on dashboard). Chelsea + Jim review BEFORE WordPress publish. Phase 1 gate (URLs published / indexed / schema-valid / GSC baseline) NOT yet met — that requires WordPress publish step from Goff team. Per Jim's 2026-05-16 directive, proceeding with Phase 1b in parallel rather than blocking on publish.
- **2026-05-16 — Phase 1b shipped.** 8 Spanish FAQ drafts at `recon/goff-law/faq-drafts-spanish/` (~11,365 words native Mexican Spanish). Mirrored to Bill AI Machine. EN/ES toggle live on `/faq-drafts`. Native Spanish reviewer needed before publish.
- **2026-05-16 — Phase 2 drafts shipped.** 8 highway/truck pages at `recon/goff-law/phase2-drafts/` (~11,500 words, all TxDOT-cited with .txdot.gov source links). Mirrored to Bill AI Machine. Viewer extended with PHASE 1 / PHASE 2 toggle. Per Jim's directive, dispatched without waiting for Phase 1 strict-gate close (WordPress publish). 4 practice-type pages (FMCSA, jackknife, fatigue, overloaded) + 4 corridor pages (I-35E, I-20, I-30, I-635 LBJ). All federal CFR + Texas Transp Code citations included. Tarrant County 58% CMV-fatal increase used as lead stat on FW page.
- **2026-05-16 — Phase 3 drafts shipped (5 MDLs × 2 cities = 10 pages).** Goff's structural moat — NO competitor targets [federal MDL] × [DFW city]. 10 pages at `recon/goff-law/phase3-drafts/` (~17,580 words). Mirrored to Bill AI Machine; viewer now has PHASE 1 / 2 / 3 toggle. MDLs covered: AFFF firefighting foam (MDL 2873 D.S.C., NAS JRB exposure anchor for FW), hernia mesh (MDLs 2846/2327/2753/2782 — Bard/Ethicon/Atrium/Covidien), hair relaxer cancer (MDL 3060 N.D. Ill., NIH Sister Study science anchor, FW Black community context), Paragard IUD (MDL 2974 N.D. Ga., CooperSurgical defendant), Amazon Delivery Vehicle (DSP-liability angle, NOT a drug MDL — TxDOT data cited on M9/M10 with Tarrant 58% CMV-fatal stat on M10). Each Dallas/FW pair has meaningfully different DFW-specific moat sections (named hospitals, named bases, named neighborhoods). Phase 3 remaining MDL × city pairings (5 MDLs × 6 other cities = 30 pages) deferred to Phase 6 programmatic build.
- **2026-05-16 — Phase 4 drafts shipped (4 suburb pages).** 4 pages at `recon/goff-law/phase4-drafts/` (~6,770 words). Frisco / McKinney / Denton / Plano — hyperlocal-dominance play. Frisco targets Snellings (most beatable). Plano = hold-the-line vs Mullen (29% contingency moat). Every page: 2 phase-1 FAQ cross-links + 1 phase-2 corridor link + 1 phase-3 mass-tort link. Geo-anchors verified (Toyota HQ Plano, Stonebridge Ranch McKinney, UNT Denton, Stonebriar Frisco, etc.). Explicit excluded-case-type disclaimer on every page to filter bad-fit traffic.
- **2026-05-16 — Phase 5 drafts shipped (4 emerging tort pages).** 4 pages at `recon/goff-law/phase5-drafts/` (~6,470 words). E-scooter Dallas, DoorDash Dallas, Gig Driver Dallas (Amazon Flex/DoorDash/UberEats/Instacart drivers as plaintiffs), Tesla Autopilot Texas (statewide). Insurance-coverage-gap section is the trust anchor on every page (gig platforms' tier structure, personal-auto commercial-use exclusion, Tesla L2 driver-assist liability split). Land-grab strategy: low volume now, +30-50% YoY growth.
- **2026-05-16 — Phase 5 retrospective written.** Full retrospective at `recon/goff-law/KEYWORD-PHASE-RETROSPECTIVE-2026-05-16.md`. All 5 phases drafted in single session per Jim's "ship it" directive. Strict gates not yet met (WordPress publish + GSC baseline = Goff team next steps). 44 total pages, ~67,925 words. Plan converted from sequential gates to drafts-shipped state; phase completion now defined by Jim/Chelsea publish action.

## Decisions (resolved 2026-05-16)

1. **Phase 1 Task 1.7** — RESOLVED: reframe to "third-party negligence at work in texas" (keeps the 170/mo volume, stays in lane). Title becomes "What To Do If You're Injured at Work in Texas (When It's NOT Workers' Comp)."
2. **Phase 3 Task 3.1** — RESOLVED: all 5 MDLs lead — AFFF, hernia mesh, hair relaxer, Paragard, Amazon DVR. With 5 MDLs × 8 DFW cities = 40-page programmatic potential; Phase 3 ships the 8 highest-priority pairings; rest deferred to a Phase 6 programmatic build.
3. **Phase 2 / TxDOT crash data** — RESOLVED: separate scoped task (Task 2.0 below) BEFORE writing pages, so highway pages can cite real crash counts per corridor.
4. **Spanish × mass-tort (Stack 4)** — RESOLVED: add parallel Phase 1b. Requires Spanish keyword pull first (new prereq Task 0.1).

## Out of Scope

- Google PPC, Meta Ads, LinkedIn Ads (per [feedback-marketing-strategy-constraint](../../C:/Users/jim/.claude/projects/c--Users-jim-OneDrive-Documents-ArnoldItkin/memory/feedback_marketing_strategy_constraint.md))
- Any med mal, nursing home, dog bite, workers comp, birth injury, generic slip-fall keyword (per [project-goff-case-exclusion-list](../../C:/Users/jim/.claude/projects/c--Users-jim-OneDrive-Documents-ArnoldItkin/memory/project_goff_case_exclusion_list.md))
- National blog content (per [local-seo playbook](../../C:/Users/jim/.claude/projects/c--Users-jim-OneDrive-Documents-ArnoldItkin/memory/reference_local_seo_pi_playbook.md))
- Texas Disciplinary Rules compliance review (per [alventra prompts memory](../../C:/Users/jim/.claude/projects/c--Users-jim-OneDrive-Documents-ArnoldItkin/memory/reference_alventra_seo_prompts.md) — Jim handles)
