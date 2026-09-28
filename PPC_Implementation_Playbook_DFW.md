# PPC Implementation Playbook
## Personal Injury Law Firm - Dallas-Fort Worth Market
### 12-Week Strategic Launch Plan

---

## Executive Summary

This playbook provides a comprehensive, week-by-week implementation guide for launching and scaling a PPC program for a personal injury law firm in the Dallas-Fort Worth metropolitan area. The DFW market represents the 4th largest metro in the United States with approximately 7.6 million residents, making it a highly competitive but lucrative market for personal injury legal services.

**Total Recommended Monthly Budget (at scale):** $75,000 - $150,000
**Expected Timeline to Full Optimization:** 90 days
**Target Cost Per Case:** $1,500 - $3,500 (depending on case type)

---

# MONTH 1: FOUNDATION & CORE CAMPAIGNS

---

## WEEK 1: Account Infrastructure & Tracking Setup

### Day 1-2: Google Ads Account Configuration

#### Account Structure Setup
```
Account Level Settings:
├── Time Zone: Central Time (US & Canada)
├── Currency: USD
├── Auto-tagging: Enabled
├── Tracking Template: {lpurl}?utm_source=google&utm_medium=cpc&utm_campaign={campaignid}&utm_content={adgroupid}&utm_term={keyword}&gclid={gclid}
└── Account-Level Automated Rules: Pause ads with CTR < 1% after 1000 impressions
```

#### Billing & Access Setup
- [ ] Add primary payment method (credit card with high limit)
- [ ] Set up backup payment method
- [ ] Configure billing threshold: $500 initial, request increase to $10,000
- [ ] Add all stakeholders with appropriate access levels:
  - Agency: Admin access
  - Client marketing director: Standard access
  - Client owner/partner: Read-only access

#### Account-Level Negative Keywords
Create a shared negative keyword list named "PI Firm - Master Negatives":

```
EMPLOYMENT/WORKERS COMP EXCLUSIONS:
workers compensation
workers comp
work injury claim
job injury lawyer
workplace injury attorney
osha violation
occupational injury

CRIMINAL/UNRELATED LEGAL:
criminal defense
criminal lawyer
dui attorney
divorce lawyer
family law
bankruptcy attorney
immigration lawyer
estate planning
real estate attorney

INFORMATIONAL/NON-COMMERCIAL:
how to
what is
definition
wikipedia
free advice
pro bono
legal aid
law school
paralegal jobs
attorney salary

GEOGRAPHIC EXCLUSIONS:
houston attorney
austin lawyer
san antonio injury
el paso accident

DIY/NON-SERVICE:
template
form
sample
example
do it yourself
self represent

COMPETITOR BRAND TERMS (for non-conquest campaigns):
[List top 10 competitor firm names]
```

### Day 3-4: Conversion Tracking Implementation

#### Google Ads Conversion Actions Setup

**Conversion Action 1: Phone Calls**
```
Conversion Name: Phone Call - Direct
Category: Phone call lead
Value: $500 (placeholder, adjust based on data)
Count: One conversion per interaction
Click-through window: 90 days
Engaged-view window: 30 days
View-through window: 1 day
Attribution: Data-driven
```

**Conversion Action 2: Form Submissions**
```
Conversion Name: Contact Form Submission
Category: Submit lead form
Value: $300
Count: One conversion per interaction
Click-through window: 90 days
Attribution: Data-driven

Implementation:
- Add Google Ads tag to thank you page
- Or fire on form submission event via GTM
```

**Conversion Action 3: Chat Initiations**
```
Conversion Name: Live Chat Engagement
Category: Submit lead form
Value: $200
Count: One conversion per interaction
Click-through window: 30 days
Attribution: Data-driven
```

**Conversion Action 4: Click-to-Call (Mobile)**
```
Conversion Name: Mobile Click-to-Call
Category: Phone call lead
Value: $400
Count: One conversion per interaction
Click-through window: 90 days
Attribution: Data-driven
```

#### Google Tag Manager Container Setup

```javascript
// GTM Container Configuration

// Tag 1: Google Ads Conversion Linker
Tag Type: Conversion Linker
Trigger: All Pages

// Tag 2: Google Ads Remarketing
Tag Type: Google Ads Remarketing
Conversion ID: [YOUR_CONVERSION_ID]
Trigger: All Pages

// Tag 3: Form Submission Tracking
Tag Type: Google Ads Conversion Tracking
Conversion ID: [YOUR_CONVERSION_ID]
Conversion Label: [FORM_SUBMISSION_LABEL]
Trigger: Form Submission Success

// Tag 4: Phone Click Tracking
Tag Type: Google Ads Conversion Tracking
Conversion ID: [YOUR_CONVERSION_ID]
Conversion Label: [PHONE_CLICK_LABEL]
Trigger: Click - tel: links
```

#### Enhanced Conversions Setup
```
Enable Enhanced Conversions for:
- Email address (hashed)
- Phone number (hashed)
- First name + Last name (hashed)

Implementation via GTM:
1. Create User-Provided Data variable
2. Map form fields to enhanced conversion fields
3. Configure conversion tag to include user data
```

### Day 5: Call Tracking Implementation

#### CallRail Account Setup

**Account Configuration:**
```
Company Name: [Firm Name]
Time Zone: Central
Industry: Legal Services
Primary Phone: [Main office number]
```

**Tracking Number Pool (Website Pool):**
```
Pool Name: Google Ads Website Pool
Numbers Needed: 8-12 numbers (based on expected traffic)
Area Codes: 214, 469, 972, 817, 682 (DFW area codes)
Whisper Message: "Google Ads call"
Recording: Enabled
Transcription: Enabled

Swap Targets:
- Main office number on all pages
- Practice area specific numbers (if applicable)
```

**Campaign-Level Tracking Numbers:**
```
Number 1: Brand Campaign
├── Whisper: "Brand campaign call"
├── Area Code: 214
└── DNI: Disabled (static number)

Number 2: High-Intent Campaign
├── Whisper: "High intent campaign call"
├── Area Code: 214
└── DNI: Disabled (static number)

Number 3: LSA Tracking
├── Whisper: "LSA call"
├── Area Code: 214
└── DNI: Disabled (static number)
```

**Call Scoring Setup:**
```
Automated Call Scoring Rules:

Score as QUALIFIED LEAD if:
- Call duration > 90 seconds
- AND caller mentions: accident, injury, hurt, crash, wreck, collision, slip, fall, medical, hospital, surgery

Score as NOT QUALIFIED if:
- Call duration < 30 seconds
- OR caller mentions: job, employment, workers comp, looking for work

Custom Tags:
- Case Type: Auto accident, Truck accident, Motorcycle, Slip & fall, Other
- Urgency: Hot (immediate need), Warm (exploring options), Cold (information only)
- Status: New lead, Callback needed, Signed, Lost
```

**CallRail + Google Ads Integration:**
```
1. Navigate to CallRail > Integrations > Google Ads
2. Connect Google Ads account
3. Enable conversion import
4. Map CallRail "Qualified Lead" to Google Ads conversion action
5. Set value to pass: $500 per qualified call
6. Enable call recording playback in Google Ads
```

### Day 6-7: Landing Page Audit & Optimization

#### Landing Page Requirements Checklist

**Above-the-Fold Elements:**
- [ ] Clear headline with primary keyword (e.g., "Dallas Car Accident Lawyers")
- [ ] Subheadline with value proposition
- [ ] Click-to-call button (prominent, contrasting color)
- [ ] Contact form (3-5 fields maximum)
- [ ] Trust indicators (badges, awards, ratings)
- [ ] Hero image (professional, not stock-looking)

**Form Optimization:**
```
Recommended Form Fields:
1. Name (required)
2. Phone Number (required)
3. Email (required)
4. Brief description of accident (optional, text area)
5. How did accident happen? (optional, dropdown)

Form Settings:
- Auto-focus on first field
- Inline validation
- Clear error messages
- Prominent submit button: "Get Your Free Consultation"
- Privacy policy link below form
```

**Page Speed Requirements:**
```
Target Metrics:
- Mobile Page Speed Score: > 50
- Desktop Page Speed Score: > 70
- Largest Contentful Paint: < 2.5 seconds
- First Input Delay: < 100ms
- Cumulative Layout Shift: < 0.1

Optimization Actions:
- Compress all images (use WebP format)
- Implement lazy loading for below-fold images
- Minify CSS and JavaScript
- Enable browser caching
- Use CDN for static assets
```

**Mobile Optimization:**
```
- Click-to-call button sticky at bottom of screen
- Form fields minimum 16px font (prevent zoom)
- Touch targets minimum 44px x 44px
- No horizontal scrolling
- Fast-loading mobile version
```

#### Landing Page Variants Needed

Create landing pages for each primary service:
1. `/car-accident-lawyer-dallas/` - Main auto accident page
2. `/truck-accident-attorney-dallas/` - Commercial truck focus
3. `/motorcycle-accident-lawyer-dallas/` - Motorcycle accidents
4. `/wrongful-death-attorney-dallas/` - Wrongful death cases
5. `/slip-fall-lawyer-dallas/` - Premises liability
6. `/uber-lyft-accident-lawyer-dallas/` - Rideshare accidents

### Week 1 Deliverables Checklist

- [ ] Google Ads account created and configured
- [ ] Billing and access set up
- [ ] All conversion actions created
- [ ] GTM container configured and published
- [ ] CallRail account set up with tracking numbers
- [ ] Call scoring rules configured
- [ ] Google Ads + CallRail integration active
- [ ] Landing pages audited and optimized
- [ ] Master negative keyword list created
- [ ] QA all tracking (test conversions)

---

## WEEK 2: Brand Protection Campaign Launch

### Campaign Purpose
Protect branded search terms from competitor conquest campaigns, capture high-intent searchers who know your firm, and maintain top position for brand queries at low cost.

### Campaign Structure

```
Campaign: [Firm Name] - Brand Protection
├── Daily Budget: $50-100 (adjust based on brand search volume)
├── Bid Strategy: Target Impression Share (95% top of page)
├── Networks: Search only
├── Locations: Texas (expanded for brand searches)
└── Ad Schedule: All hours (brand searches are always valuable)

Ad Groups:
├── AG1: Exact Brand Match
│   ├── Keywords:
│   │   ├── [firm name] (exact)
│   │   ├── [firm name] lawyers (exact)
│   │   ├── [firm name] attorneys (exact)
│   │   ├── [firm name] law firm (exact)
│   │   └── [firm name] dallas (exact)
│   └── Ads: 3 RSAs focused on brand reinforcement
│
├── AG2: Brand + Service
│   ├── Keywords:
│   │   ├── [firm name] car accident (exact)
│   │   ├── [firm name] personal injury (exact)
│   │   ├── [firm name] truck accident (exact)
│   │   └── [firm name] wrongful death (exact)
│   └── Ads: 3 RSAs with service-specific messaging
│
├── AG3: Brand + Location
│   ├── Keywords:
│   │   ├── [firm name] fort worth (exact)
│   │   ├── [firm name] plano (exact)
│   │   ├── [firm name] arlington (exact)
│   │   └── [firm name] irving (exact)
│   └── Ads: 3 RSAs with location-specific elements
│
└── AG4: Brand Misspellings
    ├── Keywords: [common misspellings of firm name]
    └── Ads: 3 RSAs (same as AG1)
```

### Ad Copy Templates - Brand Campaign

**Ad Group 1: Exact Brand Match**

