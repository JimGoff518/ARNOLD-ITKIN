# Goff Law — Master Fix-It List

**For:** Chelsea (COO) and the Goff Law web dev team
**From:** Jim Goff, based on the full SEO + UX audit completed 2026-05-12 (overnight) plus prior recon
**Updated:** 2026-05-13
**Live web version:** `https://gofflawsuperagent.up.railway.app/fixit` (after this commit deploys)
**Source of truth:** This consolidates every actionable finding from the 12 audit artifacts in `recon/goff-law/`. Read this list to know what to do; open the individual artifacts only if you need supporting detail.

---

## 30-second summary

The audit looked at **176 URLs across gofflawdfw.com**, deep-crawled **74 representative pages**, ran **12 live Google SERP queries**, audited schema markup, meta tags, technical hygiene, content depth, geographic coverage, and visual UX, and compared everything to verified competitor data on Thompson Law / Mullen & Mullen + 8 newly-discovered competitors.

**The good news:**
- Goff Law has the **strongest brand voice in DFW PI marketing** (3rd-generation Texan, former insurance defense attorney — no competitor can match this)
- Goff Law has a **dominant SERP position for Galaxy Gas / nitrous oxide injury** (4 of top 10 results = Goff pages)
- Goff Law has a **first-mover advantage** on emerging-litigation niches Thompson + Mullen don't touch (AFFF, Tepezza, PFAS, AI Liability, Suboxone, hair relaxers, Amazon truck, electric scooter, sexual assault civil claims)

**The bad news:**
- The SEO foundation has critical leaks: missing schema markup, multi-H1 theme bug on 65% of pages, no `og:image` on 70% of pages, no consolidated review display
- Zero pages for **32 DFW cities** including the wealthy north suburbs (Plano, Frisco, Allen, McKinney) AND Fort Worth (1M population)
- 9 newly-discovered competitors (Hamilton Wingo, Lyons & Simmons, Aldous, Patterson, etc.) ranking ahead of Goff on commercial-intent queries

**What this list does:** Tells you exactly what to fix, who owns each fix, how long it takes, what it costs, and how to verify it worked.

---

## 📅 Suggested rollout calendar

| Week | Focus | Owner | Effort |
|---|---|---|---|
| **Week 1 (this week)** | Gather inputs + fix theme bugs + deploy sitewide schema | Chelsea (data gathering) + WP dev (code) | ~15 hr |
| **Week 2** | AggregateRating + Hero replacement + Contact form fix | WP dev | ~15 hr |
| **Week 3** | FAQPage + Service + Attorney + Offer schema | WP dev + content writer | ~12 hr |
| **Week 4** | Meta-tag cleanup + Crisp Chat fix + W3TC config | WP dev + content writer | ~8 hr |
| **Month 2 (Weeks 5-8)** | Suburb hub builds: Frisco, Plano | Content writer + WP dev | ~80 hr |
| **Month 2 (Weeks 5-8)** | Replicate Galaxy Gas template across 5 more mass torts | Content writer | ~30 hr |
| **Month 3 (Weeks 9-12)** | Suburb hubs: Allen + McKinney + Fort Worth + start Workers' Comp | Content writer + WP dev | ~120 hr |
| **Q2 (Months 4-6)** | Run recon on 8 new competitors; deploy LocalBusiness + advanced schema; mobile UX optimization | Claude + WP dev | ~60 hr |
| **Q3-Q4 (Months 7-12)** | Spanish-language content track; blog cadence to 200+ posts; backlink building | Bilingual writer + SEO specialist or agency | ongoing |

---

## ⚡ THIS WEEK — Quick wins (~20 hours, ~$0-2K)

Status legend: ☐ = not started · 🟡 = in progress · ✅ = done

| ☐ | # | Item | Owner | Effort | Impact | Verify |
|---|---|---|---|---|---|---|
| ☐ | 1 | Gather "Inputs Needed" checklist (below) | **Chelsea** | 1-2 hr | 🚨 BLOCKER | Email sent to dev |
| ☐ | 2 | Fix multi-H1 theme bug (48 of 74 pages affected) | **WP dev** | 1-3 hr | 🔥 HIGH | `document.querySelectorAll('h1').length === 1` on any page |
| ☐ | 3 | Deploy sitewide `LegalService` schema (Block 1) | **WP dev** | 1 hr | 🔥 HIGH | Validator.schema.org returns clean |
| ☐ | 4 | Deploy `AggregateRating` + 3-5 `Review` blocks on homepage | **WP dev + Chelsea** | 2 hr | 🔥 HIGH | Google Rich Results Test shows star rating eligibility |
| ☐ | 5 | Set Yoast site-wide default `og:image` | **WP dev/Chelsea** | 30 min | MED-HIGH | Facebook Sharing Debugger shows image |
| ☐ | 6 | Write meta descriptions for 8 pages missing them | **Chelsea/writer** | 30-45 min | MED | Yoast bulk editor shows no missing desc |
| ☐ | 7 | Replace empty homepage hero (use `HERO-FIX-DRAFT.md` spec) | **WP dev** | 4-8 hr | 🔥 HIGH | Above-the-fold has: specific case result + trust badges + form OR phone CTA |
| ☐ | 8 | Move contact form ABOVE the fold on /contact | **WP dev** | 1-2 hr | HIGH | Form is first visible element on /contact |
| ☐ | 9 | Configure W3 Total Cache HTML caching (max-age 5min) | **WP dev** | 30 min | MED | `curl -I` returns Cache-Control with non-zero max-age |
| ☐ | 10 | Make Crisp Chat visible from page load | **WP dev** | 30 min | MED | Chat bubble visible on homepage without scroll |

**Subtotal:** ~12-19 hours of dev + content + Chelsea time. Achievable in one workweek.

**Cost estimate:**
- If existing WP dev is on retainer → essentially $0 incremental
- If hiring freelance specialist for one-shot → $1,500-2,000 (~$100-150/hr × 15 hours)
- Recommended freelancers: Codeable.io (vetted WP devs), WPMU DEV pros, or local Dallas WordPress freelancers via Upwork

---

## 📋 INPUTS NEEDED FROM JIM/CHELSEA (Week 1 Blocker)

**Without these, schema deployment cannot start.** Chelsea — gather these and send to the dev team in a single email.

### Review data (for AggregateRating schema)

- [ ] **Verified Google Business Profile review count** (exact number as of today)
- [ ] **Verified Google average rating** (e.g., 4.8)
- [ ] **3-5 verbatim 5-star reviews** with:
  - Reviewer's first name + last initial (e.g., "Sarah M.")
  - Date posted (YYYY-MM-DD)
  - Full review text (copy verbatim — do NOT edit)
