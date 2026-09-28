# Hamilton Wingo, LLP — Pre-Stage Recon Notes

**Status:** PRE-STAGED — awaiting classifier recovery to execute live fetches
**Pre-stage date:** 2026-05-14
**Reason for pre-stage:** Anthropic safety classifier temporarily unavailable; using read-only ops to lay all groundwork so execution drops in minutes once Bash/WebFetch/WebSearch return.

---

## Why Hamilton Wingo jumped to top priority

Existing workspace docs flagged Hamilton Wingo as **LOW threat — "different market segment, doesn't compete for volume cases"** ([goff-law-dfw-competitive-analysis-report.md:275-311](../../goff-law-dfw-competitive-analysis-report.md)). That classification is now **suspect**.

The 2026-05-11 SERP audit ([recon/goff-law/07-serp-positioning.md](../goff-law/07-serp-positioning.md)) caught Hamilton Wingo in the **top 10 organic results for "Dallas personal injury lawyer"** alongside Mullen & Mullen, DFW Injury Lawyers, and Turley Law. That is the head commercial PI query. A "reputation-only referral firm" should not be ranking there.

**Three possible explanations** that this recon must distinguish:

1. **Hamilton Wingo has quietly expanded into consumer PI** — they spun up a marketing operation we didn't know about. Most threatening scenario.
2. **The "$8B settlements" claim is doing the heavy lifting** — their authority/PR alone pushes them up Google's E-E-A-T scoring without active consumer-PI marketing. Still threatening because it means their reputation moat is strong.
3. **The SERP appearance is a fluke/personalization artifact** — they're in top 10 today but not consistently. Lowest threat scenario.

**Critical question to resolve in this recon:** Is Hamilton Wingo a sleeping giant that's woken up, or a referral firm that lucked into a SERP slot?

---

## Confirmed baseline facts (from existing workspace docs)

| Field | Value | Source |
|---|---|---|
| Firm name | Hamilton Wingo, LLP | goff-law-dfw-competitive-analysis-report.md:277 |
| Founded | 1990s (decade-level only) | competitive-analysis:278 |
| Partners | Dean Hamilton, Jim Wingo | competitive-analysis:279 |
| Website | hamiltonwingo.com | competitive-analysis:280 |
| Notable verdict | **$7.37 billion verdict — largest in Texas history** | competitive-analysis:281 |
| Settlements claim (SERP audit) | **$8 BILLION** | recon/goff-law/07-serp-positioning.md:81 |
| Practice areas | Catastrophic injuries, wrongful death, trucking, product liability, complex commercial litigation | competitive-analysis:282-287 |
| Marketing posture | Reputation-Based, Limited Advertising, Referral Network | competitive-analysis:289-292 |
| Phone | (214) 234-2900 | competitive-analysis:2625-2640 |
| Address | 3300 Oak Lawn Ave, Dallas, TX 75219 | competitive-analysis:2625-2640 |

⚠️ **Address curiosity:** 3300 Oak Lawn Ave is also referenced as Thompson Law territory in prior docs. Verify whether this is a coincidence (shared building / coworking) or a data error in source docs.

**Stale-data warning:** The "founded 1990s," partner list, and threat classification all come from a single secondary source. The big-verdict claim ($7.37B) needs corroboration. Treat all of this as starting hypotheses, not facts.

---

## Live fetch target list (run when classifier returns)

### Tier A — must fetch (Phase 1 baseline)

| # | URL | Tool | Goal |
|---|---|---|---|
| 1 | `https://hamiltonwingo.com/` | WebFetch | Homepage — hero claim, trust signals, CTA design, primary practice areas, settlement claim verbatim |
| 2 | `https://hamiltonwingo.com/robots.txt` | curl/WebFetch | Sitemap discovery, blocked-bot configuration, AI-bot policy |
| 3 | `https://hamiltonwingo.com/sitemap.xml` or `/sitemap_index.xml` | curl/WebFetch | Total page count, content types, recent lastmod dates |
| 4 | `https://hamiltonwingo.com/attorneys/` (or `/our-team/`, `/our-attorneys/`) | WebFetch | Current attorney roster — is it still just Dean + Jim or has the firm grown? Bar admission dates, prior career details |
| 5 | `https://hamiltonwingo.com/results/` (or `/verdicts-settlements/`, `/case-results/`) | WebFetch | Verbatim case results — does the $8B claim actually total to $8B when you add the individual results? Or is it puffery? |
| 6 | `https://hamiltonwingo.com/contact/` | WebFetch | Office count, intake hours, intake form fields, alternate phone numbers |
| 7 | `https://hamiltonwingo.com/practice-areas/` (or `/practice/`) | WebFetch | Are practice areas limited to catastrophic litigation, or has consumer PI been added? |

