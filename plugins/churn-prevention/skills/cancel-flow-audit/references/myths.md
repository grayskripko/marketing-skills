# Claims to correct

When the user states one of these, name it, give the short correction and the measurement that settles it on their own data, in one or two sentences. No figures are quoted for or against.

| Claim | Correction | How to check on your own data |
|---|---|---|
| "The FTC click-to-cancel rule is in force" | It was vacated on 8 July 2025; the FTC is at the advance-notice stage (March 2026) with no rule text. ROSCA and state laws such as California §17602 still apply | The dated rule rows in the cancel-flow audit |
| "There is a normal save, pause-return, recovery or churn rate to aim for" | No figure is quoted. Rates differ with price, billing channel and how the save is counted | Your own baseline, measured against a holdout |
| "Our save rate proves the offer works" | Accepted ÷ shown counts people who would have stayed anyway and people who leave when the discount ends | Share paying full price after the discount, against a holdout (save-offer economics) |
| "Extra cancel steps are harmless if people stay" | Friction-based "saves" are the conduct regulators act on, and they inflate the save rate with people who leave or dispute the charge later. This plugin does not design them | CF checks, then the holdout comparison |
| "A fixed share of all cancellations are failed payments" | The split differs by business | Count your own: failed payment, chosen, unknown (dunning plan, step 0) |
| "Paused customers come back" | Some resume, some cancel when the pause ends | Pause outcome table (save-offer economics) |
| "Do not honor means never retry" | It is a generic decline in Visa's retry-limited group (category 4); retry within the network caps. Stop only on the never-retry codes | Recovery rate by decline class (dunning plan) |
| "Retry until it goes through" | Networks charge for retries over their caps and for any retry on Visa category 1 codes; Mastercard stop codes 03 and 21 mean do not resubmit | Retry-schedule check (dunning plan) |
| "A health score needs weights first" | Weights picked by hand are guesses; test each signal against outcomes before combining | Signal table with lift, lead time and leakage (churn signals) |
| "Predicting churn prevents it" | A signal that fires days before cancelling leaves no time to act | Lead time against your response time (churn signals) |
| "More reminders mean more retention" | A nudge for a need that does not recur that often can bring the cancellation forward | Test the reminder against a holdout; judge inactivity against the product's natural cadence |
| "Rising retention in older cohorts means customers got stickier" | Older cohorts have already lost their least committed members (Fader and Hardie 2007) | Compare cohorts at the same age |
| "Keeping a customer is many times cheaper than winning one" | A folk ratio with no single source; the size depends on your own costs | Cost per incremental retained customer against your own acquisition cost |
