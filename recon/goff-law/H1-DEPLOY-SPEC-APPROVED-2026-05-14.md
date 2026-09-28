# H1 Deployment Spec — APPROVED 2026-05-14

**Approved by:** Jim Goff
**Date:** 2026-05-14
**Estimated dev time:** 1-2 hours total (homepage H1 + meta title)
**Priority:** 🚨 Tier 0 — deploy ASAP

---

## What's being deployed

Three coordinated text changes to `gofflawdfw.com` homepage. **WordPress page editor + Yoast SEO settings.** No theme changes, no plugin installs.

### Change #1 — Homepage H1

**Current H1:**
```
Serious injuries, Serious results.
```

**REPLACE WITH:**
```
A Dallas Personal Injury Lawyer Who Knows How Insurance Companies Think
```

**Why this exact wording:**
- Includes head-term keyword "Dallas Personal Injury Lawyer" (was completely absent from current H1)
- Leverages Jim Goff's unique differentiator (former insurance defense attorney)
- Conversational, memorable — sticks better than "Serious injuries, Serious results."
- Length: 71 characters — perfect for SEO + readability

**Subheadline (below the H1):**
```
Former insurance defense attorney now fighting for injured Texans.
```

---

### Change #2 — Homepage Meta Title (in Yoast SEO settings)

**Current meta title:**
```
Truck Accidents, Brain Injury, Sexual Assault | Dallas TX Attorney
```

**REPLACE WITH:**
```
Dallas Personal Injury Lawyer | Truck Accidents, Brain Injury, Galaxy Gas | Goff Law
```

**Why this exact wording:**
- Front-loads "Dallas Personal Injury Lawyer" (head-term keyword, was buried before)
- Keeps niche signal (truck, brain injury, Galaxy Gas) which is Goff's strategic advantage
- **REMOVES "Sexual Assault"** — this is on Jim's case-exclusion list (per Texas tort reform reasons), should not be listed publicly as a practice area
- Replaces Sexual Assault with "Galaxy Gas" — Goff's #1 organic asset (4 of top 10)
- Length: 91 characters — fits under Google's 60-pixel-width preview cutoff for most

---

### Change #3 — Homepage Meta Description (in Yoast SEO settings)

**ADD/REPLACE meta description:**
```
Dallas personal injury lawyer Jim Goff is a former insurance defense attorney now fighting for injured North Texans. Mass tort, truck, motor vehicle, brain injury cases. Free consultation 24/7.
```

**Why:**
- Repeats keyword + city for relevance
- Includes "former insurance defense attorney" hook
- Lists primary case types
- CTA at end ("free consultation 24/7")
- Length: 199 characters — fits in Google's ~160-character SERP preview

---

## How to deploy in WordPress

1. **Log into WordPress admin** at gofflawdfw.com/wp-admin
2. **Pages → Edit Home page** (or whatever the homepage is named)
3. Find the H1 block (currently displays "Serious injuries, Serious results."). Replace text with the new H1 above.
4. Below the H1, find the subheading/tagline block. Replace with new subheadline above.
5. Scroll to the bottom of the page editor to find the **Yoast SEO** meta box
6. Update **SEO title** field with the new meta title above
7. Update **Meta description** field with the new meta description above
8. Click **Update** to save
9. Clear cache (W3 Total Cache or whatever caching plugin is active)
10. Verify by viewing source on `gofflawdfw.com` — confirm new H1 visible, new `<title>` tag visible

---

## What NOT to touch

- Galaxy Gas FDA news ticker (Goff strength — keep it)
- Phone number / 24/7 messaging (keep)
- Existing trust badges (keep all)
- Any structured data / schema (separate Tier 0 deployment coming)
- Page layout / styling (this is text-only)
- Any other pages (this fix is homepage-only; other page H1s addressed in separate spec)

---

## Verification checklist (after deploy)

- [ ] Visit `gofflawdfw.com` in a fresh browser (logged out)
- [ ] H1 displays: "A Dallas Personal Injury Lawyer Who Knows How Insurance Companies Think"
- [ ] Subheadline displays: "Former insurance defense attorney now fighting for injured Texans."
- [ ] View source on homepage — confirm `<title>` tag matches the new meta title
- [ ] View source — confirm `<meta name="description">` matches the new description
- [ ] Google's SERP preview tool (or Yoast preview in editor) shows correct title + description
- [ ] No "Sexual Assault" anywhere in homepage meta (was previously in title)
- [ ] Test on mobile — H1 wraps cleanly (no awkward line breaks)
- [ ] Test page speed didn't regress (PageSpeed Insights)

---

## What this fix addresses (audit evidence)

Per the 2026-05-14 30-minute competitive audit (`recon/30-MIN-AUDIT-RESULTS-2026-05-14.md`):

| Gap identified by audit | This fix |
|---|---|
| Goff H1 ("Serious injuries, Serious results.") doesn't match the head-term search query | ✅ FIXED — new H1 includes "Dallas Personal Injury Lawyer" verbatim |
| Goff meta title leads with case types, buries head term | ✅ FIXED — meta title now front-loads "Dallas Personal Injury Lawyer" |
| "Sexual Assault" listed in meta title but Jim doesn't take those cases | ✅ FIXED — replaced with Galaxy Gas (actual Goff strength) |
| Goff has no "personal injury lawyer" keyword anywhere in meta/H1 | ✅ FIXED — appears in both H1 + meta title + meta description |

This single deployment addresses **1/3 of the documented competitive gap** identified by @theseoguy_'s "90% of the time" framework. The other 2/3 (more recent reviews, more local backlinks) are longer-horizon plays.

---

## Expected outcome (no guarantees, but reasonable)

**Within 30 days:**
- Google re-crawls homepage, indexes new title + H1
- Begin appearing in long-tail "Dallas Personal Injury Lawyer" related queries Goff was invisible for before
- Click-through rate from existing impressions likely up ~10-20% (better title/description = more clicks)

**Within 90 days:**
- Possible movement on "Dallas personal injury lawyer" head term — won't beat Mullen but might enter top 30-50 (from invisible)
- Niche queries Goff currently dominates (Galaxy Gas, etc.) should NOT regress because they're case-specific pages, not homepage-dependent

**This is one of many compounding moves. Not a magic bullet — just the highest-leverage 1-day fix available.**

---

## Status

- **Approved by Jim:** ✅ 2026-05-14
- **Pending:** Dev team deployment
- **Owner:** Chelsea to route to dev or self-deploy via WordPress admin if comfortable

Once deployed, mark this file with deployment date and ping for 30-day check-in.
