# Computed checks

Run these in the host's code tool when it has one. Without one, do them by hand, show the working, and mark each result "checked by hand, not computed".

## Counting rules

| Measure | Rule |
|---|---|
| words | split on runs of spaces and line breaks; "8 am" is 2, "e-mail" is 1, "3,000" is 1, a dash with spaces on both sides counts as 1 |
| characters | report with and without spaces; line breaks are not counted |
| sentences | split after `.`, `?` or `!` followed by a space and a capital or a digit; abbreviations such as "e.g." do not end a sentence |
| reading time | words ÷ the user's words per minute, rounded up to the next half minute; ask for the speed rather than assume one |

Always print the rule next to the count, because two tools can disagree by a few words.

## Weekday against date

With a code tool: parse the date and print its weekday. By hand, use Sakamoto's method:

```
t = [0, 3, 2, 5, 0, 3, 5, 1, 4, 6, 2, 4]
if month < 3: year = year - 1
weekday = (year + year//4 - year//100 + year//400 + t[month-1] + day) mod 7
0 = Sunday, 1 = Monday … 6 = Saturday
```

Worked: 4 November 2026 → 2026 + 506 − 20 + 5 + 2 + 4 = 2523; 2523 mod 7 = 3 → Wednesday.

A mismatch is always a query, never a fix: either the weekday or the date may be the intended one. Offer both readings ("Wednesday 4 November or Thursday 5 November?").

Also flag impossible dates (31 April, 29 February in a year that is not a leap year) and a date range whose end comes before its start.

## Stated count against the list

When text says "three talks", "two options" or "four steps", count the items actually listed. A mismatch is a query naming both numbers.

## Totals

- Percentages of one whole should sum to 100. Allow 1 point for rounding when each figure is rounded; anything outside is a query with the computed sum.
- Stated totals ("12 sessions across the three weeks: 4, 5 and 4") are summed and compared.
- Ranges: the low end must be below the high end; units must match on both ends.

## Relative time against a reference date

The reference is the publish date for content-refresh and the document date elsewhere. The conversion table is in `dated-items.md` where present; the rule of thumb: "last year" = reference year − 1; "this year" = reference year; "next year" = reference year + 1; "X years ago" = reference year − X. Seasons assume the northern hemisphere unless the text or user says otherwise; say which was assumed.

## Change budget

Split original and output into sentences with the rule above. Pair them in order and compare. Print:

`sentences changed: n; with a logged change: n; unlogged: 0`

Any unlogged change is undone before output. Without a code tool, print the same line with "self-checked, not computed".

## Version comparison

Align approved and final by paragraph, then by sentence. Compare word by word inside each pair. Report insertions, deletions and replacements; a sentence with no partner is an addition or a removal.
