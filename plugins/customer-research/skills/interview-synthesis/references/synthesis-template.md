# Synthesis full layout

Use this when the user asks for a full synthesis or audit trail. Select relevant sections, preserve the requested shape and avoid repeating the answer. Retain evidence checks, sample warnings and strength qualifications wherever they apply.

Include source-specific sampling qualifications only where they change interpretation; no automatic warning transition occurs at five sources.

## 1. Sources

| Id | Date | Segment | Role | Length |
|---|---|---|---|---|
| S01 | 2026-09-02 | [accounting firm, 20–50 staff, UK] | operations lead | ~2,900 words |

Leave out the Date and Length columns when the input gives neither. Do not append a fixed privacy reminder; apply redaction and minimisation throughout.

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

Each with its evidence line. Include decision-relevant rare observations with their actual support and bounded scope; a support label does not determine decision priority.

## 10. What we cannot conclude from this data

## 11. Assumptions

## 12. Self-check

Run before printing and fix every failure (theme lines without quote ids; quotes not found verbatim in the redacted input). Print this section only when the user asked for the audit trail, or to list a failure that could not be fixed. Do not hide failures.
