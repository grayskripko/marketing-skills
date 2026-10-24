# Telegram sources

All linked pages below: read 2026-10-09. These are sources for platform requirements, not proof of a connected-account runtime test.

| Source | Supports |
|---|---|
| [Bot introduction](https://core.telegram.org/bots) | BotFather registration, token secrecy, recipient initiation, bot identity and delegated business features |
| [Bot API](https://core.telegram.org/bots/api) | HTTPS JSON requests, methods and success/error fields; getMe, getWebhookInfo, getUpdates, getChat, getChatMember, sendMessage and topic fields; 4096-character text limit; pending updates at most 24 hours |
| [Bot FAQ](https://core.telegram.org/bots/faq) | Polling versus webhooks, group privacy, broadcast limits and costs |
| [Content licensing](https://telegram.org/tos/content-licensing) | AI-data restrictions; context-specific exceptions may be granted with explicit informed affirmative continued consent from all relevant users; not automatic permission |
| [Bot developer terms](https://telegram.org/tos/bot-developers) | No unsolicited spam or moderation evasion; accessible privacy policy (standard default or custom if needed), necessary data, disclosed processing and explicit active revocable consent for voluntarily submitted data |
| [API terms](https://core.telegram.org/api/terms) | Consent for account actions, no interference with normal client behaviour; free API; title/official-logo restrictions for API clients |
| [Application registration](https://core.telegram.org/api/obtaining_api_id) | Own API ID/hash, third-party-client abuse warnings and ban risk |
| [Desktop export](https://telegram.org/blog/export-and-more) | Selected-chat or full-data exports, JSON/HTML, optional media |
| [Telethon sign-in](https://docs.telethon.dev/en/stable/basic/signing-in.html) | Own application credentials, interactive authentication and session storage |
| [Telethon sessions](https://docs.telethon.dev/en/stable/concepts/sessions.html) | Session files enable account access and require protection |
| [Telethon source notice](https://github.com/LonamiWebs/Telethon) | GitHub archive reflects a move to Codeberg |
| [Pyrogram notice](https://docs.pyrogram.org/) | No longer maintained or supported |
| [TDLib getting started](https://core.telegram.org/tdlib/getting-started) | Official client library setup and optional secret chats for that client, not recovery of existing secret-chat history |

Route selection, recommendation order and no-setup alternatives are this plugin’s rules of thumb.

Maintenance: check current access features, client documentation and platform terms before changing route guidance. Specific delegated features do not imply arbitrary history access.