### Tier B — fetch if Tier A reveals expansion into consumer PI

| # | URL pattern | Goal |
|---|---|---|
| 8 | `/personal-injury-lawyer/` or `/dallas-personal-injury-lawyer/` | Confirms consumer-PI marketing exists |
| 9 | `/car-accident/`, `/truck-accident/`, `/motorcycle-accident/` | Detect template-based programmatic SEO (à la Thompson Law) |
| 10 | `/blog/` index | Blog cadence, topics, last post date — referral firms typically have no blog; SEO-active firms post weekly |
| 11 | `/galaxy-gas/` or `/nitrous-oxide/` | Are they encroaching on Goff's #1 win? |
| 12 | Spanish pages `/abogados/...` | Bilingual scaling indicator |
| 13 | Schema check via `view-source:` on homepage | LegalService / AggregateRating / Attorney schema presence |

---

## WebSearch queries to run (parallel batch, when classifier returns)

```
1. "Hamilton Wingo" Dallas "personal injury" 2026
2. "Hamilton Wingo" verdict settlement billion
3. "Dean Hamilton" attorney Dallas Texas history
4. "Jim Wingo" attorney Dallas Texas history
5. site:hamiltonwingo.com
6. "Hamilton Wingo" reviews Google
7. "Hamilton Wingo" advertising marketing
8. "$7.37 billion" Texas verdict largest history
9. "Hamilton Wingo" attorneys roster
10. "Hamilton Wingo" referrals lawyer
```

**Goal:** Confirm/refute the "reputation-based, no advertising" posture and find recent news, hires, expansions, or PR.

---

## Data extraction questions (per page)

### Homepage
1. What is the hero H1? Does it target a commercial query (e.g. "Dallas Personal Injury Lawyer") or a positioning statement (e.g. "Texas Trial Attorneys")?
2. Settlement total claim verbatim — and what time period does it cover?
3. Does any phrase indicate consumer intake (e.g. "free consultation," "no fee unless we win," "24/7 intake")?
4. Trust signals — what gets stacked? (Super Lawyers, Best Lawyers, board certs, Texas Top 100)
5. CTA design — phone number prominence, form-first or phone-first?
6. Any mention of contingency fee percentage?

### Attorneys page
1. How many attorneys currently? Compare to Mullen & Mullen's roster.
2. Founders' bios — bar admit year, law school, prior firms?
3. Any associate-tier attorneys (an associate roster signals firm-building beyond two founders)?

### Results page
1. Top 10 individual case results — extract dollar amounts. Do they sum to $8B or only $7.37B (one mega-verdict + smaller tail)?
2. Most recent dated verdict — is the firm still actively litigating recent cases or coasting on the big one?
3. Case types — predominantly catastrophic (1 mega-case per year)? Or volume PI (many mid-size)?

### Robots / sitemap
1. Total page count.
2. Spanish duplicate? (à la Thompson Law)
3. Blog count.
4. Last-modified dates — is the site actively maintained?
5. AI bots (GPTBot, ClaudeBot, Anthropic-AI, CCBot) — allowed or blocked?

---

## Cross-comparisons to make in the report

| Dimension | Thompson Law (1800lionlaw.com) | Mullen & Mullen | Goff Law DFW | Hamilton Wingo (TBD) |
|---|---|---|---|---|
| Settlements claim | $1.9B | $800M+ | TBD | **$8B (largest)** |
| Total pages | ~2,000+ | ~150 (est.) | ~100 | ??? |
| State coverage | TX/CA/AZ/GA | TX only (Dallas/Plano/Frisco) | TX only | ??? |
| Bilingual | Yes (full Spanish) | No | No | ??? |
| Blog cadence | Daily | Weekly | Variable | ??? |
| Contingency fee | Industry-standard 33-40% | 29% pre-suit | Industry-standard | ??? |
| Attorney count | ~15-20 (est) | 8-10 (est) | 1 (Jim) | 2 founders + ??? |
| Marketing intensity | Industrial-scale SEO | Mid-tier SEO + reviews moat | Niche mass-tort wins | TBD |
| Threat classification | HIGH (programmatic SEO machine) | HIGH (real organic threat) | — | **TBD** (was LOW, now suspect) |