*Responsive Search Ad 1:*
```
Headlines (15 options, system selects best 3):
H1: [Firm Name] | Official Site
H2: Dallas Personal Injury Lawyers
H3: Call Now: (214) XXX-XXXX
H4: Free Case Evaluation Today
H5: No Fee Unless We Win
H6: Millions Recovered for Clients
H7: 24/7 Legal Help Available
H8: Trusted Dallas Law Firm
H9: Over [X] Years Experience
H10: Top-Rated Injury Attorneys
H11: Fighting for Accident Victims
H12: Se Habla Español
H13: Award-Winning Legal Team
H14: Results That Matter
H15: Your Recovery, Our Priority

Descriptions (4 options, system selects best 2):
D1: Official website of [Firm Name]. Dallas-Fort Worth's trusted personal injury attorneys. Free consultations available 24/7. Call today.
D2: [Firm Name] has recovered millions for injury victims across Texas. No upfront costs - we only get paid when you win. Contact us now.
D3: Looking for [Firm Name]? We're here to help with your injury case. Experienced attorneys ready to fight for your maximum compensation.
D4: Contact [Firm Name] directly. Our award-winning Dallas injury lawyers offer free case reviews. Spanish-speaking staff available.
```

### Ad Extensions - Brand Campaign

**Sitelink Extensions (8 minimum):**
```
Sitelink 1:
Text: Free Case Evaluation
Description 1: Get your free consultation today
Description 2: No obligation, 100% confidential
Final URL: /free-consultation/

Sitelink 2:
Text: Our Case Results
Description 1: See our track record of success
Description 2: Millions recovered for clients
Final URL: /case-results/

Sitelink 3:
Text: Meet Our Attorneys
Description 1: Experienced Dallas injury lawyers
Description 2: Board certified trial attorneys
Final URL: /our-team/

Sitelink 4:
Text: Car Accident Cases
Description 1: Dallas auto accident attorneys
Description 2: We handle all vehicle crashes
Final URL: /car-accident-lawyer/

Sitelink 5:
Text: Truck Accident Lawyers
Description 1: 18-wheeler crash specialists
Description 2: We take on big trucking companies
Final URL: /truck-accident-lawyer/

Sitelink 6:
Text: Client Testimonials
Description 1: Read what our clients say
Description 2: 5-star rated law firm
Final URL: /testimonials/

Sitelink 7:
Text: About Our Firm
Description 1: Learn about [Firm Name]
Description 2: Serving DFW since [year]
Final URL: /about-us/

Sitelink 8:
Text: Contact Us Today
Description 1: Multiple office locations
Description 2: Available 24/7 for emergencies
Final URL: /contact/
```

**Callout Extensions (8 options):**
```
- Free Consultations
- No Win, No Fee
- 24/7 Availability
- Se Habla Español
- Millions Recovered
- [X]+ Years Experience
- Top-Rated on Google
- Same-Day Appointments
```

**Structured Snippet Extensions:**
```
Header: Services
Values: Car Accidents, Truck Accidents, Motorcycle Crashes, Wrongful Death, Slip & Fall, Rideshare Accidents

Header: Neighborhoods
Values: Downtown Dallas, Fort Worth, Plano, Arlington, Irving, Frisco
```

**Call Extension:**
```
Phone Number: (214) XXX-XXXX (main tracking number)
Call Reporting: On
Count calls as conversions: Yes (for brand campaign)
```

**Location Extensions:**
Link Google Business Profile to show:
- Office address
- Hours of operation
- Distance from searcher
- Directions link

**Image Extensions:**
```
Upload 4-6 images:
- Firm logo (square format)
- Office exterior
- Attorney headshots
- Award badges
- Team photo
```

### Brand Campaign Settings

```
Campaign Settings:
├── Goal: Leads
├── Networks: Search Network only (no Display)
├── Locations:
│   ├── Target: Texas
│   ├── Exclude: None
│   └── Location Options: "People in or regularly in your targeted locations"
├── Languages: English, Spanish
├── Budget: $50-100/day
├── Bidding:
│   ├── Strategy: Target Impression Share
│   ├── Where: Absolute top of page
│   ├── Target: 95%
│   └── Max CPC bid limit: $15
├── Ad Rotation: Optimize
├── Ad Schedule: All day, every day
└── Devices: All (no adjustments needed for brand)
```

### Week 2 KPI Targets

| Metric | Target | Action if Not Met |
|--------|--------|-------------------|
| Impression Share | >95% | Increase max CPC bid |
| Click-Through Rate | >15% | Improve ad copy relevance |
| Average CPC | <$5 | Check for competitor bidding |
| Quality Score | 8-10 | Improve landing page experience |
| Conversion Rate | >10% | Optimize landing page |
| Cost Per Lead | <$50 | Expected for brand terms |

### Week 2 Deliverables Checklist

- [ ] Brand campaign created with all ad groups
- [ ] All RSAs written and approved
- [ ] All ad extensions configured
- [ ] Campaign settings verified
- [ ] Landing pages mapped to ad groups
- [ ] Conversion tracking verified for brand campaign
- [ ] Initial QA completed (search for brand, verify ads show)
- [ ] Competitor brand bidding monitored (set up alerts)

---

## WEEK 3: High-Intent Keyword Campaign Launch

### Campaign Strategy Overview

This is your primary lead generation campaign targeting users actively searching for personal injury attorneys. We'll structure campaigns by service line to maintain ad relevance and Quality Score.

### Campaign 1: Car Accident Attorney (Primary)

```
Campaign: DFW - Car Accident Attorney
├── Daily Budget: $500-800
├── Bid Strategy: Maximize Conversions (initial) → Target CPA (after 30 conversions)
├── Networks: Search only
├── Locations: DFW Metro (detailed below)
└── Ad Schedule: Weighted toward high-conversion hours

Location Targeting (25-mile radius of each):
├── Dallas, TX (include)
├── Fort Worth, TX (include)
├── Arlington, TX (include)
├── Plano, TX (include)
├── Irving, TX (include)
├── Garland, TX (include)
├── Frisco, TX (include)
├── McKinney, TX (include)
├── Denton, TX (include)
└── Grand Prairie, TX (include)

Location Exclusions:
├── Oklahoma (exclude)
└── Louisiana (exclude)
```

#### Ad Group Structure - Car Accident Campaign

```
Ad Group 1: Car Accident Lawyer Dallas [HIGH INTENT]
├── Max CPC (initial): $150
├── Keywords:
│   ├── [car accident lawyer dallas] - Exact
│   ├── [car accident attorney dallas] - Exact
│   ├── [auto accident lawyer dallas] - Exact
│   ├── [dallas car accident lawyer] - Exact
│   ├── [dallas car accident attorney] - Exact
│   ├── "car accident lawyer dallas" - Phrase
│   ├── "car accident attorney dallas" - Phrase
│   └── "auto accident lawyer dallas" - Phrase
├── Negative Keywords:
│   ├── free
│   ├── cheap
│   ├── pro bono
│   └── [competitor names]
└── Landing Page: /car-accident-lawyer-dallas/

Ad Group 2: Car Accident Lawyer Fort Worth [HIGH INTENT]
├── Max CPC (initial): $125
├── Keywords:
│   ├── [car accident lawyer fort worth] - Exact
│   ├── [car accident attorney fort worth] - Exact
│   ├── [fort worth car accident lawyer] - Exact
│   ├── [auto accident attorney fort worth] - Exact
│   ├── "car accident lawyer fort worth" - Phrase
│   └── "auto accident lawyer fort worth" - Phrase
└── Landing Page: /car-accident-lawyer-fort-worth/

Ad Group 3: Car Accident Lawyer Near Me [HIGH INTENT]
├── Max CPC (initial): $175
├── Keywords:
│   ├── [car accident lawyer near me] - Exact
│   ├── [car accident attorney near me] - Exact
│   ├── [auto accident lawyer near me] - Exact
│   ├── [best car accident lawyer near me] - Exact
│   ├── "car accident lawyer near me" - Phrase
│   └── "auto accident attorney near me" - Phrase
└── Landing Page: /car-accident-lawyer-dallas/ (geo-targeted)

Ad Group 4: Car Wreck Lawyer [HIGH INTENT]
├── Max CPC (initial): $140
├── Keywords:
│   ├── [car wreck lawyer dallas] - Exact
│   ├── [car wreck attorney dallas] - Exact
│   ├── [wreck lawyer dallas] - Exact
│   ├── [dallas car wreck lawyer] - Exact
│   ├── "car wreck lawyer dallas" - Phrase
│   └── "car wreck attorney" - Phrase
└── Landing Page: /car-accident-lawyer-dallas/

Ad Group 5: Auto Injury Attorney [HIGH INTENT]
├── Max CPC (initial): $135
├── Keywords:
│   ├── [auto injury lawyer dallas] - Exact
│   ├── [auto injury attorney dallas] - Exact
│   ├── [vehicle accident lawyer dallas] - Exact
│   ├── "auto injury lawyer dallas" - Phrase
│   └── "vehicle accident attorney dallas" - Phrase
└── Landing Page: /car-accident-lawyer-dallas/

Ad Group 6: Car Accident Suburban Cities
├── Max CPC (initial): $100
├── Keywords:
│   ├── [car accident lawyer plano] - Exact
│   ├── [car accident lawyer arlington] - Exact
│   ├── [car accident lawyer irving] - Exact
│   ├── [car accident lawyer garland] - Exact
│   ├── [car accident lawyer frisco] - Exact
│   ├── [car accident lawyer mckinney] - Exact
│   ├── [car accident attorney plano] - Exact
│   ├── [car accident attorney arlington] - Exact
│   └── ... (continue pattern for all suburbs)
└── Landing Page: Geo-specific or main /car-accident-lawyer-dallas/
```

#### Ad Copy - Car Accident Campaign

**Responsive Search Ad 1 (Primary):**
```
Headlines:
H1: Dallas Car Accident Lawyers
H2: Injured in a Crash? Call Now
H3: Free Consultation - Call (214) XXX-XXXX
H4: No Fee Unless We Win Your Case
H5: Millions Recovered for Clients
H6: Top-Rated Dallas Injury Attorneys
H7: Get the Compensation You Deserve
H8: 24/7 Emergency Legal Help
H9: Fighting Insurance Companies
H10: [X] Years of Proven Results
H11: We Handle Your Case Personally
H12: Board Certified Trial Lawyers
H13: Aggressive Legal Representation
H14: Dallas Car Wreck Attorneys
H15: Se Habla Español

Descriptions:
D1: Injured in a Dallas car accident? Our experienced attorneys have recovered millions for crash victims. Free case review - no upfront costs.
D2: Don't face insurance companies alone. [Firm Name]'s car accident lawyers fight for maximum compensation. Call 24/7 for a free consultation.
D3: Texas car accident attorney with [X]+ years experience. We investigate, negotiate & litigate your case. No fee unless we win.
D4: Hurt in an auto accident in DFW? Get a free case evaluation today. Our aggressive lawyers take on insurance companies & win.
```

**Responsive Search Ad 2 (Urgency Focus):**
```
Headlines:
H1: Car Accident Today? Call Now
H2: Dallas Auto Accident Attorneys
H3: Immediate Legal Help Available
H4: Don't Wait - Evidence Fades Fast
H5: Free Same-Day Consultation
H6: We Come to You (Hospital/Home)
H7: Start Your Claim Today
H8: Time Limits Apply - Act Now
H9: Protect Your Legal Rights
H10: Call (214) XXX-XXXX Now
H11: 24/7 Attorney Hotline
H12: No Upfront Legal Fees
H13: Get What You're Owed
H14: Injured? We Can Help Today
H15: Dallas Crash Injury Lawyers

Descriptions:
D1: Just had a car accident in Dallas? Call now for immediate legal guidance. Evidence disappears fast - protect your rights today.
D2: Injured in a wreck? Don't talk to insurance without us. Free 24/7 consultation with experienced Dallas car accident attorneys.
D3: Time-sensitive: Texas has a 2-year statute of limitations. Our car accident lawyers offer same-day appointments. Call now.
D4: Hospital? Home? We come to you. Dallas car accident attorneys available 24/7 for emergencies. Free consultation, no obligations.
```

