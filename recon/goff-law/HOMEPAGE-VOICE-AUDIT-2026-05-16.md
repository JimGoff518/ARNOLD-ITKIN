# gofflawdfw.com Homepage — Voice Guide Audit + Fix-It List

**Audit date:** 2026-05-16
**Source:** Live fetch of `https://gofflawdfw.com` (homepage only — `/about` + `/practice-areas` returned HTTP 404)
**Standard:** [VOICE-GUIDE-v1-2026-05-16.md](VOICE-GUIDE-v1-2026-05-16.md)
**Auditor brief:** Identify every voice violation, propose specific rewrites, prioritize by leverage.

---

## TL;DR — the 5 things that matter most

1. **The hero is the KILLED slogan.** "Serious injuries, Serious results." is the page headline. We killed this 2026-05-16 because it's generic. Replace with **Get Goff. Get Paid. / You're not a case. You're family.** P0.

2. **Jim's strongest differentiator is buried in paragraph 3.** Jim used to be an insurance-defense lawyer — he ran the playbook the other side uses against your clients. This belongs ABOVE THE FOLD as the hero hook. Right now it's the third paragraph of an About section nobody reads. P0.

3. **Zero Spanish on the entire site.** Your stated ICP is working-class Black and Hispanic DFW. The site has no `Hablamos español`, no Spanish CTA, no language toggle. This is your single biggest commercial miss. P0.

4. **The site contradicts your case-exclusion list.** Homepage About mentions premises liability, investor fraud, partnership disputes, breach of contract — and the footer lists Sexual Assault as a practice area. Either you take these (which contradicts memory) or this is leftover old copy. Either way: positioning is muddied. P1.

5. **No practice-area hub pages, no attorney bio page.** `/about` and `/practice-areas` both 404. This means when Dianne publishes Phase 1-5, every cross-link to those parent URLs breaks. Hub pages need to exist before the 56 drafted pages go live. P1 — but a blocker, not just a polish.

---

## What's working (don't touch these)

Before the cuts, what's actually good and SHOULD be preserved or amplified:

1. **"Out of town lawyers who have never driven down Abrams Road"** — buried in About paragraph 2. This is the BEST sentence on the entire site. Specific, local, anti-establishment. Voice Guide-perfect. Promote it.
2. **"In his time fighting on behalf of the biggest insurance companies in Texas, Mr. Goff learned what insurance adjusters value most: giving you as little as you deserve until they are forced to."** — Voice Guide gold. Promote to hero.
3. **"Small firm attention, big firm results"** — works as a secondary line. Could pair with the locked brand architecture.
4. **Real awards** — Top 40 Under 40, Super Lawyers, Best Lawyers in America. These are real credentials. Promote them visibly.
5. **`/contact` phone number captured: `972-928-0085`** — now plug this into every `{{CTA_PHONE}}` token across the 56 drafted pages before publish.

---

## Section-by-section audit

### Section 1 — HERO (above the fold)

#### Current state
| Element | Copy |
|---|---|
| Headline | "Serious injuries, Serious results." |
| Main hero text | "Millions Won" |
| CTA | "Contact Us" / "Call Us 24/7" |