- [ ] **Avvo rating + review count** (if Goff has an Avvo profile)
- [ ] **Trustpilot rating + review count** (if applicable)

> 🚨 **CRITICAL:** Schema review data MUST match real review platforms. Inventing numbers triggers Google manual penalties. Use ONLY Google Business Profile (and optionally Avvo) verified data.

### Firm + attorney data (for LegalService + Attorney schema)

- [ ] **Office address confirmation** (per SERP audit: 12720 Hillcrest Rd, Suite 1045, Dallas, TX 75230 — confirm still current)
- [ ] **Office hours** (e.g., "M-F 9:00am-5:00pm; phones answered 24/7")
- [ ] **Founding year** (per SERP audit: 2023 — confirm)
- [ ] **Jim Goff's bar admission state(s)** (Texas + others?)
- [ ] **Jim Goff's bar admission year** (e.g., "Admitted: 2008")
- [ ] **Jim Goff's law school + graduation year**
- [ ] **Jim Goff's undergraduate school + graduation year**
- [ ] **Jim Goff's professional headshot URL** (hosted on the WP site)
- [ ] **Awards/credentials confirmed list** — we have: Top 40 Under 40, Super Lawyers, Best Lawyers in America. Anything else?
- [ ] **List of all other attorneys at the firm** (if any) — each needs their own Attorney schema block

### Media + social

- [ ] **Logo image URL** (PNG with transparent background, hosted on WP)
- [ ] **Office photo URL** (exterior or interior, used for OG sharing fallback)
- [ ] **Facebook page URL**
- [ ] **LinkedIn page URL**
- [ ] **X/Twitter URL** (if used)
- [ ] **YouTube channel URL** (if used)
- [ ] **Instagram URL** (if used)
- [ ] **TikTok URL** (if used)

### Contact

- [ ] **Primary phone** (confirmed: 972-928-0085)
- [ ] **Secondary phone** (if any vanity number)
- [ ] **Primary email** for the firm
- [ ] **Spanish-speaking contact info** (if applicable)

### Practice areas (for Service schema)

- [ ] **Definitive list of practice areas Goff handles.** Mark each as Primary (heavy focus), Secondary (we take these but don't promote), or Decline (we don't take these). Draft list from audit:
  - Car accident
  - Truck accident
  - Motorcycle accident
  - Pedestrian accident
  - Rideshare (Uber/Lyft)
  - Wrongful death
  - Premises liability / slip & fall
  - Dog bite
  - Brain injury / TBI
  - Spinal cord injury
  - Catastrophic injury
  - Drunk driving
  - Sexual assault (civil)
  - Nursing home abuse
  - Medical malpractice
  - Workers' comp / workplace injury
  - Electric scooter
  - Amazon truck
  - Galaxy Gas / nitrous oxide
  - Mass tort (general)
  - AFFF firefighting foam
  - PFAS / chemical exposure
  - Tepezza
  - Paragard
  - AI liability
  - Suboxone
  - Hair relaxer
  - Video game addiction
  - Privacy / emotional distress

> **Chelsea — gather these 40 items into one email + send to the dev team. Until they have this data, schema work stalls.**

---

## 🟦 FOR THE DEV TEAM — Technical fixes (in priority order)

### P0 — This week

### 1. Fix the multi-H1 theme bug (the single most important SEO fix)

**What's wrong:** 48 of 74 pages have 2 or 3 `<h1>` tags. WordPress theme is emitting BOTH the site title in the header AND the page title in the content as `<h1>`. Google guidelines explicitly say one H1 per page.

**Where the bug likely lives:**
- `wp-content/themes/{theme-name}/header.php`
- `wp-content/themes/{theme-name}/template-parts/site-header.php` (if a parts file exists)
- Or in a header.php section that uses something like `<h1 class="site-title">{site name}</h1>`

**The fix:**

```php
// BEFORE (current — wrong):
<h1 class="site-title">
  <a href="<?php echo home_url(); ?>"><?php bloginfo('name'); ?></a>
</h1>

// AFTER (correct — site title becomes a clickable link, not an H1):
<?php if ( is_front_page() ) : ?>
  <h1 class="site-title">
    <a href="<?php echo home_url(); ?>"><?php bloginfo('name'); ?></a>
  </h1>
<?php else : ?>
  <div class="site-title">
    <a href="<?php echo home_url(); ?>"><?php bloginfo('name'); ?></a>
  </div>
<?php endif; ?>
```

This keeps the homepage's H1 = site name (correct for the homepage) but uses a `<div>` (or `<a>`) on every other page so the content area's H1 is the only one.

**Verification:**
1. Open any practice-area page (e.g., `/cedar-hill/truck-accident-lawyer/`)
2. Open Chrome DevTools console
3. Run: `document.querySelectorAll('h1').length`
4. Expected result: `1`
5. Repeat on 3-4 random other pages to confirm.

**Effort:** 1-3 hours.
**Source:** `recon/goff-law/03-meta-tags-audit.md`

---

### 2. Deploy sitewide `LegalService` schema (Block 1)

**Where to deploy:** Inject sitewide via theme `header.php` so it appears in every page's `<head>`. Place inside the `<head>` element, before `</head>`.

