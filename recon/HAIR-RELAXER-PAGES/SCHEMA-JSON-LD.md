# JSON-LD Schema Blocks — Hair Relaxer Pages

**Use:** Drop each block into the corresponding page's HTML `<head>` as a `<script type="application/ld+json">` tag.

**Coverage:**
- 4 new pages — FAQPage + LegalService schema each
- 1 existing Dallas page (`/dallas/hair-relaxers/`) — FAQPage schema add (existing content has FAQ-style questions but likely no schema markup)

---

## PAGE 1 — Houston Hair Relaxer Lawyer

### FAQPage Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "I'm a Houston woman who used Dark & Lovely from age 12 to age 40. I was just diagnosed with uterine cancer. Do I have a case?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, most likely. Uterine cancer is the most strongly established qualifying condition in MDL 3060, Dark & Lovely is a primary defendant product, and 28 years of regular use significantly exceeds the four-times-per-year threshold the NIH Sister Study identified. Call 972-928-0085 for a free case review."
      }
    },
    {
      "@type": "Question",
      "name": "I used Just for Me as a child and switched to other brands as an adult. Do I qualify if I have ovarian cancer?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Mixed brand use is common and acceptable. Strength of Nature (manufacturer of Just for Me) is a primary MDL 3060 defendant, and ovarian cancer is a qualifying condition. Your childhood plus adult use history together support a strong claim."
      }
    },
    {
      "@type": "Question",
      "name": "How much is a Houston hair relaxer cancer lawsuit worth?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Projected settlement values range from $50,000 to $1,500,000+ per qualifying claim, depending on cancer type, stage at diagnosis, age, duration of hair relaxer use, and documentation strength. No definitive settlements have been finalized as of April 2026."
      }
    },
    {
      "@type": "Question",
      "name": "I never saved my hair relaxer packaging. Can I still file?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Most claimants don't have packaging — these are everyday products that get discarded after use. Your attorney works with product use history reconstruction (memory, family member statements, salon records, retail pattern documentation) to build the claim."
      }
    },
    {
      "@type": "Question",
      "name": "My mother died of uterine cancer in 2023. Can I file on her behalf?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Wrongful death and survival action claims may be filed by the deceased's spouse, children, or estate representative. The same qualifying conditions and product use history requirements apply."
      }
    },
    {
      "@type": "Question",
      "name": "What is the statute of limitations for hair relaxer cancer claims in Texas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Generally two years from the date of diagnosis OR from the date you knew or should have known the cancer was linked to hair relaxers (the discovery rule). Because the link was not widely understood until October 2022, many older diagnoses still qualify under the discovery rule."
      }
    },
    {
      "@type": "Question",
      "name": "Do I have to sue Walgreens, Sally Beauty, or my hair salon?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. The defendants in MDL 3060 are the chemical manufacturers — L'Oréal, SoftSheen-Carson, Strength of Nature, Namaste, Dabur, and others. Retailers and salons who sold or applied these products are not defendants."
      }
    },
    {
      "@type": "Question",
      "name": "Do I have to travel to Chicago or Illinois?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. The MDL is centralized procedurally, but individual claimants do not appear in court unless selected for bellwether trial. Depositions and most proceedings can be conducted remotely or in Houston."
      }
    },
    {
      "@type": "Question",
      "name": "What does it cost to hire Goff Law for a Houston hair relaxer claim?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Nothing up front. Hair relaxer cases are handled on contingency — no fee unless your claim recovers compensation. Initial consultations are free, confidential, and carry no obligation."
      }
    },
    {
      "@type": "Question",
      "name": "I was diagnosed with uterine fibroids but not cancer. Do I qualify?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Uterine fibroids are a secondary claim type in MDL 3060 — qualifying evidence is emerging but the litigation primarily centers on cancer claims. Speak with an attorney about your specific circumstances."
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
  "name": "Goff Law - Houston Hair Relaxer Lawyer",
  "description": "Goff Law represents Houston women diagnosed with uterine, endometrial, or ovarian cancer after using chemical hair relaxers (Dark & Lovely, Optimum, Just for Me, Motions) in federal MDL 3060.",
  "url": "https://gofflawdfw.com/houston-hair-relaxer-lawyer/",
  "telephone": "+1-972-928-0085",
  "priceRange": "Contingency basis — no fee unless we recover compensation",
  "areaServed": {
    "@type": "City",
    "name": "Houston",
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
  "serviceType": "Hair Relaxer Cancer Lawsuit Representation"
}
</script>
```

---

## PAGE 2 — Texas Hair Relaxer Lawyer

### FAQPage Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "I'm a military spouse stationed at Fort Cavazos. I used hair relaxers from age 14 to age 50 and was diagnosed with endometrial cancer last year. Do I have a case?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, very likely. Endometrial cancer is a primary qualifying condition, 36 years of regular use significantly exceeds the four-times-per-year threshold the NIH Sister Study identified, and military spouse status does not affect your right to file. Call 972-928-0085 for a free case review."
      }
    },
    {
      "@type": "Question",
      "name": "I live in East Texas and there are no other hair relaxer attorneys around. Can Goff Law represent me from Dallas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Texas attorneys can represent clients across the state, and MDL 3060 is filed in federal court in Illinois — no party physically appears in Texas for the federal litigation. We routinely represent women throughout Texas, including East Texas, the Panhandle, Permian Basin, Coastal Bend, and South Texas."
      }
    },
    {
      "@type": "Question",
      "name": "I'm an active-duty Black woman service member. Will filing affect my service?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. Filing a personal injury claim against private chemical manufacturers has no effect on your military service, security clearance, promotion eligibility, or any other aspect of your career."
      }
    },
    {
      "@type": "Question",
      "name": "I'm a Latina who used relaxers for very curly hair. Do I qualify?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, if you have documented use and a qualifying medical diagnosis. We have a Spanish-language information page at /abogado-alisador-cabello-texas/ with the same legal information."
      }
    },
    {
      "@type": "Question",
      "name": "What is the statute of limitations for hair relaxer cancer claims in Texas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Generally two years from the date of diagnosis OR from the date you knew or should have known the cancer was linked to hair relaxers (the discovery rule). Many older diagnoses still qualify under the discovery rule because the link was not widely understood until October 2022."
      }
    },
    {
      "@type": "Question",
      "name": "How much is a Texas hair relaxer cancer lawsuit worth?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Projected settlement values range from $50,000 to $1,500,000+ per qualifying claim. Range depends on cancer type, stage at diagnosis, age, duration of hair relaxer use, and documentation strength."
      }
    },
    {
      "@type": "Question",
      "name": "My mother died of ovarian cancer in 2021. Can I file on her behalf?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Wrongful death and survival action claims may be filed by the deceased's spouse, children, or estate representative. The discovery rule analysis applies to when you reasonably knew the cancer might be linked to hair relaxers."
      }
    },
    {
      "@type": "Question",
      "name": "I used relaxers in the 1970s, 1980s, and 1990s. Was the formulation different back then?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Some formulations have changed over time, but endocrine-disrupting chemicals (phthalates, formaldehyde-releasing preservatives, parabens) were common in hair relaxer formulations across all these decades. Older use periods are not excluded from the litigation; if anything, longer cumulative exposure typically strengthens claims."
      }
    },
    {
      "@type": "Question",
      "name": "Do I have to sue Walmart, Walgreens, CVS, or Sally Beauty?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. The defendants in MDL 3060 are the chemical manufacturers — L'Oréal, SoftSheen-Carson, Strength of Nature, Namaste, Dabur, and others. Retailers and salons are not defendants."
      }
    },
    {
      "@type": "Question",
      "name": "What does it cost to hire Goff Law for a Texas hair relaxer claim?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Nothing up front. Hair relaxer cases are handled on contingency — no fee unless your claim recovers compensation. Initial consultations are free, confidential, and carry no obligation."
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
  "name": "Goff Law - Texas Hair Relaxer Lawyer",
  "description": "Goff Law represents Texas women statewide diagnosed with uterine, endometrial, or ovarian cancer after using chemical hair relaxers in federal MDL 3060. Particular focus on military spouses and women outside major metros.",
  "url": "https://gofflawdfw.com/texas-hair-relaxer-lawyer/",
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
  "serviceType": "Hair Relaxer Cancer Lawsuit Representation"
}
</script>
```

---

## PAGE 3 — North Texas Hair Relaxer Lawyer

### FAQPage Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "I live in Cedar Hill and used Dark & Lovely from age 11 to age 45. I was diagnosed with endometrial cancer in 2024. Do I have a case?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, very likely. Endometrial cancer is a primary qualifying condition. Dark & Lovely is a primary defendant product (L'Oréal/SoftSheen-Carson). 34 years of consistent use significantly exceeds the four-times-per-year NIH threshold. A 2024 diagnosis is within the standard Texas statute of limitations. Call 972-928-0085."
      }
    },
    {
      "@type": "Question",
      "name": "I moved to Plano from Atlanta in 2010 and continued using relaxers. Does my Atlanta use history count?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Hair relaxer use history is cumulative across all locations. Your Atlanta use plus your North Texas use together support a strong cumulative exposure claim. The federal MDL applies the same standards regardless of where the use occurred."
      }
    },
    {
      "@type": "Question",
      "name": "I used Olive Oil and African Pride products. Are those covered?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Olive Oil hair products (Namaste Laboratories) and African Pride products (Strength of Nature) are both made by named MDL 3060 defendants. Mixed brand use is common and supports claims."
      }
    },
    {
      "@type": "Question",
      "name": "I'm a North Texas suburb woman of Black and Latina heritage. Are mixed-heritage women covered?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. The MDL is open to all women who used chemical hair relaxers and have qualifying diagnoses, regardless of heritage."
      }
    },
    {
      "@type": "Question",
      "name": "I went to the same Black salon in Arlington for 15 years. Should I ask for my client records?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "It's worth asking, but don't worry if records are incomplete or unavailable. Your attorney can also subpoena salon records if needed for your claim. Family corroboration of regular salon visits is often sufficient even without formal salon records."
      }
    },
    {
      "@type": "Question",
      "name": "How much is a North Texas hair relaxer cancer lawsuit worth?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Projected settlement values range from $50,000 to $1,500,000+ per qualifying claim. Range depends on cancer type, stage, age, duration of use, and documentation strength."
      }
    },
    {
      "@type": "Question",
      "name": "What is the statute of limitations for hair relaxer cancer claims in Texas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Generally two years from the date of diagnosis OR from the date you knew or should have known the cancer was linked to hair relaxers (the discovery rule). Many older diagnoses still qualify under the discovery rule because the link was not widely understood until October 2022."
      }
    },
    {
      "@type": "Question",
      "name": "I'm a teacher in Frisco ISD. Will filing a lawsuit affect my career or pension?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. Filing a personal injury claim against private chemical manufacturers has no effect on your employment, teaching license, district benefits, or Teacher Retirement System of Texas pension."
      }
    },
    {
      "@type": "Question",
      "name": "Do I have to sue Sally Beauty, Ulta, Walmart, or my favorite Black-owned beauty supply store?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. The defendants in MDL 3060 are the chemical manufacturers — L'Oréal, SoftSheen-Carson, Strength of Nature, Namaste, Dabur, and others. Retailers and salons are not defendants."
      }
    },
    {
      "@type": "Question",
      "name": "What does it cost to hire Goff Law for a North Texas hair relaxer claim?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Nothing up front. Hair relaxer cases are handled on contingency — no fee unless your claim recovers compensation. Initial consultations are free, confidential, and carry no obligation."
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
  "name": "Goff Law - North Texas Hair Relaxer Lawyer",
  "description": "Goff Law represents women throughout DFW suburbs — Plano, Frisco, Allen, McKinney, Arlington, Garland, Cedar Hill, DeSoto, Lancaster, Mansfield, Grand Prairie — diagnosed with cancer after using chemical hair relaxers.",
  "url": "https://gofflawdfw.com/north-texas-hair-relaxer-lawyer/",
  "telephone": "+1-972-928-0085",
  "priceRange": "Contingency basis — no fee unless we recover compensation",
  "areaServed": [
    {"@type": "City", "name": "Plano", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Frisco", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Arlington", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Garland", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Cedar Hill", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "DeSoto", "containedInPlace": {"@type": "State", "name": "Texas"}},
    {"@type": "City", "name": "Mansfield", "containedInPlace": {"@type": "State", "name": "Texas"}}
  ],
  "provider": {
    "@type": "Attorney",
    "name": "Jim Goff",
    "url": "https://gofflawdfw.com/"
  },
  "serviceType": "Hair Relaxer Cancer Lawsuit Representation"
}
</script>
```

---

## PAGE 4 — Abogado de Alisador de Cabello en Texas (Spanish)

### FAQPage Schema (Spanish — keep `"inLanguage": "es"`)

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "inLanguage": "es",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Usé alisadores Dark & Lovely durante 20 años y fui diagnosticada con cáncer endometrial. ¿Tengo un caso?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Sí, muy probablemente. El cáncer endometrial es una condición calificativa principal, Dark & Lovey es un producto demandado principal (L'Oréal/SoftSheen-Carson), y 20 años de uso regular excede significativamente el umbral de cuatro veces al año del Estudio NIH Sister. Llame al 972-928-0085 para una revisión de caso gratuita."
      }
    },
    {
      "@type": "Question",
      "name": "Soy una mujer latina que usó alisadores químicos. ¿Califico?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Sí. Aunque los alisadores químicos se han comercializado principalmente a mujeres afroamericanas, las mujeres latinas que usaron estos productos durante años y han sido diagnosticadas con un cáncer calificativo califican igual que cualquier otra mujer."
      }
    },
    {
      "@type": "Question",
      "name": "Soy indocumentada. ¿Puedo todavía presentar una demanda?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Sí. Su estatus migratorio no afecta su derecho a presentar una demanda en un tribunal federal por daños de un producto defectuoso. Toda la información compartida con su abogado es confidencial y protegida por el privilegio abogado-cliente. El tribunal federal no comparte información sobre demandantes con autoridades de inmigración."
      }
    },
    {
      "@type": "Question",
      "name": "¿Cuánto vale una demanda de cáncer por alisador de cabello?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Las proyecciones de acuerdo varían entre $50,000 y $1,500,000+ por reclamo calificativo, dependiendo del tipo de cáncer, la etapa al diagnóstico, la edad, la duración del uso, y la fortaleza de la documentación."
      }
    },
    {
      "@type": "Question",
      "name": "¿Cuál es el estatuto de limitaciones para reclamos de cáncer por alisador de cabello en Texas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Generalmente dos años desde la fecha del diagnóstico O desde la fecha en que usted supo o debió haber sabido que el cáncer estaba vinculado a los alisadores de cabello (la regla del descubrimiento). Porque el vínculo no era ampliamente entendido hasta octubre de 2022, muchos diagnósticos más antiguos todavía califican."
      }
    },
    {
      "@type": "Question",
      "name": "Mi madre murió de cáncer de ovario. ¿Puedo presentar una demanda en su nombre?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Sí. Los reclamos de muerte injusta y acción de supervivencia pueden ser presentados por el cónyuge, hijos, o representante del patrimonio de la fallecida."
      }
    },
    {
      "@type": "Question",
      "name": "¿Tengo que demandar a Walmart, Walgreens o Sally Beauty?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. Los demandados en MDL 3060 son los fabricantes químicos — L'Oréal, SoftSheen-Carson, Strength of Nature, Namaste, Dabur, y otros. Los minoristas y salones no son demandados."
      }
    },
    {
      "@type": "Question",
      "name": "Nunca guardé los empaques de mis alisadores. ¿Puedo todavía presentar?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Sí. La mayoría de las reclamantes no tienen empaques. Su abogado trabaja con la reconstrucción del historial de uso del producto (memoria, declaraciones de familiares, registros de salón, documentación de patrón de compra al por menor) para construir el reclamo."
      }
    },
    {
      "@type": "Question",
      "name": "¿Cuánto cuesta contratar a Goff Law para un reclamo de cáncer por alisador?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Nada por adelantado. Los casos de alisador de cabello se manejan a base de contingencia — no hay honorarios a menos que su reclamo recupere compensación. Las consultas iniciales son gratuitas, confidenciales, y no tienen obligación."
      }
    },
    {
      "@type": "Question",
      "name": "¿Goff Law tiene personal que habla español?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Sí. Atendemos a clientas en español para asegurar que el lenguaje no sea una barrera para la justicia."
      }
    }
  ]
}
</script>
```

