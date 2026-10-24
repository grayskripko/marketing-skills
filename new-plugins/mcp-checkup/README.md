# MCP Checkup

Fix an MCP connection or explain missing and failing tools from your pasted configuration, traces or files. For developers and teams using Claude Code, Codex or agent SDKs. You need redacted material and the client name; no account, API key or install is required for this review.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It bundles no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not server launchers. Installing this package does not itself launch a program or connect an account.

The default review reads only pasted material and task files you explicitly supply and returns diagnosis, corrected snippets and verification steps. The full workflow is not offline-only: both skills permit requested official-documentation retrieval, authorized live checks and optional Inspector setup through your assistant's existing tools. Documentation requests can reach code.claude.com, developers.openai.com, learn.chatgpt.com, modelcontextprotocol.io or openai.github.io and their official redirects, without putting your traces, configuration or secrets in a query. Live initialization, discovery and a documented read-only tool call contact your named trusted server and its documented authentication provider; the server receives call arguments and connection metadata, and provider charges may apply.

Optional Inspector setup can download packages from the npm registry and package download hosts and execute Inspector and the reviewed target server. The target server's own documented service destinations and data access must be reviewed before launch. Skills also give user-led checks such as `claude mcp list`, `claude mcp get <name>`, `codex mcp list`, `/mcp`, local credential setup, provider login, discovery refresh and SDK cache invalidation. These can launch or reconnect a configured server or use its authentication flow; they are not merely pasted-text analysis. Pasted commands are not executed just because they appear in a configuration. A redacted pasted trace remains a setup-free alternative.

The skills return snippets rather than instructing the assistant to overwrite configuration files. They prohibit write-tool smoke tests, message sending, purchases, account-data changes and permission expansion. Applying a proposed repair is a user-led configuration change. This package operates no publisher collection, telemetry or storage service. Your assistant provider processes and may retain the conversation and supplied files under its own terms; optional clients and Inspector may retain credentials in local files or a keychain. Support links are references you may open yourself; example `.test` endpoints are illustrative, not live destinations.

| Skill | Give it | You get |
|---|---|---|
| mcp-connect | client name, config and startup output | a supported diagnosis, minimal client-specific snippet and safe verification step |
| mcp-tool-check | discovery trace, schemas and call results | missing-tool or failed-call repair and a report of what the evidence proves |

Try “This config works in Claude Code but fails in Codex” or “The server connects, but the search tool is missing.” Attach the relevant file or paste the redacted section. Keep secrets out of the conversation. A snippet review is not a successful connection test.

The skills include source-backed configuration scope, environment, transport, session, discovery, schema and SDK permission guidance. Each skill links a dated official source register. They diagnose an existing server; they do not generate a new server or perform production writes.

## Optional live checks

If your assistant already has a client connected to the server you name, you can request discovery and a documented read-only call. Live checks need your server's normal access and may involve provider charges. Otherwise the assistant gives a concrete check matched to your client and accepts its redacted output. The package provides instructions, not a connector or execution service.

Inspector is optional. The assistant can explain its current runtime requirements and review a trusted server command before launch. Downloading it can contact the npm registry and package download hosts and execute software. A supplied Inspector trace works without setup. Keep token-bearing browser URLs private; Inspector may retain authentication data in its keychain or local secrets file.

## Data and network

Default network fetches: none. The assistant reads only pasted text and files you supply for the task. If you request current documentation, it may retrieve relevant pages on code.claude.com, developers.openai.com, learn.chatgpt.com, modelcontextprotocol.io or openai.github.io and their official redirects. No trace or config is sent in a search query. Authorized live checks contact only your named server and its documented authentication provider. Optional installation contacts the npm registry and its package download hosts; the target server may contact its own documented services, which must be reviewed before launch. No telemetry or plugin-managed storage. Host conversation retention and optional client storage still apply. See [PRIVACY.md](PRIVACY.md).

## Support and license

[Report a problem](https://github.com/grayskripko/marketing-skills/issues). MIT; see [LICENSE](LICENSE).