**Responsive Search Ad 3 (Results Focus):**
```
Headlines:
H1: $XX Million Won for Clients
H2: Proven Car Accident Results
H3: Dallas' Top-Rated Injury Firm
H4: We've Won Thousands of Cases
H5: Maximum Compensation Pursued
H6: Insurance Companies Fear Us
H7: Track Record of Big Verdicts
H8: Award-Winning Trial Lawyers
H9: See Our Case Results
H10: Fighting for What's Fair
H11: Car Accident Specialists
H12: Exposed Insurance Tactics
H13: We Don't Back Down
H14: Dallas Injury Law Leaders
H15: Results You Can Trust

Descriptions:
D1: [Firm Name] has recovered $XX million+ for Dallas car accident victims. See our proven results. Free consultation to discuss your case.
D2: Our Dallas car accident lawyers have a track record insurance companies respect. We fight for every dollar you deserve.
D3: Award-winning car accident attorneys in Dallas. [X]+ 5-star reviews. Exposed insurance company tactics. Free case review.
D4: When results matter, choose [Firm Name]. Our car accident lawyers have secured life-changing verdicts for injured clients.
```

### Campaign 2: Personal Injury Attorney (General)

```
Campaign: DFW - Personal Injury Attorney
├── Daily Budget: $400-600
├── Bid Strategy: Maximize Conversions → Target CPA
├── Networks: Search only
└── Locations: DFW Metro

Ad Groups:

Ad Group 1: Personal Injury Lawyer Dallas
├── Keywords:
│   ├── [personal injury lawyer dallas] - Exact
│   ├── [personal injury attorney dallas] - Exact
│   ├── [dallas personal injury lawyer] - Exact
│   ├── [injury lawyer dallas] - Exact
│   ├── "personal injury lawyer dallas" - Phrase
│   └── "personal injury attorney dallas" - Phrase
└── Landing Page: /personal-injury-lawyer-dallas/

Ad Group 2: Personal Injury Lawyer Fort Worth
├── Keywords:
│   ├── [personal injury lawyer fort worth] - Exact
│   ├── [personal injury attorney fort worth] - Exact
│   ├── [fort worth personal injury lawyer] - Exact
│   ├── "personal injury lawyer fort worth" - Phrase
│   └── "injury attorney fort worth" - Phrase
└── Landing Page: /personal-injury-lawyer-fort-worth/

Ad Group 3: Personal Injury Lawyer Near Me
├── Keywords:
│   ├── [personal injury lawyer near me] - Exact
│   ├── [personal injury attorney near me] - Exact
│   ├── [best personal injury lawyer near me] - Exact
│   ├── [injury lawyer near me] - Exact
│   └── "personal injury lawyer near me" - Phrase
└── Landing Page: /personal-injury-lawyer-dallas/

Ad Group 4: Accident Lawyer (General)
├── Keywords:
│   ├── [accident lawyer dallas] - Exact
│   ├── [accident attorney dallas] - Exact
│   ├── [dallas accident lawyer] - Exact
│   ├── [accident lawyer near me] - Exact
│   ├── "accident lawyer dallas" - Phrase
│   └── "accident attorney near me" - Phrase
└── Landing Page: /personal-injury-lawyer-dallas/

Ad Group 5: Injury Attorney (General)
├── Keywords:
│   ├── [injury attorney dallas] - Exact
│   ├── [injury lawyer dallas] - Exact
│   ├── [dallas injury attorney] - Exact
│   ├── "injury attorney dallas" - Phrase
│   └── "injury lawyer dallas" - Phrase
└── Landing Page: /personal-injury-lawyer-dallas/
```

### Campaign 3: Wrongful Death Attorney

```
Campaign: DFW - Wrongful Death Attorney
├── Daily Budget: $200-300
├── Bid Strategy: Maximize Conversions
├── Networks: Search only
└── Locations: DFW Metro + Statewide Texas

Ad Groups:

Ad Group 1: Wrongful Death Lawyer Dallas
├── Max CPC: $175
├── Keywords:
│   ├── [wrongful death lawyer dallas] - Exact
│   ├── [wrongful death attorney dallas] - Exact
│   ├── [dallas wrongful death lawyer] - Exact
│   ├── [wrongful death law firm dallas] - Exact
│   ├── "wrongful death lawyer dallas" - Phrase
│   └── "wrongful death attorney dallas" - Phrase
└── Landing Page: /wrongful-death-lawyer-dallas/

Ad Group 2: Wrongful Death Lawyer Texas
├── Max CPC: $150
├── Keywords:
│   ├── [wrongful death lawyer texas] - Exact
│   ├── [wrongful death attorney texas] - Exact
│   ├── [texas wrongful death lawyer] - Exact
│   ├── "wrongful death lawyer texas" - Phrase
│   └── "wrongful death attorney texas" - Phrase
└── Landing Page: /wrongful-death-lawyer-texas/

Ad Group 3: Fatal Accident Attorney
├── Max CPC: $160
├── Keywords:
│   ├── [fatal accident lawyer dallas] - Exact
│   ├── [fatal car accident attorney] - Exact
│   ├── [death by car accident lawyer] - Exact
│   ├── "fatal accident lawyer" - Phrase
│   └── "fatal crash attorney dallas" - Phrase
└── Landing Page: /wrongful-death-lawyer-dallas/
```

### Bidding Strategy Timeline

```
Week 3-4: Learning Phase
├── Strategy: Maximize Conversions (no target)
├── Rationale: Gather conversion data, let algorithm learn
├── Expected CPA: Variable (accept higher CPAs initially)
└── Goal: Accumulate 30+ conversions

Week 5-6: Transition Phase
├── Strategy: Maximize Conversions with Target CPA
├── Target CPA: Set at 20% above actual average CPA
├── Rationale: Guide algorithm while maintaining volume
└── Goal: Stabilize CPA while maintaining lead volume

Week 7+: Optimization Phase
├── Strategy: Target CPA (strict)
├── Target CPA: Reduce by 10% every 2 weeks if hitting targets
├── Rationale: Maximize efficiency
└── Goal: Achieve target CPA of $200-300 for car accidents
```

### Ad Schedule Configuration

Based on legal lead conversion patterns:

```
Ad Schedule Bid Adjustments:

Monday-Friday:
├── 6am-8am: +0%
├── 8am-10am: +15% (morning commute accidents)
├── 10am-12pm: +10%
├── 12pm-2pm: +5%
├── 2pm-4pm: +10%
├── 4pm-7pm: +20% (evening commute accidents)
├── 7pm-10pm: +5%
└── 10pm-6am: -20%

Saturday:
├── 8am-12pm: +10%
├── 12pm-6pm: +15%
├── 6pm-10pm: +5%
└── 10pm-8am: -25%

Sunday:
├── 10am-2pm: +10%
├── 2pm-6pm: +15%
├── 6pm-10pm: +5%
└── 10pm-10am: -30%
```

### Device Bid Adjustments

```
Initial Device Adjustments:
├── Desktop: +0% (baseline)
├── Mobile: +10% (people search after accidents on mobile)
└── Tablet: -10% (lower conversion rates typically)

Adjust based on data after 2 weeks.
```

### Audience Targeting (Observation Mode)

Add these audiences in "Observation" mode to collect data:

```
In-Market Audiences:
├── Legal Services
├── Auto Insurance
├── Vehicle Shopping (recently in accident, buying new car)
└── Health & Medical (potential injury victims)

Affinity Audiences:
├── Auto Enthusiasts
├── Motorcycle Enthusiasts
└── Outdoor Enthusiasts

Demographics (Observation):
├── Age: All
├── Gender: All
├── Household Income: All
└── Parental Status: All
```

### Week 3 Budget Allocation

| Campaign | Daily Budget | Monthly Budget |
|----------|--------------|----------------|
| Car Accident Attorney | $600 | $18,000 |
| Personal Injury Attorney | $400 | $12,000 |
| Wrongful Death Attorney | $200 | $6,000 |
| Brand Protection | $75 | $2,250 |
| **Total** | **$1,275** | **$38,250** |

### Week 3 KPI Targets

| Metric | Car Accident | Personal Injury | Wrongful Death |
|--------|--------------|-----------------|----------------|
| Impressions | 5,000+ | 3,000+ | 1,000+ |
| Clicks | 150+ | 100+ | 30+ |
| CTR | 3%+ | 3%+ | 3%+ |
| Avg CPC | $80-120 | $70-100 | $100-150 |
| Conversions | 10+ | 7+ | 2+ |
| Conv Rate | 6%+ | 6%+ | 6%+ |
| Cost/Conv | <$400 | <$350 | <$500 |

### Week 3 Deliverables Checklist

- [ ] Car Accident campaign created with all ad groups
- [ ] Personal Injury campaign created with all ad groups
- [ ] Wrongful Death campaign created with all ad groups
- [ ] All RSAs written (3 per ad group minimum)
- [ ] All ad extensions applied
- [ ] Negative keyword lists applied
- [ ] Audience targeting configured (observation)
- [ ] Ad schedule bid adjustments set
- [ ] Device bid adjustments set
- [ ] Landing pages live and tracking
- [ ] QA all campaigns (search queries, verify ads)

---

## WEEK 4: Local Services Ads (LSA) Application & Setup

### LSA Overview

Local Services Ads appear at the very top of Google search results, above traditional PPC ads. For personal injury attorneys, LSAs can provide:
- Premium placement
- Pay-per-lead model (not pay-per-click)
- Google Screened badge builds trust
- Lower cost per lead than traditional PPC

### Day 1-2: Eligibility & Application

#### Pre-Application Checklist
```
Business Requirements:
- [ ] Valid Texas State Bar license for all attorneys
- [ ] Professional liability insurance (malpractice)
- [ ] Physical office in DFW area
- [ ] Background check consent for all attorneys
- [ ] No disciplinary actions on record
- [ ] Business registered with Texas Secretary of State

Documentation Needed:
- [ ] Business license/registration
- [ ] Professional licenses for all attorneys
- [ ] Insurance certificates
- [ ] Photos of attorneys and office
```

#### Application Process

**Step 1: Create LSA Profile**
```
Navigate to: ads.google.com/local-services-ads
Click: "Get Started"

Business Information:
├── Business Name: [Exact firm name as registered]
├── Business Category: Personal Injury Attorney
├── Service Areas: (configure below)
├── Business Hours: 8am-6pm M-F, 9am-1pm Sat
├── Phone: Main office number
└── Website: Firm website URL
```

**Step 2: Configure Service Areas**

```
Primary Service Area Configuration:

Service Area Type: "List of cities" (more control than radius)

Cities to Include:
├── Dallas, TX
├── Fort Worth, TX
├── Arlington, TX
├── Plano, TX
├── Irving, TX
├── Garland, TX
├── Grand Prairie, TX
├── McKinney, TX
├── Frisco, TX
├── Denton, TX
├── Mesquite, TX
├── Carrollton, TX
├── Richardson, TX
├── Lewisville, TX
├── Allen, TX
├── Flower Mound, TX
├── North Richland Hills, TX
├── Bedford, TX
├── Grapevine, TX
├── Euless, TX
├── Colleyville, TX
├── Southlake, TX
├── Keller, TX
├── Coppell, TX
└── Mansfield, TX
```

**Step 3: Configure Services**

```
Services Offered (Select All Applicable):
├── Personal Injury
├── Car Accident
├── Truck Accident
├── Motorcycle Accident
├── Wrongful Death
├── Slip and Fall
├── Medical Malpractice (if applicable)
├── Product Liability (if applicable)
└── Premises Liability

Service Descriptions (create compelling copy):

Personal Injury:
"Experienced Dallas personal injury attorneys fighting for maximum compensation. Free consultations, no fee unless we win."

Car Accident:
"Dallas car accident lawyers with millions recovered. We handle insurance companies while you focus on recovery."

Truck Accident:
"Specialized truck accident attorneys taking on big trucking companies. Thorough investigation, aggressive representation."
```

