# Phase 2 — Writer's Brief: 8 Truck Accident Landing Pages

**Client:** Goff Law DFW (gofflawdfw.com)
**Attorney:** Jim Goff
**Project:** Phase 2 keyword execution — 4 truck practice-type pages + 4 DFW corridor pages
**Date issued:** 2026-05-16
**Target ICP:** People hit by 18-wheelers / commercial trucks in DFW. Often catastrophic injury. Mix of working-class and middle-class. May be the family of a deceased driver/passenger. Serious-case register throughout.

---

## Read these BEFORE you start

| Document | Why |
|---|---|
| **`recon/goff-law/VOICE-GUIDE-v1-2026-05-16.md`** | The 10 voice rules + banned/preferred word list + persona. **Non-negotiable for tone.** Read this first. Truck pages get the "serious case register" — see Tone Calibrations row 4 (Phase 2 truck pages). |
| **`recon/goff-law/TXDOT-CORRIDOR-DATA-2026-05-16.md`** | Every numeric claim on every truck page MUST source from this file. The methodology note at the top is critical. |
| **`recon/goff-law/PHASE-4v2-WRITERS-BRIEF-2026-05-16.md`** | Reference for format / depth / structure rigor. Phase 2 follows the same shape. |
| **`recon/goff-law/phase2-drafts/t01` through `t08`** | AI-drafted seeds. Useful for H1, H2 outline, citations. Your job is to upgrade the voice and lock in the data integrity. Don't ship the seed copy. Use it as scaffolding. |

---

## What we need from you

For each of the 8 pages: a markdown file with body copy (H1 + byline + lead + H2 sections + DFW Truck Crash Data block + CTA + Related Resources). Save to `recon/goff-law/phase2-drafts/<slug>.md` (overwriting the existing seed drafts). YAML frontmatter is already in each seed file — keep it, update `updated_date` to your save date.

## What we'll handle (you don't need to write these)

- FAQPage JSON-LD schema (we regenerate from your final H2 questions)
- LegalService JSON-LD (universal template — already in each seed file, leave it)
- WordPress publishing + URL setup
- Internal `{{CTA_PHONE}}` token replacement at publish time

---

## Brand architecture (LOCKED — every page)

| Slot | Hook |
|---|---|
| **Primary** | **Get Goff. Get Paid.** |
| **Secondary** | **You're not a case. You're family.** |
| **Cost reassurance** | **No win. No fee.** |
| **Spanish equivalents** | **Llame a Goff. Cobre lo suyo.** / **No eres un caso. Eres familia.** / **Sin ganar, sin pagar.** |

These appear in every CTA module and at the top of every page.

---

## Tone calibration — Phase 2 specifically

Truck cases are not fender benders. The reader is often the spouse, parent, or adult child of someone killed or permanently injured. Voice Guide rules still apply (talk like a person, name Jim, insurance is the opponent, no result promises) — but the register dials up to **serious case**. That means:

- No "wrecks" levity in lead paragraphs of corridor pages. Use "crashes" or "wrecks" but never anything that minimizes severity.
- Wrongful-death framing should be available as a soft secondary read — never the primary hook, but acknowledged in the body. The Voice Guide's "wrongful death intake" row applies: **no slogans on a death-anchored page section. Quiet, reverent.**
- "You" still wins — but if you're addressing a family member of someone killed, "you and your family" works.
- The technical regulatory language (49 CFR, FMCSA, HOS) is the trust signal. Plain-English it but don't dumb it down to the point you lose credibility. The persona is the Pleasant Grove mom from the Voice Guide — but on a truck page she's calling about her brother who got hit on I-30 and is in ICU. She needs to feel that Jim knows the federal rules.

---

## The 8 pages — at-a-glance

| # | Slug | Target keyword | Vol/mo | Comp | Type |
|---|---|---|---|---|---|
| T01 | `/practice-areas/truck-accidents/fmcsa-violations-texas/` | fmcsa violation accident lawyer texas | 25 | Low | Practice |
| T02 | `/practice-areas/truck-accidents/jackknife-crashes-texas/` | jackknife truck accident lawyer texas | 40 | Low-Med | Practice |
| T03 | `/practice-areas/truck-accidents/driver-fatigue-texas/` | truck driver fatigue accident lawyer texas | 45 | Low-Med | Practice |
| T04 | `/practice-areas/truck-accidents/overloaded-trucks-dallas/` | overloaded truck accident lawyer dallas | 30 | Low | Practice |
| T05 | `/practice-areas/truck-accidents/i-35-truck-accidents-dallas/` | i-35 truck accident lawyer dallas | 35 | Low-Med | Corridor |
| T06 | `/practice-areas/truck-accidents/i-20-truck-accidents-dallas/` | i-20 truck accident lawyer dallas | 30 | Low-Med | Corridor |
| T07 | `/practice-areas/truck-accidents/i-30-truck-accidents-fort-worth/` | i-30 truck accident lawyer fort worth | 25 | Low | Corridor |
| T08 | `/practice-areas/truck-accidents/i-635-lbj-truck-accidents-dallas/` | 635 lbj freeway accident lawyer | 45 | Med | Corridor |

