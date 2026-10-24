# Recruiting Offers

Explain why Greenhouse offer acceptance reports disagree and list offers still waiting for a response.
For recruiting operations teams and hiring analysts. Needs pasted report text or user-supplied CSV/XLSX exports plus dates, filter settings and permission scope. No accounts, keys, installs or paid APIs are required for analysis.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The current folder also contains development notes and text/JSON evaluation records; these are not runtime components and should be excluded from the submitted package.

The offer-analysis workflows use only task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, call APIs, send messages, publish content, write files, or change account settings. Results are returned in the conversation. Both skills ask you to obtain authorized Greenhouse report exports manually through Reports → Essential reports → Offer Activity/Offer Details → Filters and more → Apply; the assistant does not log in or obtain exports for you.

There is a source-verification exception: both bundled source registers instruct rechecking four public Greenhouse support articles before submission and when applying rules to a changed report. Following that instruction may retrieve those articles using the assistant's existing web tool, contacting support.greenhouse.io and the tool provider with the requested URL and ordinary connection metadata. This is not an API or account connection and does not require sending supplied offer data. The skills themselves prohibit network requests during supplied-export analysis. For that workflow, use the embedded reference text; if changed behavior needs verification without retrieval, supply the relevant article passage. GitHub documentation, privacy, author and support links identify package information, not automatic retrieval or message-delivery instructions.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms.

- **reconcile-offer-acceptance** — per-job and pooled acceptance calculations, a comparison table and a discrepancy ledger.
- **list-outstanding-offers** — a dated sent/unresolved queue, separate ambiguous histories and a coverage explanation.

Supply Activity accepted/rejected/outstanding counts and Details application/job references, status, creation/sent/resolved dates. Keep history/migration settings, export time and reporting-user scope. Redact names, salary terms and contact details when identifiers suffice. In Greenhouse: Reports → Essential reports → Offer Activity or Offer Details → Filters and more → Apply, then supply the export. Existing authorized report access is needed only to obtain exports.

Offer analysis uses supplied text/files and embedded reference knowledge. Public source rechecks are the separate retrieval exception described above. No telemetry, connectors or account changes. Read [PRIVACY.md](PRIVACY.md) for data handling.
