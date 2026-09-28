# AFFF Pages — Dev Team Deployment Package

**Project:** Replicate Galaxy Gas template across AFFF firefighter cancer mass tort (4 city-targeted pages)
**Approved by:** Jim Goff 2026-05-14
**Estimated dev time:** 4-6 hours total (1-1.5 hours per page in WordPress page editor)
**Strategic rationale:** Revenue defense post-Aldous referral loss; AFFF MDL has 15,222 pending claims, $20K-$600K projected per case, federal preemption bypasses Texas tort caps. See `recon/playbooks/local-seo-pi-playbook.md` for broader context.

---

## What's being deployed

**4 new pages on gofflawdfw.com**, each a complete city-targeted AFFF firefighter cancer landing page with FAQPage + LegalService JSON-LD schema. Each page is ~2,800 words, follows the Galaxy Gas template structure (which currently ranks 4 of top 10 organic for "Galaxy Gas injury lawyer"), and targets a distinct firefighter sub-population.

| # | URL slug | Target audience | Meta title |
|---|---|---|---|
| 1 | `/dallas-afff-lawyer/` | Dallas Fire-Rescue + DFW Airport ARFF | Dallas AFFF Lawyer \| Firefighter PFAS Cancer Lawsuit \| Goff Law |
| 2 | `/texas-afff-firefighter-lawyer/` | Texas military firefighters (Lackland, Fort Hood, Sheppard, NAS) | Texas AFFF Firefighter Lawyer \| Military & Civilian PFAS Cancer Claims \| Goff Law |
| 3 | `/north-texas-afff-lawyer/` | Plano, Frisco, Allen, McKinney, Arlington suburb firefighters | North Texas AFFF Lawyer \| Suburb Firefighter PFAS Cancer Claims \| Goff Law |
| 4 | `/houston-afff-firefighter-lawyer/` | Houston Fire + refinery emergency response + ARFF | Houston AFFF Firefighter Lawyer \| Refinery & Municipal PFAS Cancer Claims \| Goff Law |

---

## Files in this package

| File | Purpose |
|---|---|
| `01-dallas-afff-lawyer.md` | Page 1 — full content, meta, FAQ block, internal linking |
| `02-texas-afff-firefighter-lawyer.md` | Page 2 — full content |
| `03-north-texas-afff-lawyer.md` | Page 3 — full content |
| `04-houston-afff-firefighter-lawyer.md` | Page 4 — full content |
| `SCHEMA-JSON-LD.md` | FAQPage + LegalService schema blocks for all 4 pages (copy-paste ready) |
| `DEPLOYMENT-PACKAGE.md` | This file — dev instructions |

---

## Step-by-step deployment instructions

### For each of the 4 pages:

**Step 1 — Create the WordPress page**
1. WordPress admin → Pages → Add New
2. Set page title to match the H1 from the corresponding `.md` file
3. Set permalink slug to match the URL in the file header (e.g., `/dallas-afff-lawyer/` → slug: `dallas-afff-lawyer`)

**Step 2 — Paste the body content**
1. Copy everything from the `## PAGE BODY` section through the FAQ block
2. Paste into the WordPress page editor (block editor is fine)
3. Mark the H1 as a Heading 1 block (or set the page title to render as H1; depends on the theme)
4. Format H2/H3 sections per the heading hierarchy in the source file
5. Keep all internal links exactly as written (they reference other AFFF pages + existing Goff service pages)

**Step 3 — Configure Yoast SEO**
1. Scroll to the Yoast SEO meta box at the bottom of the page editor
2. **SEO title:** copy from the `## METADATA` section of the source file
3. **Meta description:** copy from the `## METADATA` section
4. **Canonical URL:** confirm matches the page slug
5. **Focus keyword:** set to the primary keyword listed in the source file (e.g., "Dallas AFFF lawyer")

**Step 4 — Add the JSON-LD schema**
1. Open `SCHEMA-JSON-LD.md`
2. Find the section for this page
3. Copy BOTH the `<script type="application/ld+json">` blocks (FAQPage + LegalService)
4. Paste into the page using ONE OF these methods:
   - **Method A (preferred):** Use Yoast's "Schema" tab if available — paste the JSON (without the `<script>` tags) into a custom schema field
   - **Method B:** Add a Custom HTML block at the top or bottom of the page body containing both `<script>` blocks
   - **Method C:** Insert via theme's "Custom Code" or "Header Code" feature targeted to this specific page only
