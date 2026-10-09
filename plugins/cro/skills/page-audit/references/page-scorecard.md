# Page scorecard PA-01 to PA-13

Each row is scored 0 (fails), 1 (partly) or 2 (passes), quotes its evidence and carries an evidence class (Seen / Data / Assumed). An Assumed row is never 0. A row with nothing to judge is "Not checked", never 2.

**No copy rows.** Headline quality, tone, wording of buttons, value proposition phrasing and the writing of testimonials are never scored here. When they look like the problem, print one line: "the wording may be the issue; a copy review fits". Offer clarity rows check whether facts are present and findable, not how well they are written.

| Id | Area | Check | 0 looks like | Source |
|---|---|---|---|---|
| PA-01 | Layout | One primary action; competing actions are visibly lighter (size, position, colour, not wording) | two equal-weight buttons side by side for different goals | heuristic of this plugin |
| PA-02 | Layout | The primary action is visible on the first screen at desktop and phone widths and is repeated after long sections | on a phone the form starts three screens down with no button above it | heuristic of this plugin |
| PA-03 | Offer clarity | The facts promised by the named traffic source (price, plan, discount, feature, audience) are present on the first screen; presence only | the ad says "plans from $X a month" and the page shows no price or plan | Google Ads Help, "About Quality Score for Search campaigns": landing page experience is how relevant and useful the page is to people who click the ad, read 2026-10-08; the first-screen test is a heuristic of this plugin |
| PA-04 | Offer clarity | Cost and commitment are findable before the action: price or price basis, trial length and renewal terms, what happens after submit | "Start trial" with no word on card requirement or renewal | Baymard cart-abandonment reasons, page updated 2025-09-22, read 2026-10-03 (extra costs 40%; total not visible up front 12%) |
| PA-05 | Trust | Proof near the decision point is attributable and checkable (named person or company, source, date or link). The row flags; it writes no proof | an unattributed quote and a star rating with no source | US: FTC 16 CFR Part 465 (consumer reviews and testimonials) and 16 CFR Part 255 (endorsement guides), read 2026-10-03 |
| PA-06 | Trust | Contact route, company identity, refund or returns terms and payment security information reachable from the page | no company name, address or contact anywhere | Baymard reasons (card-trust concern 19%; returns 13%), as PA-04 |
| PA-07 | Friction | Form on the page: count fields and steps. Five or more fields, or more than one step → hand to flow-audit | — (handoff row, not scored) | heuristic of this plugin |
| PA-08 | Friction | Nothing interrupts the path: no overlay on arrival, chat or cookie layer covering the action, exits that compete with the goal | a newsletter overlay opens before the page can be read on a phone | Google Search Central, "Avoid intrusive interstitials and dialogs", read 2026-10-03 (search guidance, used here only as a friction signal) |
| PA-09 | Speed | Field data only, at the 75th percentile: LCP ≤ 2.5 s, INP ≤ 200 ms, CLS ≤ 0.1. Lab-only scores are shown, not judged | p75 LCP 4.1 s on phones | web.dev "Web Vitals", updated 2024-10-31, read 2026-10-03 |
| PA-10 | Accessibility (conversion blockers only) | Tap targets at least 24 × 24 CSS px (WCAG 2.2 SC 2.5.8, AA; exceptions: enough spacing, an equivalent larger control, links inside a sentence); no sideways scrolling at 320 CSS px width (SC 1.4.10, AA) | the main button is a 16 px text link on phones | WCAG 2.2, Recommendation 2023-10-05, current edition 2024-12-12, read 2026-10-03 |
| PA-11 | Accessibility (conversion blockers only) | Text contrast at least 4.5:1 (SC 1.4.3), judged only from colour values the user gives (otherwise Assumed); the main action has an accessible name (SC 4.1.2) | light grey 12 px text on white, values given | as PA-10 |
| PA-12 | Measurement | The goal event is defined, fires once per conversion, and its count matches the back end within a stated tolerance | analytics shows 312 signups, the database 241 | Kohavi, Tang & Xu 2020 (trust in metrics); tolerance heuristic |
| PA-13 | Continuity | The click leads where the action implies (a trial button goes to trial signup, not to a sales form) and keeps the offer facts | "Start trial" opens a "contact sales" form | heuristic of this plugin |

## Pressure tactics seen on the page

Countdowns, stock warnings, pre-selected upsells: one line, not a score: "a pressure tactic is present; whether it is manipulative or lawful is out of scope here". A request to add one follows ground rule 4.

## Fix card

| Field | Content |
|---|---|
| Row and evidence | PA-id, quote, evidence class |
| Where | section or element |
| What is wrong | the problem, never new copy |
| Who | design, development or content owner |
| Effort | S / M / L |
| Funnel step | which step it acts on |
| Decision | Fix now / A/B test / Research first (`ship-test-research.md`) |
