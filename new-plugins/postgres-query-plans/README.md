# Postgres Query Plans

Explain this slow Postgres query plan and tell me which change has evidence behind it.
For developers and database maintainers using PostgreSQL EXPLAIN.
Needs a pasted plan, an exported plan file, an attachment, or screenshot details you describe. No database account, API key, database connection, or additional SQL client is needed to analyze a supplied plan.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. The current folder also contains text-only development notes and evaluation records. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The Claude and Codex manifests describe the same skills for their respective hosts; neither launches a connector.

Analysis uses plan text, exports, attachments, and screenshot details you explicitly supply. The skills do not execute SQL, install software, connect to a database, call database APIs, upload plans, send messages, publish content, or change account settings. They can use the assistant's existing web tools to fetch relevant public documentation under https://www.postgresql.org/docs/ when a refresh or server-version check is needed; redirects must stay on that site, and requests must never contain supplied SQL, plans, identifiers, or private context. These are real retrieval instructions, not merely source links. Manifest homepage and repository links identify the project and are not workflow endpoints.

The skills can propose SQL and guide you through your existing SQL client: EXPLAIN, EXPLAIN ANALYZE, controlled before/after tests, targeted ANALYZE, candidate indexes, and transaction-local memory or timeout settings. You run any approved test yourself; the assistant does not execute it. EXPLAIN ANALYZE runs the statement and can add load or cause side effects; read-only transactions and ROLLBACK do not contain every external effect.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain your conversation and attachments under its own terms. Documentation requests reach the public documentation host through your assistant's web tools. No skill directs extra local copies or output-file writes.

- **Explain a plan:** separate measured work from estimates; identify repeated scans, bad row estimates, spills, and the smallest supported test.
- **Compare plans:** assess an index, rewrite, or setting change using before/after measurements and query-result requirements.

Include the SQL, PostgreSQL version, parameter values with sensitive literals removed, index definitions, and full plan when available. Partial inputs still get a bounded answer. Redact identifiers and values consistently so relationships remain readable.

Text and JSON exports work directly. XML/YAML exports can be read as supplied text. A screenshot description supports only the fields you describe; unseen nodes are not inferred.

If you need to collect a plan, the agent can walk you through your existing SQL client. Plain EXPLAIN provides estimates. EXPLAIN ANALYZE executes the statement, including side effects, and may impose substantial load. Discuss a safe environment before gathering actuals. The agent does not execute SQL or install a client.

Embedded references were checked on 2026-10-11; official current documentation identified PostgreSQL 18. Version-specific options must be checked against your server version. No claim is made about a later release.

[Privacy](PRIVACY.md) · [License](LICENSE)
