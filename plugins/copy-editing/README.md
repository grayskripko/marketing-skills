# Copyedit & Proof Kit

Editor's checks for finished prose. Certain errors are fixed; the rest become questions.

## Skills

| Skill | Give it | You get |
|---|---|---|
| proofread | final text, or approved and final | Ship or Hold, counts, version diff |
| redline-edit | text and an edit level | change table, author queries |
| style-sheet | pieces meant to match | variant counts, find-and-replace list |
| cut-to-length | text and a target | exact count, cut ledger |
| content-refresh | a published page and its date | dated-item ledger, refreshed text |

## Examples

- "Final proof vs approved. Approved: 'Up to 10 guests each.' Final: 'Up to 100 guests each. Doors open Thursday 4 November 2026.'"
- "Cut to 13 words, keep times: 'Starting from next month, the office will be open from 8 am until 6 pm on weekdays only.'"
- "Posted 10 June 2024, now 3 Oct 2026. What is stale? 'Last year we added Saturday opening. Our laser cutter arrives this autumn.'"

## Sample output

Verdict: **Hold**. "10" became "100"; weekday and date disagree:

| # | Check | Quote | Question | Decision |
|---|---|---|---|---|
| 1 | PR-07 dates | "Thursday 4 November 2026" | Wednesday 4 November or Thursday 5 November? | Query |

## How it works

Separate counted passes; dates and totals computed with a code tool. Numbers, names and dates keep their values. Checks are tuned for English.

## Data and network

Network scope: this plugin runs no web search and calls no service. Only the content-refresh skill may fetch, and only one public page at a URL you give plus that site's `/robots.txt`, through your assistant's own fetch tool. It skips the page if robots.txt disallows it, and never logs in, submits forms or tries to get past bot protection; if the fetch fails, is disallowed or no such tool exists, it asks you for the text instead. Nothing is stored, and no files or settings are changed unless you ask. If your assistant has a code tool, the skills may use it to compute counts, weekdays, totals and differences.

## What it will not do

Persuasion, new copy, claim checks, voice reviews, translation, legal advice, AI-detector evasion.

## Troubleshooting

Ask for "tracked changes" to get inline marks.

## Support

Issues: https://github.com/grayskripko/marketing-skills/issues.

## License

MIT, see LICENSE.
