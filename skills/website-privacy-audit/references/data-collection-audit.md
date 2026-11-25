# Data collection audit

The goal of this audit is to identify website features and functionalities that collect personal data, share personal data with third parties and/or track website visitors. When a website visitor's browser makes a request directly to a third-party server, the visitor's IP address is generally disclosed to that third party. Additional information, such as browser information, device characteristics and referring URLs, may also be transmitted.

However, not all third-party technologies are designed to track website visitors. Some provide functionality, such as fonts, maps or video playback, while others may actively collect information about visitors and their behavior for analytics, marketing, security or other purposes.

When auditing a website, identify:

- The third-party technology and its provider.
- The purpose of the technology.
- What personal information is known or reasonably believed to be collected.
- What information is transmitted to third parties.
- Whether the technology tracks website visitors or their behavior.
- Whether the findings are confirmed, suspected or unable to be verified.

Do not assume that the absence of cookies means that no personal information is being collected or shared.

## Confidence levels for audit findings

When reporting findings from a website privacy audit, distinguish between the following:

- Confirmed: Direct evidence of the technology or activity was observed during the audit.
- Detected but not observed firing: The technology's code or configuration was identified, but the associated network requests or data collection activities were not observed during testing.
- Suspected: There are indicators that a technology or data collection activity may exist, but there is insufficient evidence to confirm it.
- Unable to verify: The technology or activity could not be verified due to technical limitations, access restrictions or other circumstances.
- Not tested: The page, functionality or consent scenario was not tested during the audit.

**Examples:**

- Google Analytics network requests were observed — Confirmed.
- Meta Pixel code was found in the website's source code, but no associated network requests were observed — Detected but not observed firing.
- Indicators suggest a possible Zapier integration — Suspected.
- Server-side data sharing with a CRM — Unable to verify.
- Technologies loading on an inaccessible checkout page — Not tested.

Assess confidence separately for the existence of a technology, its execution, the personal data it collects and the personal data it shares. Do not present assumptions as confirmed findings. Do not conclude that a technology is absent simply because it was not detected.

## Technology checklist

When scanning the website, look for anything that may collect or share visitor data, including:

1. Third-party advertising and remarketing embeds
    - Look for tracking pixels and tracking scripts.
    - Examples include Google Ads, Meta (Facebook) Pixel, LinkedIn Insight Tag, Pinterest Tag, TikTok Pixel, Reddit Pixel and X (Twitter) Pixel.
2. Third-party analytics embeds
    - Examples include Google Analytics, Hotjar, Microsoft Clarity and Snowplow.
3. Third-party calendar booking embeds
    - Examples include Calendly.
4. Content management systems
    - Determine which CMS the website is built on, such as WordPress, Squarespace, Shopify, Webflow or Duda.
5. Data linking platforms
    - These can be harder to spot. Look for signs of integrations such as Zapier.
6. eCommerce
    - Determine whether the website has an eCommerce component.
    - Identify integrated payment processors, such as Stripe, PayPal, Venmo, Apple Pay or Google Pay.
7. Forms
    - Identify form fields that request personal data, such as name, email address and phone number.
    - Include contact forms and newsletter signup forms.
    - Forms may be first-party (such as Gravity Forms on WordPress) or third-party (such as JotForm or HubSpot form embeds).
8. Third-party font loading
    - Identify whether Google Fonts are loaded remotely from Google's servers or hosted locally.
        - Remotely hosted Google Fonts result in the visitor's IP address being transmitted to Google and may raise privacy compliance concerns.
        - Encourage website owners to host fonts locally, where licensing permits, to avoid unnecessary data sharing with external font providers.
        - Additional information: https://termageddon.com/google-fonts-violates-gdpr/
    - Identify whether Adobe Fonts (Typekit) or Font Awesome are loaded from external servers.
9. Third-party hosting
    - Determine, where possible, whether the website is hosted by a third party, such as GridPane, A2 Hosting, GoDaddy, IONOS, Shopify, Squarespace or Duda.
    - WordPress is software, not a host. Many hosting companies offer WordPress hosting, so do not treat WordPress alone as identifying the host. Distinguish self-hosted WordPress software from WordPress.com's hosting service.
10. Third-party map embeds
    - Examples include Google Maps and Mapbox.
11. Third-party security and spam prevention
    - Examples include reCAPTCHA and Cloudflare Turnstile.
    - These tools may load globally in the `<head>` or only within forms.
12. Social media embeds
    - Look for embedded social media content, such as a "recent Instagram posts" or "Facebook feed" section in the body of a page. Plain links to social media profiles are not embeds.
13. Third-party customer review embeds
    - Examples include Elfsight.
14. Tag managers
    - The most common is Google Tag Manager, identified by a container ID beginning with "GTM-".
15. Third-party video embeds
    - Examples include YouTube, Vimeo and Wistia.
16. Reverse IP lookup and visitor identification tools
    - Examples include RB2B, Retention.com, Customers.ai, Warmly and LeadPost.
17. Third-party chat widgets
    - Include both standard live chat widgets and AI chat widgets.

## Additional Terms of Service considerations

The following features do not necessarily collect or share data, but they are worth noting because a Terms of Service can include disclosures that help limit liability:

1. Links to third-party websites. Terms can state that the website owner is not responsible for third-party websites.
2. Images, video and other content on the website, which applies to nearly all websites. Terms can include a DMCA disclosure.
