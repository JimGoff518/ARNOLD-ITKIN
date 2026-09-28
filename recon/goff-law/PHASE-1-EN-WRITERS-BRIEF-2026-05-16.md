# Phase 1 EN — Writer's Brief: 10 Statewide FAQ Landing Pages

**Client:** Goff Law DFW (gofflawdfw.com)
**Attorney:** Jim Goff
**Project:** 90-day keyword execution plan — Phase 1 EN (English statewide / DFW question-driven FAQ traffic)
**Date issued:** 2026-05-16
**Target ICP:** Mixed working-class + middle-class DFW residents searching question-form queries after a wreck or injury. Broader than Phase 4 (which targets working-class only) because question-driven traffic pulls from every income tier — but Voice Guide tone still applies on every page.
**Total pages:** 10

---

## Read these BEFORE you start

| Document | Why |
|---|---|
| **`recon/goff-law/VOICE-GUIDE-v1-2026-05-16.md`** | The 10 voice rules + banned/preferred word list + persona. **Non-negotiable for tone.** Read this first, every time. |
| **`recon/goff-law/FAQ-CONTENT-BRIEF-2026-05-16.md`** | The original research brief that established H1s, slugs, keyword volumes, and H2 outlines for all 10 pages. |
| **`recon/goff-law/faq-drafts/page-01-what-to-do-after-car-accident-texas.md`** through **`page-10-when-to-get-a-lawyer-after-car-accident.md`** | The AI-drafted first passes. Use these for: statute citations, factual structure, H2 outlines, schema text. **Do NOT copy the body prose** — rewrite to the Voice Guide. Treat these as research material, not finished copy. |
| **`recon/goff-law/PHASE-4v2-WRITERS-BRIEF-2026-05-16.md`** | Reference for brief format and per-page-spec depth — same shape as this document. |

---

## What we need from you (Dianne)

For each of the 10 pages: a single markdown file containing:

1. The body copy — H1 + byline + lead + 5-8 H2 sub-question sections + CTA module + Related Resources block.
2. A meta description (one line, 150-160 chars, keyword-forward, written in Voice Guide voice — see CTA pattern below).

Save to: `recon/goff-law/faq-drafts-v2/<slug>.md` (use the slugs listed per page).

## What we'll handle (you don't need to write these)

- YAML frontmatter (Jim/Chelsea add it after content is final — title, slug, target_keyword, estimated_monthly_volume, word_count_target, byline, canonical_url, updated_date)
- FAQPage JSON-LD schema — **generated from your H2s and the first 1-2 sentences of each H2 section**, so write H2s as natural question-form headers where possible (or leave the AI-draft H2 as-is) and lead each section with a clean 1-2 sentence answer
- LegalService JSON-LD schema (universal template, Chelsea pastes)
- HowTo JSON-LD on Page 3 (Chelsea generates from your H2s)
- WordPress publishing, internal-link insertion, URL configuration

If you'd rather write the frontmatter, copy the format from any existing AI-draft file (lines 1-11).

---

## Brand architecture (LOCKED — use on every page)

| Slot | Hook |
|---|---|
| **Primary** | **Get Goff. Get Paid.** |
| **Secondary** | **You're not a case. You're family.** |
| **Cost reassurance** | **No win. No fee.** |
| **Spanish equivalents (in CTA only — these are EN pages)** | **Llame a Goff. Cobre lo suyo.** / **No eres un caso. Eres familia.** / **Sin ganar, sin pagar.** |

These appear in every CTA module. The full stacked architecture ("Get Goff. Get Paid. You're not a case. You're family.") is the close.

---

## Universal page structure — Phase 1 FAQ pages

| Section | Word count | Notes |
|---|---|---|
| H1 | — | Exact text per page below. Contains target keyword naturally. |
| Byline | 1 line | `By [Jim Goff](/attorneys/jim-goff/) \| Updated 2026-05-16` |
| Lead paragraph | 80-150 words | Restate the search query in plain language. Answer it in 1-2 sentences. Cite the controlling statute/rule if one exists. Tee up what the rest of the page covers. Target keyword in first 100 words. Voice = Jim talking to the Pleasant Grove mom on her couch at night. |
| H2 sections (5-8 per page) | 150-300 each | Follow the suggested H2 outline below. Each H2 opens with a clean 1-2 sentence answer (this becomes the schema snippet), then expands. Cite statutes by section number where listed. Use the banned-word substitutions. |
| CTA module | — | Use the universal CTA template (see below). `{{CTA_PHONE}}` token. Spanish line included. |
| Related Resources | 4 links | See per-page cross-link map. |

**Word count target per page: 1,200-1,800** (specific target per page listed below — match it within +/- 150 words).

---

## Universal CTA module template

Drop in at end of body, before Related Resources. Adapt the first line to the page topic.

```markdown
---

## Get Help Today

[ONE-LINE topic hook — e.g., "Hurt in a Texas wreck and not sure who pays your bills?"]

**Get Goff. Get Paid.** You're not a case — you're family.

**No win. No fee.** Free DFW consultation, available 24/7. Hablamos español.

**Call or text Jim now: {{CTA_PHONE}}**

[Button: Get My Free Case Review →]

Goff Law DFW serves Dallas, Tarrant, Collin, Denton, Rockwall, and Kaufman counties.

---
```

**Meta description pattern (writer authors this):** restate the question, give the one-sentence answer with the key fact/statute, end with the value prop. Voice Guide rules apply. Examples in each draft's `meta_description` frontmatter field — model on those but rewrite to Voice Guide if the AI-draft uses banned words.

---

## Universal Related Resources block

Every page links to exactly 4 destinations, in this order:

1. The main car-accident practice area page — `/practice-areas/car-accident/`
2. **The Phase 1 SOL page (Page 3)** — `/faq/personal-injury-statute-of-limitations-texas/` (skip if current page IS Page 3 — substitute Page 1 instead)
3. **One Phase 1 FAQ sibling** — assigned per page below (chosen for topical adjacency)
4. **One additional Phase 1 FAQ sibling** — assigned per page below

Format as a bulleted list under an `## Related Resources` H2.

---

## Per-page specs (10 pages)

### Page 1 — What To Do After a Car Accident in Texas

