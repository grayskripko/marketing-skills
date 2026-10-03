# Sender rules

Rules that mailbox providers and laws set for the messages that follow a sign-up. Checks, not legal advice; the user confirms the technical items with their sending tool. Rows older than 6 months print "re-check this rule".

| Id | Applies to | Rule (paraphrase) | Source | Read |
|---|---|---|---|---|
| SR-01 | mail to Gmail addresses | Every sender: SPF or DKIM, valid forward and reverse DNS, TLS, spam rate in Postmaster Tools below 0.3% (Google's monitoring advice is to stay below 0.10%). Senders of more than 5,000 messages a day to Gmail: SPF and DKIM, DMARC (policy "none" is accepted) with From alignment, and marketing or subscribed mail must support one-click unsubscribe and show a visible unsubscribe link in the body. Applied from 2024-02-01. The page sets no deadline for honouring unsubscribes. | Google "Email sender guidelines", support.google.com/a/answer/81126 | 2026-10-03 |
| SR-02 | mail to Yahoo addresses | Every sender: SPF or DKIM, valid DNS, spam rate below 0.3%. Bulk senders: SPF and DKIM, DMARC at least p=none and passing, alignment, a working list-unsubscribe header with one-click (the RFC 8058 POST method is highly recommended), a visible unsubscribe link, and unsubscribes honoured within 2 days. Yahoo publishes no numeric bulk threshold: ASK, or apply the bulk rules when volume is high. | Yahoo Sender Hub, sender requirements and recommendations, senders.yahooinc.com/best-practices | 2026-10-03 |
| SR-03 | US commercial email | Opt-outs honoured within 10 business days; the opt-out mechanism keeps working for 30 days or more after the send; no fee or extra data to opt out. | CR-09 | 2026-10-03 |
| SR-04 | UK and EU marketing email | Sender identity shown and a valid address to stop messages. | CR-06, CR-08 | 2026-10-03 |

## Suppression rule used in plans

Use the strictest deadline that applies to the list: when any recipients use Yahoo addresses and the sender is a bulk sender, honour opt-outs within 2 days; CAN-SPAM's 10 business days is the legal outer limit in the US. Apply an opt-out across every list the company runs, and never re-add an address that opted out. No bought, rented, scraped or appended addresses.
