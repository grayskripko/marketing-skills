---
name: agent-resume-plan
description: "Prepare a safe plan to resume an interrupted AI agent run without duplicate actions or overwriting finished work. Use when you paste saved state, an action ledger, runtime config or approval records and ask how to resume an agent, restart a stopped run, or continue after a timeout. Return the exact preserved work, replay boundaries, pending decisions and ordered continuation steps for the supplied runtime. Not for executing a restart, sending messages, changing permissions, ordinary handoff summaries, healthy workflow design or rebuilding an agent framework."
---

# Plan a safe continuation

Give the ordered steps the user asked for, in their shape and length. Each step names what to check first and what proves it worked. Do not run, launch, send or replay anything; if the user said not to launch, prepare the command without telling them to run it.

- Keep finished files and receipted effects; never re-perform them.
- List every write that can run again from the chosen restart point and guard each one before it runs. Hold an uncertain write until an authoritative lookup for that exact request settles it. A new idempotency key cannot deduplicate the old attempt; an expired deduplication window gives no protection.
- Resume the saved state only when its identity matches the job; otherwise plan a fresh run that explicitly excludes completed work. A chat transcript is context, not a resumable checkpoint.
- When something must wait, give the safe move available now within the user's authority: a read-only lookup by operation or request ID, preparing in a scratch location that does not overlap a live writer, or a fresh session seeded from the saved facts. Never make the held side effect itself the fallback, and never take a decision that belongs to the user.
- Reuse an existing approval for the exact pending call: compare that call's arguments with the approval record, and ask for a new approval only when the target, payload or scope changed. The approver decides; say what to verify before approving.
- Independent, already-authorized work can go first.
- For a named runtime, write the documented call with the user's IDs (below), not "check your version's docs".

Documented calls; use the one that fits, never list them:

- LangGraph: on resume the interrupted node restarts from its beginning. If a subgraph was invoked inside a parent node, that parent node restarts too, so every write before the interrupt in either node runs again. Nodes whose successful writes were saved are not re-run. Inspect read-only with `graph.get_state(config, subgraphs=True)`. Resume on the same `thread_id` with `Command(resume=<the user's decision>)`. Guard each rerunnable write with a check before it, or move it into its own node. <!-- docs.langchain.com/oss/python/langgraph/interrupts ; /checkpointers (pending writes); reference.langchain.com/python/langgraph/pregel/main/Pregel/get_state, checked 2026-10-15 -->
- Codex CLI: `codex resume <SESSION_ID>` resumes that session, given by UUID or name. `--last` picks the most recent session from the current directory, and `--all` drops that directory filter. Run it from the session's workspace or pass `-C <dir>`, and state the original sandbox explicitly. <!-- learn.chatgpt.com/docs/developer-commands?surface=cli (was developers.openai.com/codex/cli/reference), checked 2026-10-15 -->
- Claude Agent SDK: `continue` takes the most recent session in the current directory, and `resume` takes a session ID. Since Claude Code 2.1.223, resume by ID searches beyond the current project directory, but the session file must be on the same machine. For another host, copy the session `.jsonl` under `~/.claude/projects/`, use a `SessionStore` adapter, or seed a fresh session with the saved results. Set allowed tools and permissions explicitly on the resuming call. <!-- code.claude.com/docs/en/agent-sdk/sessions.md, checked 2026-10-15 -->
- OpenAI Agents SDK Python: save with `result.to_state()` and `state.to_string()`. Restore with `await RunState.from_json(top_level_agent, stored)`, then call `state.approve(interruption)` or `state.reject(interruption)` on the exact interruption, then `await Runner.run(top_level_agent, state)`. Interruptions from an agent used as a tool surface on the outer run; resume the top-level agent. <!-- openai.github.io/openai-agents-python/human_in_the_loop/, checked 2026-10-15 -->
- Claude Code cloud session: when its container restarted mid-turn, that interrupted turn re-runs on resume (2.1.216+), so guard that turn's writes first. <!-- github.com/anthropics/claude-code/releases/tag/v2.1.216, checked 2026-10-15 -->
