# Phase 1b ES — Writer's Brief: 8 Spanish-Language FAQ Landing Pages

**Client:** Goff Law DFW (gofflawdfw.com)
**Attorney:** Jim Goff
**Project:** Spanish FAQ pillar pages — Phase 1b ES (companion to Phase 1 EN FAQ stack)
**Date issued:** 2026-05-16
**Target ICP:** DFW Hispanic working-class, mostly Mexican-origin, first-time legal services user
**Writer of record:** Dianne

---

## Read these BEFORE you start

| Document | Why |
|---|---|
| **`recon/goff-law/VOICE-GUIDE-v1-2026-05-16.md`** | The 10 voice rules + banned/preferred word list + **the "Spanish parallel" table at the bottom** is your primary vocabulary key. **Non-negotiable for tone.** Read this first. |
| **`recon/goff-law/SPANISH-KEYWORDS-2026-05-16.md`** | 184 Spanish DFW PI keywords. Section 3 contains the FAQ pillar candidates — your 8 pages map directly to the highest-volume entries there. |
| **`recon/goff-law/faq-drafts-spanish/`** (all 8 files) | AI-drafted starting point for each of your 8 pages. Mine these for vocabulary, cultural framing and structural cues — they are NOT shippable as-is. Your job is to refine, tighten, and pressure-test against the Voice Guide. |
| **`recon/goff-law/faq-drafts/`** (10 EN FAQ files) | Your hreflang pair partners. Each ES page links bidirectionally to its EN sibling. |
| **`recon/goff-law/PHASE-4v2-WRITERS-BRIEF-2026-05-16.md`** | The Phase 4 v2 brief is the format/structure model for this document — match its rigor. |

---

## What we need from you

For each of the 8 pages: a markdown file with the body copy (H1 + lead + H2 sections + CTA + Recursos Relacionados block + schema blocks + hreflang block). Save to `recon/goff-law/faq-drafts-spanish-v2/<slug>.md`.

The existing files in `faq-drafts-spanish/` are your **starting drafts**. Your final output should reflect:
- Voice Guide compliance (especially the Spanish parallel table)
- Native Mexican-Spanish vocabulary throughout (see "Mexican Spanish vocabulary guidance" section below)
- All cross-links wired to the correct ES sibling + EN hreflang pair
- The universal Spanish CTA block (provided below) on every page
- Schema JSON-LD with `"inLanguage": "es-US"`

## What we'll handle (you don't need to write these)

- WordPress publishing + URL setup at `/es/faq/<slug>/`
- Schema validation in Google Rich Results Test before push
- hreflang reciprocal link verification (we run a crawl post-publish)
- `{{CTA_PHONE}}` token replacement at publish time
- Spanish hub page creation at `/es/areas-de-practica/` (referenced in cross-links but built separately)

---

## Brand architecture (LOCKED — Spanish version, use on every page)

| Slot | Hook (Spanish) | English source |
|---|---|---|
| **Primary** | **Llame a Goff. Cobre lo suyo.** | Get Goff. Get Paid. |
| **Secondary** | **No eres un caso. Eres familia.** | You're not a case. You're family. |
| **Cost reassurance** | **Sin ganar, sin pagar.** | No win. No fee. |
| **Phone reassurance** | **Contestamos el teléfono.** | We pick up the phone. |
| **Status reassurance** | **Su estatus no importa. No preguntamos.** | Your status doesn't matter. We don't ask. |

These appear in every CTA module and at the top of every page. Source: Voice Guide v1, Spanish parallel table (lines 187-201).

---

## Mexican Spanish vocabulary guidance

DFW Spanish-speakers are ~75% Mexican-origin (Census ACS 2023). Vocabulary skews Mexican vernacular over Castilian or Caribbean variants. The Voice Guide's Spanish parallel table is your primary reference — the calls below extend and codify it for the FAQ context.

### Preferred vs. avoid (Mexican Spanish for DFW)