- **Target keyword:** what to do after a car accident in texas
- **Est. monthly volume:** 480 (Low competition) — **highest volume in the set**
- **Suggested H1:** `What To Do After a Car Accident in Texas: A Step-by-Step Guide`
- **URL slug:** `/faq/what-to-do-after-car-accident-in-texas/`
- **Word count target:** 1,500
- **Audience profile:** Person who just had a wreck, possibly in the last 48 hours. Mobile-first. Scared, adrenaline-down, not yet in litigation mindset. Mix of incomes; the working-class Pleasant Grove mom AND a Frisco software engineer are both reading this. Voice rules unify the tone.
- **Must-cite legal references:**
  - **Texas Transportation Code § 550.022** — duty to move vehicles out of moving traffic lane after non-injury crash
  - **CR-3** — Texas Peace Officer's Crash Report; officer files within 10 days; TxDOT online portal; ~$6-$8 cost
  - **CR-2** — old "blue form" self-report; eliminated 2017 (mention as historical context)
  - Leaving the scene of an injury crash = Texas felony (no specific statute cited in draft — keep general)
- **Key facts/data Dianne MUST include:**
  - Adrenaline masks injuries for hours/days — don't say "I'm fine" at the scene
  - The **8-shot photo checklist** (preserve the full list as drafted — it's the page's signature):
    1. Wide shot of entire scene
    2. All four corners of your vehicle
    3. Close-ups of every dent/scrape/broken part
    4. Other driver's license plate + wide shot of their vehicle
    5. Skid marks, debris, fluid leaks, final resting positions
    6. Traffic signals, stop signs, lane markings
    7. Your own injuries (re-shoot for 7 days — bruising peaks at 48-72 hrs)
    8. Other driver's insurance card and driver's license
  - 72-hour medical window — gap between crash and first doctor visit is the single biggest factor adjusters use to reduce claim value
  - Texas auto policies require "prompt notice" (24-48 hrs) to your own insurer
  - **Never give a recorded statement to the OTHER driver's insurance**
  - Event Data Recorder ("black box") holds ~20 seconds of crash data; can be lost if car gets totaled and crushed
  - Surveillance footage gets overwritten in 7-30 days
- **Suggested H2 outline (strategy-validated — modify if you have a stronger structure):**
  1. Step 1: Make sure everyone is safe and call 911
  2. Step 2: What to say (and NOT say) to the other driver
  3. Step 3: Texas crash-reporting rules — when CR-3 is required
  4. Step 4: Photograph everything — the 8-shot checklist
  5. Step 5: Get medical attention within 72 hours (why this matters for your claim)
  6. Step 6: Notify your insurance — what to say in the first 48 hours
  7. Step 7: When to call a Texas personal injury lawyer (and why waiting hurts your case)
- **Bilingual emphasis:** Standard — Spanish line in CTA module. Don't lead bilingual; ES audience gets its own ES-translated page in Phase 1 ES.
- **Cross-links (Related Resources):**
  1. `/practice-areas/car-accident/`
  2. `/faq/personal-injury-statute-of-limitations-texas/` (Page 3)
  3. `/faq/who-pays-medical-bills-after-car-accident-texas/` (Page 8 — closest topical sibling)
  4. `/faq/when-to-get-a-lawyer-after-car-accident/` (Page 10)
- **Tone notes / sensitivities:** This is a how-to page. Stay teacher-voice — calm, sequential, plain. Don't hard-sell early. Jim's voice = "this is what I'd tell a family member if they called me from the scene." Single CTA at the end.

---

### Page 2 — How Much Is My Personal Injury Case Worth?

- **Target keyword:** how much is my personal injury case worth
- **Est. monthly volume:** 390 (Low competition)
- **Suggested H1:** `How Much Is My Personal Injury Case Worth in Texas?`
- **URL slug:** `/faq/how-much-is-my-personal-injury-case-worth/`
- **Word count target:** 1,600
- **Audience profile:** Person already past the crash — has a claim open, talking to adjusters, trying to figure out if the offer they're hearing is reasonable. Higher comparison-shopper intent. Mix of incomes — the question "what's it worth" is universal.
- **Must-cite legal references:**
  - **Texas Civil Practice & Remedies Code § 41.0105** — "paid or incurred" challenge to inflated medical bills
  - **Texas Civil Practice & Remedies Code § 74.301** — medical malpractice non-economic cap ($250K against most providers)
  - **Texas Tort Claims Act** — sovereign immunity caps (~$250K per person / $500K per occurrence) for government-entity claims
  - **Texas Civil Practice & Remedies Code § 41.003** — punitive ("exemplary") damages require fraud, malice, or gross negligence by clear and convincing evidence
  - **Texas Civil Practice & Remedies Code § 41.008** — punitive cap formula (greater of $200K or 2x economic plus non-economic up to $750K)
  - **Texas modified comparative fault** — plaintiff over 50% at fault recovers nothing
- **Key facts/data Dianne MUST include:**
  - The **6 factors** that drive case value: injury severity, total medical bills (past + future), lost income + earning capacity, liability clarity, available insurance/assets, venue/jury pool
  - Economic damages categories (medical past/future, lost wages past/future, out-of-pocket, property damage)
  - Non-economic damages categories (physical pain, mental anguish, disfigurement, physical impairment, loss of enjoyment, loss of consortium)
  - **Most Texas PI cases have NO cap on pain and suffering** — caps only apply to med mal + government. Hook this to Goff's lane: motor vehicle + federal MDL = uncapped.
  - **Multiplier method** — econ damages × 1.5x to 5x based on severity; Colossus is the industry-standard software
  - Worked example: $30K medical + $10K wages = $40K economic; 3x multiplier → $40K + $120K = $160K rough value
  - Why early offers are too low (4 reasons): you don't know your damages yet, adjuster rewarded for cheap closes, adjuster bets you don't know value, release signature is permanent
  - The **3 things that increase case value most**: documented consistent medical treatment (no gaps), liability evidence locked down early, credible/prepared client
- **Suggested H2 outline:**
  1. The honest answer: it depends on these 6 factors
  2. Economic damages: medical bills + lost wages + future earnings
  3. Non-economic damages: pain, suffering, and Texas's caps
  4. Punitive damages — when Texas allows them
  5. How insurance companies calculate offers (the multiplier method)
  6. Why early settlement offers are almost always too low
  7. The 3 things that increase case value most
- **Bilingual emphasis:** Standard — Spanish CTA line only.
- **Cross-links:**
  1. `/practice-areas/car-accident/`
  2. `/faq/personal-injury-statute-of-limitations-texas/` (Page 3)
  3. `/faq/should-i-accept-first-settlement-offer/` (Page 6 — closest sibling)
  4. `/faq/pain-and-suffering-damages-texas/` (Page 9 — deep-dive on the non-econ portion)