### Day 3-4: Verification & Google Screened Badge

#### Background Check Process
```
Background Check Provider: Pinkerton (Google's partner)

Process:
1. Each attorney receives email invitation
2. Complete online application
3. Consent to background check
4. Provide required documentation
5. Wait 2-5 business days for results

Documents Required:
- Government-issued ID
- Professional license number
- Social Security Number (for background check only)
```

#### License Verification
```
Google verifies with Texas State Bar:
- Active license status
- No disciplinary actions
- Good standing

Timeline: 3-7 business days
```

#### Insurance Verification
```
Required Coverage:
- Professional Liability (Malpractice) Insurance
- Minimum coverage: Varies by state

Provide:
- Certificate of Insurance
- Insurance company contact for verification
- Policy effective dates
```

### Day 5: Profile Optimization

#### Business Profile Setup

```
Profile Photos (upload all):
├── Primary Photo: Professional headshot of lead attorney
├── Additional Photos:
│   ├── Office exterior
│   ├── Office interior (reception/meeting room)
│   ├── Team photo
│   ├── Individual attorney headshots
│   └── Award/certificate wall
└── Photo Requirements:
    ├── Minimum 300x300 pixels
    ├── Clear, professional quality
    └── No stock photos
```

#### Business Description
```
Character Limit: 1,000 characters

Example:
"[Firm Name] has been fighting for injury victims in Dallas-Fort Worth for over [X] years. Our experienced personal injury attorneys have recovered millions of dollars for clients hurt in car accidents, truck crashes, and other serious incidents.

We understand that an injury can turn your life upside down. Medical bills pile up, you can't work, and insurance companies try to pay you as little as possible. That's where we come in.

Our approach is simple: we treat every client like family and fight for maximum compensation. We handle all types of personal injury cases including car accidents, 18-wheeler crashes, motorcycle wrecks, wrongful death, and slip-and-fall injuries.

What sets us apart:
• Free consultations - no obligation
• No fee unless we win your case
• We come to you - hospital, home, wherever you need us
• 24/7 availability for emergencies
• Spanish-speaking staff available

Don't let insurance companies take advantage of you. Contact [Firm Name] today for your free case evaluation."
```

### Day 6-7: Budget & Bidding Configuration

#### LSA Budget Settings

```
Budget Configuration:
├── Budget Mode: Weekly budget
├── Weekly Budget: $2,000-4,000 (start conservative)
├── Bid Mode: Maximize leads (let Google optimize)
└── Lead Preferences: All lead types (calls, messages)

Lead Type Settings:
├── Phone Calls: Enabled
├── Messages: Enabled
└── Booking Requests: Enabled (if applicable)
```

#### LSA Bidding Strategy

```
Initial Strategy:
- Use "Maximize leads" mode
- Set budget at 50% of planned weekly spend
- Let system establish baseline

After 2 Weeks:
- Analyze cost per lead
- Adjust budget up if CPL is acceptable
- Consider manual bidding if CPL too high

Target Metrics:
- Cost per lead: $100-200
- Lead response time: <5 minutes
- Lead-to-case conversion: 10-15%
```

### LSA Lead Management

#### Lead Response Protocol
```
CRITICAL: LSA ranking factors include response time

Response Time Goals:
├── Phone calls: Answer immediately (have dedicated intake)
├── Messages: Respond within 5 minutes during business hours
└── After-hours: Response within 30 minutes

Lead Response Script (Messages):
"Thank you for contacting [Firm Name]. I'm sorry to hear about your accident. We'd like to learn more about your situation and see how we can help.

Are you available for a quick call in the next few minutes? If so, what's the best number to reach you?

If you prefer, you can call us directly at (214) XXX-XXXX.

- [Attorney Name], [Firm Name]"
```

#### Lead Categorization
```
In LSA Dashboard, categorize each lead:

Mark as "Booked":
- Consultation scheduled
- Case accepted

Mark as "Completed":
- Lead followed up but not proceeding
- Wrong case type (workers comp, etc.)

Dispute Lead (request credit):
- Wrong service area
- Spam/fake lead
- Duplicate lead
- Wrong practice area (must be clear mismatch)

Timeline to Dispute: Within 60 days
```

### LSA Reviews Strategy

#### Review Collection Plan
```
Reviews significantly impact LSA ranking and visibility.

Week 1-2 Actions:
1. Identify 10-15 past satisfied clients
2. Reach out personally to request Google review
3. Send follow-up email with direct review link
4. Thank clients who leave reviews

Ongoing Review Generation:
- Add review request to case closing process
- Send automated email 30 days post-settlement
- Include direct link to Google review page
- Respond to all reviews within 24 hours
```

#### Review Response Templates

```
5-Star Review Response:
"Thank you so much for your kind words, [Name]. It was our privilege to represent you, and we're thrilled we could help you through such a difficult time. If you ever need anything in the future, please don't hesitate to reach out. Wishing you all the best."

4-Star Review Response:
"Thank you for taking the time to share your experience, [Name]. We're glad we could help with your case. If there's anything we could have done better, we'd love to hear your feedback. Our goal is always to provide the best possible service to our clients."

Negative Review Response (rare):
"Thank you for your feedback, [Name]. We take all concerns seriously and would like to understand your experience better. Please contact our office directly at [phone] so we can address any issues. Client satisfaction is our top priority."
```

### Week 4 LSA Checklist

- [ ] LSA application submitted
- [ ] All attorney background checks initiated
- [ ] License verification in progress
- [ ] Insurance verification submitted
- [ ] Service areas configured
- [ ] Business profile optimized
- [ ] Photos uploaded
- [ ] Business description written
- [ ] Budget and bidding configured
- [ ] Lead response protocol established
- [ ] Review collection plan initiated
- [ ] Intake team trained on LSA leads

### Week 4 Budget Summary (Month 1 Total)

| Channel | Week 4 Budget | Month 1 Total |
|---------|---------------|---------------|
| Brand Protection | $525 | $2,100 |
| Car Accident | $4,200 | $12,600 |
| Personal Injury | $2,800 | $8,400 |
| Wrongful Death | $1,400 | $4,200 |
| LSA (prorated) | $1,500 | $1,500 |
| **Total** | **$10,425** | **$28,800** |

---

# MONTH 2: EXPANSION & REMARKETING

---

## WEEKS 5-6: Niche Campaign Expansion

### Campaign 4: Truck Accident Attorney

Truck accident cases are high-value (often $500K+ settlements), justifying higher CPCs and dedicated campaigns.

```
Campaign: DFW - Truck Accident Attorney
├── Daily Budget: $300-500
├── Bid Strategy: Maximize Conversions → Target CPA
├── Networks: Search only
├── Locations: DFW Metro + Major I-corridors (I-35, I-20, I-30, I-45)
└── Target CPA Goal: $400-600

Ad Groups:

Ad Group 1: Truck Accident Lawyer Dallas [HIGHEST INTENT]
├── Max CPC: $200
├── Keywords:
│   ├── [truck accident lawyer dallas] - Exact
│   ├── [truck accident attorney dallas] - Exact
│   ├── [18 wheeler accident lawyer dallas] - Exact
│   ├── [semi truck accident attorney dallas] - Exact
│   ├── [dallas truck accident lawyer] - Exact
│   ├── "truck accident lawyer dallas" - Phrase
│   ├── "18 wheeler accident lawyer dallas" - Phrase
│   └── "semi truck accident attorney" - Phrase
└── Landing Page: /truck-accident-lawyer-dallas/

Ad Group 2: 18-Wheeler Accident Lawyer
├── Max CPC: $180
├── Keywords:
│   ├── [18 wheeler accident lawyer] - Exact
│   ├── [18 wheeler accident attorney] - Exact
│   ├── [eighteen wheeler accident lawyer] - Exact
│   ├── [18 wheeler crash lawyer] - Exact
│   ├── [18 wheeler wreck attorney] - Exact
│   ├── "18 wheeler accident lawyer" - Phrase
│   └── "18 wheeler accident attorney" - Phrase
└── Landing Page: /truck-accident-lawyer-dallas/

Ad Group 3: Semi Truck Accident Lawyer
├── Max CPC: $175
├── Keywords:
│   ├── [semi truck accident lawyer] - Exact
│   ├── [semi truck accident attorney] - Exact
│   ├── [semi accident lawyer] - Exact
│   ├── [semi truck crash attorney] - Exact
│   ├── "semi truck accident lawyer" - Phrase
│   └── "semi truck accident attorney" - Phrase
└── Landing Page: /truck-accident-lawyer-dallas/

Ad Group 4: Big Rig / Commercial Truck
├── Max CPC: $160
├── Keywords:
│   ├── [big rig accident lawyer] - Exact
│   ├── [big rig accident attorney] - Exact
│   ├── [commercial truck accident lawyer] - Exact
│   ├── [commercial vehicle accident attorney] - Exact
│   ├── "big rig accident lawyer" - Phrase
│   └── "commercial truck accident lawyer" - Phrase
└── Landing Page: /truck-accident-lawyer-dallas/

Ad Group 5: Trucking Company / Fleet
├── Max CPC: $150
├── Keywords:
│   ├── [trucking company accident lawyer] - Exact
│   ├── [trucking accident attorney] - Exact
│   ├── [delivery truck accident lawyer] - Exact
│   ├── [amazon delivery truck accident] - Exact
│   ├── [fedex truck accident lawyer] - Exact
│   ├── [ups truck accident attorney] - Exact
│   ├── "trucking company accident lawyer" - Phrase
│   └── "delivery truck accident lawyer" - Phrase
└── Landing Page: /truck-accident-lawyer-dallas/

Ad Group 6: Truck Accident Fort Worth / Suburbs
├── Max CPC: $140
├── Keywords:
│   ├── [truck accident lawyer fort worth] - Exact
│   ├── [18 wheeler accident attorney fort worth] - Exact
│   ├── [truck accident lawyer arlington] - Exact
│   ├── [semi truck accident lawyer plano] - Exact
│   ├── "truck accident lawyer fort worth" - Phrase
│   └── "18 wheeler accident lawyer" + [city] variations
└── Landing Page: /truck-accident-lawyer-dallas/
```

#### Truck Accident Ad Copy

**RSA 1 - Truck Accident Primary:**
```
Headlines:
H1: Dallas Truck Accident Lawyers
H2: 18-Wheeler Crash Attorneys
H3: Call (214) XXX-XXXX Now
H4: We Fight Trucking Companies
H5: Millions Recovered in Truck Cases
H6: Free Consultation - No Fee Unless We Win
H7: Experienced Semi-Truck Lawyers
H8: Big Rig Accident? Get Help Now
H9: Taking On Insurance Giants
H10: 24/7 Emergency Response
H11: We Investigate Immediately
H12: Protect Evidence - Call Today
H13: Trucking Company Liability Experts
H14: FMCSA Violation Specialists
H15: Results Against Trucking Corps

Descriptions:
D1: Hit by an 18-wheeler? Dallas truck accident lawyers who take on the biggest trucking companies. Free consultation - we come to you.
D2: Truck accidents cause catastrophic injuries. Our Dallas attorneys have recovered millions against trucking companies. Call 24/7.
D3: Semi-truck accident? Time is critical. We dispatch investigators immediately to preserve evidence. Free case review today.
D4: Trucking companies have teams of lawyers. Level the playing field with experienced Dallas truck accident attorneys. No fee unless we win.
```

#### Truck Accident Negative Keywords (Add to Campaign)
```
truck driving jobs
truck driver salary
trucking school
cdl training
truck for sale
used trucks
truck parts
truck repair
moving truck
food truck
monster truck
fire truck
tow truck (unless pursuing)
```

### Campaign 5: Rideshare Accident Attorney (Uber/Lyft)

Growing market segment with unique insurance complexities.

