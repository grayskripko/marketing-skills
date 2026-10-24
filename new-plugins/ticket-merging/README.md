# Ticket Merging

Check whether duplicate Zendesk tickets can be merged, which ticket should survive, and what happens to their fields, comments and recipients.
For support agents and operations leads reviewing duplicate tickets before a merge.
Needs pasted ticket text or readable CSV, JSON or text exports. No Zendesk account, API key or paid API is needed to assess pasted tickets.

## Skills

- **assess-ticket-merge** — Return a pair verdict, a proposed surviving ticket, participant changes and deciding blockers, including merge-suggestion errors.
- **prepare-merge-preservation** — Turn a proposed direction into a checklist for fields, tags, important history and sensitive content, plus merge-note drafts when requested.

Paste ticket IDs, issue/order identifiers, status categories, requester and CC aliases, organization and brand, sharing and AI-agent flags, permission and privacy settings, UI/API path, brand separation, CCs-and-followers experience, redaction permission and comment channels, fields/tags and relevant public/internal comments. Keep timestamps and approval conditions. Use stable aliases instead of personal contact details. Missing data receives a focused marker in the result; a partial export is assessed within its supplied coverage.

The result is a reviewable proposal. This package reads supplied material and bundled references; it connects to no helpdesk and changes no tickets. Merge direction is explicit: source → surviving destination.

## Data and network

At runtime, external URLs fetched: none. Ticket links and attachment links are retained as references, not opened. No telemetry, background tasks, credentials or connectors. The assistant reads only the pasted material or files you provide for this task. See [PRIVACY.md](PRIVACY.md).

## Knowledge

Bundled [Zendesk source register](references/zendesk-merge-rules.md), verified 2026-10-11, covers eligibility, audience changes, field/comment handling, role errors, masking, pre-merge redaction and reporting. Submission target: 2026-10-23. Source refresh and public document publication are recorded in [BUILD-NOTES.md](BUILD-NOTES.md).
