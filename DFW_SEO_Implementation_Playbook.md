# DFW Market SEO Implementation Playbook
## Personal Injury Law Firm - 12-Week Launch Strategy

**Document Version:** 1.0
**Created:** January 2026
**Target Market:** Dallas-Fort Worth Metroplex
**Practice Area:** Personal Injury Law

---

# EXECUTIVE SUMMARY

This playbook provides a comprehensive, week-by-week implementation guide for establishing SEO dominance in the Dallas-Fort Worth personal injury legal market. The DFW metroplex represents the 4th largest metro area in the United States with approximately 7.5 million residents, making it a highly competitive but lucrative market for personal injury attorneys.

**Primary Objectives:**
- Establish strong local search presence across DFW submarkets
- Build technical SEO foundation for long-term organic growth
- Create authoritative content targeting high-intent keywords
- Develop sustainable link building and citation strategies

**Expected Outcomes (90 Days):**
- 50+ indexed pages targeting DFW personal injury keywords
- Complete Google Business Profile optimization
- 100+ local citations established
- Initial ranking improvements for long-tail keywords
- Baseline organic traffic established

---

# MONTH 1: FOUNDATION BUILDING

## WEEK 1: Technical SEO Audit & Infrastructure

### Day 1-2: Website Crawl & Technical Analysis

**Tasks:**

1. **Run Comprehensive Site Crawl**
   - Tool: Screaming Frog SEO Spider (Free up to 500 URLs, $259/year for full)
   - Alternative: Sitebulb ($13.50/month)

   **Crawl Settings:**
   ```
   Configuration > Spider > Crawl Settings:
   ☑ Check External Links
   ☑ Check Images
   ☑ Check CSS
   ☑ Check JavaScript
   ☑ Check SWF
   ☑ Crawl All Subdomains
   ```

   **Export Reports:**
   - All URLs with status codes
   - Response codes breakdown
   - Page titles (all, missing, duplicate, over 60 char)
   - Meta descriptions (all, missing, duplicate, over 155 char)
   - H1 tags (all, missing, duplicate, multiple)
   - Canonical errors
   - Redirect chains

2. **Google Search Console Setup/Audit**
   - Verify property ownership (DNS, HTML file, or tag)
   - Submit XML sitemap
   - Check for manual actions
   - Review Coverage report for errors
   - Export all crawl errors

   **Benchmark Metrics to Record:**
   | Metric | Current Value | Target (90 days) |
   |--------|--------------|------------------|
   | Total indexed pages | | +50% |
   | Coverage errors | | 0 |
   | Mobile usability errors | | 0 |
   | Average position | | Track improvement |
   | Total impressions | | +100% |
   | Total clicks | | +50% |

3. **Google Analytics 4 Audit**
   - Verify GA4 property is properly installed
   - Check for duplicate tracking codes
   - Set up conversion events:
     - Form submissions (contact, consultation request)
     - Phone calls (click-to-call)
     - Chat initiations
     - Email clicks
   - Create custom audiences for remarketing
   - Link to Google Ads account (if applicable)
   - Link to Search Console

### Day 3-4: Page Speed & Core Web Vitals

**Tasks:**