**Code template** — from `recon/goff-law/08-schema-implementation-guide.md` Block 1. Replace `{{TOKENS}}` with values from Chelsea's email.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LegalService",
  "@id": "https://gofflawdfw.com/#legalservice",
  "name": "Goff Law, PLLC",
  "alternateName": "Goff Law",
  "url": "https://gofflawdfw.com/",
  "logo": "https://gofflawdfw.com/{{PATH_TO_LOGO}}",
  "image": "https://gofflawdfw.com/{{PATH_TO_OFFICE_OR_LOGO_IMAGE}}",
  "description": "Dallas-Fort Worth personal injury law firm founded by Jim Goff. Former insurance defense attorney now fighting for injured Texans. Focus on Galaxy Gas/nitrous oxide injuries, mass tort, truck accidents, sexual assault civil claims, and emerging litigation.",
  "telephone": "+1-972-928-0085",
  "email": "{{EMAIL}}",
  "priceRange": "Free consultation · Contingency fee",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "12720 Hillcrest Rd, Suite 1045",
    "addressLocality": "Dallas",
    "addressRegion": "TX",
    "postalCode": "75230",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "32.9143",
    "longitude": "-96.7836"
  },
  "openingHoursSpecification": [{
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": ["Monday","Tuesday","Wednesday","Thursday","Friday"],
    "opens": "{{e.g., 09:00}}",
    "closes": "{{e.g., 17:00}}"
  }],
  "founder": {
    "@type": "Person",
    "name": "Jim Goff",
    "url": "https://gofflawdfw.com/{{ATTORNEY_BIO_PATH}}"
  },
  "foundingDate": "2023",
  "areaServed": [
    {"@type":"City","name":"Dallas"},
    {"@type":"City","name":"Fort Worth"},
    {"@type":"City","name":"Plano"},
    {"@type":"City","name":"Frisco"},
    {"@type":"City","name":"Allen"},
    {"@type":"City","name":"McKinney"},
    {"@type":"City","name":"Arlington"},
    {"@type":"City","name":"Garland"},
    {"@type":"City","name":"Irving"},
    {"@type":"City","name":"Cedar Hill"},
    {"@type":"City","name":"DeSoto"},
    {"@type":"AdministrativeArea","name":"Dallas-Fort Worth metroplex"},
    {"@type":"AdministrativeArea","name":"East Texas"},
    {"@type":"AdministrativeArea","name":"Texas"}
  ],
  "sameAs": [
    "{{FACEBOOK_URL}}",
    "{{LINKEDIN_URL}}",
    "{{X_TWITTER_URL}}",
    "{{YOUTUBE_URL}}",
    "https://profiles.superlawyers.com/texas/dallas/lawyer/james-goff/39e7f6d6-79f6-48f8-b016-9da49543abc7.html",
    "https://www.bestlawyers.com/lawyers/jim-goff/328523",
    "https://www.bestlawyers.com/firms/goff-law-pllc/101311/US",
    "https://www.texasbar.com/AM/Template.cfm?Section=Find_A_Lawyer&template=/Customsource/MemberDirectory/MemberDirectoryDetail.cfm&ContactID=343650",
    "https://lawyers.justia.com/lawyer/jim-goff-1670096",
    "https://lawyers.findlaw.com/texas/dallas/5194263_1/"
  ],
  "knowsAbout": [
    "Personal Injury Law","Car Accidents","Truck Accidents","Motorcycle Accidents",
    "Wrongful Death","Premises Liability","Catastrophic Injury","Brain Injury",
    "Galaxy Gas / Nitrous Oxide Injuries","Mass Tort Litigation",
    "AFFF Firefighting Foam","PFAS Chemical Exposure","Tepezza","Paragard",
    "Sexual Assault Civil Claims","Electric Scooter Accidents","Amazon Truck Accidents"
  ]
}
</script>
```

**Deployment paths in WordPress (pick one):**
- **A. Yoast SEO Organization settings** — easiest, but Yoast doesn't expose every field above. Will cover the basics; for full control use B or C.
- **B. Direct theme injection** — paste the block inside `<head>` in `header.php`. Lowest dependency.
- **C. Schema plugin** — Schema Pro, Rank Math, or WPSSO. Adds a UI for managing this.

**Recommended:** Option B (direct theme injection) — gives you the full block above with no plugin dependency.

**Validation steps after deploy:**
1. View source on the homepage and confirm the script block is present in `<head>`
2. Paste the homepage URL into https://validator.schema.org/ — should return no errors
3. Paste into https://search.google.com/test/rich-results — should show "Page is eligible for rich results"
4. Submit homepage URL to Google Search Console → URL inspection → "Request indexing"

**Effort:** 1 hour after inputs are gathered.

---

### 3. Deploy `AggregateRating` + 3-5 `Review` blocks on homepage (Block 2)

**Where:** Homepage `<head>` only (NOT sitewide). Add as a separate `<script type="application/ld+json">` block.

**Code template:**

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LegalService",
  "@id": "https://gofflawdfw.com/#legalservice",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "{{e.g., 4.8}}",
    "reviewCount": "{{e.g., 47}}",
    "bestRating": "5",
    "worstRating": "1"
  },
  "review": [
    {
      "@type": "Review",
      "author": {"@type":"Person","name":"{{Reviewer 1 first name + last initial}}"},
      "datePublished": "{{YYYY-MM-DD}}",
      "reviewRating": {"@type":"Rating","ratingValue":"5","bestRating":"5"},
      "reviewBody": "{{Verbatim review text from Google}}"
    },
    {
      "@type": "Review",
      "author": {"@type":"Person","name":"{{Reviewer 2}}"},
      "datePublished": "{{YYYY-MM-DD}}",
      "reviewRating": {"@type":"Rating","ratingValue":"5","bestRating":"5"},
      "reviewBody": "{{Verbatim review text}}"
    }
    // Add 3-5 total reviews
  ]
}
</script>
```

**Critical compliance:**
- Use ONLY real review data from Google Business Profile
- ratingValue MUST match Google's displayed average exactly
- reviewCount MUST match Google's displayed total exactly
- Review names + dates + text MUST be verbatim from Google
- Refresh the schema if review count changes by 5+ (e.g., quarterly)

**Validation:** Same as Block 1 — schema.org validator + Google Rich Results Test.

**Effort:** 2 hours after Chelsea provides review data.

---

### 4. Replace the empty homepage hero

**Current state:** Hero just says "MILLIONS WON / SERIOUS INJURIES, SERIOUS RESULTS." with no specific case result, no trust badges, no review count, no lead form.

