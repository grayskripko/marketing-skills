# Privacy: API Deprecations

Check API deprecation notices and retirement dates against response headers and supplied policy, or draft a retirement notice and migration guide from approved endpoint changes.

This package contains skills and reference text. It operates inside the assistant handling the conversation.

- Data read: pasted API documentation, response header samples, dates, policy text and local exports the user selects. These may contain customer identifiers, internal URLs or account details; redact those fields and credentials before use.
- Purpose: identify lifecycle scope/date conflicts and draft replacement notices and migration passages.
- Recipients: the assistant provider processing the conversation. The plugin sends data to no external service.
- Network scope: none. Official-source URLs in bundled references are citations and are not fetched. No connectors, searches, endpoint calls or account access.
- Storage: no plugin storage, logs or telemetry. Conversation and uploaded-file retention follows the assistant provider's settings. Requested deliverables can be saved locally by the assistant when the user asks.
- Controls: supply only needed excerpts, remove authorization headers, cookies, signed URLs and personal identifiers, and use the assistant's conversation/file deletion controls.
