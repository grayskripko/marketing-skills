# Payment-problem message skeletons

Neutral, no blame, one action per message. Slots in square brackets; the team writes the final copy. The link slot is [UPDATE_LINK]; never paste real links, tokens or card details into a template.

| Moment | Class | Subject idea | Slot 1 | Slot 2 | Slot 3 |
|---|---|---|---|---|---|
| Before expiry (about 30 days) | expiring card | Your card on file ends soon | which plan, [CARD_ENDING] last four only | what happens if nothing changes | [UPDATE_LINK] |
| Before renewal | annual plans; where rules require a reminder (CA-h; UK-DMCC from January 2027) | Your plan renews on [RENEWAL_DATE] | price and term | how to change or cancel | link to account page |
| Day 0 | soft decline | We couldn't take this month's payment | we will try again on [RETRY_DATE] | access stays on until [GRACE_END] | [UPDATE_LINK] (optional) |
| Day 0 | customer must act | Action needed to keep your plan | what to do (update or confirm with the bank) | access until [GRACE_END] | [UPDATE_LINK] |
| Day 0 | never retry | Please add a new payment method | no further attempts on the old card | access until [GRACE_END] | [UPDATE_LINK] |
| Mid-grace | any open case | Reminder: payment still pending | date access changes | how to pause instead | [UPDATE_LINK] |
| End state | any | Your plan is now [END_STATE] | what remains (data, account) | how to restart | link to account page |

At most four messages between day 0 and the end of grace (heuristic). Each message also offers a plain way to cancel or pause. Never include card numbers; show at most the card brand and last four digits if the user's system already does.

End state after grace, one of: cancel, mark unpaid with access removed, or pause. Print the trade-off of each (revenue counted, data kept, ease of return).
