# HubSpot Imports

Check this spreadsheet before I import it, map the columns, and tell me what will update or duplicate.

For people preparing HubSpot contact, company, deal, and ticket imports. Needs pasted rows, a supplied spreadsheet/export, or screenshot details you describe. No installation, keys, paid API, or account connection is needed for analysis. Importing the result requires a HubSpot account with Import and object Edit permissions.

- **Prepare HubSpot Import:** column mappings, required fields, file limits, value fixes, and supported associations.
- **Predict HubSpot Import:** row-level update/create/ignore/error forecasts, overwrite risks, repeated identifiers, error-export repair plans, and post-import checks from supplied results.

Paste the headers and representative rows, say which objects you intend to import, and whether you want to create, update, or both. To check existing-record matches, supply a recent HubSpot export with Record ID and the relevant matching properties, including secondary emails/domains when those identifiers are used. Record coverage and identifier-value coverage both matter. Keep identifiers consistent if you redact them. Described screenshots support only the information you describe; they cannot establish full-file counts.

The result is a mapping table, fixes, and a manual import handoff. Predictions are conditional on your selected settings and export coverage. Blank spreadsheet cells do not clear existing values. A mapped Record ID takes precedence over email and domain matching.

The agent can walk you through exporting records, checking property options, and choosing the import mode in HubSpot's interface. It does not log in or run the import. You can use pasted text throughout.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON platform metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable servers. Build and review notes are development documentation.

The skills analyze task text, attachments, and local files you supply, using bundled import rules. They can optionally use your assistant's existing web tool to refresh public documentation at `https://knowledge.hubspot.com` and follow those pages' public redirects. This optional path makes network requests: the requested public URL and ordinary connection metadata are disclosed to the contacted sites and the assistant's tool provider. No spreadsheet rows, CRM identifiers, private account links, or credentials are sent in those requests. Other source and support links identify references or project pages; they do not authorize account access. Without a refresh, analysis uses the supplied material and bundled references; if current rules cannot be confirmed, supply the relevant official passage or account option.

The skills may read supplied local files and create corrected CSV blocks or local output copies for the requested deliverable through your assistant's existing file tools, preserving originals. They do not direct code execution, software installation, API calls, account connections, message delivery, or automatic imports. They can guide you to export records, check account properties and import settings, create a needed property, edit a specific association label when requested, and run the prepared import or targeted retry manually in HubSpot. Those user actions access and may change your HubSpot account; the plugin does not perform them. Automatic sample-file downloading is outside the advertised workflow.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain conversations, attachments, web requests, and tool-created files under its own terms. Local output copies are managed by your assistant's existing tools, not a bundled program.

## Complete import preparation workflow

Use this sequence for contacts, companies, deals, and supported associations; ticket preparation is also covered.

1. **Define the import.** Supply the file or rows, objects, create/update intent per object, and relevant property options. For existing-record checks, supply a recent export with Record IDs and all matching values. Record sample limits and missing account options before forecasting outcomes.
2. **Map and identify.** Prepare HubSpot Import maps every column to its object/property, identifier, association label, join key, or exclusion. Check creation fields for each object, pipeline/stage options for deals, and the chosen matching identifier. Company names and deal names alone do not establish existing-record matches.
3. **Resolve duplicates and associations.** Predict HubSpot Import groups repeated object identifiers, flags conflicting property values, and compares supplied existing records. Keep intentional rows linking the same record to different records. For one-file or two-file associations, check both objects' identifiers, shared keys where needed, and label prerequisites and placement. Return ambiguous identities as exceptions for a decision.
4. **Prepare the handoff.** Produce the mapping, unambiguous corrected rows when requested, an exceptions table, and selected manual import settings. Include create/update modes, identifiers, excluded columns, formats, overwrite choices, and association joins/labels. The user runs the prepared import in their account.
5. **Review results and repair errors.** Supply the completed import summary, error export, actual settings, and a fresh export of affected records. Predict HubSpot Import separates whole-record failures from property or association failures and prepares a targeted retry using verified identifiers. Preserve successful records and intentional relationship rows.
6. **Check after import.** Compare the supplied result with the prepared mapping and forecast: created/updated/ignored/error counts per object, Record IDs, changed and preserved properties, deal pipeline/stage values, expected relationships and labels, and remaining duplicate risks. Count distinct records separately from relationship rows; identify overlapping error groups. Report differences, unresolved coverage, and the affected retry scope. Request missing relationship evidence rather than infer that links succeeded from record counts alone.

The deliverable is a preparation and verification packet based on supplied files and results. Account execution stays with the user.

## Data and network

Reads only supplied text and files needed for the task. No telemetry or separate storage service. No account requests or data uploads. Optional freshness checks fetch public articles under `knowledge.hubspot.com`, including their public redirects. No spreadsheet contents or identifiers are sent in those requests. Offline analysis uses the bundled [source register](references/hubspot-import-rules.md).

[Privacy](PRIVACY.md) · [License](LICENSE)
