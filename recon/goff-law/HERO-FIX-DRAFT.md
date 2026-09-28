# Goff Law Homepage Hero — Tier-0 Fix Spec

**Created:** 2026-05-10
**Owner:** Jim Goff (decision) + WordPress dev (implementation)
**Companion to:** [recon/goff-law/UX-RECON-PHASE-1.md](UX-RECON-PHASE-1.md)
**Estimated dev time:** 4–8 hours (one workday max)

---

## The problem

Goff Law's current homepage hero is a giant gray banner displaying only:

> MILLIONS WON
> SERIOUS INJURIES, SERIOUS RESULTS.

No specific case results, no trust badges, no review count, no lead form, no proof of any kind. Compare to:

| Competitor | What they put above the fold |
|---|---|
| **Witherite** | Full 6-field lead form + Live Chat bubble + attorney portrait |
| **Thompson Law** | "$1.9 BILLION RECOVERED" + scrolling specific case results + red CTA button |
| **Mullen & Mullen** | "JOIN The Family" + 567 reviews / 4.9★ + "29% contingency" pricing differentiator |

We are losing the 3-second-decision battle.

---

## The fix (3 components)

### Component 1 — Replace the empty hero with a proof-stack hero

**Layout (above the fold, ~600px tall on desktop):**

```
┌────────────────────────────────────────────────────────────────────────┐
│ [Galaxy Gas FDA news ticker — KEEP, this is a Goff strength]    [✕]   │
├────────────────────────────────────────────────────────────────────────┤
│ [Goff Law logo]                  [phone icon] (214) GOFF-LAW   [MENU] │
│                                  Free Consultation • 24/7              │
├────────────────────────────────────────────────────────────────────────┤
│                                                                        │
│   ┌──────────────────────────────┐  ┌──────────────────────────────┐ │
│   │  HEADLINE LEFT COLUMN        │  │  LEAD FORM (right column)    │ │
│   │                              │  │                              │ │
│   │  A Dallas Personal Injury    │  │  Tell us about your case     │ │
│   │  Lawyer Who Knows How        │  │                              │ │
│   │  Insurance Companies Think   │  │  [First Name] [Last Name]    │ │
│   │                              │  │  [Phone     ] [Zip Code ]    │ │
│   │  Former insurance defense    │  │  [Email                ]     │ │
│   │  attorney now fighting for   │  │  [What happened?       ]     │ │
│   │  injured Texans.             │  │                              │ │
│   │                              │  │  ☐ Text me updates (TCPA)    │ │
│   │  $XX MILLION recovered       │  │                              │ │
│   │  for North Texas families    │  │  [ GET MY FREE REVIEW → ]    │ │
│   │                              │  │                              │ │
│   │  [BBB] [Avvo] [SuperLawyers] │  │  100% confidential. No fee   │ │
│   │  [TBLS] [Million $ Forum]    │  │  unless we win your case.    │ │
│   └──────────────────────────────┘  └──────────────────────────────┘ │
│                                                                        │
│   ★★★★★  [X.X based on N Google reviews]      [ 24/7 ]              │
│                                                                        │
└────────────────────────────────────────────────────────────────────────┘
```

### Component 2 — Make Crisp Chat visible from page load

Crisp is already installed (verified in HTML). Just needs config so the bubble shows immediately, not on scroll/delay.

### Component 3 — Move the contact form ABOVE the fold on /contact

The /contact page above-the-fold currently shows a banner with the word "CONTACT". Form is below. **Make the form the first thing visible** when /contact loads.

---

## Inputs needed from Jim before deploying

Before the dev can implement this, fill in these blanks:

| Slot | Current value (placeholder) | Need from Jim |
|---|---|---|
| Specific dollar amount under "$XX MILLION" | "$XX MILLION" | What's the largest verifiable settlement/verdict to display? Or aggregate "Over $X million recovered for our clients"? |
| Trust badges (which to display) | BBB, Avvo, SuperLawyers, TBLS, Million $ Forum | Which of these credentials does Goff actually hold? Send me the badge images or list. |
| Aggregate review count | "[X.X based on N Google reviews]" | Goff's actual Google review count + average rating |
| Vanity phone number | "(214) GOFF-LAW" | Acquire one OR use existing 972-928-0085 (less memorable) |
| Headline copy variation | "A Dallas Personal Injury Lawyer Who Knows How Insurance Companies Think" | Approve or substitute. This builds on the existing "former defense attorney" story buried below. Other options below ↓ |

### Headline copy alternatives (pick one)

**A. The "former defense attorney" angle (RECOMMENDED — leverages existing differentiation):**
> A Dallas Personal Injury Lawyer Who Knows How Insurance Companies Think

