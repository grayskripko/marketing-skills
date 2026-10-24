# BambooHR Headcount

Explain why BambooHR report and employee directory counts differ, and identify who appears in only one export.

For HR and recruiting teams comparing employee counts. Needs pasted rows or supplied exports, export settings and a target population/date. No account, API key, paid service or connector is needed to analyze existing exports.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata. Build notes, review notes and test records are development evidence, not a runtime.

The analysis skills work only from task text, attachments, and local files that you explicitly supply. They read selected files and bundled references, preserve originals, and do not instruct the assistant to run code, install software, search the web, fetch supplied URLs or robots.txt, call APIs, send messages, publish content, or change account settings. Calculations and corrected API request fragments are returned as analysis and text; the fragments are not executed. If more records, pages or history are needed, you supply an additional export obtained through your own authorized BambooHR access. A supplied URL is treated as text: paste the relevant content instead.

There is a separate release-maintenance network instruction in each bundled `bamboohr-rules.md`: reopen its ten public pages at `https://documentation.bamboohr.com` before the planned 2026-10-17 submission and refresh changed rules. That step retrieves public documentation, exposing the requested URLs and ordinary connection metadata to BambooHR's documentation host and the browser or assistant tool provider; it does not require sending employee exports or credentials. It is not part of headcount analysis. GitHub source and support links identify the repository and support page; the skills do not open issues or send reports.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

| Skill | Request | Result |
| --- | --- | --- |
| headcount-reconcile | Why do my report and directory counts differ? | Raw-to-unique count bridge and unmatched internal IDs |
| export-diagnosis | Why are columns missing or this export failing? | Field/access/page diagnosis and minimal correction |
| headcount-as-of | How many people were in a department at month end? | Dated inclusion table and department counts |

Paste CSV, JSON, XML, or a table; alternatively select an export file for the assistant to read. Use pseudonymous internal IDs and omit names, contacts, pay and national identifiers. Supply the company label, export route/version, extraction timestamp/timezone, filters, requested/returned fields, page metadata and caller access level where available. For historical counts add employment-status and job-history rows and the hire/termination boundary used by your company.

Example requests: “Match these two exports and explain the count gap.” “A 200 response lost department: here are the requested and returned fields.” “Count people as of September 30 from these dated status and transfer rows.”

The skills distinguish directory visibility from roster membership, Active/Inactive from employment categories, and internal ID from Employee #. A count is tied to the supplied data's date, filters and readable coverage. Missing history produces unresolved IDs rather than invented past states.

## Data and network

Headcount analysis reads supplied material and selected files without fetching URLs or accessing an account. The separate public-documentation refresh for release maintenance is disclosed above. A local output file is created only when requested. See [PRIVACY.md](PRIVACY.md).

Official sources and retrieval dates are included in each skill's references. The source refresh for the planned October 17 submission is recorded in [BUILD-NOTES.md](BUILD-NOTES.md).

Support: https://github.com/grayskripko/marketing-skills/issues

MIT. See [LICENSE](LICENSE).
