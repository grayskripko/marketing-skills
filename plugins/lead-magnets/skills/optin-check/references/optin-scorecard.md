# Opt-in scorecard OP-01 to OP-20

Verdicts: pass, fail, ask (a fact the user has not given decides it) or not checked (the text for that row is missing). Quote the line that decided each verdict. Register ids point to `consent-register.md` (CR), `proof-and-urgency.md` (PU) and `sender-rules.md` (SR). Consent rows apply for the regions given; with no region, run all three and say so.

## Promise and proof

| Id | Check | Basis |
|---|---|---|
| OP-01 | The headline tells the reader what result they get and in what form (checklist, calculator, report). | heuristic of this plugin |
| OP-02 | Each "what you get" bullet maps to a section of the asset (the LB-10 promise list). Without the list: not checked. | heuristic |
| OP-03 | Any subscriber, download or customer count equals the user's real figure. Unknown: ask for it. An inflated count is a misleading claim. | PU-01, PU-06 |
| OP-04 | Testimonials are real, from real customers, attributed, and any material connection is disclosed. | PU-02, PU-03, PU-06 |
| OP-05 | A no-cost claim is honest: whatever it requires (booking a call, entering a card, starting a trial) appears right beside it. | PU-01, PU-04 (an analogy) |
| OP-06 | No false urgency or scarcity: countdowns that reset, "spots left" that are not true, deadlines that do not exist. | PU-05, PU-06 |
| OP-07 | The page says how and when the asset arrives; with double opt-in, it says to confirm and what to do if no email comes. | heuristic |

## Form (kept short: only what the capture path needs)

| Id | Check | Basis |
|---|---|---|
| OP-08 | Every field has a stated use before the next step; a phone field only when a call is the next step. | CR-05; NN/g Whitenton 2016-05-01 |
| OP-09 | Optional fields are marked as optional. | NN/g Whitenton 2016-05-01 |
| OP-10 | Each field has a visible label, not placeholder text alone; in HTML, the email and name inputs declare their purpose for autofill. | NN/g Sherwin 2014-05-11; WCAG 2.2 SC 3.3.2, SC 1.3.5 |
| OP-11 | No dialog or overlay hides the form or the page content on arrival, on mobile in particular. | Google Search Central, "Avoid intrusive interstitials and dialogs", updated 2025-12-10, read 2026-10-03 |

## Consent and notice (rows chosen by region)

| Id | Check | Basis |
|---|---|---|
| OP-12 | Marketing consent is its own unticked box that the person must actively tick. | CR-01, CR-06, CR-07 |
| OP-13 | EU and UK individuals receive the asset whether or not they tick any marketing box. | CR-02 (plugin default, cautious reading) |
| OP-14 | One box per purpose or stream; no single tick that covers marketing and sharing with other companies. | CR-03 |
| OP-15 | The form says who collects the data and links the privacy notice. California notice at collection only when the company meets a CCPA threshold; otherwise this part is an ask row. | CR-05, CR-10 |
| OP-16 | "You can unsubscribe at any time" is not presented as if it were consent. | CR-01 |

## Thank-you page and confirmation email

| Id | Check | Basis |
|---|---|---|
| OP-17 | The thank-you page delivers or links the asset at once, says what happens next and offers one next step. | heuristic |
| OP-18 | Primary-purpose test on the confirmation email: if a reasonable reader would take the subject line or opening as advertising, the message is commercial and needs accurate sender details, an honest subject, a valid postal address, a clear opt-out honoured within 10 business days, and identification as an advertisement unless the recipient gave prior affirmative consent. A delivery email with a small mention in the footer can stay transactional; say which way it falls and suggest counsel when it is close. | CR-09 |
| OP-19 | UK and EU mail: the sender's identity is not hidden and a valid address to stop messages is given. | CR-06, CR-08 |
| OP-20 | Mailbox provider rules, for the user to confirm with their sending tool (the page text cannot show them, so ask unless confirmed): spam rate below 0.3% for every sender; for bulk senders, SPF, DKIM and DMARC, one-click unsubscribe plus a visible link, and unsubscribes honoured within 2 days at Yahoo. | SR-01, SR-02 |

## Output format

Counts per group, then: id | check | verdict | quoted evidence | register id. Rewrites follow for failing rows only.

## Worked example

Form: email, phone, company size, a pre-ticked "send me offers" box; visitors from the UK and EU; nothing else given.
- Fail: OP-08 (phone and company size have no stated use; no call is promised), OP-12 (the box is ticked).
- Ask: OP-13 (does the download work without the tick?), OP-15 (who collects the data, where is the notice?), OP-03 (only if the page shows a count), OP-07 (how does the asset arrive?).
- Not checked (14): OP-01, OP-02, OP-04 to OP-06, OP-09 to OP-11, OP-14, OP-16 and OP-17 to OP-20 (no page, box wording, thank-you page or email text). 2 fail + 4 ask + 14 not checked = 20.
- Rewrites: "Work email (we send the checklist here)" and "☐ Also send me product news. Optional; the checklist arrives either way."
