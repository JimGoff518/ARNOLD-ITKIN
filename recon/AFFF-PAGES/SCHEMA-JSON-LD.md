# JSON-LD Schema Blocks — AFFF Pages

**Use:** Drop each block into the corresponding page's HTML `<head>` section as a `<script type="application/ld+json">` tag. WordPress + Yoast usually has a "Schema" tab in the page editor where these can be pasted; alternatively, the theme dev can inject via PHP hook.

**Two schema types per page:**
1. **FAQPage** — captures the FAQ block at the bottom of each page (eligible for Google AI Overview citation + featured snippets)
2. **LegalService** — captures the practice page as a legal service offering with location targeting

---

## PAGE 1 — Dallas AFFF Lawyer

### FAQPage Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "I served as a Dallas firefighter and have been diagnosed with kidney cancer. Do I have a case?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "If your kidney cancer diagnosis is medically documented and your service history shows AFFF exposure, you likely qualify to file a claim in the federal AFFF MDL 2873. Kidney cancer is the most common qualifying condition. Call 972-928-0085 for a free case review."
      }
    },
    {
      "@type": "Question",
      "name": "How much is my AFFF firefighter cancer lawsuit worth?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Legal analysts currently project settlement values between $20,000 and $600,000 per qualifying claim, depending on cancer type, exposure duration, age at diagnosis, and the specific manufacturer defendants involved. No definitive settlements have been finalized yet — actual values will be shaped by the upcoming bellwether trials."
      }
    },
    {
      "@type": "Question",
      "name": "I'm a DFW Airport firefighter. Is my AFFF exposure different from Dallas Fire-Rescue exposure?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "ARFF crews at DFW Airport had some of the most concentrated and prolonged AFFF exposure of any firefighter population, because aviation fires require AFFF as the primary suppression agent and ARFF crews train with foam regularly. Your exposure profile is, if anything, stronger documentation for a claim than structural firefighting service."
      }
    },
    {
      "@type": "Question",
      "name": "What is the statute of limitations for AFFF firefighter cancer claims in Texas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Texas statute of limitations on personal injury claims is generally two years from the date of diagnosis OR from the date the injured person knew or should have known the cancer was linked to AFFF. Because PFAS-cancer linkage was not widely understood until recently, many older diagnoses still qualify under the discovery rule. Do not assume your claim is time-barred without speaking with an attorney."
      }
    },
    {
      "@type": "Question",
      "name": "Can family members file if the firefighter has already died from cancer?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Wrongful death and survival action claims may be filed by the deceased firefighter's spouse, children, or estate representative. The same six qualifying medical conditions apply."
      }
    },
    {
      "@type": "Question",
      "name": "Do I have to sue Dallas Fire-Rescue or DFW Airport?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. The defendants in AFFF litigation are the chemical manufacturers — 3M, DuPont, Chemours, Tyco, and others — not your employer. Your service to Dallas or DFW Airport is not on trial."
      }
    },
    {
      "@type": "Question",
      "name": "What documentation do I need to file an AFFF claim?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Service records, training records showing AFFF use, medical records documenting your qualifying diagnosis, and any workplace health monitoring records. If documentation is incomplete, your attorney has tools (subpoenas, FOIA, military records requests) to recover what you cannot obtain on your own."
      }
    },
    {
      "@type": "Question",
      "name": "What does it cost to hire Goff Law for an AFFF claim?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Nothing up front. AFFF cases are handled on contingency — no fee unless your claim recovers compensation. Initial consultations are free, confidential, and carry no obligation."
      }
    },
    {
      "@type": "Question",
      "name": "How long will my AFFF case take to resolve?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "AFFF claims in the federal MDL are likely to resolve over the next 18-36 months as bellwether trials proceed and global settlement structures emerge. Some cases may resolve faster through individual settlements; others may take longer if they go to trial."
      }
    },
    {
      "@type": "Question",
      "name": "I'm a Dallas firefighter but I'm worried filing a claim will affect my pension or city benefits.",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Filing a personal injury claim against private chemical manufacturers does not affect your pension, workers' compensation, or any benefits provided by Dallas Fire-Rescue or the City of Dallas. The claim is entirely separate from your employment."
      }
    },
    {
      "@type": "Question",
      "name": "I was a contractor or volunteer firefighter, not a paid municipal firefighter. Can I still file?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, as long as you have documented AFFF exposure and a qualifying medical diagnosis. Volunteer firefighters, mutual aid responders, military firefighters, and fire equipment technicians all qualify if exposure can be documented."
      }
    }
  ]
}
</script>
```

### LegalService Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LegalService",
  "name": "Goff Law - Dallas AFFF Lawyer",
  "description": "Goff Law represents Dallas firefighters and DFW Airport ARFF personnel diagnosed with cancer after AFFF firefighting foam exposure in the federal AFFF MDL 2873.",
  "url": "https://gofflawdfw.com/dallas-afff-lawyer/",
  "telephone": "+1-972-928-0085",
  "priceRange": "Contingency basis — no fee unless we recover compensation",
  "areaServed": {
    "@type": "City",
    "name": "Dallas",
    "containedInPlace": {
      "@type": "State",
      "name": "Texas"
    }
  },
  "provider": {
    "@type": "Attorney",
    "name": "Jim Goff",
    "url": "https://gofflawdfw.com/"
  },
  "serviceType": "AFFF Firefighter Cancer Lawsuit Representation"
}
</script>
```

