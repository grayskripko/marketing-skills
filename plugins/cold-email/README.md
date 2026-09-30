# Cold Email Kit

Review, check and write one-to-one business cold emails. Scores show their evidence, your facts stay locked, and nothing is sent.

## What it does

| Skill | Give it | You get |
|---|---|---|
| cold-email-review | your email or sequence | 12-check scorecard with quotes, fact-lock table, change log, rewrite |
| cold-email-check | an email before sending, up to 25 rows, your DNS records | PASS / FIX / ASK rows, merge table, sender table |
| cold-email-write | your offer and target | plan printed first, emails, fact ledger with proof slots |
| cold-email-brief | an offer and an audience | offer brief and offer check |
| cold-email-hooks | notes on up to 20 prospects or 3 pages | dated facts, opening lines, dropped facts |

## Examples

- `Review and fix this cold email: "Re: our chat. Hi {{firstName}}, Northwind cuts AP time 40%. Book a call or see the deck"`
- `Check before sending: "Hi {{first_name}}, saw {{company}} is hiring AP staff." Rows: Ana,Acme | ,Globex | Li,Initech (Payroll)`
- `Why might my cold emails land in junk? SPF: v=spf1 include:_spf.mailhost.test ~all. DKIM: none pasted. DMARC: none`

## How it works

A scorecard row: `CE-02 | 0 | "Re: our chat" | First message with a reply prefix`. A merge row: `2 | (empty), Globex | MQ-01 first_name | fix`. Scores are checklists, not forecasts.

## What it will not do

Send email, create drafts, add contacts to tools, find addresses, scrape, fake reply subjects or history, hide the opt-out, or give legal advice; country rows name the statute to check.

## Personal data

Notes, rows and replies can contain names and addresses. The plugin reads them in the conversation and stores nothing. Addresses are never needed: redact them.

## Data and network

Network scope: only the cold-email-hooks skill fetches anything, and only public pages at URLs you give, at most 3 per run, one request each, no links followed, no login. No skill runs a web search. The plugin sends no email, looks up no address, runs no DNS query, calls no other service and stores nothing; if your assistant has a code tool, it may use it to count words and rows.

## Troubleshooting

A page fails: paste its text. Sender table says "can't tell": paste DNS records or message headers.

## Support

Issues: https://github.com/grayskripko/marketing-skills/issues

## License

MIT. See LICENSE.
