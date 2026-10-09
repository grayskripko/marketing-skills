# Cold Email Kit

Write, review and check one-to-one business cold emails. You get an email you can send, built only from the facts you give. Nothing is sent.

## What it does

| Skill | Give it | You get |
|---|---|---|
| cold-email-write | your offer and who it's for | a cold email and follow-ups, ready to paste |
| cold-email-review | an email that gets no replies | a rewrite first, then what changed and why; a 12-check score on request |
| cold-email-check | an email you're about to send, up to 25 sample rows, your DNS records | what to fix before sending, a fixed version, problem rows, what your records cover |
| cold-email-brief | your offer and audience | whether the offer is ready, and what's missing |
| cold-email-hooks | notes on up to 20 prospects, or links to up to 3 public pages | one opening line per prospect from a real, dated fact |

## Examples

- `Review and fix this cold email: "Re: our chat. Hi {{firstName}}, Northwind cuts AP time 40%. Book a call or see the deck"`
- `Check before sending: "Hi {{first_name}}, saw {{company}} is hiring AP staff." Rows: Ana,Acme | ,Globex | Li,Initech (Payroll)`
- `Why might my cold emails land in junk? SPF: v=spf1 include:_spf.mailhost.test ~all. DKIM: none pasted. DMARC: none`

## How it works

A rewrite copies your numbers, names and claims exactly and adds none; a fact it lacks is asked for, not invented. In the pre-send check, the row ", Globex" is flagged because the first name is empty, and the fix adds a fallback ("Hi there"). Scores, when you ask for them, are checklists, not reply-rate forecasts.

## What it will not do

Send email, create drafts, add contacts to tools, find addresses, scrape, fake reply subjects or history, hide the opt-out, or give legal advice; country rows name the statute to check.

## Personal data

Notes, rows and replies can contain names and addresses. The plugin reads them in the conversation and stores nothing. Addresses are never needed: redact them.

## Data and network

Network scope: only the cold-email-hooks skill fetches anything, and only public pages at URLs you give, at most 3 public pages per run, one request each plus the site's robots.txt, following no links and never logging in; a page the site's robots.txt disallows is not fetched. No skill runs a web search. The plugin sends no email, looks up no address, runs no DNS query, calls no other service and stores nothing; if your assistant has a code tool, it may use it to count words and rows.

## Troubleshooting

A page fails or its site does not allow fetching: paste its text. Sender table says "can't tell": paste DNS records or message headers.

## Support

Issues: https://github.com/grayskripko/marketing-skills/issues

## License

MIT. See LICENSE.
