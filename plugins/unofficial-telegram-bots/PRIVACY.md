# Privacy — Unofficial Telegram Bots

This package contains instructions and reference text. It runs no service, bundles no executable integration and has no telemetry.

- Data: supplied messages/files may contain names, roles, timestamps, message IDs and attachments. The skills use only the requested scope and avoid repeating unrelated personal information. Do not provide full account archives or credentials.
- Purpose: choose a Telegram integration, prepare requested notifications, and analyse permitted conversation material.
- Recipients: the assistant provider processes conversation and supplied files under its own terms. An optional authorized send transmits the message and destination to Telegram and the chosen recipient/chat. The selected transport authenticates privately with Telegram; secrets must not enter conversation or logs.
- Network scope: route selection and export review fetch nothing. Optional bot calls go only to `api.telegram.org`: `getMe` (identity), `getWebhookInfo` (webhook status), bounded `getUpdates` on a new unused bot if needed (selected incoming marker/chat metadata), `getChat` and `getChatMember` (target/permissions), and authorized `sendMessage` (destination and exact text). No website or robots.txt fetch, web search, remote media download or MTProto request.
- Retention: the package itself stores nothing. The assistant's conversation/file retention applies. User-selected connectors or local clients may retain configuration, API results or logs; configure minimal retention and secret redaction. Export analysis may create local scratch files only as needed; remove temporary copies after use without deleting the originals.
- Controls: supply the smallest permitted excerpt, use role aliases, and omit contact details. Delete assistant conversations/files through its controls. Revoke a leaked bot token in BotFather. Do not share account session files.
- Permission: exporting or redacting does not grant AI-processing rights. Third-party Telegram material needs a specifically permitted context; consent is not an automatic exception under Telegram's content terms. A deployed bot needs an accessible policy covering its actual data use: Telegram’s standard policy applies by default, but a custom policy is required if it does not fit. Required consent depends on the data use; this notice describes only this package.

Questions: https://github.com/grayskripko/marketing-skills/issues
