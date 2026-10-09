# Evidence rules

This file is identical in every skill that uses it. These are heuristics of this plugin, written so that anyone can recompute a label from the printed counts. They are not statistical tests.

## Counting

- N = number of sources (interviews, calls) or items (reviews, tickets, answers) in the input.
- A theme counts a source once, however many quotes from that source support it.
- Build the theme × source counts before writing any theme statement or the opening answer. Print them after the answer; with fewer than 10 sources, as a "Sources" column of ids in the themes table.
- Use the host's code or spreadsheet tool for counts when it is available; otherwise count by hand and recount; never say how the counts were made.

## Weighted count

A source that supports a theme with at least one unprompted quote counts 1. A source whose only support is quotes marked "prompted" (answers to a leading or hypothetical question) counts 0.5. Print the weighted count next to the raw count when they differ. Prompted quotes never lift a theme to Strong on their own.

## Strength labels (interviews, including churn interviews)

| Label | Rule |
|---|---|
| Strong | weighted count at least 3, raw count at least one third of N, and no source that contradicts the theme |
| Moderate | weighted count at least 2 without meeting Strong, or meeting Strong with a contradicting source |
| Thin | weighted count below 2: for example one source, or several whose only support is prompted answers. Kept and flagged with its count, never presented as a main finding |

A theme built only from opinion or feature-request tags carries "stated preference — check against behaviour".

## Contradiction or boundary

- A source **contradicts** a theme when it is in the same segment as at least one supporting source and reports the opposite of the theme statement itself. "The spreadsheet is fine" is the opposite of "copying is a pain", not of "they copy invoices". Only a contradiction caps the label at Moderate.
- A source from a segment with no supporting source that reports the opposite is a **boundary**, not a contradiction. Write the scope into the theme statement (for example "…for firms of 10–50 staff"), keep the label, and list the source under outliers with its segment.
- Segments are compared by the segment description (industry and size band).

## Exploratory line

- With fewer than 5 sources, put "Exploratory — fewer than 5 sources; not for sizing" directly under the opening answer and use no Strong label; themes that would be Strong are labelled Moderate.
- With 5 or more sources, do not mention the exploratory line at all.

## Behaviour tags

Every quote gets one tag:

| Tag | Meaning | Weight |
|---|---|---|
| past behaviour | something the person did, with a when | highest |
| current workaround | how they cope today | high |
| opinion or prediction | what they think or say they would do | low |
| feature request | a proposed solution | low; trace it to the need behind it |

## Rounding

Compare counts with thresholds before rounding. Print shares as whole percentages, rounding half away from zero. Ties in rankings share a rank (1, 2, 2, 4).

## Always print

- "What we cannot conclude from this data", in 2 to 4 bullets: how common the need is in the market, willingness to pay unless past spending was discussed, and segments not sampled.
- Contradictions and outliers, each with ids.
