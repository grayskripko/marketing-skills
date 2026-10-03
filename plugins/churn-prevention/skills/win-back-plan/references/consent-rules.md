# Consent rules for contacting cancelled subscribers

Re-check any row older than 6 months. Not legal advice. Jurisdictions: US, EU, UK.

| Id | Rule | Summary | Status | Read | URL |
|---|---|---|---|---|---|
| US-CANSPAM | CAN-SPAM Act (FTC compliance guide) | Commercial email needs a clear way to opt out that works for at least 30 days after sending; opt-outs honoured within 10 business days; the message identifies itself as an ad and carries a valid postal address; no misleading subject lines | in force | 2026-10-03 | https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business |
| UK-PECR | Privacy and Electronic Communications Regulations, reg. 22 (ICO guidance) | Marketing email to individuals needs consent, or the "soft opt-in": details obtained during a sale or negotiation, marketing only similar products or services from the same sender, and a clear chance to opt out when the details were collected and in every message. The ICO notes the guidance is under review after the Data (Use and Access) Act | in force | 2026-10-03 | https://ico.org.uk/for-organisations/direct-marketing-and-privacy-and-electronic-communications/guide-to-pecr/electronic-and-telephone-marketing/electronic-mail-marketing/ |
| EU-EPRIV | ePrivacy Directive 2002/58/EC, Art. 13(2), as implemented by each member state | Same structure as the UK soft opt-in: existing customers, own similar products, opt-out offered at no cost at collection and in every message; otherwise prior consent | unverified (EUR-Lex text did not load on the read date; national rules vary) | 2026-10-03 | https://eur-lex.europa.eu/eli/dir/2002/58/oj |

## How win-back-plan applies them

- A subscriber is eligible for email only if the export marks consent, or the soft opt-in conditions are met and the user confirms an opt-out was offered.
- Anyone who opted out or asked not to be contacted is suppressed in every region.
- Business-to-business contacts: national rules differ; ask the user which rule their counsel applies and suppress when unknown.
- When the consent field is missing, the plan stops at segment counts and lists "consent status" under Not checked.
