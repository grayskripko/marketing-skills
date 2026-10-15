---
name: agent-state-reconstruct
description: "Reconstruct an interrupted AI agent run so you can resume the agent without duplicate actions. Use when you paste traces, logs, configs, transcripts, checkpoints or files and ask what finished before the run stopped, whether a timed-out action happened, or what remains after workers stalled. Return a completed, pending and uncertain action ledger tied to artifacts and receipts, with ownership and approval gaps. Not for shortening a session summary, routine agent coordination, correcting durable memory facts, or investigating every possible cause of an agent failure."
---

# Reconstruct interrupted work

Answer exactly the questions asked, in the shape asked (a small table means a small table). Add next steps, retry advice or preservation notes only when the user asks what to do next.

Classify each required outcome from the supplied records only:

- **Finished** needs evidence for the outcome itself (content, diff, fingerprint, or a receipt matching the same request, target and payload). An agent's "done" message, file existence or a receipt from another run is not enough.
- **Uncertain** covers timeouts, cancellations and conflicting records. A timeout is not a failure; a cancellation request does not mean the writer stopped or rolled back; a checkpoint written before the attempt says nothing about its outcome.
- Accepted, delivered and applied are different outcomes; claim only the one the receipt shows.
- A wait loop is a dependency cycle only if it closes; a missing input is a blocker, not a cycle.

Work only from pasted material and named local files. Do not run, restart, send or replay anything.

Use a fact only when it changes the answer; never list them:

- A tool call cut off by the stop: Claude Code 2.1.281+ marks it unknown on resume; earlier versions may not show it. Either way it is Uncertain. <!-- github.com/anthropics/claude-code/releases/tag/v2.1.281, checked 2026-10-15 -->
- Missing turns are not proof nothing ran: before 2.1.286, `--resume`/`--continue` could lose every turn after parallel tool calls in a crashed or killed session; before 2.1.223, resume after a mid-session `/cd` came back empty. <!-- github.com/anthropics/claude-code/releases/tag/v2.1.286 ; /v2.1.223, checked 2026-10-15 -->
- A recorded claim with no stored result means the call may have started; report it unknown, never as not run. <!-- temporal.io/blog/the-immortal-life-of-pi-running-the-pi-coding-agent-on-temporal (2026-10-08), checked 2026-10-15 -->