**Recommended writing order (data-integrity first, easiest validation first):**
1. T03 driver fatigue — strongest existing seed, validates citation pattern
2. T01 FMCSA — anchor practice page everything else cross-links to
3. T02 jackknife
4. T04 overloaded
5. T05 I-35 Dallas (Stemmons + Mixmaster geo work)
6. T07 I-30 Fort Worth (lead-stat is the Tarrant 58% trend)
7. T06 I-20 Dallas
8. T08 I-635 / LBJ (managed-lane nuance — write last when you're warmed up on corridor patterns)

---

## Universal page structure (every page)

| Section | Word count | Notes |
|---|---|---|
| H1 | — | Preserve from existing seed (see per-page section below) |
| Byline | 1 line | "By Jim Goff \| Updated 2026-05-16" (or your save date) |
| Lead paragraph | 100-150 words | **Must open with the assigned TxDOT lead stat** (see Lead-Stat Assignments). Target keyword in first 100 words. Address reader directly. Mention "Get Goff. Get Paid." or "Goff Law DFW" naturally once in the lead. |
| H2: Why [this thing] is dangerous / matters | 200-300 | Practice pages: explain the regulatory or mechanical thing. Corridor pages: geographic + design + traffic-mix risk factors. |
| H2: Federal rules / CFR section that controls | 250-400 | The technical anchor. Cite the specific 49 CFR sections from the cheat sheet below. |
| H2: Causes / failure modes / fact patterns | 200-300 | Bulleted list. Each bullet anchored to a CFR section or Texas statute where possible. |
| H2: Who's liable (multiple parties) | 250-350 | Driver / carrier / shipper / loader / broker / maintenance contractor / component manufacturer. The "rarely just the driver" frame. |
| H2: Evidence preservation in first 30 days | 200-300 | The "6-month ELD window" hook. The list of what disappears and how fast. Spoliation letter framing. |
| H2: What the case is worth / damages framework | 150-250 | "Texas does not cap motor-vehicle injury damages" + reference to TCPRC § 71.004 for wrongful death. **No specific dollar promises.** |
| DFW Truck Crash Data block | — | Standardized format with source-linked footnotes. See "DFW Truck Crash Data block template" below. |
| CTA module | — | See "Universal CTA template" below. Brand architecture stacked. |
| Related Resources | 3 links | See cross-link map below. |

**Word count target per page: 1,400-1,800.** (Seeds run 1,200-1,500 — bring them up by deepening federal-regulation explanations and adding geo specifics on corridor pages.)

---

## TxDOT data integrity rules (NON-NEGOTIABLE)

Read this section twice before you draft anything.

### Rule 1 — Every number gets a source link

Every numeric claim on every page must be followed by a footnote that links to a `.txdot.gov` URL. Use the citation format already established in the seed drafts:

```
... 27 fatal CMV crashes in Dallas County in 2024.<sup>[1](#src1)</sup>
```

with the footnote at the bottom of the data block:

```
<a id="src1"></a><sup>1</sup> TxDOT 2024 Commercial Motor Vehicle Involved Crashes and Injuries by County (Table 30). [https://www.txdot.gov/content/dam/docs/division/trf/crash-records/2024/30.pdf](https://www.txdot.gov/content/dam/docs/division/trf/crash-records/2024/30.pdf). Pulled 2026-05-16.
```

### Rule 2 — Pull every number from `TXDOT-CORRIDOR-DATA-2026-05-16.md`. NEVER invent.

The reference document at `recon/goff-law/TXDOT-CORRIDOR-DATA-2026-05-16.md` contains every number you are authorized to use. If a number isn't in that file, don't put it on the page. If you think a useful number is missing, flag it back to Jim — don't guess.

### Rule 3 — Honest framing: county-aggregate, not corridor-specific

TxDOT's free PDFs aggregate fatal crashes by **county + road type** — not by named corridor. There is NO publicly available free TxDOT number for "fatal crashes on I-35E in 2024." That data exists inside the CRIS Query Tool but requires an interactive session.

**Required framing for every corridor page (T05-T08):**

- DO write: "Across all Dallas County interstates — including I-35E — TxDOT recorded 81 fatal crashes and 90 deaths in 2024."
- DO write: "TxDOT does not publish I-35E-specific fatal counts in its free annual reports."
- DO NOT write: "There were 81 fatal crashes on I-35E in 2024."
- DO NOT write: "I-35E saw X% of Dallas County truck fatalities."

Every corridor page must include a "honest framing first" sentence in the Crash Data H2 (the seed drafts already model this — preserve that pattern).

### Rule 4 — No invented sub-types, mile markers, or hotspots

TxDOT does not publish, for free, "rear-end vs jackknife counts on I-635" or "fatal crashes between mile marker 12 and 18." If a seed draft has a number like that, it shouldn't be there — verify against the TxDOT data file before keeping it. The data file's "Data unavailable as of 2026-05-16" cells are NOT placeholders. They mean don't claim a number.

### Rule 5 — CMV ≠ semi-truck only

TxDOT's "Commercial Motor Vehicle" category includes any vehicle with GVWR > 10,000 lbs. That's a broader bucket than 18-wheelers. When a page implies "18-wheeler" but the cited number is the CMV count, add a one-line caveat (the seed drafts already model this language — keep it). Don't drop the caveat.

### Rule 6 — Cite the table number

Every footnote should name the specific TxDOT table: Table 12 (Fatal Crashes by Road Type), Table 13 (Crashes by County), Table 30 (CMV Involved Crashes). The "How to Cite" block in the TxDOT data file shows the format.

### Rule 7 — Liability hedge

Drop the liability-hedge line at the bottom of every DFW Truck Crash Data block:

> *Crash statistics may include incidents not directly related to the legal services described and are presented for informational purposes only.*

---

## Federal regulation cheat sheet

These are the citations Dianne should have at her elbow while drafting. Each page below specifies which subset applies to that page. Cite them with section numbers in body copy and link the first instance per page to ecfr.gov.

| Citation | What it covers | Pages that should cite it |
|---|---|---|
| **49 CFR § 395.3** | Hours of Service — 11-hr driving limit, 14-hr duty limit, 30-min break, 60/70-hr weekly limit | T01, T03, T05, T06, T07, T08 |
| **49 CFR § 395.20** | Electronic Logging Device (ELD) requirement | T01, T03 |
| **49 CFR § 395.22(i)** | 6-month ELD record retention rule | T01, T03, T05, T06, T07, T08 |
| **49 CFR § 392.5** | Drug & alcohol use — 0.04% BAC limit for CDL drivers | T01, T03 |
| **49 CFR § 392.2** | Driver compliance with state traffic laws (including weight) | T01, T04 |
| **49 CFR § 393.55** | Anti-Lock Braking System (ABS) requirements | T02 |
| **49 CFR § 393.100** | Cargo securement (driver AND shipper share responsibility) | T02, T04 |
| **49 CFR Part 391** | Driver qualifications (CDL, MVR, PSP screening, drug screen) | T01 |
| **49 CFR Part 396** | Vehicle inspection, repair, maintenance (DVIRs, 12-mo maintenance file) | T01, T02 |
| **49 CFR Part 380** | Entry-level driver training | T01 |
| **49 CFR § 382.303** | Post-crash drug/alcohol testing (8 hrs alcohol, 32 hrs drugs) | T01, T02, T03, T05, T06, T07, T08 |
| **49 CFR § 395.11** | HOS recordkeeping / log completion | T03 |
| **23 U.S.C. § 127** | Federal 80,000-lb gross vehicle weight cap | T04 |
| **49 U.S.C. § 14704** | Federal cause of action against motor carriers (shipper liability hook) | T04 |
| **Texas Transportation Code § 644** | Texas adopts federal motor-carrier safety rules (including for intrastate carriers) | T01, T02, T03, T05, T06, T07, T08 |
| **Texas Transportation Code § 545.351** | "Reasonable and prudent" speed for conditions | T02, T06 |
| **Texas Transportation Code § 623** | Texas oversize/overweight permit requirement | T04 |
| **Texas Transportation Code § 545.412** | Driving while incapable of safe operation (fatigue applies) | T03 |
| **Texas Civil Practice & Remedies Code § 33.001** | Texas modified comparative fault | T02 (and others as relevant) |
| **Texas Civil Practice & Remedies Code § 71.004** | Wrongful death recovery for surviving family | All 8 pages (damages section) |

---

## Lead-stat assignments

Each page opens with one assigned TxDOT statistic. This is the first numeric claim in the lead paragraph. Do not bury it. Do not paraphrase it past recognition. All numbers below are pulled directly from `TXDOT-CORRIDOR-DATA-2026-05-16.md`.

| Page | Lead stat (opens the page) | Source table |
|---|---|---|
| **T01 FMCSA** | "Texas roads saw 546 fatal commercial-truck crashes in 2024, and Dallas and Tarrant counties alone produced 46 of them — about 8.4% of every fatal CMV crash in the state." | Table 30 (2024) |
| **T02 Jackknife** | "Texas recorded 546 fatal commercial-truck crashes in 2024, killing 608 people statewide — and Dallas plus Tarrant counties alone produced 46 of them." | Table 30 (2024) |
| **T03 Driver fatigue** | "Texas saw 546 fatal commercial-truck crashes in 2024, with 608 people killed statewide. Dallas and Tarrant counties combined for 46 of those fatal CMV wrecks — 8.4% of the state total in two counties alone." | Table 30 (2024) |
| **T04 Overloaded** | "Dallas County recorded 27 fatal commercial-truck crashes in 2024 and 3,857 total CMV-involved crashes — the highest CMV crash count of any Texas county." | Table 30 (2024) |
| **T05 I-35 Dallas** | "Across all Dallas County interstates, TxDOT recorded 81 fatal crashes and 90 deaths in 2024." | Table 12 (2024) |
| **T06 I-20 Dallas** | "Across both Dallas County and Tarrant County interstates combined, TxDOT recorded 131 fatal crashes and 149 deaths in 2024 — roughly one Interstate fatal crash every 67 hours across the two counties." | Table 12 (2024), summed |
| **T07 I-30 Fort Worth** | **"Fatal commercial truck crashes in Tarrant County jumped 58% from 2022 to 2024 according to TxDOT — from 12 fatal CMV crashes in 2022 to 19 in 2024, the highest count in the three-year data window."** *(This is the strongest single corridor-pointed stat in the dataset — Tarrant trend is moving the wrong direction. Lead with it, expand on it.)* | Table 30 (2022 + 2024) |
| **T08 I-635 LBJ** | "Across all Dallas County interstates — and I-635 is one of them — TxDOT recorded 81 fatal crashes and 90 deaths in 2024, with 27 fatal commercial motor vehicle crashes across all Dallas County roads that year." | Tables 12 + 30 (2024) |

**Most-cited stats across all 8 pages** (will appear multiple times across the suite):
1. **Dallas + Tarrant = 8.4% of Texas CMV fatal crashes (46 of 546)** — cited on T01, T02, T03, T04, T05, T06, T07, T08 (all 8)
2. **27 fatal CMV crashes in Dallas County in 2024 / 3,857 total CMV crashes** — cited on T01, T02, T03, T04, T05, T06, T08 (7 pages)
3. **Tarrant CMV fatal crashes up 58% from 12 (2022) to 19 (2024)** — cited on T01, T02, T03, T07 (lead stat) (4 pages)

---

## Universal CTA module template — Phase 2 specific

Drop in at the close of every page, before Related Resources. Use the Phase 2 version (acknowledges truck/18-wheeler context):

```markdown
---

## Get Help Today

Hurt in a wreck with a truck or 18-wheeler in DFW? **Get Goff. Get Paid.**

You're not a case — you're family.

**No win. No fee.** Available 24/7. Hablamos español.

**Call Jim now: {{CTA_PHONE}}**

[Button: Free Case Review →]

---
```

For pages that lead heavily with wrongful-death framing (any page where the H2 on damages includes substantial death-claim language), pull the brand slogans OUT of that specific section and use a quiet line:

> If a truck crash killed someone in your family, Jim takes these calls personally. Call when you're ready: {{CTA_PHONE}}

Then return to the standard CTA module at the bottom of the page.

---

## DFW Truck Crash Data block — standardized format

Every page closes the body content (before the CTA) with this block. Cite only the stats relevant to that page (mix from Lead-Stat Assignments + supporting numbers). Use the seed drafts as the template — they're already in the right format.

```markdown
---

## DFW Truck Crash Data

Recent TxDOT figures show the scope of the DFW commercial-truck risk:

- **[lead stat or supporting stat here].**<sup>[1](#src1)</sup>
- **[second stat].**<sup>[2](#src2)</sup>
- **[third stat — statewide framing].**<sup>[3](#src3)</sup>

<a id="src1"></a><sup>1</sup> [Full TxDOT citation per "How to Cite" block in TXDOT-CORRIDOR-DATA file]. [URL]. Pulled 2026-05-16.

<a id="src2"></a><sup>2</sup> [...]

<a id="src3"></a><sup>3</sup> [...]

*Crash statistics may include incidents not directly related to the legal services described and are presented for informational purposes only.*

---
```

---

## Universal Related Resources block (every page)

Every page links to exactly 3 internal resources:

1. **Phase 1 FAQ Page 1** — `/faq/what-to-do-after-car-accident-in-texas/` (universally relevant; the most-needed FAQ for any wreck victim)
2. **Truck accident practice hub** — `/practice-areas/truck-accidents/`
3. **One Phase 2 sibling page** — assigned per page below

Format:

```markdown
## Related Resources

- [What To Do After a Car Accident in Texas: Step-by-Step Guide](/faq/what-to-do-after-car-accident-in-texas/)
- [Truck Accident Practice Area](/practice-areas/truck-accidents/)
- [Assigned sibling — see per-page brief](/practice-areas/truck-accidents/[slug]/)
```

---

## Cross-link map (sibling assignments)

The third Related Resources link, assigned per page below, follows logical pairing:

| Page | Sibling link (and why) |
|---|---|
| T01 FMCSA | T03 Driver Fatigue — HOS violations are the most common FMCSA violation, natural deep-dive next step |
| T02 Jackknife | T01 FMCSA — jackknife cases usually involve FMCSA brake/maintenance violations; FMCSA is the regulatory framework |
| T03 Driver Fatigue | T01 FMCSA — fatigue is governed by HOS rules, the core FMCSA regulation |
| T04 Overloaded | T02 Jackknife — overloaded trucks jackknife; mechanical pairing |
| T05 I-35 Dallas | T08 I-635 LBJ — both Dallas County corridors, meet at the LBJ/I-35E interchange |
| T06 I-20 Dallas | T05 I-35 Dallas — both Dallas County corridors, intersect in south Dallas |
| T07 I-30 Fort Worth | T06 I-20 Dallas — both east-west connectors, run parallel across the metro |
| T08 I-635 LBJ | T05 I-35 Dallas — both Dallas corridors, meet at LBJ/I-35E |

---

# Per-page brief — 8 pages

## T01 — FMCSA Violation Truck Accident Lawyer in Texas

- **Target keyword:** fmcsa violation accident lawyer texas
- **Est. monthly volume:** 25
- **Competition:** Low
- **H1 (preserve):** FMCSA Violation Truck Accident Lawyer in Texas
- **URL slug:** `/practice-areas/truck-accidents/fmcsa-violations-texas/`
- **Word count:** 1,500-1,800 (the FMCSA topic supports depth — push toward 1,800)
- **Audience profile:** Family of someone seriously hurt or killed by a commercial truck. May not know what "FMCSA" means at intake. The page educates AND positions Jim as the lawyer who actually uses the federal framework. Working/middle class; technical literacy varies.
- **Lead stat (mandatory):** "Texas roads saw 546 fatal commercial-truck crashes in 2024, and Dallas and Tarrant counties alone produced 46 of them — about 8.4% of every fatal CMV crash in the state." (TxDOT Table 30, 2024)
- **Required federal citations (mandatory):**
  - 49 CFR § 395.3 (HOS)
  - 49 CFR § 395.20 (ELD)
  - 49 CFR Part 391 (driver qualifications)
  - 49 CFR Part 380 (entry-level training)
  - 49 CFR Part 396 (maintenance / DVIRs)
  - 49 CFR § 382.303 (post-crash drug/alcohol testing)
  - Texas Transportation Code § 644 (Texas adoption of federal rules)
- **DFW geo-anchors:** Mention DFW broadly; this is a Texas-statewide practice page, not corridor-specific. Light corridor references OK (I-35E, I-635) but don't anchor the page geographically.
- **Suggested H2 outline (from seed, polish in voice):**
  1. What FMCSA regulations are and why they matter to your claim
  2. Hours of Service (HOS) violations: 49 CFR § 395
  3. ELD tampering and falsified logs
  4. Inadequate driver training, qualification, and supervision (Part 391, Part 380)
  5. Fleet maintenance failures: 49 CFR § 396
  6. FMCSA SMS scores and the BASIC categories
  7. Why the federal framework matters for your case value
- **Cross-links:**
  1. `/faq/what-to-do-after-car-accident-in-texas/`
  2. `/practice-areas/truck-accidents/`
  3. T03: `/practice-areas/truck-accidents/driver-fatigue-texas/`
- **Tone notes:** This is the most technical of the 8. Lean into the regulatory vocabulary but always plain-English the first time a term appears. Frame "negligence per se" once and then use it. Frame the carrier as the corporate opponent — not just the driver. SMS scores and BASIC categories should be presented as "the paper trail that proves the carrier knew." This is the anchor practice page everything else links back to — get the voice right here first.

---

## T02 — Jackknife Truck Accident Lawyer in Texas

- **Target keyword:** jackknife truck accident lawyer texas
- **Est. monthly volume:** 40
- **Competition:** Low-Medium
- **H1 (preserve):** Jackknife Truck Accident Lawyer in Texas
- **URL slug:** `/practice-areas/truck-accidents/jackknife-crashes-texas/`
- **Word count:** 1,400-1,700
- **Audience profile:** Family of someone hit broadside by a sweeping trailer. Often catastrophic injury — broadside hits from 53-ft trailers at highway speed don't produce minor injuries. Strong wrongful-death tilt. Working-class to middle-class.
- **Lead stat (mandatory):** "Texas recorded 546 fatal commercial-truck crashes in 2024, killing 608 people statewide — and Dallas plus Tarrant counties alone produced 46 of them." (TxDOT Table 30, 2024)
- **Required federal citations (mandatory):**
  - 49 CFR § 393.55 (ABS on trailers)
  - 49 CFR § 393.100 (cargo securement — driver AND shipper)
  - 49 CFR § 382.303 (post-crash testing)
  - 23 U.S.C. § 127 (80,000-lb federal weight cap)
  - Texas Transportation Code § 545.351 (reasonable speed for conditions)
  - Texas Civil Practice & Remedies Code § 33.001 (modified comparative fault)
  - Texas Civil Practice & Remedies Code § 71.004 (wrongful death)
- **DFW geo-anchors:** Light. The page is a Texas-statewide practice page. OK to reference DFW corridors (I-635, downtown Dallas) when illustrating fact patterns (e.g., "a wet I-635 surface" or "a downhill curve near downtown Dallas") — don't anchor geographically.
- **Suggested H2 outline (from seed):**
  1. What is a jackknife truck accident? (physics + the 15-degree threshold)
  2. What causes jackknifes — the four primary failures (brake lock-up / speed / road conditions / cargo imbalance)
  3. Why liability in a jackknife case is rarely just "the driver" (5 parties)
  4. Evidence you must lock down in the first 30 days
  5. What a Texas jackknife case is worth (damages framework, no caps, punitive availability)
- **Cross-links:**
  1. `/faq/what-to-do-after-car-accident-in-texas/`
  2. `/practice-areas/truck-accidents/`
  3. T01: `/practice-areas/truck-accidents/fmcsa-violations-texas/`
- **Tone notes:** The physics opening (tractor + trailer pivot at the fifth-wheel coupling) is concrete and good — keep it but Voice-Guide it. The "five potential parties" frame is the centerpiece — make it scan-able with bold leads on each party. Wrongful-death framing is naturally on-page; do the quiet/reverent treatment in the damages H2. Don't end with the standard slogan stack right after a wrongful-death paragraph — separate them with one paragraph of practical "what to do next" content first.

---

## T03 — Truck Driver Fatigue Accident Lawyer in Texas

- **Target keyword:** truck driver fatigue accident lawyer texas
- **Est. monthly volume:** 45
- **Competition:** Low-Medium
- **H1 (preserve):** Truck Driver Fatigue Accident Lawyer in Texas
- **URL slug:** `/practice-areas/truck-accidents/driver-fatigue-texas/`
- **Word count:** 1,500-1,800
- **Audience profile:** Family or victim of a "he fell asleep at the wheel" crash. Often rear-end / drift-into-lane fact patterns. Catastrophic injury common. Working/middle class.
- **Lead stat (mandatory):** "Texas saw 546 fatal commercial-truck crashes in 2024, with 608 people killed statewide. Dallas and Tarrant counties combined for 46 of those fatal CMV wrecks — 8.4% of the state total in two counties alone." (TxDOT Table 30, 2024) Add the 13%-of-large-truck-crashes federal research framing AFTER the lead stat — but cite it as "federal safety researchers" rather than inventing a specific FMCSA report. The seed says "roughly 13%" — that's defensible.
- **Required federal citations (mandatory):**
  - 49 CFR § 395.3 (HOS limits — 11/14/30-min/60-70/34-hr restart)
  - 49 CFR § 395.20 (ELD requirement)
  - 49 CFR § 395.22(i) (**6-month retention — the urgency hook**)
  - 49 CFR § 395.11 (log completion)
  - 49 CFR § 382.303 (post-crash testing)
  - 49 CFR § 392.5 (BAC limit — useful for the BAC-equivalent fatigue framing)
  - Texas Transportation Code § 644
  - Texas Transportation Code § 545.412 (driving while incapable of safe operation)
- **DFW geo-anchors:** Light — Texas-statewide practice page. Reference corridor in passing where useful (e.g., "a driver running I-35 from the border hits DFW deep into HOS exposure"). Don't anchor.
- **Suggested H2 outline (from seed):**
  1. What truck driver fatigue actually means in a Texas case (BAC-equivalency framing)
  2. Hours of Service rules under 49 CFR § 395.3 (the 11/14/30/60-70/34 numbers)
  3. Electronic Logging Devices and why the 6-month FMCSA window matters
  4. What evidence proves fatigue — beyond the ELD (cross-source list)
  5. When the carrier is liable, not just the driver (negligent dispatching / supervision / hiring / training)
  6. Texas fatigue-related driving rules (TX TC § 545.412)
- **Cross-links:**
  1. `/faq/what-to-do-after-car-accident-in-texas/`
  2. `/practice-areas/truck-accidents/`
  3. T01: `/practice-areas/truck-accidents/fmcsa-violations-texas/`
- **Tone notes:** The 6-month retention window is the page's hero hook — call it out in the lead paragraph after the stat. The "BAC-equivalent fatigue" framing (18 hrs awake = 0.05% BAC, 24 hrs = 0.10%) is a strong trust signal — keep it, source it correctly to "federal safety research" rather than naming a specific study unless we can cite one. Validate the BAC-equivalence claim before publish — the seed has it but Jim should sanity-check the source.

---

## T04 — Overloaded Truck Accident Lawyer in Dallas

- **Target keyword:** overloaded truck accident lawyer dallas
- **Est. monthly volume:** 30
- **Competition:** Low
- **H1 (preserve):** Overloaded Truck Accident Lawyer in Dallas
- **URL slug:** `/practice-areas/truck-accidents/overloaded-trucks-dallas/`
- **Word count:** 1,400-1,700
- **Audience profile:** Victim of a brake-fade or tire-blowout or rollover crash where the truck was visibly or provably overweight. This is also the page where the SHIPPER-liability story matters most — many readers won't know they can sue the shipper. Working/middle class; some commercial-driver/dispatcher readers too.
- **Lead stat (mandatory):** "Dallas County recorded 27 fatal commercial-truck crashes in 2024 and 3,857 total CMV-involved crashes — the highest CMV crash count of any Texas county." (TxDOT Table 30, 2024)
- **Required federal citations (mandatory):**
  - 23 U.S.C. § 127 (federal 80,000-lb GVW cap; 20K single axle / 34K tandem)
  - 49 CFR § 392.2 (driver compliance with state weight laws)
  - 49 CFR § 393.100 (cargo securement)
  - 49 U.S.C. § 14704 (federal cause of action — shipper-liability hook)
  - Texas Transportation Code § 623 (Texas oversize/overweight permit)
- **DFW geo-anchors (corridor-tilted practice page):** I-635 (LBJ Freeway) as freight loop; I-20 east-west as transcontinental freight; distribution-center clusters in Mesquite, Wilmer-Hutchins, Coppell, Inland Port near I-45. Keep the geo references concrete — these are the warehouses where the overload decisions actually get made.
- **Suggested H2 outline (from seed):**
  1. Federal and Texas weight limits for commercial trucks (80K GVW, axle caps, TX permit)
  2. How overloading causes catastrophic crashes (brake failure / tire blowout / rollover / extended stopping)
  3. Dallas freight corridors and overload risk (I-635 + I-20 geo)
  4. Who is liable when a truck is overloaded — it is rarely just the driver (shipper / loader / broker / carrier / driver)
  5. The cargo manifest and weight scale tickets — your case in three documents (BoL / scale ticket / dispatch route plan)
  6. Why an overload case is a high-value case (damages framework, punitive availability)
- **Cross-links:**
  1. `/faq/what-to-do-after-car-accident-in-texas/`
  2. `/practice-areas/truck-accidents/`
  3. T02: `/practice-areas/truck-accidents/jackknife-crashes-texas/`
- **Tone notes:** The "five parties" frame here MUST highlight the shipper and loader — they're the deepest pockets in overload cases and most readers don't know that. The "three documents" frame (BoL / scale ticket / dispatch plan) is the page's most useful concrete explainer — preserve it. Texas-permit framing matters too: a truck running overweight off the permitted route is operating illegally, period. Use that as a discrete liability hook.

---

## T05 — I-35 Truck Accident Lawyer in Dallas

- **Target keyword:** i-35 truck accident lawyer dallas
- **Est. monthly volume:** 35
- **Competition:** Low-Medium
- **H1 (preserve):** I-35 Truck Accident Lawyer in Dallas
- **URL slug:** `/practice-areas/truck-accidents/i-35-truck-accidents-dallas/`
- **Word count:** 1,400-1,700
- **Audience profile:** Victim or family of a crash on I-35E specifically — the Dallas-side I-35 leg. NAFTA freight corridor context matters. Working-class Hispanic readers along the I-35 path (south Oak Cliff to Lewisville) — bilingual emphasis applies.
- **Lead stat (mandatory):** "Across all Dallas County interstates, TxDOT recorded 81 fatal crashes and 90 deaths in 2024 — and I-35E, the north-south freight backbone running from the Mexican border through downtown Dallas to Oklahoma, is one of the busiest interstates in that count." (TxDOT Table 12, 2024) **Honest framing required immediately — call out that the 81 is the all-Dallas-County-interstates total, not I-35E alone.**
- **Required federal citations:**
  - 49 CFR § 395.3 (HOS)
  - 49 CFR § 395.22(i) (6-month ELD retention)
  - 49 CFR § 382.303 (post-crash testing)
  - Texas Transportation Code § 644
- **DFW geo-anchors (required — corridor page):**
  - **Stemmons Freeway** segment north of downtown (oldest section of urban Interstate in Texas)
  - **Downtown Dallas Mixmaster** (where I-35E, I-30, and US-75 collide in a stack of overpasses)
  - **LBJ/I-35E interchange** (where I-635 cuts across)
  - **NAFTA Superhighway context** — Laredo → Austin → Hillsboro split → Dallas → Oklahoma City
  - **Commuter mix** — Lewisville, Carrollton, Park Cities sharing lanes with through-freight
- **Suggested H2 outline (from seed):**
  1. Why I-35E is Especially Dangerous for Trucks (NAFTA + Stemmons + Mixmaster + LBJ geography)
  2. Common Causes of Truck Crashes on I-35E (fatigue / speeding / unsafe lane changes / brake failure / cargo shift)
  3. Crash Data: What TxDOT Tells Us About Dallas County (with honest framing)
  4. Who's Liable When a Truck Crash Happens on I-35E
  5. Evidence That Disappears Within Days of an I-35E Truck Crash
  6. What To Do If You're in a Truck Crash on I-35E (6-step checklist)
- **Cross-links:**
  1. `/faq/what-to-do-after-car-accident-in-texas/`
  2. `/practice-areas/truck-accidents/`
  3. T08: `/practice-areas/truck-accidents/i-635-lbj-truck-accidents-dallas/`
- **Tone notes:** Geographic specificity is the trust signal here. Stemmons, the Mixmaster, the LBJ interchange — these are named landmarks that any DFW driver recognizes. Use them. NAFTA context elevates I-35E from "another freeway" to "the spine of US truck freight" — that elevates the regulatory urgency. Bilingual emphasis higher here than other corridors — many I-35E victims will be Spanish-speaking commercial drivers or family members.

---

## T06 — I-20 Truck Accident Lawyer in Dallas

- **Target keyword:** i-20 truck accident lawyer dallas
- **Est. monthly volume:** 30
- **Competition:** Low-Medium
- **H1 (preserve):** I-20 Truck Accident Lawyer in Dallas
- **URL slug:** `/practice-areas/truck-accidents/i-20-truck-accidents-dallas/`
- **Word count:** 1,400-1,700
- **Audience profile:** Victim/family of a crash on I-20 — south Dallas County (Mesquite, Hutchins) east, or south Tarrant (Arlington, south Fort Worth) west. Heavy Hispanic and Black demographics along this corridor. Bilingual emphasis. Working class.
- **Lead stat (mandatory):** "Across both Dallas County and Tarrant County interstates combined, TxDOT recorded 131 fatal crashes and 149 deaths in 2024 — roughly one Interstate fatal crash every 67 hours across the two counties." (TxDOT Table 12, summed)
- **Required federal citations:**
  - 49 CFR § 395.3 (HOS)
  - 49 CFR § 395.22(i) (6-month ELD)
  - 49 CFR § 382.303 (post-crash testing)
  - Texas Transportation Code § 644
  - Texas Transportation Code § 545.351 (reasonable speed)
- **DFW geo-anchors (required — corridor page):**
  - **I-20 / I-35E interchange** in south Dallas (merge crash point)
  - **I-20 / I-820 interchange** in south Tarrant (multi-level stack)
  - **Grand Prairie and Arlington commercial corridor** (heavy regional drayage)
  - **Trinity River bridges** (uphill grade approaching, brake stress)
  - **Distribution centers** — Lancaster, Wilmer, Hutchins (south Dallas drayage), Arlington (south Tarrant)
  - **Transcontinental context** — Atlanta to Los Angeles freight artery
- **Suggested H2 outline (from seed):**
  1. Why I-20 is Especially Dangerous for Trucks (transcontinental + interchange geography + drayage mix)
  2. Common Causes of Truck Crashes on I-20
  3. Crash Data: What TxDOT Tells Us About Dallas + Tarrant Counties (honest framing)
  4. Who's Liable When a Truck Crash Happens on I-20
  5. Evidence That Disappears Within Days of an I-20 Truck Crash
  6. What To Do If You're in a Truck Crash on I-20
- **Cross-links:**
  1. `/faq/what-to-do-after-car-accident-in-texas/`
  2. `/practice-areas/truck-accidents/`
  3. T05: `/practice-areas/truck-accidents/i-35-truck-accidents-dallas/`
- **Tone notes:** The "two driving cultures sharing the same lanes" frame (long-haul drivers + regional drayage drivers) is the page's unique insight — keep it. The "every 67 hours" derived statistic from the lead is powerful — present it as derived (131 fatal crashes ÷ 8,760 hours per year) and frame it as "across both counties' interstates" not "on I-20." That's the honest-framing rule. The corridor extends into Parker and Kaufman counties too — if the writer wants to reference the full I-20 corridor, the data file lists Parker County (10 fatal interstate crashes, 11 deaths) and Kaufman County (1, 1) for 2024.

---

## T07 — I-30 Truck Accident Lawyer in Fort Worth

- **Target keyword:** i-30 truck accident lawyer fort worth
- **Est. monthly volume:** 25
- **Competition:** Low
- **H1 (preserve):** I-30 Truck Accident Lawyer in Fort Worth
- **URL slug:** `/practice-areas/truck-accidents/i-30-truck-accidents-fort-worth/`
- **Word count:** 1,400-1,700
- **Audience profile:** Victim/family of a Fort Worth/Arlington I-30 crash. Stadium-area readers, downtown Fort Worth, West 7th. Mix of Hispanic (south of I-30 in east FW), Black, white working class.
- **Lead stat (mandatory) — THE STRONGEST SINGLE STAT IN THE SET:** "Fatal commercial truck crashes in Tarrant County jumped 58% from 2022 to 2024 according to TxDOT — from 12 fatal CMV crashes in 2022 to 19 in 2024, the highest count in the three-year data window. That trend runs counter to the slight statewide decline in overall fatalities, and Fort Worth's busiest east-west freight corridor — I-30 — is squarely inside the geography driving that increase." (TxDOT Table 30, 2022 + 2024)

  *Expand on this lead: the Tarrant CMV trend is the most newsworthy stat in the dataset because it's moving the OPPOSITE direction of statewide overall fatalities (which declined ~3.3% statewide in 2024 per TxDOT Crash Facts). This contrast is the page's hero argument for why a Fort Worth truck case needs urgency.*

- **Required federal citations:**
  - 49 CFR § 395.3 (HOS)
  - 49 CFR § 395.22(i) (6-month ELD)
  - 49 CFR § 382.303 (post-crash testing)
  - Texas Transportation Code § 644
- **DFW geo-anchors (required — corridor page):**
  - **Downtown Fort Worth** (tight curves, pre-modern ramp geometry)
  - **West 7th corridor**
  - **AT&T Stadium and Globe Life Field** in Arlington (entertainment district surge traffic on Cowboys / Rangers game days)
  - **I-30 / I-35W interchange** in Fort Worth
  - **I-30 / I-820 interchange**
  - **I-30 / I-635 and I-30 / I-35E interchanges** in Dallas County (eastbound)
  - **Texarkana → Little Rock → Memphis** long-haul context (eastbound origin)
- **Suggested H2 outline (from seed):**
  1. Why I-30 is Especially Dangerous for Trucks (downtown FW + stadium area + interchange geo)
  2. Common Causes of Truck Crashes on I-30 (with stadium event-traffic call-out)
  3. Crash Data: What TxDOT Tells Us About Tarrant County (lead with the 58% trend)
  4. Who's Liable When a Truck Crash Happens on I-30
  5. Evidence That Disappears Within Days of an I-30 Truck Crash
  6. What To Do If You're in a Truck Crash on I-30
- **Cross-links:**
  1. `/faq/what-to-do-after-car-accident-in-texas/`
  2. `/practice-areas/truck-accidents/`
  3. T06: `/practice-areas/truck-accidents/i-20-truck-accidents-dallas/`
- **Tone notes:** This is the most stat-driven page in the set. The 58% Tarrant rise is the entire reason for the page's urgency framing — don't let it get buried. The "trend is moving the wrong direction" line should appear in the lead AND in the data H2. Game-day surge traffic at AT&T Stadium / Globe Life Field is a Fort Worth–specific insight no other DFW law firm is making — leverage it. Don't use slogans on the wrongful-death paragraph in the damages section.

---

## T08 — I-635 / LBJ Freeway Accident Lawyer in Dallas

- **Target keyword:** 635 lbj freeway accident lawyer
- **Est. monthly volume:** 45 (highest-volume corridor target in the set)
- **Competition:** Medium
- **H1 (preserve):** I-635 / LBJ Freeway Accident Lawyer in Dallas
- **URL slug:** `/practice-areas/truck-accidents/i-635-lbj-truck-accidents-dallas/`
- **Word count:** 1,400-1,800 (this is the highest-volume corridor page — give it depth)
- **Audience profile:** North Dallas County crash victims/families — Plano, Richardson, Garland, Mesquite commuters. Mix of working-class to upper-middle. Also some managed-lane crash victims who may include affluent Northern Dallas drivers.
- **Lead stat (mandatory):** "Across all Dallas County interstates — and I-635 is one of them — TxDOT recorded 81 fatal crashes and 90 deaths in 2024, with 27 fatal commercial motor vehicle crashes across all Dallas County roads that year." (TxDOT Tables 12 + 30, 2024)
- **Required federal citations:**
  - 49 CFR § 395.3 (HOS)
  - 49 CFR § 395.22(i) (6-month ELD)
  - 49 CFR § 382.303 (post-crash testing)
  - Texas Transportation Code § 644
- **DFW geo-anchors (required — corridor page):**
  - **LBJ/I-35E interchange** (one of the most reconstructed in DFW history)
  - **High Five interchange** at US-75
  - **LBJ Express managed-lanes segment** (between I-35E and US-75 — managed/tolled, distinct design)
  - **I-635 / I-30 eastern junction** through Mesquite
  - **I-635 / I-20 southern terminus**
  - **Commuter mix** — Plano, Richardson, Garland, Mesquite
  - **Northern Dallas LBJ Express** (managed-lane operator framing)
- **Suggested H2 outline (from seed):**
  1. Why I-635 is Especially Dangerous for Trucks (interchange density + commuter mix + managed-lane design)
  2. Common Causes of Truck Crashes on I-635 (with managed-lane confusion call-out)
  3. Crash Data: What TxDOT Tells Us About Dallas County (honest framing required; explicitly note "TxDOT does not publish I-635-specific fatal counts")
  4. Who's Liable When a Crash Happens on I-635 (include toll-road operator as a possible defendant for managed-lane crashes)
  5. Evidence That Disappears Within Days of an I-635 Crash (include LBJ Express operator data as a parallel preservation target)
  6. What To Do If You're in a Crash on I-635
- **Cross-links:**
  1. `/faq/what-to-do-after-car-accident-in-texas/`
  2. `/practice-areas/truck-accidents/`
  3. T05: `/practice-areas/truck-accidents/i-35-truck-accidents-dallas/`
- **Tone notes:** The managed-lane angle is unique to this page and is the most defensible reason to call this corridor "different." Be careful with managed-lane fatality claims — TxDOT does not publish managed-lane-specific data in free reports, so do NOT claim "X crashes in the LBJ Express" without source data. The seed handles this correctly with an explicit "design distinction is corridor context, not a crash-data claim" line — preserve that pattern. The "every major freight corridor crosses here" framing is the page's distinctive geographic argument.

---

## Final checklist before you mark a page "done"

For each of the 8 pages:

- [ ] H1 preserved from the seed and includes the target keyword
- [ ] Target keyword appears in the first 100 words of the lead
- [ ] Lead paragraph opens with the assigned TxDOT lead stat (per Lead-Stat Assignments table)
- [ ] All required federal regulation citations present (per Federal Regulation Cheat Sheet, this page's row)
- [ ] Every numeric claim has a footnote link to a `.txdot.gov` URL
- [ ] No corridor-specific TxDOT numbers claimed where the data file says "Data unavailable"
- [ ] Honest-framing language ("across all Dallas County interstates," etc.) present on every corridor page
- [ ] DFW Truck Crash Data block present with 3 source-linked footnotes
- [ ] Liability hedge sentence at bottom of DFW data block
- [ ] DFW geo-anchors named (corridor pages: minimum 4 named landmarks/interchanges)
- [ ] Wrongful-death section uses quiet/reverent tone — no slogan stack adjacent
- [ ] CTA module includes `{{CTA_PHONE}}` token, "Get Goff. Get Paid.", "You're not a case. You're family.", "No win. No fee.", Hablamos español
- [ ] Related Resources block: 3 links (Phase 1 FAQ #1 + truck practice hub + assigned Phase 2 sibling)
- [ ] Voice Guide rules followed — no banned words, "you" not "the client," Jim named, insurance framed as opponent
- [ ] No result promises, no "best/top/premier/elite"
- [ ] No competitor names anywhere
- [ ] Word count 1,400-1,800
- [ ] YAML frontmatter preserved and `updated_date` updated to your save date
- [ ] Saved to `recon/goff-law/phase2-drafts/<slug>.md`

---

## Things to AVOID across all 8 pages

- **NO competitor names.** Don't mention Mullen, Witherite, Reyes, Snellings, McCraw, Thompson, Aldous, or any other firm.
- **NO result promises.** Avoid "we'll get you the most money," "guaranteed settlement," "we never lose." Phase 2 truck cases attract attention from the State Bar more aggressively than smaller-injury practice pages — keep the result-promise discipline tight.
- **NO "best / top-rated / award-winning / premier / elite"** language.
- **NO invented TxDOT numbers.** Every stat traces to the data file or doesn't appear.
- **NO claiming a corridor-specific number** (mile marker, sub-type, single-Interstate fatality count) that the TxDOT data file marks "Data unavailable."
- **NO settlement amounts, verdicts, or attorney-credential claims** that haven't been pre-cleared. Jim handles compliance — your job is to not introduce risk.
- **NO excluded case-type framing in CTAs:** medical malpractice, nursing home, dog bite, workers' comp, defamation, SSDI, birth injury. Phase 2 is purely about commercial truck / 18-wheeler PI. If you're tempted to mention a non-truck case type, don't.
- **NO downplaying of severity.** This is the serious-case register — no light-touch language in the lead. Truck crashes kill people; the page acknowledges that without theatrics.

---

## Estimated time + delivery

For each page, expect ~2-2.5 hours of writing time given the federal-regulation research, voice rigor, and TxDOT citation discipline. Estimated 8 pages × 2.25 hrs = ~18 hours of writer time total.

**Publish all 8 together** once complete to avoid related-link 404s (cross-links assume all 8 sibling URLs are live).

If anything is ambiguous about a CFR section, a TxDOT stat, or a managed-lane factual claim — flag back to Jim before drafting. Better to ask than to ship a page that needs full rewrite or, worse, gets cited as inaccurate by opposing counsel later.
