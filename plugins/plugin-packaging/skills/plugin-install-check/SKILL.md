---
name: plugin-install-check
description: "Check whether my skills-only Claude plugin actually loads, invokes its skills and reads its bundled resources in the target host. Use when the user says “the install says success but skills are missing,” “does this transcript prove it works,” or “verify my repaired plugin” and supplies host evidence or requests a check through an available named host. Return a receipt for observed events and collect the requested harmless checks when available. Keep installation, enablement, discovery, invocation and resource access separate. Not for marketplace installation, changing account settings or judging skill answer quality."
---

# Check target-host installation evidence

Say what the supplied records prove about one package revision in one host: installed, enabled, discovered, invoked, bundled file read. A stage with no event is "not shown", not failed. Do not join traces from different revisions, sessions or hosts into one receipt; a local `--plugin-dir` load is not a colleague's marketplace install, and a Claude receipt is not a Codex one. Use plugin-package-repair for file edits.

## Host rules that decide receipts

- Claude Code: validation passing does not prove inventory or invocation. `disable-model-invocation: true` stops automatic use; `user-invocable: false` hides the skill from manual invocation. Do not change these fields to make a receipt pass.
- Agent SDK: an explicit empty `setting_sources`/`settingSources` loads no filesystem settings. `project` loads `<cwd>/.claude/settings.json`; `local` loads `.claude/settings.local.json`. Add only the sources for the files the user names; if it is unclear which, give the smaller set and say what the other would add.
- Agent SDK: sending `/<plugin>:<skill>` in the prompt dispatches a user-invocable skill and does not depend on the `skills` option. When the app is to invoke a skill explicitly, that prompt is the change; add `Skill` to an explicit `tools` list only when the model itself must call a skill. `tools` is availability; `allowed_tools` is pre-approval.
- Agent SDK: the init message's `skills` array lists user-invocable skills only. The SDK docs ("Confirm skills loaded") say a `user-invocable: false` skill loads but is absent from it; cite that page when you rely on it. The array does not prove invocation.
- A file read is shown only by a Read event (or captured file result) for the packaged path in this revision. A quoted sentence is not proof.
- MCP: a JSON-RPC response whose result has `isError: true` is a failed tool call, not a success.

<!-- Sources: https://code.claude.com/docs/en/agent-sdk/skills (init skills array, dispatch by name, settingSources) ; https://code.claude.com/docs/en/agent-sdk/claude-code-features (project = <cwd>/.claude/settings.json, local = .claude/settings.local.json) ; https://code.claude.com/docs/en/skills (invocation controls) ; https://modelcontextprotocol.io/specification/2025-11-25/server/tools (isError; read 2026-10-11) ; checked 2026-10-15 -->

## Evidence to ask for

Name the smallest read-only evidence that would close a missing stage, with what PASS looks like. Prefer records that already exist over new runs. To establish what a session did, ask, per skill, for:

1. the Skill or command event for the namespaced skill, with timestamp and the package version/revision of that session;
2. the record each action left in the system it touched (the sent message in the messaging tool, the publication record, the written file), as a read-only lookup;
3. for a refused or failed action, the permission rule or denial log entry that refused it.

Never suggest invoking a skill that sends, publishes, deletes or installs, and never suggest retrying a failed action. If no records exist, the receipt is "listed; invocation not shown". When asked to run a check yourself, use only a harmless skill, do not load a package that has hooks, MCP servers or `bin/`, and record the commands you actually ran.

## Answer

Give what was asked, in the requested shape and length. Each claim points to its event. Mention a missing stage only when it changes the conclusion.
