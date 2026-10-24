# Slack export coverage notes

Verified/read 2026-10-11. No last-updated date was shown. Recheck official documentation before a later release. Current documented options do not establish historical user settings.

## Export contents

[How to read Slack data exports](https://slack.com/help/articles/220556107-How-to-read-Slack-data-exports), read 2026-10-11.

Public-only/all-conversation exports use JSON; single-user exports may use TXT. Enterprise workspace scope excludes multi-workspace channels. Missing conversation folders can reflect no retained messages within selected dates. JSON file links lack file contents. Single-user TXT includes the selected user's files and other participants' conversation messages. Canvas links/comments are separate material.

## Retention

[Customize data retention in Slack](https://slack.com/help/articles/203457187-Customize-data-retention-in-Slack), read 2026-10-11.

Paid defaults keep data for workspace lifetime; custom policies and conversation overrides differ. Free offers 90 days or one year, subject to the Enterprise-sponsored Slack Connect message exception. Daily deletion is permanent and includes pinned/saved items. Edit/deletion logs depend on settings. Business+ can hide messages while retaining them in approved all-conversation exports. Deleted channels lose messages/revisions regardless of retention. Canvas exports ordinarily contain the latest version; version-history export requires all-conversation access. Access alone does not establish that earlier versions were supplied.

## Access and setup

[Export your workspace data](https://slack.com/intl/en-us/help/articles/201658943-Export-your-workspace-data), read 2026-10-11; English localized URL loaded after a direct canonical URL error, resolving to the canonical article.

Public-channel exports exist on all plans; additional self-serve exports depend on plan, role and approval. Free file links cover the last 90 days. Workspace path: Admin → Workspace settings → Security → Import & export data → Export. Enterprise path: organization settings → Security → Exports. Select date/scope and download when ready. The assistant explains steps without operating the account.

## External participants and historical loss

[Guide to Slack import and export tools](https://slack.com/intl/en-us/help/articles/204897248-Guide-to-Slack-import-and-export-tools), read 2026-10-11; English URL resolves to canonical article.

Slack Connect file-link coverage depends on the sharing member's workspace/org and export type. Upgrading cannot restore data deleted beforehand. The guide describes limited-circumstance applications on Free/Pro, while the export-options table does not list ordinary self-serve all-conversation exports there. Do not claim these exports are impossible or promise access; refer an owner to Slack if the exception matters.

## Local analysis conventions

Authored rules of thumb, not Slack policies: separate observed exclusions, unknowns and possible causes; state each gap's effect on the user's task; ask for the smallest relevant evidence. Do not infer deletion, agreement or whole-workspace completeness from absence. No completeness percentage without an independently defined expected population. Bundled notes require no network requests at runtime.
