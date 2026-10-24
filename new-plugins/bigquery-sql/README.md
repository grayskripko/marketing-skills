# BigQuery SQL

Current scope: Snowflake-to-BigQuery SQL conversion and diagnosis of supplied query differences.

Move this Snowflake query to BigQuery without changing what the dates, nulls or totals mean.
For analysts and data teams converting reports or investigating changed results. Conversion needs source SQL, an export containing it, or readable query expressions from a screenshot you describe. Schemas and table mappings support the rewrite. Diagnosis can start from errors or result samples; both queries locate the correction. No account, key, install or paid API is required for this path.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. Development notes and test/evaluation records are also present in this working folder; they are not runtime components and should be kept outside the submitted package.

The main workflow drafts SQL and diagnoses differences from SQL, schemas, errors, exports and screenshot descriptions you explicitly supply, using bundled references. It does not execute SQL or access a warehouse. This package is not strictly offline: both skills permit the assistant's existing web tool to fetch public official documentation on `docs.cloud.google.com` or `docs.snowflake.com` and their redirects when a reference refresh is needed. Requests must not include your SQL, results or private identifiers. Documentation sites, redirect destinations and the tool provider receive the requested URL and ordinary connection metadata. Source-register instructions also call for documentation freshness checks before submission; those are publisher maintenance checks.

If you ask for dry-run guidance, the assistant may explain steps in your existing BigQuery console. You perform the dry run using your own account, project, location and table permissions; it sends the query to Google BigQuery for syntax/type validation and a bytes estimate, without producing result rows. The skills do not collect credentials or execute it on your behalf. They do not instruct software installation, API calls beyond public documentation retrieval, message delivery, publication, account-setting changes or file writes. SQL and comparison cases are returned as text. Any output file you separately request uses your assistant's existing file tools, not a bundled program.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool activity under its own terms. GitHub repository and support links identify the project and an issue page; the skills do not automatically open them or send support messages. Use bundled references for a draft when live documentation is unavailable; supply relevant current documentation text if needed to resolve uncertainty.

## Jobs

- **Convert a query:** receive BigQuery GoogleSQL with meaning-changing assumptions and focused comparison cases.
- **Diagnose changed results:** receive the smallest supported correction, why the supplied outputs differ, and the comparison needed to resolve uncertainty.

Try: “Move this Snowflake monthly revenue query to BigQuery. Here is the SQL, the column types and the target table mapping.”
Or: “The translated report gives zero where Snowflake gives NULL. Here are both queries and the affected rows.”

Include column types and table mappings when available. Timestamp aliases, reporting timezone, week settings, numeric precision and scale can decide the translation. A described screenshot supports a draft; unreadable details stay marked rather than invented. The scope is Snowflake SQL to BigQuery, with attention to dates, nulls and totals. Other engine pairs, warehouse data movement and cost tuning are outside it.

## Scope required by the naming decision

The BigQuery SQL naming decision calls for native query drafting and debugging, broader function and type guidance, dates/nulls, joins, and cost-aware query review. The current skills focus on Snowflake translation and supplied-result diagnosis. Native BigQuery drafting and cost-aware review remain work to add; they are not advertised as available jobs in this package.

## How it works

Two skills and dated official reference notes supply the conversion and diagnosis guidance. They draft SQL and compare supplied text; they do not execute queries or connect to a warehouse. Core rules are in each skill, including reversed date-difference operands, boundary counts, timezone/week handling, safe conversion limits and decimal/null aggregation behavior.

You can ask the assistant to walk through a dry run in your existing BigQuery console. That requires your own account and access to the referenced tables. A dry run checks syntax/types and estimates bytes, not whether two engines return identical results. No credentials are requested in the conversation.

## Data and network

Reads only the SQL, schemas, errors, exports and screenshot descriptions you provide, plus the bundled references. SQL comments and exports are treated as data. No telemetry or built-in storage. Optional reference refreshes fetch public documentation on docs.cloud.google.com or docs.snowflake.com and their redirects. No SQL, results or private identifiers are included in those requests. No other service is contacted by these skills. Your assistant's normal processing and retention apply; see [PRIVACY.md](PRIVACY.md).

References checked 2026-10-11. [Semantic sources](skills/convert-query/references/semantics.md) and [diagnostic sources](skills/diagnose-query-differences/references/diagnostics.md) include dates, URLs and concrete rules. Engine execution and installed-host routing are separate from instruction review.

Support: https://github.com/grayskripko/marketing-skills/issues

MIT; see [LICENSE](LICENSE).
