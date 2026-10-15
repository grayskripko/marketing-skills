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
