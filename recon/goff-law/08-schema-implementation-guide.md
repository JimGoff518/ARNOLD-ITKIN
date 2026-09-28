# Goff Law — Schema Markup Implementation Guide

**Created:** 2026-05-11
**Owner:** Goff Law WordPress dev (or Jim if comfortable in Yoast / theme files)
**Companion to:** `02-schema-audit.md` (the audit that identified these gaps)

## How to deploy

You have three deployment paths in WordPress (pick whichever your dev prefers):

1. **Yoast SEO custom blocks** — Yoast has built-in support for Organization/LocalBusiness/Article/FAQ markup. Easiest for sitewide blocks.
2. **Schema plugin** — Schema Pro, Rank Math, or WPSSO add per-page schema editors via the WP admin UI.
3. **Direct theme injection** — Add JSON-LD blocks to `header.php` or a custom hook. Lowest dependency but requires dev access.

All blocks below are **template-grade** — you replace `{{PLACEHOLDER}}` tokens with real values before deploying.

## 📋 Inputs needed from Jim before deploying

Fill these in before handing the spec to your dev:

- [ ] Verified **Google Business Profile review count** + **average rating** (e.g., "4.8 based on 47 reviews")
- [ ] Verified **Avvo rating** (if any)
- [ ] **Bar admission state(s)** + admission year for Jim Goff (Texas, year?)
- [ ] **Office address** (confirmed: 12720 Hillcrest Rd, Suite 1045, Dallas, TX 75230)
- [ ] **Office hours** (M-F 9-5? 24/7 phone?)
- [ ] **Practice area list** (final — for Service schema)
- [ ] **Founding year** (per SERP audit: "launched in 2023")
- [ ] **Social media URLs** (Facebook, LinkedIn, X, YouTube — for sameAs)
- [ ] **Logo URL** (Goff's logo file, hosted)
- [ ] **Office image** (exterior or interior photo URL)
- [ ] **Jim Goff bio photo URL**

---

## Block 1: Sitewide Organization + LegalService (every page `<head>`)

**Where to deploy:** Inject sitewide via theme `header.php` OR Yoast Organization settings. Should appear in every page's `<head>`.

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
  "description": "Dallas-Fort Worth personal injury law firm founded by Jim Goff. Former insurance defense attorney now fighting for injured Texans. Focus on Galaxy Gas / nitrous oxide injuries, mass tort, truck accidents, sexual assault civil claims, and emerging litigation.",
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
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday","Tuesday","Wednesday","Thursday","Friday"],
      "opens": "{{e.g., 09:00}}",
      "closes": "{{e.g., 17:00}}"
    }
  ],
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
    "Personal Injury Law",
    "Car Accidents",
    "Truck Accidents",
    "Motorcycle Accidents",
    "Wrongful Death",
    "Premises Liability",
    "Catastrophic Injury",
    "Brain Injury",
    "Galaxy Gas / Nitrous Oxide Injuries",
    "Mass Tort Litigation",
    "AFFF Firefighting Foam",
    "PFAS Chemical Exposure",
    "Tepezza",
    "Paragard",
    "Sexual Assault Civil Claims",
    "Electric Scooter Accidents",
    "Amazon Truck Accidents"
  ]
}
</script>
```

**Validation:** https://validator.schema.org/ + Google Rich Results Test (https://search.google.com/test/rich-results)

---

## Block 2: AggregateRating + Review (homepage + key landing pages)

**Where to deploy:** Homepage and key practice-area landing pages. Add as a SEPARATE `<script>` block (don't try to nest inside Block 1).

⚠️ **IMPORTANT:** Use ONLY real review data from Google Business Profile, Avvo, or another verifiable source. Made-up review counts violate Google guidelines and can trigger a manual penalty.

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
      "author": {"@type": "Person", "name": "{{Real reviewer first name + last initial}}"},
      "datePublished": "{{YYYY-MM-DD}}",
      "reviewRating": {
        "@type": "Rating",
        "ratingValue": "5",
        "bestRating": "5"
      },
      "reviewBody": "{{Verbatim review text from Google}}"
    },
    {
      "@type": "Review",
      "author": {"@type": "Person", "name": "{{Real reviewer 2}}"},
      "datePublished": "{{YYYY-MM-DD}}",
      "reviewRating": {"@type": "Rating", "ratingValue": "5", "bestRating": "5"},
      "reviewBody": "{{Verbatim review text}}"
    }
  ]
}
</script>
```

**Tip:** Use 3-5 real verified reviews. Google likes a few sampled reviews more than zero.

---

## Block 3: Attorney schema (each attorney bio page)

