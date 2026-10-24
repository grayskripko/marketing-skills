# Public runtime sources

Read 2026-10-11. These pages were actually opened during this build. Documentation describes current published behavior, not proof of the user's installed version. Recheck a version-sensitive behavior when the supplied host differs.

| Source | URL | Scope and supported detail |
|---|---|---|
| Claude Code subagents | https://code.claude.com/docs/en/sub-agents | `isolation: worktree` starts from the default branch by default; omitted `tools` inherits available tools. Verify the actual worker checkout and permissions. |
| Codex subagents | https://learn.chatgpt.com/docs/agent-configuration/subagents | Native delegation and thread management; CLI `/agent`; delegation follows direct requests or applicable project/skill instructions. Original URL https://developers.openai.com/codex/subagents/ redirected here when read. |
| Claude SDK subagents | https://code.claude.com/docs/en/agent-sdk/subagents | `Agent` availability and definitions; non-fork prompt context; same-session custom-definition resume; Explore/Plan resumability limits; `Agent`/legacy `Task` trace names and `parent_tool_use_id`. Original URL https://platform.claude.com/docs/en/agent-sdk/subagents redirected here when read. |
| OpenAI SDK handoffs | https://openai.github.io/openai-agents-python/handoffs/ | Control transfer versus nested `Agent.as_tool`; client/server history boundaries, filtering and summary privacy. Handoff arguments do not replace conversation input. |
| MCP cancellation | https://modelcontextprotocol.io/specification/2025-11-25/basic/utilities/cancellation | Ordinary-request notifications, request-direction and initialization restrictions, task-specific cancellation, receiver discretion and completion races. This protocol version is the cited source, not a claimed user-server version. |
| Git worktree | https://git-scm.com/docs/git-worktree | Linked checkout state, `list --porcelain`, and dirty-worktree removal safeguards. |

The source names in SKILL.md map to these rows. All operational descriptions are paraphrases. File ownership, prerequisite graphs, brief fields, acceptance states and preserving alternate diffs are this plugin's rule of thumb: public coordination conventions, not guarantees supplied by a host or enforced locks. Nothing here requires additional accounts or an API integration.