**Full implementation spec:** `recon/goff-law/HERO-FIX-DRAFT.md` (or http://gofflawdfw.com/{your-spec-location})

**Summary of the new hero (above the fold on desktop, stacked on mobile):**

```
┌────────────────────────────────────────────────────────────────────┐
│ [Galaxy Gas FDA news ticker — KEEP, this is a Goff strength]     │
├────────────────────────────────────────────────────────────────────┤
│ [Goff logo]              [phone icon] (214) GOFF-LAW    [MENU]   │
│                          Free Consultation · 24/7                  │
├────────────────────────────────────────────────────────────────────┤
│  HEADLINE LEFT COLUMN          │   LEAD FORM (right column)        │
│                                │                                   │
│  A Dallas Personal Injury      │   Tell us about your case        │
│  Lawyer Who Knows How          │   [First Name] [Last Name]        │
│  Insurance Companies Think     │   [Phone     ] [Zip Code ]        │
│                                │   [Email                ]         │
│  Former insurance defense      │   [What happened?       ]         │
│  attorney now fighting for     │   ☐ Text me updates (TCPA)        │
│  injured Texans.               │   [ GET MY FREE REVIEW → ]        │
│                                │   100% confidential. No fee       │
│  $XX MILLION recovered         │   unless we win your case.        │
│  for North Texas families      │                                   │
│                                │                                   │
│  [BBB] [Avvo] [SuperLawyers]   │                                   │
│  ★★★★★  4.8 from 47 Reviews                                       │
└────────────────────────────────────────────────────────────────────┘
```

**Recommended headline (4 options to choose from):**
- **A. "A Dallas Personal Injury Lawyer Who Knows How Insurance Companies Think"** ⭐ RECOMMENDED — leverages Jim's unique former-defense-attorney angle. No competitor can claim this.
- **B. "A Third-Generation Texan Fighting for Injured Dallasites"** — leverages the "local" angle (note: Mullen also claims local, so this is less differentiated)
- **C. "Born in Dallas. Trained by Insurance Defense. Now Fighting for You."** — hybrid of A + B
- **D. "Out-of-Town Lawyers Don't Know Dallas. We Do."** — aggressive challenge tone

**Effort:** 4-8 hours. Most of the time is form integration + responsive testing.

**Form integration:** Wire to existing CRM (whatever Goff currently uses — Lawmatics? Salesforce? HubSpot? Custom?) AND optionally trigger SMS auto-response if SMS opt-in checkbox is checked.

**Acceptance checklist (Tier 0 hero deploy):**
- [ ] Above-the-fold on desktop (1440×900): form is fully visible
- [ ] Above-the-fold on mobile (375×667): headline + first 2 form fields visible
- [ ] All trust badges render (no broken images)
- [ ] Specific case result dollar amount displayed
- [ ] Aggregate review count + star rating visible
- [ ] Form submits successfully and lands in CRM
- [ ] SMS opt-in field captured separately for TCPA audit
- [ ] Auto-responder email fires within 60 seconds
- [ ] Crisp Chat bubble visible from page load
- [ ] Page Speed Insights mobile score does NOT regress vs current baseline
- [ ] No layout breakage on iPhone SE (smallest common viewport)

---

### 5. Move contact form ABOVE the fold on /contact

**Current state:** `/contact` page shows a giant gray banner that just says "CONTACT" above the fold. Form is below.

**Fix:** Reorder the page template so the form is the FIRST thing visible when /contact loads. The banner can stay smaller (200px header strip) or be removed entirely.

**Effort:** 1-2 hours.

---

### 6. Set Yoast site-wide default `og:image`

**Path:** WP Admin → Yoast SEO → Settings → Site basics → "Default social image"

**Recommended image specs:**
- Size: 1200×630 pixels (Facebook/X/LinkedIn standard)
- Format: PNG or JPG
- Content: Logo + tagline + brand color OR a professional photo of Jim with the firm name overlay
- File size: under 200KB ideally

**Effect:** This single setting covers all 52 pages currently missing an og:image. Social sharing previews (Facebook, LinkedIn, Slack, Discord, etc.) will now show a thumbnail.

**Verification:** Use https://developers.facebook.com/tools/debug/ — paste any URL that was missing og:image. Should now show the default.

**Effort:** 30 minutes (5 minutes for the Yoast setting; 25 minutes if you need to create the image).

---

### 7. Configure W3 Total Cache HTML caching

**Path:** WP Admin → Performance → Page Cache

**Settings to change:**
- Page cache enabled: ✓ Yes
- Cache method: Disk: Enhanced (preferred)
- Cache front page: ✓
- Cache feeds: ✓
- "Don't cache pages for logged-in users": ✓
- Page cache lifetime: **300 seconds (5 minutes)** for HTML

**Why:** Currently `Cache-Control: max-age=0` means every page hit goes to PHP/DB. With 5-min caching, repeat visitors get instant responses and your server load drops dramatically.

**Verification:**
```bash
curl -sI https://gofflawdfw.com/ | grep -i cache-control
# Expected: cache-control: max-age=300, public  (or similar)
```

**Effort:** 30 minutes + 1 hour of testing to confirm no stale-content issues.

---

### 8. Make Crisp Chat visible from page load

**Path:** Crisp Dashboard → Settings → Chatbox

**Settings:**
- "Show chatbox on every page": ✓
- "Show immediately (no delay)": ✓ — important, currently it's not showing above the fold
- Position: bottom-right
- Welcome message: "Hi — got a question about your accident? Chat with us, no commitment."
- Match brand colors (Goff yellow accent if possible)

**Verification:** Open homepage in incognito. Chat bubble should be visible in lower-right within 2 seconds of page load.

**Effort:** 30 minutes.

---

### P1 — This month

### 9. Deploy `FAQPage` schema across all practice-area pages

**Where to deploy:** Each practice-area page that has FAQ-shaped content in the body (most do — verified during URL inventory).

**Approach:**
1. Open the page in WordPress edit mode
2. Find the FAQ-shaped content (usually a "Frequently Asked Questions" H2 followed by Q/A pairs)
3. Extract 5-8 Q/A pairs verbatim
4. Use Block 5 from `08-schema-implementation-guide.md` as the template
5. Replace `{{Q1}}/{{A1}}` etc. with the verbatim content
6. Paste the resulting JSON-LD block into the page's `<head>` (via Yoast custom field, Schema plugin, or theme hook)

**Critical:** FAQ content MUST be visibly on the page. Marking up content that isn't visible can trigger a Google manual penalty.

**Effort:** 6-12 hours total (most time is content writing/finding Q/A pairs on pages that don't have them yet).

**Block 5 template:**

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How long do I have to file a personal injury lawsuit in Texas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "In Texas, the statute of limitations for most personal injury claims is two years from the date of the injury. Wrongful death claims also follow a two-year statute of limitations from the date of death."
      }
    },
    {
      "@type": "Question",
      "name": "{{Q2 — lift from existing page content}}",
      "acceptedAnswer": {"@type":"Answer","text":"{{A2}}"}
    }
    // ... continue for 5-8 total Q/A pairs
  ]
}
</script>
```

**Common PI FAQ topics (use if pages lack their own):**
- "How much is my case worth?"
- "How long will my case take?"
- "Do I have to go to court?"
- "What if the insurance company offers me a settlement before I call a lawyer?"
- "What does a contingency fee mean?"
- "How quickly should I call a lawyer after an accident?"
- "What if I'm partially at fault for the accident?"
- "What evidence should I gather after my accident?"

---

### 10. Deploy `Service` schema on top 5 practice-area pages (Block 4)

Start with: car-accident, truck-accident, wrongful-death, premises-liability, Galaxy Gas. Expand to more pages later.

**Block 4 template** (one per practice-area page):

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Service",
  "@id": "https://gofflawdfw.com/{{PAGE_URL_PATH}}#service",
  "serviceType": "Legal Representation — {{PRACTICE_AREA}}",
  "name": "{{e.g., Dallas Car Accident Lawyer Service}}",
  "description": "{{e.g., Comprehensive legal representation for Dallas car accident victims. No fee unless we win.}}",
  "provider": {"@id": "https://gofflawdfw.com/#legalservice"},
  "areaServed": [
    {"@type":"City","name":"{{e.g., Dallas}}"},
    {"@type":"AdministrativeArea","name":"Dallas-Fort Worth metroplex"}
  ],
  "offers": {
    "@type": "Offer",
    "price": "0",
    "priceCurrency": "USD",
    "description": "Free initial consultation · Contingency fee"
  }
}
</script>
```

