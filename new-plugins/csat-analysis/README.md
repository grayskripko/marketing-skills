# CSAT Analysis

Check customer satisfaction (CSAT) survey counts, compare two periods and propose improvement tasks backed by ticket cases.

For support managers and operations teams. Paste text or provide readable CSV files you are allowed to use. Include ticket and response IDs that stay the same across exports, the rating scale, which ratings count as positive and period dates. No additional service account, API key, paid API or installation beyond loading the plugin is required. Your AI host's usage charges still apply. It does not connect to your helpdesk or change tickets.

## What this package runs and connects to

The skills analyze only task text, attachments and readable local files you explicitly supply. They forbid web searches or URL retrieval, including supplied URLs, and do not direct software installation, API calls, account connections, message delivery, publication or ticket changes. Source and support URLs identify references, not retrieval instructions; paste the relevant content instead. The Zendesk guide describes how to interpret supplied exports, not how to call Zendesk.

All three skills permit local calculations using your assistant's existing tools. Those tools may execute calculations and read supplied files; tool execution and temporary files are managed by your assistant provider. This is therefore a supplied-material workflow with host computation, not a no-execution workflow. Any output file you explicitly request is created by the host's existing file tools. The publisher operates no collection, telemetry or storage service; your assistant provider processes and may retain conversations and attachments under its own terms.

The skill content is Markdown instructions and reference text with JSON metadata and a static SVG icon. The `.claude-plugin` and `.codex-plugin` manifests describe the same plugin for two hosts; neither launches a connector. There are no configured hooks, MCP or LSP servers, installers or background processes. Loading the plugin does not launch the development harness or connect a helpdesk account.


## Skills

| Skill | Give it | You get |
|---|---|---|
| check-csat-data | Surveys, tickets, rating definition and invitation counts if available | Problems matching surveys to tickets, counting decisions and rates the data supports |
| investigate-csat-change | Two periods of checked ratings and ticket evidence | Figures for each period, themes backed by cases and limits of the comparison |
| turn-feedback-into-actions | Comments, ticket findings and approved facts | Proposed tasks, owners, acceptance checks and follow-up measures |

For matching Zendesk exports, bundled official-source mappings distinguish legacy rating states from current survey answers, preserve survey versions and identify the audit-to-response evidence needed for incomplete exports. Sources and verification dates are in the [Zendesk export guide](skills/check-csat-data/references/zendesk-export-guide.md).

## Start here

Ask “Check these ratings before I report CSAT,” “Compare these periods and show what changed,” or “Turn these complaints into improvement tasks.” Paste the relevant rows or attach readable exports. Remove names and contact details. Keep response, ticket and customer IDs distinct. Replace identifying IDs with stable anonymous IDs, using the same replacements across exports.

For a numbered scale, say which scores count as positive. An average rating and the percentage of satisfied respondents are different figures. Include survey invitation counts or records if you want response rates; total tickets are not a substitute. Supply the rule for repeated or updated ratings rather than silently dropping them.

## Data and network

Nothing is fetched, including URLs you supply. No telemetry, live helpdesk connection, background monitoring, sending, publication or ticket changes. The package contains instructions and reference text. The host may read the files you supply and use local calculation tools. It needs working file readers for attachments; paste text if a file cannot be read. No additional connector or paid API is needed.

## How to use the findings

Review the work before acting. The report describes respondents and supplied cases; people who did not respond may differ. Missing ticket matches, repeated ratings and changes in the groups surveyed can limit comparisons. Comments can suggest hypotheses but cannot prove causes. A tone judged from a transcript is not a measured CSAT score. This is an operations review, not an employee ranking or a promise of improved scores.

## Privacy and license

See [PRIVACY.md](PRIVACY.md) and [LICENSE](LICENSE). Support: https://github.com/grayskripko/marketing-skills/issues
