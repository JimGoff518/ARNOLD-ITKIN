# Hair Relaxer Pages — Dev Team Deployment Package

**Project:** Replicate Galaxy Gas template across Hair Relaxer mass tort (4 new city-targeted pages + Spanish bonus + schema add to existing Dallas page)
**Approved by:** Jim Goff 2026-05-14
**Estimated dev time:** 5-7 hours total (~1-1.5 hrs per new page + 30 min for schema-only update on existing Dallas page)
**Strategic rationale:** Project #2 in the niche mass tort replication sequence. Hair relaxer MDL 3060 has 11,440+ pending cases, $50K-$1.5M+ projected per case. Spanish page targets uncontested niche (NO Tier-S DFW competitor has Spanish mass-tort content).

---

## What's being deployed

| # | URL slug | Status | Target audience |
|---|---|---|---|
| 1 | `/houston-hair-relaxer-lawyer/` | **NEW** | Houston-area women (largest Black female population in Texas) |
| 2 | `/texas-hair-relaxer-lawyer/` | **NEW** | Statewide; military spouses, smaller metros, rural Texas |
| 3 | `/north-texas-hair-relaxer-lawyer/` | **NEW** | DFW suburbs (Plano, Frisco, Allen, McKinney, Arlington, Cedar Hill, DeSoto, etc.) |
| 4 | `/abogado-alisador-cabello-texas/` | **NEW** | Spanish-language; uncontested Latina niche |
| 5 | `/dallas/hair-relaxers/` | **SCHEMA ADD ONLY** | Existing page — add FAQPage JSON-LD schema; no content rewrite |

**Note on existing Dallas page:** Per Bill AI Machine "additive only" rule applied to gofflawdfw.com here too — do NOT rewrite the existing Dallas hair relaxer page content. Only ADD the FAQPage schema block. The existing ~2,200 words and FAQ-style content remain intact.

---

## Files in this package

| File | Purpose |
|---|---|
| `01-houston-hair-relaxer-lawyer.md` | New Houston page — full content, meta, FAQ block, internal linking |
| `02-texas-hair-relaxer-lawyer.md` | New Texas statewide page |
| `03-north-texas-hair-relaxer-lawyer.md` | New DFW suburbs page |
| `04-abogado-alisador-cabello-texas.md` | New Spanish-language page (Latina niche) |
| `SCHEMA-JSON-LD.md` | FAQPage + LegalService schema blocks for all 4 new pages + FAQPage for existing Dallas page |
| `DEPLOYMENT-PACKAGE.md` | This file — dev instructions |

---

## Step-by-step deployment instructions

### For each of the 4 NEW pages:

**Step 1 — Create the WordPress page**
1. WordPress admin → Pages → Add New
2. Set page title to match the H1 from the corresponding `.md` file
3. Set permalink slug to match the URL in the file header

**Step 2 — Paste the body content**
1. Copy everything from `## PAGE BODY` through the FAQ block
2. Paste into the WordPress page editor
3. Mark H2/H3 hierarchy per the source file
4. Keep all internal links exactly as written

**Step 3 — Configure Yoast SEO**
1. Yoast meta box: paste SEO title, meta description, focus keyword from `## METADATA` section
2. Canonical URL: confirm matches page slug

**Step 4 — Add the JSON-LD schema**
1. Open `SCHEMA-JSON-LD.md`
2. Find the section for this page
3. Copy BOTH the `<script type="application/ld+json">` blocks (FAQPage + LegalService)
4. Inject via Yoast Schema tab, Custom HTML block, or theme's custom-code feature
5. Validate with https://search.google.com/test/rich-results

**Step 5 — For the Spanish page specifically:**
1. Set the WordPress page language attribute to `es` (Spanish) if your theme/plugin supports it
2. In the `<head>` of the page, add these hreflang declarations:
   ```html
   <link rel="alternate" hreflang="es" href="https://gofflawdfw.com/abogado-alisador-cabello-texas/" />
   <link rel="alternate" hreflang="en" href="https://gofflawdfw.com/texas-hair-relaxer-lawyer/" />
   ```
