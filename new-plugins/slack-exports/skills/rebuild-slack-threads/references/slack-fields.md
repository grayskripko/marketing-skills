# Slack export field notes

Verified/read 2026-10-11. No last-updated date was shown. These notes describe documentation available that day.

## Official sources

- [How to read Slack data exports](https://slack.com/help/articles/220556107-How-to-read-Slack-data-exports), read 2026-10-11: conversation folders contain daily JSON history; indexes resolve member/conversation IDs; Enterprise uses org_users.json. TXT loses thread boundaries. Export edit/deletion records use original_ts, previous content and event ts; records live on the event date and depend on retention. TXT timestamps are GMT. TXT Message edits logs retain event time/actor, original message time and historical text; updated wording is in Messages. Deletion logs retain removed text. Reaction user lists can be incomplete. JSON file links are not file bytes; single-user TXT includes files sent by the selected user.
- [Retrieving messages](https://docs.slack.dev/messaging/retrieving-messages/), read 2026-10-11: thread_ts equals ts for a parent and differs for a reply. Parents retain thread_ts after replies are deleted. The sample replies array is deprecated; metadata stubs are not reply contents. Developer payload guidance does not establish that every export contains every field or authorize API access.
- [Message event](https://docs.slack.dev/reference/events/message/), read 2026-10-11: subtypes distinguish bot posts, conversation lifecycle and revision events. Event payloads and help-page export records can have different shapes. Do not force event wrappers onto export examples.

## Local analysis conventions

Authored rules of thumb, not Slack policies: preserve timestamp strings; join within workspace and conversation; sort exact decimals; keep source provenance; merge identical copies without discarding conflicts or revisions; flag absent parents; require supplied evidence for a decision. An explicit approval-reaction convention can establish approval only within its supplied scope and attribution; emoji alone does not define approval. Merge broadcast copies only when identity and content support it. Reply-count discrepancy measures metadata versus supplied unique replies, not permanent deletion; snapshots may differ.