- **Tone notes / sensitivities:** **No specific dollar promises.** When using example numbers, frame as "an example" or "a typical case might look like" — never "your case is worth X." Voice Guide rule 8 (no result promises) is doing heavy lifting on this page. Avoid the banned word "compensation" — use "money," "what you're owed."

---

### Page 3 — How Long Do I Have To File a Personal Injury Claim in Texas?

- **Target keyword:** how long do i have to file personal injury claim texas
- **Est. monthly volume:** 290 (Low competition)
- **Suggested H1:** `How Long Do I Have To File a Personal Injury Claim in Texas? (Statute of Limitations Guide)`
- **URL slug:** `/faq/personal-injury-statute-of-limitations-texas/`
- **Word count target:** 1,300
- **Audience profile:** Person whose injury happened a while ago — weeks, months, sometimes nearly two years. High urgency intent. May include surviving family members of someone who died (wrongful death section critical). Government-vehicle injury readers are a sub-segment with the most acute deadline pressure.
- **Must-cite legal references:**
  - **Texas Civil Practice & Remedies Code § 16.003(a)** — 2-year personal injury SOL
  - **Texas Civil Practice & Remedies Code § 16.003(b)** — 2-year wrongful death (from date of death, not date of injury)
  - **Texas Civil Practice & Remedies Code § 16.001** — minors' tolling (until age 18)
  - **Texas Civil Practice & Remedies Code § 16.063** — defendant's absence from Texas tolling
  - **Texas Civil Practice & Remedies Code § 71.021** — survival action (estate may pursue decedent's pre-death pain and suffering)
  - **Texas Tort Claims Act § 101.101** — 6-month written notice for claims against government entities
  - **City of Dallas charter** — 90-day notice (verify; draft cites this)
  - **City of Fort Worth** — 6-month notice
  - Texas Supreme Court discovery rule — limited to latent disease / hidden defect (asbestos, certain fraud, certain toxic exposure)
- **Key facts/data Dianne MUST include:**
  - "Bring suit" = file the lawsuit; demand letters / claim filings / hiring a lawyer DO NOT stop the clock
  - 730 days passes = right to sue is gone forever
  - Insurance company playbook: stringing along claimants with friendly emails for 22 months, then going dark for last 2 months
  - Tolling situations (narrow): minor under 18; mental incapacity at time of injury; defendant absent from Texas
  - Voluntary intoxication does NOT count as incapacity
  - Wrongful death — only spouse, children, parents have standing (NOT siblings, grandparents, unmarried partners)
  - Discovery rule applies to mass tort cases (hernia mesh, hair-relaxer cancer, defective medical devices) — relevant to Goff's federal MDL lane
  - Most Texas PI lawyers won't take a case with under 60 days left on the statute
  - Filing a lawsuit ≠ going to trial — most filed cases still settle, but filing preserves leverage
- **Suggested H2 outline:**
  1. The 2-year rule: Texas Civil Practice and Remedies Code § 16.003
  2. When the 2-year clock starts (and when it pauses)
  3. Exceptions: minors, mental incapacity, discovery rule
  4. Wrongful death: same 2 years, different start date
  5. Claims against government entities: 6-month notice rule (much shorter)
  6. Why "I'll wait and see" almost always backfires
- **Bilingual emphasis:** Standard — Spanish CTA line only.
- **Cross-links:**
  1. `/practice-areas/car-accident/`
  2. `/faq/what-to-do-after-car-accident-in-texas/` (Page 1 — substitute for SOL since this IS the SOL page)
  3. `/faq/when-to-get-a-lawyer-after-car-accident/` (Page 10 — urgency-paired)
  4. `/faq/who-pays-medical-bills-after-car-accident-texas/` (Page 8)
- **Tone notes / sensitivities:** This is the **hub page** of the Phase 1 set — every other page cross-links here. Schema gets a bonus **HowTo JSON-LD** on top of FAQPage (Chelsea generates) — Dianne, if you can structure the page so that the "how to calculate your filing deadline" workflow is implicit in the H2 progression, it'll feed the HowTo schema cleanly. Section 5 (government entities) is the highest-stakes section — write it like a fire alarm. Tone calibration: this is the "your house is on fire" page in the set; urgency is the brand here.

---

### Page 4 — How Much Do Personal Injury Lawyers Charge in Texas?

- **Target keyword:** how much do personal injury lawyers charge in texas
- **Est. monthly volume:** 280 (Low competition)
- **Suggested H1:** `How Much Do Personal Injury Lawyers Charge in Texas?`
- **URL slug:** `/faq/how-much-do-personal-injury-lawyers-charge-texas/`
- **Word count target:** 1,200 (shortest target in the set — be tight)
- **Audience profile:** Comparison shopper. Has decided they need a lawyer (or is close to it) and is now trying to understand the money math before they sign anything. High intent. Reads carefully. Will compare your number to two other firms' numbers. Includes a sub-segment who's been burned before or by a family member's experience with a sketchy fee deal.
- **Must-cite legal references:**
  - Texas requires fee agreements ("contingent fee contract") to be in writing and signed by the client
  - Texas referral fee splits permitted with proper disclosure
  - Most physical injury recoveries are tax-free (note: consult CPA)
- **Key facts/data Dianne MUST include:**
  - **Standard Texas contingency scale: 33⅓% pre-suit / 40% in litigation / 45% on appeal**
  - $0 upfront, $0 if no recovery, contingency aligns incentives
  - Three flows out of the trust account, in order: case expenses → attorney's fee → medical liens/subrogation → net to client
  - Common case expense categories: filing fees, medical records ($25-$200/provider), police reports + crash reconstruction, expert fees ($5K-$25K each), depositions, mediation, investigation, trial exhibits
  - **The critical question to ask: "Are case expenses deducted BEFORE or AFTER the attorney's fee is calculated?"** Net vs. gross model — worked example:
    - $300K settlement, $30K expenses, 40% fee
    - Net model: ($300K - $30K) × 40% = $108K fee; client nets $162K
    - Gross model: $300K × 40% = $120K fee; client nets $150K after expenses
  - Fee agreement read-before-you-sign checklist: percentage scale + when each tier triggers; expense handling (net vs. gross); subrogation/lien handling; termination clause / quantum meruit; referral fee disclosure; settlement authority always with you (the client)
  - Why "cheap" lawyers cost more in the end: volume-settlement model depends on closing files fast at low value; higher percentage of properly worked case often nets the client more
- **Suggested H2 outline:**
  1. Contingency fees explained: $0 upfront, paid only if you win
  2. The standard 33⅓% / 40% / 45% sliding scale in Texas
  3. What "case expenses" cover and who pays them
  4. The fee agreement: what to read before you sign
  5. How fees are calculated on a settlement vs. trial verdict
  6. Why "cheap" lawyers often cost more in the end
- **Bilingual emphasis:** Standard — Spanish CTA line only.
- **Cross-links:**
  1. `/practice-areas/car-accident/`
  2. `/faq/personal-injury-statute-of-limitations-texas/` (Page 3)
  3. `/faq/should-i-hire-a-personal-injury-lawyer/` (Page 5 — closest sibling)
  4. `/faq/how-much-is-my-personal-injury-case-worth/` (Page 2)
- **Tone notes / sensitivities:** Money page. Be **specific with numbers** — Voice Guide rule 10 (specifics over adjectives). Don't say "competitive rates" — say "33⅓% pre-suit." Avoid "compensation" (banned) — say "money," "what you recover." When discussing the net/gross math, walk through the dollar example. Section 6 ("cheap lawyers cost more") is the trust-building beat — let Jim sound like he's been on the wrong end of cleanup work from those firms.

---

### Page 5 — Should I Hire a Personal Injury Lawyer?

- **Target keyword:** should i hire a personal injury lawyer
- **Est. monthly volume:** 210 (Low competition)
- **Suggested H1:** `Should I Hire a Personal Injury Lawyer? (Honest Guide)`
- **URL slug:** `/faq/should-i-hire-a-personal-injury-lawyer/`
- **Word count target:** 1,400
- **Audience profile:** Decision-undecided. Probably has a real claim but hasn't committed. Susceptible to firms that hard-sell — so the honest "you might not need one" framing is the differentiator. Mix of incomes, leans middle-class (working-class searchers tend to skip this query and go straight to "lawyer near me").
- **Must-cite legal references:**
  - **Insurance Research Council (IRC) Auto Injury Claims Studies** — represented claimants recover ~3x more on average, even after attorney fees (industry-funded research; cite the source by name)
- **Key facts/data Dianne MUST include:**
  - When you probably DON'T need a lawyer (the honest list):
    - True minor fender-bender, no injury, property only
    - Property damage only — no one hurt
    - You were already paid fairly and the offer covers everything
    - Total claim value under $2,000-$3,000
  - The **5 situations where you absolutely need one**:
    1. ER visit, imaging (MRI/CT), or follow-up treatment
    2. Lost time from work (even a few days)
    3. Other driver uninsured/underinsured/fled the scene
    4. Commercial vehicle, truck, or rideshare crashes
    5. Insurance is denying liability, blaming you, or delaying
  - IRC stat: ~3x recovery for represented claimants — call it out as INSURANCE-INDUSTRY data, not plaintiff data
  - What adjusters won't tell you (4): first offer is a starting point; medical bills are negotiable; future medical is part of your claim; recorded statement can sink your case
  - What to look for in a Texas PI lawyer (5): recent Texas trial experience (last 2 years); who handles your case day-to-day; caseload per attorney; specialization not generalist; communication standard
  - 5 questions to ask in free consult: is my case worth pursuing; fee structure + expenses; realistic range of outcomes; how long; what can I do or not do right now
- **Suggested H2 outline:**
  1. When you probably don't need a lawyer (and we'll tell you so)
  2. The 5 situations where you absolutely need one
  3. The data: represented claimants recover 3x or more on average
  4. What insurance adjusters won't tell you
  5. What to look for in a Texas PI lawyer (beyond TV ads)
  6. Free consultations: what to ask in the first call
