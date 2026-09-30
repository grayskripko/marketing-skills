# Customer Research Kit

## What it does

Traceable customer research from text you paste or attach, with no connectors. Interview notes become a quote ledger with ids, a theme-by-source count table, a fixed evidence-strength rule, contradictions and a self-check that every quote is verbatim. Participants are pseudonymised by default. The kit also checks interview guides for leading questions, codes why customers cancel (stated versus evidenced reason), and builds an ideal customer profile marked backed or assumed line by line.

## Sample output

| Theme | Evidence | Count | Strength |
|---|---|---|---|
| Month-end close is slowed by manual transfer, for firms of 10+ staff | S01-Q03, S03-Q07, S06-Q01, S09-Q04 | 4 of 11 sources, 2 segments | Strong |

Self-check: theme lines without ids 0; quotes not found verbatim 0.

## Skills

| You give | Skill |
|---|---|
| A research goal, or a draft interview guide | `interview-guide` |
| 2+ interview transcripts or call notes | `interview-synthesis` |
| Many reviews, tickets or survey answers | `feedback-analysis` |
| Subscription cancellations or customer exit notes | `churn-analysis` |
| Findings or a list of top customers | `icp-profile` |

## Examples

- "Why did they cancel? C1 'too pricey' (setup never finished, 2 logins) C2 'too pricey' C3 'moved to a rival' C4 'owner left'"
- "Check my interview guide: 'Would you use a faster invoicing tool? Don't you hate manual entry? How much would you pay?'"
- "Theme 5 calls: S1 'Close takes 4 days' S2 'We re-key invoices' S3 'I copy bank rows' S4 'Fridays go on exports' S5 'Close is OK'"

## How it works

Every theme cites ledger ids and shows "k of N sources". Strong needs at least 3 sources and a third of N with no same-segment contradiction; below 5 sources results are marked exploratory. Answers to leading questions count for less.

## Personal data

The kit reads personal data only inside your conversation and stores nothing. Output replaces names with role labels, removes contact details, turns company names into segment descriptions and drops sensitive details. Ids are pseudonyms, not anonymisation. Remove personal data you do not need before pasting.

## Data and network

Network scope: this plugin fetches nothing and runs no web search; it works only on text and files you paste or attach, runs no code of its own and stores nothing, and if the assistant has a code or spreadsheet tool it may use it to count codes and themes.

## What it will not do

- Research employees or job candidates, or profile a named person.
- Invent quotes or treat simulated customers as evidence.
- Predict or score churn.
- Write copy, outreach or content plans.
- Give legal advice.

## Troubleshooting

- **Counts look off:** without a code tool they are approximate; ask for a recount.
- **Self-check shows mismatches:** ask for the listed quotes to be re-pulled from the input.

## Support

GitHub Issues: https://github.com/grayskripko/marketing-skills/issues

## License and privacy

MIT License, see [LICENSE](LICENSE). Privacy policy: [PRIVACY.md](PRIVACY.md).
