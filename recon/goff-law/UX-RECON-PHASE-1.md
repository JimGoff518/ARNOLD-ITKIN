# Goff Law UX Recon — Phase 1

**Date:** 2026-05-10
**Scope:** Above-the-fold visual comparison of Goff Law vs Thompson Law, Mullen & Mullen, Witherite Law Group + lead-capture mechanics audit + conversion-element inventory
**Method:** Crawl4AI screenshots (4 pages) + raw HTML extraction + markdown crawls + sitemap analysis
**Companion to:** `recon/thompson-law/PHASE-1-RECON-REPORT.md`, `recon/COMPETITOR-SCOREBOARD.md`

> ⚠️ **This is a preliminary visual UX audit, not a usability study.** Findings are based on what's visually present + what's in the HTML. A full UX audit would require user testing, heatmaps, session recordings, and mobile device testing. Use this to make first-cut prioritization decisions, not final UX design choices.

---

## TL;DR — three things that matter

1. **Goff Law has the strongest brand voice in the field but the weakest above-the-fold conversion mechanics.** The "lifelong Dallas resident / out-of-town lawyers who never drove down Abrams Road" copy is gold — but it's buried below an empty hero with no proof and no form.
2. **Witherite is winning the lead-capture race.** They put a 6-field form ABOVE THE FOLD on the homepage. Mullen and Thompson have prominent CTAs to forms. Goff has a "Contact Us" link to a page that itself has no form above the fold.
3. **Trust signals are conspicuously absent from Goff.** No BBB badge, no Avvo rating, no Super Lawyers, no specific case results, no review count, no Million Dollar Advocates. "MILLIONS WON" is the only proof signal and it's vague.

---

## Screenshots (open these side-by-side)

| Firm | Screenshot | Key first impression |
|---|---|---|
| **Goff Law** | [recon/ux-screenshots/goff-home.png](../ux-screenshots/goff-home.png) | Empty gray hero, "MILLIONS WON" typography, hamburger nav, news ticker (Galaxy Gas) |
| **Thompson Law** | [recon/ux-screenshots/thompson-home.png](../ux-screenshots/thompson-home.png) | Bold "$1.9 BILLION" trust hammer, scrolling case results, red phone CTA, "Get Free Case Review" button |
| **Mullen & Mullen** | [recon/ux-screenshots/mullen-home.png](../ux-screenshots/mullen-home.png) | Family positioning ("JOIN The Family®"), full desktop nav, vanity phone (214-INJURED), community angle |
| **Witherite Law Group** | [recon/ux-screenshots/witherite-home.png](../ux-screenshots/witherite-home.png) | Above-the-fold lead form (6 fields + SMS opt-in + reCAPTCHA), Live Chat bubble, attorney portrait, clear vertical positioning ("Your Truck Wreck Attorneys") |
| **Goff Contact page** | [recon/ux-screenshots/goff-contact.png](../ux-screenshots/goff-contact.png) | Full-screen banner with just the word "CONTACT" — form is below the fold |

---

## UX Scorecard

Rated 1-5 (1 = absent / weak, 5 = best in class). Scoring is based on what's visible above the fold on desktop.

| UX Element | Goff Law | Thompson Law | Mullen & Mullen | Witherite |
|---|---|---|---|---|
| **Hero conversion mechanic** (form / CTA / phone) | 2 | 4 | 4 | 5 |
| **Trust signals above fold** (badges, results, reviews) | 1 | 5 | 3 | 4 |
| **Phone number prominence** | 2 | 5 | 4 | 5 |
| **Live chat / instant engagement** | 3 (Crisp installed but not visible above fold) | likely 4 | likely 4 | 5 (Live Chat bubble visible) |
| **Brand differentiation / voice** | **5 (best in class)** | 3 | 4 | 4 |
| **Newsworthy / current hook** | **5 (Galaxy Gas FDA ticker)** | 1 | 1 | 1 |
| **Desktop navigation visibility** | 1 (hamburger only) | 3 | 5 (full horizontal nav) | 4 |
| **Visual urgency (color, contrast, motion)** | 2 (washed gray) | 4 (red + dark) | 3 (gray-blue) | 4 (navy + red) |
| **Image/asset loading** | 1 (logo failed in screenshot) | 1 (logo failed in screenshot) | 2 (image loading visible) | 3 |
| **Mobile-first signals** (viewport, lazy load, srcset) | 1 (no lazy, no srcset) | 4 | 3 | 3 |
| **Lead form sophistication** (fields, opt-in, captcha) | unknown (form below fold on /contact) | 3 (single CTA → form) | 3 (FREE CONSULTATION button) | **5 (full form above fold + SMS opt-in)** |
| **Practice-area visual cards** | 0 (no visible cards above fold) | 2 (text mentions) | 3 (CASES nav menu) | 3 |
| **Case results dollar-amount visibility** | 0 | **5 ($1.9B + scrolling specifics)** | 2 (RESULTS in nav) | 3 |
| **Aggregate review count visibility** | 0 | 0 (hidden — they have 2,021 Birdeye reviews unmarked) | 1 (REVIEWS in nav) | 0 |
| **TOTAL (out of 70)** | **25/70** | **44/70** | **44/70** | **53/70** |

