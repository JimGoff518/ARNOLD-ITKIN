# Goff Law — Technical Hygiene Audit

**Crawl date:** 2026-05-11
**Target:** https://gofflawdfw.com/

## TL;DR

Technical hygiene is **solid for the basics** but has some performance + observability gaps worth addressing.

✅ Clean canonicalization (all variants redirect to https://gofflawdfw.com/ no-www)
✅ HSTS enabled (1 year)
✅ Standard security headers (X-Frame-Options, X-Content-Type-Options, XSS-Protection, Referrer-Policy)
✅ HTTP/2 enabled
✅ W3 Total Cache plugin active

⚠️ `Cache-Control: max-age=0` means browsers re-fetch every page on every visit (poor performance)
⚠️ No `Content-Security-Policy` header
⚠️ DataForSeoBot blocked in robots.txt (matters if you subscribe to DataForSEO for your own site analytics)
⚠️ No core-web-vitals data captured in this audit (manual PageSpeed Insights check required)

---

## robots.txt

```
User-agent: *
Disallow: /wp-admin/
Disallow: /wp-includes/
Allow: /wp-admin/admin-ajax.php
Disallow: /wp-json/
Disallow: /*?rest_route=

User-agent: Bytespider
Disallow: /

User-agent: PetalBot
Disallow: /

User-agent: DataForSeoBot
Disallow: /

Sitemap: https://gofflawdfw.com/sitemap_index.xml
```

| Aspect | Status | Notes |
|---|---|---|
| Sitemap declaration | ✅ Present | `/sitemap_index.xml` |
| Crawl-delay | ✅ Not set | Google will crawl at its own pace |
| Disallow blocks affecting SEO | ✅ Only WordPress admin/API (standard) | |
| Major-bot blocks | ⚠️ Bytespider (TikTok), PetalBot (Huawei), **DataForSeoBot** | TikTok+Huawei block is fine. DataForSEO block matters only if Jim subscribes to that SERP API for monitoring his own site. |

**Action item:** If Jim subscribes to DataForSEO, remove the `DataForSeoBot Disallow: /` block so DataForSEO can audit gofflawdfw.com.

---

## HTTPS + canonicalization

| URL tested | Final URL | HTTP | # Redirects | Verdict |
|---|---|---|---|---|
| `http://gofflawdfw.com/` | `https://gofflawdfw.com/` | 200 | 1 | ✅ Clean |
| `http://www.gofflawdfw.com/` | `https://gofflawdfw.com/` | 200 | 2 | ✅ Clean (1 extra hop) |
| `https://gofflawdfw.com/` | `https://gofflawdfw.com/` | 200 | 0 | ✅ Canonical |
| `https://www.gofflawdfw.com/` | `https://gofflawdfw.com/` | 200 | 1 | ✅ Clean |

**Verdict:** All variants converge to `https://gofflawdfw.com/` (no-www, HTTPS). Standard, correct setup. The `http://www` path has 2 redirects (HTTP→HTTPS+www then drop www) — could be collapsed to 1 hop via server config but very minor.

---

## Response headers (homepage)

```
HTTP/1.1 200 OK
Server: Apache
Strict-Transport-Security: max-age=31536000
X-Frame-Options: SAMEORIGIN
X-XSS-Protection: 1; mode=block
X-Content-Type-Options: nosniff
Referrer-Policy: strict-origin-when-cross-origin
X-Powered-By: W3 Total Cache/2.7.1
Cache-Control: max-age=0, public, must-revalidate, proxy-revalidate, public, must-revalidate, proxy-revalidate
Vary: Accept-Encoding,Cookie
Upgrade: h2,h2c
Last-Modified: Wed, 29 Apr 2026 21:08:50 GMT
ETag: "21388-6509fc127ae7d"
Content-Type: text/html; charset=UTF-8
```

| Header | Status | Notes |
|---|---|---|
| HSTS | ✅ `max-age=31536000` (1 year) | Strong. Could add `includeSubDomains` and submit for HSTS preload list for extra credit. |
| Compression (Content-Encoding) | ⚠️ Not in this response | The `Vary: Accept-Encoding` header suggests it IS compressed — header may not be returned on HEAD requests. Verify with `curl --compressed`. |
| Cache-Control | ⚠️ `max-age=0, must-revalidate` | Browsers must check server every visit. Poor for repeat-visitor performance. W3 Total Cache should override this for static assets. |
| Server | Apache | Fine; not Nginx but not a problem. |
| HTTP/2 | ✅ `Upgrade: h2,h2c` | Modern protocol enabled. |
| ETag | ✅ Present | Allows conditional GETs (304 Not Modified). |
| HTTP/1.1 protocol | ✅ With h2 upgrade | OK |
| X-Frame-Options | ✅ SAMEORIGIN | Clickjacking protection. |
| X-XSS-Protection | ✅ Enabled | Legacy XSS protection (mostly redundant in modern browsers). |
| X-Content-Type-Options | ✅ nosniff | MIME-sniffing protection. |
| Referrer-Policy | ✅ strict-origin-when-cross-origin | Standard. |
| **Content-Security-Policy** | ❌ **MISSING** | No CSP. Modern security best practice — adds XSS + injection defense. Optional but recommended. |
| **Permissions-Policy** | ❌ Missing | Controls browser features (camera, mic, geolocation). Low priority. |

---

## Performance signals (cannot be measured from this audit — manual check required)

The plan calls for PageSpeed Insights / Lighthouse data. That requires either an API key (free but rate-limited) or a manual check via web UI.

**Action item:** Run these manually and paste scores back into this doc:
- **PageSpeed Insights**: https://pagespeed.web.dev/?url=https%3A%2F%2Fgofflawdfw.com%2F
- **GTmetrix**: https://gtmetrix.com/ (more detailed waterfall)
- **WebPageTest**: https://www.webpagetest.org/

Specific metrics to capture:
- LCP (Largest Contentful Paint) — Google's core metric, should be < 2.5s
- INP (Interaction to Next Paint) — should be < 200ms
- CLS (Cumulative Layout Shift) — should be < 0.1
- Mobile vs Desktop scores (Goff likely scores worse on mobile — most WP sites do)
- Page weight (homepage is 136KB which is reasonable; image-heavy pages may be 2-5MB)

**Common WP performance wins** (for the dev to address once measurements are in):
- Lazy-load below-the-fold images (verify in Phase 2 of UX recon — we already noted lazy-loading is missing on 35 homepage images)
- Use WebP / AVIF instead of JPEG
- Defer non-critical JS
- Inline critical CSS
- Set static asset `Cache-Control` to 1 year (currently `max-age=0`)

---

## Issues found (ranked)

| Priority | Issue | Fix | Effort |
|---|---|---|---|
| P1 | Cache-Control max-age=0 on HTML | Verify W3TC is configured for HTML caching OR set sensible Cache-Control (e.g., 5min for HTML, 1yr for static) | M (dev configuration) |
| P1 | No CSP header | Add Content-Security-Policy header (start in report-only mode) | M-L (requires testing) |
| P1 | DataForSeoBot blocked | Remove `DataForSeoBot Disallow: /` block IF Jim subscribes to DataForSEO | S (5 min) |
| P2 | Lazy-load missing on images (per UX recon) | Add `loading="lazy"` attribute via theme | M (theme work) |
| P2 | Missing Permissions-Policy header | Add modern Permissions-Policy header | S (config) |
| P3 | `http://www` has 2 redirects | Collapse to 1 hop in server config | S (config) |

---

## Comparison vs Thompson Law

| Aspect | Goff Law | Thompson Law |
|---|---|---|
| HTTPS canonicalization | ✅ Clean | ✅ Clean |
| HSTS | ✅ 1 year | (not audited) |
| HTTP/2 | ✅ | ✅ (assumed) |
| Stack | WordPress + Apache + W3 Total Cache | WordPress + Yoast |
| robots.txt crawl-delay | None | None |
| Sitemap structure | 4 sub-sitemaps (post, page, category, author) | 23 sub-sitemaps (huge site) |

No major technical hygiene gaps vs Thompson. The bigger gaps for Goff are on the **content/schema/UX side**, not technical infrastructure.

---

## Raw data
- robots.txt: `%TEMP%\goff-robots.txt`
- sitemap_index.xml: `%TEMP%\goff-sitemap-index.xml`
- Headers captured in this doc above.
