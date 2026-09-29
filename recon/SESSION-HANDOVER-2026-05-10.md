# Session Handover — 2026-05-10

**For:** the next Claude Code session (or future Jim) picking up this work
**Session run by:** Claude Opus 4.7 (1M context), interactive
**Duration:** ~ evening of 2026-05-09 + morning/evening of 2026-05-10

---

## What got done tonight

### 1. Crawl4AI MCP server installed and operational
- Docker container `crawl4ai` running on `localhost:11235`
- Registered with Claude Code as MCP server `c4ai-sse`
- **Lifecycle gotcha:** does NOT auto-restart on machine reboot. Run `docker start crawl4ai` after rebooting Windows.

### 2. Phase 1 + Phase 2 recon complete on Thompson Law
- Real URL is **`1800lionlaw.com`** (NOT `thompsons.law` — that's a UK firm)
- Reports at:
  - `recon/thompson-law/PHASE-1-RECON-REPORT.md` — site footprint + positioning + vulnerabilities
  - `recon/thompson-law/PHASE-2-DEEP-DIVE-REPORT.md` — schema audit + SERP positioning + authority signals

### 3. Major narrative-shifting findings
- **Thompson Law is invisible at the top of Google for DFW commercial queries.** Their ~2,000-page programmatic SEO factory doesn't crack top 10 organic for any tested query — including Dallas itself.
- **The actual organic competitor in DFW PI is Mullen & Mullen** (mullenandmullen.com). Appears in 4 of 6 SERPs tested.
- **Suburb specialists own each suburb** (Snellings/Frisco, McCraw/McKinney, Burress/Allen, Vecchio/Plano).
- **Witherite owns Dallas truck SERPs** specifically.
- **Schema markup is a major Goff opportunity** — Thompson Law lacks Attorney, AggregateRating, Service, and Offer schema despite their volume.

### 4. Existing competitive analysis docs corrected
The original strategy docs all cited the wrong Thompson Law URL (`thompsons.law` UK firm). Three docs corrected with:
- URL replacements (thompsons.law → 1800lionlaw.com)
- Visible correction notices at the top of each doc
- Inline `~~strikethrough~~ ⚠️ STALE` flags on quantitative metrics measured against the wrong URL

Affected docs:
- `goff-law-dfw-competitive-analysis-COMPLETE.md` (canonical source; others consolidated into this)

### 5. Full SEO audit plan written
- Plan: `docs/plans/2026-05-10-goff-law-full-seo-audit.md`
- 6 phases, ~14 tasks, 80-150 min runtime
- Designed to be executed via the `superpowers:executing-plans` skill in a parallel session
- Deliverables will land at `recon/goff-law/01-*.md` through `10-prioritized-roadmap.md`
- **Status as of this handover:** plan written, NOT yet executed. Jim chose the parallel-session execution path.

---

### 6. Strategic positioning SVG (for the COO deck)
- File: `recon/dfw-pi-positioning-map.svg` (1400×1050, dark mode)
- 2x2: Geographic scope (Local ↔ National) × Practice depth (Generalist ↔ Specialist)
- Plots every firm we have intel on
- Goff Law shown twice: orange star (current, in "Local Generalists" war zone) + green star (target, in "Local Specialist" with emerging-litigation niches), connected by dotted strategic-move arrow
- Thompson Law demoted to grey ("Brand/ad-spend · NOT organic threat")
- Mullen & Mullen + Witherite flagged red as real threats

### 7. Competitor scoreboard ("the burn book")
- File: `recon/COMPETITOR-SCOREBOARD.md`
- Tier S/A/B/C ranking of every DFW PI firm by ACTUAL organic threat
- Includes the "Not actually competitors" wall of shame (thompsons.law UK, thompsonlawtx.com estate-planning, Arnold & Itkin Houston)
- Live SERP scoreboard table for the 6 tested queries
- Top-10 strike order

### 8. Weekly automated SERP rank watch
- claude.ai routine ID: `trig_01D6LVUNAgUTqnPgidRa7drG`
- Cron: `0 13 * * 1` (every Monday 8am Central / 13:00 UTC)
- Manage at: https://claude.ai/code/routines/trig_01D6LVUNAgUTqnPgidRa7drG
- Runs the 6 SERP queries, tracks 4 priority firms, computes diff vs last week, saves `DFW-SERP-Watch-YYYY-WNN.md` to Goff's Google Drive
- Baseline run kicked off 2026-05-10 evening
- DST gotcha: cron is UTC — will drift to 7am Central in Nov 2026 when DST ends

### 9. UX recon (Phase 1)
- Report: `recon/goff-law/UX-RECON-PHASE-1.md`
- Screenshots: `recon/ux-screenshots/{goff-home,goff-contact,thompson-home,mullen-home,witherite-home}.png`
- Visual + conversion-mechanic comparison of Goff vs Thompson, Mullen, Witherite
- UX scoreboard: **Goff 25/70, Witherite 53/70 (best), Thompson + Mullen tied at 44/70**
- Headline finding: Goff has the strongest brand voice in the field but the weakest above-the-fold conversion mechanics
- Quick-win matrix with effort/impact ratings
- Phase 2 backlog: mobile device testing, PageSpeed measurement, heatmap install, A11y audit

### 10. Mullen & Mullen Phase 1 recon (the REAL organic threat)
- Report: `recon/mullen-mullen/PHASE-1-RECON-REPORT.md`
- Raw artifacts: `recon/mullen-mullen/raw/` (8 page crawls + sitemap + robots + raw HTML)
- Headline: Mullen has 29% pre-suit contingency (vs industry 33-35%), 567 Google reviews, 43-year tenure, 3 DFW offices (Dallas + Plano + Frisco)
- Critical reframe: Goff's "lifelong Dallas resident" angle is NOT unique — Mullen claims the same local positioning. Goff's truly defensible moats: former insurance defense attorney + mass tort/emerging litigation depth.
- Phase 2 backlog: schema audit, backlinks, blog discovery, lead-form mystery shop, pricing math audit

### 11. Goff Law Homepage Hero Fix — drop-in spec
- File: `recon/goff-law/HERO-FIX-DRAFT.md`
- Tier-0 UX fix specification ready for the WordPress dev
- Includes: ASCII mockup, HTML/CSS code skeleton, 4 headline copy alternatives, inputs needed from Jim, form integration notes, acceptance checklist
- Estimated impact: 50-100% lift in homepage lead capture rate (industry benchmark)
- Estimated dev time: 4-8 hours

### 12. Interactive Competitive Intelligence Dashboard
- File: `recon/dashboard.html` (single self-contained HTML, ~750 lines)
- Modern dark mode UI (Tailwind via CDN, Inter font, scroll animations)
- Sections: Hero · Stats · Threat Ranking (S/A/B/C tiers) · Embedded SVG Positioning Map · Live SERP Standings · Expandable Competitor Profiles · The Strike List · Artifact Grid
- Companion file: `recon/dfw-pi-positioning-map.svg` (must be in same folder)
- Portable: works locally OR can be added to Bill AI Machine at `C:\Users\jim\OneDrive\Documents\Bill AI Machine\` (separate Streamlit + RAG app deployed to gofflawsuperagent.up.railway.app)

---

## What's queued next

### Immediate (next session — Jim's pick)
1. **Execute the SEO audit plan** in a parallel session. Command:
   ```
   /superpowers:execute-plan docs/plans/2026-05-10-goff-law-full-seo-audit.md
   ```
   If that command isn't available, paste this instead:
   ```
   Read docs/plans/2026-05-10-goff-law-full-seo-audit.md and execute it task by task using the superpowers:executing-plans skill. The workspace is not a git repo — skip git commits, use "save artifact + verify" as the checkpoint instead.
   ```

### Phase 3 backlog (after Goff audit)
1. Phase 1 recon vs **Mullen & Mullen** (mullenandmullen.com) — THE organic threat
2. Phase 1 recon vs **Witherite** (witheritelaw.com) — Dallas truck specialist
3. Phase 1 recon vs **Snellings Law** (snellingsinjurylaw.com) — Frisco
4. Phase 1 recon vs **McCraw Law Group** (mccrawlawgroup.com) — McKinney
5. Phase 1 recon vs **Burress Law** — Allen
6. Phase 1 recon vs **Vecchio Injury Law** (vecchioinjurylaw.com) — Plano
7. Pull paid-tool data (Ahrefs/SEMrush) on the corrected competitor set

---

## Standing context the next session needs

### About Jim
- Principal at Goff Law PLLC, DFW PI attorney
- Email: jim@gofflawdfw.com
- Site: gofflawdfw.com
- Technically hands-on (runs Docker, configures Claude Code MCPs)
- Terse communication style — match it

### About the workspace
- Located at `c:\Users\jim\OneDrive\Documents\ArnoldItkin`
- Despite the directory name "ArnoldItkin," the actual subject is **Goff Law PLLC** competitive strategy
- Arnold & Itkin is NOT a competitor (they're a Houston maritime/offshore firm)
- **Workspace is NOT a git repo** — no commits, no branches. Use "save artifact + verify" as the checkpoint instead of git.

### Budget context
- $55K-100K/mo proposed marketing spend
- Targeting 18x ROI ($720K → $13.5M projection)
- Audience for major deliverables: Jim's COO

### Tools available in this workspace
- Crawl4AI MCP (local Docker, see `memory/reference_crawl4ai_mcp.md`)
- WebSearch
- All standard Claude Code file tools (Read/Write/Edit/Glob/Grep)
- Box, Google Drive, Microsoft 365 MCPs (deferred — load via ToolSearch when needed)
- Existing keyword research: `DFW_Personal_Injury_Keyword_Research.md` + `gsc-data/` (Google Search Console exports)
- Content calendars: `goff-law-content-calendar-2025-2026.md`, `goff-law-dfw-domination-content-calendar.md`

### What NOT to do
- Don't email/message anyone or post externally without explicit approval
- Don't modify the live `gofflawdfw.com` site (audit + draft only)
- Don't use `thompsons.law` for Thompson Law (it's a UK firm)
- Don't trust the "DA 55 / 25K monthly traffic / 200+ keywords" claims for Thompson Law in the original docs — those were measured against the wrong URL
- Don't restart Docker Desktop without confirming with Jim first (it can be flaky)

---

## Tooling reference card

**Verify Crawl4AI is alive:**
```
docker ps --filter "name=crawl4ai" --format "{{.Names}}: {{.Status}}"
curl -s http://localhost:11235/health
```

**Restart Crawl4AI after reboot:**
```
docker start crawl4ai
```

**Crawl a URL to markdown:**
```
curl -s -X POST http://localhost:11235/md \
  -H "Content-Type: application/json" \
  -d '{"url": "https://example.com/", "f": "fit"}' \
  -o "$TEMP/output.json" \
  -w "HTTP %{http_code} | %{size_download}b\n" --max-time 90
```

**Get raw HTML for schema audit (Crawl4AI strips `<head>` — use direct curl):**
```
curl -sL --max-time 30 -A "Mozilla/5.0 Chrome/130" "https://example.com/" -o "$TEMP/raw.html"
```

**Verify MCP is registered:**
```
claude mcp list
```

---

## Known quirks discovered tonight

1. **Some sites have broken bare-apex TLS** (e.g., `https://thompsons.law` connection-resets). Always test `www.` prefix as fallback.
2. **Crawl4AI's `/html` endpoint returns CLEANED HTML** without `<head>`. For schema/meta-tag audits, use direct `curl` against the host instead.
3. **Crawl4AI's `/sitemap.xml` request can return an HTML 404 page styled as 200**. Check first 200 chars to confirm `<?xml`.
4. **Python 3.14 is installed but `pip` requires `python -m pip`** (no standalone `pip` on PATH).
5. **`/tmp/` doesn't exist on Windows** — use `$TEMP` or `%TEMP%` in scripts.
6. **Don't use bash heredocs in PowerShell** — the shell is bash via the Bash tool, but Windows path conventions still apply for output files.
