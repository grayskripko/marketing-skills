# Platform sources

Read 2026-10-09.

- [Claude Code subagents](https://code.claude.com/docs/en/sub-agents), sections “Manage subagent context,” “Fork the current conversation,” and “Chain subagents”: ordinary subagents start with separate context; forks inherit the current conversation. The main agent can pass one completed result to the next worker. Use the host's available native controls; command availability depends on version and settings.
- [Claude Code plugin dependencies](https://code.claude.com/docs/en/plugins/dependencies), sections “Declare dependencies” and “Test a plugin and its dependency locally”: `dependencies` is an array; a bare name resolves in the same marketplace. Both local plugins can be supplied with `--plugin-dir`. A missing required dependency prevents loading.

The comparison criteria, semantic splitting, stopping choices and dynamic scheduling in these skills are this plugin's rules of thumb, not platform requirements or measured effectiveness claims.
