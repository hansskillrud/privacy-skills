# Third-party technology signatures

Use these signatures to recognize common third-party technologies in page source, the rendered DOM, network requests and browser storage. They are illustrative detection aids, not installation instructions and not an exhaustive list. Do not execute or inject any code.

A match is evidence that a technology is present. It is not, on its own, evidence that the technology executed, collected personal data or shared it. Confirm execution by observing the network requests listed, and apply the confidence levels and principles in `references/data-collection-audit.md`. Providers change their domains and cookie names over time, so verify attribution rather than relying on a single signal.

## Advertising and remarketing

| Technology | Script or code signals | Network request domains | Cookies and storage |
|---|---|---|---|
| Meta (Facebook) Pixel | `fbq('init', …)`, `fbevents.js` | `connect.facebook.net`, `www.facebook.com/tr` | `_fbp`, `_fbc` |
| Google Ads / conversion tracking | `gtag('config', 'AW-…')` | `googleadservices.com`, `googleads.g.doubleclick.net`, `www.google.com/pagead` | `_gcl_au`, `_gcl_aw` |
| LinkedIn Insight Tag | `_linkedin_partner_id`, `lintrk`, `insight.min.js` | `snap.licdn.com`, `px.ads.linkedin.com` | `li_sugr`, `bcookie`, `lidc`, `UserMatchHistory` |
| TikTok Pixel | `ttq.load(…)` | `analytics.tiktok.com` | `_ttp` |
| Pinterest Tag | `pintrk(…)` | `s.pinimg.com/ct/core.js`, `ct.pinterest.com` | `_pin_unauth`, `_pinterest_ct_ua` |
| Reddit Pixel | `rdt('init', …)` | `www.redditstatic.com/ads/pixel.js`, `alb.reddit.com` | `_rdt_uuid` |
| X (Twitter) Pixel | `twq('config', …)` | `static.ads-twitter.com`, `analytics.twitter.com`, `t.co/i/adsct` | `muc_ads`, `personalization_id` |
| Microsoft Advertising (UET) | `uetq`, `bat.js` | `bat.bing.com` | `_uetsid`, `_uetvid` |

## Analytics, session recording and tag management

| Technology | Script or code signals | Network request domains | Cookies and storage |
|---|---|---|---|
| Google Analytics 4 | `gtag('config', 'G-…')`, `gtag/js?id=G-` | `www.googletagmanager.com/gtag/js`, `*.google-analytics.com`, `analytics.google.com` | `_ga`, `_ga_<ID>` |
| Google Tag Manager | `GTM-` container ID, `dataLayer` | `www.googletagmanager.com/gtm.js` | none directly; inspect the tags it loads |
| Google Consent Mode | `gtag('consent', 'default', …)` | `gcs=` and `gcd=` parameters on Google requests | requests may be sent without cookies |
| Microsoft Clarity | `clarity(…)`, `clarity.ms/tag/` | `www.clarity.ms`, `*.clarity.ms/collect` | `_clck`, `_clsk`, `CLID` |
| Hotjar | `hjid`, `static.hotjar.com` | `static.hotjar.com`, `*.hotjar.com`, `*.hotjar.io` | `_hjSessionUser_<ID>`, `_hjSession_<ID>` |
| Contentsquare (Hotjar's parent company) | `t.contentsquare.net/uxa/` | `t.contentsquare.net`, `*.contentsquare.net` | `_cs_id`, `_cs_s` |
| Cloudflare Web Analytics | `data-cf-beacon` | `static.cloudflareinsights.com`, `cloudflareinsights.com/cdn-cgi/rum` | none (cookieless) |
| HubSpot tracking | `js.hs-scripts.com`, `_hsq` | `js.hs-scripts.com`, `track.hubspot.com`, `js.hs-analytics.net` | `hubspotutk`, `__hstc`, `__hssc` |

## Functional embeds that contact third-party servers

| Technology | Script or code signals | Network request domains | Cookies and storage |
|---|---|---|---|
| Google Fonts (remote) | `<link>` to `fonts.googleapis.com` | `fonts.googleapis.com`, `fonts.gstatic.com` | none; IP address still sent |
| Adobe Fonts (Typekit) | `use.typekit.net` | `use.typekit.net`, `p.typekit.net` | none |
| Font Awesome (kit or CDN) | `kit.fontawesome.com`, `use.fontawesome.com` | `kit.fontawesome.com`, `ka-f.fontawesome.com` | none |
| Google reCAPTCHA | `grecaptcha`, `recaptcha/api.js` | `www.google.com/recaptcha`, `www.gstatic.com/recaptcha` | `_GRECAPTCHA` |
| Cloudflare Turnstile | `cf-turnstile` | `challenges.cloudflare.com` | none typically |
| YouTube embed | `<iframe>` to `youtube.com/embed` | `www.youtube.com`, `i.ytimg.com`, `googlevideo.com` | `YSC`, `VISITOR_INFO1_LIVE` (privacy-enhanced `youtube-nocookie.com` embeds still contact Google) |
| Vimeo embed | `<iframe>` to `player.vimeo.com` | `player.vimeo.com`, `vimeocdn.com` | `vuid` |
| Google Maps embed | `<iframe>` to `google.com/maps/embed`, `maps.googleapis.com` | `maps.googleapis.com`, `maps.gstatic.com` | varies |
| Calendly | `assets.calendly.com`, `calendly-inline-widget` | `calendly.com`, `assets.calendly.com` | varies |

## Using these signatures

- Search the original HTML and the rendered DOM for the script or code signals.
- Filter network requests by the listed domains, and note whether each request happened before consent, after rejection or after acceptance.
- Check cookies and local storage for the listed names. Many tools also store identifiers in local storage instead of cookies.
- For technologies not listed here, identify the provider from the request domain and research its purpose before drawing conclusions.
- When a tag manager is present, expect additional technologies that do not appear in the page source.
