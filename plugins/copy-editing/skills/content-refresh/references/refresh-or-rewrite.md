# Refresh, light refresh, or recommend a rewrite

## Decision

| Outcome | Conditions | What the skill does |
|---|---|---|
| Light refresh | five ledger items or fewer change, and the page's main point is still true | changes those items only |
| Refresh | more than five items change, or one section is out of date as a whole, but the main point holds | keeps the structure and places new facts into the sections that already exist |
| Rewrite recommended | the main point is no longer true, or the page now serves a different reader | stops, names the reason, lists the ledger; writes nothing new |

Counting rule: a ledger item "changes" when its status is Stale (either kind). Check items do not count, but more than five of them gets a note: "Many items need your facts before this page can be called current."

## Seam check

After the edits, read each changed sentence with the one before and after it:

- a new fact that contradicts an old sentence ("12 hours" here, "10 hours" in the FAQ below);
- the same fact now stated twice;
- time words that no longer fit ("next year" beside a past date; "new" beside a two-year-old item);
- tense breaks where a future sentence became past.

Each seam is a finding with its location; fix it only if the fix is another ledger item, otherwise query.

## Updated-date line

Suggest "Updated [month year]" only when a Stale value was replaced or a section was added. Wording-only edits get no new date. If the page shows a date in more than one place, the visible date and any date in the page's structured data should agree; say so as advice, without changing code. A year in the URL or title is a finding only.

## Basis (read 2026-10-03)

- "Creating helpful, reliable, people-first content" (Google Search Central): https://developers.google.com/search/docs/fundamentals/creating-helpful-content (its self-assessment asks whether dates are changed to make pages seem fresh when the content has not substantially changed).
- Google Search Central, "Influence your byline dates": https://developers.google.com/search/docs/appearance/publication-dates (a visible, labelled date that agrees with the date in structured data).

If this note is more than six months old when you use it, re-check these pages.