---

## PAGE 2 — Texas AFFF Firefighter Lawyer

### FAQPage Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "I served as a military firefighter at Lackland AFB in the 1980s. Can I still file an AFFF claim?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Lackland AFB hosted the Air Force's primary firefighter training school, meaning service members who trained there typically have well-documented AFFF exposure history. The statute of limitations runs from when you knew or should have known the cancer was linked to AFFF, not from your service date."
      }
    },
    {
      "@type": "Question",
      "name": "I'm a Texas veteran receiving VA disability for kidney cancer. Can I still file an AFFF lawsuit?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. VA disability compensation and an AFFF MDL claim are entirely separate. VA benefits compensate for your service connection; the MDL claim compensates for the manufacturers' concealment of known health risks. Many veterans pursue both simultaneously."
      }
    },
    {
      "@type": "Question",
      "name": "I'm a Texas firefighter who trained at Goodfellow AFB. Does that count even though I went to civilian work afterward?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Goodfellow AFB is one of the highest-exposure firefighter training installations in the DoD, because firefighters from the Air Force, Army, Navy, and Marine Corps all trained there for decades. If you trained at Goodfellow and have a qualifying diagnosis, you have strong AFFF exposure documentation."
      }
    },
    {
      "@type": "Question",
      "name": "What is the statute of limitations for AFFF firefighter cancer claims in Texas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Generally two years from the date of diagnosis OR the date you knew or should have known the cancer was linked to AFFF. The discovery rule is fact-specific. Do not assume your claim is time-barred without speaking with an attorney."
      }
    },
    {
      "@type": "Question",
      "name": "I served on a Naval Air Station in Texas. Is my exposure different from a structural firefighter?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Naval ARFF crews had some of the most concentrated AFFF exposure of any military firefighter population because all aviation fuel fire training requires foam deployment. Your exposure profile is, if anything, stronger documentation for a claim."
      }
    },
    {
      "@type": "Question",
      "name": "How much is a Texas military firefighter AFFF lawsuit worth?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Projected settlement values range from $20,000 to $600,000 per qualifying claim. Military firefighter claims with strong DoD documentation and high cumulative exposure tend toward the higher end of the projected range."
      }
    },
    {
      "@type": "Question",
      "name": "Do I have to sue the U.S. military or the Department of Defense?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. The defendants in AFFF litigation are the chemical manufacturers — 3M, DuPont, Chemours, Tyco, and others — not the military or any government entity. Your service is not on trial."
      }
    },
    {
      "@type": "Question",
      "name": "Will filing an AFFF claim affect my VA benefits or military pension?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. Filing a personal injury claim against private chemical manufacturers has no effect on VA disability compensation, VA healthcare, military pensions, or any other federal benefits."
      }
    },
    {
      "@type": "Question",
      "name": "I have records showing AFFF use but my medical records don't mention PFAS. Can I still file?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Most firefighter medical records pre-2018 don't mention PFAS because the connection wasn't widely understood. Your attorney will coordinate the medical nexus opinion linking your diagnosis to your exposure history; this is a normal part of the claim-building process."
      }
    },
    {
      "@type": "Question",
      "name": "I was a civilian contractor providing fire support at a Texas military installation. Do I qualify?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, if you have documented AFFF exposure and a qualifying medical diagnosis. Contractors, GS civilian firefighters, mutual aid responders, and volunteer firefighters all qualify if exposure can be documented."
      }
    }
  ]
}
</script>
```

### LegalService Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LegalService",
  "name": "Goff Law - Texas AFFF Firefighter Lawyer",
  "description": "Goff Law represents Texas military and civilian firefighters diagnosed with cancer after AFFF firefighting foam exposure. Statewide representation for Lackland AFB, Fort Hood, Sheppard AFB, Naval Air Stations, and municipal firefighter cancer claims.",
  "url": "https://gofflawdfw.com/texas-afff-firefighter-lawyer/",
  "telephone": "+1-972-928-0085",
  "priceRange": "Contingency basis — no fee unless we recover compensation",
  "areaServed": {
    "@type": "State",
    "name": "Texas"
  },
  "provider": {
    "@type": "Attorney",
    "name": "Jim Goff",
    "url": "https://gofflawdfw.com/"
  },
  "serviceType": "AFFF Firefighter Cancer Lawsuit Representation"
}
</script>
```

