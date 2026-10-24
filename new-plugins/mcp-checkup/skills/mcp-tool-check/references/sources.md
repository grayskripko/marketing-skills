# Official source register

Read 2026-10-11. These are public operational and diagnostic references. Dates in specification URLs identify the cited protocol revision, not a claim that it is the newest revision. Client and SDK pages are moving documentation; verify installed versions before applying newer fields.

| Source | Scope and supporting passage, paraphrased | Used for |
|---|---|---|
| [Claude Code MCP](https://code.claude.com/docs/en/mcp), read 2026-10-11 | Installation scopes and precedence: local outranks project, then user; complete entries are selected. Environment expansion documents variable and default forms. | JSON wrapper, paths, scope conflicts, variable expansion, diagnostic commands. Managed configurations and desktop differences require surface-specific review. |
| [Codex MCP](https://developers.openai.com/codex/mcp), read 2026-10-11; redirects to [MCP for CLI](https://learn.chatgpt.com/docs/extend/mcp?surface=cli) | Connect/configure sections document user and trusted-project TOML, transport fields, environment-sourced bearer tokens and allow/deny filters. | Codex snippets and client filtering; not hosted-plugin equivalence. |
| [MCP transports](https://modelcontextprotocol.io/specification/2025-11-25/basic/transports), read 2026-10-11 | stdio reserves stdout for protocol messages. Streamable HTTP POST accepts JSON and SSE; GET can be refused; assigned session IDs accompany later requests. | Distinguish log noise, endpoint behavior and sessions. |
| [MCP lifecycle](https://modelcontextprotocol.io/specification/2025-11-25/basic/lifecycle), read 2026-10-11 | Initialize negotiates version and capabilities; client sends initialized notification afterward. | Trace order and compatibility. |
| [MCP tools](https://modelcontextprotocol.io/specification/2025-11-25/server/tools), read 2026-10-11 | Tools capability, cursor-based discovery, input/output schemas, untrusted annotations and separate protocol/tool errors. | Discovery completeness, argument repair, structured results and failed tool execution. |
| [Claude Agent SDK MCP](https://code.claude.com/docs/en/agent-sdk/mcp), read 2026-10-11 | Explicit settingSources must include project to load project configuration. MCP tool naming and permissions have separate sections. | SDK configuration loading and denied-call diagnosis. |
| [OpenAI Agents SDK MCP](https://openai.github.io/openai-agents-python/mcp/), read 2026-10-11 | Filtering, caching and pagination sections describe local MCP server classes, complete tool-list pagination and invalidate_tools_cache. | Distinguish filtered or stale SDK discovery from transport failure. |
| [MCP Inspector](https://modelcontextprotocol.io/docs/tools/inspector), read 2026-10-11; redirects to [current Inspector guide](https://modelcontextprotocol.io/docs/2026-07-28/tools/inspector) | npx launches the tool and target; current runtime minimum is Node 22.19.0. Tools inspection and calls are supported. Browser URLs carry a per-launch token. Secrets can persist in the OS keychain or a local secrets file. | Optional setup guidance, deliberate read-only checks and privacy disclosure. Recheck runtime requirements before installing. |

## Local authored decisions

Diagnosis-first output, minimal configuration edits and the proposed read-only smoke sequence are this plugin's rules of thumb. They are not protocol mandates. Fictional company names, reserved example endpoints, variable names and tool calls are illustrative input, not working services or observed runs.
