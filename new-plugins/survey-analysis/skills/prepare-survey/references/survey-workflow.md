# Survey workflow notes

These are this plugin's rules of thumb for supplied-file analysis, not legal, statistical or platform requirements. No numerical privacy threshold or causal inference method is prescribed.

## Definitions

- A response row is not necessarily a unique person. Preserve both source-row and supplied respondent IDs.
- Eligible means the supplied routing says the question applies. Answered means a valid answer under the stated question definition. Unknown routing must remain unknown.
- A respondent share uses distinct respondents as the base. A selection share uses selected options as the base. A mention count needs its own explicit unit.
- A confirmed code records an interpretation supported by the answer. An uncertain code remains a review proposal. A coding workbook supports checking these interpretations; it does not establish that they are objectively true.
- Reidentification can occur through a quote, a small segment or subtraction of visible totals. Use the supplied disclosure policy and safe grouping; no universal cutoff is implied.