1. **Run Core Web Vitals Assessment**
   - Tool: Google PageSpeed Insights (https://pagespeed.web.dev/)
   - Tool: GTmetrix (https://gtmetrix.com/)

   **Test These Pages:**
   - Homepage
   - Main practice area pages (Car Accidents, Truck Accidents, etc.)
   - Contact page
   - Attorney bio pages
   - Blog index and sample posts

   **Record Baseline Metrics:**
   | Page | LCP | FID/INP | CLS | Mobile Score | Desktop Score |
   |------|-----|---------|-----|--------------|---------------|
   | Homepage | | | | | |
   | Car Accident | | | | | |
   | Contact | | | | | |

   **Target Benchmarks:**
   - Largest Contentful Paint (LCP): < 2.5 seconds
   - Interaction to Next Paint (INP): < 200 milliseconds
   - Cumulative Layout Shift (CLS): < 0.1
   - Mobile Score: 70+
   - Desktop Score: 85+

2. **Image Optimization Audit**
   - Tool: Screaming Frog > Images report
   - Check for:
     - Images over 100KB
     - Missing alt text
     - Non-optimized formats (convert to WebP)
     - Missing width/height attributes (causes CLS)

   **Create Optimization List:**
   ```
   Priority 1: Hero images on landing pages
   Priority 2: Attorney photos
   Priority 3: Blog featured images
   Priority 4: Decorative images
   ```

3. **Implement Speed Fixes**
   - Enable GZIP/Brotli compression
   - Implement browser caching
   - Minify CSS/JavaScript
   - Defer non-critical JavaScript
   - Preload critical resources
   - Implement lazy loading for below-fold images

### Day 5: Mobile & Security Audit

**Tasks:**

1. **Mobile-Friendliness Test**
   - Tool: Google Mobile-Friendly Test
   - Tool: BrowserStack for device testing

   **Check:**
   - Tap target sizes (minimum 48x48 pixels)
   - Font sizes (minimum 16px for body text)
   - Viewport configuration
   - No horizontal scrolling
   - Click-to-call functionality
   - Form usability on mobile

2. **Security Audit**
   - Verify SSL certificate is valid and properly installed
   - Check for mixed content warnings
   - Ensure all pages redirect HTTP to HTTPS
   - Verify HSTS is implemented
   - Check for security headers:
     - X-Content-Type-Options
     - X-Frame-Options
     - Content-Security-Policy

3. **Schema Markup Audit**
   - Tool: Google Rich Results Test
   - Tool: Schema.org Validator

   **Required Schema Types for Law Firm:**
   ```json
   {
     "@context": "https://schema.org",
     "@type": "LegalService",
     "name": "[Firm Name]",
     "image": "[Logo URL]",
     "url": "[Website URL]",
     "telephone": "[Phone Number]",
     "priceRange": "Free Consultation",
     "address": {
       "@type": "PostalAddress",
       "streetAddress": "[Address]",
       "addressLocality": "Dallas",
       "addressRegion": "TX",
       "postalCode": "[ZIP]",
       "addressCountry": "US"
     },
     "geo": {
       "@type": "GeoCoordinates",
       "latitude": [LAT],
       "longitude": [LONG]
     },
     "areaServed": [
       {"@type": "City", "name": "Dallas"},
       {"@type": "City", "name": "Fort Worth"},
       {"@type": "City", "name": "Arlington"},
       {"@type": "City", "name": "Plano"},
       {"@type": "City", "name": "Irving"}
     ],
     "openingHoursSpecification": {
       "@type": "OpeningHoursSpecification",
       "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
       "opens": "08:00",
       "closes": "18:00"
     }
   }
   ```

   **Additional Schema to Implement:**
   - Attorney profiles (Person schema with attorney credentials)
   - FAQ schema on practice area pages
   - Review/Rating schema (aggregate ratings)
   - Breadcrumb schema
   - Article schema for blog posts

### Day 6-7: Technical Issues Resolution

**Tasks:**

1. **Fix Critical Crawl Errors**

   | Issue Type | Priority | Resolution |
   |------------|----------|------------|
   | 404 errors | Critical | Redirect to relevant pages or restore |
   | 500 errors | Critical | Fix server configuration |
   | Redirect chains | High | Consolidate to single redirect |
   | Redirect loops | Critical | Break loop, establish correct target |
   | Orphan pages | Medium | Add internal links or noindex |
   | Duplicate content | High | Canonical tags or consolidate |

2. **URL Structure Optimization**

   **Ideal URL Format:**
   ```
   /[practice-area]/
   /[practice-area]/[location]/
   /blog/[post-title]/
   /about/[attorney-name]/
   ```

   **DFW-Specific URL Examples:**
   ```
   /car-accident-lawyer-dallas/
   /truck-accident-attorney-fort-worth/
   /motorcycle-accident-lawyer-arlington/
   /wrongful-death-attorney-plano/
   ```

3. **XML Sitemap Optimization**
   - Generate dynamic XML sitemap
   - Include only indexable pages
   - Organize by content type:
     - /sitemap-pages.xml
     - /sitemap-posts.xml
     - /sitemap-attorneys.xml
   - Submit to Google Search Console
   - Submit to Bing Webmaster Tools

4. **Robots.txt Audit**
   ```
   User-agent: *
   Allow: /
   Disallow: /wp-admin/
   Disallow: /wp-includes/
   Disallow: /thank-you/
   Disallow: /confirmation/
   Disallow: /*?*

   Sitemap: https://[domain].com/sitemap.xml
   ```

### Week 1 Deliverables Checklist

| Task | Status | Owner | Notes |
|------|--------|-------|-------|
| Complete site crawl | ☐ | | |
| GSC setup/audit | ☐ | | |
| GA4 audit & goals | ☐ | | |
| Core Web Vitals baseline | ☐ | | |
| Mobile audit | ☐ | | |
| Security audit | ☐ | | |
| Schema implementation | ☐ | | |
| Fix critical errors | ☐ | | |
| Sitemap optimization | ☐ | | |
| Robots.txt update | ☐ | | |

### Week 1 KPIs to Establish

| KPI | Baseline Value | Notes |
|-----|----------------|-------|
| Indexed pages | | |
| Crawl errors | | |
| Mobile usability score | | |
| Desktop PageSpeed score | | |
| Mobile PageSpeed score | | |
| Core Web Vitals pass rate | | |
| SSL/Security score | | |

---

## WEEK 2: On-Page Optimization

### Day 8-9: Keyword Research & Mapping

**Tasks:**

1. **Primary Keyword Research**
   - Tool: Ahrefs ($99-199/month) or SEMrush ($129/month)
   - Alternative: Ubersuggest ($29/month)

   **DFW Personal Injury Keyword Categories:**

   **Tier 1: High-Intent Practice Area Keywords**
   | Keyword | Est. Monthly Volume | Difficulty | Priority |
   |---------|---------------------|------------|----------|
   | dallas personal injury lawyer | 1,900 | 65 | 1 |
   | fort worth personal injury attorney | 720 | 55 | 1 |
   | car accident lawyer dallas | 1,600 | 60 | 1 |
   | truck accident attorney dallas | 590 | 50 | 1 |
   | dallas car accident attorney | 1,300 | 58 | 1 |
   | motorcycle accident lawyer dallas | 320 | 45 | 2 |
   | 18 wheeler accident lawyer dallas | 480 | 48 | 1 |
   | wrongful death attorney dallas | 390 | 52 | 2 |
   | slip and fall lawyer dallas | 210 | 40 | 2 |
   | workplace injury attorney dallas | 260 | 42 | 2 |

   **Tier 2: Location Modifier Keywords (DFW Submarkets)**
   | Location | Population | Search Modifier |
   |----------|------------|-----------------|
   | Dallas | 1.3M | [practice] lawyer dallas |
   | Fort Worth | 935K | [practice] attorney fort worth |
   | Arlington | 394K | [practice] lawyer arlington tx |
   | Plano | 287K | [practice] attorney plano |
   | Irving | 256K | [practice] lawyer irving tx |
   | Garland | 246K | [practice] attorney garland tx |
   | Frisco | 219K | [practice] lawyer frisco tx |
   | McKinney | 199K | [practice] attorney mckinney tx |
   | Grand Prairie | 197K | [practice] lawyer grand prairie |
   | Denton | 148K | [practice] attorney denton tx |

   **Tier 3: Long-Tail & Question Keywords**
   ```
   how much is my car accident case worth dallas
   what to do after a car accident in texas
   how long do I have to file a personal injury claim in texas
   best personal injury lawyer in dallas
   free consultation personal injury attorney dallas
   no win no fee lawyer dallas texas
   average car accident settlement in texas
   ```

2. **Keyword Mapping Document**

   Create comprehensive mapping spreadsheet:
   ```
   | URL | Primary Keyword | Secondary Keywords | Search Intent | Content Type |
   |-----|-----------------|-------------------|---------------|--------------|
   | /car-accident-lawyer-dallas/ | car accident lawyer dallas | dallas car accident attorney, auto accident lawyer dallas | Transactional | Landing Page |
   | /truck-accident-attorney-dallas/ | truck accident attorney dallas | 18 wheeler accident lawyer dallas, semi truck accident attorney | Transactional | Landing Page |
   ```

3. **Competitor Keyword Gap Analysis**
   - Tool: Ahrefs Content Gap or SEMrush Keyword Gap

   **Top DFW Competitors to Analyze:**
   - Thompson Law
   - Rasansky Law Firm
   - The Law Offices of Tim O'Hare
   - Tate Law Offices
   - Reyes Browne Reilley

   **Export:**
   - Keywords competitors rank for that you don't
   - Keywords with ranking opportunity (positions 11-30)
   - High-volume keywords with low competition

### Day 10-11: Title Tag & Meta Description Optimization

**Tasks:**

1. **Title Tag Optimization**

   **Formula:**
   ```
   [Primary Keyword] | [Secondary Keyword] | [Brand]
   OR
   [Primary Keyword] - [Value Proposition] | [Brand]
   ```

   **Character Limit:** 50-60 characters

   **DFW-Optimized Title Tag Examples:**

   | Page | Optimized Title Tag |
   |------|---------------------|
   | Homepage | Dallas Personal Injury Lawyers | Free Consultation | [Firm] |
   | Car Accident | Car Accident Lawyer Dallas | No Win, No Fee | [Firm] |
   | Truck Accident | Dallas Truck Accident Attorney | 18-Wheeler Injuries | [Firm] |
   | Fort Worth | Fort Worth Personal Injury Lawyer | Free Consult | [Firm] |
   | Plano | Plano Personal Injury Attorney | Serving Collin County | [Firm] |
   | Arlington | Arlington TX Injury Lawyer | Tarrant County | [Firm] |

2. **Meta Description Optimization**

   **Formula:**
   ```
   [Action verb] + [Primary Keyword] + [Value proposition] + [CTA with urgency]
   ```

   **Character Limit:** 150-160 characters

   **Optimized Meta Description Examples:**

   | Page | Meta Description |
   |------|------------------|
   | Homepage | Injured in Dallas? Our experienced personal injury lawyers fight for maximum compensation. Free consultation, no fee unless we win. Call 24/7: (XXX) XXX-XXXX |
   | Car Accident | Dallas car accident lawyer with $100M+ recovered. We handle insurance companies so you can focus on recovery. Free case review - call now. |
   | Truck Accident | Serious truck accident injuries? Our Dallas 18-wheeler accident attorneys have won millions for victims. Available 24/7. Free consultation today. |

3. **Implement Changes**
   - Update all title tags in CMS
   - Update all meta descriptions
   - Ensure no duplicates across site
   - Track all changes in spreadsheet for monitoring

### Day 12-13: Header & Content Optimization

**Tasks:**

1. **H1 Tag Optimization**
   - One H1 per page
   - Include primary keyword
   - Make it compelling/benefit-focused

   **Examples:**
   | Page | Optimized H1 |
   |------|--------------|
   | Car Accident | Dallas Car Accident Lawyers Fighting for Your Rights |
   | Truck Accident | Experienced Truck Accident Attorneys in Dallas |
   | Homepage | Dallas Personal Injury Lawyers | Millions Recovered |

2. **Header Hierarchy Optimization (H2-H6)**

   **Ideal Structure for Practice Area Page:**
   ```
   H1: Dallas Car Accident Lawyer

   H2: Why Choose [Firm] for Your Car Accident Case
     H3: Proven Track Record
     H3: No Fee Unless We Win
     H3: 24/7 Availability

   H2: Common Car Accident Injuries We Handle
     H3: Whiplash and Neck Injuries
     H3: Traumatic Brain Injuries
     H3: Spinal Cord Injuries
     H3: Broken Bones and Fractures

   H2: What to Do After a Car Accident in Dallas
     H3: Seek Medical Attention
     H3: Document the Scene
     H3: Contact a Lawyer

   H2: Understanding Texas Car Accident Laws
     H3: Statute of Limitations
     H3: Comparative Negligence
     H3: Minimum Insurance Requirements

   H2: Areas We Serve in DFW
     H3: Dallas County
     H3: Tarrant County
     H3: Collin County
     H3: Denton County

   H2: Frequently Asked Questions

   H2: Contact Our Dallas Car Accident Lawyers Today
   ```

3. **Content Optimization Checklist**

   For each landing page, ensure:
   | Element | Requirement | Status |
   |---------|-------------|--------|
   | Word count | Minimum 1,500 words | ☐ |
   | Primary keyword in first 100 words | Yes | ☐ |
   | Primary keyword density | 1-2% | ☐ |
   | LSI keywords included | 5-10 variations | ☐ |
   | Internal links | 3-5 relevant links | ☐ |
   | External links | 1-2 authoritative sources | ☐ |
   | Images with alt text | 3-5 images | ☐ |
   | Call-to-action | Above and below fold | ☐ |
   | Contact information | Phone + form | ☐ |
   | Trust signals | Reviews, awards, results | ☐ |

### Day 14: Internal Linking & Image Optimization

**Tasks:**

1. **Internal Linking Audit & Strategy**
   - Tool: Screaming Frog > Internal Link Report
   - Tool: Sitebulb for visualization

   **Identify:**
   - Pages with low internal link count (<3 inbound links)
   - Orphan pages (no internal links)
   - Top linked pages (ensure they're priority pages)

   **Internal Linking Rules:**
   ```
   1. Every page should have 3-5 internal links pointing to it
   2. Use descriptive anchor text (not "click here")
   3. Link from high-authority pages to pages you want to rank
   4. Create content hubs with hub-and-spoke structure
   5. Add contextual links within body content
   6. Include related practice area links in sidebar/footer
   ```

   **Hub-and-Spoke Model for DFW:**
   ```
   Hub: /personal-injury-lawyer-dallas/
   ├── Spoke: /car-accident-lawyer-dallas/
   ├── Spoke: /truck-accident-attorney-dallas/
   ├── Spoke: /motorcycle-accident-lawyer-dallas/
   ├── Spoke: /wrongful-death-attorney-dallas/
   └── Spoke: /workplace-injury-lawyer-dallas/
   ```

2. **Image Optimization Implementation**

   **For Each Image:**
   - Compress to under 100KB (tool: TinyPNG, ShortPixel)
   - Convert to WebP format with JPEG fallback
   - Add descriptive alt text with keywords
   - Add width and height attributes
   - Implement lazy loading

   **Alt Text Examples:**
   | Image | Optimized Alt Text |
   |-------|-------------------|
   | Car crash scene | Car accident scene in Dallas requiring legal representation |
   | Attorney headshot | John Smith, Dallas personal injury attorney |
   | Office exterior | [Firm Name] law office in downtown Dallas |
   | Courtroom | Dallas County courthouse where personal injury cases are tried |

3. **Create/Update Image Alt Text Spreadsheet**
   ```
   | Image URL | Current Alt | Optimized Alt | Status |
   |-----------|-------------|---------------|--------|
   | /images/hero.jpg | | Dallas car accident lawyer helping client | ☐ |
   ```

### Week 2 Deliverables Checklist

| Task | Status | Owner | Notes |
|------|--------|-------|-------|
| Keyword research complete | ☐ | | |
| Keyword mapping document | ☐ | | |
| Competitor analysis | ☐ | | |
| Title tags optimized | ☐ | | |
| Meta descriptions optimized | ☐ | | |
| H1 tags optimized | ☐ | | |
| Header hierarchy fixed | ☐ | | |
| Content optimization (existing pages) | ☐ | | |
| Internal linking improvements | ☐ | | |
| Image optimization | ☐ | | |

### Week 2 KPIs to Track

| KPI | Baseline | Week 2 | Change |
|-----|----------|--------|--------|
| Pages with optimized titles | | | |
| Pages with meta descriptions | | | |
| Average content length | | | |
| Internal links per page | | | |
| Images with alt text | | | |

---

## WEEK 3: Local SEO Setup

### Day 15-16: Google Business Profile Optimization

**Tasks:**

1. **GBP Claim/Verification**
   - Go to business.google.com
   - Search for existing listing or create new
   - Verify via postcard, phone, email, or instant verification
   - If multiple locations, set up location groups

   **Verification Timeline:**
   - Postcard: 5-14 days
   - Phone: Instant (if available)
   - Email: Instant (if available)
   - Video verification: 24-48 hours

2. **Complete GBP Optimization**

   **Business Information:**
   | Field | Requirement | Example |
   |-------|-------------|---------|
   | Business Name | Exact legal name (no keyword stuffing) | [Firm Name] |
   | Primary Category | Personal Injury Attorney | Personal Injury Attorney |
   | Secondary Categories | Add 2-5 relevant | Lawyer, Legal Services, Accident Attorney |
   | Address | Full street address | 123 Main St, Suite 500, Dallas, TX 75201 |
   | Service Area | Define DFW cities | Dallas, Fort Worth, Arlington, Plano, Irving, etc. |
   | Phone | Local number (214 or 972) | (214) XXX-XXXX |
   | Website | Primary URL | https://www.[firm].com |
   | Hours | Include all hours | Mon-Fri: 8AM-6PM, Sat-Sun: By Appointment |
   | Special Hours | Holidays | Set holiday hours |

   **Business Description (750 characters):**
   ```
   [Firm Name] is a leading Dallas personal injury law firm serving
   clients throughout the DFW metroplex. Our experienced attorneys
   have recovered millions of dollars for victims of car accidents,
   truck accidents, workplace injuries, and wrongful death. We handle
   cases in Dallas, Fort Worth, Arlington, Plano, Irving, and
   surrounding communities. With a no-win, no-fee guarantee, you pay
   nothing unless we recover compensation for your injuries. Contact
   us 24/7 for a free consultation with a dedicated personal injury
   lawyer who will fight for your rights.
   ```

3. **GBP Media Optimization**

   **Required Photos (minimum):**
   | Type | Quantity | Specifications |
   |------|----------|----------------|
   | Logo | 1 | 250x250px, PNG |
   | Cover photo | 1 | 1080x608px |
   | Office exterior | 3-5 | Show signage, building |
   | Office interior | 5-10 | Reception, conference rooms |
   | Team photos | All attorneys | Professional headshots |
   | At work photos | 3-5 | Attorneys working, meetings |

   **Photo Naming Convention:**
   ```
   dallas-personal-injury-lawyer-office-exterior.jpg
   [attorney-name]-dallas-injury-attorney.jpg
   [firm-name]-conference-room-dallas.jpg
   ```

4. **GBP Services Setup**

   **Add Services:**
   - Car Accident Representation
   - Truck Accident Claims
   - Motorcycle Accident Cases
   - Wrongful Death Lawsuits
   - Workplace Injury Claims
   - Slip and Fall Cases
   - Medical Malpractice
   - Product Liability

   For each service, add description and pricing (Free Consultation)

5. **GBP Products (if applicable)**
   - Free Case Evaluation
   - Free Legal Consultation
   - Case Settlement Calculator

6. **GBP Attributes**

   Enable relevant attributes:
   - Online appointments
   - Wheelchair accessible
   - Free Wi-Fi
   - LGBTQ+ friendly
   - Identifies as veteran-owned (if applicable)
   - Identifies as women-owned (if applicable)

### Day 17-18: Citation Building Foundation

**Tasks:**

1. **NAP Consistency Audit**
   - Tool: Moz Local ($99/year)
   - Tool: BrightLocal ($39/month)
   - Tool: Whitespark ($41/month)

   **Verify NAP is identical across:**
   - Website footer
   - Website contact page
   - Google Business Profile
   - All existing citations

   **NAP Format (standardize):**
   ```
   [Firm Name]
   123 Main Street, Suite 500
   Dallas, TX 75201
   (214) 555-1234
   ```

2. **Primary Data Aggregator Submissions**

   These feed data to hundreds of directories:
   | Aggregator | Cost | Submission URL |
   |------------|------|----------------|
   | Data Axle (Infogroup) | Free | expressupdate.com |
   | Neustar/Localeze | Free | neustarlocaleze.biz |
   | Foursquare | Free | foursquare.com/business |
   | Apple Maps | Free | mapsconnect.apple.com |

3. **Tier 1 Legal Directory Submissions**

   | Directory | DA | Priority | Cost |
   |-----------|-----|----------|------|
   | Avvo | 92 | Critical | Free/Premium |
   | FindLaw | 90 | Critical | Paid listing |
   | Justia | 88 | Critical | Free/Premium |
   | Martindale-Hubbell | 85 | Critical | Paid listing |
   | Super Lawyers | 83 | High | By invitation/paid |
   | Lawyers.com | 82 | High | Paid listing |
   | Nolo | 79 | High | Free/Premium |
   | HG.org | 71 | Medium | Free listing |
   | Lawinfo.com | 68 | Medium | Paid listing |
   | Best Lawyers | 78 | High | By invitation |

4. **Tier 2 General Business Directories**

   | Directory | DA | Priority |
   |-----------|-----|----------|
   | Yelp | 94 | Critical |
   | BBB | 91 | Critical |
   | Yellow Pages | 85 | High |
   | Bing Places | 94 | Critical |
   | Apple Maps | 100 | Critical |
   | Facebook Business | 96 | Critical |
   | LinkedIn Company Page | 98 | Critical |
   | Manta | 65 | Medium |
   | Citysearch | 58 | Medium |
   | Local.com | 54 | Low |

5. **Create Citation Tracking Spreadsheet**
   ```
   | Directory | URL | Submission Date | Status | Login Info | Notes |
   |-----------|-----|-----------------|--------|------------|-------|
   | Avvo | | | | | |
   | FindLaw | | | | | |
   ```

### Day 19-20: Local Schema & Geo-Targeting

**Tasks:**

1. **Implement Local Business Schema**

   **Homepage Schema:**
   ```json
   {
     "@context": "https://schema.org",
     "@type": "LegalService",
     "@id": "https://[domain].com/#organization",
     "name": "[Firm Name]",
     "alternateName": "[Firm Name] Personal Injury Lawyers",
     "url": "https://[domain].com",
     "logo": "https://[domain].com/logo.png",
     "image": "https://[domain].com/office.jpg",
     "description": "Dallas personal injury law firm...",
     "telephone": "(214) XXX-XXXX",
     "email": "info@[domain].com",
     "priceRange": "Free Consultation",
     "currenciesAccepted": "USD",
     "paymentAccepted": "Contingency Fee",
     "address": {
       "@type": "PostalAddress",
       "streetAddress": "123 Main Street, Suite 500",
       "addressLocality": "Dallas",
       "addressRegion": "TX",
       "postalCode": "75201",
       "addressCountry": "US"
     },
     "geo": {
       "@type": "GeoCoordinates",
       "latitude": 32.7767,
       "longitude": -96.7970
     },
     "hasMap": "https://maps.google.com/?cid=XXXXX",
     "openingHoursSpecification": [
       {
         "@type": "OpeningHoursSpecification",
         "dayOfWeek": ["Monday","Tuesday","Wednesday","Thursday","Friday"],
         "opens": "08:00",
         "closes": "18:00"
       }
     ],
     "areaServed": [
       {"@type": "City", "name": "Dallas", "sameAs": "https://en.wikipedia.org/wiki/Dallas"},
       {"@type": "City", "name": "Fort Worth"},
       {"@type": "City", "name": "Arlington"},
       {"@type": "City", "name": "Plano"},
       {"@type": "City", "name": "Irving"},
       {"@type": "City", "name": "Garland"},
       {"@type": "City", "name": "Grand Prairie"},
       {"@type": "City", "name": "McKinney"},
       {"@type": "City", "name": "Frisco"},
       {"@type": "City", "name": "Denton"}
     ],
     "sameAs": [
       "https://www.facebook.com/[firm]",
       "https://www.linkedin.com/company/[firm]",
       "https://twitter.com/[firm]"
     ],
     "aggregateRating": {
       "@type": "AggregateRating",
       "ratingValue": "4.9",
       "reviewCount": "127"
     }
   }
   ```

2. **Attorney Schema for Each Lawyer**
   ```json
   {
     "@context": "https://schema.org",
     "@type": "Attorney",
     "name": "John Smith",
     "jobTitle": "Personal Injury Attorney",
     "image": "https://[domain].com/john-smith.jpg",
     "url": "https://[domain].com/about/john-smith/",
     "telephone": "(214) XXX-XXXX",
     "email": "jsmith@[domain].com",
     "worksFor": {
       "@type": "LegalService",
       "name": "[Firm Name]"
     },
     "alumniOf": {
       "@type": "CollegeOrUniversity",
       "name": "SMU Dedman School of Law"
     },
     "knowsAbout": ["Personal Injury Law", "Car Accidents", "Truck Accidents"],
     "areaServed": "Dallas-Fort Worth"
   }
   ```

3. **Location Page Schema (for each city page)**
   - Implement on Fort Worth, Arlington, Plano pages
   - Include city-specific address if satellite office
   - Otherwise use service area schema

4. **GeoTargeting Implementation**
   - Add hreflang tags if multilingual (English/Spanish for DFW)
   - Set geographic target in Search Console
   - Include city names in strategic locations:
     - Footer
     - About page
     - Contact page
     - Service area page

### Day 21: Review Strategy Setup

**Tasks:**

1. **Review Platform Prioritization**

   | Platform | Priority | Target Reviews |
   |----------|----------|----------------|
   | Google Business Profile | Critical | 50+ (90-day goal) |
   | Avvo | High | 25+ |
   | Facebook | High | 20+ |
   | Yelp | Medium | 15+ |
   | Lawyers.com | Medium | 10+ |

2. **Review Generation System**

   **Create Review Request Email Template:**
   ```
   Subject: Would you share your experience with [Firm Name]?

   Dear [Client Name],

   It was our pleasure to represent you in your [case type] matter.
   We hope you're doing well and that the outcome has provided the
   closure you deserved.

   If you were satisfied with our services, we would greatly
   appreciate if you could take a moment to share your experience.
   Your feedback helps others who are searching for legal help
   after an accident.

   Leave a Google Review: [Direct Link]

   Thank you for trusting [Firm Name] with your case.

   Best regards,
   [Attorney Name]
   ```

3. **Set Up Review Monitoring**
   - Tool: Google Alerts for firm name
   - Tool: ReviewTrackers or BirdEye
   - Set up Slack/email notifications for new reviews
   - Create review response templates (positive and negative)

4. **Review Response Templates**

   **Positive Review Response:**
   ```
   Thank you so much for your kind words, [Name]. It was our
   privilege to represent you, and we're thrilled we could help
   you get the compensation you deserved. We wish you continued
   healing and success. If you ever need anything in the future,
   please don't hesitate to reach out.

   - [Attorney Name], [Firm Name]
   ```

   **Negative Review Response:**
   ```
   [Name], we're sorry to hear about your experience and take
   your feedback seriously. We strive to provide excellent service
   to all our clients. Please contact our office at (214) XXX-XXXX
   so we can discuss your concerns and work toward a resolution.
   Thank you for bringing this to our attention.

   - [Attorney Name], [Firm Name]
   ```

### Week 3 Deliverables Checklist

| Task | Status | Owner | Notes |
|------|--------|-------|-------|
| GBP claimed and verified | ☐ | | |
| GBP fully optimized | ☐ | | |
| GBP photos uploaded (20+) | ☐ | | |
| Data aggregator submissions | ☐ | | |
| Tier 1 legal citations (10) | ☐ | | |
| Tier 2 business citations (10) | ☐ | | |
| Local schema implemented | ☐ | | |
| Attorney schema implemented | ☐ | | |
| Review system established | ☐ | | |
| Citation tracking spreadsheet | ☐ | | |

### Week 3 KPIs to Track

| KPI | Target | Actual | Notes |
|-----|--------|--------|-------|
| GBP completeness score | 100% | | |
| Citations submitted | 20+ | | |
| Google reviews | 5+ | | |
| GBP views | Track baseline | | |
| GBP actions (calls, directions) | Track baseline | | |

---

## WEEK 4: Content Foundation

### Day 22-23: Content Audit & Strategy

**Tasks:**

1. **Existing Content Audit**
   - Tool: Screaming Frog
   - Tool: Google Analytics 4

   **Evaluate Each Page:**
   | URL | Word Count | Organic Traffic | Conversions | Quality Score | Action |
   |-----|-----------|-----------------|-------------|---------------|--------|
   | | | | | 1-5 | Keep/Update/Merge/Delete |

   **Quality Scoring Criteria:**
   - 5: Excellent - ranking well, driving conversions
   - 4: Good - solid content, minor updates needed
   - 3: Average - needs significant refresh
   - 2: Poor - thin content, rewrite needed
   - 1: Delete - duplicate or irrelevant

2. **Content Gap Analysis**
   - Tool: Ahrefs Content Gap
   - Tool: SEMrush Topic Research

   **Identify Missing Content:**
   - Practice areas without dedicated pages
   - Location pages needed
   - FAQ content gaps
   - Blog topics competitors cover

3. **DFW Content Strategy Development**

   **Content Pillars:**
   ```
   Pillar 1: Car Accidents in DFW
   ├── Types of car accidents
   ├── Common injuries
   ├── Texas car accident laws
   ├── Insurance claims process
   └── Settlement process

   Pillar 2: Truck/18-Wheeler Accidents
   ├── Commercial trucking regulations
   ├── Common causes
   ├── Determining liability
   ├── Federal regulations
   └── Case complexity

   Pillar 3: DFW Location Content
   ├── Dallas neighborhoods
   ├── Major highways (I-35, I-30, 635, etc.)
   ├── County-specific content
   └── Local statistics

   Pillar 4: Texas Personal Injury Law
   ├── Statute of limitations
   ├── Comparative negligence
   ├── Damage caps
   ├── Insurance requirements
   └── Settlement vs trial
   ```

4. **Create Editorial Calendar (Months 1-3)**

   **Template:**
   | Week | Content Type | Topic | Target Keyword | Author | Status |
   |------|--------------|-------|----------------|--------|--------|
   | 5 | Landing Page | Car Accident Lawyer Dallas | car accident lawyer dallas | | |
   | 5 | Landing Page | Truck Accident Attorney | truck accident attorney dallas | | |
   | 6 | Landing Page | Fort Worth PI Lawyer | personal injury lawyer fort worth | | |
   | 7 | Blog Post | What to Do After Accident | after car accident dallas | | |
   | 8 | Blog Post | Settlement Timeline | how long car accident settlement texas | | |

### Day 24-25: Content Templates & Guidelines

**Tasks:**

1. **Practice Area Landing Page Template**

   **Structure (2,000-3,000 words):**
   ```
   [Hero Section]
   - H1: Keyword-optimized headline
   - Subheadline: Value proposition
   - CTA button: Free Consultation
   - Trust signals: Awards, reviews, results

   [Section 1: Introduction] ~200 words
   - Hook addressing pain point
   - Empathy statement
   - Brief firm introduction
   - Primary keyword in first paragraph

   [Section 2: Why Choose Us] ~300 words
   - H2: Why Choose [Firm] for Your [Practice Area] Case
   - 3-4 differentiators with H3s
   - Case results (redacted)
   - Testimonial quote

   [Section 3: Types of Cases] ~400 words
   - H2: Types of [Practice Area] Cases We Handle
   - Bulleted list with brief descriptions
   - Internal links to sub-pages

   [Section 4: Common Injuries] ~300 words
   - H2: Common Injuries in [Practice Area] Cases
   - List of injuries with descriptions
   - Compensation information

   [Section 5: Legal Process] ~400 words
   - H2: The [Practice Area] Legal Process in Texas
   - Step-by-step timeline
   - What to expect

   [Section 6: Texas Laws] ~300 words
   - H2: Texas [Practice Area] Laws You Should Know
   - Statute of limitations
   - Comparative fault
   - Damage caps (if applicable)

   [Section 7: FAQ] ~300 words
   - H2: Frequently Asked Questions
   - 5-7 questions with schema markup
   - Link to full FAQ page

   [Section 8: Areas Served] ~200 words
   - H2: Serving Accident Victims Throughout DFW
   - List of cities served
   - Map embed

   [Section 9: CTA] ~100 words
   - H2: Contact Our [Location] [Practice Area] Lawyers Today
   - Phone number
   - Contact form
   - Office address
   ```

2. **Location Page Template**

   **Structure (1,500-2,000 words):**
   ```
   [Hero Section]
   - H1: [City] Personal Injury Lawyers
   - City-specific imagery
   - Local phone number (if available)

   [Section 1: Local Introduction] ~200 words
   - Reference to city/community
   - Local statistics (accidents, population)
   - Connection to community

   [Section 2: Services in City] ~300 words
   - H2: Personal Injury Services in [City]
   - List of practice areas
   - Links to practice area pages

   [Section 3: Local Expertise] ~300 words
   - H2: Why Choose a [City] Personal Injury Lawyer
   - Knowledge of local courts
   - Relationships with local medical providers
   - Understanding of local juries

   [Section 4: Local Hazards] ~300 words
   - H2: Common Accident Locations in [City]
   - Dangerous intersections
   - Highway statistics
   - Construction zones

   [Section 5: Local Resources] ~200 words
   - H2: [City] Legal and Medical Resources
   - Local courthouse information
   - Hospital/ER locations
   - Police department contacts

   [Section 6: Testimonials] ~150 words
   - H2: What [City] Clients Say About Us
   - Local client testimonials

   [Section 7: Contact] ~150 words
   - H2: Contact Our [City] Office
   - Address (if office exists)
   - Service area statement (if no office)
   - Contact form
   - Map embed
   ```

3. **Blog Post Template**

   **Structure (1,200-1,800 words):**
   ```
   [Featured Image]
   - Relevant, optimized image
   - Alt text with keyword

   [Introduction] ~150 words
   - Hook
   - Problem statement
   - Preview of content
   - Table of contents (for longer posts)

   [Main Content] ~800-1200 words
   - H2 sections (3-5)
   - H3 subsections as needed
   - Bulleted/numbered lists
   - Statistics with citations
   - Images/infographics

   [Key Takeaways] ~100 words
   - Bulleted summary

   [CTA Section] ~100 words
   - Related to topic
   - Consultation offer
   - Internal links to practice areas

   [Author Bio]
   - Attorney photo
   - Brief bio
   - Credentials
   ```

4. **Content Style Guide**

   **Voice & Tone:**
   - Professional but approachable
   - Empathetic and understanding
   - Confident but not boastful
   - Clear and jargon-free

   **Formatting Standards:**
   - Paragraphs: 3-4 sentences max
   - Sentences: 20 words average
   - Reading level: 8th-9th grade
   - Active voice preferred

   **SEO Requirements:**
   - Primary keyword in H1, first paragraph, and 1-2 H2s
   - Secondary keywords in remaining H2s
   - Keyword density: 1-2%
   - Internal links: 3-5 per page
   - External links: 1-2 authoritative sources
   - Image alt text: Descriptive with keyword

### Day 26-27: Core Page Content Development

**Tasks:**

1. **Homepage Content Enhancement**

   **Required Elements:**
   - Hero with clear value proposition
   - Practice area overview with links
   - Case results (anonymized)
   - Client testimonials (3-5)
   - Attorney introduction
   - Areas served in DFW
   - Trust badges/awards
   - Multiple CTAs
   - Contact information

2. **About Page Optimization**

   **Required Elements:**
   - Firm story and mission
   - Founding date and history
   - Community involvement
   - Awards and recognition
   - Professional affiliations
   - Team photo

   **DFW-Specific Content:**
   - Why the firm serves DFW
   - Local roots/connections
   - Community involvement in Dallas/Fort Worth

3. **Contact Page Enhancement**

   **Required Elements:**
   - Multiple contact methods (phone, email, form)
   - Office address with map embed
   - Hours of operation
   - Free consultation offer
   - Response time expectation
   - Service area list

   **DFW-Specific:**
   - Driving directions from major highways
   - Parking information
   - Public transit options
   - List of cities served

4. **Attorney Bio Pages**

   **For Each Attorney:**
   - Professional photo
   - Name and title
   - Practice area focus
   - Education (law school, undergrad)
   - Bar admissions
   - Professional associations
   - Awards/recognitions
   - Speaking engagements
   - Publications
   - Personal interests (humanizing)
   - Case results
   - Contact information

### Day 28: FAQ & Supporting Content

**Tasks:**

1. **Main FAQ Page Creation**

   **DFW Personal Injury FAQs to Include:**

   **General Questions:**
   - How much does a personal injury lawyer cost?
   - How long will my case take?
   - What is my case worth?
   - Do I have to go to court?
   - What if I can't afford medical treatment?

   **Texas-Specific Questions:**
   - What is the statute of limitations in Texas?
   - How does Texas comparative fault work?
   - What are the minimum insurance requirements in Texas?
   - Can I sue if I was partially at fault?

   **DFW-Specific Questions:**
   - Which courts handle personal injury cases in Dallas?
   - What are the most dangerous roads in DFW?
   - How do I report an accident in Dallas/Fort Worth?

   **Practice Area Questions:**
   - What should I do after a car accident?
   - How are truck accident cases different?
   - What compensation can I receive for my injuries?

2. **Process/How It Works Page**

   **Content:**
   - Step 1: Free Consultation
   - Step 2: Case Investigation
   - Step 3: Medical Treatment Coordination
   - Step 4: Demand and Negotiation
   - Step 5: Litigation (if necessary)
   - Step 6: Settlement or Verdict

   Each step includes: description, timeline, what client can expect

3. **Results/Case Results Page**

   **Format:**
   - Case type
   - Brief description
   - Settlement/verdict amount
   - Timeline
   - (All anonymized/redacted as required)

   **Categories:**
   - Car Accidents
   - Truck Accidents
   - Wrongful Death
   - Workplace Injuries

4. **Service Area Page**

   **Content:**
   - Introduction to DFW service area
   - Interactive map
   - List of cities served (linked to location pages)
   - County breakdown
   - Distance willing to travel
   - Virtual consultation options

### Week 4 Deliverables Checklist

| Task | Status | Owner | Notes |
|------|--------|-------|-------|
| Content audit complete | ☐ | | |
| Content gap analysis | ☐ | | |
| Editorial calendar (3 months) | ☐ | | |
| Landing page template | ☐ | | |
| Location page template | ☐ | | |
| Blog post template | ☐ | | |
| Content style guide | ☐ | | |
| Homepage content enhanced | ☐ | | |
| About page optimized | ☐ | | |
| Contact page enhanced | ☐ | | |
| Attorney bios complete | ☐ | | |
| FAQ page created | ☐ | | |
| Process page created | ☐ | | |
| Results page created | ☐ | | |
| Service area page created | ☐ | | |

### Week 4 KPIs to Track

| KPI | Baseline | End of Week 4 | Notes |
|-----|----------|---------------|-------|
| Total indexed pages | | | |
| Total word count (site) | | | |
| Pages with 1,500+ words | | | |
| FAQ questions covered | | | |
| Content templates created | | 4 | |

---

# MONTH 1 COMPLETION CHECKPOINT

## Summary of Month 1 Accomplishments

| Category | Tasks Completed | Status |
|----------|-----------------|--------|
| Technical SEO | Site crawl, speed optimization, schema | ☐ |
| On-Page SEO | Keywords, titles, meta, headers | ☐ |
| Local SEO | GBP, citations, reviews | ☐ |
| Content | Templates, core pages, strategy | ☐ |

## Month 1 KPI Dashboard

| Metric | Baseline | Month 1 | Target | Status |
|--------|----------|---------|--------|--------|
| Indexed Pages | | | +20% | |
| Technical Errors | | | 0 critical | |
| PageSpeed Mobile | | | 70+ | |
| GBP Views | | | Track | |
| Citations Live | 0 | | 20+ | |
| Google Reviews | | | 5+ | |
| Organic Traffic | | | Track | |

---

# MONTH 2: CONTENT EXPANSION

## WEEKS 5-6: Core Landing Page Creation

### Week 5: Primary Practice Area Pages

**Tasks:**

**Day 29-30: Car Accident Landing Page**

Create comprehensive car accident page targeting "car accident lawyer dallas"

**Page Requirements:**
- URL: /car-accident-lawyer-dallas/
- Word count: 2,500-3,000 words
- Target keyword: car accident lawyer dallas
- Secondary: dallas car accident attorney, auto accident lawyer dallas tx

**Content Sections:**
1. Hero with compelling headline and CTA
2. Why choose our Dallas car accident lawyers (differentiators)
3. Types of car accidents we handle:
   - Rear-end collisions
   - T-bone accidents
   - Head-on collisions
   - Side-swipe accidents
   - Multi-vehicle pileups
   - Hit and run accidents
   - Uber/Lyft accidents
   - Uninsured motorist claims
4. Common car accident injuries
5. What to do after a car accident in Dallas (step-by-step)
6. Texas car accident laws (statute of limitations, fault rules)
7. How car accident settlements work
8. DFW-specific: dangerous intersections and highways
9. FAQs (5-7 questions with schema)
10. Contact section with form

**On-Page Optimization:**
- Title: Car Accident Lawyer Dallas | Free Consultation | [Firm]
- Meta: Injured in a Dallas car accident? Our experienced attorneys have recovered millions. Free consultation, no fee unless we win. Call 24/7.
- H1: Dallas Car Accident Lawyers Fighting for Maximum Compensation
- Schema: FAQPage, LegalService

**Day 31-32: Truck Accident Landing Page**

Create comprehensive truck accident page targeting "truck accident attorney dallas"

**Page Requirements:**
- URL: /truck-accident-attorney-dallas/
- Word count: 2,500-3,000 words
- Target keyword: truck accident attorney dallas
- Secondary: 18 wheeler accident lawyer dallas, semi truck accident attorney

**Content Sections:**
1. Hero emphasizing complexity of truck cases
2. Why truck accidents require specialized attorneys
3. Types of truck accidents:
   - 18-wheeler accidents
   - Semi-truck collisions
   - Commercial truck accidents
   - Delivery truck accidents
   - Tanker accidents
   - Wide-turn accidents
   - Jackknife accidents
   - Underride accidents
4. Common causes (driver fatigue, overloading, maintenance)
5. Determining liability (multiple parties)
6. Federal trucking regulations (FMCSA)
7. Catastrophic injuries in truck accidents
8. DFW trucking corridors (I-35, I-20, I-30)
9. FAQs (5-7 questions)
10. Contact section

**Day 33-35: Additional Practice Area Pages**

Create pages for remaining high-priority practice areas:

**Motorcycle Accident Page:**
- URL: /motorcycle-accident-lawyer-dallas/
- Word count: 2,000-2,500 words
- Focus: Unique challenges, bias against riders, severity of injuries

**Wrongful Death Page:**
- URL: /wrongful-death-attorney-dallas/
- Word count: 2,000-2,500 words
- Focus: Compassionate tone, eligible survivors, types of damages

**Workplace Injury Page:**
- URL: /workplace-injury-lawyer-dallas/
- Word count: 2,000-2,500 words
- Focus: Workers' comp vs third-party claims, Texas opt-out employers

### Week 6: Location Pages

**Day 36-37: Fort Worth Location Page**

**Page Requirements:**
- URL: /personal-injury-lawyer-fort-worth/
- Word count: 1,800-2,200 words
- Target keyword: personal injury lawyer fort worth
- Secondary: fort worth injury attorney, accident lawyer fort worth tx

**Unique Content:**
- Fort Worth-specific statistics
- Tarrant County courthouse information
- Local hospitals (JPS, Harris, Texas Health)
- Dangerous roads (I-30, I-35W, 820)
- Fort Worth community connection

**Day 38-39: Arlington Location Page**

**Page Requirements:**
- URL: /personal-injury-attorney-arlington-tx/
- Word count: 1,500-1,800 words
- Target keyword: personal injury attorney arlington tx

**Unique Content:**
- Arlington's position between Dallas and Fort Worth
- AT&T Stadium and Globe Life Field event traffic
- Major highways (I-30, SH-360)
- Arlington police/hospital information
- No public transportation unique challenges

**Day 40-42: Additional Priority Location Pages**

Create location pages for:

| City | URL | Word Count | Target Keyword |
|------|-----|------------|----------------|
| Plano | /personal-injury-lawyer-plano/ | 1,500 | personal injury lawyer plano |
| Irving | /accident-attorney-irving-tx/ | 1,500 | accident attorney irving tx |
| Garland | /injury-lawyer-garland-tx/ | 1,200 | injury lawyer garland texas |
| Grand Prairie | /personal-injury-grand-prairie/ | 1,200 | personal injury lawyer grand prairie |

**For Each Location Page Include:**
- City-specific accident statistics
- Local court information
- Hospital/medical facility references
- Major road/highway information
- Community connection statement
- Service area map
- Contact information

### Weeks 5-6 Deliverables Checklist

| Task | Status | Word Count | Target KW | Owner |
|------|--------|------------|-----------|-------|
| Car accident page | ☐ | 2,500+ | car accident lawyer dallas | |
| Truck accident page | ☐ | 2,500+ | truck accident attorney dallas | |
| Motorcycle accident page | ☐ | 2,000+ | motorcycle accident lawyer dallas | |
| Wrongful death page | ☐ | 2,000+ | wrongful death attorney dallas | |
| Workplace injury page | ☐ | 2,000+ | workplace injury lawyer dallas | |
| Fort Worth page | ☐ | 1,800+ | personal injury lawyer fort worth | |
| Arlington page | ☐ | 1,500+ | personal injury attorney arlington | |
| Plano page | ☐ | 1,500+ | personal injury lawyer plano | |
| Irving page | ☐ | 1,500+ | accident attorney irving | |
| Garland page | ☐ | 1,200+ | injury lawyer garland | |
| Grand Prairie page | ☐ | 1,200+ | personal injury grand prairie | |

### Weeks 5-6 KPIs

| KPI | Target | Actual |
|-----|--------|--------|
| New pages published | 11 | |
| Total new word count | 20,000+ | |
| Pages indexed (within 2 weeks) | 11 | |
| Internal links added | 50+ | |

---

## WEEKS 7-8: Blog Content Launch

### Week 7: Foundation Blog Posts

**Day 43-44: Pillar Blog Post #1**

**Topic:** Complete Guide to Car Accident Claims in Texas
- URL: /blog/car-accident-claims-texas-complete-guide/
- Word count: 3,000-4,000 words
- Target keyword: car accident claim texas

**Comprehensive Outline:**
```
H1: The Complete Guide to Car Accident Claims in Texas (2026)

H2: Understanding Texas Car Accident Laws
  H3: At-Fault vs No-Fault: Texas Rules
  H3: Statute of Limitations (2 Years)
  H3: Comparative Negligence in Texas

H2: Steps to Take After a Car Accident
  H3: At the Scene
  H3: Within 24 Hours
  H3: Within the First Week
  H3: Ongoing Steps

H2: Types of Compensation Available
  H3: Medical Expenses
  H3: Lost Wages
  H3: Pain and Suffering
  H3: Property Damage
  H3: Future Damages

H2: The Insurance Claim Process
  H3: Filing Your Claim
  H3: Dealing with Adjusters
  H3: Common Insurance Tactics
  H3: When to Accept vs Negotiate

H2: When to Hire a Car Accident Lawyer
  H3: Signs You Need Legal Help
  H3: What a Lawyer Does for Your Case
  H3: Contingency Fee Arrangements

H2: Timeline: How Long Will Your Case Take?
  H3: Settlement Timeline
  H3: Litigation Timeline
  H3: Factors That Affect Duration

H2: Frequently Asked Questions

H2: Get Help with Your Texas Car Accident Claim
```

**Day 45-46: Pillar Blog Post #2**

**Topic:** Truck Accident Lawsuits: What Makes Them Different
- URL: /blog/truck-accident-lawsuits-what-makes-them-different/
- Word count: 2,500-3,000 words
- Target keyword: truck accident lawsuit

**Day 47-49: Supporting Blog Posts**

Create 4 supporting blog posts (1,200-1,500 words each):

| Post Title | Target Keyword | Type |
|------------|----------------|------|
| What to Do Immediately After a Car Accident in Dallas | what to do after car accident dallas | How-to |
| How Long Does a Personal Injury Case Take in Texas? | how long personal injury case texas | Informational |
| Texas Statute of Limitations for Personal Injury: What You Need to Know | texas statute of limitations personal injury | Legal guide |
| Average Car Accident Settlement in Texas: What to Expect | average car accident settlement texas | Data-driven |

### Week 8: Topical Blog Expansion

**Day 50-51: Local/DFW-Focused Content**

Create DFW-specific blog posts (1,200-1,500 words each):

| Post Title | Target Keyword | Angle |
|------------|----------------|-------|
| Most Dangerous Intersections in Dallas: A Data-Driven Analysis | dangerous intersections dallas | Local data |
| I-35 Accidents in DFW: Causes, Statistics, and Legal Rights | i-35 accidents dallas | Highway focus |
| What to Know About Filing a Car Accident Claim in Dallas County | car accident claim dallas county | Local process |

**Day 52-54: Question-Targeted Content**

Create FAQ-style posts targeting question keywords:

| Post Title | Target Keyword |
|------------|----------------|
| How Much Is My Car Accident Case Worth? | how much is my car accident case worth |
| Do I Need a Lawyer for a Minor Car Accident? | do i need lawyer for minor car accident |
| Can I Sue If I Was Partially At Fault in Texas? | can i sue if partially at fault texas |
| What Happens If the Other Driver Doesn't Have Insurance? | other driver no insurance texas |

**Day 55-56: Injury-Focused Content**

Create injury-specific content:

| Post Title | Target Keyword |
|------------|----------------|
| Whiplash After a Car Accident: Symptoms, Treatment & Compensation | whiplash car accident compensation |
| Traumatic Brain Injuries in Car Accidents: Long-Term Impact | traumatic brain injury car accident |
| Back Injuries from Car Accidents: Types and Legal Recovery | back injury car accident settlement |

### Blog Content Guidelines

**Publishing Schedule:**
- Week 7: 6 posts (2 pillar + 4 supporting)
- Week 8: 9 posts (3 local + 4 FAQ + 2 injury)
- Total: 15 blog posts in 2 weeks

**Internal Linking Strategy:**
```
Pillar Post: Car Accident Claims Guide
├── Links TO: All car accident-related supporting posts
├── Links FROM: All car accident supporting posts
├── Links TO: Car accident landing page
└── Links TO: Contact page

Supporting Posts:
├── Link to relevant pillar post
├── Link to relevant practice area page
├── Link to 1-2 other supporting posts
└── Link to contact/consultation page
```

**Blog Post Optimization Checklist:**
| Element | Requirement |
|---------|-------------|
| Title tag | Keyword + compelling hook, <60 char |
| Meta description | Keyword + benefit + CTA, <160 char |
| H1 | Keyword-optimized, matches title |
| URL | Short, keyword-rich |
| Featured image | Optimized, relevant, with alt text |
| Word count | 1,200+ (supporting), 2,500+ (pillar) |
| Internal links | 3-5 minimum |
| External links | 1-2 authoritative sources |
| CTA | Contact form or phone number |
| Schema | Article schema implemented |
| Categories/tags | Properly categorized |

### Weeks 7-8 Deliverables Checklist

| Post | Status | Words | Published | Indexed |
|------|--------|-------|-----------|---------|
| Car Accident Claims Guide | ☐ | 3,000+ | | |
| Truck Accident Lawsuits | ☐ | 2,500+ | | |
| What to Do After Accident | ☐ | 1,200+ | | |
| How Long Does Case Take | ☐ | 1,200+ | | |
| Statute of Limitations | ☐ | 1,200+ | | |
| Average Settlement Texas | ☐ | 1,200+ | | |
| Dangerous Intersections Dallas | ☐ | 1,200+ | | |
| I-35 Accidents DFW | ☐ | 1,200+ | | |
| Dallas County Claims | ☐ | 1,200+ | | |
| Case Worth | ☐ | 1,200+ | | |
| Minor Accident Lawyer | ☐ | 1,200+ | | |
| Partially At Fault | ☐ | 1,200+ | | |
| Uninsured Driver | ☐ | 1,200+ | | |
| Whiplash Compensation | ☐ | 1,200+ | | |
| TBI Car Accident | ☐ | 1,200+ | | |

### Weeks 7-8 KPIs

| KPI | Target | Actual |
|-----|--------|--------|
| Blog posts published | 15 | |
| Total blog word count | 22,000+ | |
| Posts indexed (within 2 weeks) | 15 | |
| Organic blog traffic | Track baseline | |
| Blog engagement (time on page) | >2 min avg | |

---

# MONTH 2 COMPLETION CHECKPOINT

## Summary of Month 2 Accomplishments

| Category | Tasks Completed | Status |
|----------|-----------------|--------|
| Practice Area Pages | 5 core pages created | ☐ |
| Location Pages | 6 DFW city pages | ☐ |
| Blog Content | 15 posts published | ☐ |
| Internal Linking | Structure established | ☐ |

## Month 2 KPI Dashboard

| Metric | Month 1 | Month 2 | Change | Target |
|--------|---------|---------|--------|--------|
| Indexed Pages | | | | +50 |
| Total Site Words | | | | +40,000 |
| Organic Sessions | | | | Track |
| Keyword Rankings | | | | Track top 100 |
| GBP Actions | | | | +25% |
| Citations Live | | | | 40+ |

---

# MONTH 3: AUTHORITY BUILDING

## WEEKS 9-10: Link Building Initiation

### Week 9: Link Building Foundation

**Day 57-58: Link Profile Audit & Strategy**

**Tasks:**

1. **Current Link Profile Analysis**
   - Tool: Ahrefs Backlink Checker
   - Tool: Moz Link Explorer
   - Tool: Majestic

   **Analyze:**
   - Total referring domains
   - Domain authority/rating
   - Link quality (spam score)
   - Anchor text distribution
   - Link velocity
   - Competitor comparison

   **Baseline Metrics:**
   | Metric | Current | 90-Day Target |
   |--------|---------|---------------|
   | Referring Domains | | +30 |
   | Domain Rating | | +5 points |
   | Organic Keywords | | +200 |

2. **Competitor Backlink Analysis**
   - Export competitor backlinks
   - Identify common linking domains
   - Find link gap opportunities
   - Categorize by link type:
     - Legal directories
     - News/media
     - Local business
     - Educational
     - Resource pages

3. **Link Building Strategy Document**

   **Link Types to Pursue:**
   | Type | Target Quantity | Priority |
   |------|-----------------|----------|
   | Legal directories (remaining) | 15 | High |
   | Local business directories | 20 | High |
   | DFW news/media mentions | 5 | High |
   | Resource page links | 10 | Medium |
   | Guest posts | 3-5 | Medium |
   | Scholarship links | 2-3 | Medium |
   | Sponsorship mentions | 5 | Medium |

**Day 59-60: Legal Directory Completion**

**Tasks:**

Complete remaining legal directory submissions:

| Directory | DA | Status | Profile URL |
|-----------|-----|--------|-------------|
| LegalZoom | 72 | ☐ | |
| Legal.io | 55 | ☐ | |
| AttorneyPages | 48 | ☐ | |
| LawGuru | 52 | ☐ | |
| LawLink | 45 | ☐ | |
| LawyerCentral | 44 | ☐ | |
| USAttorneys | 50 | ☐ | |
| AttorneyFind | 42 | ☐ | |
| LawyerDB | 40 | ☐ | |
| AttorneyLocate | 38 | ☐ | |

**For Each Directory:**
- Create unique profile description
- Upload firm logo and photos
- Add all practice areas
- Include DFW service area
- Add attorney profiles
- Verify NAP consistency

**Day 61-63: Local Business Directory Expansion**

**DFW-Specific Directories:**

| Directory | Type | Status |
|-----------|------|--------|
| Dallas Regional Chamber | Business | ☐ |
| Fort Worth Chamber of Commerce | Business | ☐ |
| DFW Business Network | Business | ☐ |
| Dallas Bar Association | Legal | ☐ |
| Tarrant County Bar Association | Legal | ☐ |
| Texas Trial Lawyers Association | Legal | ☐ |
| Dallas Hispanic Bar Association | Legal | ☐ |
| Dallas Association of Young Lawyers | Legal | ☐ |
| North Texas Business Council | Business | ☐ |
| Plano Chamber of Commerce | Business | ☐ |
| Arlington Chamber of Commerce | Business | ☐ |
| Irving-Las Colinas Chamber | Business | ☐ |
| Garland Chamber of Commerce | Business | ☐ |
| McKinney Chamber of Commerce | Business | ☐ |
| Frisco Chamber of Commerce | Business | ☐ |

**General Business Directories:**
| Directory | DA | Status |
|-----------|-----|--------|
| Hotfrog | 52 | ☐ |
| Cylex | 48 | ☐ |
| eLocal | 55 | ☐ |
| Brownbook | 58 | ☐ |
| Spoke | 62 | ☐ |
| Tupalo | 50 | ☐ |
| Fyple | 45 | ☐ |
| ShowMeLocal | 48 | ☐ |
| USCity | 52 | ☐ |
| CitySquares | 55 | ☐ |

### Week 10: Active Link Acquisition

**Day 64-66: Resource Page Link Building**

**Tasks:**

1. **Find Resource Page Opportunities**

   **Search Queries:**
   ```
   "dallas" + "resources" + "accident"
   "texas" + "legal resources" + "injury"
   "dfw" + "helpful links" + "legal"
   "dallas" + "community resources"
   site:.edu + "dallas" + "legal resources"
   site:.gov + "texas" + "accident resources"
   ```

2. **Identify Target Pages:**
   - University legal resource pages
   - Government victim assistance pages
   - Non-profit resource directories
   - Hospital patient resource pages
   - Insurance company resource lists

3. **Outreach Template:**
   ```
   Subject: Suggestion for Your [Page Name] Resource Page

   Dear [Name/Webmaster],

   I recently came across your helpful resource page for
   [topic] at [URL]. It's a great collection of information
   for people in Dallas dealing with [situation].

   I noticed you list several legal resources, and I wanted
   to suggest adding [Firm Name] to your page. We're a Dallas-based
   personal injury law firm that offers free consultations to
   accident victims throughout the DFW area.

   Our resource page on [topic] at [URL] might be particularly
   helpful for your visitors looking for information on
   [specific topic].

   Thank you for considering this addition. Please let me know
   if you have any questions.

   Best regards,
   [Name]
   [Firm Name]
   ```

4. **Track Outreach:**
   | Target Site | Contact | Date Sent | Response | Link Live |
   |-------------|---------|-----------|----------|-----------|
   | | | | | |

**Day 67-68: Digital PR & Media Outreach**

**Tasks:**

1. **Create Press-Worthy Content**

   **Ideas for DFW Market:**
   - Annual DFW traffic accident statistics report
   - Most dangerous roads in Dallas infographic
   - Texas personal injury settlement trends study
   - Local safety initiative announcement
   - Commentary on high-profile local cases

2. **Local Media Targets:**
   | Outlet | Type | Contact |
   |--------|------|---------|
   | Dallas Morning News | Newspaper | Legal/Metro desk |
   | Fort Worth Star-Telegram | Newspaper | Local news |
   | D Magazine | Magazine | Legal section |
   | Dallas Observer | Alt-weekly | News desk |
   | WFAA (ABC) | TV | Assignment desk |
   | KXAS (NBC) | TV | Assignment desk |
   | KDFW (FOX) | TV | Assignment desk |
   | KTVT (CBS) | TV | Assignment desk |
   | Dallas Business Journal | Business | Legal reporter |

3. **HARO (Help A Reporter Out)**
   - Sign up at helpareporter.com
   - Set up alerts for: personal injury, car accidents, Texas law, Dallas
   - Respond to relevant queries within 24 hours
   - Track responses and placements

4. **Legal Commentary Opportunities**
   - Sign up for ExpertFile
   - Create profile on ProfNet
   - Offer commentary on local accident news
   - Provide expert quotes for legal publications

**Day 69-70: Guest Posting & Content Partnerships**

**Tasks:**

1. **Identify Guest Post Opportunities**

   **Search Queries:**
   ```
   "write for us" + legal
   "guest post" + personal injury
   "contribute" + law blog
   "submit article" + legal
   "guest author" + attorney
   ```

2. **Target Sites:**
   | Site | DA | Topic Focus | Contact |
   |------|-----|-------------|---------|
   | Above the Law | 75 | Legal news | |
   | Lawyerist | 65 | Law practice | |
   | Attorney at Work | 60 | Legal practice | |
   | Texas Lawyer | 58 | Texas legal | |
   | JD Supra | 72 | Legal content | |
   | Lexology | 68 | Legal news | |

3. **Guest Post Topics:**
   - Texas Personal Injury Law Updates
   - What Car Accident Victims Should Know About Texas Law
   - The Future of Personal Injury Litigation in Texas
   - How Technology is Changing Personal Injury Cases

4. **Guest Post Pitch Template:**
   ```
   Subject: Guest Post Idea: [Specific Topic]

   Dear [Editor Name],

   I'm [Name], a personal injury attorney at [Firm Name] in Dallas,
   with [X] years of experience handling [practice areas].

   I'd love to contribute a guest article to [Publication] on
   [specific topic]. Given your readers' interest in [relevant topic],
   I think this would provide valuable insights on [specific angle].

   Here's my proposed outline:
   [Brief 3-4 point outline]

   I've previously written for [publications if any], and you can
   see my writing samples at [URL].

   Would this be of interest to your editorial team?

   Best regards,
   [Name]
   [Credentials]
   ```

### Weeks 9-10 Deliverables Checklist

| Task | Status | Quantity | Notes |
|------|--------|----------|-------|
| Link profile audit | ☐ | 1 | |
| Competitor backlink analysis | ☐ | 5 competitors | |
| Legal directory submissions | ☐ | 15 | |
| Local directory submissions | ☐ | 15 | |
| Chamber memberships | ☐ | 3-5 | |
| Resource page outreach | ☐ | 20 emails | |
| Media list compiled | ☐ | 20 contacts | |
| HARO setup | ☐ | 1 | |
| Guest post pitches | ☐ | 5 | |

### Weeks 9-10 KPIs

| KPI | Target | Actual |
|-----|--------|--------|
| New referring domains | 15+ | |
| Directory profiles created | 30 | |
| Resource page links acquired | 3-5 | |
| Media mentions | 1-2 | |
| Guest posts placed | 1 | |

---

## WEEKS 11-12: Local SEO Expansion

### Week 11: Citation & GBP Enhancement

**Day 71-72: Citation Audit & Cleanup**

**Tasks:**

1. **Citation Audit**
   - Tool: BrightLocal Citation Tracker
   - Tool: Whitespark Local Citation Finder
   - Tool: Moz Local

   **Check:**
   - All citations from Weeks 3 & 9-10 are live
   - NAP consistency across all citations
   - Duplicate listings identification
   - Incorrect information flagged

2. **Fix Citation Issues**
   | Issue Type | Action | Priority |
   |------------|--------|----------|
   | Duplicate listings | Claim and merge or delete | High |
   | Incorrect NAP | Submit correction | High |
   | Incomplete profiles | Add missing info | Medium |
   | Missing photos | Upload | Low |

3. **Additional Citation Opportunities**

   **Industry-Specific:**
   | Directory | Focus | Status |
   |-----------|-------|--------|
   | Injury Board | PI attorneys | ☐ |
   | 1800-Car-Wreck | Car accidents | ☐ |
   | AccidentAttorneys.org | Accidents | ☐ |
   | TopPersonalInjuryLawyers | PI ranking | ☐ |
   | ExpertLaw | Legal Q&A | ☐ |

**Day 73-74: Google Business Profile Advanced Optimization**

**Tasks:**

1. **GBP Posts Strategy**

   **Post Schedule:**
   | Week | Post Type | Topic |
   |------|-----------|-------|
   | 1 | What's New | Recent case result |
   | 2 | Event | Free consultation week |
   | 3 | Offer | Free case evaluation |
   | 4 | Update | Blog post promotion |

   **Post Format:**
   - Image: 1200x900 optimized
   - Text: 100-300 words
   - CTA: Book, Call, Learn More
   - Link: Relevant page

   **Example Posts:**
   ```
   [What's New]
   Our Dallas car accident lawyers recently secured a $1.2M
   settlement for a client injured in a rear-end collision on
   I-35. If you've been injured in a car accident, we're here
   to help. Free consultations available 24/7.
   [Call Now Button]

   [Offer]
   FREE Case Evaluation for Dallas Accident Victims
   Injured in an accident? Get a free, no-obligation case
   review from our experienced personal injury attorneys.
   We handle car accidents, truck accidents, and more.
   No fee unless we win your case.
   [Book Now Button]
   ```

2. **GBP Q&A Management**
   - Seed 10-15 questions (from different accounts)
   - Provide detailed answers
   - Monitor for new questions weekly

   **Sample Q&As:**
   ```
   Q: Do you offer free consultations?
   A: Yes! We offer free, no-obligation consultations for all
   personal injury cases. You can call us 24/7 at (214) XXX-XXXX
   or fill out our online form to schedule your free case review.

   Q: What areas do you serve?
   A: We serve clients throughout the Dallas-Fort Worth metroplex,
   including Dallas, Fort Worth, Arlington, Plano, Irving, Garland,
   McKinney, Frisco, and surrounding communities.

   Q: How much does a personal injury lawyer cost?
   A: We work on a contingency fee basis, which means you pay
   nothing unless we win your case. Our fee is a percentage of
   your recovery, so there's no upfront cost or out-of-pocket
   expense to hire us.
   ```

3. **Review Generation Push**

   **Goal:** 20+ new Google reviews in Week 11

   **Tactics:**
   - Email campaign to recent clients
   - SMS follow-up to satisfied clients
   - In-person request at case closing
   - QR code on business cards and office signage

   **Review Request Timing:**
   - Settlement received: Immediate outreach
   - Case won: Within 24 hours
   - Positive interaction: Same day

**Day 75-77: Local Content Expansion**

**Tasks:**

1. **Create Additional Location Pages**

   Expand to secondary DFW cities:
   | City | Population | Page Status |
   |------|------------|-------------|
   | McKinney | 199K | ☐ |
   | Frisco | 219K | ☐ |
   | Denton | 148K | ☐ |
   | Mesquite | 150K | ☐ |
   | Carrollton | 142K | ☐ |
   | Richardson | 121K | ☐ |
   | Lewisville | 117K | ☐ |
   | Allen | 108K | ☐ |

2. **Neighborhood/Area Content**

   Create content for Dallas neighborhoods:
   - Downtown Dallas
   - Uptown Dallas
   - Deep Ellum
   - Oak Lawn
   - Highland Park
   - University Park
   - East Dallas
   - North Dallas
   - South Dallas
   - Oak Cliff

3. **Highway/Corridor Content**

   Create pages targeting major DFW highways:
   | Highway | Target Keyword |
   |---------|----------------|
   | I-35 | i-35 accident lawyer dallas |
   | I-30 | i-30 car accident attorney |
   | I-635 (LBJ) | lbj freeway accident lawyer |
   | I-20 | i-20 accident attorney dallas |
   | US-75 | us 75 accident lawyer |
   | SH-121 | 121 tollway accident attorney |
   | Dallas North Tollway | dallas north tollway accident |

### Week 12: Local Engagement & Review Strategy

**Day 78-79: Community Engagement**

**Tasks:**

1. **Local Sponsorship Opportunities**

   | Opportunity | Type | Link Potential |
   |-------------|------|----------------|
   | Dallas charity events | Sponsorship | Event page link |
   | Local sports teams | Sponsorship | Team page link |
   | School programs | Donation | Recognition page |
   | Community festivals | Booth/sponsor | Listing |
   | Non-profit organizations | Partnership | About page |

2. **Local Event Participation**
   - DFW legal community events
   - Chamber of Commerce meetings
   - Bar association events
   - Community safety fairs
   - Local networking groups

3. **Educational Outreach**
   - Offer free legal seminars at community centers
   - Partner with driving schools on safety education
   - Provide know-your-rights workshops
   - Speak at local business groups

**Day 80-81: Review Expansion to Secondary Platforms**

**Tasks:**

1. **Review Platform Optimization**

   | Platform | Current Reviews | Target | Status |
   |----------|-----------------|--------|--------|
   | Google | | 50+ | |
   | Avvo | | 30+ | |
   | Facebook | | 20+ | |
   | Yelp | | 15+ | |
   | Lawyers.com | | 10+ | |
   | BBB | | 5+ | |

2. **Review Response Protocol**
   - Respond to all reviews within 24 hours
   - Personalize responses (use reviewer name)
   - Thank for positive reviews
   - Address concerns in negative reviews professionally
   - Never argue or become defensive

3. **Review Monitoring Setup**
   - Set up Google Alerts for firm name
   - Configure BirdEye or ReviewTrackers
   - Weekly review audit
   - Monthly review report

**Day 82-84: Performance Analysis & Optimization**

**Tasks:**

1. **Local Ranking Audit**
   - Tool: BrightLocal Local Search Grid
   - Tool: Local Falcon

   **Check Rankings For:**
   | Keyword | Dallas | Fort Worth | Arlington | Plano |
   |---------|--------|------------|-----------|-------|
   | personal injury lawyer | | | | |
   | car accident attorney | | | | |
   | truck accident lawyer | | | | |

2. **GBP Insights Analysis**

   **Metrics to Review:**
   - Search queries (direct vs discovery)
   - Views (Search vs Maps)
   - Customer actions (calls, directions, website)
   - Photo views vs competitor average
   - Post engagement

3. **Local SEO Optimization Adjustments**
   - Update GBP based on insights
   - Adjust content for underperforming locations
   - Add more photos/posts for engagement
   - Respond to any new reviews

### Weeks 11-12 Deliverables Checklist

| Task | Status | Notes |
|------|--------|-------|
| Citation audit complete | ☐ | |
| Citation errors fixed | ☐ | |
| GBP posts (8 total) | ☐ | |
| GBP Q&A seeded (15) | ☐ | |
| New Google reviews (20+) | ☐ | |
| Secondary location pages (8) | ☐ | |
| Highway pages (7) | ☐ | |
| Community sponsorship (2) | ☐ | |
| Review platform expansion | ☐ | |
| Local ranking audit | ☐ | |

### Weeks 11-12 KPIs

| KPI | Target | Actual |
|-----|--------|--------|
| Total live citations | 100+ | |
| Google reviews | 50+ | |
| Average Google rating | 4.8+ | |
| GBP views | +50% from baseline | |
| GBP actions | +50% from baseline | |
| Local pack rankings | Track improvement | |

---

# MONTH 3 COMPLETION CHECKPOINT

## Summary of Month 3 Accomplishments

| Category | Tasks Completed | Status |
|----------|-----------------|--------|
| Link Building | Directories, outreach, PR | ☐ |
| Citations | 100+ citations live | ☐ |
| Reviews | 50+ Google reviews | ☐ |
| Local Content | Location + highway pages | ☐ |
| GBP Optimization | Posts, Q&A, media | ☐ |

## Month 3 KPI Dashboard

| Metric | Month 2 | Month 3 | Change | Target |
|--------|---------|---------|--------|--------|
| Referring Domains | | | +30 | |
| Domain Rating | | | +5 pts | |
| Citations Live | | | 100+ | |
| Google Reviews | | | 50+ | |
| Organic Keywords | | | +200 | |
| Organic Traffic | | | +50% | |
| GBP Views | | | +100% | |
| GBP Actions | | | +75% | |

---

# 90-DAY COMPREHENSIVE KPI DASHBOARD

## Technical SEO Metrics

| Metric | Baseline | Day 30 | Day 60 | Day 90 | Target |
|--------|----------|--------|--------|--------|--------|
| Indexed Pages | | | | | +50 |
| Crawl Errors | | | | | 0 |
| Mobile PageSpeed | | | | | 70+ |
| Desktop PageSpeed | | | | | 85+ |
| Core Web Vitals Pass | | | | | Yes |

## Content Metrics

| Metric | Baseline | Day 30 | Day 60 | Day 90 | Target |
|--------|----------|--------|--------|--------|--------|
| Total Pages | | | | | +50 |
| Total Blog Posts | | | | | +15 |
| Total Word Count | | | | | +60,000 |
| Avg Time on Page | | | | | >2 min |

## Ranking Metrics

| Metric | Baseline | Day 30 | Day 60 | Day 90 | Target |
|--------|----------|--------|--------|--------|--------|
| Keywords in Top 10 | | | | | 10+ |
| Keywords in Top 30 | | | | | 50+ |
| Keywords in Top 100 | | | | | 200+ |
| Featured Snippets | | | | | 5+ |

## Traffic Metrics

| Metric | Baseline | Day 30 | Day 60 | Day 90 | Target |
|--------|----------|--------|--------|--------|--------|
| Organic Sessions | | | | | +100% |
| Organic Users | | | | | +100% |
| New vs Returning | | | | | Track |
| Bounce Rate | | | | | <60% |

## Local SEO Metrics

| Metric | Baseline | Day 30 | Day 60 | Day 90 | Target |
|--------|----------|--------|--------|--------|--------|
| GBP Views | | | | | +200% |
| GBP Actions | | | | | +150% |
| Local Pack Rankings | | | | | Top 3 |
| Citations Live | 0 | 20 | 50 | 100 | 100+ |
| Google Reviews | | | | | 50+ |
| Average Rating | | | | | 4.8+ |

## Link Building Metrics

| Metric | Baseline | Day 30 | Day 60 | Day 90 | Target |
|--------|----------|--------|--------|--------|--------|
| Referring Domains | | | | | +50 |
| Domain Rating | | | | | +10 |
| Total Backlinks | | | | | +100 |

## Conversion Metrics

| Metric | Baseline | Day 30 | Day 60 | Day 90 | Target |
|--------|----------|--------|--------|--------|--------|
| Form Submissions | | | | | Track |
| Phone Calls | | | | | Track |
| Chat Initiations | | | | | Track |
| Consultation Requests | | | | | Track |
| Conversion Rate | | | | | 3%+ |

---

# RECOMMENDED TOOLS SUMMARY

## Essential Tools (Must-Have)

| Tool | Purpose | Cost | Priority |
|------|---------|------|----------|
| Google Search Console | Search monitoring | Free | Critical |
| Google Analytics 4 | Traffic analytics | Free | Critical |
| Google Business Profile | Local SEO | Free | Critical |
| Screaming Frog | Technical audits | Free/Paid | Critical |
| Ahrefs OR SEMrush | Keyword/backlink research | $99-199/mo | Critical |

## Recommended Tools

| Tool | Purpose | Cost | Priority |
|------|---------|------|----------|
| BrightLocal | Local SEO/citations | $39/mo | High |
| PageSpeed Insights | Speed analysis | Free | High |
| Schema Markup Validator | Schema testing | Free | High |
| Moz Local | Citation management | $99/yr | Medium |
| HARO | PR/link building | Free | Medium |
| ReviewTrackers | Review monitoring | $49/mo | Medium |

## Content Tools

| Tool | Purpose | Cost |
|------|---------|------|
| Clearscope OR SurferSEO | Content optimization | $170-89/mo |
| Grammarly | Writing quality | Free/Premium |
| Hemingway Editor | Readability | Free |
| Canva | Graphics/images | Free/Premium |

---

# APPENDIX A: DFW MARKET INTELLIGENCE

## Dallas-Fort Worth Demographics

- **Population:** 7.5+ million (4th largest US metro)
- **Major Counties:** Dallas, Tarrant, Collin, Denton, Rockwall, Kaufman, Ellis
- **Primary Cities:** Dallas, Fort Worth, Arlington, Plano, Irving, Garland, Frisco, McKinney

## DFW Traffic & Accident Statistics

- **Annual Traffic Fatalities:** ~650-700 (TxDOT data)
- **Annual Serious Injuries:** ~4,000+
- **Most Dangerous Highways:** I-35, I-30, I-635, I-20, US-75
- **Peak Accident Times:** 7-9 AM, 4-7 PM weekdays

## Competitive Landscape

**Top DFW Personal Injury Firms (by visibility):**
1. Thompson Law
2. Rasansky Law Firm
3. The Law Offices of Tim O'Hare
4. Tate Law Offices
5. Ted B. Lyon & Associates
6. Reyes Browne Reilley
7. Carabin Shaw
8. Anderson Injury Lawyers
9. Witherite Law Group
10. The Fell Law Firm

## Local Search Volume Estimates

| Keyword | Monthly Volume |
|---------|----------------|
| dallas personal injury lawyer | 1,900 |
| car accident lawyer dallas | 1,600 |
| dallas car accident attorney | 1,300 |
| fort worth personal injury attorney | 720 |
| truck accident attorney dallas | 590 |
| 18 wheeler accident lawyer dallas | 480 |
| wrongful death attorney dallas | 390 |
| motorcycle accident lawyer dallas | 320 |

---

# APPENDIX B: SCHEMA MARKUP TEMPLATES

## LocalBusiness Schema (Complete)
```json
{
  "@context": "https://schema.org",
  "@type": "LegalService",
  "@id": "https://[domain].com/#organization",
  "name": "[Firm Name]",
  "alternateName": "[Firm Name] Personal Injury Lawyers",
  "url": "https://[domain].com",
  "logo": {
    "@type": "ImageObject",
    "url": "https://[domain].com/logo.png",
    "width": 250,
    "height": 250
  },
  "image": [
    "https://[domain].com/office-1.jpg",
    "https://[domain].com/office-2.jpg"
  ],
  "description": "Dallas personal injury law firm serving the DFW metroplex.",
  "telephone": "+1-214-XXX-XXXX",
  "email": "info@[domain].com",
  "faxNumber": "+1-214-XXX-XXXX",
  "priceRange": "Free Consultation",
  "currenciesAccepted": "USD",
  "paymentAccepted": "Contingency Fee",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Main Street, Suite 500",
    "addressLocality": "Dallas",
    "addressRegion": "TX",
    "postalCode": "75201",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 32.7767,
    "longitude": -96.7970
  },
  "hasMap": "https://maps.google.com/?cid=XXXXX",
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
      "opens": "08:00",
      "closes": "18:00"
    },
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Saturday", "Sunday"],
      "opens": "00:00",
      "closes": "00:00",
      "description": "By Appointment Only"
    }
  ],
  "areaServed": [
    {
      "@type": "City",
      "name": "Dallas",
      "@id": "https://en.wikipedia.org/wiki/Dallas"
    },
    {
      "@type": "City",
      "name": "Fort Worth"
    },
    {
      "@type": "City",
      "name": "Arlington"
    },
    {
      "@type": "City",
      "name": "Plano"
    },
    {
      "@type": "City",
      "name": "Irving"
    }
  ],
  "sameAs": [
    "https://www.facebook.com/[firm]",
    "https://www.linkedin.com/company/[firm]",
    "https://twitter.com/[firm]",
    "https://www.instagram.com/[firm]"
  ],
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.9",
    "bestRating": "5",
    "worstRating": "1",
    "ratingCount": "127"
  },
  "review": [
    {
      "@type": "Review",
      "author": {
        "@type": "Person",
        "name": "John D."
      },
      "reviewRating": {
        "@type": "Rating",
        "ratingValue": "5"
      },
      "reviewBody": "Excellent experience with this firm..."
    }
  ]
}
```

## FAQ Schema Template
```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How much does a personal injury lawyer cost in Dallas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Most Dallas personal injury lawyers, including our firm, work on a contingency fee basis. This means you pay nothing upfront and only pay a fee if we win your case. The fee is typically a percentage of your settlement or verdict."
      }
    },
    {
      "@type": "Question",
      "name": "What is the statute of limitations for personal injury in Texas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "In Texas, you generally have two years from the date of your injury to file a personal injury lawsuit. However, there are exceptions that may shorten or extend this deadline, so it's important to consult with an attorney as soon as possible."
      }
    }
  ]
}
```

## Article Schema Template
```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "What to Do After a Car Accident in Dallas",
  "image": "https://[domain].com/blog/car-accident-dallas.jpg",
  "datePublished": "2026-01-15",
  "dateModified": "2026-01-15",
  "author": {
    "@type": "Person",
    "name": "John Smith",
    "url": "https://[domain].com/about/john-smith/"
  },
  "publisher": {
    "@type": "Organization",
    "name": "[Firm Name]",
    "logo": {
      "@type": "ImageObject",
      "url": "https://[domain].com/logo.png"
    }
  },
  "description": "Learn the essential steps to take after a car accident in Dallas, including how to protect your legal rights and when to contact an attorney.",
  "mainEntityOfPage": {
    "@type": "WebPage",
    "@id": "https://[domain].com/blog/what-to-do-after-car-accident-dallas/"
  }
}
```

---

# APPENDIX C: OUTREACH TEMPLATES

## Guest Post Pitch
```
Subject: Guest Post: [Specific Topic Idea]

Dear [Editor Name],

I'm [Name], a personal injury attorney with [X] years of experience
practicing in the Dallas-Fort Worth area. I specialize in [practice areas]
and have handled cases involving [specific experience].

I'd like to contribute a guest article to [Publication] on the topic of
"[Proposed Title]." Given your readers' interest in [relevant topic],
I believe this would provide valuable insights on [specific angle].

Proposed outline:
1. [Point 1]
2. [Point 2]
3. [Point 3]
4. [Point 4]

The article would be approximately [word count] words and completely
original. I can also provide custom graphics if helpful.

Previous writing samples:
- [Link 1]
- [Link 2]

Would this be of interest? I'm happy to adjust the topic or angle
based on your editorial needs.

Best regards,
[Name]
[Title], [Firm Name]
[Phone] | [Email]
```

## Resource Page Outreach
```
Subject: Resource Suggestion for [Page Name]

Hello [Name/Webmaster],

I came across your [description of page] while researching [topic]
resources for accident victims in the Dallas area. It's a helpful
collection that I've actually shared with some of my clients.

I noticed you include several legal resources on the page. I wanted
to suggest adding our guide on "[Resource Title]" which covers
[brief description]. It's been well-received by readers looking
for information on [topic].

Here's the link: [URL]

Either way, thank you for maintaining such a helpful resource for
the community.

Best,
[Name]
[Firm Name]
```

## HARO Response Template
```
Subject: RE: [HARO Query Subject Line]

Hi [Reporter Name],

I'm [Name], a personal injury attorney at [Firm Name] in Dallas, Texas.
I have [X] years of experience handling [relevant practice area] cases
and would be happy to provide expert commentary on your query.

[Your response to their specific question - 2-4 paragraphs]

Key points:
- [Bullet point 1]
- [Bullet point 2]
- [Bullet point 3]

Feel free to use any or all of the above. I'm available for follow-up
questions by phone at [number] or email.

Bio for attribution:
[Name] is a personal injury attorney at [Firm Name] in Dallas, Texas.
With [X] years of experience, he/she has recovered [results] for
accident victims throughout the DFW metroplex. [Website URL]

Best regards,
[Name]
[Phone] | [Email] | [Website]
```

---

# APPENDIX D: WEEKLY REPORTING TEMPLATE

## Weekly SEO Report

**Week of:** [Date Range]
**Prepared by:** [Name]

### Executive Summary
[2-3 sentence overview of the week's activities and results]

### Tasks Completed This Week
| Task | Status | Notes |
|------|--------|-------|
| | ☑ Complete | |
| | ☑ Complete | |
| | ⏳ In Progress | |

### Key Metrics
| Metric | Last Week | This Week | Change |
|--------|-----------|-----------|--------|
| Organic Sessions | | | |
| Organic Users | | | |
| GBP Views | | | |
| GBP Actions | | | |
| New Reviews | | | |
| Citations Added | | | |

### Ranking Changes
| Keyword | Previous | Current | Change |
|---------|----------|---------|--------|
| | | | |

### Content Published
| Title | URL | Target Keyword | Indexed |
|-------|-----|----------------|---------|
| | | | |

### Issues/Blockers
- [Issue 1]
- [Issue 2]

### Next Week's Priorities
1. [Priority 1]
2. [Priority 2]
3. [Priority 3]

---

**END OF PLAYBOOK**

*This playbook should be reviewed and adjusted monthly based on performance data and market changes. SEO is an ongoing process that requires continuous optimization and adaptation.*