**Where to deploy:** Jim Goff's bio page + any other attorney bio pages.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Attorney",
  "@id": "https://gofflawdfw.com/{{ATTORNEY_BIO_PATH}}#attorney",
  "name": "Jim Goff",
  "alternateName": "James Meadows Goff",
  "image": "https://gofflawdfw.com/{{PATH_TO_ATTORNEY_PHOTO}}",
  "jobTitle": "Founding Attorney",
  "telephone": "+1-972-928-0085",
  "email": "{{EMAIL}}",
  "url": "https://gofflawdfw.com/{{ATTORNEY_BIO_PATH}}",
  "description": "Founder of Goff Law, PLLC. Former insurance defense attorney now representing injured Texans. Practice focuses on truck accidents, mass tort (Galaxy Gas, AFFF, PFAS, Tepezza), brain injury, sexual assault civil claims, and personal injury litigation throughout the DFW metroplex.",
  "worksFor": {
    "@id": "https://gofflawdfw.com/#legalservice"
  },
  "alumniOf": {
    "@type": "EducationalOrganization",
    "name": "{{LAW_SCHOOL_NAME}}",
    "url": "{{LAW_SCHOOL_URL}}"
  },
  "knowsAbout": [
    "Personal Injury Litigation",
    "Truck Accident Cases",
    "Mass Tort Litigation",
    "Galaxy Gas / Nitrous Oxide Injuries",
    "Civil Sexual Assault Claims",
    "Brain Injury and Catastrophic Injury"
  ],
  "hasCredential": [
    {
      "@type": "EducationalOccupationalCredential",
      "credentialCategory": "Bar Admission",
      "recognizedBy": {
        "@type": "Organization",
        "name": "State Bar of Texas"
      },
      "validIn": {"@type": "State", "name": "Texas"},
      "dateCreated": "{{ADMISSION_YEAR}}"
    }
  ],
  "award": [
    "Top 40 Under 40",
    "Super Lawyers",
    "Best Lawyers in America"
  ],
  "memberOf": [
    {"@type": "Organization", "name": "State Bar of Texas"}
  ],
  "sameAs": [
    "https://profiles.superlawyers.com/texas/dallas/lawyer/james-goff/39e7f6d6-79f6-48f8-b016-9da49543abc7.html",
    "https://www.bestlawyers.com/lawyers/jim-goff/328523",
    "https://lawyers.justia.com/lawyer/jim-goff-1670096",
    "https://lawyers.findlaw.com/texas/dallas/5194263_1/",
    "https://directory.dmagazine.com/lawyers/james-goff/"
  ]
}
</script>
```

---

## Block 4: Service schema template (one per practice-area page)

**Where to deploy:** Each practice-area page (car-accident, truck-accident, wrongful-death, premises-liability, Galaxy Gas, mass tort, etc.). Replace `{{PRACTICE_AREA}}` and `{{SERVICE_DESCRIPTION}}`.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Service",
  "@id": "https://gofflawdfw.com/{{PAGE_URL_PATH}}#service",
  "serviceType": "Legal Representation — {{PRACTICE_AREA}}",
  "name": "{{e.g., Dallas Car Accident Lawyer Service}}",
  "description": "{{e.g., Comprehensive legal representation for Dallas car accident victims. Goff Law fights insurance companies to recover medical bills, lost wages, and pain and suffering. No fee unless we win.}}",
  "provider": {
    "@id": "https://gofflawdfw.com/#legalservice"
  },
  "areaServed": [
    {"@type": "City", "name": "{{e.g., Dallas}}"},
    {"@type": "AdministrativeArea", "name": "Dallas-Fort Worth metroplex"}
  ],
  "offers": {
    "@type": "Offer",
    "price": "0",
    "priceCurrency": "USD",
    "description": "Free initial consultation · Contingency fee · No fee unless we win"
  },
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Case Evaluation",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Free Case Review"
        }
      }
    ]
  }
}
</script>
```

**Apply across these pages** (per content inventory):
- `/dallas-personal-injury-lawyer/*` (12 pages)
- `/dallas/*` (9 pages)
- `/legal-services/*` (6 pages)
- `/cedar-hill/*` (17 pages)
- `/desoto-*-lawyer/` (25 pages)
- All Galaxy Gas pages
- All mass tort pages

---

## Block 5: FAQPage schema template

