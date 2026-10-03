# Cancel-flow checks CF-01 to CF-16

Each check gets Pass, Fail or Not checkable, the user's own words quoted as evidence, and the source id from `cancel-rules.md`. "Heuristic" means a practice of this plugin, not a legal duty; say so in the output. Every Fail comes with the compliant alternative from the last column.

| Id | Check | Source | Compliant alternative |
|---|---|---|---|
| CF-01 | A customer who joined online can also finish cancelling online | CA-d; DE-312k; UK-DMCC (from January 2027); US-ROSCA "simple mechanisms", with US-AMZ as an enforcement example | A cancel link or button in the account area that completes the job online |
| CF-02 | No phone call, chat, agent or email exchange is needed to finish | CA-d ("obstruct or delay"); DP-FTC | Remove the human step; offer contact as an option, never as the gate |
| CF-03 | The way in is easy to find from account or billing settings, without searching help pages | CA-d ("prominently located"); DE-312k (always available, directly and easily reachable). DE: a login required before the button can be reached is printed as **Fail (risk)** against DE-312k; say the statute text does not mention login and counsel should confirm | Put "Cancel subscription" on the plan or billing page itself; in Germany, reachable without logging in |
| CF-04 | At most one save step before the final confirmation | heuristic; DP-FTC and DP-MATHUR describe repeated interruptions as a pattern. Not a California rule | Keep one screen with one offer, then the confirmation |
| CF-05 | Every screen with an offer also shows a cancel control that stays visible next to it | CA-e2 ("continuously and proximately displayed") | Show "Cancel" beside the offer on the same screen, same reachability as the accept button |
| CF-06 | Any deadline on an offer is real and its date is stated | DP-MATHUR (false urgency); DP-FTC | State the real end date, or drop the deadline |
| CF-07 | No copy that shames or guilt-trips the customer for leaving | DP-MATHUR (confirmshaming); DP-FTC | Neutral wording, for example "Your plan ends on [END_DATE]" |
| CF-08 | No second offer after the customer has declined one in the same session | heuristic; DP-MATHUR (nagging). Not a California rule | Proceed to the confirmation after one decline |
| CF-09 | Any reason survey can be skipped and never blocks the exit | heuristic; CA-d ("obstruct or delay"); DP-FTC | Mark the survey optional and keep the confirm button active |
| CF-10 | The cancellation takes effect once the customer goes on; no waiting period, call-back or "we will process this in 2 days" | CA-d ("immediately accessible" email route; no steps that "obstruct or delay"); CA-e2 ("promptly process") | Process at once; the service may run to the end of the paid period |
| CF-11 | The final screen states the end date and what stays accessible | heuristic; DE-312k confirmation page | Show end date, data handling and how to restart |
| CF-12 | A confirmation reaches the customer on a durable medium (email or receipt) with date and time | DE-312k; EU-WF (for withdrawals); UK-DMCC (detail awaits secondary legislation) | Send an email receipt straight away |
| CF-13 | Offer terms are complete: discounted price, how long it lasts, the price after it ends | US-ROSCA (material terms); CA-g for later price changes | Print all three on the offer screen |
| CF-14 | Pause and downgrade are offered as alternatives with an end date, never as the only way out | heuristic | List pause or downgrade beside "Cancel", each with its end date |
| CF-15 | The cancellation still goes through if the save step fails to load or errors | heuristic | Fall back to the confirmation screen on any error |
| CF-16 | EU only: during the withdrawal period, a withdrawal function is available for contracts concluded online | EU-WF (from 19 June 2026) | Add a "withdraw from contract here" control with a confirm step and a durable receipt |

## Parity table (part a of the audit)

Count each path from the same starting point (logged-in home or account page) to the final state:

| Measure | Sign-up | Cancel | Difference |
|---|---|---|---|
| Screens | | | |
| Required actions (clicks, fields) | | | |
| Channels used (web, app, email, phone, chat) | | | |
| Humans involved | | | |

A cancel path longer than the sign-up path is not by itself a breach anywhere in this register; it is printed so the team can see the gap. Breaches are named only through CF ids and their sources.

## What the audit never suggests

Hidden or moving cancel controls, mandatory calls or chats, waiting periods after the customer persists, invented deadlines, guilt copy, blocking surveys, pre-selected "stay" options, or a second offer after a decline (ground rule 4).
