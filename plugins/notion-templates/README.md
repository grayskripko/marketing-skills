Design Notion templates and databases for your workflow, fix formulas and prepare import-ready CSV from pasted notes or exports.

# Notion Templates

For people turning a recurring process into a tracker. Paste the workflow, existing property names and types, or exported rows. Drafting needs no account, paid API or installation. Applying the design requires your own Notion account; CSV import uses desktop or web.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable runtimes. Development notes and test records are documentation, not runtime components.

These skills work from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. Source and support URLs are references, not retrieval instructions; supply the relevant content rather than a URL alone.

The CSV skill instructs the assistant to validate the final CSV with a real CSV reader when available, comparing headers, fields and record counts with the supplied source. This may use the assistant's existing local code or file tools; no parser or runtime is bundled and no installation or network access is requested. If a reader is unavailable, the skill directs field-by-field inspection without claiming parser execution. All three skills permit reading user-selected files and creating explicitly requested local output files when the host supports them. Execution and temporary files are managed by the assistant provider.

The skills also give manual Notion setup steps: the user creates databases, properties, views and templates, imports CSV through Notion desktop/web, and checks formula drafts or sample records in a scratch database. These user actions can connect to Notion and change the user's workspace; the assistant does not perform them or claim they succeeded. Notion receives the content the user enters or imports under its own terms.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool outputs under its own terms. Requested local output files are created by the assistant's existing tools and remain where the host saves them.

| Skill | What you give | What you get |
|---|---|---|
| notion-template-design | Workflow and constraints | Databases, property types, views, relations, rollups and reusable page content |
| notion-formula-fix | Formula, property types, desired behavior and sample rows | Copyable expression and boundary checks |
| notion-csv-prepare | Table or export and target schema | UTF-8 CSV, property map and post-import setup steps |

Try: “Make a tracker for our equipment loans.” “Fix this completion percentage when Total is zero.” “Turn these rows into a Notion CSV.”

CSV is a row import, not a complete workspace template. Relations, formulas, rollups, views and reusable page content have separate setup steps. CSV imports add rows rather than updating existing records. Formula drafts include sample checks to run in a scratch database before use.

Redact unrelated personal details and never provide passwords or tokens.

See [PRIVACY.md](PRIVACY.md), [LICENSE](LICENSE) and the source notes linked from each skill. Support: https://github.com/grayskripko/marketing-skills/issues
