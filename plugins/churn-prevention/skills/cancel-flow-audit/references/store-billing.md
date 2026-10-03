# Store billing: App Store and Google Play

Re-check any row older than 6 months. When the store bills the customer, the store runs payment retries and the cancellation screen. The merchant controls only in-app messages, access during the grace period or hold, its own server's handling of the status it receives, and the offers the store lets it configure.

| Id | Store | Rule | Status | Read | URL |
|---|---|---|---|---|---|
| APL-CANCEL | App Store | Cancellation of App Store subscriptions runs in the customer's Apple account settings; the merchant reviews only the in-app path to the subscription management page and its own messages | in force | 2026-10-03 | https://developer.apple.com/documentation/retentionmessaging |
| APL-RETRY | App Store | After a failed renewal the subscription enters billing retry, and the store tries to collect for up to 60 days. Recovery after the grace period starts a new billing date | in force | 2026-10-03 | https://developer.apple.com/documentation/storekit/reducing-involuntary-subscriber-churn |
| APL-GRACE | App Store | Optional billing grace period with full access while the store retries: weekly plans 3 or 6 days (a longer setting is capped at 6); monthly and longer plans 3, 16 or 28 days. Not available for monthly plans with a 12-month commitment. Changes take up to 24 hours and affect upcoming renewals | in force | 2026-10-03 | https://developer.apple.com/help/app-store-connect/manage-subscriptions/enable-billing-grace-period-for-auto-renewable-subscriptions |
| APL-LINK | App Store | The app may show its own message asking the customer to fix billing, and may link to the account's payment page | in force | 2026-10-03 | https://developer.apple.com/documentation/storekit/reducing-involuntary-subscriber-churn |
| APL-RM | App Store | Retention Messaging API: after the customer taps cancel in Apple's subscription page, a confirm-cancellation screen can show one message the developer configured (text, image, switch plan or promotional offer) beside Apple's own cancel and keep buttons. Pre-release, access by request; shown on iOS and iPadOS 15.1 or later | pre-release, access by request | 2026-10-03 | https://developer.apple.com/documentation/retentionmessaging |
| APL-ARG | App Store | App Review Guidelines, section on auto-renewable subscriptions: cited by name only, no section quoted | unverified (not re-read at build) | — | https://developer.apple.com/app-store/review/guidelines/ |
| GP-CANCEL | Google Play | Google Play subscriptions are cancelled in the Play account; same limit as APL-CANCEL | unverified (not re-read at build) | — | https://support.google.com/googleplay/android-developer/ |
| GP-HOLD | Google Play | Since 1 December 2025 the default account hold is 60 days minus the grace period the developer set; plans on the old 30-day default switched automatically, plans with custom values were not changed. Google says the formula may change | in force | 2026-10-03 | https://support.google.com/googleplay/android-developer/answer/16631229 |
| GP-GRACE | Google Play | Grace-period options and default length | unverified (not stated on the page read); ask the user for their configured value | — | — |

## What the skills do with store-billed accounts

- Cancel-flow audit: review only the in-app path to the store's management page and any in-app message; the store's own screens are outside the merchant's control. Any store offer surface (APL-RM) follows the same one-offer rule as the web flow.
- Dunning plan: no merchant-side retry schedule. Plan the grace-period choice, access during grace or hold, and in-app messages pointing to the store's payment page.
