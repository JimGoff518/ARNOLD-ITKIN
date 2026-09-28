# JSON-LD Schema Blocks — Paragard Pages

**Use:** Drop each block into the corresponding page's HTML `<head>` as a `<script type="application/ld+json">` tag.

**Coverage:** 5 pages — FAQPage + LegalService schema each (10 schema blocks total).

---

## PAGE 1 — Dallas Paragard Lawyer

### FAQPage Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {"@type":"Question","name":"I had a Paragard IUD removed at a Dallas OB-GYN clinic and a piece broke off and stayed in my uterus. Do I qualify?","acceptedAnswer":{"@type":"Answer","text":"Yes, very likely. Paragard breakage during removal with retained fragments is the primary qualifying scenario in MDL 2974. If you have medical records documenting the breakage and the retained fragment, you should speak with an attorney. Call 972-928-0085 for a free case review."}},
    {"@type":"Question","name":"I had to have a hysterectomy because of Paragard complications. Is that a stronger case?","acceptedAnswer":{"@type":"Answer","text":"Yes. Hysterectomy as a direct consequence of Paragard-related complications typically supports higher-value claims because the injury is severe, irreversible, and well-documented."}},
    {"@type":"Question","name":"The first bellwether trial was a defense verdict. Does that mean my case is worthless?","acceptedAnswer":{"@type":"Answer","text":"No. Bellwether trials test specific plaintiffs' cases under specific facts. A defense verdict in one trial does not establish that all Paragard plaintiffs lose. Subsequent bellwether trials may produce different outcomes, and settlement negotiations often advance after multiple bellwether data points."}},
    {"@type":"Question","name":"How much is my Dallas Paragard lawsuit worth?","acceptedAnswer":{"@type":"Answer","text":"Projected settlement values currently range from $40,000 to $400,000+ per qualifying claim, depending on severity of complications, whether infertility resulted, number of surgeries required, and documentation strength. Values are being recalibrated following the first bellwether defense verdict."}},
    {"@type":"Question","name":"I had a Mirena IUD, not a Paragard. Do I qualify?","acceptedAnswer":{"@type":"Answer","text":"No, not under MDL 2974. Mirena, Kyleena, Liletta, and Skyla are hormonal IUDs made by different manufacturers and subject to separate litigation. Paragard is the only non-hormonal copper IUD on the U.S. market."}},
    {"@type":"Question","name":"What is the statute of limitations for Paragard claims in Texas?","acceptedAnswer":{"@type":"Answer","text":"Generally two years from the date of injury OR from the date you knew or should have known the injury was linked to a defective product (the discovery rule). Speak with an attorney before assuming your claim is time-barred."}},
    {"@type":"Question","name":"Do I have to sue my OB-GYN or the Dallas clinic where the device was removed?","acceptedAnswer":{"@type":"Answer","text":"No. The defendants are the manufacturers — Teva Pharmaceuticals and CooperSurgical — not your healthcare providers. Your OB-GYN, clinic, or hospital is not on trial."}},
    {"@type":"Question","name":"Do I have to travel to Georgia for my case?","acceptedAnswer":{"@type":"Answer","text":"No. MDL 2974 is centralized in the Northern District of Georgia procedurally, but individual claimants do not appear in court unless selected for bellwether trial."}},
    {"@type":"Question","name":"What does it cost to hire Goff Law for a Paragard claim?","acceptedAnswer":{"@type":"Answer","text":"Nothing up front. Paragard cases are handled on contingency — no fee unless your claim recovers compensation. Initial consultations are free, confidential, and carry no obligation."}},
    {"@type":"Question","name":"My fertility is affected and we wanted more children. Can that be part of my claim?","acceptedAnswer":{"@type":"Answer","text":"Yes. Loss of fertility, whether primary (cannot become pregnant) or secondary (cannot carry to term safely), is a significant component of Paragard claims and often increases case value substantially."}}
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
  "name": "Goff Law - Dallas Paragard Lawyer",
  "description": "Goff Law represents Dallas women injured by Paragard IUD breakage, uterine perforation, embedded fragments, or surgical complications in federal MDL 2974.",
  "url": "https://gofflawdfw.com/dallas-paragard-lawyer/",
  "telephone": "+1-972-928-0085",
  "priceRange": "Contingency basis — no fee unless we recover compensation",
  "areaServed": {"@type":"City","name":"Dallas","containedInPlace":{"@type":"State","name":"Texas"}},
  "provider": {"@type":"Attorney","name":"Jim Goff","url":"https://gofflawdfw.com/"},
  "serviceType": "Paragard IUD Injury Lawsuit Representation"
}
</script>
```

---

## PAGE 2 — Houston Paragard Lawyer

### FAQPage Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {"@type":"Question","name":"I had my Paragard removed at Texas Medical Center and pieces broke off. Do I qualify?","acceptedAnswer":{"@type":"Answer","text":"Yes, very likely. Paragard breakage during removal with retained fragments is the primary qualifying scenario in MDL 2974. TMC operative reports typically provide strong documentation. Call 972-928-0085."}},
    {"@type":"Question","name":"I had a hysterectomy because Paragard fragments couldn't be retrieved any other way. Is that a stronger case?","acceptedAnswer":{"@type":"Answer","text":"Yes. Hysterectomy due to Paragard complications represents one of the most severe and well-documented injury categories, typically supporting higher-value claims."}},
    {"@type":"Question","name":"The first bellwether trial was a defense verdict. Should I still file?","acceptedAnswer":{"@type":"Answer","text":"That's a judgment call we'll help you make. The defense verdict does not invalidate other claims, but it does mean settlement value projections are now lower and uncertain. We're open with claimants about the changed landscape."}},
    {"@type":"Question","name":"How much is a Houston Paragard lawsuit worth?","acceptedAnswer":{"@type":"Answer","text":"Projected values currently range from $40,000 to $400,000+ per qualifying claim, depending on severity, surgeries required, fertility impact, and documentation. Being recalibrated post-first-bellwether."}},
    {"@type":"Question","name":"I had a Mirena, not a Paragard. Do I qualify?","acceptedAnswer":{"@type":"Answer","text":"No, MDL 2974 covers Paragard only. Mirena, Kyleena, Liletta, and Skyla are hormonal IUDs subject to separate litigation."}},
    {"@type":"Question","name":"I'm a Houston Latina who had Paragard complications. Are Spanish-speaking attorneys available?","acceptedAnswer":{"@type":"Answer","text":"Yes. We have a Spanish-language information page at /abogada-paragard-texas/ and Spanish-speaking client communication available."}},
    {"@type":"Question","name":"Do I have to sue Planned Parenthood Gulf Coast or my Houston OB-GYN?","acceptedAnswer":{"@type":"Answer","text":"No. The defendants are the manufacturers — Teva Pharmaceuticals and CooperSurgical — not your healthcare providers."}},
    {"@type":"Question","name":"What is the statute of limitations for Paragard claims in Texas?","acceptedAnswer":{"@type":"Answer","text":"Generally two years from the date of injury OR the date you knew or should have known the injury was linked to the device (the discovery rule)."}},
    {"@type":"Question","name":"Do I have to travel to Georgia for my case?","acceptedAnswer":{"@type":"Answer","text":"No. The MDL is centralized procedurally; individual claimants typically don't appear in court unless selected for bellwether trial."}},
    {"@type":"Question","name":"My infertility was attributed to Paragard complications. How does that affect my case?","acceptedAnswer":{"@type":"Answer","text":"Loss of fertility — primary or secondary — is a significant component of Paragard claims and often substantially increases case value because the injury is permanent and severe."}}
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
  "name": "Goff Law - Houston Paragard Lawyer",
  "description": "Goff Law represents Houston women injured by Paragard IUD breakage including Texas Medical Center, Houston Methodist, Memorial Hermann, and Planned Parenthood Gulf Coast patients in federal MDL 2974.",
  "url": "https://gofflawdfw.com/houston-paragard-lawyer/",
  "telephone": "+1-972-928-0085",
  "priceRange": "Contingency basis — no fee unless we recover compensation",
  "areaServed": {"@type":"City","name":"Houston","containedInPlace":{"@type":"State","name":"Texas"}},
  "provider": {"@type":"Attorney","name":"Jim Goff","url":"https://gofflawdfw.com/"},
  "serviceType": "Paragard IUD Injury Lawsuit Representation"
}
</script>
```

