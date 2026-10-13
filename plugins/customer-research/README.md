# Customer Research Kit

## What it does

Paste interview notes, reviews, support tickets or cancellation reasons and get the main themes or reasons first, each backed by the customers' own words and a count you can check ("4 of 11 interviews"), plus where customers disagree. The kit also checks interview questions for leading wording or writes a new guide, separates the reason customers gave for cancelling from the reason the notes show, and drafts an ideal customer profile that marks each line as backed by data or assumed. Names are replaced with role labels. No connectors needed.

## Sample output

**Answer:** month-end close is slowed by manual transfer between bank and books, for firms of 10+ staff (4 of 11 interviews: S01, S03, S06, S09). The table shows the evidence.

| Theme | Evidence | Count | Strength |
|---|---|---|---|
| Month-end close is slowed by manual transfer, for firms of 10+ staff | S01-Q03, S03-Q07, S06-Q01, S09-Q04 | 4 of 11 sources, 2 segments | Strong |

## Skills

| You give | Skill |
|---|---|
| A research goal, or a draft interview guide | `interview-guide` |
| 2+ interview transcripts or call notes | `interview-synthesis` |
| A batch of reviews, tickets or survey answers | `feedback-analysis` |
| Subscription cancellations or customer exit notes | `churn-analysis` |
| Findings or a list of top customers | `icp-profile` |

## Examples

- "Why did they cancel? C1 'too pricey' (setup never finished, 2 logins) C2 'too pricey' C3 'moved to a rival' C4 'owner left'"
- "Check my interview guide: 'Would you use a faster invoicing tool? Don't you hate manual entry? How much would you pay?'"
- "Theme 5 calls: S1 'Close takes 4 days' S2 'We re-key invoices' S3 'I copy bank rows' S4 'Fridays go on exports' S5 'Close is OK'"

## How it works

Every theme cites quote ids and shows "k of N sources". A theme is called strong only when at least 3 interviews and at least a third of all interviews support it, and no interview in the same segment says the opposite. Answers to leading questions count half. With fewer than 5 interviews, results are marked exploratory.

## Personal data

The kit reads personal data only inside your conversation and stores nothing. Output replaces names with role labels, removes contact details, turns company names into segment descriptions and drops sensitive details. Ids are pseudonyms, not anonymisation. Remove personal data you do not need before pasting.

## Data and network

The plugin fetches nothing and runs no web search. It works only on text and files you paste or attach, runs no code of its own and stores nothing. If the assistant has a code or spreadsheet tool, it may use it to count.

## What it will not do

- Research employees or job candidates, or profile a named person.
- Invent quotes or treat simulated customers as evidence.
- Predict or score churn.
- Write copy, outreach or content plans.
- Give legal advice.

## Troubleshooting

- **Counts look off:** without a code tool they are counted by hand; ask for a recount.
- **A quote doesn't match your notes:** ask for it to be re-pulled from the input.

## Related plugins

Where this plugin stops and another one of mine continues:

- [Ad Copy & Creative Preflight](https://github.com/grayskripko/marketing-skills/blob/storm/plugins/ad-creative/README.md): angle-matrix takes exactly the reviews, survey answers and call notes this plugin has coded and turns them into evidence-traced ad angles.
- [Churn Prevention](https://github.com/grayskripko/marketing-skills/blob/storm/plugins/churn-prevention/README.md): churn-analysis explains why people cancel but changes nothing; Churn Prevention acts on it with cancel-flow, save-offer, dunning and win-back plans and tests churn signals on account data.
- [Copywriting & Positioning](https://github.com/grayskripko/marketing-skills/blob/main/plugins/copywriting-kit/README.md): The quote ledger and ICP give evidence ids and the customer's own words, which copy-proof-check and page-copy need so claims stay within evidence.

## Questions and feedback

If a skill works wrongly for your task, tell me in GitHub Discussions — I read every message: https://github.com/grayskripko/marketing-skills/discussions

Bug reports also work in GitHub Issues: https://github.com/grayskripko/marketing-skills/issues

Sergey Skripko. I build AI agents.

## License and privacy

MIT License, see [LICENSE](LICENSE). Privacy policy: [PRIVACY.md](PRIVACY.md).
