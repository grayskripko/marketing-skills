# Synthesis full layout

Use this for full transcripts, or when the user asks for the audit trail. It comes after the opening answer (SKILL.md, "How the answer reads"). Leave out any section with nothing in it.

If N < 5, the line directly under the opening answer is: **Exploratory — fewer than 5 sources; not for sizing.** If N ≥ 5, say nothing about it.

## 1. Sources

| Id | Date | Segment | Role | Length |
|---|---|---|---|---|
| S01 | 2026-09-02 | [accounting firm, 20–50 staff, UK] | operations lead | ~2,900 words |

Leave out the Date and Length columns when the input gives neither. Below the table, one fixed line: **Reminder: remove personal data you do not need before pasting.**

## 2. Quote ledger

| Id | Quote (verbatim, redacted) | What it shows | Tag | Prompted |
|---|---|---|---|---|
| S03-Q07 | "Month-end takes us four days, and one of those is copy-paste." | pain; cost of workaround | past behaviour | |
| S05-Q02 | "Yes, a dashboard would be nice." | feature request | feature request | yes |

Quotes are at most about 40 words; cut only at sentence boundaries and mark the cut with "…".

## 3. Theme × source matrix

| Theme | S01 | S02 | S03 | … | Sources | Segments |
|---|---|---|---|---|---|---|
| Month-end is manual | 1 | 0 | 1 | … | 4 of 11 | 2 |

## 4. Themes

| Theme | Evidence | Count | Strength | Notes |
|---|---|---|---|---|
| Month-end close is slowed by manual transfer between bank and books, for firms of 10+ staff | S01-Q03, S03-Q07, S06-Q01, S09-Q04 | 4 of 11 sources, 2 segments | Strong | S08 (under 10 staff, a segment with no supporting source) reports the opposite: listed under outliers |

## 5. Contradictions and outliers

Contradictions (same segment, opposite experience) and boundaries (other segment, opposite experience), each with ids and segment. Thin themes worth watching, with ids.

## 6. Next steps

Up to 5 actions, each with the ids it would settle.

## 7. Needs behind requests

| Request (id) | Need behind it (ids) |
|---|---|

## 8. Customer phrase bank

Verbatim phrases by theme, with ids.

## 9. Top findings (up to 5)

Each with its evidence line. Thin themes never appear here.

## 10. What we cannot conclude from this data

## 11. Assumptions

## 12. Self-check

Run before printing and fix every failure (theme lines without quote ids; quotes not found verbatim in the redacted input). Print this section only when the user asked for the audit trail, or to list a failure that could not be fixed. Do not hide failures.