```
Campaign: DFW - Rideshare Accident Attorney
├── Daily Budget: $150-250
├── Bid Strategy: Maximize Conversions
├── Networks: Search only
├── Locations: DFW Metro (especially airport corridors, downtown)
└── Target CPA Goal: $300-400

Ad Groups:

Ad Group 1: Uber Accident Lawyer
├── Max CPC: $125
├── Keywords:
│   ├── [uber accident lawyer] - Exact
│   ├── [uber accident attorney] - Exact
│   ├── [uber crash lawyer] - Exact
│   ├── [uber car accident lawyer] - Exact
│   ├── [uber accident lawyer dallas] - Exact
│   ├── [uber driver accident attorney] - Exact
│   ├── "uber accident lawyer" - Phrase
│   └── "uber accident attorney dallas" - Phrase
└── Landing Page: /uber-accident-lawyer-dallas/

Ad Group 2: Lyft Accident Lawyer
├── Max CPC: $120
├── Keywords:
│   ├── [lyft accident lawyer] - Exact
│   ├── [lyft accident attorney] - Exact
│   ├── [lyft crash lawyer] - Exact
│   ├── [lyft car accident lawyer] - Exact
│   ├── [lyft accident lawyer dallas] - Exact
│   ├── [lyft driver accident attorney] - Exact
│   ├── "lyft accident lawyer" - Phrase
│   └── "lyft accident attorney dallas" - Phrase
└── Landing Page: /lyft-accident-lawyer-dallas/

Ad Group 3: Rideshare Accident General
├── Max CPC: $110
├── Keywords:
│   ├── [rideshare accident lawyer] - Exact
│   ├── [rideshare accident attorney] - Exact
│   ├── [ride share crash lawyer] - Exact
│   ├── [rideshare injury lawyer] - Exact
│   ├── [rideshare accident lawyer dallas] - Exact
│   ├── "rideshare accident lawyer" - Phrase
│   └── "rideshare accident attorney" - Phrase
└── Landing Page: /rideshare-accident-lawyer-dallas/

Ad Group 4: Uber/Lyft Passenger Injury
├── Max CPC: $100
├── Keywords:
│   ├── [uber passenger injury lawyer] - Exact
│   ├── [lyft passenger accident attorney] - Exact
│   ├── [hurt in uber accident] - Exact
│   ├── [injured as uber passenger] - Exact
│   ├── [rideshare passenger injury] - Exact
│   ├── "uber passenger injury lawyer" - Phrase
│   └── "lyft passenger accident attorney" - Phrase
└── Landing Page: /rideshare-accident-lawyer-dallas/
```

#### Rideshare Ad Copy

**RSA 1 - Rideshare Primary:**
```
Headlines:
H1: Uber Accident Lawyers Dallas
H2: Lyft Crash Attorneys - Call Now
H3: Rideshare Accident? Get Help
H4: Free Consultation (214) XXX-XXXX
H5: We Know Uber & Lyft Insurance
H6: Passenger or Driver - We Help Both
H7: Complex Insurance? We Navigate It
H8: Dallas Rideshare Injury Lawyers
H9: No Fee Unless We Win
H10: 24/7 Attorney Hotline
H11: Hit by Uber Driver? Call Us
H12: Lyft Accident Compensation
H13: Multiple Insurance Policies = More Money
H14: Rideshare Crash Specialists
H15: Get What You Deserve

Descriptions:
D1: Uber or Lyft accident in Dallas? Rideshare cases involve complex insurance - our attorneys know how to maximize your recovery. Free consultation.
D2: Injured as a rideshare passenger or hit by an Uber/Lyft driver? We handle all rideshare accident claims. Call 24/7 for free case review.
D3: Rideshare accidents have multiple insurance policies. Our Dallas lawyers know how to access all available coverage. No fee unless we win.
D4: Dallas rideshare accident attorneys with experience against Uber and Lyft. We fight for passengers and drivers. Free consultation today.
```

### Campaign 6: Motorcycle Accident Attorney

High-severity injuries, strong case values.

```
Campaign: DFW - Motorcycle Accident Attorney
├── Daily Budget: $200-300
├── Bid Strategy: Maximize Conversions
├── Networks: Search only
├── Locations: DFW Metro
└── Target CPA Goal: $300-450

Ad Groups:

Ad Group 1: Motorcycle Accident Lawyer Dallas
├── Max CPC: $140
├── Keywords:
│   ├── [motorcycle accident lawyer dallas] - Exact
│   ├── [motorcycle accident attorney dallas] - Exact
│   ├── [dallas motorcycle accident lawyer] - Exact
│   ├── [motorcycle crash lawyer dallas] - Exact
│   ├── [motorcycle injury attorney dallas] - Exact
│   ├── "motorcycle accident lawyer dallas" - Phrase
│   └── "motorcycle accident attorney dallas" - Phrase
└── Landing Page: /motorcycle-accident-lawyer-dallas/

Ad Group 2: Motorcycle Accident Lawyer Near Me
├── Max CPC: $150
├── Keywords:
│   ├── [motorcycle accident lawyer near me] - Exact
│   ├── [motorcycle accident attorney near me] - Exact
│   ├── [motorcycle crash lawyer near me] - Exact
│   ├── [best motorcycle accident lawyer] - Exact
│   ├── "motorcycle accident lawyer near me" - Phrase
│   └── "motorcycle injury attorney near me" - Phrase
└── Landing Page: /motorcycle-accident-lawyer-dallas/

Ad Group 3: Motorcycle Wreck / Crash
├── Max CPC: $130
├── Keywords:
│   ├── [motorcycle wreck lawyer] - Exact
│   ├── [motorcycle crash attorney] - Exact
│   ├── [bike accident lawyer dallas] - Exact
│   ├── [biker injury attorney] - Exact
│   ├── "motorcycle wreck lawyer" - Phrase
│   └── "motorcycle crash attorney dallas" - Phrase
└── Landing Page: /motorcycle-accident-lawyer-dallas/

Ad Group 4: Hit Motorcycle / Biker
├── Max CPC: $125
├── Keywords:
│   ├── [hit while on motorcycle] - Exact
│   ├── [car hit my motorcycle] - Exact
│   ├── [biker hit by car lawyer] - Exact
│   ├── [motorcycle hit by truck] - Exact
│   ├── "hit while on motorcycle" - Phrase
│   └── "biker hit by car" - Phrase
└── Landing Page: /motorcycle-accident-lawyer-dallas/
```

#### Motorcycle Ad Copy

**RSA 1 - Motorcycle Primary:**
```
Headlines:
H1: Dallas Motorcycle Accident Lawyers
H2: Biker Injury Attorneys - Call Now
H3: We Ride, We Understand
H4: Free Consultation (214) XXX-XXXX
H5: Fighting for Injured Riders
H6: Motorcycle Crash? Get Help Today
H7: No Fee Unless We Win
H8: We Take on Insurance Companies
H9: Riders Helping Riders
H10: Maximum Compensation for Bikers
H11: Experienced Motorcycle Lawyers
H12: Hit by a Car? Call Us
H13: Dallas Biker Injury Attorneys
H14: 24/7 - We're Here for Riders
H15: Aggressive Representation

Descriptions:
D1: Injured in a motorcycle accident in Dallas? Our attorneys are fellow riders who understand what you're going through. Free consultation 24/7.
D2: Motorcyclists face bias from insurance companies. We fight back and get riders the compensation they deserve. No fee unless we win.
D3: Dallas motorcycle accident lawyers with a track record of results for bikers. We handle your case while you focus on recovery.
D4: Hit by a car on your motorcycle? Time is critical. Our Dallas biker injury attorneys investigate immediately. Call for free case review.
```

### Weeks 5-6 Budget Allocation

| Campaign | Daily Budget | Bi-Weekly Budget |
|----------|--------------|------------------|
| Brand Protection | $75 | $1,050 |
| Car Accident | $600 | $8,400 |
| Personal Injury | $400 | $5,600 |
| Wrongful Death | $200 | $2,800 |
| Truck Accident | $400 | $5,600 |
| Rideshare Accident | $200 | $2,800 |
| Motorcycle Accident | $250 | $3,500 |
| LSA | $285/day | $4,000 |
| **Total** | **$2,410** | **$33,750** |

### Weeks 5-6 KPI Targets (Niche Campaigns)

| Campaign | Target CPA | Target Conv Rate | Target CPL (LSA) |
|----------|------------|------------------|------------------|
| Truck Accident | $400-600 | 5%+ | N/A |
| Rideshare | $300-400 | 5%+ | N/A |
| Motorcycle | $300-450 | 5%+ | N/A |

---

## WEEKS 7-8: Remarketing Campaign Launch

### Remarketing Strategy Overview

Remarketing targets users who visited your website but didn't convert. For PI firms, this is critical because:
- Decision cycle can be days/weeks after accident
- Users research multiple firms
- Staying top-of-mind increases conversion

### Audience Creation in Google Ads

```
Navigate: Tools > Audience Manager > Audience Lists

Audience 1: All Website Visitors
├── Type: Website visitors
├── List members: Visitors of a page
├── Visited page URL contains: [your domain]
├── Pre-fill: Include past 30 days
├── Membership duration: 90 days
└── Description: All visitors to any page

Audience 2: Car Accident Page Visitors (No Conversion)
├── Type: Website visitors
├── List members: Visitors of a page who did NOT visit another page
├── Visited page URL contains: /car-accident
├── Did NOT visit URL containing: /thank-you, /confirmation
├── Membership duration: 30 days
└── Description: Visited car accident pages but didn't convert

Audience 3: Truck Accident Page Visitors (No Conversion)
├── Type: Website visitors
├── List members: Visitors of a page who did NOT visit another page
├── Visited page URL contains: /truck-accident
├── Did NOT visit URL containing: /thank-you, /confirmation
├── Membership duration: 30 days
└── Description: Visited truck accident pages but didn't convert

Audience 4: Contact Page Abandoners
├── Type: Website visitors
├── List members: Visitors of a page who did NOT visit another page
├── Visited page URL contains: /contact, /free-consultation
├── Did NOT visit URL containing: /thank-you
├── Membership duration: 14 days
└── Description: Started to contact but didn't complete

Audience 5: Converters (Exclusion List)
├── Type: Website visitors
├── List members: Visitors of a page
├── Visited page URL contains: /thank-you, /confirmation
├── Membership duration: 540 days
└── Description: People who converted - exclude from remarketing

Audience 6: High-Intent Visitors (Time on Site)
├── Type: Website visitors
├── List members: Custom combination
├── Rules: Visitors who spent 2+ minutes on site
├── Membership duration: 60 days
└── Description: Engaged visitors who researched but didn't convert
```

### Display Remarketing Campaign

```
Campaign: DFW - Display Remarketing
├── Campaign Type: Display
├── Goal: Leads
├── Daily Budget: $100-150
├── Bid Strategy: Target CPA ($50 goal)
├── Networks: Google Display Network
├── Locations: DFW Metro (same as search campaigns)
└── Frequency Cap: 5 impressions per day per user

Ad Group 1: General Remarketing
├── Audience: All Website Visitors (exclude converters)
├── Targeting: Audiences only (not content)
└── Ads: Responsive display ads + image ads

Ad Group 2: Car Accident Remarketing
├── Audience: Car Accident Page Visitors (exclude converters)
├── Targeting: Audiences only
└── Ads: Car accident specific messaging

Ad Group 3: Truck Accident Remarketing
├── Audience: Truck Accident Page Visitors (exclude converters)
├── Targeting: Audiences only
└── Ads: Truck accident specific messaging

Ad Group 4: Hot Leads (Contact Abandoners)
├── Audience: Contact Page Abandoners (exclude converters)
├── Targeting: Audiences only
├── Bid Adjustment: +50%
└── Ads: Urgency messaging - "Still have questions?"
```