---

## PAGE 3 — North Texas AFFF Lawyer

### FAQPage Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "I served at Plano Fire-Rescue and have been diagnosed with thyroid cancer. Do I qualify?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Thyroid cancer is one of the six recognized qualifying conditions in the federal AFFF MDL. If your service history shows AFFF exposure — which is standard for any career Plano firefighter — you likely qualify. Call 972-928-0085 for a free case review."
      }
    },
    {
      "@type": "Question",
      "name": "I trained at TEEX Fire School in College Station but worked my whole career in Frisco. Does my TEEX training count toward exposure documentation?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. TEEX has documented AFFF use for decades of certification and continuing education training. Your TEEX training rosters plus your Frisco departmental service rosters together provide strong exposure documentation."
      }
    },
    {
      "@type": "Question",
      "name": "I'm an ARFF crew member at McKinney National Airport. Is my exposure different from a structural firefighter?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "ARFF crews at regional airports had concentrated and prolonged AFFF exposure because aviation fuel fire training requires foam deployment. Your exposure profile is, if anything, stronger documentation for a claim than structural firefighting service."
      }
    },
    {
      "@type": "Question",
      "name": "I was a volunteer firefighter in a North Texas suburb department, not a career firefighter. Do I qualify?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, if you have documented AFFF exposure and a qualifying medical diagnosis. Volunteer firefighters, mutual aid responders, and reserve crews all qualify if exposure can be documented."
      }
    },
    {
      "@type": "Question",
      "name": "What is the statute of limitations for AFFF firefighter cancer claims in Texas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Generally two years from the date of diagnosis OR the date you knew or should have known the cancer was linked to AFFF (the discovery rule). The discovery rule is fact-specific; the safer path is to act promptly."
      }
    },
    {
      "@type": "Question",
      "name": "How much is a North Texas suburb firefighter AFFF lawsuit worth?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Projected settlement values range from $20,000 to $600,000 per qualifying claim. Range depends on cancer type, exposure duration, age at diagnosis, and specific manufacturer defendants involved."
      }
    },
    {
      "@type": "Question",
      "name": "Do I have to sue Plano (or my city) to file an AFFF claim?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. The defendants are the chemical manufacturers — 3M, DuPont, Chemours, Tyco, and others — not your fire department or municipality. Your service to your city is not on trial."
      }
    },
    {
      "@type": "Question",
      "name": "Will filing affect my pension, workers' comp, or city health insurance?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. Filing a personal injury claim against private chemical manufacturers has no effect on municipal pensions, workers' compensation, or any employment-related benefits."
      }
    },
    {
      "@type": "Question",
      "name": "I served in multiple North Texas suburbs over my career. How do you document that?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "We work with the personnel records from each department, plus your DD-214 (if you also served in the military), training rosters from regional academies, and mutual aid response logs. Multi-department service history often strengthens claims by demonstrating cumulative exposure."
      }
    }
  ]
}
</script>
```

### LegalService Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LegalService",
  "name": "Goff Law - North Texas AFFF Lawyer",
  "description": "Goff Law represents firefighters from Plano, Frisco, Allen, McKinney, Arlington, Garland, Irving, Mesquite, and surrounding North Texas suburb departments in federal AFFF firefighter cancer claims.",
  "url": "https://gofflawdfw.com/north-texas-afff-lawyer/",
  "telephone": "+1-972-928-0085",
  "priceRange": "Contingency basis — no fee unless we recover compensation",
  "areaServed": [
    {"@type": "City", "name": "Plano", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Frisco", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Allen", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "McKinney", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Arlington", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Garland", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Irving", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Mesquite", "containedInPlace": {"@type": "State", "name": "Texas"}}
  ],
  "provider": {
    "@type": "Attorney",
    "name": "Jim Goff",
    "url": "https://gofflawdfw.com/"
  },
  "serviceType": "AFFF Firefighter Cancer Lawsuit Representation"
}
</script>
```

