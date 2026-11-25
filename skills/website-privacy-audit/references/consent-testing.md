# Consent testing methodology

When auditing a website's consent implementation, determine:

- What third-party technologies are present on the website?
- Does the website have a consent solution installed?
- Can you identify the consent solution provider?
- Is the website presenting an opt-in or opt-out consent model?
- Does the consent solution appear to behave differently depending on the visitor's geographic location?
- Does the consent solution appropriately control third-party technologies based on the visitor's consent preferences?

Perform as many of the following tests as your available tools and the website's consent configuration permit:

## Test 1 — Before consent

Open the website in a fresh browser session without existing cookies, browser storage or consent preferences. Identify which third-party technologies, network requests, cookies and other storage mechanisms are present before interacting with the consent banner.

## Test 2 — Reject all

Reject all non-essential technologies. Identify whether non-essential technologies continue to load, transmit data or store information despite the visitor's rejection.

## Test 3 — Accept all

Using a fresh browser session, accept all technologies. Identify which additional technologies, network requests, cookies and storage mechanisms become active.

## Test 4 — Selective consent

Where available, test individual consent categories, such as Functional, Analytics and Marketing. Verify that technologies respect the visitor's selected preferences.

## Test 5 — Withdraw consent

After accepting non-essential technologies, locate the mechanism for changing or withdrawing consent. Withdraw consent and verify whether future non-essential tracking and data collection activities stop as appropriate.

## Test 6 — Consent persistence

Refresh the website and navigate to additional pages. Verify that the visitor's consent preferences are retained and respected.

## Test 7 — Website functionality

Identify whether essential website features remain functional when non-essential technologies are rejected.

## Test 8 — Global Privacy Control (GPC)

Where your available tools permit, visit the website using a fresh browser session with Global Privacy Control enabled.

Identify whether the website recognizes the GPC signal and adjusts its consent settings, applicable opt-out preferences and third-party technology behavior accordingly.

Compare the website's behavior with and without GPC enabled.

Report the observed differences and any potential issues. Do not assume that GPC recognition is legally required for every website or that it requires blocking every non-essential technology.

## Important testing considerations

- Use fresh, isolated browser sessions when comparing independent consent scenarios.
- Document the geographic location from which the website was tested, if known.
- Distinguish between scripts being downloaded, scripts being executed, personal data being transmitted and information being stored on the visitor's device.
- Do not assume that a script is improperly loading simply because it was detected before consent. Evaluate its purpose, behavior and applicable consent configuration.
- Do not assume that the absence of cookies means that no personal information is being collected or shared.
- Document which tests were successfully completed and which could not be performed.
- Report observed behavior and potential issues without making definitive legal compliance determinations.

- Some providers offer consent modes that let their scripts run before consent without setting tracking cookies. For example, with Google Consent Mode in advanced mode, Google scripts load and send cookieless requests before consent, and set cookies only after consent is given. Inspect cookieless requests and consent signals as well as cookies. The absence of cookies does not mean the absence of data transmission.
- If the website loads Google Tag Manager or another tag manager, flag it. Tag managers can load additional tags and scripts that do not appear in the page source.
- Include the do-it-yourself testing guide described in `references/report-template.md`, so the user can repeat these tests in their own browser.

## Service-level disclosures

Does the cookie banner provide details about each third-party Service identified on the website?

For example, in addition to controlling Google Analytics based on the visitor's consent preferences, does the consent solution provide disclosures explaining what Google Analytics does, what personal information it collects and its purpose?

Encourage website owners to provide comprehensive, service-level disclosures within their consent solution so visitors can make informed decisions.

Identify any Services detected during the audit that are not disclosed within the consent solution. Flag these as potential disclosure gaps and opportunities for improvement. Specific legal disclosure requirements vary by applicable law. Report the gaps you observe without making legal determinations.

## Consent choice design

Does the consent banner provide visitors with clear, accessible and meaningful privacy choices?

For websites presenting an opt-in consent model, identify whether the banner provides clearly visible accept and deny buttons. Evaluate whether rejecting non-essential technologies is as easy as accepting them.

For websites presenting an opt-out consent model, identify whether visitors are provided with clear and accessible mechanisms to exercise applicable opt-out rights.

Flag design practices that may manipulate or discourage visitors from exercising their privacy choices, such as misleading button labels, unequal button prominence or unnecessary steps required to reject or opt out. Encourage website owners to make privacy choices equally accessible and easy to understand.
