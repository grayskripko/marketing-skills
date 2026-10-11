# Evidence rules

This file is identical in every skill that uses it. These are heuristics of this plugin, written so that anyone can recompute a label from the printed counts. They are not statistical tests.

## Counting

- Define N separately for each source type using usable research records; preserve the supplied record total and identify excluded non-research instructions by id. Redact sensitive details without dropping otherwise usable records. Do not sum source types into unique people or accounts unless overlap is known.
- A theme counts a source once, however many quotes from that source support it.
- Build source counts before writing findings. Cite supporting ids and meaningful counts within the requested deliverable; print a matrix only when requested for an audit trail.
- Use the host's code or spreadsheet tool for counts when it is available; otherwise count by hand and recount; never say how the counts were made.

## Weighted count

Default: each independent source contributes 1 per theme for unprompted support and 0.5 for prompted-only support. Use 0 for bare assent without customer-supplied detail when the question supplies the entire claim; retain its raw count. Merge records only when supplied ids establish the same participant/account; preserve record totals and state the counting unit. When interviewer wording is missing and prompting cannot be assessed, retain raw support and mark the affected weight unknown rather than assigning 0, 0.5 or 1. Calculate a support range using 0–1 for unknown contributions: give a strength label only if every value in that range gives the same label under the gates below; otherwise state "strength unresolved — prompting unknown", the count and the bounded finding. Prompted-only support never earns Strong. Show raw and weighted support when they differ, and disclose only the weighting or counting exception that affects the conclusion. These labels do not establish causation or prevalence.

## Strength labels (interviews, including churn interviews)

| Label | Rule |
|---|---|
| Strong | Default: Strong requires weighted support ≥3, raw support ≥ceil(N/3), N≥5, at least one unprompted supporting source, and no same-segment contrary report; Moderate requires weighted support ≥2 without Strong, including otherwise-Strong themes capped by a contradiction or N<5; Thin requires weighted support <2. Use the same numerical gates with N restricted to a named segment when supplied segment data show that the theme concerns only that segment; never choose a segment just to raise a label. Apply the N<5 cap within that segment. State the population and gates used beside the label. A Thin observation can lead when it directly answers the question or records a concrete consequential incident; retain Thin and its count rather than promoting its strength. |
| Moderate | Apply the default and segment-specific gates in the Strong row; weighted support ≥2, otherwise not Strong. State any contradiction or small-population cap. |
| Thin | Default weighted support <2. Use an explicitly bounded incident observation in the opening when the supplied incident directly answers the requested decision; keep Thin and the source count. |

A theme built only from opinion or feature-request tags carries "stated preference — check against behaviour".

## Contradiction or boundary

- A source **contradicts** a theme when it is in the same segment as at least one supporting source and reports the opposite of the theme statement itself. "The spreadsheet is fine" is the opposite of "copying is a pain", not of "they copy invoices". Only a contradiction caps the label at Moderate.
- A source from a segment with no supporting source that reports the opposite is a **boundary**, not a contradiction. Write the scope into the theme statement (for example "…for firms of 10–50 staff"), keep the label, and list the source under outliers with its segment.
- Segments are compared by the segment description (industry and size band).

## Exploratory line

- Default: with fewer than 5 independent interview sources in the population being described, say "Exploratory — k interviews; not for sizing" and cap otherwise-Strong themes at Moderate, leaving Thin unchanged. Use the named segment’s independent interview count when supplied data support a segment-specific claim, and separate interview and short-feedback counts when both are supplied. With 5 or more interviews omit the small-round line, but retain a claim-specific sampling qualification when recruitment excludes a relevant segment or the user asks about prevalence. State which source population was counted; no interview count makes market sizing valid.
- Default: omit the small-round line at N≥5; use a specific coverage or prevalence qualification when supplied recruitment or segment data reveal a gap. Say which limitation applies.

## Behaviour tags

Every quote gets one tag:

| Tag | Meaning | Weight |
|---|---|---|
| past behaviour | something the person did, with a when | highest |
| current workaround | how they cope today | high |
| opinion or prediction | what they think or say they would do | low |
| feature request | a proposed solution | low; trace it to the need behind it |

## Rounding

Default: compare exact counts with thresholds before rounding; print whole percentages, with halves rounded away from zero. Use one decimal place when unequal exact shares would otherwise display as the same percentage and the comparison matters. Show k/N and state the precision used. Rank exact ties equally using competition ranks (1, 2, 2, 4); use consecutive tied ranks (1, 2, 2, 3) only when the user supplies that ranking convention, and name it.

## Include with the affected claim

State limits on market prevalence, willingness to pay without past-spending evidence, and unsampled segments wherever the requested conclusion depends on them. Retain relevant contradictions and outliers with ids beside the claim they qualify. Separate sections are optional; these evidentiary qualifications are not.