3. Also add reciprocal hreflang declarations on the English `/texas-hair-relaxer-lawyer/` page:
   ```html
   <link rel="alternate" hreflang="en" href="https://gofflawdfw.com/texas-hair-relaxer-lawyer/" />
   <link rel="alternate" hreflang="es" href="https://gofflawdfw.com/abogado-alisador-cabello-texas/" />
   ```
4. The schema for the Spanish page has `"inLanguage": "es"` and `"availableLanguage": ["es", "en"]` — preserve those exactly

**Step 6 — Publish**
1. Publish status = Published
2. Clear cache
3. Verify URL loads
4. Test on mobile

### Repeat steps 1-6 for all 4 NEW pages.

### For the EXISTING Dallas page (`/dallas/hair-relaxers/`):

**Schema-only update (no content changes):**

1. Navigate to the existing Dallas hair relaxer page in WordPress admin
2. Add the FAQPage schema block from `SCHEMA-JSON-LD.md` (the "EXISTING DALLAS PAGE — Schema add-on" section)
3. Inject via Yoast Schema tab OR a Custom HTML block at the page bottom
4. Validate with Google's Rich Results Test
5. **Important:** Verify the FAQ questions in the schema match the actual FAQ-style questions in the existing page content. If any differ, edit the schema to match the actual page content verbatim (Google penalizes FAQ schema that doesn't match visible page content).

---

## Verification checklist (after all 5 pages updated)

Visit each URL in a fresh browser (logged out) and confirm:

- [ ] `gofflawdfw.com/houston-hair-relaxer-lawyer/` — loads, H1 visible, FAQ block visible, phone 972-928-0085 visible
- [ ] `gofflawdfw.com/texas-hair-relaxer-lawyer/` — same checks
- [ ] `gofflawdfw.com/north-texas-hair-relaxer-lawyer/` — same checks
- [ ] `gofflawdfw.com/abogado-alisador-cabello-texas/` — same checks, Spanish content rendering correctly, hreflang in `<head>`
- [ ] `gofflawdfw.com/dallas/hair-relaxers/` — existing content unchanged, NEW schema block present in source
- [ ] View source on each — confirm `<title>`, `<meta name="description">`, AND JSON-LD `<script>` blocks
- [ ] Run each through https://search.google.com/test/rich-results — FAQPage schema validates without errors
- [ ] Internal links between all 5 hair relaxer pages work
- [ ] Mobile rendering — content readable, Spanish page renders cleanly
- [ ] PageSpeed Insights — no regression

---

## Cross-linking from existing pages (after deploy)

To boost the new pages' authority, add cross-links from EXISTING pages within 1 week:

**Homepage (`gofflawdfw.com/`):**
- "Practice Areas" menu: "Hair Relaxer Cancer Lawsuits" → link to `/dallas/hair-relaxers/`

**Existing Dallas hair relaxer page (`/dallas/hair-relaxers/`):**
- Add to "Related" / "Other Service Areas" section: links to all 4 new pages (Houston, Texas, North Texas, Spanish)

**Product Liability page:**
- Reference hair relaxer as a current product liability mass tort → link

**Catastrophic Injury page:**
- Reference cancer cases including hair relaxer → link

**Wrongful Death page:**
- Reference hair relaxer cancer death claims → link

**Galaxy Gas page:**
- "Related Mass Torts" section: link to hair relaxer

**AFFF pages (when deployed):**
- "Related Mass Torts" section: link to hair relaxer pages

---

## Sitemap submission

After deployment:
1. **WordPress XML sitemap** — Yoast auto-adds new pages. Verify at `gofflawdfw.com/sitemap_index.xml`
2. **Google Search Console** — Inspect URL → Request Indexing for each of the 4 NEW pages
3. **Bing Webmaster Tools** — same submission

---

## What this deployment ACCOMPLISHES strategically

| Goal | Mechanism |
|---|---|
| **Replicate Galaxy Gas SERP success** | Same template that ranks 4 of top 10 for Galaxy Gas, applied to hair relaxer |
| **Revenue defense post-Aldous referral loss** | Hair relaxer cases project $50K-$1.5M+ per case = serious revenue per signed case |
| **Federal preemption (Texas tort caps don't apply)** | MDL 3060 is federal — bypasses Texas $250K non-economic cap |
| **AI Overview / featured snippet eligibility** | FAQ schema on all 5 pages (including existing Dallas) |
| **No PPC required** | Pure organic SEO; aligns with locked strategy |
| **Spanish niche entry — UNCONTESTED** | Zero Tier-S DFW competitors have Spanish mass-tort content. First-mover advantage. |
| **High-value cases only** | $50K-$1.5M+ per case (much higher than AFFF's $20K-$600K) |
| **Settlement timing tailwind** | Most likely global settlement late 2026 — claims filed now participate in early settlement waves |

---

## Why the Spanish page is the secret weapon

Every other DFW PI competitor profiled (Reyes, Mullen, Witherite, Hamilton Wingo, Lyons & Simmons, McCraw, Aldous, Thompson Law, Snellings, J. Alexander) has zero Spanish mass-tort pages. Several have Spanish PI pages (Reyes, Thompson, McCraw, Lyons & Simmons, Hamilton Wingo intake) but NONE target Spanish-speaking Latina hair relaxer cancer claimants.

This is the single most defensible niche in the entire DFW PI competitive landscape:
- Latina chemical hair relaxer use is real and historically underrepresented in litigation marketing
- Spanish language + hair relaxer + Texas geography = empty SERP
- Even modest organic traffic (5-20 qualified leads per year) = 2-5 signed cases at $50K-$500K fees per case = $100K-$2.5M revenue annually

If even one in five queries from this niche becomes a signed case, the Spanish page alone justifies the entire Project #2 deployment.

---

## Expected timeline to results

- **Week 1:** Pages live, indexed, schema validated
- **Weeks 2-4:** Google crawls + ranks; long-tail hair relaxer queries appear in GSC impressions
- **Months 2-3:** Featured snippet / AI Overview citations surface for FAQ questions
- **Months 3-6:** First hair relaxer inquiries from organic search likely arrive
- **Months 6-12:** Full SERP positioning established
- **Late 2026:** Global MDL 3060 settlement expected → spike in cases qualifying for early settlement tier

---

## Future expansion (Project #3 candidates)

After hair relaxer pages are live and indexed, the same template applies to:

| Mass tort | Why next | Federal MDL? |
|---|---|---|
| **Tepezza (hearing loss)** | Horizon Therapeutics manufacturer; thousands of plaintiffs | Yes — N.D. Illinois MDL 3079 |
| **Paragard IUD fragmentation** | Active MDL; women's reproductive product (synergy with hair relaxer page audience) | Yes — N.D. Georgia MDL 2974 |
| **Suboxone tooth decay** | Newer MDL; growing | Yes — S.D. Ohio MDL 3092 |
| **Social media addiction (Meta MDL)** | Families of teens with mental health injury | Yes — N.D. California MDL 3047 |
| **AI Liability (emerging)** | First-mover niche, no incumbents | Not yet centralized |

Each future project follows the same template: 4 city-targeted pages + 1 Spanish page (where audience demographics support it) + FAQ schema + LegalService schema. After two successful deployments (AFFF + Hair Relaxer), subsequent projects should run faster.

---

## Status

- **Drafted:** ✅ 2026-05-14
- **Approved by Jim:** ✅ 2026-05-14
- **Pending:** Dev team WordPress deployment
- **Owner:** Chelsea to route to dev or coordinate deployment

Once deployed, update this file with deployment date + URLs for 30-day check-in.
