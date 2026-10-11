# Evidence rules

This file is identical in every skill that uses it. These are heuristics of this plugin, written so that anyone can recompute a label from the printed counts. They are not statistical tests.

## Counting

- Define N separately for each source type using usable research records; preserve the supplied record total and identify excluded non-research instructions by id. Redact sensitive details without dropping otherwise usable records. Do not sum source types into unique people or accounts unless overlap is known.
- A theme counts a source once, however many quotes from that source support it.
- Build source counts before writing findings. Cite supporting ids and meaningful counts within the requested deliverable; print a matrix only when requested for an audit trail.
- Use the host's code or spreadsheet tool for counts when it is available; otherwise count by hand and recount; never say how the counts were made.

## Weighted count

For interview-derived evidence, separate spontaneous reports, elicited concrete experience, leading agreement and hypothetical preference. Count raw sources once per theme. Do not weight by default. If the user requests the legacy heuristic, unprompted support counts 1 and prompted-only support counts 0.5; show raw and weighted support, disclose the convention and compare sensitivity. This is not a bias correction or effectiveness measure. Use item-count rules for short feedback and keep mixed-source denominators separate.

## Strength labels (interviews, including churn interviews)

Use raw k/N, evidence type, independence, coverage, corroboration and contrary evidence by default. The legacy Strong/Moderate/Thin scheme is optional for comparable interviews when requested: Strong ≥3 weighted sources and ≥one third raw support with no contrary source; Moderate ≥2 weighted sources or contrary evidence; Thin <2. These are descriptive conventions only. Keep rare consequential observations eligible as findings with their actual count and scope.

A theme built only from opinion or feature-request tags carries "stated preference — check against behaviour".

## Contradiction or boundary

- A source **contradicts** a theme when it is in the same segment as at least one supporting source and reports the opposite of the theme statement itself. "The spreadsheet is fine" is the opposite of "copying is a pain", not of "they copy invoices". If the optional legacy label scheme is requested, a contradiction caps its label at Moderate; otherwise report the contrary evidence and scope directly.
- A source from a segment with no supporting source that reports the opposite is a **boundary**, not a contradiction. Write the scope into the theme statement (for example "…for firms of 10–50 staff"), retain the source and its segment as contrary evidence; retain a label only if the optional scheme was requested.
- Compare segments using decision-relevant supplied attributes, such as role, workflow, tenure, product version, use context, industry or size. Keep unexplained variation visible; do not create post-hoc segments merely to improve a strength label.

## Exploratory line

Qualify prevalence-sensitive claims according to recruitment, independence, coverage and the target population at any N. State the relevant source type and usable count when coverage matters. Five sources do not remove a sampling limitation or establish market prevalence.

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

## Include with the affected claim

State limits on market prevalence, willingness to pay without past-spending evidence, and unsampled segments wherever the requested conclusion depends on them. Retain relevant contradictions and outliers with ids beside the claim they qualify. Separate sections are optional; these evidentiary qualifications are not.
