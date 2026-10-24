# Ramp Exports

Map a Ramp accounting export to the supplied target template, checking source-page state, transaction/refund layout and dimension headers.
For finance operations teams preparing accounting import files.
Needs pasted text or a readable export, target headers, and any required account or dimension lookups. No account access, keys or installation beyond the plugin is needed.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. The folder also contains development notes and evaluation records; these are not a runtime. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable servers.

Routine mapping and export-state analysis use only task text, attachments, and local files you explicitly supply, plus the bundled rule registers. The skills do not direct code execution, software installation, API calls, account access, message delivery, publishing, or remote writes. Requested CSV or other output files are created by your assistant's existing file tools, not by a bundled program. Instructions about Ramp customization, syncing, resets and ERP imports are guidance for the user; the skills do not perform those operations.

An explicit documentation-refresh request permits network retrieval through your assistant's existing web tool of these five official articles and `https://support.ramp.com/robots.txt`:

- `https://support.ramp.com/custom-accounting-csv-exports/`
- `https://support.ramp.com/exporting-your-data-to-csv/`
- `https://support.ramp.com/universal-csv-overview/`
- `https://support.ramp.com/marking-transactions-as-synced/`
- `https://support.ramp.com/quickbooks-desktop-file-export-overview`

Same-host redirects are allowed; another host requires a new user instruction. These requests disclose the requested URL and ordinary connection metadata to Ramp's support site and the assistant's tool provider. Supplied financial rows, personal information and credentials are not included in requests. This optional refresh makes network requests; routine supplied-material analysis does not. If refresh is unavailable, use the bundled dated guidance and supplied evidence, identifying any unresolved current behavior. Other source, publisher and support links identify references, not additional retrieval permissions.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments, retrieved pages and requested output files under its own terms.

## Skills

- **map-accounting-export** — produce a target-ordered column map and transformed rows, with unresolved cells identified.
- **check-export-state** — explain missing rows, unchanged queue state or readiness blockers from supplied page text and export history.

Paste the originating page and tab, selected filters, accounting integration, exact export action, layout/refund setting and a purchase/refund sample. Supply target field meanings as well as headers when names are ambiguous. Partial evidence still yields a partial mapping.

Built-in guidance covers signed versus typed refunds, double-line requirements, generated dimension names, preview versus committed exports, and manual-export reset behavior. Custom CSV settings cover card transactions and Bill Pay; reimbursement customization follows a different boundary.

[Privacy](PRIVACY.md) · [License](LICENSE)