---

## Report skeleton (match Thompson Law / Mullen Phase 1 format)

```
# Hamilton Wingo — Phase 1 Recon Report

## Critical alert — [if existing docs misclassified the threat level]
## Footprint at a glance — page count, settlements, attorneys, offices
## Page architecture — template-based or bespoke?
## Positioning & messaging stack — brand identifiers, promise stack, trust signals
## Practice area coverage — catastrophic-only or consumer PI added?
## Schema markup audit — preliminary view-source check
## Recent activity signals — blog cadence, last-modified, new attorneys
## SEO posture — robots.txt, sitemap, bilingual, AI bot policy
## Verdicts/settlements analysis — does $8B claim hold up?
## Vulnerabilities (where Goff can compete)
## Strengths (what Goff cannot match directly)
## Threat reclassification — final HIGH / MED / LOW with reasoning
## Recommended Phase 2 deep-dive questions
```

---

## Specific cross-checks against existing intel

### Versus the SERP audit (recon/goff-law/07-serp-positioning.md)

The SERP audit caught Hamilton Wingo on the "Dallas personal injury lawyer" head term. This recon must verify:
- Is Hamilton Wingo's current ranking page targeting "Dallas personal injury lawyer" as a primary query?
- Is it on a dedicated PI landing page or just the homepage?
- What other commercial-intent queries do they currently rank for? (Re-run targeted WebSearches: "Dallas truck accident lawyer," "Dallas wrongful death lawyer," "Dallas catastrophic injury lawyer")

### Versus the competitive analysis report (goff-law-dfw-competitive-analysis-report.md)

The existing classification needs reconciliation:
- Lines 275-311 say "Threat Level: LOW (different market segment)"
- Lines 289-292 say "Strategy: Reputation-Based, Limited Advertising, Referral Network"
- SERP audit contradicts both. Reconcile in the recon report's "Threat reclassification" section.

### Versus Thompson Law

- 3300 Oak Lawn Ave — is this also Thompson Law's address? Need to verify. Could be coincidence (shared coworking building) or a data error in source docs.
- Settlement claims race: Thompson Law claims $1.9B, Hamilton Wingo claims $8B. Both can't be Dallas's biggest. Which one is doing the rounding more aggressively?

---

## What this recon enables for Jim/Chelsea

1. **Updates the competitor scoreboard** ([recon/COMPETITOR-SCOREBOARD.md](../COMPETITOR-SCOREBOARD.md)) — Hamilton Wingo currently absent or undertiered.
2. **Updates the intel dashboard** at gofflawsuperagent.up.railway.app/intel — threat ranking, profile card, strike list.
3. **Resolves the $8B claim ambiguity** for Chelsea's COO briefing — is this real or marketing puffery?
4. **Informs the geographic strategy** — if Hamilton Wingo is consumer-PI-active, it changes the Dallas head-term battle plan. If they're still pure-catastrophic-referral, the head-term battle is between Goff and Mullen & Mullen with Hamilton Wingo as a flanking threat only.
5. **Identifies any new emerging-litigation overlap** — if they touch Galaxy Gas, AFFF, or other mass torts where Goff currently dominates, that's a major defensive concern.

---

## Execution checklist (when classifier returns)

- [ ] Batch-fetch Tier A URLs (7 pages) via WebFetch in parallel
- [ ] Run 10 WebSearch queries in parallel
- [ ] Conditional: Tier B URLs if Tier A shows consumer-PI expansion
- [ ] Write `PHASE-1-RECON-REPORT.md` using report skeleton above
- [ ] Update `recon/COMPETITOR-SCOREBOARD.md` with Hamilton Wingo tier placement
- [ ] Update Bill AI Machine `/intel` route — add Hamilton Wingo profile card
- [ ] Update memory: write `reference_hamilton_wingo_recon.md`, add to `MEMORY.md`
- [ ] Reconcile/correct existing competitive-analysis docs lines 275-311 if threat classification changes

---

## Files referenced

- `goff-law-dfw-competitive-analysis-report.md` (workspace root) — lines 275-311, 2625-2640
- `recon/goff-law/07-serp-positioning.md` — line 19 (Dallas PI SERP), line 81 ($8B claim, top-10 placement)
- `recon/COMPETITOR-SCOREBOARD.md` — needs Hamilton Wingo row added
- `recon/thompson-law/PHASE-1-RECON-REPORT.md` — template for output format
- `recon/mullen-mullen/PHASE-1-RECON-REPORT.md` — template for output format