| Concept | USE (Mexican DFW) | AVOID (wrong register or wrong dialect) | Why |
|---|---|---|---|
| Car | **carro** (informal) or **auto** (neutral) | coche (Spain), automóvil (overly formal) | "Carro" wins in informal queries per keyword research (rank #4 Dallas head term); "auto" works in formal headers |
| Insurance | **aseguranza** (vernacular) or **aseguradora** (formal/correct) | el seguro (when referring to the company specifically) | "Aseguranza" is the working-class DFW Mexican-American term; "aseguradora" is the legally correct term. **Use "aseguranza" in body copy and CTAs, "aseguradora" once in formal contexts like statute citations.** This is a deliberate code-switch — the Voice Guide endorses it. |
| Lawyer | **abogado** | letrado (Spain), licenciado (used in Mexico as a title but feels stiff in PI marketing) | Voice Rule 4 = "Name Jim. Always." — so use "Jim Goff" first, "Jim," or "abogado" second |
| Crash / Wreck | **choque** (preferred, Mexican vernacular) or **accidente** (neutral) | colisión (legalese), siniestro (insurance-industry jargon) | "Choque" is keyword rank #8 in Dallas; matches Voice Rule 6 anti-jargon |
| To sue | **demandar** | querellar (criminal-law connotation), entablar acción judicial (legalese) | Plain, direct |
| Personal injury | **lesiones personales** | daños personales (Caribbean variant), perjuicios personales (overly formal) | Matches highest-volume Spanish keyword ("abogado de lesiones personales") |
| 18-wheeler / Big rig | **camión de 18 ruedas** (high-volume keyword) or **tractocamión** (Mexican formal) | semi-remolque (too formal), tráiler (Anglicism but acceptable as alt) | Use both in the same page when possible to capture variant queries |
| Money / Compensation | **dinero**, **lo que le deben**, **lo que cobre** | compensación (lawyer-speak — banned in Voice Rule 7), recompensa (wrong nuance), indemnización (legalese OK once for accuracy) | Voice Rule 7 explicitly bans "compensación" in body copy. Use "dinero" or "lo que le deben." Indemnización is OK in formal statute paragraphs (1 use max per page). |
| Hurt / Injured | **lesionado**, **herido**, **lo lastimaron** | accidentado (passive, removes agency), víctima (avoid victim-language per Voice Rule) | Voice Rule 2: "you" not "the client" — frame as direct: "si lo lastimaron" |
| Wrongful death | **muerte injusta** (standard TX legal Spanish) | homicidio culposo (criminal-law framing), fallecimiento (too soft) | Use "muerte injusta" in headers; "fallecimiento" is OK in sympathetic context (intro to wrongful death intake) |
| Hit-and-run | **atropello y fuga** | huida después de accidente (descriptive but not natural) | Mexican-Spanish standard |
| Statute of limitations | **plazo de prescripción** | (no good alternative — this is the correct term) | Always cite English statute number in parens: "el Código de Práctica Civil y Recursos de Texas, sección 16.003 (Texas Civil Practice and Remedies Code § 16.003)" |
| Settlement | **arreglo** (vernacular) or **acuerdo** (neutral) | transacción (legalese), conciliación (formal but uncommon) | "Arreglo" is more natural for working-class readers; "acuerdo" for headers |
| Health insurance | **seguro médico** | seguro de salud (acceptable, less common in DFW) | Stick with "seguro médico" |
| Contingency fee | **pago por contingencia** or **honorarios de contingencia** | tarifa contingente (wrong calque) | Both are acceptable. Pair with the plain-language explanation: "$0 por adelantado — solamente cobramos si ganamos." |
| Pain and suffering | **dolor y sufrimiento** | daños morales (Spain variant, can confuse), penas (vague) | Direct translation reads cleanly. "Daños morales" is OK once if explaining the term. |
| You / formal address | **usted** (throughout) | tú (too informal for legal content) | All 8 pages = "usted" form. The persona (Pleasant Grove mom) expects respect. Mexican Spanish in formal/professional contexts defaults to "usted." |
| Undocumented | **indocumentado** | ilegal (offensive, never use), sin papeles (informal — OK in dialogue framing but not as the technical term) | "Indocumentado" matches the keyword research (high-volume Section 3 query) and is the respectful term |

### Don't translate these — keep in English (with Spanish parenthetical context)

- **Texas statute citations** — always cite in English: "Texas Civil Practice and Remedies Code § 16.003" / "Texas Labor Code § 406.033" / "Texas Insurance Code § 1952.152" / "Texas Tort Claims Act"
- **Brand names** — Uber, Lyft, Amazon, DoorDash, AT&T, Paragard, Colossus, Blue Cross, ERISA, Medicare, Medicaid
- **Document codes** — CR-3, MMI (Maximum Medical Improvement), PIP, MedPay, UM/UIM, MDL, EDR (Event Data Recorder), LOP (Letter of Protection)
- **Defined legal terms used in a US-Texas context** — "discovery rule," "made whole doctrine," "subrogation," "quantum meruit," "Letter of Protection" — translate them inline once, then keep the English term for accuracy: *"la regla del descubrimiento (en inglés, discovery rule)"*

### Code-switching is allowed and natural

Pages may include code-switched phrases like *"firmar el release"* or *"la carta de subrogation"* when the reader will encounter those exact words on insurance forms. The keyword research (Section 8, "abogado hernia mesh español Dallas") confirms 2nd-gen DFW Hispanic users code-switch in search. Don't over-purify the Spanish to the point of unfamiliarity.

---

## Cultural sensitivities (apply across all 8 pages, called out per-page below)

The Hispanic DFW working-class audience for these pages carries specific concerns that affect read-through and conversion. Address them **explicitly** on the relevant page, not as caveats but as primary content.

### The three concerns that block conversion

1. **Immigration status anxiety.** The single biggest reason DFW Hispanic accident victims do not call a lawyer. Lead-pipe address: *"Su estatus migratorio NO afecta su derecho a recibir compensación bajo la ley de Texas."* This sentence (or its equivalent) appears on **every page** that touches "should I call a lawyer" intent — that's pages S01, S05, S07, and S08. Don't bury it as a final paragraph; treat it as a top-of-page trust signal where relevant.

2. **Cost / "no tengo dinero para un abogado."** This is the second biggest barrier. The contingency fee structure is *the* answer, but it has to be explained in plain Spanish — not as "honorarios de contingencia" but as "nosotros no cobramos a menos que ganemos. $0 por adelantado." Lead with the dollar amount, not the term. Pages S04 and S05 carry the heaviest load here.

3. **Bilingual service as feature, not accommodation.** Voice Rule 9. Never write "se ofrece traducción al español" or "hablamos un poco de español." Write: *"Hablamos español. Jim contesta su llamada en español si lo prefiere."* This frames Spanish as native-quality service, not a courtesy add-on. Every CTA includes this line.

### Tone register for Hispanic working-class DFW

- **Formal "usted" throughout** — never "tú." The persona (DFW Mexican-American mom or dad, working-class, 30-55) expects respect from a professional, and "tú" reads as condescending or overly familiar.
- **Family-first framing where authentic.** Voice Guide secondary hook = "No eres un caso. Eres familia." Use this hook in CTA only — do not sprinkle "como familia" through body copy or it becomes performative.
- **Anti-insurance framing is identical to English.** Voice Rule 6 applies fully in Spanish. The "aseguranza" is always the opponent. Frame it that way every time.
- **No religious appeals.** The audience may be Catholic, evangelical, secular — don't assume. The Voice Guide explicitly avoids religious framing in body copy.
- **Avoid sentimentality.** The persona is dealing with a real injury and real bills. Warm, direct, respectful — not weepy. Jim's voice = a friend who happens to be a lawyer, not a priest or a counselor.

---

## hreflang setup (critical for ES-EN SEO)

Every Spanish page needs a reciprocal hreflang block in the WordPress page `<head>`. This signals to Google that the ES and EN pages are translations of each other (not duplicate content), which preserves ranking for both. The same block must also be added to the EN page pointing at its ES sibling — that part is handled by the publisher, but flag it back to them so they don't miss it.

### Template — paste this in WordPress page head for every Spanish FAQ page

```html
<!-- hreflang for ES FAQ page — replace SLUGS with each page's actual slugs -->
<link rel="alternate" hreflang="en-us" href="https://gofflawdfw.com/faq/[EN-SLUG-HERE]/" />
<link rel="alternate" hreflang="es-us" href="https://gofflawdfw.com/es/faq/[ES-SLUG-HERE]/" />
<link rel="alternate" hreflang="x-default" href="https://gofflawdfw.com/faq/[EN-SLUG-HERE]/" />
```

### Hand to the publisher with this note

> "These hreflang tags must appear in the `<head>` of BOTH the Spanish page AND the matching English page — not just the Spanish one. The `x-default` always points to the English version (Google convention for US-market multilingual sites where English is the primary language). After publish, run a crawl with Screaming Frog or Sitebulb and verify reciprocal hreflang on every pair — broken hreflang silently hurts both versions."

Each page-by-page spec below lists the exact EN-SLUG and ES-SLUG to use.

---

## If Dianne doesn't write fluent Spanish

If you do not write fluent Mexican-Spanish yourself, you **must** partner with a native Mexican-Spanish reviewer/translator before any of these pages publishes. Here's what to flag:

### Why this matters specifically

The drafts in `faq-drafts-spanish/` are AI-generated. They are competent but have audible accuracy issues a native Mexican speaker will catch immediately. Common AI-Spanish failure modes to watch for:

- **Wrong dialect drift.** AI often defaults to a Spain-influenced or "neutral LatAm" register that reads as foreign or stiff to DFW Mexican-American readers. Example: "coche" instead of "carro/auto"; "vosotros" instead of "ustedes"; "ordenador" instead of "computadora."
- **Backtranslation tells.** Phrases like "abogado de personalidad lesiones" (calque of "personal injury lawyer" word-for-word) instead of "abogado de lesiones personales." Any time a phrase reads like English-arranged-into-Spanish, flag it.
- **Mistranslated legal terms.** "Liability" → "responsabilidad" is correct; "liability insurance" → "seguro de responsabilidad civil" is correct. But AI sometimes outputs "seguro de fiabilidad" (wrong — that means "reliability insurance"). Statute names, "premises liability," "subrogation," "non-subscriber" — verify every one.
- **Gender agreement errors at scale.** "La abogada" vs "el abogado" (Jim is male — use "el abogado" / "abogado" only). "La aseguranza" (feminine) → "la aseguranza es responsable" (correct). AI can flip these mid-paragraph.
- **Overformal register.** The drafts sometimes slip into Castilian formality ("conviene que usted considere..."). Mexican DFW working-class register is direct, not flowery. The native reviewer should be allowed to ruthlessly shorten.

### Recommended workflow

1. **You** edit the AI draft for SEO, voice, structure, and brand architecture against this brief.
2. **Native Mexican-Spanish reviewer** (ideally a DFW-based Spanish speaker, second-best a Mexico City editor familiar with US legal Spanish) does a vocabulary + register pass. Pay for this — do not crowdsource to a friend who "speaks Spanish."
3. **You** integrate reviewer edits, push to staging.
4. **Native reviewer** does a second pass on the staged page (reads it with formatting + CTA in context).
5. **Publish.**

If you do write fluent Mexican-Spanish yourself: still get a second-set-of-eyes pass before publish. Even native writers benefit from a peer review on legal content.

### Recommended sourcing

For a paid native reviewer in DFW: post on Bilingual Source DFW, AILA Texas chapter, or LinkedIn for "DFW Spanish-English legal content reviewer." Budget $50-$100 per page for review pass (8 pages = $400-$800 one-time spend). Cheaper than republishing later.

---

## Universal Spanish CTA module template

Paste this at the bottom of every Spanish FAQ page, just before the Recursos Relacionados block. Token `{{CTA_PHONE}}` is replaced at publish time.

```markdown
---

## Obtenga Ayuda Hoy

¿Lastimado en un accidente? **Llame a Goff. Cobre lo suyo.** No eres un caso — eres familia.

**Sin ganar, sin pagar.** Consulta gratis, disponible las 24 horas. Hablamos español. Su estatus no importa — no preguntamos.

**Llame a Jim ahora: {{CTA_PHONE}}**

[Botón: Revisión Gratuita de Mi Caso →]

---
```

### Variant for the wrongful-death-adjacent S03 (plazo de prescripción) — softer register when discussing deceased family

For pages that touch wrongful death or family fatality (S03 specifically references muerte injusta in the body), use this softer CTA opener — same brand architecture, less direct opening line:

```markdown
---

## Obtenga Ayuda Hoy

Si usted o un ser querido resultó lesionado o falleció en un accidente en Texas, **no espere.** **Sin ganar, sin pagar.** Consulta gratis, disponible las 24 horas. Hablamos español. Su estatus no importa — no preguntamos.

**Llame a Jim: {{CTA_PHONE}}**

[Botón: Revisión Gratuita de Mi Caso →]

---
```

---

## The 8 pages — universal structure (every page)

| Section | Word count | Notes |
|---|---|---|
| YAML frontmatter | — | Already present in existing drafts; preserve and update only `updated_date` if you revise after 2026-05-16 |
| H1 | — | In Spanish; target keyword natural placement |
| Byline | 1 line | "Por [Jim Goff](/attorneys/jim-goff/) \| Actualizado el 16 de mayo de 2026" |
| Lead paragraph | 80-130 words | Address reader directly using "usted." Include target keyword in first 100 words. Set the answer immediately — Hispanic users disproportionately want the answer at the top of the page (Section 3 of keyword research confirms FAQ snippet capture is easier in Spanish DFW SERPs than English). |
| H2 body sections | 5-8 per page | Each H2 is a question or claim. Each section 150-300 words. Match the existing draft's H2 structure as your starting point, but pressure-test every header against the Voice Guide — if it reads as lawyer-speak, rewrite it. |
| Statute citation block | — | Cite Texas statute in English with Spanish translation context. Pattern: *"El Código de Práctica Civil y Recursos de Texas, sección 16.003 (Texas Civil Practice and Remedies Code § 16.003), establece que..."* |
| Cultural callout (where applicable) | 50-100 words | Immigration status callout on S01, S05, S07, S08. Cost / "no tengo dinero" callout on S04 and S05. |
| CTA module | — | Universal Spanish CTA above. `{{CTA_PHONE}}` token. |
| Recursos Relacionados block | 4-5 links | Spanish hub + 2 Spanish FAQ siblings + EN hreflang sibling. Specific per page below. |
| Schema JSON-LD | — | FAQPage with `"inLanguage": "es-US"` + LegalService with same. Preserve from existing drafts; update only if you change H2 questions. |
| hreflang block | — | Per the template above. Specific URLs per page below. |

**Word count target per page: 1,200-1,500.** Spanish runs ~15% longer than English for the same content, so the EN target of 1,000-1,300 maps to ES 1,200-1,500.

---

## Page-by-page spec (8 pages)

Prioritization order (volume × strategic value):
1. **S01** — qué hacer después de un accidente (480/mo, highest volume Spanish FAQ in DFW)
2. **S03** — plazo de prescripción (320/mo)
3. **S02** — cuánto vale mi caso (260/mo)
4. **S04** — cuánto cobra un abogado (160/mo)
5. **S05** — debo contratar un abogado (150/mo)
6. **S06** — debo aceptar primera oferta (130/mo)
7. **S08** — quién paga las facturas médicas (110/mo)
8. **S07** — lesionado en el trabajo (85/mo)

---

### Page S01 — Qué Hacer Después de un Accidente de Auto en Texas

- **Target keyword (Spanish):** qué hacer después de un accidente de auto en texas
- **Est. monthly volume:** 480 *(directional — verify in Ahrefs Lite per Spanish keyword research methodology note)*
- **Competition:** Low-Medium (highest-volume FAQ in the Spanish DFW dataset)
- **Suggested H1:** **Qué Hacer Después de un Accidente de Auto en Texas: Guía Paso a Paso**
- **URL slug:** `/es/faq/que-hacer-despues-de-un-accidente-de-auto-en-texas/`
- **Word count target:** 1,300-1,500
- **English equivalent (hreflang pair):** `/faq/what-to-do-after-car-accident-in-texas/` — file: `page-01-what-to-do-after-car-accident-texas.md`
- **Audience profile:** DFW Hispanic working-class driver who has just been in a crash (or whose family member has) — searching from a phone, often in the hours after the wreck. Per the Voice Guide persona: "Pleasant Grove mom rear-ended on I-45."
- **Must-cite legal references:**
  - Texas Transportation Code § 550.022 (Texas Transportation Code § 550.022) — duty to move vehicles when safe
  - CR-3 form (Texas Peace Officer's Crash Report) — TxDOT 10-day filing rule, $6-$8 cost via TxDOT portal
  - Note: no statute-of-limitations deep-dive here; cross-link to S03 for that
- **Key facts Dianne must include:**
  - 911 call requirement when injuries/significant damage
  - Don't admit fault, don't apologize, don't say "I'm fine" (adrenaline masks injury for hours-to-days)
  - 8-photo checklist (preserve from existing draft — well-structured)
  - 72-hour medical window with both medical and legal reasoning
  - 24-48 hour insurance notice (only your own insurer; never give recorded statement to the OTHER driver's insurer)
  - Don't sign any medical authorization for full medical history
  - Hit-and-run: police report still possible at station; preserves rights
- **Suggested H2 outline (preserve from existing draft — strong structure):**
  - Paso 1: Asegúrese de que todos estén a salvo y llame al 911
  - Paso 2: Qué decir (y qué NO decir) al otro conductor
  - Paso 3: Reglas para reportar el choque en Texas — cuándo se requiere el CR-3
  - Paso 4: Tome fotos de todo — la lista de 8 fotos
  - Paso 5: Reciba atención médica dentro de las 72 horas (por qué esto importa para su caso)
  - Paso 6: Avise a su aseguranza — qué decir en las primeras 48 horas
  - Paso 7: Cuándo llamar a un abogado de lesiones personales en Texas (y por qué esperar le perjudica)
- **Hispanic-specific concerns to address on this page:**
  - **Immigration status callout** (Paso 7 or new standalone block): *"Su estatus migratorio NO afecta su derecho a recibir compensación bajo la ley de Texas."* This page captures top-of-funnel Hispanic users who don't yet know they're allowed to call.
  - Working-class cost concern (brief mention in Paso 7): contingency fee explained in plain Spanish — "Llamar al abogado es gratis. Contratarlo también es gratis."
- **Cross-link assignments (Recursos Relacionados block):**
  1. Spanish hub: `/es/areas-de-practica/accidentes-de-auto/`
  2. Spanish FAQ sibling: `/es/faq/cuanto-vale-mi-caso-de-lesiones-personales-texas/` (natural next question)
  3. Spanish FAQ sibling: `/es/faq/plazo-prescripcion-lesiones-personales-texas/` (urgency reinforcement)
  4. EN hreflang pair: `/faq/what-to-do-after-car-accident-in-texas/`
- **Tone notes:** This is the top-of-funnel page — first impression for many Hispanic DFW visitors. Open with the Voice Guide intro pattern: address the reader directly, "Si lo acaban de chocar en la I-35, en la I-635 o en cualquier intersección del Metroplex..." Specific roads + DFW geography signals you know the area (Voice Guide visual voice principle).

---

### Page S02 — Cuánto Vale Mi Caso de Lesiones Personales en Texas

- **Target keyword (Spanish):** cuánto vale mi caso de lesiones personales
- **Est. monthly volume:** 260 *(directional)*
- **Competition:** Low
- **Suggested H1:** **Cuánto Vale Mi Caso de Lesiones Personales en Texas**
- **URL slug:** `/es/faq/cuanto-vale-mi-caso-de-lesiones-personales-texas/`
- **Word count target:** 1,200-1,500
- **English equivalent (hreflang pair):** `/faq/how-much-is-my-personal-injury-case-worth/` — file: `page-02-how-much-is-my-personal-injury-case-worth.md`
- **Audience profile:** DFW Hispanic user with an active injury, post-treatment-start, considering whether to settle or hire counsel. Bottom-of-funnel disguised as TOFU per keyword research note.
- **Must-cite legal references:**
  - $250,000 cap on non-economic damages — **applies only to medical malpractice**, NOT to motor vehicle / truck / Uber/Lyft / wrongful death / mass tort cases (Texas Civil Practice and Remedies Code Chapter 74)
  - Texas exemplary damages cap: greater of $200,000, or 2× economic damages plus equal-to non-economic up to $750,000 (Texas Civil Practice and Remedies Code § 41.008)
  - Insurance Research Council statistic: represented claimants recover ~3.5× more than unrepresented (cite IRC by name)
- **Key facts Dianne must include:**
  - The 6 factors (severity, medical bills past+future, lost income, liability clarity, policy limits, county jury patterns)
  - Distinction: economic damages (with receipts) vs non-economic damages (pain/suffering) vs punitive damages
  - Multiplier method explanation with worked example ($40K × 3 = $120K example)
  - Colossus software mention (insurance adjusters' internal valuation tool)
  - MMI (Maximum Medical Improvement) — explain term inline, use English acronym
  - **Critical correction to flag for review:** existing draft uses "compensación" in body — replace with "dinero" / "lo que le deben" per Voice Rule 7. Same for "víctima" → "persona lesionada" / "alguien lastimado."
- **Suggested H2 outline:**
  - La respuesta honesta: depende de estos 6 factores
  - Daños económicos: facturas médicas, salario perdido e ingresos futuros
  - Daños no económicos: dolor, sufrimiento y los límites en Texas
  - Daños punitivos — cuándo los permite Texas
  - Cómo calculan las aseguranzas las ofertas (el método del multiplicador)
  - Por qué las primeras ofertas casi siempre son demasiado bajas
  - Las 3 cosas que más aumentan el valor de un caso
- **Hispanic-specific concerns to address on this page:**
  - Mass tort framing matters here — Hispanic DFW women are a primary user base for hair-relaxer / Paragard (per Section 4 of keyword research). Mention that mass-tort cases are also uncapped on non-economic damages.
  - Confidence-building tone: Mexican working-class readers often undervalue their own cases. The "no cap on motor vehicle non-economic damages" message is the key correction.
- **Cross-link assignments:**
  1. Spanish hub: `/es/areas-de-practica/lesiones-personales/`
  2. Spanish FAQ sibling: `/es/faq/debo-aceptar-primera-oferta-aseguradora/` (companion settlement-decision question)
  3. Spanish FAQ sibling: `/es/faq/cuanto-cobra-un-abogado-de-lesiones-personales-texas/` (fee transparency — the natural follow-on concern)
  4. EN hreflang pair: `/faq/how-much-is-my-personal-injury-case-worth/`
- **Tone notes:** Honest, direct, no result promises (Voice Rule 8). Open with "depende" — but explain immediately WHY it depends. The reader is value-shopping; respect their intelligence by giving them the real framework.

---

### Page S03 — Plazo de Prescripción por Lesiones Personales en Texas

- **Target keyword (Spanish):** cuánto tiempo tengo para demandar en texas
- **Est. monthly volume:** 320 *(directional)*
- **Competition:** Low
- **Suggested H1:** **Cuánto Tiempo Tengo Para Presentar una Demanda por Lesiones en Texas**
- **URL slug:** `/es/faq/plazo-prescripcion-lesiones-personales-texas/`
- **Word count target:** 1,200-1,500
- **English equivalent (hreflang pair):** `/faq/personal-injury-statute-of-limitations-texas/` — file: `page-03-personal-injury-statute-of-limitations-texas.md`
- **Audience profile:** DFW Hispanic user with a past injury (weeks to months out), wondering if it's "too late." High urgency intent — every visitor to this page is making a time-sensitive decision.
- **Must-cite legal references:**
  - **Texas Civil Practice and Remedies Code § 16.003** — the 2-year rule (cite in English, with Spanish gloss: "Código de Práctica Civil y Recursos de Texas, sección 16.003")
  - **Texas Tort Claims Act** — 6-month notice rule for government entities
  - **City of Dallas / City of Fort Worth** — 90-day local ordinance shorter notice
  - Minor tolling rule (paused until age 18, then 2 years runs)
  - Discovery rule for mass torts (malla de hernia, alisadores, Paragard, AFFF)
  - Wrongful death — 2 years from DATE OF DEATH, not date of accident
- **Key facts Dianne must include:**
  - 2-year clock starts on the date of injury (or, for wrongful death, date of death)
  - Insurance negotiation does NOT pause the clock — this is the single most important point
  - Government cases: 6-month state notice + 90-day Dallas/FW ordinance
  - Discovery rule examples (mass torts where injury emerges years later)
  - Evidence loss timeline: traffic cam footage (7-30 days), business cam footage (7-90 days), trucker logbooks (federal 6-month retention), EDR data (lost when car destroyed)
- **Suggested H2 outline:**
  - La regla de los dos años: Código de Práctica Civil y Recursos de Texas, § 16.003
  - Cuándo empieza a correr el reloj de los dos años (y cuándo se pausa)
  - Excepciones: menores de edad, incapacidad mental y la regla del descubrimiento
  - Muerte injusta: los mismos 2 años, pero con fecha de inicio diferente
  - Demandas contra entidades del gobierno: la regla de los 6 meses (mucho más corta)
  - Por qué "voy a esperar a ver qué pasa" casi siempre sale mal
- **Hispanic-specific concerns to address on this page:**
  - DART bus + city vehicle accidents disproportionately affect DFW Hispanic working-class users (transit-dependent commuter base). Mention these specifically in the government-entity section.
  - The 6-month government notice rule is the single most-missed deadline by this audience because no one tells them about it. Lead with it where the government angle applies.
- **Cross-link assignments:**
  1. Spanish hub: `/es/areas-de-practica/muerte-injusta/` (S03 touches wrongful death; this is the most thematic hub link)
  2. Spanish FAQ sibling: `/es/faq/que-hacer-despues-de-un-accidente-de-auto-en-texas/` (preserves evidence early)
  3. Spanish FAQ sibling: `/es/faq/debo-contratar-abogado-de-lesiones-personales/` (calls the reader to action)
  4. EN hreflang pair: `/faq/personal-injury-statute-of-limitations-texas/`
- **Tone notes:** Use the softer CTA variant (above) — this page touches wrongful death. Urgency throughout but never alarmist. Pattern: "Aquí está el plazo. Aquí está la excepción. Aquí está por qué esperar le perjudica."

---

### Page S04 — Cuánto Cobra un Abogado de Lesiones Personales en Texas

- **Target keyword (Spanish):** cuánto cobra un abogado de lesiones personales texas
- **Est. monthly volume:** 160 *(directional)*
- **Competition:** Low
- **Suggested H1:** **Cuánto Cobra un Abogado de Lesiones Personales en Texas**
- **URL slug:** `/es/faq/cuanto-cobra-un-abogado-de-lesiones-personales-texas/`
- **Word count target:** 1,300-1,500 (heaviest financial-mechanics page; needs space)
- **English equivalent (hreflang pair):** `/faq/how-much-do-personal-injury-lawyers-charge-texas/` — file: `page-04-how-much-do-personal-injury-lawyers-charge-texas.md`
- **Audience profile:** DFW Hispanic user who has decided they probably need help but is blocked on cost. The #2 conversion blocker after immigration status. Frequently a researcher (spouse/relative) Googling on behalf of an injured family member.
- **Must-cite legal references:**
  - Texas contingent fee contract requirement: must be in writing and signed (Texas Disciplinary Rules of Professional Conduct 1.04 — but **do NOT cite the specific TDR; Jim handles compliance**; the requirement itself can be stated)
  - Standard Texas contingency scale: 33⅓% pre-suit / 40% post-suit / 45% post-appeal
  - Client retains settlement authority always (never the attorney's decision to accept/reject)
- **Key facts Dianne must include:**
  - $0 upfront, no hourly billing, no retainer — repeat this three times in different framings
  - The 33⅓ / 40 / 45 scale (most common; some firms differ — disclose)
  - **Case costs vs. attorney fees** — the critical distinction
  - **Net vs. gross fee model** — the question every client should ask before signing: "Are costs deducted before or after my fee is calculated?" Show worked example ($300K settlement, $30K costs, 40% fee — $108K vs $120K result, $12K swing)
  - The 7 contract items to verify before signing (percentage scale, costs handling, lien handling, termination clause, referral fees, settlement authority)
  - Why "cheap" lawyers usually cost more (a 25% lawyer on a $100K case = $75K to client; a 40% lawyer on the same case settled for $250K = $150K to client)
  - Reflect IRC data point already in S05: represented claimants ~3.5× more
- **Suggested H2 outline:**
  - Pago por contingencia explicado: $0 por adelantado, se cobra solo si ganamos
  - La escala estándar de 33⅓% / 40% / 45% en Texas
  - Qué cubren los "gastos del caso" y quién los paga
  - El contrato de honorarios: qué leer antes de firmar
  - Cómo se calcula el honorario en un arreglo (settlement) vs. veredicto de jurado
  - Por qué los abogados "baratos" muchas veces salen más caros al final
  - Cuándo llamar a un abogado de lesiones personales en Texas
- **Hispanic-specific concerns to address on this page:**
  - **THIS IS THE COST-OBJECTION PAGE.** Open with the explicit reframe: *"Sé que mucha gente en nuestra comunidad piensa 'los abogados son carísimos, yo no puedo pagar eso.' Esa preocupación es válida en muchos tipos de derecho — divorcio, criminal, inmigración — donde se cobra por hora o se exige un retainer. Pero en lesiones personales, no es así."* (This wording is in the existing draft; keep it.)
  - Compare directly to other lawyer experiences Hispanic readers have likely had (immigration, divorce, criminal) — those required upfront money, this doesn't.
  - Conclude with the trust signal: "No nos pagan si no ganamos. Si usted nunca ha contratado a un abogado antes — sea por costumbre, por miedo, o porque pensaba que no podía — esta es la única área del derecho donde no hay ningún riesgo financiero por llamar."
- **Cross-link assignments:**
  1. Spanish hub: `/es/areas-de-practica/lesiones-personales/`
  2. Spanish FAQ sibling: `/es/faq/debo-contratar-abogado-de-lesiones-personales/` (the next question they'll ask)
  3. Spanish FAQ sibling: `/es/faq/cuanto-vale-mi-caso-de-lesiones-personales-texas/` (puts the fee in context vs. recovery)
  4. EN hreflang pair: `/faq/how-much-do-personal-injury-lawyers-charge-texas/`
- **Tone notes:** Heaviest "explainer" voice on the whole stack. Take the time to do the math out loud (worked examples). Plain numbers, real percentages. NO promises of recovery amounts. Voice Rule 8 enforcement on this page in particular — easy to slip into "we'll get you the most."

---

### Page S05 — ¿Debo Contratar un Abogado de Lesiones Personales?

- **Target keyword (Spanish):** debo contratar abogado de lesiones personales
- **Est. monthly volume:** 150 *(directional)*
- **Competition:** Low
- **Suggested H1:** **¿Debo Contratar un Abogado de Lesiones Personales? (Guía Honesta)**
- **URL slug:** `/es/faq/debo-contratar-abogado-de-lesiones-personales/`
- **Word count target:** 1,200-1,500
- **English equivalent (hreflang pair):** `/faq/should-i-hire-a-personal-injury-lawyer/` — file: `page-05-should-i-hire-a-personal-injury-lawyer.md`
- **Audience profile:** Mid-funnel — has been hurt, has been thinking about it for a few days to a few weeks, may already have an insurance offer in hand. Researching whether legal help is worth it.
- **Must-cite legal references:**
  - Insurance Research Council finding: represented claimants recover ~3× more than unrepresented (cite IRC by name as the source — neutral, industry-funded research)
  - UM/UIM coverage exists in Texas; insurer is your opponent once a claim is opened
  - Texas contingency fee structure (cross-references S04)
- **Key facts Dianne must include:**
  - **Cases where you probably DON'T need a lawyer** (counterintuitive but builds trust):
    - Minor bump, no injuries
    - Property damage only
    - Already paid fairly and offer covers everything
    - Total claim < $2,000-$3,000
  - **5 situations where you DO need a lawyer:**
    - Any ER visit, MRI/CT, follow-up treatment
    - Any lost work time
    - Other driver uninsured / underinsured / fled
    - Commercial vehicle / truck / Uber/Lyft
    - Insurer denying liability, blaming you, delaying payment
  - "No tengo dinero" myth — direct rebut with contingency explanation
  - IRC 3× recovery statistic (already in existing draft — keep)
  - 5 questions to ask in the free consultation
  - What adjusters won't tell you (4 points)
- **Suggested H2 outline:**
  - Cuándo probablemente NO necesita un abogado (y se lo diremos)
  - Las 5 situaciones donde SÍ necesita un abogado
  - "No tengo dinero para un abogado" — esta es la verdad
  - Los datos: las personas con abogado recuperan 3 veces más
  - Lo que los ajustadores de seguros NO le van a decir
  - Su estatus migratorio NO afecta su derecho a compensación
  - Qué buscar en un abogado de Texas (más allá de los anuncios)
  - Consultas gratis: qué preguntar en la primera llamada
- **Hispanic-specific concerns to address on this page:**
  - **Both barrier-concerns hit at full strength on this page** — immigration status AND cost. Each gets a dedicated H2 (not buried in body copy).
  - The "we will tell you when you DON'T need us" frame is particularly effective with Hispanic working-class readers who have been burned by salespeople and high-pressure tactics. Lean into it.
- **Cross-link assignments:**
  1. Spanish hub: `/es/areas-de-practica/lesiones-personales/`
  2. Spanish FAQ sibling: `/es/faq/cuanto-cobra-un-abogado-de-lesiones-personales-texas/` (cost concern reinforcement)
  3. Spanish FAQ sibling: `/es/faq/debo-aceptar-primera-oferta-aseguradora/` (the most common adjacent decision)
  4. EN hreflang pair: `/faq/should-i-hire-a-personal-injury-lawyer/`
- **Tone notes:** Honest mid-funnel page. Disclose what makes a case NOT viable. Treat the reader as a peer evaluating their options. The vibe is "trusted neighbor who happens to be a lawyer" — exactly the Voice Guide persona.

---

### Page S06 — ¿Debo Aceptar la Primera Oferta de la Aseguranza?

- **Target keyword (Spanish):** debo aceptar primera oferta de la aseguradora
- **Est. monthly volume:** 130 *(directional)*
- **Competition:** Low
- **Suggested H1:** **¿Debo Aceptar la Primera Oferta de la Aseguranza?**
- **URL slug:** `/es/faq/debo-aceptar-primera-oferta-aseguradora/`
- **Word count target:** 1,200-1,500
- **English equivalent (hreflang pair):** `/faq/should-i-accept-first-settlement-offer/` — file: `page-06-should-i-accept-first-settlement-offer.md`
- **Audience profile:** Active offer in hand, deciding NOW. Highest-intent decision page in the stack. Reader may sign within 24-48 hours of reading.
- **Must-cite legal references:**
  - "Full and Final Release of All Claims" — Texas courts enforce strictly; very narrow fraud exception
  - Maximum Medical Improvement (MMI) — define inline, use English acronym
  - Colossus (Allstate's valuation software) — mention as the industry tool; jury values typically 2-5× Colossus output
  - 95% of filed cases still settle (so "filing the suit" doesn't mean "going to trial")
  - Texas minimum bodily injury liability: $30K per person / $60K per accident
- **Key facts Dianne must include:**
  - The answer in 2 words: "Casi nunca."
  - Why first offers are designed low (anchoring + your treatment isn't done + future bills aren't on table + lost earning capacity ignored + adjuster software undervalues + financial pressure leverage)
  - What "Full and Final Release" forfeits (medical past+future, lost wages past+future, pain+suffering, later-discovered disability, often related parties)
  - 4 questions to answer before signing (MMI reached? all damage categories covered? subrogation/liens subtracted? second opinion gotten?)
  - Settlement negotiation rhythm: 3-6 rounds typical (demand → first offer 25-40% → counter → second offer 50-65% → continued negotiation → resolution or suit)
  - Movable vs. genuinely-low offers (when low IS the realistic ceiling vs. when low is anchoring)
- **Suggested H2 outline:**
  - La respuesta corta: casi nunca
  - Por qué la primera oferta está diseñada para ser baja
  - Qué significa "liberación completa y final" (y por qué es permanente)
  - Las 4 preguntas que debe hacer antes de aceptar cualquier oferta
  - Cómo funcionan realmente las contra-ofertas en casos de Texas
  - Cuándo una oferta baja puede subir — y cuándo no
- **Hispanic-specific concerns to address on this page:**
  - Financial pressure framing — Hispanic working-class readers often face genuine, urgent bills (medical, rent, lost wages). Acknowledge this rather than dismiss it: "Sabemos que las facturas no esperan. Pero firmar es para siempre."
  - "Permanent" framing translated for cultural emphasis: *"En cuanto usted firma, el caso se acaba. Permanentemente. No hay regreso."*
- **Cross-link assignments:**
  1. Spanish hub: `/es/areas-de-practica/lesiones-personales/`
  2. Spanish FAQ sibling: `/es/faq/cuanto-vale-mi-caso-de-lesiones-personales-texas/` (companion: what should the offer be?)
  3. Spanish FAQ sibling: `/es/faq/debo-contratar-abogado-de-lesiones-personales/` (the next decision)
  4. EN hreflang pair: `/faq/should-i-accept-first-settlement-offer/`
- **Tone notes:** Urgent but not panicky. The reader is in decision mode — be the calm friend who says "wait, let me show you what you're about to sign." Voice Rule 5: short sentences win on this page especially.

---

### Page S07 — Lesionado en el Trabajo en Texas (Reclamo de Tercero)

- **Target keyword (Spanish):** qué hacer si me lesiono en el trabajo en texas
- **Est. monthly volume:** 85 *(directional)*
- **Competition:** Low
- **Suggested H1:** **Qué Hacer Si Me Lesiono en el Trabajo en Texas (Cuando NO Es Compensación Laboral)**
- **URL slug:** `/es/faq/lesionado-en-el-trabajo-texas-reclamo-tercero/`
- **Word count target:** 1,300-1,500 (complex topic; needs the room)
- **English equivalent (hreflang pair):** `/faq/injured-at-work-texas-third-party-claim/` — file: `page-07-injured-at-work-texas-third-party-claim.md`
- **Audience profile:** DFW Hispanic worker (or worker's family member) who was hurt on the job — frequently construction, oilfield service, warehouse, delivery driver, gig contractor. The persona overlaps heavily with high-Hispanic-density employers like roofing, framing, restaurant kitchen, Amazon DSP.
- **Must-cite legal references:**
  - **Texas Labor Code § 406.033** — non-subscriber defense forfeiture (contributory negligence, assumption of risk, fellow-servant doctrine all unavailable)
  - **Texas Labor Code § 408.001(b)** — gross negligence exemplary damages for wrongful death even when employer carries workers' comp
  - **Texas Labor Code § 409.001** — 30-day notice to employer to preserve workers' comp benefits
  - **Texas Civil Practice and Remedies Code § 16.003** — 2-year statute of limitations on the negligence claim
  - Texas Department of Insurance, Division of Workers' Compensation database at tdi.texas.gov — public lookup for subscriber/non-subscriber status
  - ~28% of Texas employers are non-subscribers (TDI data point — use exactly this)
- **Key facts Dianne must include:**
  - **Critical disclaimer at top of page:** Goff Law does NOT handle pure workers' comp cases. If it's pure WC, refer to a WC specialist at no cost. This page is for the cases that are NOT pure WC.
  - 4 situations where you can sue outside of comp:
    1. Employer is non-subscriber
    2. A third party caused the injury (other driver, defective equipment, separate subcontractor, negligent property owner)
    3. You're a 1099 contractor (comp often doesn't apply at all)
    4. Gross negligence resulting in death (exemplary damages)
  - Why third-party recoveries are usually multiple times larger than what comp would pay (full pain+suffering, full lost earning capacity, full mental anguish, exemplary in some cases)
  - The damages comparison table (existing draft has a good one — preserve)
  - 1099 misclassification is common — and the worker may actually be an employee with full rights
  - Hold-harmless clauses in 1099 contracts often unenforceable for gross negligence
  - The 30-day notice trap: report to employer in writing within 30 days even if pursuing third-party, just to preserve all options
- **Suggested H2 outline:**
  - Su estatus migratorio NO afecta su derecho a compensación *(lead with this — most important to this audience)*
  - Cuándo puede demandar más allá de la comp laboral en Texas
  - La excepción del empleador "no suscriptor" (Texas es único)
  - Reclamos por negligencia de un tercero: cuando alguien más causó su lesión
  - Lesiones de contratistas 1099 — la comp laboral puede no aplicar en absoluto
  - Cómo los daños se diferencian de la comp laboral (sin límite en dolor y sufrimiento)
  - El plazo de 2 años y la trampa de los 30 días para avisar al empleador
- **Hispanic-specific concerns to address on this page:**
  - **Immigration status is the lead H2 on this page** — work-injury Hispanic visitors carry the highest deportation fear of any FAQ audience. Front-load the reassurance.
  - Acknowledge industries with high DFW Hispanic concentration in the third-party section: construction, oilfield, warehouses, delivery. Use those examples specifically.
  - The "you might be misclassified as 1099 when you're actually an employee" callout matters — many DFW Hispanic workers are pushed into 1099 status illegally by small employers.
- **Cross-link assignments:**
  1. Spanish hub: `/es/areas-de-practica/lesiones-personales/`
  2. Spanish FAQ sibling: `/es/faq/debo-contratar-abogado-de-lesiones-personales/` (decision support)
  3. Spanish FAQ sibling: `/es/faq/quien-paga-facturas-medicas-accidente-auto-texas/` (medical-bill anxiety overlap)
  4. EN hreflang pair: `/faq/injured-at-work-texas-third-party-claim/`
- **Tone notes:** Educational, calm, anti-fear. The reader is afraid of two things: (1) getting deported for asserting rights, (2) losing their job for asserting rights. Neither fear is the reality under Texas law. Address both head-on. Use the disclaimer-at-top blockquote pattern from the existing draft — it builds trust by being explicit about what Goff DOES and DOESN'T do.

---

### Page S08 — ¿Quién Paga las Facturas Médicas Después de un Accidente?

- **Target keyword (Spanish):** quién paga las facturas médicas después de un accidente
- **Est. monthly volume:** 110 *(directional)*
- **Competition:** Low
- **Suggested H1:** **¿Quién Paga las Facturas Médicas Después de un Accidente de Auto en Texas?**
- **URL slug:** `/es/faq/quien-paga-facturas-medicas-accidente-auto-texas/`
- **Word count target:** 1,300-1,500 (heavy mechanics page like S04)
- **English equivalent (hreflang pair):** `/faq/who-pays-medical-bills-after-car-accident-texas/` — file: `page-08-who-pays-medical-bills-after-car-accident-texas.md`
- **Audience profile:** DFW Hispanic user 1-30 days post-accident, with medical bills starting to arrive. The reader is anxious and confused — many in this demo have limited or no health insurance.
- **Must-cite legal references:**
  - **Texas Insurance Code § 1952.152** — PIP minimum $2,500, requires written rejection to waive
  - Texas minimum bodily injury liability: $30K per person / $60K per accident
  - UM/UIM (Uninsured / Underinsured Motorist) — must be offered by Texas insurers; requires written rejection to waive
  - ERISA self-funded plan subrogation (strongest type) vs. Texas-insured plans (made-whole doctrine protection) vs. Medicare/Medicaid federal liens
  - ~20% of Texas drivers uninsured (TDI estimate; treat as directional)
- **Key facts Dianne must include:**
  - **The core truth lead:** in Texas, you pay first and get reimbursed later — the at-fault insurer doesn't cut checks during treatment.
  - PIP coverage: $2,500 minimum by default; opt-out requires written rejection; no-fault; covers medical bills + lost wages + replacement services
  - MedPay vs PIP: MedPay is medical-only, often higher limits, no written rejection needed
  - Health insurance subrogation — typical 30-50% reduction available through good legal negotiation
  - At-fault driver's insurance pays at the END of the case (6-18 months typical), not during
  - UM/UIM is the most important coverage on YOUR own policy for serious crashes — $100K UM/UIM costs $10-$30/month in DFW
  - **Letter of Protection (LOP)** — the critical mechanism for Hispanic uninsured readers: lets you get treatment with $0 upfront because the attorney promises payment from settlement. Explain this in plain Spanish.
- **Suggested H2 outline:**
  - Respuesta corta: usted paga primero, después le reembolsan
  - Cobertura PIP: el mínimo de $2,500 en Texas + cómo opt-out
  - MedPay vs. PIP: cuál es la diferencia
  - Seguro médico: derechos de subrogación y lo que se llevan de regreso
  - El seguro del conductor responsable: cuándo (y cómo) pagan
  - ¿Qué pasa si el otro conductor no tiene seguro? Cobertura UM/UIM
  - Cartas de protección: cómo los abogados consiguen tratamiento sin costo por adelantado
- **Hispanic-specific concerns to address on this page:**
  - **Heaviest "no health insurance" demographic concern across the 8 pages.** The Letter of Protection (Carta de Protección) section is the single most valuable callout for this audience. Pull it forward; don't bury it.
  - Specific framing: *"Esto es particularmente importante para los pacientes hispanos sin seguro o con seguro limitado en DFW. Si usted no tiene Blue Cross, no tiene Medicare, y no califica para Medicaid — pero necesita una resonancia magnética y posiblemente cirugía — la Carta de Protección es muchas veces el único camino real al tratamiento que necesita sin endeudarse antes de que su caso se resuelva."*
  - Don't moralize about the insurance gap. Just provide the solution.
- **Cross-link assignments:**
  1. Spanish hub: `/es/areas-de-practica/lesiones-personales/`
  2. Spanish FAQ sibling: `/es/faq/debo-contratar-abogado-de-lesiones-personales/` (next decision)
  3. Spanish FAQ sibling: `/es/faq/cuanto-vale-mi-caso-de-lesiones-personales-texas/` (case-value education for context)
  4. EN hreflang pair: `/faq/who-pays-medical-bills-after-car-accident-texas/`
- **Tone notes:** Educational + practical. The reader is opening bills as they read this. Lead with the answer (you pay first), then walk through every layer of coverage they might have. The Letter of Protection section is the most important paragraph in the entire 8-page stack for the uninsured Hispanic audience — make it sing.

---

## Things to AVOID across all 8 pages

- **NO competitor names.** Reyes, McCraw, Mullen, Witherite, Aldous, Snellings, Hamilton Wingo — not mentioned in any form. Differentiate by Goff positives.
- **NO result promises.** Voice Rule 8. "Maximum recovery," "we'll get you the most money," "guaranteed settlement" — banned.
- **NO "best / top-rated / premier / elite / experienced / aggressive"** language in EN or ES. Per Voice Rule 10: specifics over adjectives.
- **NO excluded case types** as recommended legal pathways: medical malpractice, nursing home, dog bite, generic slip-and-fall, pure workers' comp, SSDI, defamation, birth injury. Disclaim them where relevant (S07 has the cleanest example).
- **NO "compensación" as a primary word for money.** Use "dinero" or "lo que le deben" per Voice Rule 7. Exception: "compensación" appears once each on S05 and S07 where it directly answers a high-volume Spanish query ("derecho a recibir compensación") — that's intentional SEO-anchored use. Keep that single use; replace any others with "dinero."
- **NO "víctima" / "víctima de negligencia."** Use "persona lesionada" / "alguien que se lastimó" / "lo lastimaron."
- **NO "tú" form.** Always "usted."
- **NO translation of Texas statute numbers.** Always cite in English: "Texas Civil Practice and Remedies Code § 16.003."
- **NO machine-translated Spanish without native review.** See "If Dianne doesn't write fluent Spanish" section.
- **NO assumption that all Hispanic readers are immigrants.** Many readers are 2nd/3rd-gen US-born Tejanos. Avoid "como inmigrante" framing.

---

## Universal excluded-case disclaimer (adapt per page where applicable)

For any page where it makes sense to clarify what Goff doesn't take (S05 and S07 are the natural fits), use this Spanish version of the standard disclaimer:

> Jim maneja accidentes de carro, choques de camión y 18 ruedas, accidentes de motocicleta, choques de Uber y Lyft, y casos de muerte injusta. También representa a personas lesionadas por medicamentos defectuosos y dispositivos médicos en demandas masivas federales (mass torts).
>
> **Lo que NO manejamos:** compensación laboral pura, la mayoría de casos de mala práctica médica, casos de hogares de ancianos, mordeduras de perro, caídas comunes sin culpa clara, discapacidad del Seguro Social, y casos de difamación. Si su caso es uno de esos, lo referiremos con un abogado de confianza que sí los maneje. No tomamos casos que no podemos pelear de verdad.

---

## Final checklist before you mark a page "done"

For each of the 8 pages:

- [ ] H1 contains target keyword (natural reading, not awkward calque)
- [ ] Target keyword appears in first 100 words of body
- [ ] Lead paragraph addresses reader directly using "usted"
- [ ] Mexican Spanish vocabulary verified against the table above (carro/auto, aseguranza, choque, demandar, lesiones personales, indocumentado, dinero-not-compensación, etc.)
- [ ] Texas statutes cited in English with Spanish gloss
- [ ] Cultural callout present where applicable (immigration status on S01/S05/S07/S08; cost on S04/S05; LOP on S08; deportation fear on S07)
- [ ] Voice Guide rules followed — no banned words, "you" not "the client," Jim named, insurance framed as opponent
- [ ] Word count 1,200-1,500
- [ ] Universal Spanish CTA module included with `{{CTA_PHONE}}` token
- [ ] Recursos Relacionados block links to: 1 ES hub + 2 ES FAQ siblings + 1 EN hreflang sibling (URLs per page above)
- [ ] hreflang block included in page head with correct EN-SLUG + ES-SLUG + x-default pointing to EN
- [ ] FAQPage JSON-LD with `"inLanguage": "es-US"` (preserve from existing drafts; update if H2s changed)
- [ ] LegalService JSON-LD with `"inLanguage": "es-US"` + `"availableLanguage": ["en", "es"]`
- [ ] Native Mexican-Spanish reviewer pass completed (or self-confirm if you write fluently)
- [ ] No competitor names anywhere
- [ ] No result promises anywhere
- [ ] Excluded case types disclaimed where applicable (S05, S07)
- [ ] Saved to `recon/goff-law/faq-drafts-spanish-v2/<slug>.md`

---

## Questions? Stuck?

Anything ambiguous about voice, vocabulary, or specific cultural framing — flag back to Jim before drafting. Better to ask than to ship a page that needs a full rewrite.

Estimated time per page: 2-3 hours including native-speaker review pass. 8 pages × 2.5 hrs avg = ~20 hours total writer time + ~$400-$800 budget for native-speaker review.

Recommended publish strategy: publish all 8 together to avoid related-link 404s, AND coordinate with the EN-side publisher so the hreflang reciprocal links go live on the EN pages on the same day. A one-sided hreflang block hurts both pages until the second side ships.

---

## Brand voice quick-reference (Spanish — pin this above your monitor)

| Concept | Spanish (use this) |
|---|---|
| Primary tagline | **Llame a Goff. Cobre lo suyo.** |
| Secondary | **No eres un caso. Eres familia.** |
| Cost reassurance | **Sin ganar, sin pagar.** |
| Phone reassurance | **Contestamos el teléfono.** |
| Status reassurance | **Su estatus no importa. No preguntamos.** |
| Spanish service | **Hablamos español. Jim contesta su llamada en español si lo prefiere.** |

If a paragraph could be confused with something written by a generic immigration/divorce attorney, rewrite it. If it sounds like Jim — someone who lives in DFW, who knows the streets, who isn't going to make the reader feel small — it passes.