### LegalService Schema (Spanish version)

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LegalService",
  "inLanguage": "es",
  "name": "Goff Law - Abogado de Alisador de Cabello en Texas",
  "description": "Goff Law representa a mujeres latinas en Texas diagnosticadas con cáncer de útero, endometrial u ovárico después de usar alisadores químicos de cabello en MDL 3060 federal. Hablamos español.",
  "url": "https://gofflawdfw.com/abogado-alisador-cabello-texas/",
  "telephone": "+1-972-928-0085",
  "priceRange": "Base de contingencia — no hay honorarios a menos que recuperemos compensación",
  "areaServed": {
    "@type": "State",
    "name": "Texas"
  },
  "provider": {
    "@type": "Attorney",
    "name": "Jim Goff",
    "url": "https://gofflawdfw.com/"
  },
  "serviceType": "Representación legal de demanda de cáncer por alisador de cabello",
  "availableLanguage": ["es", "en"]
}
</script>
```

---

## EXISTING DALLAS PAGE — Schema add-on

The existing `/dallas/hair-relaxers/` page has FAQ-style questions in its content but likely lacks proper FAQPage schema markup. Add this block to that page to enable AI Overview / featured snippet eligibility.

### FAQPage Schema for existing Dallas page

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "I stopped using relaxers years ago, does it still count?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Hair relaxer cancer claims are based on cumulative lifetime exposure, not current use. If you used chemical hair relaxers for multiple years and have been diagnosed with a qualifying cancer, you may qualify regardless of when you stopped using them. The chemicals' effects persist long after use ends."
      }
    },
    {
      "@type": "Question",
      "name": "I only used one brand. Do I still qualify?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, if the brand is one of the named MDL 3060 defendants (Dark & Lovely, Optimum, Just for Me, Motions, African Pride, Olive Oil, and many others). Single-brand use can support a claim just as well as mixed-brand use."
      }
    },
    {
      "@type": "Question",
      "name": "I used store-bought kits, not salon products. Does that matter?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. Store-bought kits and salon applications qualify equally. The chemical formulations and the resulting exposure are the same regardless of where the product was applied."
      }
    },
    {
      "@type": "Question",
      "name": "No one else in my family has cancer. Could it still be from the product?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Hair relaxer cancer claims are based on chemical exposure, not genetic predisposition. The NIH Sister Study found that women who used hair relaxers more than four times per year had more than double the risk of uterine cancer regardless of family cancer history. Many qualifying claimants have no family history of cancer."
      }
    },
    {
      "@type": "Question",
      "name": "I never saved the packaging. Does that matter?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. Most claimants don't have packaging — these are everyday products that get discarded after use. Your attorney works with product use history reconstruction (memory, family member statements, salon records, retail pattern documentation) to build the claim."
      }
    },
    {
      "@type": "Question",
      "name": "I do not have medical insurance. Can I still file?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Insurance status does not affect your right to file a claim. Hair relaxer cases are handled on contingency — no fee unless your claim recovers compensation. If you need help accessing care during the litigation, your attorney may be able to connect you with resources."
      }
    },
    {
      "@type": "Question",
      "name": "My diagnosis was a few years ago. Am I too late?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Probably not. Texas's statute of limitations runs from the date of diagnosis OR from the date you knew or should have known the cancer was linked to hair relaxers (the discovery rule). Because the link was not widely understood until the October 2022 NIH study, many older diagnoses still qualify under the discovery rule."
      }
    },
    {
      "@type": "Question",
      "name": "I had fibroids, not cancer. Do I qualify?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Uterine fibroids are a secondary claim type in MDL 3060. Qualifying evidence for fibroid claims is emerging but the litigation primarily centers on cancer claims. Speak with an attorney about your specific circumstances."
      }
    },
    {
      "@type": "Question",
      "name": "The product was not recalled. Does that affect my claim?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. A product does not need to be recalled to be the subject of a product liability claim. The MDL 3060 litigation is proceeding based on the manufacturers' failure to warn of known health risks, regardless of whether they have recalled any specific product."
      }
    },
    {
      "@type": "Question",
      "name": "The brand I used is not in the news. Should I still call?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Many brands beyond those most frequently mentioned in news coverage are named in MDL 3060. The list of named defendants includes L'Oréal USA, SoftSheen-Carson, Strength of Nature, Namaste Laboratories, Dabur USA, Godrej SON Holdings, Revlon, and others. Call to discuss your specific brand history."
      }
    }
  ]
}
</script>
```

**Note:** Use the SAME questions as currently in the page's FAQ section to match what users see (the questions above are reconstructed from the WebFetch audit; verify against the actual page content and adjust if any differ).