### Display Ad Creative

#### Responsive Display Ad Setup

```
Ad Group: General Remarketing

Images (upload all sizes):
├── Square (1:1): 1200x1200, 300x300
├── Landscape (1.91:1): 1200x628, 600x314
├── Portrait (4:5): 960x1200 (optional)
└── Logo: 1200x1200 (square), 512x128 (landscape)

Headlines (5 options):
H1: Injured in an Accident?
H2: Dallas Personal Injury Lawyers
H3: Free Consultation Available
H4: No Fee Unless We Win
H5: [Firm Name] - Here to Help

Long Headlines (5 options):
L1: Injured in a Dallas Accident? Get the Compensation You Deserve.
L2: Don't Face Insurance Companies Alone - Free Consultation Today
L3: Dallas Personal Injury Lawyers Fighting for Your Rights
L4: Millions Recovered for Injury Victims - We Can Help You Too
L5: Still Researching? Let's Talk About Your Case - No Obligation

Descriptions (5 options):
D1: Free consultation with experienced Dallas injury attorneys. Call today.
D2: We fight insurance companies so you can focus on recovery.
D3: No upfront costs - we only get paid when you win. Call now.
D4: Dallas accident lawyers with millions in case results.
D5: Still have questions? Our attorneys are here to help 24/7.

Business Name: [Firm Name]

Call-to-Action: Choose "Get Quote" or "Contact Us"

Final URL: /remarketing-landing/ (special landing page) or main site
```

#### Static Image Ads (Create These Sizes)

```
Required Sizes:
├── 300x250 (Medium Rectangle) - Most common
├── 336x280 (Large Rectangle)
├── 728x90 (Leaderboard)
├── 300x600 (Half Page)
├── 320x100 (Large Mobile Banner)
└── 320x50 (Mobile Leaderboard)

Ad Design Elements:
├── Firm logo (prominent)
├── Headline: "Injured? We Can Help"
├── Subhead: "Free Consultation | No Fee Unless We Win"
├── Phone number
├── CTA Button: "Get Your Free Case Review"
├── Trust badge (ratings, awards)
└── Professional, clean design (not flashy)
```

### YouTube Remarketing Campaign

```
Campaign: DFW - YouTube Remarketing
├── Campaign Type: Video
├── Goal: Leads
├── Daily Budget: $50-75
├── Bid Strategy: Maximum CPV → Target CPV
├── Networks: YouTube videos, Display Network video partners
└── Frequency Cap: 3 impressions per day

Ad Group: YouTube Remarketing
├── Audience: All Website Visitors + High-Intent Visitors
├── Exclude: Converters
├── Placements: In-stream (skippable), In-feed
└── Ads: 2-3 video ads

Video Ad Requirements:
├── Length: 30-60 seconds (skippable after 5 seconds)
├── Format: MP4, 16:9 aspect ratio
├── Resolution: 1080p minimum
└── Content:
    ├── Hook in first 5 seconds (grab attention)
    ├── Address viewer directly ("Were you recently in an accident?")
    ├── Value proposition (free consultation, no fee unless win)
    ├── Social proof (results, testimonials)
    └── Clear CTA with phone number and URL
```

### RLSA (Remarketing Lists for Search Ads)

Add remarketing audiences to search campaigns in observation mode, then bid adjust:

```
Search Campaign Modifications:

Car Accident Campaign:
├── Add Audience: All Website Visitors
│   └── Bid Adjustment: +30%
├── Add Audience: Car Accident Page Visitors
│   └── Bid Adjustment: +50%
└── Add Audience: Contact Page Abandoners
    └── Bid Adjustment: +75%

Rationale: Users who visited before and return via search are highly qualified.
Pay more to win their click.
```

### Remarketing Exclusions

```
Exclude from ALL remarketing:
├── Converters (anyone who hit thank you page)
├── Careers page visitors (job seekers)
├── Current client portal users (if applicable)
└── Blog-only visitors with <30 seconds on site (low intent)
```

### Weeks 7-8 Remarketing Budget

| Campaign Type | Daily Budget | Bi-Weekly Budget |
|--------------|--------------|------------------|
| Display Remarketing | $125 | $1,750 |
| YouTube Remarketing | $60 | $840 |
| RLSA Bid Increases | ~$200 incremental | $2,800 |
| **Remarketing Total** | **~$385** | **$5,390** |

### Month 2 Total Budget Summary

| Campaign Category | Daily Budget | Month 2 Total |
|------------------|--------------|---------------|
| Brand Protection | $75 | $2,250 |
| Core Search (Car, PI, Wrongful Death) | $1,200 | $36,000 |
| Niche Search (Truck, Rideshare, Motorcycle) | $850 | $25,500 |
| LSA | $285 | $8,550 |
| Display Remarketing | $125 | $3,750 |
| YouTube Remarketing | $60 | $1,800 |
| **Month 2 Total** | **$2,595** | **$77,850** |

### Weeks 7-8 Deliverables Checklist

- [ ] All remarketing audiences created
- [ ] Display remarketing campaign launched
- [ ] Responsive display ads created
- [ ] Static image ads designed (all sizes)
- [ ] YouTube remarketing campaign launched
- [ ] Video ad(s) produced and uploaded
- [ ] RLSA audiences added to search campaigns
- [ ] Bid adjustments set for remarketing audiences
- [ ] Frequency caps configured
- [ ] Exclusion audiences applied
- [ ] Remarketing-specific landing page created (optional)

---

# MONTH 3: OPTIMIZATION & SCALING

---

## WEEKS 9-10: Competitor Conquest Testing

### Competitor Conquest Strategy

Bidding on competitor brand names is legal but requires careful execution to avoid trademark issues and wasted spend.

#### Pre-Launch Competitive Analysis

```
Research Competitors to Target:

Top DFW Personal Injury Firms (Example - Research Actual):
1. [Competitor A] - High visibility, TV advertising
2. [Competitor B] - Billboards, strong brand
3. [Competitor C] - Heavy PPC advertiser
4. [Competitor D] - LSA dominant
5. [Competitor E] - Strong reviews/reputation

Criteria for Targeting:
├── High brand search volume (use Keyword Planner)
├── Similar practice areas (personal injury)
├── Not a referral source or professional contact
├── Brand name is not trademarked for advertising
└── Cost-effective CPCs (test and evaluate)
```

### Competitor Conquest Campaign Structure

```
Campaign: DFW - Competitor Conquest (Test)
├── Daily Budget: $100-200 (test budget)
├── Bid Strategy: Manual CPC (maintain control)
├── Networks: Search only
├── Locations: DFW Metro
└── Status: Test for 2 weeks, evaluate performance

IMPORTANT LEGAL NOTES:
├── Do NOT use competitor names in ad copy
├── Do NOT use competitor trademarked terms in display URLs
├── Focus ads on your firm's strengths vs. "why not them"
└── Monitor for competitor complaints

Ad Groups (1 per competitor):

Ad Group 1: [Competitor A] Brand
├── Max CPC: $75 (start low, test)
├── Keywords:
│   ├── [[competitor a name]] - Exact
│   ├── [[competitor a name] lawyer] - Exact
│   ├── [[competitor a name] attorney] - Exact
│   ├── [[competitor a name] reviews] - Exact
│   └── "[competitor a name]" - Phrase
├── Negative Keywords:
│   ├── jobs
│   ├── careers
│   ├── salary
│   └── office
└── Landing Page: /why-choose-us/ (differentiator page)

Ad Group 2: [Competitor B] Brand
├── Max CPC: $75
├── Keywords: [same pattern as above]
└── Landing Page: /why-choose-us/

[Repeat for 3-5 top competitors]
```

### Conquest Ad Copy Guidelines

**What TO Do:**
- Focus on your firm's unique value propositions
- Highlight differentiators (experience, results, service)
- Include strong trust signals
- Use compelling CTAs

**What NOT To Do:**
- Never mention competitor by name
- Never make comparative claims ("better than...")
- Never use competitor trademarks
- Never disparage competition

**RSA for Conquest Campaigns:**
```
Headlines:
H1: Looking for the Best? Compare Us
H2: Award-Winning Dallas Injury Lawyers
H3: $XX Million+ in Verdicts & Settlements
H4: Free Consultation (214) XXX-XXXX
H5: No Fee Unless We Win Your Case
H6: See Why Clients Choose [Firm Name]
H7: Top-Rated on Google & Avvo
H8: Personalized Attention Guaranteed
H9: We Answer Our Phones 24/7
H10: Read Our 5-Star Reviews
H11: The Results Speak for Themselves
H12: Experience That Makes the Difference
H13: Not Just Any Lawyer - The Right Lawyer
H14: Proven Track Record in DFW
H15: Let Our Results Convince You

Descriptions:
D1: Researching injury lawyers? See why clients across DFW choose [Firm Name]. Free consultation - call to discuss your case today.
D2: When your case matters, experience counts. [X]+ years, $XX million recovered. Schedule your free consultation now.
D3: Not all injury lawyers are created equal. [Firm Name] offers personalized service and proven results. Compare us to the competition.
D4: Looking for the right Dallas injury attorney? Read our reviews, see our results, then decide. Free case evaluation.
```

### Competitor Campaign Monitoring

```
Daily Monitoring Checklist (Week 1):
├── Check impression share by competitor keyword
├── Review search terms for irrelevant queries
├── Monitor CPCs (stop if too high for ROI)
├── Track CTR (should be 2%+ to continue)
└── Note any competitor response (counter-bidding)

Performance Thresholds (Stop/Pause if):
├── CPC consistently >$150 with no conversions
├── CTR <1.5% after 1000 impressions
├── Zero conversions after $500 spend
└── Competitor legal complaint (rare but possible)

Performance Thresholds (Scale if):
├── CPA similar to or better than generic campaigns
├── CTR >3%
├── Conversion rate >3%
└── Positive ROI indicated
```

### Weeks 9-10 Optimization Tasks

#### Search Query Analysis

```
Review process (weekly during optimization):

1. Export Search Terms Report (last 7 days)
2. Sort by cost (highest first)
3. Identify:
   ├── Irrelevant terms → Add as negatives
   ├── High-performing terms not as keywords → Add as exact match
   ├── Themes of waste → Add phrase match negatives
   └── New opportunities → Create new ad groups

Common Negative Keywords to Add (ongoing):
├── Job-related: hiring, careers, salary, job
├── DIY: how to file, self represent, template
├── Other locations: houston, austin, san antonio
├── Other practice areas: workers comp, criminal, divorce
└── Competitor terms (for non-conquest campaigns)
```

#### Quality Score Optimization

```
For keywords with Quality Score <6:

1. Check Expected CTR component
   └── Fix: Write more relevant ad copy, use keyword in headline

2. Check Ad Relevance component
   └── Fix: Create tighter ad groups, fewer keywords per group

3. Check Landing Page Experience component
   └── Fix: Improve page speed, mobile experience, content relevance

Action Plan by QS:
├── QS 1-3: Pause keyword, not worth fixing
├── QS 4-5: Major optimization needed or pause
├── QS 6-7: Optimize landing page and ad copy
├── QS 8-10: Performing well, maintain
```

#### Bid Optimization

```
After 30+ conversions, transition campaigns to Target CPA:

Steps:
1. Calculate actual CPA from last 30 days
2. Set Target CPA at current CPA (don't reduce yet)
3. Monitor for 1 week - ensure volume maintained
4. If stable, reduce Target CPA by 10%
5. Repeat reduction every 2 weeks if hitting targets

Bid Adjustment Analysis:
├── Device: Adjust based on conversion rate by device
├── Time of Day: Increase bids during high-conversion hours
├── Location: Increase bids in high-value zip codes
├── Audience: Increase bids for engaged audiences
└── Demographics: Adjust if data shows clear patterns
```

#### Ad Copy Testing

