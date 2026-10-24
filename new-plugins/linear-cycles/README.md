# Linear Cycles

Explain why a Linear cycle graph differs from an issue export and how much work the team completed. Use estimates and membership history to explain early additions and cooldown outcomes.

For product and engineering teams reviewing cycle delivery. Paste graph totals or descriptions, current issue CSV/text, team estimate settings and membership/cooldown activity. No account, keys, installable connector or paid API is required.

## What this package runs and connects to

The reporting workflow uses Markdown instructions and bundled reference text, JSON metadata, and a static SVG icon. Installing it does not run a program or connect an account. There are no installers, hooks, MCP or LSP servers, or background processes. Both platform manifests are metadata for the same reporting skills.

The two reporting skills analyze task text, attachments, and local files you explicitly supply. They do not instruct the assistant to run code, install software, call APIs, connect accounts, send reports, publish content, or change Linear settings or issues. They prohibit network requests during skill execution and do not fetch supplied attachment or view links. Missing information must be supplied as text or a selected file. Their export-completion advice asks you or an authorized admin to obtain CSV exports in Linear; that user-led action accesses your Linear account and creates a downloaded file, but the skills do not perform it.

Source maintenance is a separate network activity: both bundled source registers instruct the reader to reopen public Linear documentation before submission, and the skills refer to those registers for refreshing rules or source maintenance. The listed destinations are `https://linear.app/docs/cycle-graph`, `/docs/filters`, `/docs/use-cycles`, `/docs/issue-property#estimates`, `/docs/estimates`, `/docs/issue-properties-home`, and `/docs/exporting-data`. Opening them sends the requested URL and ordinary connection metadata to Linear and any assistant web-tool provider used; no issue export upload is instructed. GitHub repository, privacy, and support links identify package information; the skills do not retrieve them or submit support messages.

This working folder also includes development records and `tests/bfix/validate.py`. That Python validator is not invoked by installation or either skill. If run manually, it uses Python and PyYAML to read local package files and writes `tests/bfix/validation.json`; it makes no network requests. Under the scanhold packaging rules, move development material (`tests/`, `BUILD-NOTES.md`, and `REVIEW.md`) outside the submitted folder before claiming an executable-free package. This current folder therefore does not make that claim.

The publisher receives no task data through these instructions and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled reporting program.

| Skill | Input | Result |
|---|---|---|
| cycle-scope-report | Graph, current export, filters and estimates | Historical/current scope, weighted completion, issue-count success and explained differences |
| cycle-cooldown-history | Dates, membership events and automation settings | Per-issue previous/next-cycle attribution and rollover exceptions |

Ask “Explain why this cycle graph differs from my export” or “Where should these cooldown completions count?” Export rows can support current totals; membership history is needed for planned additions and a historical scope bridge. Include the capture date, team timezone and status-category mapping. If obtaining data in Linear, use Export issues as CSV from the command menu; supply activity text or an individual-issue PDF for membership events. View exports have role-based limits: 250 issues for members and 2,000 for admins (owners on Enterprise).

## Data and network

The skills read pasted content and files you select for the task. Network fetches: none during the reporting workflow; the separate source-maintenance instructions are disclosed above. Public Linear documentation is embedded in dated source registers. Issue data is not sent to Linear or any other external service by these instructions. No telemetry, background storage or account changes. Your assistant processes the conversation and files under its normal retention settings. Omit names and descriptions when IDs and fields suffice.

## Sources and support

See [source register](skills/cycle-scope-report/references/sources.md) for current field rules and URLs. Support: https://github.com/grayskripko/marketing-skills/issues

MIT; see [LICENSE](LICENSE).