**B. The "lifelong Dallas" angle (also unique to Goff):**
> A Third-Generation Texan Fighting for Injured Dallasites

**C. The hybrid:**
> Born in Dallas. Trained by Insurance Defense. Now Fighting for You.

**D. The aggressive challenge:**
> Out-of-Town Lawyers Don't Know Dallas. We Do.

All four are stronger than "Millions Won" because they say something Thompson Law / Mullen & Mullen / Witherite cannot truthfully say.

---

## HTML/CSS code skeleton (drop-in)

This is a Tailwind-ish pseudo-implementation the WordPress dev can adapt to your theme (Avada / Divi / GeneratePress / whatever):

```html
<!-- HERO SECTION — Goff Law Tier-0 fix -->
<section class="hero" style="
  background: linear-gradient(135deg, #1a1a1a 0%, #2c2c2c 100%);
  color: #fff;
  padding: 4rem 2rem;
  min-height: 600px;
">
  <div class="container" style="max-width: 1200px; margin: 0 auto;">
    <div class="hero-grid" style="
      display: grid;
      grid-template-columns: 1fr 480px;
      gap: 4rem;
      align-items: center;
    ">

      <!-- LEFT: Headline + proof stack -->
      <div class="hero-left">
        <h1 style="
          font-size: clamp(2rem, 4vw, 3.5rem);
          font-weight: 800;
          line-height: 1.1;
          margin-bottom: 1.5rem;
          color: #fff;
        ">
          A Dallas Personal Injury Lawyer<br>
          Who Knows How Insurance<br>
          Companies Think.
        </h1>
        <p style="
          font-size: 1.25rem;
          color: #d4af37;  /* Goff's existing yellow accent — punched up */
          margin-bottom: 2rem;
          line-height: 1.4;
        ">
          Former insurance defense attorney now fighting for injured Texans.
        </p>

        <!-- Specific case result -->
        <div class="result-stat" style="
          margin-bottom: 2rem;
          padding: 1rem 1.5rem;
          border-left: 4px solid #d4af37;
          background: rgba(212, 175, 55, 0.08);
        ">
          <div style="font-size: 2rem; font-weight: 800;">$XX MILLION</div>
          <div style="font-size: 0.9rem; color: #ccc; text-transform: uppercase; letter-spacing: 1px;">
            recovered for North Texas families
          </div>
        </div>

        <!-- Trust badge row -->
        <div class="trust-badges" style="
          display: flex;
          gap: 1.5rem;
          align-items: center;
          flex-wrap: wrap;
          margin-bottom: 1rem;
          opacity: 0.9;
        ">
          <img src="/badges/bbb.png" alt="BBB Accredited" height="50">
          <img src="/badges/avvo.png" alt="Avvo Rated" height="50">
          <img src="/badges/super-lawyers.png" alt="Super Lawyers" height="50">
          <img src="/badges/tbls.png" alt="Texas Board Legal Specialization" height="50">
          <img src="/badges/million-dollar.png" alt="Million Dollar Advocates Forum" height="50">
        </div>

        <!-- Review aggregate -->
        <div class="review-row" style="
          display: flex;
          align-items: center;
          gap: 1rem;
          color: #ccc;
        ">
          <span style="font-size: 1.5rem; color: #fbbf24;">★★★★★</span>
          <span><strong>X.X</strong> based on <strong>N Google Reviews</strong></span>
        </div>
      </div>

      <!-- RIGHT: Lead form -->
      <div class="hero-form" style="
        background: #fff;
        color: #1a1a1a;
        padding: 2rem;
        border-radius: 8px;
        box-shadow: 0 20px 60px rgba(0,0,0,0.4);
      ">
        <h2 style="
          font-size: 1.5rem;
          font-weight: 700;
          margin-bottom: 0.5rem;
          color: #1a1a1a;
        ">
          Tell Us About Your Case
        </h2>
        <p style="font-size: 0.9rem; color: #666; margin-bottom: 1.5rem;">
          Free, confidential consultation — no fee unless we win.
        </p>

        <form action="/contact-submit" method="post" id="hero-lead-form">
          <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 0.75rem; margin-bottom: 0.75rem;">
            <input type="text" name="first_name" placeholder="First Name" required
              style="padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; width: 100%;">
            <input type="text" name="last_name" placeholder="Last Name" required
              style="padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; width: 100%;">
          </div>
          <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 0.75rem; margin-bottom: 0.75rem;">
            <input type="tel" name="phone" placeholder="Phone Number" required
              style="padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; width: 100%;">
            <input type="text" name="zip" placeholder="Zip Code"
              style="padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; width: 100%;">
          </div>
          <input type="email" name="email" placeholder="Email" required
            style="padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; width: 100%; margin-bottom: 0.75rem;">
          <textarea name="message" placeholder="Briefly: what happened?" rows="3"
            style="padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; width: 100%; margin-bottom: 0.75rem; resize: vertical;"></textarea>

          <!-- SMS opt-in (TCPA compliant) -->
          <label style="display: flex; gap: 0.5rem; align-items: flex-start; font-size: 0.8rem; color: #666; margin-bottom: 1rem; line-height: 1.3;">
            <input type="checkbox" name="sms_optin" style="margin-top: 0.2rem;">
            <span>Text me updates about my case. By checking this, I consent to receive text messages from Goff Law about my case. Message and data rates may apply. Reply STOP to opt out.</span>
          </label>

          <button type="submit" style="
            width: 100%;
            padding: 1rem;
            background: #d4af37;
            color: #1a1a1a;
            border: none;
            border-radius: 4px;
            font-size: 1.1rem;
            font-weight: 700;
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 1px;
          ">
            Get My Free Review →
          </button>
        </form>

        <p style="font-size: 0.75rem; color: #999; text-align: center; margin-top: 1rem; line-height: 1.4;">
          100% confidential. Available 24/7. No fee unless we win your case.
        </p>
      </div>

    </div>
  </div>
</section>

<!-- Mobile: stack form below headline. Add this CSS: -->
<style>
@media (max-width: 768px) {
  .hero-grid {
    grid-template-columns: 1fr !important;
    gap: 2rem !important;
  }
  .trust-badges {
    justify-content: center !important;
  }
}
</style>
```

