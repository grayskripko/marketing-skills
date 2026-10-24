# Jira Imports

Prepare this CSV so Jira imports the hierarchy and fields correctly.
For people moving work into Jira Cloud. Supply CSV text, an export, or a description of the import screen and errors. Preparation needs no account, keys, or installation. To import the result, you need Jira access and the permissions for your chosen importer.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The Claude and Codex manifests are platform metadata, not connectors.

These skills analyze task text, attachments, and local files you explicitly supply. They may use your assistant's available CSV reader to parse supplied records and create local output files only when requested; those tools are provided by your assistant, not bundled here. The skills do not prescribe shell commands, software installation, or API calls. This is not a strictly offline workflow: for rule verification, both skills permit your assistant to search and fetch public pages on support.atlassian.com and linked official Atlassian documentation, including redirects. CSV contents, logs, identifiers, and attachment URLs must never be placed in those searches or requests. The skills do not fetch attachment URLs or private Jira pages. Source-register links identify documentation that may be retrieved for this verification; GitHub publisher and support links identify project pages, not account connectors.

The skills prepare CSVs, mappings, and instructions; you perform Jira validation, imports, retries, configuration changes, and any Create or customer-request Send actions through your own Jira interface. Those user-operated actions can create or update Jira records, expose mapped comments, send configured notifications, and cause Jira to retrieve HTTP(S) attachment URLs. The plugin does not perform these account actions or verify attachment access itself.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments, tool activity, and local outputs under its own terms. Public documentation searches and fetches use your assistant's existing browsing tools and contact their search service and the requested documentation sites.

| Skill | Your request | Result |
|---|---|---|
| jira-csv-prepare | Prepare my CSV for Jira | Corrected CSV, field and value mappings, blocked rows, import handoff |
| jira-import-repair | Fix this failed Jira import | Row fixes, cause tied to the error, safe retry scope |

The instructions distinguish bulk creation, the administrator's External System Import, and the new import experience. They cover numeric parent IDs, parent-first ordering, header naming, required fields, quoting, repeated columns, date formats, field limits and current error meanings. New service-space imports include reporter and request-type/status checks. Child-only retries require verified existing-target and existing-parent support on the chosen route. When service import controls cannot preserve reporters and request types, it can prepare a small user-operated Create handoff instead. The company-managed hierarchy procedure is separate from team-managed setup.

Paste records directly for a no-setup path. A screenshot description can identify a route or error, but cannot recover unseen CSV rows. Attachments may be supplied if your assistant can read files. Preserve IDs and replace unrelated personal details with consistent aliases; real user identifiers belong only in the final local import file.

An agent can walk you through Settings → System → External System Import, route selection, mappings and validation. It prepares files and instructions; you perform the Jira import. It does not read your Jira account or change configuration. A partial import needs its result log before a retry file can be called safe.

## CSV import coverage

Prepare hierarchy and field mappings for the selected Jira Cloud CSV importer, including assignee/reporter identities, date formats and status values. Compare bulk creation, old administrator import and new import controls before choosing a route. Prevent duplicate creation by reconciling source rows with import results and excluding successful rows from retries.

Attachment columns need HTTP(S) URLs reachable by Jira; local file paths and browser access alone do not establish readiness. Work-item links require the selected link type and Work item ID mapping in the new importer; Parent mappings describe hierarchy separately. Preserve unresolved attachment access and link targets as blockers.

After the user imports, reconcile source, created, updated, failed and unknown counts using the supplied log and result export. Compare the intended parent relationships, assignees/reporters, dates, statuses, custom fields, link types/direction and attachment presence with the resulting work items. Return mismatches and a retry scope that excludes successful creation rows.

Official source records and verification dates are linked from each skill. They were checked on 2026-10-11; review them again before the planned 2026-10-14 submission if documentation changes.

Privacy: [PRIVACY.md](PRIVACY.md). License: [LICENSE](LICENSE).
Support: https://github.com/grayskripko/marketing-skills/issues
