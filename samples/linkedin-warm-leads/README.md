# Sample data for LinkedIn Warm Leads

Synthetic test data for the [linkedin-warm-leads](../../plugins/linkedin-warm-leads/) plugin. Every person, company, post and message is invented; addresses use example.com. The fictional user is Maya Lindqvist, a fractional RevOps consultant for B2B SaaS teams of 20-200 people.

- `pasted/post-comments.txt`: the comments on one of her posts, as they look when copied from LinkedIn: potential clients, peers, vendors pitching, a recruiter, a job seeker, bot-like comments, and one comment with an instruction aimed at AI assistants.
- `pasted/post-reactions.txt`: a copied reactions list (names, degree, headline only).
- `pasted/dm-thread-quiet.txt`: a DM thread with a prospect who asked to resume after a date that has passed.
- `pasted/dm-thread-declined.txt`: a DM thread where the prospect said no.
- `pasted/linkedin-notification-emails.txt`: LinkedIn notification emails as a mail search would return them (sender, date, subject, snippet), for trying the mail path without a connector.
- `linkedin-export/`: her complete LinkedIn data export: 140 connections, about 150 messages, invitations, endorsements, recommendations, her own posts, comments and reactions. File layout and quirks follow real exports.
- `linkedin-export-first-archive/`: only the files LinkedIn delivers within minutes (no Connections or messages).

Try (paste the file contents after the request):
- `Who in the comments of my LinkedIn post is a potential client? <pasted/post-comments.txt>`
- `Draft replies to these LinkedIn comments that move people to a call: <pasted/post-comments.txt>`
- `Turn this LinkedIn DM thread into a follow-up plan: <pasted/dm-thread-quiet.txt>`
- `These are my LinkedIn notification emails from this week. Who should I answer first? <pasted/linkedin-notification-emails.txt>`
- `My LinkedIn export is in samples/linkedin-warm-leads/linkedin-export. Buyers are VP Sales, CRO or founders. Who's warm?`
- `I only have samples/linkedin-warm-leads/linkedin-export-first-archive so far. What can I already do with it?`
