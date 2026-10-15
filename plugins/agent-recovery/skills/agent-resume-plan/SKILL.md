---
name: agent-resume-plan
description: "Prepare a safe plan to resume an interrupted AI agent run without duplicate actions or overwriting finished work. Use when you paste saved state, an action ledger, runtime config or approval records and ask how to resume an agent, restart a stopped run, or continue after a timeout. Return the exact preserved work, replay boundaries, pending decisions and ordered continuation steps for the supplied runtime. Not for executing a restart, sending messages, changing permissions, ordinary handoff summaries, healthy workflow design or rebuilding an agent framework."
---

# Plan a safe continuation

Give the ordered steps the user asked for, in their shape and length. Each step names what to check first and what proves it worked. Do not run, launch, send or replay anything; if the user said not to launch, prepare the command without telling them to run it.

- Keep finished files and receipted effects; never re-perform them.
- List every write that can run again from the chosen restart point and guard each one before it runs. Hold an uncertain write until an authoritative lookup for that exact request settles it. A new idempotency key cannot deduplicate the old attempt; an expired deduplication window gives no protection.
- Resume the saved state only when its identity matches the job; otherwise plan a fresh run that explicitly excludes completed work. A chat transcript is context, not a resumable checkpoint.
- Reuse an existing approval for the exact pending call; ask for a new one only when the target, payload or scope changed.
- Independent, already-authorized work can go first.
- Exact command syntax depends on the installed library or CLI version; say so once instead of asserting undocumented behavior.

Use a fact only when it changes the answer; never list them:

- Claude Code cloud sessions (2.1.216+) re-run the interrupted turn on resume, so guard its writes first. Before 2.1.216 a resumed background agent fell back to the default agent's prompt and tools. <!-- github.com/anthropics/claude-code/releases/tag/v2.1.216, checked 2026-10-15 -->
- Claude Agent SDK Python 0.2.137+: rewind with `resume_session_at` plus the `resume_drops_turn` guard, not by editing transcript files. <!-- github.com/anthropics/claude-agent-sdk-python/releases/tag/v0.2.137, checked 2026-10-15 -->
- OpenAI Agents SDK Python: resume with the original Session backend and ID and the returned state, not by replaying completed tools; after a partial Conversations append, repair remote history before retrying (0.24.0). Approval resume keeps completed tool results from 0.23.0. <!-- github.com/openai/openai-agents-python/releases/tag/v0.24.0 ; /v0.23.0, checked 2026-10-15 -->
- LangGraph before 1.2.15 could save a checkpoint past a failed DeltaChannel write, replay exit-mode delta writes out of order, and let ToolNode swallow invalid resume values (prebuilt 1.1.1). <!-- github.com/langchain-ai/langgraph/releases/tag/1.2.15, checked 2026-10-15 -->
