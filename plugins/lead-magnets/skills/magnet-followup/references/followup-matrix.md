# Follow-up matrix

What each sign-up may receive, by region, subscriber type and the consent the form recorded. Register ids point to `consent-register.md` (CR) and `sender-rules.md` (SR). Checks, not legal advice.

## Cells

| Region | Subscriber | Consent recorded | Allowed after delivery | Basis |
|---|---|---|---|---|
| EU | individual | delivery only (no box ticked) | the asset only (one delivery message); no promotion and no follow-up tips | CR-02, CR-06 |
| EU | individual | ticked stream X | stream X only, with an opt-out in each message | CR-01, CR-03 |
| EU | individual who bought earlier | delivery only | the customer exception may cover similar own products if an opt-out was offered at collection: confirm with counsel; in France an account without a purchase does not count | CR-06 |
| EU-DE | individual | ticked stream X | as EU; keep the confirmed double opt-in click as proof (case law, not statute) | CR-12 |
| EU | company address (legal person) | any | national law decides: ASK by member state | CR-06 |
| UK | individual or sole trader | delivery only | the asset only; a download is not treated as a sale or negotiations, so the soft opt-in is not assumed: confirm with counsel | CR-07 |
| UK | individual or sole trader | trial sign-up, quote request or request for details recorded | similar products under the soft opt-in, if an opt-out was offered at collection and is in every message | CR-07 |
| UK | individual | ticked stream X | stream X only | CR-07 |
| UK | corporate subscriber | any | allowed, with sender identity and a working opt-out | CR-07, CR-08 |
| UK | any (charity soft opt-in) | n/a | applies to charities only; not to commercial senders | CR-07 |
| US | any, B2B included | none needed | allowed under CAN-SPAM duties; honour opt-outs | CR-09, SR-03 |
| US-CA | individual | any | as US, plus notice at collection if the company meets the thresholds: ASK | CR-10 |
| any | any | hand-raise (reply, demo or call request, top scorecard band, calculator result above the user's level) | a person answers the request itself; that answer is not marketing | heuristic |
| other | any | any | ASK | CR-11 |

## Message jobs (titles only)

1. Deliver: the asset, or the link to it, and nothing else in the subject or opening (keeps the message transactional under the primary-purpose test, CR-09).
2. Help them use it: one tip or worked case for the asset itself, only in cells where marketing is allowed or the person ticked a stream that covers it (never in a "delivery only" cell for EU or UK individuals).
3. One next step tied to the offer, only in cells that allow promotion.
4. Reading channel for readers who are not ready: a low-frequency newsletter or digest they chose; never a sales push.

No subject lines, wait times, angles or body copy.

## Cadence ceiling, exits, hand-to-person rule

- Cadence ceiling: an upper limit per week that the user sets; this plugin's default is one promotional message a week per stream (heuristic, editable).
- Exits: opt-out (immediate), the conversion is reached, or a set number of messages with no click (the user picks the number).
- Hand to a person when a reader raises a hand: replies, books or asks for a demo, lands in the top band of a scorecard, or gets a calculator result above a level the user sets. The user sets a response-time target; the plugin does not invent one.

## Suppression

Follow `sender-rules.md`: the strictest deadline that applies (2 days for bulk mail to Yahoo addresses; 10 business days as the US legal limit), applied across all lists; an opted-out address is never re-added; no bought, rented, scraped or appended addresses.

## Fields to store

| Field | Why |
|---|---|
| consent wording version (or a copy of the text shown) | proof of what the person saw, CR-04 |
| timestamp of the sign-up | proof of when, CR-04 |
| source page or form id | proof of how and where, CR-04 |
| region or country as declared | chooses the matrix row |
| boxes ticked, one field per stream | proof per stream, CR-03 |
| subscriber type when known (individual or company address) | chooses the matrix row |
| opt-out date | suppression |

Store only what links the record to the processing (EDPB 05/2020 para 106). Counting events: the analytics events `generate_lead` on form submit and `qualify_lead` when sales accepts the lead, as listed among Google Analytics lead-generation events (support.google.com/analytics/answer/9267735, read 2026-10-03). A thank-you page view is a weaker count: reloads and return visits can fire it twice. Do not read opens as interest. Under Apple Mail Privacy Protection, messages are fetched in the background, which registers an open whether or not anyone looked at it (apple.com/legal/privacy/data/en/mail-privacy-protection, dated 2025-12-12, read 2026-10-03).

## Consent-proof audit (optional)

On a pasted export, count by row id:
- rows with no consent wording version;
- rows with no timestamp;
- rows with no source page;
- rows flagged for marketing but with no ticked box recorded;
- rows with an opt-out date that are still flagged mailable.
Print each as k/n of all rows, list at most 10 ids per check, and never print an email address or name. If the id column holds email addresses, names or phone numbers, use row numbers (row 1, row 2 …) instead and say so. A row can fail several checks; say so under the table.
