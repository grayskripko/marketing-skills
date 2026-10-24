# Slack Exports

Read this Slack export, rebuild the threads, and tell me what this archive leaves out.

For people reviewing old team discussions. Give the assistant Slack JSON/TXT exports, pasted records, an archive inventory, or screenshots described in your own words. No account, keys, paid service or installation is needed for analysis.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable runtimes.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

If you need an export, `check-slack-export-gaps` explains user-performed steps in Slack: an authorized owner/admin opens workspace Admin → Workspace settings → Security → Import & export data → Export, or Enterprise organization settings → Security → Exports, selects scope/dates and downloads the export. Additional export access may require contacting Slack for approval. Those actions use your browser and Slack account and connect to Slack; the assistant does not perform them. Analysis of an already supplied export requires no additional network requests. The bundled coverage notes also ask the publisher to recheck official Slack documentation before a later release; that maintenance check is separate from task analysis.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program. The skills themselves do not direct file writes.

| Skill | What you get |
|---|---|
| rebuild-slack-threads | Parent/reply history, source-linked decisions and missing context |
| check-slack-export-gaps | Coverage findings for dates, conversations, retention and attachments |

Channel and user mapping uses supplied indexes or explicit mappings; unresolved IDs remain visible. Timezone handling preserves exact timestamps and uses UTC for JSON unless a known zone is requested; Slack TXT uses GMT. Summaries are source-linked to supplied records. Coverage findings distinguish missing/deleted content, export type, selected dates and retention constraints.

JSON can support confirmed thread links. TXT gives a flattened chronology; a screenshot description supports only the content and relationships you describe. Missing messages stay missing. File links are not document contents. These skills analyze supplied archives and do not connect to Slack or recover deleted data.

Ask: “Put these replies back under the original messages,” “What did this discussion actually decide?” or “Can this export tell me what happened in DMs?” For a combined request, the history and relevant gaps come together.

## Data and network

Archive URLs, attachment links and canvas download links are not fetched. Analysis uses only material you supply and bundled official reference notes. Reading supplied files does not authorize running code or retrieving remote content. User-performed export/setup actions and assistant-provider processing are described above. Redact irrelevant names, email addresses and private links while preserving stable pseudonyms and timestamps needed to join replies.

## Documentation and support

See [PRIVACY.md](PRIVACY.md), [BUILD-NOTES.md](BUILD-NOTES.md), and the references linked from each skill. Questions: https://github.com/grayskripko/marketing-skills/issues

MIT; see [LICENSE](LICENSE).
