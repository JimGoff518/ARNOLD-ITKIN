# Paragard Pages — Dev Team Deployment Package

**Project:** Replicate Galaxy Gas template across Paragard mass tort (5 city-targeted pages including Spanish)
**Approved by:** Jim Goff 2026-05-16
**Estimated dev time:** 5-7 hours total (~1-1.5 hrs per page)
**Strategic rationale:** Project #3 in the niche mass tort replication sequence. Paragard MDL 2974 has 3,984 cases pending, $40K-$400K+ projected per case. **UNCONTESTED in DFW** — 0 of 25 reconned competitors have any Paragard-specific landing pages. Spanish page targets Latina niche where 0 competitors compete.

⚠️ **Honest context:** First bellwether trial ended in defense verdict (January 2026). Settlement landscape has shifted. All 5 pages reflect this transparently — Goff is positioning as the "honest about the litigation state" firm to differentiate from mass-tort marketing firms that promise oversimplified outcomes.

---

## What's being deployed

| # | URL slug | Target audience |
|---|---|---|
| 1 | `/dallas-paragard-lawyer/` | Dallas-area women + Parkland/UT Southwestern/Methodist patients |
| 2 | `/houston-paragard-lawyer/` | Houston-area women + Texas Medical Center, Houston Methodist, Memorial Hermann patients |
| 3 | `/texas-paragard-iud-lawyer/` | Statewide; military spouses (Fort Cavazos, JBSA), rural Texas, smaller metros |
| 4 | `/north-texas-paragard-lawyer/` | DFW suburbs — Plano, Frisco, Allen, McKinney, Arlington, Garland, Cedar Hill |
| 5 | `/abogada-paragard-texas/` | **Spanish-language — UNCONTESTED Latina niche** |

---

## Files in this package

| File | Purpose |
|---|---|
| `01-dallas-paragard-lawyer.md` | Dallas page — full content, meta, FAQ, internal linking |
| `02-houston-paragard-lawyer.md` | Houston page |
| `03-texas-paragard-iud-lawyer.md` | Statewide page (military spouse + rural focus) |
| `04-north-texas-paragard-lawyer.md` | DFW suburbs page |
| `05-abogada-paragard-texas.md` | Spanish-language page (uncontested Latina niche) |
| `SCHEMA-JSON-LD.md` | 10 schema blocks (FAQPage + LegalService for each page) |
| `DEPLOYMENT-PACKAGE.md` | This file |

---

## Step-by-step deployment instructions

Same as AFFF + Hair Relaxer deployment packages. For each page:

1. **WordPress page creation** — title from H1, slug from URL header
2. **Body content paste** — copy from `## PAGE BODY` through FAQ block
3. **Yoast SEO meta config** — SEO title, meta description, focus keyword from `## METADATA` section
4. **JSON-LD schema injection** — copy both schema blocks from `SCHEMA-JSON-LD.md` into Yoast Schema tab OR Custom HTML block OR theme's custom-code feature; validate with https://search.google.com/test/rich-results
5. **For the Spanish page** — set page language to `es` and add hreflang declarations linking to/from the English `/texas-paragard-iud-lawyer/` page
6. **Publish + clear cache + verify mobile + verify URL loads + verify rich results validate**

---

## Verification checklist (after all 5 pages live)

- [ ] All 5 URLs load
- [ ] H1, meta, FAQ blocks visible on each
- [ ] Phone 972-928-0085 visible above the fold on each page
- [ ] JSON-LD schema validates for each page (Rich Results Test)
- [ ] Spanish page renders correctly with hreflang in `<head>`
- [ ] Internal links between all 5 pages work
- [ ] Internal links to Hair Relaxer + AFFF + Galaxy Gas pages work (cross-mass-tort linking)
- [ ] Mobile rendering clean
- [ ] PageSpeed no regression

---

## Cross-linking from existing pages (after deploy)

| Existing page | Add link to |
|---|---|
| Homepage | Add "Paragard IUD Lawsuits" to Practice Areas menu → `/dallas-paragard-lawyer/` |
| Existing Dallas hair relaxer page (`/dallas/hair-relaxers/`) | Add "Related Mass Torts" section → all 5 Paragard pages |
| Houston Hair Relaxer (when deployed) | Add "Related Mass Torts" → `/houston-paragard-lawyer/` |
| Spanish Hair Relaxer (when deployed) | Add "Casos Relacionados" → `/abogada-paragard-texas/` |
| Product Liability page | Reference Paragard as current medical device mass tort |
| Catastrophic Injury page | Reference Paragard severe complications cases |
| Wrongful Death page | Reference Paragard wrongful death claims (rare but possible) |
| Galaxy Gas page | "Related Mass Torts" → Paragard |
| AFFF pages (when deployed) | "Related Mass Torts" → Paragard |

