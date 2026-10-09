# Redesigned flow spec (part d of the audit)

Fill one row per screen with the user's own facts (their offer, their page names, their plan). Leave a slot in square brackets only for a fact the user did not give, and name it. The team writes the final words.

| Screen | Purpose | Content | Cancel control | Logged event |
|---|---|---|---|---|
| 1. Entry | Start from the plan or billing page | "Cancel subscription" link or button | Is the entry | cancel_started |
| 2. Optional reason | Learn the reason group (group names on screen, never R-numbers) | Reason options from `reason-offer-map.md`, plus "Skip" | "Continue to cancel" always active | reason_selected or reason_skipped |
| 3. One offer (only if the reason group has one) | Present one alternative | The user's offer as given: price during the offer, how long, price after (a slot only for a term not given) | "Cancel subscription" beside "Accept", same size class (California: label "click to cancel" or a similar phrase, CA-e2) | offer_shown, offer_accepted, offer_declined |
| 4. Confirmation | Finish | [END_DATE], what happens to data, how to restart | Is the final step | cancel_confirmed |
| Receipt | Durable record | Email with date and time of the request and the end date | — | receipt_sent |

Store-billed subscriptions replace screens 3–4 with the store's own management page; see `store-billing.md`.

Events to log for later measurement (feed the save-offer analysis): account id, timestamp, reason group, offer id and terms, accept or decline, paused flag and pause end date, holdout flag, cancel_confirmed timestamp. A holdout is a random share of sessions that see no offer; 10% is an editable default.

If the customer chooses pause or downgrade, the screen states the date the pause ends or the new price starts, and what happens then.
