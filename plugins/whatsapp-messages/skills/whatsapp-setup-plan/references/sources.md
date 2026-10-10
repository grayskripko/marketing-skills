# Sources and scope

Read 2026-10-09. Source-backed statements below are separate from editorial rules of thumb.

- Export chat produces a text snapshot, optionally with media; it is not a restorable backup. Inspect the actual file rather than assume timestamp layout or a universal message cap. Official help: https://faq.whatsapp.com/1180414079177245/ . Opened read 2026-10-09: browser extraction was empty; direct HTTP returned the help page. Export details also agree with the supplied topic research’s indexed official help reading.
- Official Cloud API supports business messaging and webhooks, not a general consumer-inbox mirror. Setup guide: https://developers.facebook.com/documentation/business-messaging/whatsapp/get-started . Opened read 2026-10-09: browser extraction failed; direct HTTP succeeded. Account-specific onboarding remains to be checked.
- Existing Business App onboarding is documented; do not assume a new number or deleting an account is required. https://developers.facebook.com/documentation/business-messaging/whatsapp/embedded-signup/onboarding-business-app-users . Opened read 2026-10-09 by direct HTTP; account eligibility remains unverified.
- Recipient opt-in, opt-out compliance, approved templates for initiation/outside the 24-hour reply window, and clear human escalation for automated replies: https://whatsappbusiness.com/policy/ . Live policy read confirms these conditions.
- Rates depend on market/category and chargeable delivered messages; verify current rates before estimating. https://whatsappbusiness.com/products/platform-pricing/ . Opened read 2026-10-09. Service messages and eligible utility replies are free; free-entry-point conditions and volume tiers affect chargeable volume. No numeric rate is adopted here.
- Current Platform terms incorporate additional Meta terms; AI-provider eligibility is unresolved, not certified by this package. https://www.whatsapp.com/legal/WhatsApp-Terms-for-WhatsApp-Business-Platform and https://www.facebook.com/legal/Meta-Terms-for-WhatsApp-Business-Platform . Opened read 2026-10-09: the WhatsApp terms were readable; browser extraction of incorporated Meta terms redirected to login, while direct HTTP returned a page. HTTP success alone does not certify the proposed AI use.
- Unofficial browser clients can lead to account blocking. https://github.com/wwebjs/whatsapp-web.js . Live maintainer README warns of this risk. Authentication design: https://wwebjs.dev/guide/creating-your-bot/authentication .
- Baileys is an unofficial WebSocket client; installation, pairing and saved authentication are required. https://github.com/WhiskeySockets/Baileys and https://baileys.wiki/ . Opened read 2026-10-09; no runtime integration was tested.
- A representative unofficial MCP bridge keeps a local message database and warns about prompt injection/exfiltration: https://github.com/lharries/whatsapp-mcp . Opened read 2026-10-09; no MCP is bundled.
- Export possession does not remove privacy obligations. https://www.whatsapp.com/legal/privacy-policy and https://www.whatsapp.com/legal/terms-of-service .

Business-use restrictions and country-specific exceptions are also in the Business Messaging Policy above; opt-in and templates do not establish permitted use. Opened read 2026-10-09.

Editorial rules of thumb: deliverable first, source locations, participant labels, no network, file inspection before parsing, no guessed owners/deadlines, and comparison before integration. None is a claimed law or quantitative finding.

- On-Premises API is retired; do not offer a new deployment. https://developers.facebook.com/docs/whatsapp/on-premises/sunset/ . Opened read 2026-10-09: browser extraction failed, direct HTTP succeeded; supplied topic research records the retirement. No migration was tested.