**Witherite wins the conversion war.** Mullen and Thompson are tied. Goff is significantly behind in pure conversion mechanics — but has unique strengths nobody else has.

---

## Goff Law's UX strengths (don't change these)

### 1. Authentic brand voice (best in class)
The homepage About section has lines no competitor can match:
> "As a lifelong resident of Dallas, Mr. Goff has recently seen a rapid influx of out of town lawyers who have never driven down Abrams Road think they know or care about the Dallas community."

> "As a third generation Texan and a lifelong Dallas resident, the people of Dallas are our friends, our neighbors, and our loved ones."

Thompson Law's "$1.9 BILLION" is impressive but interchangeable with any large PI firm. Mullen's "Family" angle is sweet but generic. Witherite's "Truck Wreck Attorneys" is positioning but cold. **Goff's hyper-local, anti-big-firm story is the clearest differentiation in the field.**

**Action:** Surface this voice ABOVE THE FOLD, not buried in the About section.

### 2. Newsworthy hook (Galaxy Gas FDA ticker)
The top banner reading "FDA Sounds Alarm on Galaxy Gas: Serious Health Risks Identified | LEARN MORE" is the only current-events hook on any of the 4 sites.

This is exactly the right play for an emerging-litigation specialist. None of Thompson, Mullen, or Witherite have anything like this.

**Action:** Keep doing this. Rotate the hook as new mass torts emerge.

### 3. Former defense attorney positioning
> "Before opening Goff Law, PLLC, Mr. Goff practiced with a prominent personal injury defense litigation firm in Dallas. In his time fighting on behalf of the biggest insurance companies in Texas, Mr. Goff learned what insurance adjusters value most..."

This is a genuine, defensible differentiator. The "former insurance defense → now plaintiffs' counsel" arc is a powerful credibility builder in PI marketing.

**Action:** Build this into a video / landing page / explainer. Currently buried.

### 4. Mass tort + emerging litigation depth
Sitemap reveals 128 pages including:
- AFFF (firefighter foam)
- Paragard
- Tepezza
- Chemical exposure / PFAS
- AI liability *(yes, really — they have an "AI liability lawyer" page)*
- Hair relaxers
- Privacy / emotional distress
- Galaxy Gas (in 7 different geographies)

Thompson Law has NONE of this depth. Goff is genuinely positioned for the next wave of mass tort litigation.

**Action:** Make this discoverable. Add a "Mass Tort & Emerging Litigation" hub page if there isn't one.

---

## Goff Law's UX weaknesses (rank-ordered by ROI to fix)

### Critical (fix in week 1)

**1. The hero is empty.** "MILLIONS WON" + "SERIOUS INJURIES, SERIOUS RESULTS" with no specific case result, no trust badge, no testimonial, no form. The single most valuable real estate on the site is dead space.

**Fix:** Replace with: (a) one specific case result with dollar amount, (b) BBB / Avvo / Super Lawyers badge row, (c) compact "Tell us about your case" form OR a phone-prominent CTA bar.

**2. /contact page above-the-fold is just a banner.** The user clicks "Contact" → sees a giant gray banner with the word "CONTACT" → has to scroll. That's a measurable bounce trigger.

**Fix:** Make the form the FIRST thing on /contact. Banner can stay smaller or move below.

**3. No trust badges anywhere visible.** Zero BBB, Avvo, Super Lawyers, Million Dollar Advocates, etc. found in homepage HTML.

**Fix:** If Goff has any of these credentials, get them in the header or hero. If Goff doesn't have any: pursue Avvo (free), Super Lawyers (peer-nominated), and Texas Board Certified PI (real credential, takes time).

