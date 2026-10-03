# Decline classes and retry limits

Re-check any row older than 6 months. Card-network figures here come from acquirer and processor pages, not from the networks' own rulebooks, which are not public; say so when citing them. Where sources disagree the row is marked "conflicting sources". If a figure cannot be confirmed for the user's processor, print beside it: "check your processor's current network retry limits".

## Classes

| Class | Covers | Action |
|---|---|---|
| Never retry | Visa category 1: 04, 07, 12, 14, 15, 41, 43, 46, 57, R0, R1, R3. Mastercard merchant advice codes 03 and 21. Processor hard declines, for example incorrect_number, lost_card, pickup_card, stolen_card, revocation_of_authorization, revocation_of_all_authorizations, highest_risk_level, transaction_not_allowed | Ask for a new payment method; no further attempts on this card |
| Customer must act | authentication_required (strong customer authentication); Visa category 3 "cannot approve with these details", for example 54 expired card, 55 wrong PIN, 82, N7, 1A, 70 | Send an update or authenticate link on day 0; use an account updater if the processor offers one; retry only after the details change |
| Wait and retry | Visa category 2 "cannot approve at this time", for example 51 insufficient funds, 61, 65, 91, 96; Visa category 4, all other codes, including 05 do not honor; processing errors | Spaced retries within the caps below |
| Store-billed | Charges made by the App Store or Google Play | Not under the merchant's retry control; see `store-billing.md` |

Code 14 sits in both Visa category 1 and category 3; treat it as never retry. authentication_required is on one processor's hard-decline list because it cannot succeed without the customer; this plugin puts it under "customer must act", which also means no blind retry.

## Caps

| Id | Network | Limit | Status | Read | URL |
|---|---|---|---|---|---|
| VISA-CAT | Visa | Category 1 codes: no reattempt at all; a fee applies to each reattempt | in force per acquirer page | 2026-10-03 | https://docs.adyen.com/development-resources/raw-acquirer-responses/visa-integrity-fees |
| VISA-CAP | Visa | Categories 2 to 4: a capped number of reattempts per card in 30 days. **Sources disagree**: 15 (Adyen page; Evolve page updated 2025-10-30) versus 20 (PayPal page dated 2026-05-15). Plan to 15, the lower figure, and confirm with your processor | conflicting sources | 2026-10-03 | https://docs.adyen.com/development-resources/raw-acquirer-responses/visa-integrity-fees ; https://developers.getevolved.com/enterprise/docs/visas-processing-integrity-fee-program ; https://www.paypal.com/us/brc/article/avoid-excessive-retries-penalties |
| MC-MAC | Mastercard | Merchant advice code 03 (do not try again) and 21 (recurring payment cancelled): stop | in force per acquirer page | 2026-10-03 | https://www.paypal.com/us/brc/article/avoid-excessive-retries-penalties |
| MC-CAP | Mastercard | Fees start after 10 attempts on one card in 24 hours, or after 35 in 30 days (one acquirer source; Mastercard text not read) | in force per acquirer page | 2026-10-03 | https://www.paypal.com/us/brc/article/avoid-excessive-retries-penalties |
| MC-RETRY-AFTER | Mastercard | Advice codes that ask for a retry after a set time | unverified (not read at build); do not cite timings | — | — |
| PROC-HARD | Stripe (example of one processor) | The hard-decline list in the first table plus authentication_required; its documented default schedule is 8 tries within 2 weeks. State this as that processor's default, never as advice | in force | 2026-10-03 | https://docs.stripe.com/billing/revenue-recovery/smart-retries |

## Retry-schedule check

Flag, with counts (ids only when the user asks):
1. Any attempt after a never-retry code → "retry after never-retry code".
2. Any card with more attempts than the lowest applicable cap in the window (Visa: 15 in 30 days, the planning figure from VISA-CAP; Mastercard: 10 in 24 hours or 35 in 30 days) → "over network cap".
3. Retries on customer-must-act declines before the details changed → "blind retry".

A wait-and-retry decline (including 05 do not honor) retried within the caps is **not** flagged.

## Recovery by class

Per class: recovered by retry, recovered after a card update, recovered by customer action, lost. Each as a rate with n and a Wilson interval, plus median days to recovery. Mix shares (class counts as a share of all failures) carry no interval.