5. Confirm with Yoast's preview or Google's Rich Results Test (https://search.google.com/test/rich-results) that the schema validates

**Step 5 — Publish**
1. Set publication status to Published
2. Clear cache (W3 Total Cache or whatever caching plugin is active)
3. Verify the page loads at the correct URL
4. Test on mobile

### Repeat for all 4 pages.

---

## Verification checklist (after all 4 pages live)

Visit each URL in a fresh browser (logged out) and confirm:

- [ ] `gofflawdfw.com/dallas-afff-lawyer/` — loads, H1 visible, FAQ block visible, phone number 972-928-0085 visible above the fold
- [ ] `gofflawdfw.com/texas-afff-firefighter-lawyer/` — same checks
- [ ] `gofflawdfw.com/north-texas-afff-lawyer/` — same checks
- [ ] `gofflawdfw.com/houston-afff-firefighter-lawyer/` — same checks
- [ ] View source on each page — confirm `<title>` tag, `<meta name="description">`, and BOTH JSON-LD `<script>` blocks present
- [ ] Run each page through https://search.google.com/test/rich-results — FAQPage schema validates without errors
- [ ] Internal links between the 4 pages work (each page has a "Related" section linking to the other 3)
- [ ] Mobile rendering — content readable, no awkward line breaks in H1
- [ ] PageSpeed Insights — no regression from baseline

---

## Cross-linking from existing pages (after deploy)

To boost the new pages' authority and signal Goff's mass-tort breadth, add these links from EXISTING pages within 1 week of deployment:

**Homepage (`gofflawdfw.com/`):**
- Add to footer or "Practice Areas" menu: "AFFF Firefighter Cancer Lawsuits" → link to `/dallas-afff-lawyer/`

**Galaxy Gas page (`gofflawdfw.com/dallas/galaxy-gas-lawyer/`):**
- Add to "Related Practice Areas" sidebar: "AFFF Firefighter Cancer (companion mass tort)" → link to `/dallas-afff-lawyer/`

**Product Liability page:**
- Add reference to AFFF as a current product liability mass tort → link to `/dallas-afff-lawyer/`

**Catastrophic Injury page:**
- Add note about AFFF cancer cases → link to `/dallas-afff-lawyer/`

**Wrongful Death page:**
- Add reference to deceased firefighter AFFF claims → link to `/dallas-afff-lawyer/`

---

## Sitemap submission

After deployment:
1. **WordPress XML sitemap** — Yoast will auto-add the new pages to the XML sitemap. Verify at `gofflawdfw.com/sitemap_index.xml`
2. **Google Search Console** — submit the new URLs individually for crawling:
   - Inspect URL → Request Indexing for each of the 4 pages
3. **Bing Webmaster Tools** — same submission process

---

## Optional: Hreflang / international targeting

These pages target Texas firefighters specifically (English-language US market). No hreflang needed. If a Spanish version is added later (e.g., `/abogado-afff-bombero-texas/`), the English version would need `hreflang="es"` + `hreflang="en"` declarations linking the pair.

---

## What this deployment ACCOMPLISHES strategically

| Goal | Mechanism |
|---|---|
| **Replicate Galaxy Gas SERP success** | Same template that ranks 4 of top 10 for Galaxy Gas, applied to AFFF |
| **Revenue defense post-Aldous referral loss** | Direct-from-search PI client pipeline for $50-200K mass tort cases |
| **Federal preemption (Texas tort caps don't apply)** | AFFF is federal MDL — bypasses Texas $250K non-economic cap |
| **AI Overview / featured snippet eligibility** | FAQ schema enables Google's AI Mode to cite Goff Law in answers |
| **No PPC required** | Pure organic SEO — aligns with locked "no PPC until $1.5M+" strategy |
| **Uncontested SERP territory** | Zero of 9 reconned DFW PI competitors have any AFFF presence |
| **High-value cases only** | $20K-$600K per case (vs $5-15K fender-bender fees) = better per-case economics |

---

## Expected timeline to results

- **Week 1:** Pages live, indexed, FAQ schema validated
- **Weeks 2-4:** Google crawls + ranks; long-tail AFFF queries begin appearing in GSC impressions
- **Months 2-3:** Featured snippet / AI Overview citations start surfacing for FAQ questions
- **Months 3-6:** First firefighter inquiries from organic search likely arrive
- **Months 6-12:** Full SERP positioning established for `[city] AFFF lawyer` queries

This is not a magic-bullet deployment. It's the patient, compounding work of building defensible niche SERP territory. Galaxy Gas didn't get to 4 of top 10 overnight either.

---

## Future expansion (Project #2 candidates)

After AFFF pages are live and indexed, the same template applies cleanly to:

| Mass tort | Why next | Timeline |
|---|---|---|
| **Hair relaxer (ovarian cancer)** | Federal MDL active, large plaintiff pool, uncontested niche; bonus Spanish-language opportunity | Project #2 |
| **Tepezza (hearing loss)** | Federal MDL active, Horizon Therapeutics manufacturer | Project #3 |
| **Paragard IUD** | Active MDL, fragmentation injury cases | Project #4 |
| **Suboxone tooth decay** | Newer MDL, growing | Project #5 |
| **Social media addiction (Meta MDL)** | Federal MDL, families of teens with mental health injury | Project #6 |
| **AI Liability (emerging)** | First-mover niche, no incumbents | Project #7 |

Each project follows the same pattern: 4 city-targeted pages + FAQ schema + LegalService schema + cross-linking + sitemap submission. After the first AFFF deployment, subsequent mass-tort deployments should run faster (2-3 days each) because the template + dev process is now known.

---

## Status

- **Drafted:** ✅ 2026-05-14
- **Approved by Jim:** ✅ 2026-05-14
- **Pending:** Dev team WordPress deployment
- **Owner:** Chelsea to route to dev or coordinate deployment

Once deployed, update this file with deployment date + URLs of live pages for 30-day check-in.