**Effort:** 2-3 hours for the top 5.

---

### 11. Deploy `Attorney` schema for Jim Goff bio page (Block 3)

Block 3 template is in `08-schema-implementation-guide.md`. Needs bar admission year + law school + photo URL from Chelsea's checklist.

**Effort:** 1-2 hours.

---

### 12. Deploy `Offer` schema for free consultation (Block 6)

**Where:** Homepage + /contact page.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Offer",
  "name": "Free Personal Injury Case Consultation",
  "description": "Confidential, no-obligation consultation. No fee unless we win.",
  "url": "https://gofflawdfw.com/contact/",
  "price": "0",
  "priceCurrency": "USD",
  "availability": "https://schema.org/InStock",
  "seller": {"@id": "https://gofflawdfw.com/#legalservice"}
}
</script>
```

**Effort:** 30 minutes.

---

### 13. Write meta descriptions for 8 pages missing them

**Specifically the 8 pages:**

| Page | Suggested meta desc (you can edit) |
|---|---|
| `/dallas-personal-injury-lawyer` | Dallas personal injury lawyer Jim Goff fights insurance companies for injured Texans. Free consultation, no fee unless we win. Call (972) 928-0085. |
| `/dallas-personal-injury-lawyer/catastrophic-injury` | Dallas catastrophic injury attorney for brain, spinal cord, and severe injury cases. Former defense attorney now fighting for victims. Free consult. |
| `/dallas-personal-injury-lawyer/catastrophic-injury/spinal-cord-injury-attorney` | Dallas spinal cord injury lawyer at Goff Law. Experienced in catastrophic SCI cases. No fee unless we win. Call (972) 928-0085 for a free review. |
| `/dallas-personal-injury-lawyer/medical-malpractice` | Dallas medical malpractice attorney for misdiagnosis, surgical errors, and birth injuries. Free consultation. No fee unless we win your case. |
| `/dallas-personal-injury-lawyer/nursing-home-abuse` | Dallas nursing home abuse lawyer protects elderly victims of neglect, abuse, and wrongful death. Free, confidential consultation. (972) 928-0085. |
| `/dallas-personal-injury-lawyer/premises-liability` | Dallas premises liability attorney for slip and fall, inadequate security, and dangerous property cases. No fee unless we win. Free consultation. |
| `/dallas/.../dallas-lyft-attorney` | Dallas Lyft accident attorney for injured rideshare passengers and drivers. Goff Law handles complex insurance claims. Free consultation 24/7. |
| `/dallas/.../uber-accident` | Dallas Uber accident lawyer for injured rideshare passengers and drivers. Free case review. No fee unless we win. Call (972) 928-0085. |

**Format rules:**
- 120-155 characters total
- Include city + practice area + at least one of: phone, "free consultation", or "no fee unless we win"
- Avoid keyword-stuffing

**Effort:** 30-45 minutes for all 8.

---

### 14. Trim 40 oversized meta descriptions

These get truncated in SERP. Better to rewrite them at the right length.

**Approach:**
1. Open Yoast bulk editor (WP Admin → Yoast SEO → Tools → Bulk editor)
2. Filter to descriptions over 160 chars
3. Trim each to ≤155 chars while preserving the most important hook

**Effort:** 2 hours.

---

### 15. Add SMS opt-in to lead form (TCPA-compliant)

**Required UI:**

```html
<label>
  <input type="checkbox" name="sms_optin">
  <span>Text me updates about my case. By checking this, I consent to receive
  text messages from Goff Law about my case. Message and data rates may apply.
  Reply STOP to opt out.</span>
</label>
```

**Backend wiring:**
- Capture SMS opt-in state separately in CRM (TCPA audit requirement: must be able to prove the user actively opted in)
- If checked: trigger SMS within 60 seconds via Twilio or whatever SMS provider Goff uses
- Sample auto-SMS: *"Hi [first name], it's the team at Goff Law. We got your message about your case. Calling you shortly. — Reply STOP to opt out."*

**Effort:** 4-6 hours including SMS provider setup.

**Vendor recommendations:**
- Twilio (~$0.0075/SMS, technical setup required)
- SimpleTexting (~$25/mo for 500 SMS, easy UI)
- Lawmatics (if Goff uses Lawmatics for intake, it has SMS built-in)
- Lead Docket (similar — PI-firm-specific)

---

### 16. Add `loading="lazy"` and `srcset` to images

**Current state:** 35 images on homepage. ZERO use lazy loading or srcset.

**Quick fix:** WordPress 5.5+ auto-adds `loading="lazy"` to images BUT only if the theme uses `the_post_thumbnail()` and similar functions. If the theme uses raw `<img>` tags, lazy loading won't fire.

**Approach:**
1. Audit the theme files for raw `<img>` tags
2. Replace with `the_post_thumbnail()` or `wp_get_attachment_image()` where possible
3. For unavoidable raw `<img>` tags, manually add `loading="lazy"` (except for above-the-fold images, which should NOT be lazy)
4. Ensure responsive images are emitted via `srcset` (WordPress does this automatically if `wp_calculate_image_srcset` is enabled)

**Verification:**
- Open any practice page in DevTools → Network tab
- Throttle to "Slow 3G"
- Reload — below-the-fold images should not load until scrolled into view
- Check the `<img>` tags in DOM — should have `srcset="..."` with multiple sizes

**Effort:** 4-8 hours depending on theme complexity.

---

### P2 — When convenient (this quarter)

### 17. Add `Content-Security-Policy` header

Start in report-only mode:

```
Content-Security-Policy-Report-Only:
  default-src 'self';
  script-src 'self' 'unsafe-inline' https://www.googletagmanager.com https://www.google-analytics.com https://client.crisp.chat;
  style-src 'self' 'unsafe-inline' https://fonts.googleapis.com;
  img-src 'self' data: https:;
  font-src 'self' https://fonts.gstatic.com;
  report-uri /csp-report;
