# Airbnb Cancellations

Calculate what I owe this guest if they cancel, and show which dates and policy apply.
For Airbnb home hosts and co-hosts working from pasted reservation text, receipts or exports. Needs booking and cancellation timestamps, listing timezone, check-in and checkout, reservation policy. Refund calculations additionally need the payment breakdown; deadline questions do not need prices or receipts. No account, keys, paid API or setup required.

| Skill | Ask | Result |
|---|---|---|
| airbnb-refund-calculation | What do I still owe this guest? | Itemized refund, retained charges and remaining settlement, with formulas |
| airbnb-cancellation-deadlines | Which policy and dates apply? | Reservation policy, exact local cutoffs and the cancellation branch |

Use the calculation skill when amounts matter; use the deadline skill when choosing or explaining a cutoff. Both preserve the policy attached to the booking. Short stays, monthly stays, Italy booking-date rules, California grace, South Korean Strict rules and German loss disputes are covered. If monthly after-check-in terms conflict, the result identifies the exact reservation breakdown needed.

Paste redacted facts and any cancellation-preview or refund-confirmation text. For a refund calculation, include nightly prices after discounts, cleaning, taxes, Airbnb guest fees, amount collected, refunds already made and any promised extra refund. A chat message about canceling is distinct from a confirmed platform cancellation.

The skills use embedded policy knowledge. When current wording needs verification, the assistant fetches public Airbnb Help Center pages cited in the references, official Help Center links needed for that question, and Airbnb robots.txt. It sends no booking details in requests, performs no account access, and makes no reservation or payment changes. Paths disallowed by robots.txt are not fetched. No telemetry or plugin storage.

Sources were verified on 2026-10-11. Planned submission window: 2026-10-21. Source dates and policy conflicts are in each skill's linked references. See [PRIVACY.md](PRIVACY.md) and [BUILD-NOTES.md](BUILD-NOTES.md).
