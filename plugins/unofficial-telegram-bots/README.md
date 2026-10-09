# Unofficial Telegram Bots

Help set up a Telegram bot and prepare a selected alert. Get setup instructions and message drafts; a live call requires a separately available secure tool.

Independent project; not affiliated with or endorsed by Telegram. Trademarks mentioned belong to their respective owners.

For people who need alerts or answers from a selected conversation.
Needs permitted pasted text or JSON/HTML exports for offline work. Optional live bot calls need a Telegram account to create a bot, a privately configured bot token, and a secure HTTPS-capable tool. No paid API or account connection is needed for supplied text.

This is an independent instructions-only plugin, not an official Telegram product. It ships no sender executable, MCP server, account client, scheduler or persistent listener.

| Skill | Give it | You get |
|---|---|---|
| telegram-route | the job and access you need | Bot API, account-client or export recommendation; setup and risks |
| telegram-bot-notify | destination and exact text, or a setup problem | a draft, concrete HTTP method sequence, or an authorized API-confirmed send through an available secure tool |
| telegram-export-review | permitted export/excerpts and a question | summary, decisions, actions or reply with message references |

## Try it

- “Help me create a Telegram bot and prepare one alert without pasting a token here.”
- “Can a bot read my old private chats, or should I export them?”
- “From these permitted messages, list only agreed actions and cite the message IDs.”

## Setup and no-setup choices

For existing text/files: provide only the relevant permitted excerpt or selected export. Reading supplied text/files needs no additional install or keys. To export in Telegram Desktop, use Settings → Advanced → Export Telegram data, or a selected chat's menu → Export chat history. Choose JSON or HTML, a limited date range and only needed media. UI labels may vary. If export is unavailable, paste a permitted excerpt.

For bot notifications: the agent can guide `/newbot` in official BotFather, local secret configuration, recipient initiation or group/channel membership, and read-only `getMe`/target checks. The notification skill contains the endpoint, JSON payloads and response checks. Use an existing secure Bot API tool or have the agent prepare a local HTTPS client that reads secrets privately. A new transport is a separate implementation and needs its own authorized live verification. Never paste tokens in the conversation. A setup request does not authorize a test send. Without a secure tool, get the ready-to-paste message instead.

For account access: the route skill explains application registration, current Telethon/TDLib options, interactive local login and session protection. It does not install or connect an account. An account session grants broad access; flooding and spam can cause bans. Bots ordinarily cannot read the owner's personal inbox, and updates are not an archive. Continuous monitoring needs a separate running component.

## Content and limits

An export or public chat is not permission for AI use. Telegram restricts AI processing of platform data; context-specific exceptions may be granted with all relevant users' explicit continuing consent, rather than automatically arising from consent. Third-party content needs a permitted specific use. With unclear rights, get an analysis template or work from original material you have rights to process. Redaction alone does not establish rights. Bot-submitted data has separate disclosed-use and revocable-consent requirements. See each skill's source references.

Exports are snapshots; missing media and later/deleted messages cannot be reconstructed. Sending success confirms API acceptance, not reading by a recipient. No bulk outreach, scraping, whole-account AI indexing or ban-evasion guidance. The agent can walk through authorized live verification; this package makes no claim of an account-level runtime test.

## Data and network

Network scope: route selection and export review fetch nothing. The bot skill optionally calls only `api.telegram.org` for `getMe`, `getWebhookInfo`, bounded `getUpdates` on a new unused bot if needed, `getChat`, `getChatMember` and explicitly authorized `sendMessage`. These fetch identity, webhook status, selected update/target/permission metadata, and send the chosen text and destination. No web search, website or robots.txt fetch, remote attachments or MTProto requests. No telemetry. Supplied files are read locally or in the assistant's existing file environment; assistant-provider processing and retention still apply.

Ordinary bot use is free within Telegram's limits; hosting and assistant usage are separate. This plugin does not enable paid broadcasts or quote a universal cost. It stores nothing itself; local configuration or tools the user chooses may retain secrets and records. See [PRIVACY.md](PRIVACY.md).

Public plugin documentation and privacy pages are not published yet; use this README and the bundled PRIVACY.md.

Support: https://github.com/grayskripko/marketing-skills/issues

MIT. See [LICENSE](LICENSE).