---

## PAGE 3 — Texas Paragard IUD Lawyer

### FAQPage Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {"@type":"Question","name":"I'm a military spouse at Fort Cavazos who had Paragard removed at the military hospital and pieces stayed inside. Do I qualify?","acceptedAnswer":{"@type":"Answer","text":"Yes, very likely. Military medical records typically provide strong documentation. Filing does not affect your spouse's military service or your military benefits."}},
    {"@type":"Question","name":"I'm an active-duty Texas service member with Paragard breakage. Will filing affect my career?","acceptedAnswer":{"@type":"Answer","text":"No. Filing a personal injury claim against private manufacturers does not affect your military service, security clearance, promotion eligibility, or any military benefits."}},
    {"@type":"Question","name":"I live in rural Texas where Paragard removal happened years ago at a community clinic that's now closed. Can I still file?","acceptedAnswer":{"@type":"Answer","text":"Yes. Your attorney has tools (subpoenas, medical records requests) to recover records from closed facilities or transferred patient records. Do not assume your case is impossible without speaking with an attorney."}},
    {"@type":"Question","name":"The first bellwether trial was a defense verdict. Should I still file?","acceptedAnswer":{"@type":"Answer","text":"That's a judgment call we'll help you make. The defense verdict has changed the settlement landscape but does not invalidate all claims. We're transparent about the changed context."}},
    {"@type":"Question","name":"How much is a Texas Paragard lawsuit worth?","acceptedAnswer":{"@type":"Answer","text":"Projected values range from $40,000 to $400,000+ per qualifying claim, depending on severity, surgeries, fertility impact, and documentation. Being recalibrated post-first-bellwether."}},
    {"@type":"Question","name":"What is the statute of limitations for Paragard claims in Texas?","acceptedAnswer":{"@type":"Answer","text":"Generally two years from the date of injury OR the date you knew or should have known the injury was linked to the device (the discovery rule). Older injuries may still qualify."}},
    {"@type":"Question","name":"I had a Mirena IUD, not a Paragard. Do I qualify?","acceptedAnswer":{"@type":"Answer","text":"No, MDL 2974 covers Paragard only. Mirena, Kyleena, Liletta, and Skyla are hormonal IUDs subject to separate litigation."}},
    {"@type":"Question","name":"Can my husband or family file on my behalf if I died from Paragard complications?","acceptedAnswer":{"@type":"Answer","text":"Yes. Wrongful death and survival action claims may be filed by the deceased's spouse, children, or estate representative."}},
    {"@type":"Question","name":"I'm Latina and Spanish is my first language. Is help available in Spanish?","acceptedAnswer":{"@type":"Answer","text":"Yes. We have a Spanish-language information page at /abogada-paragard-texas/."}},
    {"@type":"Question","name":"What does it cost to hire Goff Law for a Texas Paragard claim?","acceptedAnswer":{"@type":"Answer","text":"Nothing up front. Contingency basis — no fee unless your claim recovers compensation. Initial consultations are free, confidential, and no obligation."}}
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
  "name": "Goff Law - Texas Paragard IUD Lawyer",
  "description": "Goff Law represents Texas women statewide — military spouses, rural Texas, smaller metros — injured by Paragard IUD breakage in federal MDL 2974.",
  "url": "https://gofflawdfw.com/texas-paragard-iud-lawyer/",
  "telephone": "+1-972-928-0085",
  "priceRange": "Contingency basis — no fee unless we recover compensation",
  "areaServed": {"@type":"State","name":"Texas"},
  "provider": {"@type":"Attorney","name":"Jim Goff","url":"https://gofflawdfw.com/"},
  "serviceType": "Paragard IUD Injury Lawsuit Representation"
}
</script>
```

---

## PAGE 4 — North Texas Paragard Lawyer

### FAQPage Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {"@type":"Question","name":"I had my Paragard removed at Baylor Scott & White in Plano and pieces stayed inside. Do I qualify?","acceptedAnswer":{"@type":"Answer","text":"Yes, very likely. Baylor Scott & White operative reports typically provide comprehensive documentation. Call 972-928-0085 for a free case review."}},
    {"@type":"Question","name":"I'm a Frisco teacher in TRS (Teacher Retirement System of Texas). Will filing affect my pension?","acceptedAnswer":{"@type":"Answer","text":"No. Filing a personal injury claim against private manufacturers has no effect on TRS, employer benefits, teaching license, or district insurance."}},
    {"@type":"Question","name":"I had to have a hysterectomy because of Paragard fragments that couldn't be retrieved otherwise. Is that a stronger case?","acceptedAnswer":{"@type":"Answer","text":"Yes. Hysterectomy due to Paragard complications represents one of the most severe and well-documented injury categories, typically supporting higher-value claims."}},
    {"@type":"Question","name":"My OB-GYN said the breakage was a known risk and not the manufacturer's fault. Does that affect my claim?","acceptedAnswer":{"@type":"Answer","text":"No. Whether your provider characterized the breakage as a known risk or as defective product is not determinative of the MDL claim. The federal litigation's central allegation is that the manufacturers failed to adequately warn doctors and patients about the breakage risk."}},
    {"@type":"Question","name":"The first bellwether trial was a defense verdict. Should I still file?","acceptedAnswer":{"@type":"Answer","text":"That's a judgment call we'll help you make based on your specific circumstances. The defense verdict has changed the landscape but does not invalidate all claims."}},
    {"@type":"Question","name":"How much is a North Texas Paragard lawsuit worth?","acceptedAnswer":{"@type":"Answer","text":"Projected values currently range from $40,000 to $400,000+ per qualifying claim. Being recalibrated post-first-bellwether."}},
    {"@type":"Question","name":"What is the statute of limitations for Paragard claims in Texas?","acceptedAnswer":{"@type":"Answer","text":"Generally two years from the date of injury OR the date you knew or should have known the injury was linked to the device (the discovery rule)."}},
    {"@type":"Question","name":"I had a Mirena IUD, not a Paragard. Do I qualify?","acceptedAnswer":{"@type":"Answer","text":"No, MDL 2974 covers Paragard only. Mirena and other hormonal IUDs are subject to separate litigation."}},
    {"@type":"Question","name":"I want to start a family and now I can't because of Paragard complications. How does that affect my case?","acceptedAnswer":{"@type":"Answer","text":"Loss of fertility is a significant component of Paragard claims and often substantially increases case value because the injury is permanent and severe."}},
    {"@type":"Question","name":"What does it cost to hire Goff Law for a North Texas Paragard claim?","acceptedAnswer":{"@type":"Answer","text":"Nothing up front. Contingency basis — no fee unless your claim recovers compensation."}}
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
  "name": "Goff Law - North Texas Paragard Lawyer",
  "description": "Goff Law represents women throughout the DFW suburbs — Plano, Frisco, Allen, McKinney, Arlington, Garland, Cedar Hill — injured by Paragard IUD breakage in federal MDL 2974.",
  "url": "https://gofflawdfw.com/north-texas-paragard-lawyer/",
  "telephone": "+1-972-928-0085",
  "priceRange": "Contingency basis — no fee unless we recover compensation",
  "areaServed": [
    {"@type":"City","name":"Plano","containedInPlace":{"@type":"State","name":"Texas"}},
    {"@type":"City","name":"Frisco","containedInPlace":{"@type":"State","name":"Texas"}},
    {"@type":"City","name":"Allen","containedInPlace":{"@type":"State","name":"Texas"}},
    {"@type":"City","name":"McKinney","containedInPlace":{"@type":"State","name":"Texas"}},
    {"@type":"City","name":"Arlington","containedInPlace":{"@type":"State","name":"Texas"}},
    {"@type":"City","name":"Garland","containedInPlace":{"@type":"State","name":"Texas"}}
  ],
  "provider": {"@type":"Attorney","name":"Jim Goff","url":"https://gofflawdfw.com/"},
  "serviceType": "Paragard IUD Injury Lawsuit Representation"
}
</script>
```

