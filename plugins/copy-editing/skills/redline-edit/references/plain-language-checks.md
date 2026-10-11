# Plain-language checks (medium and heavy levels)

These checks guide the edit internally, not a score. When the user requests before/after checks, show concrete familiar-wording and direct-sentence comparisons, with verified numerical measures only where useful. Otherwise do not print a checklist. They point at sentences worth a second look; they do not grade the text.

| Check | How | Note |
|---|---|---|
| average sentence length | words ÷ sentences (`computed-checks.md`) | report only |
| sentences over 25 words | list each with its count | the GOV.UK A to Z style guide asks writers to check sentences over 25 words to see whether they can be split (read 2026-10-03); a review prompt, not a rule |
| passive where the actor is known | "the form must be signed by the member" | rewrite to active only if the actor is named in the text; if not, query and never invent an actor |
| nominalisations | "make a decision", "carry out an inspection" | verb form when meaning stays the same |
| abbreviations not expanded on first use | first occurrence without the full form | expand only when the full form is in the text or certain; otherwise query |
| headings | texts over 300 words with no headings | heavy level adds them; medium level notes the gap |

## Frame

The international standard is ISO 24495-1:2023 (Plain language, Part 1), published June 2023. It is named for the user's own reading only; its text was not available to this plugin, and nothing here summarises it. The US government's plain-language guide series now lives on digital.gov (plainlanguage.gov redirects there; read 2026-10-03).

## Obligations stay locked

Words that set duties, permissions, conditions or deadlines (must, shall, may, should, unless, by, within) are locked items. Any change that could move who must do what, or by when, becomes a query. The lock keeps the strength and the holder, not the wrapper: "it is recommended that you should" → "you should" is allowed at medium and heavy; "should" → "must", or dropping "should", is not. This is an editing check, not legal review.

## Sources (read 2026-10-03)

- GOV.UK A to Z style guide: https://guidance.publishing.service.gov.uk/writing-to-gov-uk-standards/style-guides/a-to-z-style-guide/
- digital.gov plain language guide series: https://digital.gov/guides/plain-language

Maintainer note: review source wording outside user editing runs when a source change could affect these checks. The executing agent must respect the skill's network scope and must not claim current source verification from this snapshot. If uncertain source wording determines the requested edit, identify that limitation.
