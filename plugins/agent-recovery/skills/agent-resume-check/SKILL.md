---
name: agent-resume-check
description: "A question about whether the user's own resumed AI agent run really finished without duplicate actions, even a quick one-liner: my AI agent says it finished after I restarted it, did it; my agent's records look doubled after I resumed it, how do I verify. Check whether a resumed AI agent run finished the pending work without duplicate actions or damage to completed artifacts. Use when you paste before-and-after files, receipts, traces or checkpoint exports and ask whether agent recovery worked, whether a retry after interruption sent twice, or whether an interrupted run is now complete. Return in plain words what the supplied records show went right and what went wrong, within their coverage, and the check that settles each open item. Not for ordinary checks of merged worker results, performing the restart, broad agent benchmarking, routine code review, model tuning or accepting a success message as proof."
---

# Check the resumed outcome

Answer the user's questions directly, in their words and order, as briefly as they asked. State plainly what went right and what went wrong; do not replace that with a label. End with the check or lookup that settles each open item.

Judge from the supplied records:

- The agent's success message or a clean resume is not proof. Check the outcome itself: content, a diff, a fingerprint, or a receipt matching the same request, target and payload.
- An export only proves absence within its coverage; a paginated or time-cut export cannot rule out a duplicate.
- Two attempts are not necessarily two effects, and two effects can carry different request IDs. A confirmed duplicate stays a breach of an exactly-once requirement even after cleanup.
- Without a before-record, preservation of earlier work cannot be confirmed. A new run is not a resume of the old one.

If no records are supplied, answer the question in general terms, name the specific record or lookup (request ID, target and time) that would settle it, and ask the user to paste it. Work only from pasted material and named local files. Do not run, restart, send or replay anything.

Use a fact only when it changes the answer; never list them:

- A Claude Code rewind does not prove a full restore: checkpoints cover only Claude's edits, not user edits or Bash commands. <!-- anthropic.com/news/enabling-claude-code-to-work-more-autonomously (2025-09-29), checked 2026-10-15 -->
- Rejecting a stale worker's transcript write does not stop its tool's external effect; check the target system. <!-- temporal.io/blog/the-immortal-life-of-pi-running-the-pi-coding-agent-on-temporal (2026-10-08), checked 2026-10-15 -->
