# Template blocks

## Block table columns

block | fixed or variable | source column | unique per page (yes or no) | rule when empty

Typical blocks: title, main heading, summary line built from row facts, fact table, comparison against the hub average, notes the business wrote itself, links to the parent category and to related pages, last-updated date of the data.

## Targets (rules of thumb of this plugin)

- Default: target 40% variable text for prose-heavy pages. Use a complete row-fact table plus its decision explanation instead of a token-share gate when supplied pages are structured specifications, directories or lookup results and every required decision field is present; report the actual share and which test was used. Never add words just to pass. Measure fixed and variable text with the sample-QA whitespace-and-punctuation tokenisation; for prose target t, variable tokens = ceil(fixed tokens × t/(1−t)); at 40%, ceil(fixed × 2/3).
- Above the fold: the default 3 decision-relevant facts; use all required facts under the 2-fact/1-difference task exception when fewer facts fully answer that decision, and say which target was used.
- Pass mark for publishing a row: its profile earns a page (the default 3 filled independent decision facts and 2 differing jointly filled decision fields against every other profile; use 2 filled facts and 1 differing field only when supplied user tasks or customer questions show that field alone changes the required action and the page fully answers that task, naming the task, field, counts and selected test; compared with every other profile).

## Banned blocks

- Paragraphs where only the name or a synonym changes from page to page.
- Generic introductions repeated on every page.
- Filler such as lists of nearby places or "near me" sentences with no data behind them.
- Question-and-answer blocks written to fill space rather than from real customer questions.
- Any text, link or markup shown to crawlers but not to people.
- Numbers, ratings or reviews not present in the user's data.

## Empty-value rules

- Required field empty: the page is not published.
- Optional field empty: the block is hidden, never filled with a placeholder sentence.
- Row below the pass mark: not built; listed in the hub table. Only a row that must exist as a page for users (for example linked from the product) is built with `noindex, follow`. Rule of thumb of this plugin: a page left on noindex for a long time may stop passing links, so merging into the hub is the default.

## Structured data

Only where the row has the underlying data (for example a real price for an offer). Never markup for content the page does not show.
