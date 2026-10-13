# Google Sheets Imports

Why is my Google Sheets import stuck, stale or asking for access?
For people troubleshooting Google Sheets IMPORTRANGE. Paste the formula, full error detail and relevant source/destination facts, share a small redacted export, or describe the screenshot. Diagnosis needs no account connection, keys or installation. Applying the suggested repair requires your normal Google Sheets access.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable servers.

Diagnosis uses the formulas, error text, redacted exports and screenshot descriptions you supply. The skills do not direct code execution, software installation, API calls, message delivery, publishing, file writes or account automation. Spreadsheet URLs are formula data and are not fetched. The Google Developers API guide is a syntax reference, not permission to call the Sheets API.

**Documentation verification makes network requests only when you explicitly request it.** In that case, both skills permit the assistant's existing browsing tools to retrieve only these exact reference URLs and their redirects; otherwise they use the bundled references without browsing:

- https://support.google.com/docs/answer/3093340?hl=en
- https://support.google.com/docs/answer/12159115?hl=en
- https://support.google.com/drive/answer/2494893?hl=en
- https://support.google.com/docs/answer/14239833?hl=en
- https://support.google.com/docs/answer/63175?hl=en
- https://developers.google.com/workspace/sheets/api/guides/concepts#cell

These requests expose the requested URL and ordinary connection metadata to the destination sites and the assistant's browsing provider; redirected requests also reach the redirect destinations. User spreadsheet contents are not included. The dated embedded references support diagnosis when browsing is unavailable. Repository and support links identify the project; the skills do not direct their retrieval.

The assistant may advise you to open a source sheet, request owner access, choose Allow access, review sharing/export restrictions, test a formula in an empty area, or edit formulas and prepare an approved-only source or summary. You apply those actions through your own Google account; Google Sheets IMPORTRANGE itself uses the internet to transfer source data. The plugin does not perform those changes or implement Apps Script or Connected Sheets alternatives.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation and supplied files under its own terms.

## What you get

- **Import errors:** a corrected formula or next action for connection grants, missing access, invalid range details, export restrictions and volatile-function errors.
- **Import freshness:** a short repair plan for slow or stale imports, chained dependencies, large ranges and request throttling.

The guidance includes Google's 10 MB per-request cap, creator-wide import usage, hourly update checks while open, named/table range support and the difference between new and existing formulas under export restrictions. It preserves your actual tab names, locale separators and required coverage. It does not promise immediate refresh.

## Using it

Give the destination formula and its full popup error, not only `#REF!`. Describe whether you can open the source under the same Google account, who edits the destination, and any sharing restriction you know about. For stale results, include the source-change time, the destination's last observed value and any intermediate spreadsheets. A CSV export contains values, so also paste formulas and error details separately.

The agent can walk you through Google's own connection and sharing screens. Before connecting sheets, remember that every destination editor may import any part of that source. Use a separate approved source containing only shareable data when needed. Never make a private source public just to fix an import.

[Privacy](PRIVACY.md) · [License](LICENSE)
