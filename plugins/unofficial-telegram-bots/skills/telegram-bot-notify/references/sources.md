# Telegram sources

All linked pages below: read 2026-10-09. These are sources for platform requirements, not proof of a connected-account runtime test.

| Source | Supports |
|---|---|
| [Bot introduction](https://core.telegram.org/bots) | BotFather registration, token secrecy, recipient initiation, bot identity and delegated business features |
| [Bot API](https://core.telegram.org/bots/api) | HTTPS JSON requests, methods and success/error fields; getMe, getWebhookInfo, getUpdates, getChat, getChatMember, sendMessage and topic fields; 4096-character text limit; pending updates at most 24 hours |
| [Bot FAQ](https://core.telegram.org/bots/faq) | Polling versus webhooks, group privacy, broadcast limits and costs |
| [Content licensing](https://telegram.org/tos/content-licensing) | AI-data restrictions; context-specific exceptions may be granted with explicit informed affirmative continued consent from all relevant users; not automatic permission |
| [Bot developer terms](https://telegram.org/tos/bot-developers) | No unsolicited spam or moderation evasion; accessible privacy policy (standard default or custom if needed), necessary data, disclosed processing and explicit active revocable consent for voluntarily submitted data |

The verification sequence, no-default-recipient policy, no blind resend and manual-paste fallback are this plugin’s rules of thumb.

Maintenance: check current Bot API methods and bot developer terms before changing notification guidance.
