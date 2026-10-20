# LinkedIn Warm Leads

Find the people in your own LinkedIn network who are worth writing to, from the data export LinkedIn gives you ("Get a copy of your data"). The plugin reads the CSV files you supply, ranks your connections against the customer you describe, shows the shared history behind each one, and drafts messages you send yourself. Nothing is sent and LinkedIn is never opened.

## What it does

| Skill | Give it | You get |
|---|---|---|
| warm-leads-find | your export and who buys from you | the people to contact first, each with the evidence and its date, people to leave alone, a first-message draft per person, and on request a sortable CSV |
| warm-leads-revive | your export | messages you never answered, timings people gave that have passed, promises you did not keep, accepted invitations with no first message, likely job changes, with a reply draft for each |
| warm-leads-export | a question about the export, or the first small archive | how to request it, which files arrive when, what they contain and never contain, and what the first archive is already good for |

## Examples

- `My LinkedIn export is in this folder. I sell fractional RevOps to B2B SaaS teams of 20-200; buyers are VP Sales, CRO or founders. Who are the 10 people to contact this week?`
- `Find LinkedIn conversations in my export that I dropped and that are worth reopening, and draft a reply for each.`
- `I only got the first, small LinkedIn data archive so far. What can I already do with it to find clients?`

A synthetic export (invented people, no real data) to try these on is in [samples/linkedin-warm-leads](https://github.com/grayskripko/marketing-skills/tree/main/samples/linkedin-warm-leads).

## How it works

Warmth comes only from what the export records between you and each person: who asked about your work or described a problem you solve, two-way conversations and who wrote last, recommendations and endorsements, and the notes on invitations. Recent history counts more. People who pitched you, sent only automated congratulations or never exchanged a word are not counted as warm. People who said no or asked not to be contacted are listed separately and never get a draft.

Fit comes from job titles, because that is all the export says about a person's role. Company size, industry and location are not in the export, so the plugin does not guess them from a company name; it uses them only when you or the person's own messages state them.

The export never contains who liked or commented on your posts, post impressions, profile viewers or second-degree contacts, and email addresses are blank for most connections. The plugin says so instead of guessing.

## What it will not do

Send messages or invitations, open or log in to LinkedIn, scrape or look up profiles, find or verify email addresses, enrich contacts from other sources, or write one message for a blast to your whole network (it offers a post plus personal notes for the warmest people instead). Drafts are capped at 25 people per request.

## Getting the export

LinkedIn: Me > Settings & Privacy > Data Privacy > Download your data. Pick at least Connections, Messages and Invitations. Smaller categories arrive within minutes; Connections and Messages within 48 hours. The download link works for 72 hours. Unzip it and point the assistant at the folder, or upload Connections.csv and messages.csv. The files are read only when you ask, only in the current conversation.

## Personal data

Your export holds other people's names, employers and message text. The plugin uses only the files you supply for the task, reads them inside your conversation, adds nothing from outside, and stores nothing. It does not repeat email addresses or phone numbers unless you ask. Delete the archive and the conversation when you are done. See [PRIVACY.md](PRIVACY.md).

## Data and network

The plugin ships instructions only, no code and no service. It makes no network requests, runs no web search and calls no other tool or service. If your assistant has a code tool, it may run a short local script to summarise large CSV files, and it writes a file only when you ask for one.

## Troubleshooting

- "No Connections.csv": only the first archive has arrived; the second one follows within 48 hours. The first archive is still useful (invitations with notes, recommendations).
- Names look wrong or duplicated: two people can share a name; the plugin matches people by profile URL.
- The file is too large to upload: filter messages.csv to the last 24 months, or use Claude Code on the unzipped folder.

## Questions and feedback

If a skill works wrongly for your task, tell me in GitHub Discussions; I read every message: https://github.com/grayskripko/marketing-skills/discussions

Bug reports and security concerns also work in GitHub Issues: https://github.com/grayskripko/marketing-skills/issues

Sergey Skripko. I build AI agents.

## License

MIT. See LICENSE.
