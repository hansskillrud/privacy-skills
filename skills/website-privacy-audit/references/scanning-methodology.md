# Website scanning methodology

## Scope and page selection

Review one or more pages of the website from a privacy perspective. Identify the technologies that indicate the website owner is collecting or sharing visitor data, the policies currently published on the website, and whether clear disclosures are made for specific website features.

- Look for a sitemap to choose pages. Adding `/sitemap.xml` to the main URL often leads to the sitemap, and `robots.txt` may list its location.
- Prioritize the homepage and pages likely to contain data collection, such as contact, booking, newsletter signup, cart and checkout pages.
- Scan each selected page thoroughly. Fully scanning a few pages is better than partially scanning many.
- Tell the user which pages you audited and, where possible, which pages you did not.
- Report pages you could not access. For example, if the website sells products but you could not reach the checkout page, say so.

## Inspection methods

When auditing a website, use as many of the following inspection methods as your available tools permit:

- Inspect the original HTML source code.
- Inspect the rendered DOM after JavaScript has executed.
- Inspect browser network requests, including requests initiated by other scripts.
- Inspect first-party and third-party cookies.
- Inspect local storage and session storage.
- Inspect embedded iframes.
- Inspect tracking pixels and image-based tracking requests.
- Inspect externally hosted fonts, stylesheets and other resources.
- Identify technologies loaded through tag managers.
- Scroll through pages to identify technologies that are lazy-loaded.
- Interact with website features, such as video players and expandable content, that may initiate additional third-party requests.
- Inspect pages containing forms, videos, maps, booking tools and eCommerce functionality.
- Evaluate website behavior before and after interacting with the consent banner.

Do not rely exclusively on the website's HTML source code, as many third-party technologies are dynamically loaded.

Do not assume that a technology is absent simply because it was not detected during the scan. Some technologies may only load under certain conditions, in certain geographic locations, after specific user interactions or on pages that were not audited.

Some data collection and sharing activities may occur server-side and may not be detectable through a browser-based audit.

If your available tools do not support any of these inspection methods, disclose these limitations in your final report.
