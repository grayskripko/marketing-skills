# Platform rules and source register

Sources opened on 2026-10-11. These are public platform facts, not a claim about the user's installed version. Current documentation may describe releases newer than the user's installation. No numeric performance claims are made.

| Source | Scope and deciding fact | Date read |
| --- | --- | --- |
| [Codex AGENTS.md discovery](https://learn.chatgpt.com/docs/agent-configuration/agents-md) | At launch, global then project root-to-cwd discovery; first nonempty override/base/fallback per directory, deeper selected guidance overrides earlier guidance. Configurable fallback names and combined-size cap can change the chain. | 2026-10-11 |
| [Claude Code memory](https://code.claude.com/docs/en/memory) | Ancestor/local memory is combined, nested memory is loaded on demand; imports are relative to the containing file. Rule `paths` scopes loading. Missing paths loads unconditionally; invalid YAML is ignored and can load a rule without its intended scope. | 2026-10-11 |
| [Claude Agent SDK system prompts](https://code.claude.com/docs/en/agent-sdk/modifying-system-prompts) | Current query defaults enable user/project settings; explicit sources select matching file guidance and an empty list disables it. Loading is independent of the system prompt preset. | 2026-10-11 |
| [MCP tools specification](https://modelcontextprotocol.io/specification/2025-06-18/server/tools) | This dated protocol revision says annotations must be considered untrusted unless from trusted servers. An annotation is not evidence of permission enforcement. | 2026-10-11 |

SDK caveat: [the migration guide](https://platform.claude.com/docs/es/agent-sdk/migration-guide) describes an earlier no-filesystem-settings default. The current system-prompt page differs. Inspect explicit settings and the user's SDK version rather than assuming either default for every release. Migration guide read 2026-10-11.

House practices, not platform requirements: report maps and minimal diffs, preserve policy intent, keep unresolved choices explicit, use supplied definitions to check stale references, and distinguish file presence, loading, following, permission enforcement and execution. No public runtime connection or obedience claim follows from this text.
