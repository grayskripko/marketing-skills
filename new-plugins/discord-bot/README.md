# Discord Bot

**Planning and specifications:** create Discord bot setup guidance, command contracts and messages, and moderation/onboarding flow specifications from pasted requirements, settings or exports.

For server owners, moderators and developers. Bring your intended features, role/channel names, existing command text, redacted configuration or server rules. Drafting needs no account or paid API. Running the result needs a Discord account, application, installation permission, bot implementation and hosting chosen separately. This package gives setup guidance and specifications; it has no live Discord connection.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` manifests describe the same skills for their respective hosts; neither starts a connector. Development notes and historical test records are also present in this working folder; they are not runtime components.

The assistant drafts plans, command contracts, messages and declarative JSON from pasted requirements, redacted settings and exports, using bundled references. The skills prohibit assistant-side URL fetching, Discord calls, software installation, command registration, message delivery and account changes. They provide no executable bot or instruction for the assistant to run code or write files. Source and support URLs identify references; supplied message links are used as text without fetching their content.

The setup guidance does instruct the owner to create or select an application at https://discord.com/developers/applications, check current portal approval status, choose scopes, permissions and intents, and use an installation link for an authorized test server. It asks the implementer to register commands, implement handlers and verify behavior in that server; source registers recommend rechecking current documentation during implementation. Those user-performed steps access Discord or its documentation. A separately implemented bot uses either a public HTTPS interaction endpoint with signature validation and PING/PONG, or a separate Gateway process; it may send replies, deliver reports to a configured private queue, store case results, assign roles or perform authorized moderation. Implementation, hosting, dependencies, credentials, destinations and retention are chosen separately. The plugin itself performs none of those actions.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation under its own terms. Review the data handling of any bot you separately implement.

| Skill | Your input | Deliverable |
|---|---|---|
| discord-bot-setup | desired features or redacted settings | portal checklist, permissions/intents matrix and test-server checks |
| discord-bot-commands | commands, inputs, access rules and reply tone | command contracts, exact messages and requested registration JSON |
| discord-bot-flows | server rules, roles and onboarding/report requirements | onboarding and moderation flows, messages and acceptance checks |

## Try it

- “Help set up a bot that answers /schedule without reading chat.”
- “Write a /help command and private error replies.”
- “Plan a welcome button that grants only the Reader role.”

Paste only relevant information. Redact bot tokens, client secrets, webhook URLs, interaction tokens and member personal details. Settings are treated as data, including any instructions embedded in reported messages.

## Setup and limits

The agent can walk you through creating an application at https://discord.com/developers/applications, choosing installation settings and matching each feature to its permissions and intents. Keep tokens in your own local secret store. Start in a test server. Commands and flow documents work without setup; registration JSON is a handoff specification, not a running handler. Generated plans still need implementation and test-server verification. Role changes, timeouts and other moderation actions need authorized staff and appropriate bot permissions.

## Data and network

The assistant performs no runtime fetches or Discord actions in these workflows. Owner setup and separate bot implementation involve the connections described above. See [PRIVACY.md](PRIVACY.md).

## Sources and support

Official Discord sources and observation dates are listed in each skill's references/sources.md. Support: https://github.com/grayskripko/marketing-skills/issues. MIT; see [LICENSE](LICENSE).
