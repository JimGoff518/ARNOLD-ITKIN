# 90-Day Keyword Execution Plan — Draft Retrospective

**Date:** 2026-05-16 (drafts shipped in single session; published rollout TBD by Goff/Chelsea)
**Parent plan:** `docs/plans/2026-05-16-keyword-execution-90-day.md`
**Status:** All 5 phases drafted; WordPress publish + GSC baseline = Jim/Chelsea step

---

## Output Summary

| Phase | Pages | Words | Source dir | Volume target |
|---|---|---|---|---|
| 1 EN — FAQ | 10 | ~14,240 | `recon/goff-law/faq-drafts/` | 2,510/mo aggregate |
| 1b ES — FAQ | 8 | ~11,365 | `recon/goff-law/faq-drafts-spanish/` | est. matches EN |
| 2 — Truck/Highway | 8 | ~11,500 | `recon/goff-law/phase2-drafts/` | 275/mo aggregate |
| 3 — Mass Tort × DFW | 10 | ~17,580 | `recon/goff-law/phase3-drafts/` | 308/mo aggregate |
| 4 — Suburb | 4 | ~6,770 | `recon/goff-law/phase4-drafts/` | 845/mo aggregate |
| 5 — Emerging Tort | 4 | ~6,470 | `recon/goff-law/phase5-drafts/` | 110/mo aggregate |
| **Total** | **44** | **~67,925** | — | **~4,000/mo target** |

Live preview viewer: `gofflawsuperagent.up.railway.app/faq-drafts` (after Railway redeploy).

---

## What Worked

1. **Sequenced parallel agent dispatch.** Each phase = 2 parallel agents writing ~4-5 pages each from a shared brief + research files. Output consistency was good (voice + structure + schema patterns held across all 44 pages).

2. **Source-cited data as trust anchor.** Phase 2 truck pages cite TxDOT directly (every numeric claim hyperlinked to `.txdot.gov`). Phase 3 mass-tort pages cite specific MDL court / judge / FDA action. This is the SEO differentiator vs generic competitor content.

3. **Honest framing where data is incomplete.** Phase 2 corridor pages don't claim per-corridor stats TxDOT doesn't publish — they say so explicitly ("TxDOT does not publish I-635-specific fatal counts in free reports"). This is a trust signal AND avoids E-E-A-T penalties.

4. **City-pair differentiation in Phase 3.** Dallas vs FW versions of the same MDL had genuinely different DFW content (named hospitals, named bases, named neighborhoods). NOT copy-paste with city swap.

5. **No competitor bashing.** Held the line on this across all 44 pages. Differentiation done positively (Goff's focus / federal experience / responsiveness / bilingual) rather than attacking others.

6. **Filter-language for traffic quality.** Phase 4 suburb pages explicitly disclaim excluded case types ("we don't handle workers' comp / medmal / dog bite — we'll refer you"). Filters bad-fit traffic, signals trust, reduces wasted intake.

## Friction Encountered

1. **TxDOT corridor-isolation gap.** TxDOT free PDFs aggregate by county+road-type; per-corridor extraction needs an interactive CRIS Query session (~1-2 hrs). Per locked decision, Phase 2 shipped with county-aggregate framing — accepted trade-off. If Phase 2 underperforms, the CRIS Query session is the next-best lever.

2. **Cross-link slug uncertainty.** Phase 4 agent flagged ambiguity on Phase 2 highway slugs (assumed `/practice-areas/truck-accidents/dallas-north-tollway/` but Phase 2 actually built `/practice-areas/truck-accidents/i-35-truck-accidents-dallas/` etc.). Generic risk across all 44 pages: assumed URL slugs need a global find-replace audit before publish.

3. **Phase 4 cross-linked to a non-existent Phase 3 page.** Plano page (S4) referenced an "Amazon DSP/DDA3 Plano" mass-tort page that doesn't exist — only Dallas + FW Amazon DVR exist. **Fix:** S4 Plano link should swap to Amazon Dallas (M9) or AFFF.

4. **Phase 1 strict gate never closed during this session.** WordPress publish + GSC baseline are Jim/Chelsea steps. All 5 phases were drafted on the in-progress side of the gate per Jim's explicit "ship it" directive. Accepted deviation from the strict [[feedback-phase-order]] rule; documented in plan status log.

5. **Spanish drafts need native-speaker review.** Mexican Spanish vocabulary choices (carro, aseguranza) were made deliberately for the DFW Hispanic-American audience — but they're non-standard from a strictly grammatical perspective. Native review recommended before publish.

## Recommendations Before WordPress Publish

### Global (applies to all 44 pages)

1. **`{{CTA_PHONE}}` global find-replace** with the actual call/text number.
2. **`/attorneys/jim-goff/` bio URL verification.** If different, find-replace.
3. **URL slug audit.** Phase 4 + Phase 5 link to assumed slugs from Phases 2 + 3 — verify match before publish.
4. **Publish each phase together.** Otherwise cross-links 404. Phase 1 (10 pages), 1b (8 pages), 2 (8 pages), 3 (10 pages), 4 (4 pages), 5 (4 pages) — bundle each.
5. **Build practice-area hub pages** if they don't exist: `/practice-areas/mass-tort/`, `/practice-areas/truck-accidents/`, `/practice-areas/car-accident/`, `/locations/` parent. Drafts assume these exist.

### Phase-specific

- **Phase 1 ES:** native Mexican Spanish reviewer recommended.
- **Phase 1 Page 9 (Pain & Suffering):** generic ranges only (no specific Texas verdicts) — per locked decision. If Jim later wants verified verdict citations, that's a v2 revision.
- **Phase 2 corridors:** if rankings underperform at 90 days, run a CRIS Query session for per-corridor data and update.
- **Phase 3 hair relaxer (M5/M6):** community-context sensitivity review before publish.
- **Phase 3 contingency %:** verify Pages 4 + 10 percentages match Goff's actual engagement letter.
- **Phase 5 DoorDash $1M coverage figure (E2):** verify still current — gig-platform insurance limits do get adjusted.

## What's Next After Publish

1. **GSC baseline:** save filter for each phase URL set. Track impressions/clicks Day 30 → Day 90.
2. **Phase 6 — programmatic mass-tort × city build.** If Phase 3 traction validates, expand the 5 MDLs × 6 remaining DFW cities (Plano, Frisco, Arlington, McKinney, Denton, Irving) = 30 more pages. Templating-friendly.
3. **Spanish Phase 2/3/4/5.** Currently only Phase 1 has Spanish drafts. If Phase 1 ES wins, extend.
4. **Schema validation pass.** Run Google's Rich Results test on every URL post-publish.
5. **Local-SEO touch.** GBP categories + attributes + Google Posts referencing the new content (per [[reference-local-seo-pi-playbook]] guidance).

---

## Plan Gate Reality Check

The original plan defines Phase N "done" as: pages **published, indexed, schema-valid, GSC baseline saved**. Under that strict definition, ALL 5 phases are still on the in-progress side of their gate (drafts complete, publish pending).

What was actually shipped this session:
- 44 WordPress-ready draft markdown files
- Sidebar-navigated review viewer at `/faq-drafts` (Bill AI Machine)
- Source-of-truth in `recon/goff-law/` + mirrored to Bill AI Machine static dir
- Full plan, memory artifacts, and this retrospective

Publish, schema validation, and GSC baseline are Goff team next steps.