```

Run in report-only mode for 7 days. Review reports. Then promote to enforcement (`Content-Security-Policy` without `-Report-Only`).

**Effort:** Medium — requires testing all dependencies (Yoast, Crisp Chat, Google Tag Manager, fonts, etc.).

### 18. Add `Permissions-Policy` header

```
Permissions-Policy: camera=(), microphone=(), geolocation=(self), payment=()
```

**Effort:** 30 minutes.

### 19. Collapse the `http://www` 2-hop redirect to 1 hop

In Apache .htaccess or server config, ensure a single redirect from `http://www.gofflawdfw.com/` directly to `https://gofflawdfw.com/`, not via `https://www.gofflawdfw.com/`.

**Effort:** 15 minutes.

### 20. (Conditional) Remove `DataForSeoBot Disallow` from robots.txt

Only if Goff subscribes to DataForSEO. See Chelsea's decision list below.

**Effort:** 5 minutes.

### 21. Add `LocalBusiness` schema variant with hours

Block 1 already has hours via `openingHoursSpecification`. If you want a richer Local Pack appearance, add a separate `LocalBusiness` schema with detailed hours, services menu, etc.

**Effort:** 1 hour.

---

## 🟧 FOR CHELSEA (CEO/COO) — Strategic + Operational Decisions

### Tier 0 — This week (no cost, just decisions + data)

### A. Gather the "Inputs Needed" list above and email it to the dev team

This is the **single biggest blocker right now**. Until the dev team has this data, nothing schema-related can ship.

**Suggested email template:**

> Subject: Goff Law SEO audit — data needed to start fixes
>
> Hi [Dev Lead],
>
> Jim and Claude completed a comprehensive SEO audit of gofflawdfw.com on May 12. The audit identified ~20 fixable items, but several require business data from us before you can start work.
>
> Below is the data you need. Most should be quick to gather; please flag any that need additional research:
>
> [paste the "Inputs Needed" checklist]
>
> Once you have these, please start with the multi-H1 theme fix (highest priority) and the sitewide LegalService schema deployment.
>
> Full audit + fix-it list: https://gofflawsuperagent.up.railway.app/fixit
>
> Thanks,
> Chelsea

### B. Decide on a SERP monitoring tool

The audit has a pending recommendation: **Ahrefs Lite at $129/mo** (foundational for serious competitive SEO).

**Options ranked by value:**

| Tool | Monthly cost | What you get | Best for |
|---|---|---|---|
| **Ahrefs Lite** ⭐ | $129 | Backlinks, traffic estimates, keyword research, site audit, rank tracking | **Recommended.** Most-cited industry tool. Data Goff has been hand-waving about. |
| SEMrush Pro | $139 | Comparable to Ahrefs, slightly better PPC angle | Pick if Goff plans heavy paid-search investment |
| Moz Pro | $99 | Domain Authority is the industry-cited metric | Cheaper option, smaller dataset |
| DataForSEO | ~$1-5 | Pure API. No UI. Wire into existing Monday cron. | Bargain option; ~$1/mo gets 10x more SERP data than free WebSearch |
| (Stay free) | $0 | Just the existing Claude Monday cron | If marketing budget is tight |

**Action needed:** Decide and subscribe. Then send me the credentials so I can pull the data on a future Claude session.

### C. Approve homepage hero copy direction

