---
name: agent-state-reconstruct
description: "Reconstruct an interrupted AI agent run so you can resume the agent without duplicate actions. Use when you paste traces, logs, configs, transcripts, checkpoints or files and ask what finished before the run stopped, whether a timed-out action happened, or what remains after workers stalled. Return a completed, pending and uncertain action ledger tied to artifacts and receipts, with ownership and approval gaps. Not for shortening a session summary, routine agent coordination, correcting durable memory facts, or investigating every possible cause of an agent failure."
---

# Reconstruct interrupted work

Answer exactly the questions asked, in the shape asked. Keep table rows to the outcomes the decision is about, so a small table stays small. If the user asks for an action table, what remains or what is safe, give the safe next move for each open item. End with the one check or lookup that settles each open item, and skip fix lists nobody asked for.

Classify each required outcome from the supplied records only:

- **Finished** needs evidence for the outcome itself: content, a diff, a fingerprint, or a receipt matching the same request, target and payload. An agent's "done" message, file existence or a receipt from another run is not enough.
- **Uncertain** covers timeouts, cancellations and conflicting records:
  - a timeout is not a failure;
  - a cancellation request does not mean the writer stopped or rolled back;
  - a checkpoint written before the attempt says nothing about its outcome.
- Accepted, delivered and applied are different outcomes; claim only the one the receipt shows.
- A wait loop is a dependency cycle only if it closes; a missing input is a blocker, not a cycle.
- When something must wait, name the safe move available now within the user's authority. That can be a read-only lookup by request ID, or preparing in a scratch location that does not overlap a writer that may still be live. The held side effect itself is never the fallback.

Work only from pasted material and named local files. Do not run, restart, send or replay anything.

Use a fact only when it changes the answer; never list them:

- A tool call cut off by the stop: Claude Code 2.1.281+ marks it unknown on resume; earlier versions may not show it. Either way it is Uncertain. <!-- github.com/anthropics/claude-code/releases/tag/v2.1.281, checked 2026-10-15 -->
- A recorded claim with no stored result means the call may have started; report it unknown, never as not run. <!-- temporal.io/blog/the-immortal-life-of-pi-running-the-pi-coding-agent-on-temporal (2026-10-08), checked 2026-10-15 -->
- MCP: `notifications/cancelled` is only a request; the receiver may ignore it or get it after it finished. Cancel a task-augmented request with `tasks/cancel` on its `taskId`, then poll `tasks/get` until the status is terminal (`completed`, `failed` or `cancelled`). A task stays `cancelled` even if execution went on, so check the target for the effect. <!-- modelcontextprotocol.io/specification/2025-11-25/basic/utilities/cancellation ; /basic/utilities/tasks, checked 2026-10-15 -->
