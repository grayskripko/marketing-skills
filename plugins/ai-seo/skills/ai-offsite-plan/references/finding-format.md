# Finding format

Every skill in this plugin uses these fields to sort and reason about findings, so results from the different skills line up. The user sees plain sentences without IDs; show the full table only when the user asks for it.

## Fields

| Field | What goes in it |
|---|---|
| ID | Internal only, never shown in a plain answer. Prefix plus number: `ACC-1` (crawler and snippet access), `CIT-2` (quotability of passages), `FRS-1` (freshness), `ENT-1` (source identity), `GAP-1` (answer gap), `MEAS-1` (measurement result), `OFF-1` (off-site source). |
| Where | A URL, a passage located by its heading, an export row, a prompt ID, or a cited domain. |
| Issue | One sentence describing what is wrong or missing. No advice in this field. |
| Evidence | What was actually seen: the tag or directive, the quoted passage (short), the column values, or the counts with n. |
| Evidence level | Observed, From user data, or Needs verification (see below). |
| Impact | High, Medium or Low, judged by how directly the issue stops the page or brand from being quoted accurately for the user's goal. |
| Effort | S (under a day), M (a few days), L (a sprint or more). A rough guess; say so if the team size is unknown. |
| Fix | The concrete change: where, what, and who usually does it (content, developer, PR or community owner). |
| How to verify | The check that shows the fix worked, and when: usually the next panel run, the next export period, or a re-fetch of the page. |
| Might be intentional | Yes or No. Yes only for the patterns each skill lists (for example a training-only crawler blocked on purpose, snippet limits on paywalled sections). Always No when a control blocks the page or passage the user wants cited. When Yes, the finding asks the owner to confirm instead of calling it an error. |

## Evidence levels

- **Observed**: seen directly in a fetched page, in HTML or text the user pasted, or in a robots.txt file. Quote the exact value.
- **From user data**: read from a log, export or pasted answer the user provided. Name the file or source and the columns used, with n.
- **Needs verification**: cannot be confirmed from here. Name the tool or step that would confirm it, for example a rendering check in a browser or crawler that runs JavaScript, URL Inspection in Search Console, the next panel run, or the platform's own report.

Anything assumed rather than seen (the buyer's intent, which engines matter, why a rate changed) goes into an **Assumptions** list. It is never written as a finding.

## Example rows

| ID | Where | Issue | Evidence | Level | Impact | Effort | Fix | Verify | Intentional? |
|---|---|---|---|---|---|---|---|---|---|
| ACC-1 | `/guides/invoice-approval` | The key answer sits inside a block excluded from snippets | `<div data-nosnippet>` wraps the "How approval works" section | Observed | High | S | Remove `data-nosnippet` from that section (developer) | Re-fetch the page; the next panel run for the approval prompts | No |
| MEAS-2 | Engine B, unbranded prompts | Mention rate fell between August and September | 21/90 runs to 8/90 runs; 5 prompts moved down, none up | From user data | High | M | Check the lost prompts in the page check and the answer gap | Next monthly run with the same settings | No |

## Rules

- One issue per finding. The same issue on many pages is one finding with a count and up to 3 examples.
- Every rate taken from AI answers carries its n and the dates of the runs.
- If a check could not be run (no access, cap reached, tool missing, no answers pasted), list it under "Not checked" with the way to check it. Do not guess a result.
