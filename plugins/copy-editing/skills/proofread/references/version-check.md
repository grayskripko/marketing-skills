# Version check: approved against final

Use when the user gives an approved version and a final one.

## Steps

1. Number the intended changes the user lists as IC-1, IC-2 … If there are none, say "no intended changes listed".
2. Align by paragraph, then by sentence (`computed-checks.md`, version comparison).
3. For each difference record: approved text, final text, type (insert, delete, replace, move), and class.
4. Class:
   - **expected** — matches an IC item, or is a PR fix made in this proof;
   - **unexpected** — anything else;
   - **unexpected addition, confirm** — a new sentence or paragraph not in the IC list.
5. Locked items: compare every locked value in the approved text with the final. An unexpected change to one is a blocker, and so is an unexpected removal of a sentence that carries a condition or a limit. An unexpected wording change that keeps every value is "unexpected, confirm", not a blocker.
6. Also check the final for PR-11 markers and PR-12 debris introduced by the revision.

## Table

`# · approved · final · type · class · note`

## What counts as a change

Spacing and straight-versus-curly quote differences are reported in one summary line, not row by row, unless they alter meaning. Everything else is listed, including a single changed digit.

## Common traps

- A number changed in one place but not in its repeat elsewhere: report both locations.
- A date moved but its weekday left as it was: one version-check row plus a PR-07 query.
- A removed sentence still referred to later ("as noted above"): PR-12.

## Example

Approved: "Registration closes 30 November. Up to 12 people per team."
Final: "Registration closes 30 November. Up to 120 people per team. TODO: add venue map."
Intended changes: none.

- 1 · "12" → "120" · replace · unexpected · blocker (locked number).
- 2 · added "TODO: add venue map." · insert · unexpected addition · blocker (PR-11 leftover marker).

Verdict: Hold.