```
Testing Framework:

Current: 3 RSAs per ad group

Add: 1 new RSA variation every 2 weeks focusing on:
├── Week 9: Test urgency messaging
├── Week 10: Test results/social proof messaging
├── Week 11: Test empathy/understanding messaging
├── Week 12: Test authority/expertise messaging

Measurement:
├── Primary: Conversion rate
├── Secondary: CTR
├── Tertiary: Quality Score impact

Winner Criteria:
├── Statistically significant improvement (95% confidence)
├── Minimum 100 clicks per ad
└── Minimum 10 conversions per ad (for CR comparison)
```

### Weeks 9-10 Budget Allocation

| Campaign | Daily Budget | Bi-Weekly Budget |
|----------|--------------|------------------|
| Brand Protection | $75 | $1,050 |
| Car Accident | $650 | $9,100 |
| Personal Injury | $425 | $5,950 |
| Wrongful Death | $200 | $2,800 |
| Truck Accident | $425 | $5,950 |
| Rideshare | $200 | $2,800 |
| Motorcycle | $275 | $3,850 |
| Competitor Conquest (Test) | $150 | $2,100 |
| LSA | $285 | $4,000 |
| Display Remarketing | $125 | $1,750 |
| YouTube Remarketing | $60 | $840 |
| **Total** | **$2,870** | **$40,190** |

---

## WEEKS 11-12: Final Optimization & Scaling

### Performance Audit

#### Comprehensive Account Audit Checklist

```
Campaign Level:
├── [ ] All campaigns using appropriate bid strategies
├── [ ] Budget utilization >90% (increase if capped)
├── [ ] Campaign-level negatives reviewed
├── [ ] Location targeting verified
├── [ ] Ad schedule optimized based on data
└── [ ] Networks set correctly (no accidental Display)

Ad Group Level:
├── [ ] No ad groups with <3 keywords
├── [ ] No ad groups with >20 keywords
├── [ ] Each ad group has 3+ RSAs
├── [ ] Ad group themes are tightly focused
├── [ ] Negative keywords at ad group level where needed
└── [ ] All ad groups have conversion data (pause if not)

Keyword Level:
├── [ ] Pause keywords with QS <5 and no conversions
├── [ ] Add high-performing search terms as keywords
├── [ ] Review match types - shift to exact where efficient
├── [ ] Check for keyword cannibalization
├── [ ] Ensure bid adjustments make sense
└── [ ] Remove duplicate keywords across ad groups

Ad Level:
├── [ ] Remove ads with CTR <2% (if sufficient data)
├── [ ] Ensure winning ad variations are active
├── [ ] Check for disapproved ads
├── [ ] Verify final URLs are correct
├── [ ] Test new ad variations
└── [ ] Check ad strength scores
```

### Scaling Strategy

#### Criteria for Budget Increases

```
Scale Campaign Budget if:
├── CPA at or below target for 14+ consecutive days
├── Budget limited (campaign hitting daily cap)
├── Impression share lost to budget >20%
├── Conversion volume desired is higher
└── Seasonality/demand increase expected

How to Scale:
├── Increase budget by 20-30% at a time
├── Wait 3-5 days for algorithm to adjust
├── Monitor for CPA increase
├── If CPA increases >20%, reduce budget slightly
└── Continue incremental increases if stable
```

#### Geographic Expansion Options

```
Option 1: Expand to Surrounding Texas Cities
├── Add: Waco, Tyler, Wichita Falls (within driving distance)
├── Create separate campaigns for distant cities
├── Lower budget allocation initially
└── Monitor case acquisition feasibility

Option 2: Expand to State-Level for High-Value Cases
├── Add: Texas statewide for truck accidents, wrongful death
├── Rationale: High-value cases justify travel
├── Separate campaigns with Texas-wide targeting
└── Adjust ad copy: "Serving All of Texas"

Option 3: Expand to Additional Practice Areas
├── Add: Premises liability campaign
├── Add: Medical malpractice (if firm handles)
├── Add: Product liability (if firm handles)
└── Use same structure as existing campaigns
```

### Advanced Optimization Techniques

#### Portfolio Bid Strategies

```
Create Portfolio Strategy for Similar Campaigns:

Portfolio Name: DFW - Injury Cases - Target CPA
├── Campaigns Included:
│   ├── Car Accident
│   ├── Personal Injury
│   ├── Motorcycle Accident
│   └── Rideshare Accident
├── Strategy: Target CPA
├── Target CPA: $300
└── Benefits: Shared learning, budget flexibility

Rationale: Algorithm can shift budget between campaigns
to hit overall CPA target, maximizing total conversions.
```

#### Audience Layer Optimization

```
Convert observation audiences to targeting (if data supports):

If In-Market: Legal Services audience shows 2x conversion rate:
├── Create new ad group targeting only that audience
├── Broader keywords acceptable (algorithm + audience = intent)
├── Potentially lower CPCs due to less competition
└── Test with small budget before scaling

Demographic Targeting:
If Age 35-54 shows significantly higher conversion rate:
├── Add bid adjustment +25% for that age range
├── Or create separate campaign targeting that demographic
└── Test removing very low-performing demographics
```

#### Value-Based Bidding Setup

```
If tracking actual case values:

1. Import offline conversions with values:
   ├── Car accident signed case: $2,500
   ├── Truck accident signed case: $10,000
   ├── Motorcycle accident signed case: $4,000
   ├── Wrongful death signed case: $15,000
   └── Slip and fall signed case: $1,500

2. Set up enhanced conversions for leads

3. Switch to "Maximize Conversion Value" or "Target ROAS"

4. Algorithm will prioritize higher-value case types

Benefits:
├── More truck accident and wrongful death conversions
├── Better allocation of budget to valuable cases
├── Higher overall case value from same spend
```

### Final KPI Dashboard

#### Key Metrics by Campaign (Targets at 90-Day Mark)

| Campaign | Monthly Budget | Target CPA | Target Conv/Month | Target Conv Rate |
|----------|---------------|------------|-------------------|------------------|
| Brand Protection | $2,250 | <$50 | 45+ | >10% |
| Car Accident | $20,000 | $250-300 | 70-80 | 6%+ |
| Personal Injury | $13,000 | $275-325 | 40-50 | 5%+ |
| Wrongful Death | $6,000 | $400-500 | 12-15 | 5%+ |
| Truck Accident | $13,000 | $400-500 | 25-35 | 5%+ |
| Rideshare | $6,000 | $300-350 | 18-20 | 5%+ |
| Motorcycle | $8,500 | $300-400 | 25-30 | 5%+ |
| Competitor Conquest | $4,500 | $350-450 | 10-15 | 4%+ |
| LSA | $8,500 | $150-200 | 45-55 | N/A |
| Display Remarketing | $3,750 | <$100 | 35-40 | 1%+ |
| YouTube Remarketing | $1,800 | <$150 | 12-15 | 0.5%+ |
| **TOTAL** | **$87,300** | **Blended $275** | **337-410** | **--** |

#### Lead Quality Metrics (Track via CRM)

```
Lead Source Tracking:

Track for each lead:
├── Source (Google Ads, LSA, etc.)
├── Campaign
├── Keyword (where possible)
├── Landing page
├── Call or form
├── Lead score (qualified/not qualified)
├── Consultation scheduled (Y/N)
├── Case signed (Y/N)
├── Case type
└── Estimated case value

Calculate:
├── Lead-to-consultation rate by campaign
├── Consultation-to-sign rate by campaign
├── Cost per signed case by campaign
├── Average case value by campaign
├── ROI by campaign
```

### Month 3 Budget Summary

| Week | Total Daily Budget | Weekly Spend |
|------|-------------------|--------------|
| Week 9 | $2,870 | $20,090 |
| Week 10 | $2,870 | $20,090 |
| Week 11 | $2,950 (scaled) | $20,650 |
| Week 12 | $2,950 | $20,650 |
| **Month 3 Total** | **--** | **$81,480** |

---

# APPENDIX

---

## Appendix A: Complete Keyword List by Campaign

### Car Accident Keywords (Full List)

```
High-Intent (Exact Match Priority):
├── [car accident lawyer dallas]
├── [car accident attorney dallas]
├── [auto accident lawyer dallas]
├── [dallas car accident lawyer]
├── [car wreck lawyer dallas]
├── [car accident lawyer near me]
├── [best car accident lawyer dallas]
├── [car accident lawyer fort worth]
├── [car crash attorney dallas]
├── [vehicle accident lawyer dallas]
├── [car accident injury lawyer]
├── [dallas auto accident attorney]
├── [car accident attorney near me]
├── [car wreck attorney dallas]
├── [auto injury lawyer dallas]

Secondary (Phrase Match):
├── "car accident lawyer dallas"
├── "auto accident attorney dallas"
├── "car wreck lawyer"
├── "car crash attorney"
├── "vehicle accident lawyer"
├── "car accident injury lawyer"

Location Variations:
├── [car accident lawyer plano]
├── [car accident lawyer arlington]
├── [car accident lawyer irving]
├── [car accident lawyer garland]
├── [car accident lawyer frisco]
├── [car accident lawyer mckinney]
├── [car accident lawyer denton]
├── [car accident lawyer mesquite]
├── [car accident lawyer richardson]
├── [car accident lawyer grand prairie]
├── [car accident lawyer carrollton]
├── [car accident lawyer lewisville]
├── [car accident lawyer allen]
├── [car accident lawyer flower mound]
├── [car accident attorney fort worth]
├── [auto accident lawyer arlington]
└── [car wreck attorney plano]
```

### Truck Accident Keywords (Full List)

```
High-Intent:
├── [truck accident lawyer dallas]
├── [truck accident attorney dallas]
├── [18 wheeler accident lawyer dallas]
├── [18 wheeler accident attorney]
├── [semi truck accident lawyer]
├── [big rig accident attorney]
├── [commercial truck accident lawyer]
├── [trucking accident attorney dallas]
├── [dallas truck accident lawyer]
├── [truck wreck lawyer dallas]
├── [18 wheeler crash lawyer]
├── [semi accident attorney]
├── [tractor trailer accident lawyer]
├── [trucking company accident attorney]
├── [delivery truck accident lawyer]
├── [amazon truck accident lawyer]
├── [fedex truck accident attorney]
├── [ups truck accident lawyer]
├── [truck accident lawyer near me]
├── [truck accident attorney fort worth]

Phrase Match:
├── "truck accident lawyer"
├── "18 wheeler accident attorney"
├── "semi truck accident lawyer"
├── "commercial truck crash attorney"
├── "trucking accident lawyer dallas"
```

### Personal Injury Keywords (Full List)

```
High-Intent:
├── [personal injury lawyer dallas]
├── [personal injury attorney dallas]
├── [dallas personal injury lawyer]
├── [injury lawyer dallas]
├── [injury attorney dallas]
├── [personal injury lawyer near me]
├── [accident lawyer dallas]
├── [accident attorney dallas]
├── [personal injury law firm dallas]
├── [best personal injury lawyer dallas]
├── [personal injury attorney fort worth]
├── [injury lawyer fort worth]
├── [dallas accident attorney]
├── [personal injury attorney near me]
├── [accident injury lawyer dallas]
```

### Wrongful Death Keywords (Full List)

```
High-Intent:
├── [wrongful death lawyer dallas]
├── [wrongful death attorney dallas]
├── [wrongful death law firm dallas]
├── [dallas wrongful death lawyer]
├── [fatal accident lawyer dallas]
├── [wrongful death attorney texas]
├── [wrongful death lawyer near me]
├── [fatal car accident attorney]
├── [death by negligence lawyer]
├── [wrongful death lawsuit attorney]
├── [wrongful death claim lawyer dallas]
├── [family wrongful death attorney]
├── [wrongful death lawyer fort worth]
├── [fatal crash attorney dallas]
├── [wrongful death suit lawyer]
```

---

## Appendix B: Negative Keyword Master List