---

## PAGE 4 — Houston AFFF Firefighter Lawyer

### FAQPage Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "I'm a Houston Fire Department firefighter diagnosed with kidney cancer. Do I have a case?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Houston Fire Department deployed AFFF for decades. Kidney cancer is the most common qualifying condition in the federal AFFF MDL. If your service history shows AFFF exposure — standard for any career HFD firefighter — you likely qualify. Call 972-928-0085 for a free case review."
      }
    },
    {
      "@type": "Question",
      "name": "I served as a refinery emergency response team member at Pasadena, Deer Park, Baytown, or Texas City. Am I covered?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Refinery emergency response personnel had some of the most intensive AFFF exposure of any firefighter population in the United States. Your training and incident response records typically provide strong documented exposure history."
      }
    },
    {
      "@type": "Question",
      "name": "I'm an ARFF crew member at IAH or Hobby. Is my exposure different from a structural firefighter?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "ARFF crews at major airports trained with and deployed AFFF for aviation fuel fires more frequently than structural firefighters did. Your exposure profile is, if anything, stronger documentation for a claim than structural firefighting service."
      }
    },
    {
      "@type": "Question",
      "name": "I served in NASA JSC fire service. Do federal civilian firefighters qualify?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Federal civilian firefighters, contractors, and military firefighters all qualify if exposure can be documented and a qualifying medical diagnosis exists. NASA records typically provide good documentation."
      }
    },
    {
      "@type": "Question",
      "name": "How much is a Houston refinery firefighter AFFF lawsuit worth?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Projected settlement values range from $20,000 to $600,000 per qualifying claim. Houston refinery and ARFF claims with strong exposure documentation often sit toward the higher end of the range because cumulative exposure is unusually well-documented."
      }
    },
    {
      "@type": "Question",
      "name": "Do I have to sue Houston Fire Department or my refinery employer to file an AFFF claim?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. The defendants in AFFF litigation are the chemical manufacturers — 3M, DuPont, Chemours, Tyco, and others — not your employer. Your service is not on trial."
      }
    },
    {
      "@type": "Question",
      "name": "Will filing affect my municipal pension or refinery retirement benefits?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. Filing a personal injury claim against private chemical manufacturers has no effect on pensions, workers' compensation, or any employment-related benefits."
      }
    },
    {
      "@type": "Question",
      "name": "Goff Law is in Dallas. Can you represent Houston firefighters?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Texas attorneys can represent clients across the state, and AFFF claims are filed in federal court in South Carolina — no party physically appears in Texas for the MDL litigation. We routinely represent Texas clients statewide."
      }
    },
    {
      "@type": "Question",
      "name": "I worked as a contractor at multiple Houston petrochemical facilities. Does that complicate the claim?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Multi-facility service history often strengthens claims by documenting broader cumulative exposure. We work with employment records from each facility plus your tax records and any union records to document complete exposure history."
      }
    },
    {
      "@type": "Question",
      "name": "What does it cost to hire Goff Law for an AFFF claim?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Nothing up front. AFFF cases are handled on contingency — no fee unless your claim recovers compensation. Initial consultations are free, confidential, and carry no obligation."
      }
    }
  ]
}
</script>
```

### LegalService Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LegalService",
  "name": "Goff Law - Houston AFFF Firefighter Lawyer",
  "description": "Goff Law represents Houston Fire Department, ARFF crews at IAH and Hobby, NASA JSC fire service, and refinery emergency response personnel from Pasadena, Deer Park, Texas City, and Baytown in federal AFFF firefighter cancer claims.",
  "url": "https://gofflawdfw.com/houston-afff-firefighter-lawyer/",
  "telephone": "+1-972-928-0085",
  "priceRange": "Contingency basis — no fee unless we recover compensation",
  "areaServed": [
    {"@type": "City", "name": "Houston", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Pasadena", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Deer Park", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Texas City", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Baytown", "containedInPlace": {"@type": "State", "name": "Texas"}}
  ],
  "provider": {
    "@type": "Attorney",
    "name": "Jim Goff",
    "url": "https://gofflawdfw.com/"
  },
  "serviceType": "AFFF Firefighter Cancer Lawsuit Representation"
}
</script>
```
