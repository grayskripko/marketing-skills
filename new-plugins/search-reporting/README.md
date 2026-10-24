# Search Reporting

Explain Google Search Console AI impressions and why chart and page totals differ.
For agencies and freelancers preparing client search reports. Needs pasted report text or user-supplied chart/table exports, filter labels and original unavailable-value symbols. No account, keys, installs or paid API are required.

## What this package runs and connects to

This skills-only package contains Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The Claude and Codex manifests describe the same skills for their respective hosts; neither configures a connector or server.

The assistant reads only task text, attachments and local files you explicitly supply, plus bundled references. Both skills say “Fetch nothing”: they do not direct assistant web searches, URL or robots.txt retrieval, API calls, software installation, message delivery, publishing or account-setting changes. Source and support URLs are references, not assistant connection endpoints; supply relevant text when a rule needs updating.

This is not a strict no-execution or pasted-text-only workflow. Your assistant may use its existing local calculation tools on supplied data; execution and temporary files are managed by your assistant provider, with no bundled calculation program or requested network access. Reconciliation may create an audit/report file when you explicitly request one, using the assistant's existing file tools and your specified format and destination; it must not overwrite raw exports. No delivery or publication is instructed.

Some next steps require you to use Google's online Search Console yourself: the impressions skill recommends selecting the property, trying the official report-opening link and inspecting Settings → Search generative AI without changing it. Reconciliation recommends a separate rare-value filtered capture or matching chart/table exports when evidence is missing. Those user actions contact Google under your own account; the assistant does not open the report, connect that account or fetch those captures. Public Google Help and GitHub support links can also be opened by you.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain conversation, attachments and tool outputs under its own terms. Requested output files remain under your control.

| Skill | Request | Result |
|---|---|---|
| generative-ai-impressions | Explain what a generative-AI report counts, using its supplied title and filters | Client explanation with the supplied scope |
| search-export-reconciliation | Check why chart and table totals differ | Client table; requested source ledger and calculation record |

Keep report title, property, dates, search type and filters with each export. Copy `~` or `-` from the screen before exporting; export zeros alone cannot recover those symbols. Include preliminary-data notes and file/sheet/cell locations when available. For several exports, identify repeated rows so they are not added twice. Files may be CSV, spreadsheet text or pasted tables; use inputs the assistant can read.

Official source rules were verified on 2026-10-11; the dated register is linked from each skill. See the execution and connection disclosure above and [PRIVACY.md](PRIVACY.md).

## Examples

- “Explain these AI impressions to my client: dedicated Search AI chart 240, complete week, text-based, no filters.”
- “Reconcile these chart and page exports for my client; include an audit file linking each figure to its source cells.”

## Support and license

[Support](https://github.com/grayskripko/marketing-skills/issues). MIT; see [LICENSE](LICENSE). See [PRIVACY.md](PRIVACY.md) for data handling.