#### Violations
- **Rule 4 (Name Jim. Always.):** Jim's name is nowhere in the hero. The page is supposed to encode the brand into recall — instead, anyone could read this hero and not know who Jim is.
- **Killed slogan still live:** "Serious injuries, Serious results." was replaced 2026-05-16 per the Voice Guide. Get this off the page.
- **"Millions Won" is a Rule 7.02 risk:** It implies a result promise without context (what timeframe? cumulative? per case?). Vague enough to be either misleading or meaningless.
- **CTA is generic:** "Contact Us" / "Call Us 24/7" doesn't name Jim, doesn't address customer fear, doesn't use the brand architecture, no bilingual.
- **No social proof above the fold:** Per the local SEO playbook (60% of leads from map pack, reviews = #1 ROI lever), the hero should surface a review snippet, star count, or named-result trust signal.

#### Proposed rewrite (full above-the-fold)

```
[H1] Get Goff. Get Paid.
[Sub] You're not a case. You're family. · No eres un caso. Eres familia.

[Hero hook paragraph, 30 words]
Jim Goff used to fight for the biggest insurance companies in Texas.
Now he fights them — for you. Hurt in a DFW wreck? He'll tell you
straight up if you have a case.

[CTA stack]
[BUTTON, primary] Call Jim now: (972) 928-0085
[BUTTON, secondary] Free case review →
[Inline] No win. No fee. · Hablamos español. · Available 24/7.

[Trust strip]
★★★★★ Top 40 Under 40 · Super Lawyers · Best Lawyers in America
```

**What this fixes:**
- Locked brand architecture in the hero (Get Goff / Get Paid / You're not a case / Sin ganar parallel)
- Jim named (Rule 4)
- Killed slogan removed
- The single strongest differentiator (defense-counsel background) is now the hook, not buried in paragraph 3
- Spanish line in the hero (ICP alignment)
- CTA is action + name + cost reassurance + bilingual + availability — every fear addressed in one block
- Awards become trust strip, not buried at the bottom
- Phone number is the actual number, not a token

---

### Section 2 — ABOUT (3 paragraphs)

#### Paragraph 1 — Current
> "At Goff Law, PLLC you are not just another case–YOU are the case. We strive to serve the one person who matters most: YOU. We do not serve ourselves. Our focus is to serve individuals throughout the Dallas-Fort Worth metroplex through a often confusing and challenging legal process. Our firm focuses on only serving individuals who have been injured in an accident or lost their investment because of the actions of someone they trusted."

#### Violations
- **Rule 1 (Talk like a person, not a lawyer):** "We strive to serve the one person who matters most" — corporate-speak loop.
- **Rule 2 (You, not the client):** "serving individuals" — should be "you."
- **Rule 4 (Name Jim):** "Goff Law, PLLC" is the legal entity, not the brand. Use "Goff Law DFW" or "Jim Goff."
- **Banned phrase:** "We strive to" — corporate.
- **Typo:** "a often" should be "an often."
- **POSITIONING PROBLEM:** "lost their investment because of the actions of someone they trusted" — this is investor fraud, NOT in the stated PI lane per case-exclusion list. Either Jim takes investor fraud cases (in which case the keyword strategy needs to expand) or this is leftover old copy that's muddying the brand.
- **Voice Guide already has a sharper version of the first line:** "You're not a case. You're family." beats "you are not just another case—YOU are the case" in 6 words instead of 14.

#### Proposed rewrite
> "Get Goff. Get Paid. You're not a case — you're family.
>
> Jim Goff is a Dallas personal injury lawyer. He started Goff Law DFW in 2023. He takes the calls himself. He works the cases himself. He gets paid when you get paid."

#### Paragraph 2 — Current
> "As a lifelong resident of Dallas, Mr. Goff has recently seen a rapid influx of out of town lawyers who have never driven down Abrams Road think they know or care about the Dallas community. As a third generation Texan and a lifelong Dallas resident, the people of Dallas are our friends, our neighbors, and our loved ones. We strive to provide honest and aggressive representation during the hardest, most vulnerable position in your life. Mr. Goff's practice has focused exclusively on litigation in Texas State and Federal District Courts throughout the country representing both Plaintiffs and Defendants. Mr. Goff's practice has encompassed the broad spectrum of both personal injury and commercial litigation, including wrongful death, auto accidents, premises liability, investor fraud, partnership disputes, as well as breach of contract."

#### Violations
- **Rule 4:** "Mr. Goff" — should be "Jim" or "Jim Goff" (the formal honorific is corporate).
- **Banned phrase:** "honest and aggressive representation" — "aggressive" is banned (Rule 10).
- **Banned phrase:** "during the hardest, most vulnerable position in your life" — corporate-speak (Voice Guide banned: "time of need" pattern).
- **Rule 1:** "Plaintiffs and Defendants" — civilians don't process this language.
- **POSITIONING PROBLEM (cont.):** "encompassed the broad spectrum of both personal injury and commercial litigation, including wrongful death, auto accidents, premises liability, investor fraud, partnership disputes, as well as breach of contract." — Mixed practice. Premises liability = excluded per case list. Investor fraud / partnership disputes / breach of contract = commercial law, dilutes PI positioning.

#### KEEP this part (rare voice-perfect line):
> "out of town lawyers who have never driven down Abrams Road think they know or care about the Dallas community"

Promote this. Specific. Local. Anti-establishment. This is the rare native Voice Guide sentence on the page.

#### Proposed rewrite
> "Jim grew up in Dallas. Third-generation Texan. He's seen out-of-town lawyers who have never driven down Abrams Road show up here and pretend they know the city. The people of Dallas are his neighbors. He's not interested in being a billboard lawyer.
>
> Jim handles car wrecks, truck and 18-wheeler crashes, motorcycle accidents, rideshare collisions, wrongful death, and federal mass-tort lawsuits for defective drugs and devices. He doesn't handle workers' comp, most medical malpractice, dog bites, or generic slip-and-falls — for those, he'll refer you to a lawyer he trusts."

(The second paragraph here is also a fix for the **case-exclusion contradiction** — it explicitly names what Jim does and doesn't take.)

#### Paragraph 3 — Current (THIS IS THE BURIED GOLD)
> "Before opening Goff Law, PLLC, Mr. Goff practiced with a prominent personal injury defense litigation firm in Dallas. In his time fighting on behalf of the biggest insurance companies in Texas, Mr. Goff learned what insurance adjusters value most: giving you as little as you deserve until they are forced to. Mr. Goff has the unique perspective of knowing how the insurance companies value your doctors, your injuries, their risk, and your future. Let us handle your past and work with you on your future."

#### What's wrong
- **Buried.** This is paragraph 3 of a 3-paragraph wall. Nobody reads paragraph 3 of an About section. THIS IS THE STRONGEST DIFFERENTIATOR ON THE ENTIRE SITE and it's in the worst position.
- **Rule 4:** "Mr. Goff" → "Jim."
- **"Let us handle your past and work with you on your future"** — generic closer that doesn't land.

#### Proposed rewrite (PROMOTE TO HERO HOOK OR ABOVE-THE-FOLD CALLOUT)

> "Jim used to work for the insurance companies.
>
> Before opening Goff Law DFW, Jim spent years on the defense side — fighting FOR the biggest insurance companies in Texas. He saw exactly how adjusters value your doctors, your injuries, and your future: as little as possible, for as long as possible, until they're forced to pay.
>
> Now he uses what he learned on the other side. For you."

This is the ONE thing that makes Jim impossible to compete with on this dimension. Promote it.

---

### Section 3 — CAR ACCIDENT ATTORNEY block

#### Current
> "Texas consistently ranks among the states with the highest number of car accidents in the United States due to its large population, new residents, and distracted drivers. Car wrecks can cause devastating injuries and financial hardships.
>
> Our team has extensive experience handling all types of car wreck cases, from rear-end collisions to drunk drivers and hit-and-runs. We are here to help you navigate the complex legal process and recover the compensation you deserve."

#### Violations
- **Generic.** No DFW specificity. No named landmarks/highways. Could be ANY Texas firm.
- **Rule 3:** "Our team" — use "we" or "Jim."
- **Banned phrases:** "extensive experience" (Rule 10), "compensation" (use "money" / "what you're owed"), "complex legal process" (corporate-speak), "navigate" (corporate).
- **Stats are stale:** "In 2023, there were 3,855 fatal car crashes in Texas" — we're in 2026. The Phase 2 TxDOT data has 2024 numbers. Update.

#### Proposed rewrite
> "If you got hurt in a wreck in DFW — on I-35, in a Plano parking lot, anywhere from Mesquite to Mansfield — Jim Goff has handled the case.
>
> Texas had 4,150 traffic fatalities in 2024 (TxDOT). Dallas County alone saw 305 fatal crashes — about 1 every 29 hours. Most of those weren't accidents. Someone was careless. And the insurance company is going to come at you fast.
>
> Jim handles rear-end collisions, drunk-driver crashes, hit-and-runs, and rideshare wrecks. He'll tell you straight up if you have a case. No fee unless you win.
>
> **Get Goff. Get Paid.**"

---

### Section 4 — TRUCK ACCIDENT ATTORNEY block

#### Current
> "Truck wrecks can result in catastrophic injuries and significant financial losses for victims due to the size and weight of most commercial vehicles. Trucking wrecks often involve multiple liable parties, including trucking companies, brokers, drivers, manufacturers, and Amazon trucks.
>
> Our comprehensive approach to truck accident litigation involves thorough investigation, meticulous case preparation, and aggressive advocacy to ensure our clients receive maximum compensation for their injuries, medical expenses, lost wages, and pain and suffering.
>
> Whether you've been injured in a collision with a commercial truck, semi-trailer, or tractor-trailer, we're here to fight for your rights and hold the responsible parties accountable."

#### Violations
- **Banned words:** "comprehensive approach," "thorough investigation," "meticulous case preparation," "aggressive advocacy" — all corporate-speak (Rule 1, Rule 10).
- **Banned phrase:** "maximum compensation" — Rule 7 + Rule 8 (result promise + corporate money word).
- **Banned word:** "victims" — Voice Guide preferred: "someone who got hurt" or "you."
- **Rule 6 missed:** Insurance/trucking company should be framed as opponent. Currently neutral.
- **"injured" + "collision"** — Voice Guide preferred: "hurt" + "wreck."
- **Rule 4:** Jim not named.

#### Proposed rewrite
> "Dallas County had 27 fatal commercial-truck crashes in 2024. Tarrant County had 19 — up 58% from 2022. Together, DFW accounts for 8.4% of every fatal truck crash in Texas, in just two counties (TxDOT).
>
> Truck cases are different. The trucking company has insurance lawyers on retainer who show up within hours. They'll send adjusters to the scene before the tow truck leaves. And they'll start losing evidence — driver logs, ELD data, dashcam footage — by the end of week one.
>
> Jim sends preservation letters the same day you call. He pulls the carrier's FMCSA SMS scores. He knows exactly how the trucking company's defense lawyers think — because he used to be one.
>
> **Get Goff. Get Paid.**"

---

### Section 5 — DANGEROUS DRUGS/PRODUCTS block

#### Current
> "At our law firm, our team of seasoned attorneys is deeply committed to representing individuals affected by defective products and dangerous drugs. We specialize in tackling complex cases that involve product defects, safety oversights, and negligence by large corporations. Our mission is to advocate vigorously for the rights of victims and to secure the compensation they rightfully deserve.
>
> Product defects can arise from flawed design, manufacturing errors, or failure to provide adequate warnings or instructions. Similarly, pharmaceutical products can become dangerous due to side effects that were not properly disclosed or due to unsafe ingredients. In any of these scenarios, our firm is dedicated to holding responsible parties accountable, ensuring that justice is served for the harm they have caused to consumers.
>
> If you've been injured by a dangerous product or drug, seek legal assistance promptly. You have the right to pursue full and fair compensation."

#### Violations
This is the most corporate-speak-saturated section on the page. Violations on nearly every line:
- "At our law firm, our team of seasoned attorneys" — Rule 3 (use "we" not "our team"), Rule 10 ("seasoned" = banned adjective).
- "deeply committed to representing individuals" — corporate-speak.
- "We specialize in tackling complex cases" — corporate-speak.
- "Our mission is to advocate vigorously for the rights of victims" — corporate-speak + "vigorously" banned + "victims" banned.
- "Our firm is dedicated to holding responsible parties accountable, ensuring that justice is served" — corporate-speak loop.
- "seek legal assistance promptly" — use "call Jim" or "call us today."
- "pursue full and fair compensation" — "full and fair" + "compensation" both banned.

#### Proposed rewrite
> "If a drug company hid side effects from you, or a medical device hurt you — you have a federal lawsuit. Jim Goff handles them.
>
> Active cases Goff Law DFW is working on right now: AFFF firefighting foam (cancer), Hernia mesh (revision surgery, chronic pain), Hair relaxer (uterine and ovarian cancer), Paragard IUD (breakage during removal). These are federal multi-district litigation cases — the kind the big mass-tort billboards farm out to call centers in other states.
>
> Jim works your case himself. From Dallas. In federal court.
>
> **Get Goff. Get Paid.**"

(This rewrite also fixes a real positioning issue: it names the specific active MDLs Jim does, which connects directly to the Phase 3 mass-tort pages Dianne will write.)

---

### Section 6 — WHY CHOOSE US block

#### Current
> **Heading: WHY CHOOSE US**
>
> "Experience matters. We have experience defending the insurance companies. We know what they are going to use against you in your accident case and what it takes to ensure your maximum recovery.
>
> Small firm attention, big firm results. At Goff Law you get the experience and results you would expect from the lawyers you see on the billboards but a level of customer service that cannot be matched. Size matters, go with someone who knows you and most importantly, your case.
>
> Recognized in Texas as the best of the best. Despite launching in 2023, Goff Law has already been recognized as one of the top law firms in the Metroplex. Jim Goff has received the following awards:
> Top 40 under 40
> SuperLawyer
> BestLawyers in America"

#### Violations
- **Heading: WHY CHOOSE US** — generic. Replace.
- **"Experience matters" / "Recognized in Texas as the best of the best" / "top law firms"** — banned (Rule 10: no "best/top-rated").
- **"maximum recovery"** — banned (Rule 7/8).
- **"customer service that cannot be matched"** — corporate-speak.
- **"Despite launching in 2023"** — apologetic framing; reframe positively.

#### KEEP / amplify
- **"We have experience defending the insurance companies. We know what they are going to use against you in your accident case"** — strong voice. KEEP, but rework.
- **Real awards (Top 40 Under 40, Super Lawyers, Best Lawyers in America)** — KEEP, formatted better.

#### Proposed rewrite
> **Heading: WHY JIM**
>
> **Jim worked for the insurance companies. Now he works for you.**
> Before opening Goff Law DFW, Jim spent years on the defense side, fighting FOR the biggest insurance companies in Texas. He knows the playbook because he ran it. He knows how the adjusters value your doctor, your injuries, your future. And he knows what it takes to make them pay.
>
> **You won't be a case here. You'll be family.**
> Jim takes the calls. Jim works the case. Jim gets paid when you get paid. There's no junior associate, no assigned paralegal — just Jim and the team he built.
>
> **Real awards from real lawyers and judges.**
> ★ Texas Super Lawyers
> ★ Best Lawyers in America
> ★ Top 40 Under 40
>
> Awarded since 2023.

---

### Section 7 — FOOTER

#### Current footer practice-area links
| Link | Issue |
|---|---|
| Sexual Assualt Attorney | **TYPO** ("Assualt" → "Assault"). Also: is this in Jim's actual lane? Charla Aldous owns sexual assault per memory. Needs Jim confirmation. |
| Hair Relaxer Lawsuits | ✓ In-lane (Phase 3 M5/M6) |
| Car Accident Attorney | ✓ In-lane |
| Electric Scooter Accident | ✓ In-lane (Phase 5 E1) |
| Amazon Truck Accident | ✓ In-lane (Phase 3 M9/M10) |
| Truck Accident Attorney | ✓ In-lane (Phase 2) |
| Brain Injury Attorney | ✓ In-lane (catastrophic, no Texas caps) |
| Drunk Driving Accident | ✓ In-lane |

#### Footer recommendations
- Fix "Assualt" → "Assault" typo immediately (P0 — typos in a lawyer's footer = trust killer).
- Confirm whether Jim takes sexual assault cases. If yes, leave the link. If no (because Aldous owns it), remove.
- Add Spanish footer block: "Hablamos español. Llame a Jim al (972) 928-0085."
- Add GBP review widget or review snippet block in footer.

---

## Cross-cutting infrastructure findings

### 1. Missing hub pages (BLOCKER for Phase 1-5 publish)
- `/about` returns 404. Build it. Jim's bio + the defense-counsel story + the brand architecture + awards belong here.
- `/practice-areas` returns 404. Build a parent page that lists all practice areas with one-liner descriptions, links to each individual practice page.
- `/attorneys/jim-goff/` — does this exist? Every drafted page (44 drafts + 16 Phase 4 v2) links to this. Verify. If not, build the bio stub.

### 2. No Spanish presence anywhere
- No language toggle in header.
- No `/es/` URL structure.
- No `Hablamos español` line in CTA, footer, or hero.
- This is the single biggest commercial alignment miss vs. the ICP.

### 3. No social proof above the fold
- No GBP review widget visible.
- No "★★★★★ 4.9 (XX reviews)" trust strip.
- No client testimonial blocks.
- Per local SEO playbook, reviews = #1 ROI lever for working-class consumers.

### 4. CTA architecture inconsistent
- Hero CTA: "Contact Us" / "Call Us 24/7"
- Practice area CTAs: implicit/missing
- Footer CTA: "Let's Get In Touch" with a generic form
- No unified primary CTA pattern. Every block should have the same CTA voice (Get Goff. Get Paid. + Call Jim now + bilingual).

### 5. Typos
- "Assualt" in footer
- "a often" in About paragraph 1 (should be "an often")
- Both unacceptable on a lawyer's site.

### 6. Stale data
- "In 2023, there were 3,855 fatal car crashes in Texas" — 2024 numbers are available (TxDOT 4,150). Update.

### 7. Case-exclusion-list contradictions
Homepage mentions practice areas that contradict the stated case-exclusion list:
- Premises liability (in About) — excluded
- Investor fraud (in About) — outside stated PI lane
- Partnership disputes (in About) — outside stated PI lane
- Breach of contract (in About) — outside stated PI lane
- Sexual Assault (footer link) — unclear if in lane

Decide whether these stay or go. The decision affects keyword strategy.

---

## Prioritized action list

### P0 — Ship this week (highest leverage, lowest effort)

| # | Action | Effort | Why P0 |
|---|---|---|---|
| 1 | Replace hero with the proposed rewrite (Get Goff. Get Paid. + buried-gold defense-counsel hook + bilingual CTA + awards trust strip) | 2 hrs WP work | Every visitor sees the killed slogan today. Fix the front door. |
| 2 | Fix "Assualt" typo in footer | 5 min | Trust-killer typo on a lawyer's site |
| 3 | Update phone number token `{{CTA_PHONE}}` → `972-928-0085` across all 56 drafted pages | 30 min global find-replace | Unblocks all 56 pages for publish |
| 4 | Add bilingual line ("Hablamos español. Llame al 972-928-0085.") to footer + hero + every CTA module | 1 hr WP work | ICP alignment — Hispanic working class is the demo |

### P1 — Ship this month (medium leverage, medium effort)

| # | Action | Effort | Why P1 |
|---|---|---|---|
| 5 | Build `/about` page using the proposed About rewrites + Jim's bio | 4 hrs (writing + WP build) | Currently 404; cross-link target for all 56 pages |
| 6 | Build `/practice-areas` parent page listing all practice areas with one-line descriptions | 3 hrs | Currently 404; cross-link target for Phase 2/3/5 pages |
| 7 | Build `/attorneys/jim-goff/` bio page | 3 hrs (overlaps with #5 if architecture combines) | All 56 drafted pages link to this byline URL |
| 8 | Rewrite all 3 practice-area homepage blocks (Car Accident, Truck Accident, Dangerous Drugs/Products) per the proposed rewrites | 2 hrs | Brings the homepage practice copy in line with Voice Guide + brand architecture |
| 9 | Update stale 2023 stats to 2024 TxDOT numbers | 30 min | E-E-A-T / freshness signal |
| 10 | Decide on case-exclusion contradictions (premises liability, investor fraud, partnership disputes, breach of contract, sexual assault) — remove or expand keyword strategy to cover | 1 hr decision + 30 min copy edits | Positioning clarity |

### P2 — Ship this quarter (lower leverage, higher effort)

| # | Action | Effort | Why P2 |
|---|---|---|---|
| 11 | Add GBP review widget / star-rating trust strip near hero | 2 hrs (depends on theme) | Local SEO playbook #1 ROI lever |
| 12 | Build a Spanish-language site at `/es/` (parallel hub) — or at minimum a Spanish landing page | 8 hrs+ | Major ICP investment; pairs with Phase 1b ES drafts |
| 13 | Add testimonial blocks (with proper consent + Texas Rule 7.02 compliance) | Time-variable | Trust signal |
| 14 | Add a language toggle in the header | 3 hrs dev | UX for Spanish-language users |

---

## What this audit DOES NOT cover (out of scope, flag for follow-up)

- Page-speed / Core Web Vitals performance audit
- Schema markup audit (separate technical SEO pass)
- Mobile UX audit (separate UX recon — Phase 1 UX recon at `recon/goff-law/UX-RECON-PHASE-1.md` covered this, scored Goff 25/70 vs Witherite 53/70)
- Backlink profile / off-page SEO
- GBP audit (separate — see `recon/GBP-AUDIT-RESULTS-2026-05-16.md`)
- Inner page audits beyond homepage (e.g., individual practice area pages if they exist on different slugs)

---

## What I'd ship next, if you want to attack a P0

The single highest-leverage 2-hour task: **replace the hero with the proposed rewrite.** That alone fixes:
- Killed slogan removal
- Brand architecture deployment
- Promotes the buried-gold defense-counsel hook
- Adds bilingual presence above the fold
- Adds the real awards as a trust strip
- Names Jim
- Replaces vague "Millions Won" with concrete CTA

If Chelsea has WordPress access, this is a 2-hour edit that changes the front door of the firm. The other P1 work compounds AFTER the hero is right.

Want me to draft the exact HTML/Gutenberg block code for the new hero so Chelsea can paste it in?
