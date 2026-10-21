# LinkedIn Warm Leads

Turn the LinkedIn activity you already have into conversations: the comments on your posts, your DM threads and your own network. You type one line and paste what you see on LinkedIn (or give one post URL, your data export, or ask it to read LinkedIn notification emails in your mail). The plugin sorts people, writes the replies and messages, and you send them yourself. It never logs in to LinkedIn, never looks anyone up and never sends anything.

## What it does

| Skill | Give it | You get |
|---|---|---|
| linkedin-comments-leads | the comments (or reactions) on your post, pasted or as a screenshot; or the post URL; or "check my mail" | who is a potential client, a peer, a vendor pitching you, a job seeker or a bot, with their own words as evidence, the next step for each, and DM drafts for the best few |
| linkedin-reply-to-comments | the comments on your post | a public reply per comment that answers it and keeps the thread going, tagged reply / DM next / skip, plus the DMs for people who showed a need |
| linkedin-dm-follow-up | one DM thread you paste; or your export; or "check my mail" | where the conversation stands, whether and when to follow up, the next message and one later nudge; or the list of conversations you dropped, with a draft each |
| linkedin-connections-leads | your LinkedIn data export and who buys from you | the connections to contact first, each with the shared history and its date, people to leave alone, first-message drafts, and on request a sortable CSV |
| linkedin-export-guide | a question about the export | how to request it, which files arrive when, what they contain and never contain, and what the first archive is already good for |

## Examples

- `Who in the comments of my LinkedIn post is a potential client? I sell fractional RevOps to B2B SaaS teams of 20-200. <paste the comments>`
- `Draft replies to these LinkedIn comments that move people to a call: <paste the comments>`
- `Turn this LinkedIn DM thread into a follow-up plan: <paste the thread>`
- `My LinkedIn export is in this folder. I sell fractional RevOps to B2B SaaS teams; buyers are VP Sales, CRO or founders. Who's warm?`

Synthetic test data (invented people, no real data) is in [samples/linkedin-warm-leads](https://github.com/grayskripko/marketing-skills/tree/main/samples/linkedin-warm-leads): pasted post comments, a DM thread, LinkedIn notification emails and a full data export.

## Where the input comes from

- **What you paste.** On LinkedIn, open the post, click "Load more comments" until all are shown, select the comments and copy. A screenshot also works. For a DM thread, select the messages and copy.
- **A post URL you give.** If your assistant has a web-fetch tool, it opens that one page once, because you asked. Logged out, LinkedIn shows only the post and a few comments, so the plugin says how many it could read and asks you to paste the rest. It opens no other LinkedIn page.
- **Your mail, when you ask.** With a Gmail or Outlook connector, it searches only LinkedIn notification emails (comments on your post, new messages) and reads sender, subject and snippet. Snippets are short, so it says so.
- **Your CRM, when you ask.** With a CRM connector, it checks only the names on the list (for example, whether a commenter is already a client).
- **Your LinkedIn data export.** Me > Settings & Privacy > Data Privacy > Download your data; pick Connections, Messages and Invitations. Smaller files arrive within minutes, Connections and Messages within 48 hours. Unzip and point the assistant at the folder.

## How it judges people

From their own words and the headline LinkedIn shows next to them: a question about your work, a stated problem, a request for your resource or price, a timing they gave. Praise alone is not a buying signal; vendors and recruiters pitching you are not leads; people who said no are never followed up. Company size and budget are not in a comment or the export, so the plugin does not guess them.

## What it will not do

Send messages, post, comment, like or connect on LinkedIn; open LinkedIn on its own or any page other than the one URL you give; scrape or look up profiles; find or verify email addresses; enrich contacts from other sources; or write one message to blast to every commenter or your whole network (it gives personal drafts for the best few). Drafts are capped per request (10 DMs for comments, 25 for an export).

## Personal data

Comments, messages and exports hold other people's names, headlines and words. The plugin uses only what you supply or ask it to read for the task, inside your conversation, adds nothing from outside, and stores nothing. See [PRIVACY.md](PRIVACY.md).

## Data and network

The plugin ships instructions only, no code and no service. It makes no requests of its own. Your assistant's own tools are used only when you ask: its web fetch for the one post URL you give, and your mail or CRM connector for a search you ask for. With a code tool it may run a short local script to summarise a large export, and it writes a file only when you ask for one.

## Troubleshooting

- "Only a few comments were read from the URL": LinkedIn shows few comments to logged-out readers. Paste the comments instead.
- "No comment emails found": check LinkedIn Settings > Notifications > Email for "Comments and reactions"; some people get a digest or nothing. Pasting works without it.
- "No Connections.csv": only the first archive has arrived; the second follows within 48 hours.
- Names look duplicated: two people can share a name; the export path matches people by profile URL.

## Questions and feedback

If a skill works wrongly for your task, tell me in GitHub Discussions; I read every message: https://github.com/grayskripko/marketing-skills/discussions

Bug reports and security concerns also work in GitHub Issues: https://github.com/grayskripko/marketing-skills/issues

Sergey Skripko. I build AI agents.

## License

MIT. See LICENSE.
