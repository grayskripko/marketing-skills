# Telegram Bot

Set up a Telegram bot and prepare one alert. You get setup steps and message drafts. Checking the bot or sending a message needs a separately available tool that keeps the bot token private.


For bot alerts, summaries and reply drafts from supplied chat messages.
For offline work, provide pasted text or JSON/HTML exports you have permission to process. For optional live bot calls, you need a Telegram account to create a bot, a token stored in private configuration and a secure tool that can make HTTPS requests. Supplied text needs no paid API or account connection.

This independent plugin provides instructions. It includes no sending program, MCP server, personal-account client, scheduler or service that keeps listening for updates.

| Skill | Give it | You get |
|---|---|---|
| telegram-route | the job and access you need | a recommendation to use a bot, a personal-account client or an export, with setup steps and risks |
| telegram-bot-notify | destination and exact text, or a setup problem | a draft, Bot API request steps, or an authorized send confirmed by the API through an available secure tool |
| telegram-export-review | permitted export/excerpts and a question | summary, decisions, actions or reply with message references |

## Try it

- “Help me create a Telegram bot and prepare one alert without pasting a token here.”
- “Can a bot read my old private chats, or should I export them?”
- “From these permitted messages, list only agreed actions and cite the message IDs.”

## Setup and no-setup choices

For existing text/files: provide only the relevant permitted excerpt or selected export. Reading supplied text/files needs no additional install or keys. To export in Telegram Desktop, use Settings → Advanced → Export Telegram data, or a selected chat's menu → Export chat history. Choose JSON or HTML, a limited date range and only needed media. UI labels may vary. If export is unavailable, paste a permitted excerpt.

For bot alerts, the agent can guide you through `/newbot` in official BotFather and local secret storage. It can explain how the recipient starts the bot or adds it to a group or channel. It can also guide read-only `getMe` and destination checks. The notification skill contains the endpoint, JSON payloads and response checks. Use an existing secure Bot API tool or have the agent prepare a local HTTPS client that reads secrets privately. A new tool for making requests is a separate implementation. It needs its own authorized live checks. Never paste tokens in the conversation. A setup request does not authorize a test send. Without a secure tool, get the ready-to-paste message instead.

For personal-account access, the route skill explains application registration and the current Telethon/TDLib options. It also explains local interactive login and how to protect the saved session. It does not install or connect an account. An account session grants broad access. Flooding and spam can cause bans. Bots ordinarily cannot read the owner’s personal inbox. Updates are not an archive. Continuous monitoring needs a separate running component.

## Content and limits

Having an export or seeing a public chat does not give permission for AI use. Telegram restricts AI processing of its data. It may grant an exception for a specific use when every relevant user gives explicit, informed consent, actively agrees and keeps consenting. Consent alone does not grant an exception. Content from other people needs permission for the specific use. If rights are unclear, get an analysis template or use original material you have rights to process. Removing identifying details alone does not establish rights. Data submitted to a bot has separate requirements: explain its use and obtain consent users can withdraw. See each skill’s source references.

Exports are snapshots. Missing media and later or deleted messages cannot be reconstructed. Sending success confirms API acceptance, not reading by a recipient. No bulk outreach, scraping, AI indexing of a whole account or advice for evading bans. The agent can walk through authorized live verification; this package does not claim to have been tested with a live account.

## Data and network

Network scope: route selection and export review fetch nothing. The bot skill optionally calls only `api.telegram.org` for `getMe`, `getWebhookInfo`, bounded `getUpdates` on a new unused bot if needed, `getChat`, `getChatMember` and explicitly authorized `sendMessage`. These calls fetch the bot identity, webhook status, selected updates, destination details and permissions. A send submits the chosen text and destination. No web search, website or robots.txt fetch, remote attachments or MTProto requests. No telemetry. Supplied files are read locally or in the assistant’s existing file environment. The assistant provider’s processing and retention still apply.

Ordinary bot use is free within Telegram’s limits. Hosting and assistant usage are separate. This plugin does not enable paid broadcasts or quote a universal cost. It stores nothing itself. Local configuration or tools the user chooses may retain secrets and records. See [PRIVACY.md](PRIVACY.md).

Public plugin documentation and privacy pages are not published yet; use this README and the bundled PRIVACY.md.

Support: https://github.com/grayskripko/marketing-skills/issues

MIT. See [LICENSE](LICENSE).