`HERO-FIX-DRAFT.md` has 4 headline options (see Item #4 in dev section). **Recommended: Option A** ("A Dallas Personal Injury Lawyer Who Knows How Insurance Companies Think").

**Action needed:** Approve and notify dev team.

### Tier 1 — This month (decisions that drive content production)

### D. Approve scope for the suburb expansion

The audit confirms zero Goff pages for 32 DFW cities. Top 5 priority builds per ROI:

| # | City | Pop. | Top competitor | Why this one |
|---|---|---|---|---|
| 1 | **Frisco** | 220k | Snellings Law | Snellings is single incumbent; Thompson has Spanish-only; high-CPC zip codes |
| 2 | **Plano** | 300k | Vecchio | Vecchio leads but is displaceable; high income |
| 3 | **Allen** | 110k | Hwang/Burress | Wealthy Collin County; multiple smaller incumbents (more displaceable) |
| 4 | **McKinney** | 210k | McCraw Law Group | McCraw founded there — hardest opponent, but high reward |
| 5 | **Fort Worth** | 1M | Patterson Law Group | 1M population! Zero current Goff coverage. The biggest single market gap. |

**Decision needed:** Approve which subset to build first AND approve a content production budget (~$2-5K for the first 2-3 city hubs).

### E. Decide on content production model

Tier 1 + Tier 2 work assumes regular content production capacity.

| Option | Cost | Pros | Cons |
|---|---|---|---|
| **A. Freelance legal content writer** | $0.25-1.00/word ($500-2,000 per 2,000-word page) | Pay-per-deliverable, easy to scale | Need to vet quality; legal-niche writers are rare |
| **B. Bill AI Machine + Jim review** | Cheaper, just Jim's time | Tightly aligned with firm voice; uses existing tooling | Requires Jim to QA every output |
| **C. Content agency (monthly retainer)** | $2,000-8,000/mo for ~10 pages | Includes writing + editing + SEO optimization | Long contracts; risk of generic content |
| **D. In-house marketing hire** | $80-150K annual | Maximum quality + alignment | Long ramp; high commitment |

**Recommended for Goff's stage:** Start with **A** (freelance) on a project basis. Specifically:
- **Avalon Content** (PR Newswire alum, legal niche, $0.50-0.75/word)
- **Express Writers** (legal vertical, $0.30-0.50/word)
- **Upwork: filter "Legal Writer + 5+ stars + $50/hr range"**

Move to **C** or **D** if monthly output exceeds 15 pages.

**Decision needed.**

### F. Start a Google review-collection program

Mullen & Mullen displays **567 Google reviews / 4.9★** as their core trust signal. Per Phase 2 SERP findings, this is a real competitive moat.

**Goal:** 100+ Google reviews in 90 days.

**Implementation options:**

| Tool | Monthly cost | What it does |
|---|---|---|
| **BirdEye** ⭐ | $300-500 | Industry standard for PI firms. Auto-requests reviews via SMS/email post-case. Filters negative reviews to internal team. |
| **Podium** | $300-500 | Comparable to BirdEye. Better UI. |
| **NiceJob** | $75 | Cheaper, simpler. Less automation. |
| **Manual via Lawmatics/CRM** | $0 | Add a post-case email/SMS template. Less automation but free if CRM is already in place. |

**Recommended:** BirdEye at $300/mo IF Goff is committed to investing in reviews. Manual via CRM if budget is tight in Tier 0.

**Decision needed:** which tool, who owns it operationally.

### Tier 2 — This quarter

### G. Approve Phase 1 recon on 8 newly-discovered competitors

The SERP audit surfaced 8 firms NOT in our prior recon:

| Firm | Why it matters | Recon priority |
|---|---|---|
| **Hamilton Wingo** | $8B settlements claim — potentially bigger than Thompson Law! Top 10 for Dallas PI. | 🔴 HIGH |
| **Lyons & Simmons** | $1B+ verdicts. Top 10 for Dallas wrongful death + oilfield. | 🟧 MED |
| **Aldous Law** | Top 10 for Dallas truck, wrongful death, oilfield. Multi-vertical Dallas player. | 🟧 MED |
| **Patterson Law Group** | Fort Worth dominator + has Plano page. | 🟧 MED (Fort Worth threat) |
| **Coby Wooten** | Fort Worth specialist. 10x Top Attorney in FW magazine. | 🟢 LOW |
| **Kraft & Associates** | 45+ years Dallas car-accident specialty. | 🟢 LOW |
| **Thomas J. Henry Law** | 200+ attorneys, statewide. Already known via Phase 2. | 🟧 MED |
| **Zehl Law** | "Undefeated" Dallas truck (largest 18-wheeler recoveries in Dallas County). Houston-based. | 🟧 MED |

**Action:** Tell Claude to run Phase 1 recon on these in a future session. ~30-45 min per firm × 8 = 4-6 hours of automated work. **No cost; just authorization.**

### H. Hire a content writer

To execute the Tier 1 + Tier 2 content roadmap, Goff needs a content production pipeline. See Option matrix in section E above.

### Tier 3 — Long game (6-12 months)

### I. Spanish-language content track

Thompson Law has 150+ Spanish PI pages. Goff has zero. ~30% of DFW PI claimants are Hispanic.

**Approach:** Bilingual content writer or translation service. Start with the top 10 highest-traffic English pages, translate + culturally adapt.

**Budget:** $8-20K for initial translation of 10-20 pages.

### J. Hire dedicated SEO specialist or contract with agency

The audit identifies enough work to keep someone busy for 12+ months. At Goff's $55-100K/mo marketing budget, dedicated SEO ownership is reasonable.

**Budget:** $4-12K/mo for an agency; $80-150K annual for in-house.

**Recommended Dallas-area agencies:**
- Juris Digital (already in Goff's knowledge base; PI-specialist)
- LawRank (PI-niche; ~$5K/mo)
- Local Dallas SEO firms with legal-vertical experience

---

## ✍️ FOR THE CONTENT WRITER (whenever Chelsea hires one)

### Week 5-8 priorities

1. **Write 8 missing meta descriptions** (per dev item #13) — 45 minutes
2. **Trim 40 oversized meta descriptions** to ≤155 chars — 2 hours
3. **Write 5-8 FAQ Q/A pairs per practice-area page** — for FAQPage schema deployment — ~12-16 hours across all pages
4. **Build the Frisco landing page hub:** 1 city overview (2,500-3,000 words) + 5-7 practice-area sub-pages (1,500-2,000 words each) — ~40-60 hours
5. **Build the Plano landing page hub:** same structure — ~40-60 hours
6. **Build the Allen landing page hub:** same structure — ~40-60 hours
7. **Build the McKinney landing page hub:** same structure — ~40-60 hours (hardest because McCraw is well-entrenched)

### Months 3-4 priorities

8. **Replicate the Galaxy Gas success pattern across other mass torts:**
   - AFFF: 4 geo pages (currently 3) — add 1
   - Tepezza: 4 geo pages (currently 3) — add 1
   - Paragard: 4 geo pages (currently 3) — add 1
   - AI Liability: 4 geo pages (currently 3) — add 1
   - Suboxone: 4 geo pages (currently 1) — add 3
   - Hair Relaxer: 4 geo pages (currently 1) — add 3
9. **Expand the 3 thin hub pages:**
   - `/east-texas/` — currently under 500 words → target 2,500-4,000
   - `/houston/` — same
   - `/legal-services/` — same
10. **Build Fort Worth landing page hub** — same scale as Frisco

### Months 5-6 priorities

11. **Add Workers' Compensation / Workplace Injury vertical** — major Texas opportunity, completely missing
12. **Add Oilfield + Plant & Refinery + Construction Accident pages** — heavy-industry Texas verticals
13. **Expand Nursing Home Abuse** (1 → 5 pages across cities)
14. **Expand Medical Malpractice** (1 → 5 pages across cities)
15. **Arlington + Irving + Garland city pages**

### Long game (Months 7-12)

16. **Spanish-language translation** of the top 20 English pages
17. **Blog content cadence** — target 4-8 posts/month, focused on long-tail commercial queries (settlement amounts, statute of limitations specifics, "what to do after X" guides). Goal: 200+ posts by end of year 1.
18. **Backlink-bait content:** in-depth original research, infographics, local data deep-dives (DFW accident statistics, court-specific guidance, expert witness rosters)

---

## 🎯 SERP-impact summary (so Chelsea can quantify ROI conversations)

| Tier | Effort/Cost | Expected SERP impact within window |
|---|---|---|
| **Tier 0 (this week)** | ~$0-2K | Schema rich results begin appearing (star ratings, FAQ boxes); multi-H1 fix helps Google understand pages; og:image fixes social-share CTR; hero replacement lifts conversion 50-100% (industry benchmark) |
| **Tier 1 (this month)** | ~$2-5K + $129/mo tool | First page-1 SERP appearances in suburb-specific queries (Frisco/Plano PI lawyer); Galaxy Gas template replicates to 4-5 more mass torts |
| **Tier 2 (this quarter)** | ~$5-15K | Fort Worth visibility unlocked; Workers' Comp + Oilfield verticals start ranking; competitive intel against 8 new firms closes strategic-blindspot risk |
| **Tier 3 (12 months)** | ~$30-60K | Per existing executive report projection: avg pos 40 → avg pos 5 = **10-20x organic clicks** from same 42K impression base. $720K invested → $13.5M revenue potential (18x ROI). |

---

## 📊 Before/after KPI tracking table

Fill this in over the next 90 days to measure progress.

| Metric | Baseline (2026-05-12) | 30-day target | 90-day target | Source |
|---|---|---|---|---|
| Schema types on every page | 4 (auto-Yoast) | 7+ (add LegalService, Service, Offer, FAQPage where applicable) | 10+ | Re-run audit `02-schema-audit.md` |
| Pages with multi-H1 | 48 / 74 | 0 | 0 | DevTools console check |
| Pages with og:image | 22 / 74 | 74 / 74 | 74 / 74 | Yoast bulk editor |
| Pages missing meta desc | 8 | 0 | 0 | Yoast bulk editor |
| Pages with oversized desc (>160) | 40 | 0 | 0 | Yoast bulk editor |
| Homepage conversion (form submits / visitors) | (current baseline) | +30-50% | +50-100% | Google Analytics |
| Avg Google organic position | 40 | 30 | 20 | Google Search Console |
| Monthly organic clicks | 170 | 250 | 400 | Google Search Console |
| Galaxy Gas SERP positions in top 10 | 4 | 4+ | 5+ | Re-run SERP audit |
| Frisco / Plano / Allen / McKinney pages | 0 | 1-2 hubs live | All 4 hubs + practice pages | URL inventory |
| Google review count | (current) | +20 | +60 | Google Business Profile |
| Pages with FAQPage schema | 0 | 5-10 | 20+ | Re-run audit |

---

## 📧 COMMUNICATION TEMPLATES

### Template 1: Chelsea → dev team kickoff email

> **Subject:** Goff Law SEO audit complete — fix-it list + data needed
>
> Hi [Dev Lead],
>
> Jim and I completed a comprehensive SEO audit of gofflawdfw.com (overnight, finished 2026-05-12). The full audit + fix-it list is here:
>
> 🔗 **Web version:** https://gofflawsuperagent.up.railway.app/fixit
> 📁 **Source folder:** `recon/goff-law/` in the ArnoldItkin workspace
>
> Top 4 priority items for you to start on:
>
> 1. **Fix multi-H1 theme bug** — 48 of 74 pages have 2-3 `<h1>` tags. Likely in `header.php`. ~1-3 hours.
> 2. **Deploy sitewide LegalService schema** — ready-to-paste JSON-LD block in `08-schema-implementation-guide.md`. ~1 hour after I send you the inputs below.
> 3. **Deploy AggregateRating + Review schema** on homepage. ~2 hours after I send review data.
> 4. **Replace empty homepage hero** with the spec in `HERO-FIX-DRAFT.md`. ~4-8 hours.
>
> **Data I'm pulling for you and will send tomorrow:**
> - Verified Google review count + 5 verbatim 5-star reviews
> - Jim's bar admission year + law school + headshot
> - Office hours + social media URLs
> - [Full checklist in the fix-it list]
>
> Quote me on hours + start date. Aim for Tier 0 complete by [date 2 weeks out].
>
> Thanks,
> Chelsea

### Template 2: Chelsea → content writer outreach

> **Subject:** Legal content writing project — Dallas PI law firm
>
> Hi [Writer],
>
> Goff Law (gofflawdfw.com) is a Dallas-Fort Worth personal injury firm. We're hiring a freelance legal content writer for a multi-month project building out new geographic + practice-area content.
>
> Initial scope: 4-6 city landing page hubs (Frisco, Plano, Allen, McKinney) — each 1 city overview (~2,500 words) + 5-7 practice-area sub-pages (~1,500-2,000 words each).
>
> Rate range: $0.50-1.00/word depending on experience.
> Volume estimate: 60,000-80,000 words total for the city hub project.
> Timeline: 8-12 weeks.
>
> Requirements:
> - Legal writing experience preferred (PI niche bonus)
> - Familiarity with Texas tort law
> - SEO awareness (keyword integration, heading hierarchy, schema-friendly structure)
> - Will follow our content briefs + edits without ego
>
> If interested, please send: writing samples (legal vertical preferred), rate quote per 1,000 words, and capacity (pages/month).
>
> Thanks,
> Chelsea Goff (COO, Goff Law PLLC)

---

## ❓ Open questions that need decisions

Before any of this can ship, three forks need to be resolved:

1. **WP dev capacity** — Is your current dev on retainer? Does this fit their hours? If not, we may need to bring in a specialist for the Tier 0 schema work (one-shot ~$1,500).

2. **Content writer model** — Hire freelance, agency retainer, Bill AI Machine + Jim review, or in-house?

3. **Tool subscription** — Ahrefs ($129/mo) or DataForSEO ($1-5/mo) or stay free? Decision pending from 2026-05-11.

---

## 📁 Where the full detail lives

Each item above is sourced from one of these audit artifacts. Open these if you need supporting data:

| Topic | File |
|---|---|
| URL inventory + sitemap | `recon/goff-law/01-url-inventory.md` |
| Schema gaps + ideal schema set | `recon/goff-law/02-schema-audit.md` |
| Meta tags, H1, og:image issues | `recon/goff-law/03-meta-tags-audit.md` |
| HTTPS, headers, technical hygiene | `recon/goff-law/04-technical-hygiene.md` |
| Practice areas + locations covered | `recon/goff-law/05-content-inventory.md` |
| Gap matrix vs competitors | `recon/goff-law/06-content-gap-analysis.md` |
| Live SERP positions + new competitors | `recon/goff-law/07-serp-positioning.md` |
| **Ready-to-paste schema JSON-LD blocks** | `recon/goff-law/08-schema-implementation-guide.md` |
| On-page quick wins | `recon/goff-law/09-on-page-quick-wins.md` |
| **COO-briefing roadmap (Tier 0-3)** | `recon/goff-law/10-prioritized-roadmap.md` |
| UX scorecard + screenshots | `recon/goff-law/UX-RECON-PHASE-1.md` |
| Homepage hero redesign spec | `recon/goff-law/HERO-FIX-DRAFT.md` |
| Strategic positioning map | `recon/dfw-pi-positioning-map.svg` |
| Competitor scoreboard | `recon/COMPETITOR-SCOREBOARD.md` |

---

## ✅ How to track progress

Suggested workflow:

1. **Paste this list into your project management tool** (Asana / Trello / Linear / Notion). Each top-level item becomes a card. Effort + impact + owner become metadata.
2. **Mark items complete** as they ship. Update the status legend (☐ → 🟡 → ✅).
3. **Re-run the audit at 30 days** (same plan at `docs/plans/2026-05-10-goff-law-full-seo-audit.md`). Compare against the Before/After KPI tracking table.
4. **Brief the COO weekly** with status against this checklist.

---

*This fix-it list represents ~150 hours of structured remediation work and ~$8-25K of one-time costs (depending on writer/dev rates), plus optional ongoing tool subscriptions. Spread across 90 days, it transforms Goff Law from "decent niche-litigation specialist with a strong brand voice but weak SEO foundation" to "DFW PI firm with comprehensive geographic coverage, dominant emerging-litigation moat, full schema rich-result eligibility, and competitive intelligence against every meaningful market player."*

*— End of fix-it list.*
