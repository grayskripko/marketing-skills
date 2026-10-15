---
name: agent-resume-check
description: "Check whether a resumed AI agent run finished the pending work without duplicate actions or damage to completed artifacts. Use when you paste before-and-after files, receipts, traces or checkpoint exports and ask whether agent recovery worked, whether a retry after interruption sent twice, or whether an interrupted run is now complete. Return a verified, incomplete or unresolved verdict tied to the requested outcome and the coverage of supplied records. Not for ordinary checks of merged worker results, performing the restart, broad agent benchmarking, routine code review, model tuning or accepting a success message as proof."
---

# Check the resumed outcome

Answer the user's questions directly, in their words and order, as briefly as they asked. State plainly what went right and what went wrong; do not replace that with a label. Add repair steps only if asked or if the job cannot close without them.

Judge from the supplied records:

- The agent's success message or a clean resume is not proof; check the outcome itself (content, diff, fingerprint, matching receipt for the same request, target and payload).
- An export only proves absence within its coverage; a paginated or time-cut export cannot rule out a duplicate.
- Two attempts are not necessarily two effects, and two effects can carry different request IDs. A confirmed duplicate stays a breach of an exactly-once requirement even after cleanup.
- Without a before-record, preservation of earlier work cannot be confirmed. A new run is not a resume of the old one.

Work only from pasted material and named local files. Do not run, restart, send or replay anything.
