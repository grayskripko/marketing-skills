# Cold Email Kit

Write, review and check one-to-one business cold emails. You get cold-email copy built only from the facts you give; sending still depends on required identity, applicable recipient requirements and correct template rendering. Nothing is sent.

## What it does

| Skill | Give it | You get |
|---|---|---|
| cold-email-write | your offer and who it's for | a cold email and follow-ups, ready to paste |
| cold-email-review | an email that gets no replies | a rewrite in your requested format, relevant change notes and an editorial score on request |
| cold-email-check | an email you're about to send, up to 25 sample rows, your DNS records | requested fixes, corrected copy, row decisions or an assessment of supplied records |
| cold-email-brief | your offer and audience | whether the offer is ready, and what's missing |
| cold-email-hooks | notes on up to 20 prospects, or links to up to 3 public pages | one opening line per prospect from a real, dated fact |

## Examples

- `Review and fix this cold email: "Re: our chat. Hi {{firstName}}, Northwind cuts AP time 40%. Book a call or see the deck"`
- `Check before sending: "Hi {{first_name}}, saw {{company}} is hiring AP staff." Rows: Ana,Acme | ,Globex | Li,Initech (Payroll)`
- `Why might my cold emails land in junk? SPF: v=spf1 include:_spf.mailhost.test ~all. DKIM: none pasted. DMARC: none`

## How it works

A rewrite preserves retained factual values, scope and dates exactly and adds no facts. It can remove deceptive content or competing asks, explaining material removals; missing details are omitted or asked for when they change the work. In the pre-send check, the row ", Globex" is flagged because the first name is empty, and the fix adds a fallback ("Hi there"). Scores, when you ask for them, are checklists, not reply-rate forecasts.

## What it will not do

Send email, create drafts, add contacts to tools, find addresses, scrape, fake reply subjects or history, hide the opt-out, or give legal advice; country rows name the statute to check.

## Personal data

Notes, rows and replies can contain names and addresses. Use data or a named export explicitly supplied for the task; the plugin does not scan memory, chat history or unrelated files and stores nothing. Addresses are never needed: redact them.

## Data and network

Network scope: two kinds of fetch, nothing else.
1. **Pages you link, in cold-email-hooks.** Only public pages at URLs you give, at most 3 public pages per run, one request each plus the site's robots.txt, following no links and never logging in; a page the site's robots.txt disallows is not fetched.
2. **The author's page at https://black-vector.com/cold-email/deliverability, only after you say yes.** Advice in any of the five skills can rest on dated rules (for example Gmail's bulk-sender requirements, CAN-SPAM's opt-out duty, Germany's consent rule or LinkedIn's 200-character note): drafting, rewriting or checking an email or LinkedIn message, choosing which people or countries to contact, working from notes about named business contacts, or reading sender records. The bundled copy is dated 2026-10-12 and may be out of date, so an answer may end with a short note: the official page it relied on, its date, and an offer to check it against the plugin's changelog of these rules, https://black-vector.com/cold-email/deliverability, a page kept by the plugin author on a domain he owns. The official pages it names (for example Google, Yahoo at yahooinc.com, Microsoft, the FTC at ftc.gov, legislation.gov.uk, the ICO at ico.org.uk or LinkedIn) are for you to open; the assistant does not fetch them. It fetches that page only if you say yes or ask for it, tells you what changed, and you decide whether to revise anything. If you never say yes, nothing is fetched.

No skill runs a web search. The plugin sends no email, looks up no address, runs no DNS query, calls no other service and stores nothing; if your assistant has a code tool, it may use it to count words and rows.

What the author's page at https://black-vector.com/cold-email/deliverability keeps: see the [privacy policy](PRIVACY.md).

## Troubleshooting

A page fails or its site does not allow fetching: paste its text. Sender table says "can't tell": paste DNS records or message headers.

## Related plugins

Where this plugin stops and another one of mine continues:

- [Customer Research Kit](https://github.com/grayskripko/marketing-skills/blob/wind/plugins/customer-research/README.md): cold-email-brief needs a segment and the pain in the buyer's words; icp-profile and interview synthesis supply both marked backed or assumed instead of guessed.
- [Sales Enablement & Role-Play](https://github.com/grayskripko/marketing-skills/blob/storm/plugins/sales-enablement/README.md): Once replies turn into meetings, demo-runbook builds the demo from the prospect's stated pains and call-coaching scores how the calls went, which cold-email does not cover.
- [Marketing Ideas & Growth Experiments](https://github.com/grayskripko/marketing-skills/blob/storm/plugins/marketing-ideas/README.md): after the sequence has run, paste sent, replies and meetings into idea-readout to decide scale, iterate or stop with 95% ranges.

## Questions and feedback

If a skill works wrongly for your task, tell me in GitHub Discussions — I read every message: https://github.com/grayskripko/marketing-skills/discussions

Bug reports also work in GitHub Issues: https://github.com/grayskripko/marketing-skills/issues

Sergey Skripko. I build AI agents.

## License

MIT. See LICENSE.