**Where to deploy:** Every practice-area page that has FAQ content. Most Goff pages have FAQ-shaped content in the body (visible during URL inventory) but it's not marked up.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "{{e.g., How long do I have to file a personal injury lawsuit in Texas?}}",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "{{e.g., In Texas, the statute of limitations for most personal injury claims is two years from the date of the injury. Wrongful death claims also follow a two-year statute of limitations from the date of death. Certain exceptions apply for minors and cases involving fraud.}}"
      }
    },
    {
      "@type": "Question",
      "name": "{{Q2 — lift from existing page content}}",
      "acceptedAnswer": {"@type": "Answer", "text": "{{A2}}"}
    },
    {
      "@type": "Question",
      "name": "{{Q3}}",
      "acceptedAnswer": {"@type": "Answer", "text": "{{A3}}"}
    },
    {
      "@type": "Question",
      "name": "{{Q4}}",
      "acceptedAnswer": {"@type": "Answer", "text": "{{A4}}"}
    },
    {
      "@type": "Question",
      "name": "{{Q5}}",
      "acceptedAnswer": {"@type": "Answer", "text": "{{A5}}"}
    }
  ]
}
</script>
```

**Tip:** Each page should have 5-8 FAQ entries. Lift questions verbatim from page body content where possible. If page lacks FAQs, this is a chance to write them while adding markup. Common PI FAQ topics: "How much is my case worth?", "How long will my case take?", "Do I have to go to court?", "What if the insurance company offers me a settlement?", "What does a contingency fee mean?"

---

## Block 6: Offer schema for free consultation (homepage + every consult CTA)

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Offer",
  "name": "Free Personal Injury Case Consultation",
  "description": "Confidential, no-obligation consultation with Goff Law. No fee unless we win your case.",
  "url": "https://gofflawdfw.com/contact/",
  "price": "0",
  "priceCurrency": "USD",
  "availability": "https://schema.org/InStock",
  "seller": {
    "@id": "https://gofflawdfw.com/#legalservice"
  },
  "category": "Legal Consultation",
  "areaServed": [
    {"@type": "AdministrativeArea", "name": "Dallas-Fort Worth metroplex"},
    {"@type": "AdministrativeArea", "name": "Texas"}
  ]
}
</script>
```

---

## Bonus: VideoObject schema (if Goff has video content)

If Goff has video on landing pages (intro videos, testimonials, attorney explainers), mark them up:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "VideoObject",
  "name": "{{Video title}}",
  "description": "{{Video description}}",
  "thumbnailUrl": "{{Thumbnail URL}}",
  "uploadDate": "{{ISO date}}",
  "contentUrl": "{{Video file URL or YouTube URL}}",
  "embedUrl": "{{YouTube embed URL}}",
  "duration": "PT2M30S"
}
</script>
```

---

## Deployment checklist

Once all blocks are deployed:

- [ ] **Validate** each block at https://validator.schema.org/
- [ ] **Test** with Google Rich Results Test (https://search.google.com/test/rich-results)
- [ ] **Deploy to staging first** if a staging environment exists
- [ ] **Submit updated sitemap** to Google Search Console after deployment
- [ ] **Wait 7-14 days** for Google to re-crawl + start showing rich results
- [ ] **Re-crawl with this audit method in 30 days** to confirm rich result eligibility (re-run Task B2 from the plan)
- [ ] **Monitor GSC "Enhancements" section** for new "Sitelinks search box", "FAQ", "Breadcrumbs", "Review snippets" rich-result reports

---

## Common pitfalls to avoid

1. **DO NOT** add `Review` schema without real reviews. Google can penalize fake review markup.
2. **DO NOT** add `AggregateRating` higher than what real review platforms (Google Business Profile, Avvo) report. Must be verifiable.
3. **DO NOT** add `FAQPage` schema for content that isn't visibly on the page. Google can penalize hidden-content markup.
4. **DO NOT** duplicate `@id` values across blocks unless you intentionally want them to merge (the `@id` linkage is how blocks reference each other — e.g., Service schema's `provider` points to `https://gofflawdfw.com/#legalservice` which is the LegalService block's `@id`).
5. **DO** keep schema in sync with page content. If the page says "20 years experience" but schema says "10 years", Google may distrust both.
6. **DO** test mobile-responsive rendering of schema-driven rich results — most rich results show differently on mobile vs desktop.

---

## Expected SERP wins after deployment

Per Phase 2 Thompson Law analysis + general SEO research:

| Rich result type | Driven by schema | Estimated CTR lift |
|---|---|---|
| Sitelinks search box | WebSite | +5-10% on brand searches |
| Star ratings | AggregateRating + Review | **+15-30%** CTR on listings |
| FAQ accordion under listing | FAQPage | **+10-25%** CTR — claims more SERP real estate |
| Attorney rich card | Attorney | +5-15% on attorney name searches |
| Breadcrumb trail | BreadcrumbList | Cosmetic; +2-5% |
| Service rich result | Service | +5-10% on service queries |

**Conservative composite estimate:** 30-60% lift in organic CTR for pages with full schema treatment, depending on which rich results Google actually awards. Not all rich results trigger every time — Google selects per-query.

---

## Effort estimate

- Block 1 (Sitewide LegalService): 1 hour to gather inputs + deploy
- Block 2 (AggregateRating + Review): 1-2 hours (depends on review data gathering)
- Block 3 (Attorney): 1-2 hours per attorney
- Block 4 (Service templates × N practice areas): 4-6 hours (covers all practice pages once)
- Block 5 (FAQPage × N pages): 6-12 hours (writing/finding 5-8 FAQs per page is the heavy lift)
- Block 6 (Offer): 30 minutes
- Testing + validation: 2 hours

**Total: ~16-24 hours of dev + content work.** Could be parallelized across a content writer (FAQ writing) and a dev (markup deployment).