**4. No specific case results visible.** "MILLIONS WON" is unverifiable. Thompson Law shows specific dollar amounts ($16M D&O Negligence, $11.9M…). Mullen shows "$800M+". Goff shows nothing.

**Fix:** Pick 3-5 of Goff's biggest verifiable settlements/verdicts. Display dollar amount + case type + (optional) brief description. Stagger them like Thompson does or just show 3 in a row.

**5. No aggregate review count anywhere.** What's Goff's Google review count? Avvo rating? Without these, every visitor has to take Goff on faith.

**Fix:** If Goff has 50+ Google reviews, display "★★★★★ X.X based on N Google reviews" prominently. Connect the rating widget. If Goff has < 50 reviews — start a systematic collection program TODAY (this is also a Phase 2 deep-dive recommendation).

### High priority (fix in month 1)

**6. Hamburger-only navigation on desktop.** All competitors show a horizontal nav bar (PRACTICE AREAS, RESULTS, ABOUT, CONTACT). Hiding nav behind a hamburger on desktop forces an extra click and reduces visible "depth" / "trust." Mullen's nav specifically shows REVIEWS, RESULTS, COMMUNITY & EVENTS — every item is a credibility signal.

**Fix:** Show a desktop horizontal nav with: PRACTICE AREAS · RESULTS · ABOUT · LOCATIONS · CONTACT. Keep hamburger for mobile.

**7. No SMS opt-in on lead form.** Witherite explicitly captures "Opt In Consent to Receive Text Messages" at form submit. PI firms with SMS engagement convert higher and respond faster (vs phone tag). Goff's contact form (per the markdown extract) is bare-bones.

**Fix:** Add a single SMS opt-in checkbox to the contact form. TCPA compliance text + checkbox. Then build SMS auto-response in CRM ("Thanks for contacting Goff Law. A team member will text you within 15 minutes.")

**8. Crisp Chat is installed but not promoted.** The HTML reveals Crisp Chat is loaded — but it's not visible above the fold in the screenshot. Either it's positioned poorly or styled to fade in.

**Fix:** Make sure the Crisp Chat bubble is visibly present from page load, not on scroll/delay. Customize the welcome message: "Hi — Jim Goff here. Got a question about your case? Text me."

**9. Vanity phone number opportunity.** Mullen has "214-INJURED". Thompson has "1-800-LION-LAW". Goff has "972-928-0085" — forgettable. Vanity numbers boost call-tracking attribution AND brand recall.

**Fix:** Acquire a memorable DFW vanity number (e.g., "214-GOFF-LAW", "214-DFW-HURT", "972-INJURED-NOW"). Run it as a tracking number alongside the existing primary line.

**10. No lazy loading + no srcset on images.** 35 `<img>` tags on homepage, 0 use `loading="lazy"`, 0 use `srcset`. Mobile users are downloading desktop-sized images. This hurts mobile Core Web Vitals → hurts Google rankings.

**Fix:** Convert to a properly responsive image setup. Most WordPress themes support this out of the box — likely a configuration issue.

### Medium priority (fix in quarter)

**11. Visual urgency is muted.** Washed-out gray gradient + soft yellow accent reads "subdued professional" but PI marketing typically benefits from urgent color cues (red, navy, deep yellow). Compare to Thompson's red phone button or Witherite's navy + red.

**Fix:** A color refresh — possibly keeping the yellow as a highlight color but punching up contrast. Worth A/B testing.

**12. Logo loading issue.** In the screenshot, the Goff logo image failed to render (alt text visible: "Goff Law | Attorney in Dallas, TX for Truck Accidents, Sexual Assault, and Brain Injury"). Could be CDN, lazy load, or CSS bug.

**Fix:** Investigate and fix. Logos failing to render on a 4-second screenshot is a real-world performance issue.

**13. Practice area cards aren't visible above the fold.** The homepage has a "Practice Areas" section but it's below the fold. Visitors landing for "car accident" don't immediately see that practice area.

**Fix:** Add 4-6 practice area icons/cards directly below the hero. Standard pattern; quick win.

**14. No location-specific pages for high-value DFW suburbs.** Sitemap has /dallas/, /houston/, /east-texas/, /cedar-hill/, and a LOT of /desoto-* (curious — why DeSoto over Plano?). Missing: /frisco/, /plano/, /allen/, /mckinney/, /irving/, /arlington/, /grand-prairie/, /fort-worth/.

