# Flow checks FL-01 to FL-16

Verdict per row: PASS, FIX, CHECK (cannot tell from what was given) or not applicable. Each row quotes the evidence and carries an evidence class.

| Id | Check | Source |
|---|---|---|
| FL-01 | Buying or signing up does not require creating an account first; a guest path or account creation after the order exists | Baymard reasons list (account required: 18% of US shoppers who abandoned, "just browsing" excluded), updated 2025-09-22 |
| FL-02 | The total cost, shipping, taxes and fees included, is shown before the payment step | Baymard reasons: extra costs 40%; total not visible up front 12% |
| FL-03 | The number of steps is shown and progress is visible | heuristic of this plugin |
| FL-04 | Labels sit outside the fields; no placeholder-only labels | NN/g, Whitenton, "Website Forms Usability: Top 10 Recommendations", 2016-05-01; NN/g, "Placeholders in Form Fields Are Harmful", 2014-05-11, reviewed 2018-09-10; WCAG 2.2 SC 3.3.2 (A) |
| FL-05 | One column, one field per row (short related pairs such as city and postcode excepted) | NN/g, Whitenton 2016 |
| FL-06 | Required and optional fields are marked; optional fields are few | NN/g, Whitenton 2016 |
| FL-07 | Format rules (password rules, date format) are shown before entry, not only in the error | WCAG 2.2 SC 3.3.2 (A) |
| FL-08 | Errors appear next to the field, say what is wrong and suggest a fix; entered data survives the error | WCAG 2.2 SC 3.3.1 (A), 3.3.3 (AA) |
| FL-09 | Nothing given earlier in the same flow is asked again (shipping copied to billing on request) | WCAG 2.2 SC 3.3.7 Redundant Entry (A) |
| FL-10 | Login or account steps need no memory or puzzle test; pasting into password fields works | WCAG 2.2 SC 3.3.8 Accessible Authentication (Minimum) (AA) |
| FL-11 | Accepted payment methods are shown before the payment step | Baymard reasons: not enough payment methods 9% |
| FL-12 | Delivery time and returns terms are visible before payment | Baymard reasons: slow delivery 20%; returns policy 13% |
| FL-13 | Every error, empty or declined state offers a way forward (retry, other method, contact) | heuristic of this plugin |
| FL-14 | The confirmation says what happens next and when | heuristic of this plugin |
| FL-15 | No reset or clear-form button | NN/g, Whitenton 2016 |
| FL-16 | The phone keyboard matches each field (email, tel, numeric) | WHATWG HTML input types and autofill, read 2026-10-03 |

All sources read 2026-10-03. WCAG 2.2 is cited as Recommendation 2023-10-05, current edition 2024-12-12.
