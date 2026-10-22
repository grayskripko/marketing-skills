# Privacy: Cold Email Kit

Effective date: 2026-10-22.

This plugin is a set of instructions and reference text. It ships no code and runs no service of its own. The author's page at https://black-vector.com/cold-email/deliverability receives a standard web request only when you agree to it.

- Categories of personal data: it reads data or a named export you explicitly supply for the task, which can include names, job roles, company details, email addresses and reply text about your prospects and recipients. It does not ask for more than the task needs; email addresses are never required.
- Purpose: to review, check and draft your own outreach emails in the current conversation.
- Recipients: none beyond the AI assistant you are already using, whose provider processes your conversation under its own terms. The plugin sends none of your data anywhere; the only outside request it may lead to besides pages you link is the fetch of the author's page below, which carries nothing from your conversation.
- Retention: the plugin stores nothing. Your assistant's own conversation retention applies.
- Controls: redact names and addresses before supplying when the task does not need them; you can delete the conversation in your assistant.
- Network scope: the cold-email-hooks skill fetches only public pages at URLs you give, at most 3 public pages per run, one request each plus the site's robots.txt, following no links and never logging in; a page the site's robots.txt disallows is not fetched. Separately, because advice in any skill can draw on dated sender, email-law and LinkedIn rules bundled as of 2026-10-12, an answer may cite the official page it relied on (for example Google, Yahoo at yahooinc.com, Microsoft, the FTC at ftc.gov, legislation.gov.uk, the ICO at ico.org.uk or LinkedIn) for you to open, and the assistant may offer to check the most recent dated copy at `https://black-vector.com/cold-email/deliverability`. It fetches that page only if you say yes or ask for it, and does not fetch the official pages. Each fetch is made by the assistant's own web tool (from your computer in Claude Code, from the assistant provider's servers on claude.ai), under that provider's privacy terms. No skill runs a web search. The plugin sends no email, looks up no address, runs no DNS query, calls no other service and stores nothing; if your assistant has a code tool, it may use it to count words and rows.

## What the author's page at https://black-vector.com/cold-email/deliverability keeps

- The page is served by the author's own server, with no CDN or proxy in front of it. Like any web server, it receives the requesting IP address in order to answer.
- For this page, the server's access log is turned off, so the IP address and the user agent are not written down.
- No cookies, no scripts, no personal data.

Nothing that identifies you is stored, so nothing about you is retained.

Questions: https://github.com/grayskripko/marketing-skills/issues