---

## Form integration

The form posts to `/contact-submit` (placeholder). Wire to whichever lead-handling you currently use:

- If WordPress + WPForms / Gravity Forms: replace the `<form>` with their shortcode/embed
- If WordPress + a custom REST endpoint: implement `/wp-json/goff/v1/lead-submit`
- If Salesforce / HubSpot / Lawmatics CRM: use their Web-to-Lead form embed

**Required wiring:**
1. New leads land in your existing CRM
2. SMS opt-in field is captured separately (TCPA audit trail)
3. Auto-responder fires within 60 seconds: "Thanks for contacting Goff Law. A team member will reach out within 15 minutes."
4. If SMS opt-in checked: trigger an SMS within 60 seconds: "Hi [first name], it's the team at Goff Law. We got your message about your case. Calling you shortly. — Reply STOP to opt out."

---

## Crisp Chat visibility fix

In the Crisp Chat widget settings, ensure:
- `Show on page load: Yes` (not "show after delay" or "show on scroll")
- `Welcome message: "Hi — got a question about your accident? Text us here, no commitment."` (or similar)
- `Position: bottom-right` (not bottom-left where it might overlap the chat with the form)
- Match brand color: Goff yellow accent

---

## /contact page above-the-fold fix

The current /contact page shows a giant "CONTACT" banner above the fold. The form sits below.

**Fix:** Move the form to be the first thing visible. Same lead form as Component 1 above. The banner can stay smaller (e.g., a 200px-tall page header with breadcrumbs), or go entirely.

---

## Acceptance checklist

When the dev hands this back, verify:
- [ ] Above-the-fold on desktop (1440×900): form is fully visible
- [ ] Above-the-fold on mobile (375×667): headline + first 2 form fields visible
- [ ] All 5 trust badges render (no broken images)
- [ ] Specific case result dollar amount displayed
- [ ] Aggregate review count + star rating visible
- [ ] Form submits successfully and lands in CRM
- [ ] SMS opt-in field captured separately
- [ ] Auto-responder email fires
- [ ] Crisp Chat bubble visible from page load
- [ ] /contact page form is above the fold
- [ ] Page Speed Insights mobile score does NOT regress (test before/after)
- [ ] No layout breakage on iPhone SE (smallest common viewport)

---

## Estimated impact

Industry data on PI law firm form-vs-CTA conversion:
- Switching from "CTA → form on next page" to "form on hero" typically lifts lead capture **40-100%**
- Adding trust badges (BBB, Avvo, SuperLawyers) typically lifts conversion **10-25%**
- Adding specific case results vs vague "Millions Won" lifts conversion **15-30%**
- SMS opt-in collected at form submit → 2-3x faster intake response → higher close rate downstream

**Conservative composite estimate:** 50-100% lift in homepage lead capture rate. If Goff currently gets 10 form fills/week from the homepage, this could push to 15-20/week at no additional traffic cost.

(All numbers above are industry benchmarks, not Goff-specific. Actual results depend on traffic mix, ad targeting, and CRM responsiveness. Test, don't trust.)