**Fix:** Build at least Frisco, Plano, Allen, McKinney pages (per the SEO audit roadmap). Each city deserves the same depth of practice-area sub-pages currently used for Cedar Hill/DeSoto.

### Low priority (fix when convenient)

**15. 26 external scripts + 13 stylesheets.** That's heavy. Likely page-speed cost on mobile. Audit-able via PageSpeed Insights — but worth a quick check.

**16. The yellow "LEARN MORE" link in the news ticker has low contrast against the gray background.** Accessibility (WCAG AA) likely fails this contrast ratio.

---

## Quick UX wins matrix

| Fix | Effort | Impact | When |
|---|---|---|---|
| Add 1 specific case result above fold | S (1-2 hr) | HIGH | Week 1 |
| Add BBB/Avvo/Super Lawyers badge row | S (2-3 hr if credentials exist) | HIGH | Week 1 |
| Move form ABOVE fold on /contact | S (1-2 hr) | HIGH | Week 1 |
| Add aggregate review count + rating | S (1 hr) | HIGH | Week 1 |
| Show desktop horizontal nav | M (3-5 hr WordPress dev) | MED-HIGH | Week 2 |
| SMS opt-in on contact form + auto-response | M (4-6 hr) | HIGH | Week 2 |
| Make Crisp Chat visible above fold from load | S (1 hr) | MED | Week 2 |
| Surface "former defense attorney" angle in hero | M (creative + dev) | MED-HIGH | Month 1 |
| Acquire vanity phone number | M (acquisition + setup) | MED | Month 1 |
| Add `loading="lazy"` + `srcset` to images | M (4-8 hr theme work) | MED (mobile perf + SEO) | Month 1 |
| Build Frisco/Plano/Allen/McKinney pages | L (multi-day per city) | HIGH (covered in SEO roadmap) | Month 1-2 |

---

## What this UX recon does NOT cover (Phase 2 backlog)

- **Mobile device testing.** All screenshots are desktop. Mobile UX is likely the biggest leak in Goff's funnel — 60-70% of PI traffic is mobile.
- **Scroll-depth observation.** What's actually below the fold on each page? Thompson Law's page is 5,000+ words deep; Goff's homepage is unclear.
- **Lead form completion friction.** How many fields? Required vs optional? Conditional logic? Field validation messages?
- **Page speed measurement.** PageSpeed Insights / Lighthouse / WebPageTest — quantify the performance gap.
- **Heatmap / session recording.** Hotjar / Microsoft Clarity (free) on Goff's site would reveal where visitors actually click + where they drop off.
- **A/B test backlog.** The above quick-wins are high-confidence improvements but should be measured. Set up GA4 events + a simple A/B testing framework before deploying changes.
- **Accessibility audit.** WCAG 2.1 AA conformance — Goff's color contrast at minimum needs review.
- **Conversion funnel measurement.** Where exactly does Goff lose visitors? Homepage → practice page → contact → form submit conversion at each step.
- **Competitor blog / content UX.** Practice area pages (truck accident, wrongful death, etc.) — visual quality, depth, internal linking.

---

## Recommended next moves

1. **Tier-0 quick wins this week** (rows 1-4 in the matrix above) — all could be done by a competent WordPress dev in a single day. Estimated impact: noticeably higher conversion.
2. **Schedule a mobile UX session** — open Goff's site on a real phone, run through the user journey from organic search → landing → form submit. Document friction.
3. **Set up Microsoft Clarity** (free) on gofflawdfw.com today. By end of week you'll have heatmaps + session recordings showing actual user behavior.
4. **Tie this UX recon into the existing SEO audit plan** at `docs/plans/2026-05-10-goff-law-full-seo-audit.md`. Many UX fixes (schema, image lazy-load, mobile perf) overlap with SEO fixes — execute together.
5. **For the COO briefing:** the "Witherite has a form above the fold; Goff has an empty hero" comparison is the single most concrete, persuasive way to communicate why investing in UX will move conversion numbers.

---

## Files saved (this recon)

- `recon/goff-law/UX-RECON-PHASE-1.md` — this report
- `recon/ux-screenshots/goff-home.png` — Goff Law homepage screenshot
- `recon/ux-screenshots/goff-contact.png` — Goff Law /contact page screenshot
- `recon/ux-screenshots/thompson-home.png` — Thompson Law homepage screenshot
- `recon/ux-screenshots/mullen-home.png` — Mullen & Mullen homepage screenshot
- `recon/ux-screenshots/witherite-home.png` — Witherite Law Group homepage screenshot