```
CATEGORY: Employment/Workers Comp
workers compensation
workers comp
work injury
job injury
workplace accident
occupational injury
work related injury
on the job injury
employer negligence
osha
warehouse injury
construction accident
factory injury
office injury
repetitive stress
carpal tunnel

CATEGORY: Other Legal Practice Areas
criminal defense
criminal lawyer
dui attorney
dwi lawyer
divorce attorney
family law
child custody
bankruptcy lawyer
immigration attorney
estate planning
real estate lawyer
business attorney
contract lawyer
intellectual property
employment law
labor attorney
tax attorney

CATEGORY: DIY/Informational
how to file
how to sue
can i sue
what to do after
template
form
sample
free legal advice
pro bono
legal aid
self represent
without lawyer
no lawyer
law school
paralegal
legal assistant

CATEGORY: Geographic (Outside DFW)
houston lawyer
austin attorney
san antonio injury
el paso accident
corpus christi
lubbock
amarillo
midland
odessa
brownsville
mcallen
beaumont
waco lawyer (unless targeting)
tyler attorney (unless targeting)
california
florida
new york

CATEGORY: Jobs/Careers
attorney jobs
lawyer salary
law firm hiring
legal jobs
paralegal jobs
legal assistant jobs
careers
employment
job openings
work for
hiring

CATEGORY: Unqualified/Low Value
cheap lawyer
free lawyer
discount attorney
low cost
pro bono
no money
can't afford
payment plan
legal aid society
public defender

CATEGORY: Specific Exclusions
mesothelioma (unless handling)
asbestos (unless handling)
class action
mass tort (unless handling)
social security disability
veteran benefits
medical malpractice (unless handling)
nursing home abuse (unless handling)
birth injury (unless handling)
dog bite (unless handling)
defamation
slander
libel
```

---

## Appendix C: Landing Page Best Practices

### Essential Elements

```
HEADER SECTION:
├── Firm logo (top left)
├── Phone number (top right, clickable)
├── Simple navigation (or no navigation for PPC)
└── Trust badges (awards, ratings)

HERO SECTION:
├── Headline with primary keyword
│   Example: "Dallas Car Accident Lawyers"
├── Subheadline with value proposition
│   Example: "Fighting for Maximum Compensation Since [Year]"
├── Hero image (professional, relatable)
├── Primary CTA button ("Free Case Review")
└── Phone number (clickable)

FORM SECTION (Above Fold):
├── Headline: "Get Your Free Consultation"
├── Fields:
│   ├── Name (required)
│   ├── Phone (required)
│   ├── Email (required)
│   └── Tell us about your accident (optional)
├── Submit button: "Get My Free Case Review"
├── Privacy statement link
└── "No fee unless we win" statement

SOCIAL PROOF SECTION:
├── Client testimonials (3-5)
├── Case results (with disclaimers)
├── Awards and recognition
├── Review platform ratings (Google, Avvo)
└── Media mentions (if applicable)

WHY CHOOSE US SECTION:
├── 3-5 differentiators with icons
│   ├── Free consultations
│   ├── No fee unless we win
│   ├── [X] years experience
│   ├── $[X] million recovered
│   └── 24/7 availability
└── Brief explanation of each

PRACTICE AREA DETAILS:
├── Information about case type
├── What to do after accident
├── How the legal process works
├── FAQ section
└── Related practice areas links

ABOUT THE FIRM:
├── Brief firm history
├── Attorney photos and bios
├── Firm values/approach
└── Credentials and memberships

FOOTER:
├── Contact information
├── Office addresses
├── Practice areas links
├── Legal disclaimers
├── Privacy policy link
└── Secondary phone number CTA
```

### Mobile Optimization Requirements

```
├── Page load time <3 seconds
├── Click-to-call buttons (sticky at bottom)
├── Form fields sized for touch (min 44px height)
├── Font size minimum 16px (prevents zoom)
├── Buttons minimum 44px x 44px
├── No horizontal scrolling
├── Compressed images
├── Simplified navigation
├── Form visible without scrolling
└── Trust badges visible early
```

---

## Appendix D: Reporting Templates

### Weekly Report Template

```
WEEK OF: [Date Range]
ACCOUNT: [Firm Name] - Google Ads

EXECUTIVE SUMMARY:
├── Total Spend: $X,XXX
├── Total Leads: XX
├── Cost Per Lead: $XXX
├── Change vs. Prior Week: +/-X%
└── Key Highlights: [2-3 bullet points]

CAMPAIGN PERFORMANCE:
| Campaign | Spend | Clicks | Conv | CPA | CTR | Conv Rate |
|----------|-------|--------|------|-----|-----|-----------|
| Brand    | $XXX  | XXX    | XX   | $XX | XX% | XX%       |
| Car Acc  | $X,XXX| XXX    | XX   | $XXX| X%  | X%        |
| [etc.]   |       |        |      |     |     |           |

TOP PERFORMING KEYWORDS:
1. [keyword] - X conversions, $XX CPA
2. [keyword] - X conversions, $XX CPA
3. [keyword] - X conversions, $XX CPA

AREAS OF CONCERN:
├── [Issue 1]
├── [Issue 2]
└── [Proposed solutions]

OPTIMIZATIONS MADE:
├── [Action 1]
├── [Action 2]
└── [Action 3]

NEXT WEEK PRIORITIES:
├── [Priority 1]
├── [Priority 2]
└── [Priority 3]
```

### Monthly Report Template

```
MONTH: [Month Year]
ACCOUNT: [Firm Name] - Google Ads

EXECUTIVE SUMMARY:
├── Total Spend: $XX,XXX
├── Total Leads: XXX
├── Cost Per Lead: $XXX
├── Signed Cases: XX (from CRM)
├── Cost Per Case: $X,XXX
└── Estimated Case Value: $X,XXX,XXX

MONTH-OVER-MONTH TRENDS:
| Metric     | Last Month | This Month | Change |
|------------|------------|------------|--------|
| Spend      | $XX,XXX    | $XX,XXX    | +X%    |
| Leads      | XXX        | XXX        | +X%    |
| CPL        | $XXX       | $XXX       | -X%    |
| Signed     | XX         | XX         | +X%    |

CHANNEL BREAKDOWN:
| Channel    | Spend   | Leads | CPL   | Signed | CPC  |
|------------|---------|-------|-------|--------|------|
| Search     | $XX,XXX | XXX   | $XXX  | XX     | $XXX |
| LSA        | $X,XXX  | XX    | $XXX  | XX     | N/A  |
| Display RM | $X,XXX  | XX    | $XX   | XX     | $X   |
| YouTube    | $X,XXX  | XX    | $XXX  | X      | $X   |

KEYWORD PERFORMANCE (Top 10):
[Table with keyword, impressions, clicks, cost, conv, CPA]

QUALITY SCORE DISTRIBUTION:
├── QS 8-10: XX% of keywords
├── QS 6-7: XX% of keywords
└── QS 1-5: XX% of keywords

OPTIMIZATIONS COMPLETED:
├── [List all optimizations made]

RECOMMENDATIONS FOR NEXT MONTH:
├── [Recommendation 1 with rationale]
├── [Recommendation 2 with rationale]
└── [Recommendation 3 with rationale]

BUDGET RECOMMENDATION:
├── Current: $XX,XXX/month
├── Recommended: $XX,XXX/month
└── Rationale: [Explanation]
```

---

## Appendix E: Emergency Response Protocol

### Immediate Actions for Common Issues

```
ISSUE: Ads Not Showing
├── Check payment method (billing issues)
├── Check campaign status (not paused)
├── Check ad approval status
├── Review quality score (too low)
├── Check budget (depleted)
└── Search for own ads (use Ad Preview tool, not regular search)

ISSUE: Sudden CPA Spike
├── Check search terms for irrelevant traffic
├── Review auction insights (new competitor?)
├── Check for landing page issues (404, slow load)
├── Review recent changes (revert if necessary)
├── Check conversion tracking (still working?)
└── Segment by device, location, time for patterns

ISSUE: Lead Volume Drop
├── Check impression share (lost to budget/rank?)
├── Review search volume trends (seasonal?)
├── Check for new competitors
├── Review ad disapprovals
├── Check Quality Scores
├── Verify conversion tracking working
└── Review landing page functionality

ISSUE: High Spend, No Conversions
├── Immediately reduce budgets
├── Verify conversion tracking
├── Review search terms for relevance
├── Check landing page (loading, form working)
├── Review ad copy for misleading content
└── Consider pausing problem campaigns

ISSUE: Competitor Legal Complaint (Conquest)
├── Pause competitor campaign immediately
├── Remove any potentially infringing content
├── Document all ads and keywords used
├── Consult with firm's legal team
├── Evaluate whether to resume (modified) or abandon
└── Focus budget on non-conquest campaigns
```

---

## Appendix F: Implementation Timeline Summary

```
MONTH 1 SUMMARY:
├── Week 1: Foundation
│   ├── Account setup
│   ├── Conversion tracking
│   ├── Call tracking
│   └── Landing page optimization
├── Week 2: Brand Protection Launch
│   ├── Brand campaign live
│   └── All extensions configured
├── Week 3: Core Campaign Launch
│   ├── Car Accident campaign
│   ├── Personal Injury campaign
│   └── Wrongful Death campaign
└── Week 4: LSA Setup
    ├── Application submitted
    ├── Verification in progress
    └── Profile optimized

MONTH 2 SUMMARY:
├── Weeks 5-6: Niche Expansion
│   ├── Truck Accident campaign
│   ├── Rideshare campaign
│   └── Motorcycle campaign
└── Weeks 7-8: Remarketing
    ├── Audience creation
    ├── Display remarketing
    ├── YouTube remarketing
    └── RLSA implementation

MONTH 3 SUMMARY:
├── Weeks 9-10: Conquest Testing
│   ├── Competitor campaign launch
│   ├── Search query optimization
│   └── Quality Score improvements
└── Weeks 11-12: Optimization & Scale
    ├── Performance audit
    ├── Bid strategy optimization
    ├── Budget scaling
    └── Advanced techniques

POST-90 DAYS:
├── Ongoing optimization
├── New campaign testing
├── Geographic expansion (if applicable)
├── Value-based bidding implementation
└── Continuous improvement
```

---

## Appendix G: Vendor & Tool Recommendations

```
CALL TRACKING:
├── Primary: CallRail ($45-145/month)
├── Alternative: CallTrackingMetrics
└── Alternative: Invoca (enterprise)

LANDING PAGES:
├── Unbounce ($90-225/month)
├── Instapage ($199-499/month)
└── Leadpages ($37-79/month)

CRM FOR LEAD TRACKING:
├── Clio Grow (legal-specific)
├── Lawmatics (legal-specific)
├── Salesforce (enterprise)
└── HubSpot (general, free tier)

REPORTING:
├── Google Looker Studio (free)
├── AgencyAnalytics ($12-18/client)
├── Databox ($72-231/month)
└── Supermetrics (for data connections)

COMPETITOR RESEARCH:
├── SpyFu ($39-299/month)
├── SEMrush ($119-449/month)
├── Ahrefs ($99-999/month)
└── iSpionage ($59-299/month)

LANDING PAGE TESTING:
├── Google Optimize (free, sunsetting)
├── VWO ($49-1,999/month)
├── Optimizely (enterprise pricing)
└── Unbounce A/B testing (included)
```

---

*Document Version: 1.0*
*Created: [Date]*
*Last Updated: [Date]*
*Author: [Agency/Consultant Name]*

---

**DISCLAIMER:** This playbook contains strategic recommendations based on industry best practices for personal injury law firm PPC advertising. Actual results will vary based on market conditions, competition, budget, landing page quality, and intake processes. All budget figures are estimates and should be adjusted based on actual performance data. Legal advertising must comply with Texas State Bar advertising rules and all applicable regulations.