---

## PAGE 5 — Abogada de Paragard en Texas (Spanish)

### FAQPage Schema (Spanish)

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "inLanguage": "es",
  "mainEntity": [
    {"@type":"Question","name":"Me retiraron el Paragard en una clínica de salud para mujeres y se rompió, dejando piezas dentro de mí. ¿Califico?","acceptedAnswer":{"@type":"Answer","text":"Sí, muy probablemente. La ruptura del Paragard durante la extracción con fragmentos retenidos es el escenario calificativo principal en MDL 2974. Llame al 972-928-0085 para una revisión de caso gratuita."}},
    {"@type":"Question","name":"Soy indocumentada. ¿Puedo todavía presentar una demanda?","acceptedAnswer":{"@type":"Answer","text":"Sí. Su estatus migratorio no afecta su derecho a presentar una demanda en un tribunal federal por daños de un producto defectuoso. Toda la información es confidencial y protegida por el privilegio abogado-cliente."}},
    {"@type":"Question","name":"La primera prueba bellwether fue un veredicto de defensa. ¿Debo todavía presentar?","acceptedAnswer":{"@type":"Answer","text":"Esa es una decisión que le ayudaremos a tomar. El veredicto de defensa ha cambiado el panorama del acuerdo pero no invalida todos los reclamos. Somos transparentes sobre el contexto cambiado."}},
    {"@type":"Question","name":"¿Cuánto vale una demanda de Paragard?","acceptedAnswer":{"@type":"Answer","text":"Las proyecciones de acuerdo actualmente varían entre $40,000 y $400,000+ por reclamo calificativo. Siendo recalibradas después de la primera bellwether."}},
    {"@type":"Question","name":"Tuve que tener una histerectomía debido a complicaciones de Paragard. ¿Es ese un caso más fuerte?","acceptedAnswer":{"@type":"Answer","text":"Sí. La histerectomía debido a complicaciones de Paragard representa una de las categorías de lesiones más severas y mejor documentadas, típicamente apoyando reclamos de mayor valor."}},
    {"@type":"Question","name":"Tenía un Mirena, no un Paragard. ¿Califico?","acceptedAnswer":{"@type":"Answer","text":"No, MDL 2974 cubre solo Paragard. Mirena, Kyleena, Liletta, y Skyla son DIUs hormonales sujetos a litigación separada."}},
    {"@type":"Question","name":"¿Cuál es el estatuto de limitaciones para reclamos de Paragard en Texas?","acceptedAnswer":{"@type":"Answer","text":"Generalmente dos años desde la fecha de la lesión O desde la fecha en que usted supo o debió haber sabido que la lesión estaba vinculada al dispositivo (la regla del descubrimiento)."}},
    {"@type":"Question","name":"¿Tengo que demandar a mi OB-GYN o a Planned Parenthood?","acceptedAnswer":{"@type":"Answer","text":"No. Los demandados son los fabricantes — Teva Pharmaceuticals y CooperSurgical — no sus proveedores de atención médica."}},
    {"@type":"Question","name":"¿Tengo que viajar a Georgia?","acceptedAnswer":{"@type":"Answer","text":"No. El MDL está centralizado procesalmente; las demandantes individuales típicamente no aparecen en la corte a menos que sean seleccionadas para prueba bellwether."}},
    {"@type":"Question","name":"¿Cuánto cuesta contratar a Goff Law para un reclamo de Paragard?","acceptedAnswer":{"@type":"Answer","text":"Nada por adelantado. Los casos de Paragard se manejan a base de contingencia — no hay honorarios a menos que su reclamo recupere compensación."}}
  ]
}
</script>
```

### LegalService Schema (Spanish)

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LegalService",
  "inLanguage": "es",
  "name": "Goff Law - Abogada de Paragard en Texas",
  "description": "Goff Law representa a mujeres latinas en Texas lesionadas por la ruptura del DIU Paragard en MDL 2974 federal. Hablamos español.",
  "url": "https://gofflawdfw.com/abogada-paragard-texas/",
  "telephone": "+1-972-928-0085",
  "priceRange": "Base de contingencia — no hay honorarios a menos que recuperemos compensación",
  "areaServed": {"@type":"State","name":"Texas"},
  "provider": {"@type":"Attorney","name":"Jim Goff","url":"https://gofflawdfw.com/"},
  "serviceType": "Representación legal de demanda por lesiones de DIU Paragard",
  "availableLanguage": ["es", "en"]
}
</script>
```