- **Bilingual emphasis:** Standard — Spanish CTA line only.
- **Cross-links:**
  1. `/practice-areas/car-accident/`
  2. `/faq/personal-injury-statute-of-limitations-texas/` (Page 3)
  3. `/faq/how-much-do-personal-injury-lawyers-charge-texas/` (Page 4 — closest sibling, fee-paired)
  4. `/faq/when-to-get-a-lawyer-after-car-accident/` (Page 10)
- **Tone notes / sensitivities:** This is the **trust-building page**. Section 1 (when you DON'T need us) is the most important section in the whole brief from a brand-voice perspective — it has to feel actually honest, not strategically honest. If you can name a real-sounding scenario where Jim has told someone "you don't need me," do it. Voice Guide rule 4 (name Jim) applies hard here — this is a Jim-on-the-phone moment. **No "best/top-rated/aggressive"** language anywhere (Voice Guide). The CTA can be slightly softer than other pages — the value prop here is honesty, not urgency.

---

### Page 6 — Should I Accept the First Settlement Offer?

- **Target keyword:** should i accept first settlement offer
- **Est. monthly volume:** 180 (Low competition)
- **Suggested H1:** `Should I Accept the First Settlement Offer From the Insurance Company?`
- **URL slug:** `/faq/should-i-accept-first-settlement-offer/`
- **Word count target:** 1,300
- **Audience profile:** Has an offer on the table right now, in their inbox or in a voicemail. Time-pressured. Emotionally invested in the idea of "being done with this." This is the "I'm about to sign something I shouldn't" page — write it like you're trying to stop someone from clicking the wrong button.
- **Must-cite legal references:**
  - "Full and Final Release of All Claims" — standard settlement release language; Texas courts enforce strictly
  - Texas exceptions for setting aside a release: fraud or mutual mistake (extremely hard to prove)
  - **Maximum Medical Improvement (MMI)** — the standard for when settlement should be considered
- **Key facts/data Dianne MUST include:**
  - First offer is **almost never** the fair number — anchoring tactic
  - Behavioral research: first number sets the psychological frame even when both sides know it isn't final
  - 5 reasons first offers are low: treatment not finished; future medical needs not on the table; lost earning capacity ignored; pain and suffering undervalued by Colossus-class software; you're under financial pressure
  - What "Full and Final" legally extinguishes: past medical bills, future medical (even if unknown), past + future lost wages, past + future pain and suffering, future-discovered disability, often claims against connected parties (employers, vehicle owners)
  - **The 4 questions to answer before signing:**
    1. Have I reached MMI, or do doctors expect more treatment?
    2. Does this offer cover ALL categories of damages?
    3. Have I subtracted what I'll actually owe (subrogation, liens, ERISA, Medicare/Medicaid)?
    4. Have I talked to a Texas PI attorney for a second opinion?
  - Typical Texas PI negotiation rhythm (6 steps): demand letter → first offer (25-40% of demand) → counter → second offer (50-65%) → continued negotiation → resolution or litigation
  - **~95% of filed cases still settle** — but for more after suit is filed
  - Movable lowballs vs. hard cases (the honest distinction):
    - Movable: clear liability, consistent medical, finished treatment, sympathetic story, adequate coverage
    - Hard: disputed liability, treatment gaps, pre-existing conditions, low-impact crash with serious-injury claim, minimum policy limits ($30K) with damages over coverage
- **Suggested H2 outline:**
  1. The short answer: almost never
  2. Why the first offer is designed to be low
  3. What "full and final" really means (and why it's permanent)
  4. The 4 questions to ask before accepting any offer
  5. How counter-offers actually work in Texas PI cases
  6. When a "lowball" can become a fair offer — and when it can't
- **Bilingual emphasis:** Standard — Spanish CTA line only.
- **Cross-links:**
  1. `/practice-areas/car-accident/`
  2. `/faq/personal-injury-statute-of-limitations-texas/` (Page 3)
  3. `/faq/how-much-is-my-personal-injury-case-worth/` (Page 2 — closest sibling, value-paired)
  4. `/faq/pain-and-suffering-damages-texas/` (Page 9)
- **Tone notes / sensitivities:** Insurance company is the opponent — Voice Guide rule 6 explicit here. Frame the adjuster as a trained professional doing a job — not as a villain (the system is the villain). CTA opener should be specific: "If you have an offer on the table right now, get a free second opinion before you sign." Avoid the banned word "compensation" — use "money," "what you're owed." Be **direct about the asymmetry** — they have software and training; you have a phone and adrenaline.

---

### Page 7 — What To Do If You're Injured at Work in Texas (When It's NOT Workers' Comp)

- **Target keyword:** what to do if injured at work texas
- **Est. monthly volume:** 170 (Low competition)
- **Suggested H1:** `What To Do If You're Injured at Work in Texas (When It's NOT Workers' Comp)`
- **URL slug:** `/faq/injured-at-work-texas-third-party-claim/`
- **Word count target:** 1,500
- **Audience profile:** Worker who got hurt on the job. Most are searching this assuming workers' comp applies. Page's job is to filter — keep the ones with a third-party / non-subscriber / 1099 angle, refer the pure WC ones out. Demographically: heavy working-class, often Hispanic on construction/oilfield/delivery jobs, often distrustful of "the system." Voice Guide working-class register lands hard here.
- **Must-cite legal references:**
  - **Texas Labor Code § 406.033** — non-subscriber employer loses contributory negligence, assumption of risk, fellow-servant defenses
  - **Texas Labor Code § 408.001(b)** — surviving family exemplary damages claim for gross negligence in workplace death cases
  - **Texas Labor Code § 409.001** — 30-day employer notice deadline for workers' comp claims
  - **Texas Civil Practice & Remedies Code § 16.003** — 2-year SOL for negligence claims
  - **Texas Department of Insurance, Division of Workers' Compensation** — free public database at tdi.texas.gov to verify subscriber status
- **Key facts/data Dianne MUST include:**
  - **MANDATORY DISCLAIMER AT THE TOP** (this is a Jim-locked decision):
    > Goff Law DFW does **not** handle workers' compensation claims. If your injury is comp-only — your employer carries Texas workers' comp insurance and no third party caused your injury — we'll refer you to a workers' comp specialist at no charge. This page covers what to do if your case is **not** a standard workers' comp claim.
  - Texas is the ONLY state where workers' comp is optional for private employers
  - ~28% of Texas employers are non-subscribers (Texas Department of Insurance data)
  - **The 4 situations where you have a claim outside WC:**
    1. Employer is a non-subscriber
    2. A third party caused your injury
    3. You're a 1099 contractor
    4. Gross negligence resulting in death (even with WC coverage)
  - Third-party scenarios: another driver hit you while driving for work; defective equipment from a manufacturer; another contractor on a multi-employer worksite; negligent property owner; commercial trucks (federal trucking regs + corporate insurance)
  - 1099 reality cuts both ways: no automatic WC, but free to sue under regular negligence. Misclassification is common; hold-harmless clauses not always enforceable in Texas; gross negligence waivers limited.
  - **The damages comparison table** (preserve this table — it's the page's signature):
    | Damage | Workers' Comp | Third-Party / Non-Subscriber |
    |---|---|---|
    | Medical bills | Paid, capped by state fee schedule | Paid in full, including future care |
    | Lost wages | ~70% AWW, capped | Full lost wages, past + future |
    | Lost earning capacity | Limited impairment benefit | Full economic loss |
    | Pain and suffering | **Not available** | Full recovery (no cap in most TX cases) |
    | Mental anguish | **Not available** | Full recovery |
    | Disfigurement | Limited | Full recovery |
    | Loss of consortium | **Not available** | Available |
    | Exemplary (punitive) damages | Only in gross-negligence death cases | Available for gross negligence |
  - 30-day employer notice trap: even if pursuing third-party, give written notice to employer within 30 days to preserve every option
- **Suggested H2 outline:**
  1. When you can sue beyond workers' comp in Texas
  2. The non-subscriber employer loophole (Texas is unique)
  3. Third-party negligence claims: when someone else caused your work injury
  4. 1099 contractor injuries — workers' comp may not apply at all
  5. How damages differ from workers' comp (no caps on pain/suffering)
  6. The 2-year clock and the 30-day employer-notice trap
- **Bilingual emphasis:** Slightly elevated — the demo here skews to construction/oilfield/delivery workers, many Spanish-first. Keep the Spanish CTA line but consider a soft Spanish callout at the top of the CTA module (e.g., "Hablamos español. Su estatus no importa. No preguntamos.")
- **Cross-links:**
  1. `/practice-areas/car-accident/`
  2. `/faq/personal-injury-statute-of-limitations-texas/` (Page 3 — critical: dual deadline page)
  3. `/faq/should-i-hire-a-personal-injury-lawyer/` (Page 5 — closest filter-traffic sibling)
  4. `/faq/who-pays-medical-bills-after-car-accident-texas/` (Page 8)
- **Tone notes / sensitivities:** **The workers' comp disclaimer at the top is non-negotiable** — Jim's lane is explicitly NOT workers' comp (Jim's exclusion list per project memory). The page filters traffic; that's the strategy. Don't bury the disclaimer; it goes above the lead. Use "the company" or "the employer's insurance" framing — Voice Guide rule 6 holds. Don't say "victim of negligence" — say "someone who got hurt." Avoid suggesting Goff handles WC even peripherally; the refer-out promise is the trust signal.

---

### Page 8 — Who Pays Medical Bills After a Car Accident in Texas?

- **Target keyword:** who pays medical bills after car accident texas
- **Est. monthly volume:** 150 (Low competition)
- **Suggested H1:** `Who Pays Medical Bills After a Car Accident in Texas?`
- **URL slug:** `/faq/who-pays-medical-bills-after-car-accident-texas/`
- **Word count target:** 1,400
- **Audience profile:** Has bills arriving NOW. ER bill, ambulance bill, follow-up doctor bill. Panicked about how to pay. May not yet have a lawyer. Often lower-income — this is a high-stress, working-class-heavy query. The page has to answer the immediate question (you pay first, then get reimbursed) without making the reader feel doomed.
- **Must-cite legal references:**
  - **Texas Insurance Code § 1952.152** — mandatory $2,500 PIP unless rejected in writing
  - Texas is a fault-based insurance state (at-fault driver legally responsible, but no payment obligation until liability + damages established)
  - **Texas minimum bodily injury liability: $30,000 per person / $60,000 per accident**
  - ERISA self-funded plans — strongest subrogation rights
  - Texas "made whole" doctrine — limits fully-insured plan subrogation when client didn't recover full damages
  - Medicare and Medicaid federal lien rights — must be resolved before case closes
- **Key facts/data Dianne MUST include:**
  - **Headline answer:** In Texas, you pay your medical bills first and get reimbursed later. The at-fault driver's insurance does not cut a check until your treatment is finished and your case is settled.
  - **PIP basics:** $2,500 default Texas-mandatory PIP; no-fault; covers medical + lost wages + replacement services; also covers passengers; ~30 days to pay after submission; can buy higher limits ($5K, $10K, $25K) for usually <$100/year
  - PIP rejection trap: many drivers signed the rejection without reading it; check declarations page
  - **MedPay vs. PIP differences:**
    - PIP: medical + lost wages + replacement services
    - MedPay: medical only
    - MedPay typically has higher limits available
    - MedPay does not require written rejection (you have it or you don't)
    - Many DFW drivers carry both = stacked coverage
  - **Health insurance subrogation** — most plans can demand reimbursement; ERISA strongest; Texas "made whole" doctrine; Medicare/Medicaid federal liens
  - Skilled negotiators routinely reduce health insurance subrogation claims by 30-50%
  - Don't let an ER tell you they can't bill health insurance because it was a car accident — that's a billing-desk reflex, not the law
  - At-fault carrier process: 6-18 months typical for a case; requires full medical records, itemized bills, lost wages proof, medical causation opinion, signed release
  - **About 20% of Texas drivers are uninsured** — UM/UIM is the cheapest catastrophic-injury insurance you can buy ($10-$30/month for $100K+ in coverage)
  - **Letters of Protection (LOPs)** — attorney's written promise to medical provider that bill gets paid from settlement; allows specialists/MRIs/surgery/PT at $0 out of pocket; DFW network of orthopedists, neurologists, pain mgmt, surgical centers, imaging facilities accept them
  - LOP caveat: provider bills sometimes come in higher than insurance-negotiated rates; lawyer negotiates them down at end of case
- **Suggested H2 outline:**
  1. Short answer: you pay first, then get reimbursed (here's why)
  2. PIP coverage: Texas's $2,500 default + opt-out
  3. MedPay vs. PIP: what's different
  4. Health insurance: subrogation rights and what they take back
  5. The at-fault driver's insurance: when (and how) they pay
  6. What happens if the other driver is uninsured (UM/UIM coverage)
  7. Letters of protection: how lawyers get treatment without upfront cost
- **Bilingual emphasis:** Slightly elevated — high working-class density on this query. Spanish CTA line at minimum; consider a one-line callout that hospitals can bill regardless of immigration status.
- **Cross-links:**
  1. `/practice-areas/car-accident/`
  2. `/faq/personal-injury-statute-of-limitations-texas/` (Page 3)
  3. `/faq/what-to-do-after-car-accident-in-texas/` (Page 1 — closest sibling)
  4. `/faq/when-to-get-a-lawyer-after-car-accident/` (Page 10)
- **Tone notes / sensitivities:** This is a **fear-management page**. The lead has to acknowledge "the painful truth" (Voice Guide-compatible — bills first, reimbursement later) and immediately offer the solution path (PIP/MedPay/health/LOPs). Don't be cheery. Don't be doomy either. Calm + specific. The LOP section is the **emotional payoff** — "you can get the treatment with $0 out of pocket if we structure it right." Avoid "compensation" — use "money," "what you're owed." Frame the at-fault insurance as the opponent that won't pay until forced to.

---

### Page 9 — How Much Can You Sue For Pain and Suffering in Texas?

- **Target keyword:** how much can you sue for pain and suffering in texas
- **Est. monthly volume:** 190 (Low competition)
- **Suggested H1:** `How Much Can You Sue For Pain and Suffering in Texas?`
- **URL slug:** `/faq/pain-and-suffering-damages-texas/`
- **Word count target:** 1,500
- **Audience profile:** Searcher is in active research mode and probably has a real injury (broken bone, back issue, head injury). They want a number. Page can't give one — but it CAN give the math, the categories, and the caps that don't apply. Mix of incomes, leans middle-class on this query.
- **Must-cite legal references:**
  - **Texas Civil Practice & Remedies Code Chapter 41** — damages generally; punitive caps; does NOT cap compensatory pain and suffering in ordinary negligence
  - **Medical malpractice non-economic cap: $250,000** against a single provider (2003 tort reform)
  - **Texas Tort Claims Act caps: $250K per person / $500K per occurrence** for most municipal claims
  - **Most Texas PI cases — no cap on pain and suffering** (this is the page's core message)
  - Colossus, Claims IQ — proprietary insurance valuation software
- **Key facts/data Dianne MUST include:**
  - The 5 categories of pain and suffering in Texas: physical pain (past + future); mental anguish (anxiety, depression, PTSD, fear, humiliation); physical impairment (loss of ability to do things); disfigurement (scars, amputations); loss of consortium (spouse's claim in serious cases)
  - **Multiplier method tiers:**
    - 1.5x-2x — minor soft-tissue, full recovery
    - 2x-3x — moderate, months of treatment, some lasting symptoms
    - 3x-4x — serious, surgery, ongoing pain or limitation
    - 4x-5x+ — catastrophic, permanent disability, lifetime impact
  - Worked example: $40K medical + surgery + nerve damage → adjuster might say $80K-$120K (2-3x); plaintiff lawyer might argue $160K-$200K (4-5x). Gap = where good lawyering lives.
  - Multiplier is a negotiating convention, not law; juries don't have to use it; catastrophic cases routinely blow past multiplier predictions.
  - **Per-diem method:** daily wages × days from injury to MMI. Example: $250/day × 600 days = $150K. Especially effective for chronic-pain and long-recovery cases.
  - Per-diem and multiplier are usually used as cross-checks
  - **The cap clarity hook:** ONLY med mal + government cases have non-econ caps. Car wreck, truck crash, motorcycle, commercial vehicle, defective products, federal mass torts = NO CAP. **Goff's lane = uncapped.**
  - Why adjusters undervalue vs. juries (3): software discounts mental anguish; software discounts future suffering; software assumes you won't file suit
  - Cases that go to mediation post-filing routinely settle for **2-5x the first pre-suit offer**
  - **Documentation that increases awards:** tell every doctor every symptom; daily pain journal; see right specialists; mental health treatment if needed; weekly recovery photos; family testimony
  - **Range of awards by injury type (GENERIC ranges only — no specific verdicts):**
    - Soft tissue with full recovery — low five figures
    - Surgical orthopedic with full recovery — high five to low six figures
    - Permanent orthopedic with ongoing pain — mid six figures
    - TBI / spinal cord / severe burns — high six to seven figures
    - Catastrophic / quadriplegic / wrongful death — seven figures+
- **Suggested H2 outline:**
  1. Pain and suffering damages: what counts in Texas
  2. The multiplier method (1.5x – 5x medical bills)
  3. The per-diem method (and when juries use it)
  4. Caps that apply: medical malpractice ($250K) — and why most cases have NO cap
  5. How insurance adjusters value pain and suffering differently than juries
  6. Documentation that increases pain-and-suffering awards
  7. Range of awards by injury type
- **Bilingual emphasis:** Standard — Spanish CTA line only.
- **Cross-links:**
  1. `/practice-areas/car-accident/`
  2. `/faq/personal-injury-statute-of-limitations-texas/` (Page 3)
  3. `/faq/how-much-is-my-personal-injury-case-worth/` (Page 2 — closest sibling, value-paired)
  4. `/faq/should-i-accept-first-settlement-offer/` (Page 6)
- **Tone notes / sensitivities:** **CRITICAL — generic ranges only. NO specific verdict citations.** Per Voice Guide rule 8 (no result promises) and Jim-handles-compliance memory. Section 7 award-range list must be framed as "general ranges" and explicitly note "every case is different, no lawyer can promise a specific outcome." Section 4 has a real differentiation hook — when the page says "most cases have NO cap on pain and suffering" and ties it to Goff's lane (motor vehicle + federal MDL, both uncapped), it doubles as a positioning move. Don't say "the client" — say "you." Don't say "compensation" — say "money," "what a jury can award."

---

### Page 10 — When To Get a Lawyer After a Car Accident

- **Target keyword:** when to get a lawyer after car accident
- **Est. monthly volume:** 220 (Low competition)
- **Suggested H1:** `When To Get a Lawyer After a Car Accident in Texas`
- **URL slug:** `/faq/when-to-get-a-lawyer-after-car-accident/`
- **Word count target:** 1,300
- **Audience profile:** Just-after-the-crash window — closer to Page 1 audience than Page 5. High urgency. Already suspects they need a lawyer; trying to confirm the timing. Mix of incomes; the question is universal but skews slightly working-class.
- **Must-cite legal references:**
  - Texas contingency fee model (referenced — not a statute citation but a system reference)
  - Spoliation letter — preservation demand sent to at-fault driver, insurer, tow yard
  - **EDR (Event Data Recorder) "black box"** — ~20 seconds of crash data; lost if vehicle totaled and crushed
  - CR-3 — Texas Peace Officer's Crash Report
- **Key facts/data Dianne MUST include:**
  - **The headline answer: within the first 7 days, almost always.**
  - The "call this week" trigger list: hospital/ER visit; missed work; pain at 72 hours; commercial vehicle involved; any fatality; other driver's insurance has called you
  - **3 evidence problems that get worse every day you wait:**
    1. Witnesses forget (useful day 1, different account day 14, useless day 60)
    2. Vehicles repaired/scrapped (tow yards release in 15-30 days; black-box data + crush patterns + brake/tire/airbag data gone forever)
    3. Surveillance footage overwritten (30-day cycle, sometimes 7-14 days)
  - By day 30, two of three evidence categories may be unrecoverable. By day 60, often all three.
  - **Insurance adjuster speed:** at-fault carrier notified within 24 hrs; by 48 hrs they've often called the at-fault driver for recorded statement, pulled the police report, calculated settlement range, started trying to reach you, begun looking for liability defenses
  - **3 adjuster traps in the first call:**
    - "Just confirm you're feeling fine today, right?"
    - "Can you describe what happened in your own words?"
    - "We'd like to send you a quick $1,500 to cover the inconvenience"
  - **Specific "don't wait" triggers** (8): ambulance/hospital admission; commercial vehicle; you were a passenger; uninsured/hit-and-run driver; >1 day missed work; pain at 72 hours; other driver's insurance has contacted you; fatality
  - **What a lawyer does in the first 48 hours (7 things):**
    1. Spoliation letter — preserve vehicle + EDR
    2. Preservation requests to nearby businesses for surveillance
    3. Take over all insurance communication
    4. Pull CR-3, identify witnesses for early outreach
    5. Coordinate medical treatment (LOPs if no health insurance)
    6. Open case file (photos, statements, records authorizations, timeline)
    7. Notify your own insurance for PIP / MedPay / UM/UIM
  - **Cost: $0 to call, $0 to hire** (contingency); $0 if we lose. Standard fees: 33⅓% / 40% / 45%.
- **Suggested H2 outline:**
  1. The honest answer: within the first 7 days, almost always
  2. The 3 evidence problems that get worse every day you wait
  3. Why insurance adjusters move faster than you think
  4. Specific triggers: when waiting is malpractice on yourself
  5. What a lawyer does in the first 48 hours
  6. Cost: $0 to call, $0 to hire (contingency)
- **Bilingual emphasis:** Standard — Spanish CTA line only.
- **Cross-links:**
  1. `/practice-areas/car-accident/`
  2. `/faq/personal-injury-statute-of-limitations-texas/` (Page 3 — deadline-paired)
  3. `/faq/should-i-hire-a-personal-injury-lawyer/` (Page 5 — closest sibling)
  4. `/faq/what-to-do-after-car-accident-in-texas/` (Page 1)
- **Tone notes / sensitivities:** Urgency page — pairs with Page 3 (SOL) as the two pages where the brand voice leans most into "the clock is moving." Section 4 H2 uses the phrase "when waiting is malpractice on yourself" — this is sharp and on-voice; keep something like it. Section 6 (cost) should be reassuring after the urgency setup — "and by the way, it's free." Insurance company = opponent (Voice Guide rule 6). Avoid "the client" → "you" (rule 2). Don't say "the attorney" → "Jim" or "the lawyer" (rule 4).

---

## Things to AVOID across all 10 pages

- **NO competitor names.** Do not mention Mullen & Mullen, Witherite, Angel Reyes, Snellings, McCraw, Thompson, Aldous, Lyons & Simmons, Hamilton Wingo, J. Alexander, or any other firm. Differentiate by Goff's positives, not by attacking others.
- **NO result promises.** Voice Guide rule 8. Avoid: "we'll get you the most money," "guaranteed settlement," "we always win." Use "we fight to get every dollar we can" / "we don't get paid unless you do."
- **NO specific verdict citations.** Generic ranges only on Page 9. "Tens of thousands" / "six figures" / "seven figures" framings are fine. Specific dollar amounts tied to specific case results require Jim's pre-approval.
- **NO "best / top-rated / award-winning / premier / elite / aggressive / tireless / decades of experience"** language. Voice Guide rules 1, 8, 10.
- **NO lawyer jargon.** Banned word list (Voice Guide): compensation, damages, maximum recovery, collision, victim of negligence, plaintiff, defendant, negligence (use "they hurt you" / "they were careless"), pursue legal action, pre-litigation phase, aggressive representation, tireless advocacy, time of need, insurance carrier, opposing party, counsel, retain our services, schedule a consultation, subsequent to the accident, statute of limitations (use "the deadline to sue" when speaking plainly; cite the statute name where load-bearing).
- **NO mention of excluded case types in CTA modules:** medical malpractice, nursing home abuse, dog bite (generic), workers' comp (Page 7 is the exception — and that page disclaims it explicitly), birth injury, SSDI, defamation, generic slip-and-fall. If a Phase 1 page surfaces one of these cases, refer-out language is the answer (Page 7 has the template).
- **NO stock-photo placeholders or image specs in body copy.** Visual selection happens elsewhere.
- **NO "the client" — always "you."** Voice Guide rule 2.
- **NO "the firm" — always "we."** Voice Guide rule 3.
- **NO "the attorney" / "our managing partner" — always "Jim" or "Jim Goff."** Voice Guide rule 4.

---

## Per-page checklist — mark each page "done" only when ALL are true

For each of the 10 pages:

- [ ] H1 contains target keyword (natural reading, not awkward)
- [ ] Target keyword appears in first 100 words of body
- [ ] Byline `By [Jim Goff](/attorneys/jim-goff/) | Updated 2026-05-16` present under H1
- [ ] Lead paragraph is 80-150 words, answers the query in the first 2 sentences, restates the controlling statute/rule by name where applicable
- [ ] All required statute citations from the "Must-cite legal references" list appear in the body, by section number
- [ ] All required facts/data from the "Key facts/data" list appear in the body
- [ ] H2 outline matches the suggested outline (or has a strategy-equivalent alternative — flag to Jim if you change it)
- [ ] Each H2 section opens with a clean 1-2 sentence answer (this feeds the FAQPage schema)
- [ ] CTA module uses the universal template, includes `{{CTA_PHONE}}` token, includes Spanish "Hablamos español" line
- [ ] Brand architecture stack present in CTA: "Get Goff. Get Paid." + "You're not a case. You're family." + "No win. No fee."
- [ ] Related Resources block contains exactly 4 links, in the specified order, per the cross-link map for this page
- [ ] Meta description written (150-160 chars, restates question + key answer fact + value prop, Voice Guide rules applied)
- [ ] Word count within +/- 150 of the per-page target
- [ ] Voice Guide rules followed — no banned words, "you" not "the client," Jim named, insurance framed as opponent, no result promises
- [ ] No competitor names anywhere
- [ ] No specific verdict citations (Page 9 — generic ranges only)
- [ ] Page 7 only: workers' comp disclaimer is the FIRST thing under the H1 (above the lead)
- [ ] Saved to `recon/goff-law/faq-drafts-v2/<slug>.md`

---

## Prioritization order

Write in this order — highest-traffic + foundation pages first, so the cross-link graph fills in cleanly as you go:

1. **Page 1 — What to do after a car accident** (480/mo) — highest volume; the foundation page; cross-link destination for many others
2. **Page 3 — SOL / how long do I have to file** (290/mo) — the hub page; cross-linked from every other page; gets the bonus HowTo schema
3. **Page 2 — Case worth** (390/mo) — second-highest volume; foundational to Page 6 and Page 9
4. **Page 4 — Lawyer fees** (280/mo) — money page; paired with Page 5
5. **Page 10 — When to get a lawyer** (220/mo) — urgency page; paired with Page 3
6. **Page 5 — Should I hire a lawyer** (210/mo) — trust page; paired with Page 4
7. **Page 9 — Pain and suffering** (190/mo) — deep-dive on non-economic damages; requires Page 2 first
8. **Page 6 — First settlement offer** (180/mo) — urgency page; requires Page 2 first
9. **Page 7 — Injured at work** (170/mo) — filter-traffic page; standalone (no required predecessor)
10. **Page 8 — Who pays medical bills** (150/mo) — lowest volume; references Page 1 and Page 10

**Publish all 10 together** once complete to avoid related-link 404s. Estimated writing time per page: ~1.5-2 hours given the research and voice rigor. Total ~16-20 hours.

---

## Questions? Stuck?

Anything ambiguous about strategy, voice, statute scope, or a fact you can't verify in the existing drafts — flag to Jim or ask before drafting. Better to ask than to ship a page that needs a full rewrite. **Do not invent facts or statute citations** — if it's not in the AI-draft or this brief, stop and ask.
