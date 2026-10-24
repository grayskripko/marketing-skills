# Attio Imports

Move this CRM export into Attio without losing links or making duplicate people.
For people moving contacts, companies and deals into Attio. Give the assistant pasted tables, CRM exports, or screenshots described in text. Preparing files requires no account, keys, install or paid service; uploading them requires an Attio workspace and appropriate import permissions.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON platform metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The .claude-plugin and .codex-plugin directories contain platform metadata, not executable runtimes.

These skills analyze task text, attachments, screenshot descriptions and local files that you explicitly supply. They may use your assistant's existing local file and data-processing tools to prepare CSVs, preserve original and held rows, and validate supplied files. Preparation instructs use of a proper CSV writer and full-file local validation when tools exist; this may involve host code execution, although no code or named command is bundled. Transformed output files are written only at your chosen destination; temporary files and tool execution are managed by your assistant provider. The skills do not direct software installation.

When current documentation is needed, both skills permit your assistant's existing web/search tools to fetch cited public https://attio.com/help pages or relevant official help pages found on that site, using generic searches restricted to that site. The requested URLs, generic search terms and ordinary connection metadata are processed by Attio's site and the assistant's web/search providers as applicable. CRM rows, personal identifiers and private task context are not included in those requests; links embedded in CRM rows are not opened. This optional documentation lookup makes network requests. Preparation can otherwise use supplied data and bundled references without documentation retrieval.

The skills do not call Attio account APIs, log in, connect to a CRM or migration service, upload exports, send messages, publish content, execute imports or retries, or change account settings. They can explain user-performed imports, scoped UI corrections and cancellation, and the optional documented Import2 migration setup. If you follow those instructions yourself, uploading an import sends your reviewed CRM file to Attio; choosing Import2 involves a separate service and its account/data handling. Neither action is performed by this package. GitHub source, privacy and support URLs identify documentation or support pages; they are not runtime connection instructions.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments, tool activity and generated files under its own terms. See [PRIVACY.md](PRIVACY.md).

| Skill | Result |
|---|---|
| attio-import-prepare | CSVs, column mappings, matching keys, held rows and ordered import steps |
| attio-import-repair | Error diagnosis, corrected mapping and a narrow retry plan |

Ask “Get my contacts and opportunities ready for Attio” or “Why did this import lose company links?” Existing Attio exports help check matches. Sample rows support a sample assessment; they cannot establish that the entire export is safe.

The assistant prepares and explains. You review the files and perform the import through Attio's official UI. CSV cannot import notes or tasks. An optional documented migration service can be explained if requested; no connection is included.

## Import scope

| Area | Coverage |
|---|---|
| Supported objects | People, Companies and Deals; object records and list entries are mapped separately. Custom-object preparation requires the supplied destination schema, required attributes, unique keys and rules. |
| Multi-select fields | Commas separate labels; labels cannot contain commas. Imported values append to existing selections. |
| Relationship mappings | Resolve source foreign keys first, then map linked unique attributes or actual Attio Record IDs. Multi-value relationships accept unique linked attributes; other linked fields need a separate object import. |
| Update behavior | Match verified unique keys or existing Record IDs. Blank cells preserve values; multi-values append. Use Update existing for lists and Entry IDs for specific repeated entries. |
| Error recovery | Diagnose required values, missing IDs, multiple matches, rule failures, invalid formats and partial results; prepare retries from confirmed failed or unapplied rows. |

## Verification checklist

Before import:

- Confirm destination objects/lists, required fields, matching keys and relationship targets.
- Check all supplied rows, CSV limits, multiselect labels, dates, owner/stage values and held conflicts.
- Compare column mappings and raw/mapped values; check the preview and list update setting.

After import or repair:

- Reconcile distinct source keys with created, updated, skipped and failed results.
- Inspect company/person/deal links, representative field values and repeated list entries.
- Compare fresh supplied exports or UI results before preparing a retry; retain originals and held rows.

Official facts were checked 2026-10-11; see [sources](references/attio-imports.md). Recheck relevant official documentation when material import behavior is uncertain or may have changed.

MIT. See [LICENSE](LICENSE). Support: https://github.com/grayskripko/marketing-skills/issues
