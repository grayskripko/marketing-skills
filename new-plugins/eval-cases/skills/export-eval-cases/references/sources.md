# Export source register

| Source | Read | Scope and deciding knowledge |
|---|---|---|
| [JSON Lines format](https://jsonlines.org/) | 2026-10-11 | UTF-8; each physical line is a valid JSON value; blank lines are invalid. Use serialization rather than joining unescaped strings. |
| [Claude Code programmatic use](https://code.claude.com/docs/en/headless) | 2026-10-11 | `structured_output` is schema-produced final content, distinct from the response envelope. |
| [Codex non-interactive mode](https://developers.openai.com/codex/noninteractive), [redirect destination](https://learn.chatgpt.com/docs/non-interactive-mode) | 2026-10-11 | `--output-schema` shapes a final response; `--json` is an event stream. Neither defines the user's case importer. |
| [MCP tools](https://modelcontextprotocol.io/specification/2026-07-28/server/tools) | 2026-10-11 | `structuredContent` is server-produced tool data, separate from model structured generation. |

The review collection, sidecar, field mapping and neutral interchange fallback are authored rules of thumb. They are not native integrations. Compatibility depends on the user's actual target contract and validation. No runner-specific field names are inferred from these sources.
