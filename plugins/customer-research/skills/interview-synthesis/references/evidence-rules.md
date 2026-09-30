# Evidence rules

This file is identical in every skill that uses it. These rules are heuristics of this plugin, written so that anyone can recompute a label from the printed counts. They are not statistical tests.

## Counting

- N = number of sources (interviews, calls) or items (reviews, tickets, answers) in the input.
- A code or theme counts a source once, however many quotes from that source support it.
- Print the theme × source matrix before any theme statement.
- Use the host's code or spreadsheet tool for counts when it is available; otherwise write "approximate" next to each count.

## Weighted count

A source that supports a theme with at least one unflagged quote counts 1. A source that supports it only with quotes flagged "low-weight: prompted" (answers to a leading or hypothetical question) counts 0.5. Print both the raw count and the weighted count.

## Strength labels (interviews and churn notes)

| Label | Rule |
|---|---|
| Strong | weighted count at least 3, raw count at least one third of N, and no source that contradicts the theme |
| Moderate | weighted count at least 2 without meeting Strong, or meeting Strong with a contradicting source |
| Single-source | weighted count below 2. Kept and flagged, never in the top findings |

## Contradiction or boundary

- A source **contradicts** a theme when it is in the same segment as at least one supporting source and reports the opposite experience. Only a contradiction caps the label at Moderate.
- A source from a segment with no supporting source that reports the opposite is a **boundary**, not a contradiction. Write the scope into the theme statement (for example "…for firms of 10–50 staff"), keep the label, and list the source under outliers with its segment.
- Segments are compared by the segment description in the sources table (industry and size band).

## Exploratory line

- With fewer than 5 sources, write "Exploratory — fewer than 5 sources; not for sizing" at the top and use no Strong label; themes that would be Strong are labelled Moderate.
- With 5 or more sources, do not mention the exploratory line at all.
- Prompted quotes therefore never lift a theme to Strong on their own.
- A theme built only from opinion or feature-request tags carries "stated preference — check against behaviour".

## Behaviour tags

Every ledger quote gets one tag:

| Tag | Meaning | Weight |
|---|---|---|
| past behaviour | something the person did, with a when | highest |
| current workaround | how they cope today | high |
| opinion or prediction | what they think or say they would do | low |
| feature request | a proposed solution | low; trace it to the need behind it |

## Rounding

Compare counts with thresholds before rounding. Print shares as whole percentages, rounding half away from zero. Ties in rankings share a rank (1, 2, 2, 4).

## Always print

- "What we cannot conclude from this data": at least how common the need is in the market, willingness to pay unless past spending was discussed, and anything about segments not sampled.
- Contradictions and outliers, each with ids.
