# Build skeletons and checks

## Skeletons

- **Checklist.** A title that names the result. Phases in the order the user's team works. Each item: an action that starts with a verb, a "done when" test the reader can verify, and one line on why it matters. Stated time to complete at the top. The last item points to the next step the offer helps with.
- **Template.** What the template produces and for whom. The fields in order; under each, an instruction of one or two lines; one example row taken from the user's material, or `[DATA NEEDED: an example row]`. A short "common mistakes" list only if the user's notes contain them.
- **Scorecard / self-assessment.** 8 to 15 questions with fixed answer options and points; the scoring rule; 3 or 4 bands with score ranges that do not overlap; for every band, the next step it suggests. The highest-need band's next step is the bridge to the offer.
- **Calculator spec.** Inputs (name, unit, allowed range, default marked "yours" or "assumption"); the formula written out; three test cases with expected outputs; edge cases (zero, out of range, impossible combinations); the result text; the step that sends the result by email. Every input appears in the formula. Spec only: no code, no layout.
- **Sample or mini-audit.** What the reader sends (with a note to remove personal data), what comes back, the sections of the returned audit, delivery time and how many the team can do per week.
- **Workshop or live session.** Promise, audience, capacity, run of show by minutes, what attendees prepare, what each attendee leaves with, when the joining details arrive, and what happens after the session.
- **Short course.** Lesson titles, the single job of each lesson and one exercise per lesson. No email text.
- **Guide.** Section headings, each carrying a single claim plus a slot for its source; only the opening section is drafted in full.
- **Own-figures report.** The question each table answers, the base (n) of every figure, how the data was gathered and anonymised, and the publication permission.
- **Swipe file.** Each example with what makes it work and its permission status.

## Build checks (run before writing; after the asset, only failures or changes are shown, in plain words, each naming the line)

| Id | Check |
|---|---|
| LB-01 | The first usable result sits on page 1 or in step 1. |
| LB-02 | One job, one reader: the asset serves the reader and job named in the promise line; a second job becomes a separate asset. |
| LB-03 | Every figure, quote, customer, case or name comes from the user's material; anything else is left out, and the answer names what is missing after the asset. |
| LB-04 | The asset promises nothing its content does not deliver. |
| LB-05 | It matches the promise line from magnet-plan ("[who] gets [result] in [time]"); without one, write one and mark it as an assumption. |
| LB-06 | Any rule that can change (laws, platform limits, prices) carries the date it was checked and "re-check after 6 months". |
| LB-07 | Calculator test cases reproduce when recomputed, and every input appears in the formula. |
| LB-08 | Reading or use time is stated. |
| LB-09 | For exported documents: real heading levels, and text set as text rather than inside images unless that exact look is essential, as with a logo (WCAG 2.2, success criteria 1.3.1 and 1.4.5, W3C Recommendation of 2024-12-12, read 2026-10-08). |
| LB-10 | The promise list is exported: each claim the opt-in page may make, tied to the section that fulfils it, plus a "do not promise" list of claims the asset cannot support. |

## Worked example: calculator spec

Inputs: hours logged in the month (h, 0 or more, yours), hours billed in the month (h, 0 or more, yours), blended hourly rate (currency, above 0, yours).
Formula: unbilled value = (hours logged − hours billed) × rate.
Test cases (recomputed):
1. 160 logged, 140 billed, 90 per hour → (160 − 140) × 90 = 1,800.
2. 0 logged, 0 billed, 90 per hour → 0, with the note "no hours logged this month".
3. 120 logged, 130 billed → stopped before computing: "billed hours exceed logged hours; check the time data".
Result text: "You logged [x] hours you did not bill: about [value] this month." Keep step: "Email me this result."
If the user lists an input the formula does not use (for example the number of clients), LB-07 fails: give it a term if one makes sense, such as "per-client average = unbilled value ÷ clients", otherwise remove it, and say which.
