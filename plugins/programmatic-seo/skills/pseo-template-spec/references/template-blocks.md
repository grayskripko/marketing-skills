# Template blocks

## Block table columns

block | fixed or variable | source column | unique per page (yes or no) | rule when empty

Typical blocks: title, main heading, summary line built from row facts, fact table, comparison against the hub average, notes the business wrote itself, links to the parent category and to related pages, last-updated date of the data.

## Targets (rules of thumb of this plugin)

- Variable share: on a typical row, at least 40% of the page's words come from row data or from text written for that row.
- Above the fold: at least three facts that set the page apart.
- Pass mark for publishing a row: its profile earns a page (at least 3 filled columns that set a page apart, and a difference of at least 2 such columns from every other profile).

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
