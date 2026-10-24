# NetSuite Journals

Check a NetSuite journal CSV before import, or fix failed rows using pasted errors and reference exports. Explain append versus replacement; existing-line changes need complete current lines, and replacements need every retained populated field and its mapping.
For accountants and finance teams preparing NetSuite journal imports. Needs pasted CSV or local exports, selected import settings, account/subsidiary references and any results.csv errors. For any existing-journal line update, include complete current lines. Replacements also need every retained populated line field and its mapping. No keys, account connection or additional installation is needed.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

| Skill | Ask | Result |
|---|---|---|
| journal-csv-preflight | Will this CSV add lines or replace them? | Row-level findings, mapping changes, balance calculations and a proposed CSV where evidence is complete. |
| journal-import-repair | Why did these journal rows fail? | Error-to-row repairs, unresolved references and a retry plan tied to actual job results. |

Include the import assistant, record type, Add/Update/Add or Update setting, Overwrite Sublists setting and reference types. Useful context includes OneWorld, account numbering, book-specific fields, form mappings, payment application, posting period and whether references are complete. A partial export still supports visible findings and marked repair fragments.

Regular and two-subsidiary intercompany journals are covered. Advanced intercompany entries are identified separately; their specialized fields and Auto Balance need their own mapping evidence. Statistical and period-end journals are separate jobs.

## Data and network

Reads only text and local exports you supply. Fetches nothing during use, uses no connectors and performs no NetSuite account actions. Oracle rules are embedded in dated references. No telemetry or plugin storage. See [PRIVACY.md](PRIVACY.md).

## Contents

Two self-contained skills, official Oracle references, dual manifests, an icon and an MIT license. [BUILD-NOTES.md](BUILD-NOTES.md) records source verification, review and local validation.

Support: https://github.com/grayskripko/marketing-skills/issues
