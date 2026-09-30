# Inventory rules R1 to R8

These are this plugin's rules. Numeric lines are heuristics of this plugin, computed from the user's own list; print them when used. Google sources are named where they exist.

## Before the rules

- **Low traffic line:** 25% of the median of the traffic column (clicks or visits) in the user's list. Heuristic.
- **Stronger page in a group:** more conversions, then more clicks or visits, then more backlinks, then the newer page.
- A rule that needs a column the user did not supply is skipped and listed under Not checked.
- **Retire candidate:** a row that meets every R5 condition on the columns present, but the backlinks column is missing, gets "retire candidate — confirm backlinks" and goes into the top 10 actions with "check backlinks first".
- A row that no checked rule can decide, and that fails R5 on the columns present, gets "keep (not enough data)".

## Order of checking

R2 first, inside duplicate groups. Then R6 for every remaining row. Then R1, R3, R4, R5 and R8 in that order; the first match sets the fate. R7 applies to every row.

## Rules

- **R1 Keep.** The piece serves a current offer on the user's offer list (or is itself a product or pricing page by its URL or title), or has conversions above 0 in the period, or has traffic at or above the low traffic line. Without an offer list from the user, the offer part is not checked. If R3 also holds, the fate is Update.
- **R2 Merge.** Two or more pieces answer the same buyer question with the same intent. Keep the stronger page; the others are "merge into" it (move any unique part, then redirect). Decided before the other rules for group members.
- **R3 Update.** Still relevant, and the user marks a fact, price, product detail or screenshot as changed.
- **R4 Redirect.** No conversions, traffic below the low traffic line, and the user's list contains a broader or better page that answers the same question. Redirect to that page.
- **R5 Retire (404 or 410).** No conversions, traffic below the low traffic line, 0 backlinks, no better page to redirect to, and no current reader for it. Needs the conversions, traffic and backlinks columns; without all three, R5 is not checked.
- **R6 Leave alone.** Checked before R1, R3, R4 and R5. At any traffic level, pages that are correct and needed by a small audience or for legal reasons: legal and policy pages, support and implementation docs, reference pages, changelogs, archived announcements. Mark "Might be deliberate: Yes" and ask the owner to confirm.
- **R7 Never on age alone.** A publication or update date is never a reason for any fate. Google's helpful-content page lists, among its self-assessment questions, adding or removing lots of content mainly to seem fresher, and changing dates without substantial changes, as signs of content made for search engines rather than people (Google Search Central, "Creating helpful, reliable, people-first content", https://developers.google.com/search/docs/fundamentals/creating-helpful-content).
- **R8 Consolidate scaled near-duplicates.** Many templated pages whose text differs only in a swapped word (a city, an industry) → consolidate into the few pages with something distinct to say; list the survivors.

## Why merging and 404 or 410

Google's crawl-budget guide advises consolidating duplicate content and returning 404 or 410 for permanently removed pages (Google Search Central, "Large site owner's guide to managing your crawl budget", https://developers.google.com/crawling/docs/crawl-budget). The guide is written for large sites (about a million pages changing weekly, or ten thousand changing daily), so on small sites the gain is mainly for readers, not crawling.

## Effort sizes for actions

S: redirect, retire, small fact fix. M: update a section, merge two pages. L: rewrite or merge three or more pages.
