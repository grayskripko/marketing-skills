# Official source register

All sources below read 2026-10-10. Paraphrases, not copied platform text. Recheck current documentation during implementation; these skills do not fetch it at runtime.

- [Application setup](https://docs.discord.com/developers/quick-start/getting-started) — read 2026-10-10. Application creation, installation contexts, scopes, local secret handling and test-server development.
- [Gateway intents](https://docs.discord.com/developers/events/gateway) — read 2026-10-10. Intents select event delivery. GUILD_MEMBERS is privileged; MESSAGE_CONTENT controls access to message content. Enable only required privileged intents and check current approval status in the portal; no fixed eligibility threshold is assumed.
- [Interaction responses](https://docs.discord.com/developers/interactions/receiving-and-responding) — read 2026-10-10. Initial response or defer within 3 seconds; interaction follow-ups within the 15-minute token window. HTTP endpoint validates Ed25519 request signatures and handles PING; Gateway and HTTP are distinct delivery choices.
- [Permissions](https://docs.discord.com/developers/topics/permissions) — read 2026-10-10. Server and channel permissions differ from intents. Role grants need lower target roles; moderation has action-specific hierarchy and permission restrictions.
- [Application commands](https://docs.discord.com/developers/interactions/application-commands) — read 2026-10-10. Command names/descriptions and option limits; required options precede optional options. Installation contexts and default member permissions do not replace handler authorization.
- [Rate limits](https://docs.discord.com/developers/topics/rate-limits) — read 2026-10-10. Honor 429 and retry_after rather than hard-coding throughput; avoid blind retries of non-idempotent actions.

## Authored recommendations

Minimum permissions, human moderation review, exact role allowlists, duplicate suppression, private receipts and deliverable-first answers are workflow rules of thumb. They are not claimed to be Discord mandates. No demand or install count establishes effectiveness.
