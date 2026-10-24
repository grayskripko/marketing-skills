# Patreon official knowledge register

All pages below loaded with article content on **2026-10-11**. “Updated” is the date displayed by Patreon; it is distinct from the read date. These rules concern Patreon memberships, not digital-product purchases. Exact CSV headings come from the supplied export.

| Official source / displayed update | Deciding knowledge | Read |
|---|---|---|
| [Relationship manager billing statuses](https://support.patreon.com/hc/en-us/articles/204606025-Relationship-manager-billing-statuses) — 2026-04-07 | Active includes scheduled charges. Retrying suspends access. Paid-subscription Canceled is displayed at access expiry. A non-annual refunded bill does not itself cancel renewal; use the specific annual-refund rule below. Fraud has no automatic retry. Gifted by you/others identifies redeemed active gifts. | 2026-10-11 |
| [Track your members' benefit eligibility status](https://support.patreon.com/hc/en-us/articles/35894742951565-Track-your-members-benefit-eligibility-status) — 2025-04-24 | Current or previous month; monthly and annual members included. Eligible soon is a future renewal before month-end. New includes rejoined members; Continuing covers ongoing members. Tier filters and CSV export available. | 2026-10-11 |
| [How to use your Relationship manager](https://support.patreon.com/hc/en-us/articles/360045516212-How-to-use-your-Relationship-manager) — 2026-09-11 | Export inherits filters. Status describes the latest attempted charge. Last Charge Date is an attempt, while annual CSV reflects membership start. Next Charge Date is scheduled renewal. Cancel Date is access end. Charge frequency distinguishes annual rows. Lifetime may lag; email may be withheld by choice. Payment failed can become free after roughly 30 days. | 2026-10-11 |
| [Managing members with custom pledges](https://support.patreon.com/hc/en-us/articles/360044376211-Managing-members-with-custom-pledges) — 2026-06-17 | No tier pledge has no tier rewards. Paying more does not upgrade tier. Creator cannot assign a member's tier. No-tier access is to All members or Paid members only posts, not a tier inferred from price. | 2026-10-11 |
| [Find my members' shipping addresses](https://support.patreon.com/hc/en-us/articles/204606015-Find-my-members-shipping-addresses) — 2026-07-13 | Enable Shipping address collection in tier Advanced settings. Address is in Contact information or exported CSV. Absence can mean no supplied address and physical-benefit opt-out; it does not prove payment failure. | 2026-10-11 |
| [FAQ: Fan gifting](https://support.patreon.com/hc/en-us/articles/31345081474189-FAQ-Fan-gifting) — 2026-07-10 | Patreon merchandise is not earned through gift-only membership; recipient must make an attached payment. Gift purchase earnings precede redemption, so proceeds do not prove recipient access. Fan-purchased gifts have a 90-day redemption window. | 2026-10-11 |
| [Track delivery with Benefits feature](https://support.patreon.com/hc/en-us/articles/360004710212-Track-delivery-with-Benefits-feature) — 2026-10-08 | Gifted accounts absent from Benefits tracking. Frequencies: monthly or one-time; per-creation offers one-time only. Annual members receive tier-linked monthly benefits. Due and Completed track delivery. Subscription creators can deliver to currently active members or for prior-month successful payments. Legacy billing migration deadline is November 1, 2026; automatic migration can pause billing until multiplier/prices configured. | 2026-10-11 |
| [Gifting memberships to your fans](https://support.patreon.com/hc/en-us/articles/31345065123597-Gifting-memberships-to-your-fans-creator-to-fan-gifts) — 2026-07-19 | Canceling a redeemed gift ends gift access immediately, before planned expiry; separate paid access needs account evidence. Redeemed gift access and Benefits tracking are separate; gift accounts lack tracking until paid conversion. Same guide gives conflicting billing-continuation and pause/resume accounts for existing subscribers, so their exact schedule needs account evidence. | 2026-10-11 |

| [How to manage refunds for your fans](https://support.patreon.com/hc/en-us/articles/39611657224717-How-to-manage-refunds-for-your-fans) — 2026-09-11 | Full annual refund ends membership/access immediately; partial annual refund ends access after the refund month. Rejoining is a new immediately charged membership. This specific rule takes precedence over the general Refunded billing-status summary. | 2026-10-11 |

## Decision matrix

| Input signal | Current access / monthly delivery decision |
|---|---|
| Active payment | Can have access before a charge; inspect month eligibility for a paid-month policy |
| Eligible soon | Plan only; confirm the successful renewal before paid-month fulfillment |
| Annual, old charge | Not a monthly exclusion; use coverage or month eligibility |
| Retrying / failed / fraud | Reconcile failed attempt and current access; do not label a payment successful |
| Canceled now, prior month eligible | Historical eligibility can satisfy a prior-month delivery policy; an earned digital reward needs an accessible delivery route |
| Non-annual refunded bill | Check bill/month and creator terms; refund alone does not cancel renewal |
| Annual full refund | Membership/access ended immediately; do not assume renewal or rejoining |
| Annual partial refund | Access ends after the refund month; obtain refund date if absent |
| Canceled redeemed gift | Gift access ended immediately; original expiry is superseded, separate paid access needs evidence |
| Redeemed gift | Tier access and delivery tracking differ; treat merchandise accrual separately |
| No tier | No tier-specific rewards, regardless of pledge amount |
| Address absent | A fulfillment exception, not proof of payment status |
| Completed | Prevent repeat delivery for this member + benefit + period only |

Annual access termination and renewal-setting evidence are separate. A Refunded label alone does not establish the setting; if renewal is specifically asked about, identify any missing cancellation/renewal evidence rather than predict a future charge.

## Scope and upkeep

The creator's benefit terms decide inheritance, delivery cutoff and creator-managed physical rewards. Join keys, duplicate handling and the ready/awaiting-renewal labels are workflow conventions, not Patreon CSV fields. Never turn a filtered list into an audience-wide total.

For a fulfillment period affected by the November 1, 2026 legacy-billing migration, use the creator’s supplied billing notice and configuration to establish whether billing was migrated, paused or resumed. The platform's gifting guide contains conflicting explanations of existing subscribers' billing continuation versus pause/resume; this package uses only redeemed access and merchandise/tracking facts and makes no gift billing-timeline prediction.
