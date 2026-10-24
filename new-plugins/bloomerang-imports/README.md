# Bloomerang Imports

Check a Bloomerang donation CSV before import for missing fields, donor matches, unsupported records and file limits.
For nonprofit staff preparing Bloomerang CRM imports. Give it pasted CSV rows or exported files; add constituent exports and configured fund values when available. No account, keys, paid API or installation beyond loading the plugin is required for these checks.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not connectors. The current folder also contains development notes and text/CSV/JSON evaluation records; those are not runtime components.

By default, these skills use text, attachments and local files you explicitly supply. They permit your assistant's existing tools to parse CSVs, count records and serialized bytes, reconcile amounts, and write requested corrected CSVs, held-row files and trace records to your chosen destination. This may involve host code execution; no executable program is bundled, no software installation is instructed, and CSV cells and their links must never be executed or followed. Tool execution and temporary files are managed by your assistant provider.

If you explicitly request a current-rule check, both skills may retrieve public HTTPS article pages on `help.bloomerang.com` and that site's `robots.txt` using your assistant's existing web tool. These requests disclose the requested URL and ordinary connection metadata to that site and the tool provider. Off-domain redirects and logins are prohibited; blocked access falls back to article text you supply. There is no web search, API integration, account connection, automatic upload or donor-data network transfer. Source article URLs can be retrieval targets only in this requested check; repository and support URLs identify the project and support page.

The skills return analysis and prepared files. Preview review, downloading skipped records, manual field entry and any small test or final import are actions for the operator in Bloomerang CRM; the skills do not perform account operations, send messages, publish content or change account settings. Operator-run imports can create CRM records and, when configured, trigger donation acknowledgements.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool activity under its own terms. Requested output files are created by your assistant's existing file tools and remain under your control.

| Skill | Ask for | Result |
|---|---|---|
| bloomerang-import-check | Check this donation CSV before import; explain these skipped-record errors | Readiness decision, affected rows, matching evidence and exact repairs |
| bloomerang-import-prepare | Fix these donation rows and split people from organizations | Separate CSVs, field mappings, held rows and reconciled counts/amounts |

## How to use it

1. Paste the CSV or supply the export. Say whether donors are existing, new, or mixed, and whether any gifts were already imported.
2. Add a constituent export with account numbers and relevant matching fields, and the fund/custom-value list if available. Say whether the export is complete.
3. Ask for a preflight or corrected files. Unresolved rows remain visible with the detail needed to resolve them.
4. Review the returned mappings and files. In Bloomerang CRM, use separate donation import templates for individuals and organizations and review the preview before running the import. Actual account operations are performed in Bloomerang CRM by the operator.

The embedded rules cover the 10,000-row/2MB limits, creation names versus matching evidence, supported import types, existing configured values, date/amount errors and the fact that donations are created rather than updated. Files keep IDs as text and each donation on its own row. A partial export cannot establish that a donor is new.

This package handles Bloomerang CRM donation imports. Fundraising offline gifts, peer-to-peer participants, Volunteer imports, giving-total reconciliation and account merging are separate jobs.

See [PRIVACY.md](PRIVACY.md), [LICENSE](LICENSE), and the dated [source register](skills/bloomerang-import-check/references/bloomerang-import-rules.md).
Support: https://github.com/grayskripko/marketing-skills/issues
