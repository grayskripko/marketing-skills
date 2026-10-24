# Newsletter Analytics

Analyze newsletter snapshots from supplied reports and exports: check metric definitions, compare issues, review subscriber growth and write a short decision memo.

For publishers and teams working from pasted reports or local CSV exports, including Substack, Mailchimp and beehiiv. No login, paid API or account connection is required. Bring the data you already have; available export fields depend on your provider and plan.

## What this package runs and connects to

The newsletter workflow uses Markdown skills and reference text, JSON platform metadata, and a static SVG icon. It provides no installer, hooks, MCP or LSP server, or background process; installing the metadata does not launch a program or connect an account.

These skills analyze pasted task text and local files you explicitly select, and may read the bundled measurement notes. They prohibit fetching URLs, including supplied report links, and do not direct web search, API calls, account connections, message delivery, publishing, subscriber changes, credential handling, or software installation. Mailchimp and beehiiv documentation links identify historical sources, and GitHub links identify repository and support pages; they are not retrieval instructions. Paste the relevant contents of a report link instead.

This is offline source analysis, with optional host calculation tools, rather than a strict no-execution workflow. Your assistant may use its existing code or spreadsheet tools to read selected exports, match records and compute figures. Execution and temporary calculation files are managed by your assistant provider, not a plugin server. The skills request written answers and do not instruct file writes or running a campaign; re-export and experiment suggestions are advice for a later user action. Any output file you explicitly request uses your assistant's existing file tools.

The publisher receives no task data through this workflow and operates no collection, telemetry, or storage service for it. Your assistant provider still processes and may retain conversations, attachments and tool inputs under its own terms. This network boundary concerns plugin-directed activity, not the provider's inference or tool infrastructure.

| Skill | Ask for | Useful inputs |
|---|---|---|
| check-newsletter-data | Explain conflicting reports or rate labels | report fields, definitions, counts and tracking settings |
| compare-issue-results | Compare issues fairly | issue IDs, send dates, capture dates, counts and audience scope |
| review-subscriber-growth | Separate net growth, imports and source outcomes | subscriber counts at different dates, dated signups and status changes, groups measured for the same time, and optional costs |
| write-newsletter-readout | Give a manager the decision and next test | pasted results, decision, reader and length |

Start with whichever job you need. The memo skill also works directly from raw reports. Include sent and delivered counts, unique versus total event definitions, email versus web scope, bot settings, dates and timezones when available. Missing fields do not stop useful work. Keep rates separate when their definitions differ. Leave rates unavailable when the number to divide by is missing.

Examples: “Why do these two click reports disagree?” “Compare these three issues.” “Did the list grow through signups or imports?” “Write a short results update for our publisher.”

The answer shows formulas using your figures, explains which comparisons they support and notes only limits that change the decision. To compare subscriber groups, the records must show who belongs to each group. Each group needs the same measurement time after signup. The share currently paying does not show how many free subscribers became paid. Results show measured differences. They do not prove causes, predict revenue or test inbox placement.

## Data and network

Reads only pasted material and user-selected local files. Fetches nothing, even when a URL is supplied. No sending, account changes, credential handling, tracking service or plugin-owned storage. An assistant may use its local calculation tools to read selected exports and compute figures. The assistant provider processes the conversation under its own terms. Redact subscriber contact details; use totals or anonymized IDs when records need to be matched. See [PRIVACY.md](PRIVACY.md).

Snapshot analysis uses supplied Substack, Mailchimp and beehiiv reports or exports. For a report link, paste its contents or upload an export.

## Support and license

[Support](https://github.com/grayskripko/marketing-skills/issues). MIT; see [LICENSE](LICENSE).