---

## What this deployment ACCOMPLISHES strategically

| Goal | Mechanism |
|---|---|
| **Pure greenfield SERP territory** | 0 of 25 reconned DFW competitors have any Paragard-specific landing pages |
| **Revenue defense post-Aldous referral loss** | Paragard cases project $40K-$400K+ per case |
| **Federal preemption (Texas tort caps don't apply)** | MDL 2974 is federal |
| **AI Overview / featured snippet eligibility** | FAQ schema on all 5 pages |
| **No PPC required** | Pure organic SEO; aligns with locked strategy |
| **Spanish niche entry — UNCONTESTED** | Same play that worked for hair relaxer |
| **Women's health mass tort cluster** | Combines with hair relaxer for unified women's mass tort positioning |
| **Honest-about-litigation-state positioning** | First bellwether defense verdict differentiates Goff from "everyone wins millions" mass tort marketers |
| **Audience synergy with hair relaxer** | Same demographic profile — women of reproductive age — natural cross-linking |

---

## Why the honest framing about the first bellwether matters

Most mass tort marketing firms running Paragard ads will not mention the January 2026 defense verdict. They will continue projecting "up to $1M+" settlement values that may not materialize.

Goff Law's pages explicitly mention the defense verdict and frame settlement projections as recalibrated downward. This positions Goff as the trustworthy firm — claimants who research their case and find that competitor sites overpromised while Goff was honest will sign with the firm that told them the truth.

This is a counterintuitive marketing move that should serve Goff well long-term: **honest expectation-setting builds trust that closes cases**.

---

## Why Paragard is structurally smart even with the defense verdict

1. **3,984 pending cases means active litigation pipeline.** Even if average settlement values are lower than originally projected, the volume of pending claims means global settlement is likely eventually.

2. **The audience is reproductive-age women — same as Hair Relaxer.** Cross-linking and combined women's mass tort positioning is more efficient than disconnected single-tort marketing.

3. **The Spanish niche is uncontested across all 25 DFW competitors.** Even modest Spanish-speaking Latina case flow (2-5 cases/year) at $40K-$400K per case = $80K-$2M annual revenue from one Spanish landing page.

4. **Settlement timing tailwind.** Bellwether trials are happening NOW. Late 2026 or 2027 likely sees global settlement structures emerge. Claims filed now participate in early settlement waves.

5. **No incumbents means first-mover advantage on SERP positioning.** When global settlement is announced and the public starts searching aggressively, Goff is positioned to capture organic traffic that no DFW competitor is currently competing for.

---

## Expected timeline to results

- **Week 1:** Pages live, indexed, schema validated
- **Weeks 2-4:** Google crawls + ranks; long-tail Paragard queries appear in GSC
- **Months 2-3:** Featured snippet / AI Overview citations surface
- **Months 3-6:** First Paragard inquiries from organic search arrive
- **Months 6-12:** Full SERP positioning established
- **Late 2026 / 2027:** Likely global settlement emerges → spike in inquiries → Goff positioned to capture

---

## Status

- **Drafted:** ✅ 2026-05-16
- **Approved by Jim:** ✅ 2026-05-16
- **Pending:** Dev team WordPress deployment
- **Owner:** Chelsea to route to dev or coordinate deployment

Once deployed, update this file with deployment date + URLs for 30-day check-in.

---

## Project #3 complete summary

| Project | Tort | URL count | Word count | Status |
|---|---|---|---|---|
| #1 | AFFF Firefighter Cancer | 4 pages | ~11,400 | Drafted; pending Chelsea/dev deploy |
| #2 | Hair Relaxer Cancer | 4 new + schema add to existing Dallas | ~10,800 | Drafted; pending Chelsea/dev deploy |
| #3 | Paragard IUD | 5 pages (including Spanish) | ~13,200 | **Drafted; pending Chelsea/dev deploy** |

**Total mass tort content shipped to dev pipeline: 13 new pages + 1 existing-page schema add-on = ~35,400 words of niche mass tort content across 3 federal MDLs, all uncontested in DFW.**

When Chelsea is ready, all three projects can be deployed in sequence over ~3 weeks of dev work. Or parallelized if multiple dev resources are available.

---

## Project #4 candidate (next in queue per the top-25 gap analysis)

Next federal MDL with zero DFW competitor coverage and clear template fit:

- **Tepezza (hearing loss) — MDL 3079 N.D. Illinois**
  - Horizon Therapeutics manufacturer
  - Hearing loss / tinnitus from thyroid eye disease treatment
  - Adult population, both genders (different demographic from Paragard/Hair Relaxer)
  - No DFW competitor coverage
  - Federal preemption applies

Whenever you want to greenlight Project #4 — same template, ~5-7 hours of drafting on my side, ~5-7 hours dev deploy.
