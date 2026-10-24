# Export interpretation and participation labels

Sources checked and retrieved 2026-10-11. These are local knowledge notes; using the skills does not require network access. Apply vendor facts only to an identified Qualtrics export, not every CSV.

## Qualtrics headers and response states

[Understanding Your Dataset](https://www.qualtrics.com/support/survey-platform/data-and-analysis-module/data/download-data/understanding-your-dataset/), sections “File Format Basics,” “Status / Response Type,” “Finished and Progress,” and “Question Responses.”

CSV/TSV has three header records: field IDs, field names/question text, then import IDs; responses start at record four. Detect this structure before removing metadata; preserve each layer and source record references. Do not blindly drop three records from a transformed file or apply this layout to XLSX. Reconcile response records separately from metadata.

Status can be values or labels: 0/IP Address (normal), 1/Survey Preview, 2/Survey Test, 4/Imported, 16/Offline, 17/Offline Preview, 256/Synthetic. Preserve raw status and decoded type; unknown codes stay unresolved. Apply the supplied inclusion policy, not an automatic status filter.

Finished=1/True means reaching an endpoint, including a screen-out. Imported responses with an empty Finished field default to True/1 regardless of Progress. Keep a supplied blank Finished value blank in the prepared data. Describe the documented import default separately from observed endpoint evidence: an empty exported field alone does not establish that the default was applied to this record. Neither the default nor endpoint status establishes substantive completion or eligibility. Preserve partial/imported records; use routing and the analysis policy to decide inclusion.

The dataset page describes labels as the default; inspect the actual export representation.

## Qualtrics recode lineage

[Recode Values](https://www.qualtrics.com/support/survey-platform/survey-module/question-options/recode-values/), sections “Recode Value Order,” “Possible Recode Values,” “Exporting a Data Dictionary,” and FAQs.

After the first response, recodes stop automatically following sequential choice order. Editing recodes changes later downloads, including previously collected answers. Different choices assigned the same recode become indistinguishable in exported values. The FAQ describes numeric values as the default, unlike the dataset page: support both values and labels; never decide representation from an assumed default.

Use a supplied dictionary matching the export and wave for interpretations that depend on its mapping. If the necessary mapping is absent, ask the user to supply the matching artifact; do not access the account. Deliver supported raw-code or combined-category results while leaving only mapping-dependent interpretations unresolved. Preserve raw code, mapped label, mapping source and export/mapping dates separately. A current dictionary does not establish an older export's mapping. If unavailable, report raw-code frequencies and identify the mapping needed; do not interpret a large code as better.

Dictionary recovery: Survey tab → Tools → Import/Export → Export survey to Word, with Show Coded Values enabled. Ask for this supplied artifact; do not access the account. It lists questions and recodes beside choices. When collisions already destroyed distinctions, a dictionary cannot reconstruct which choice was selected from a numeric export alone. Request label-level evidence only if the requested measure needs that distinction; a combined category remains countable when every colliding choice is on the same side of its boundary. Explain that boundary briefly beside the requested comparison.

## Participation boundary

[AAPOR Standard Definitions](https://aapor.org/standards-and-ethics/standard-definitions/), “Background” and “Downloads” (lists the 10th edition, 2023).

AAPOR outcome rates depend on final dispositions of sampled cases. Invitations and recorded replies alone do not establish a standardized response rate. For a descriptive ratio, name numerator and denominator units and the inclusion rule: e.g., unique people with at least one recorded reply per invited person, including partial replies. Repeated invitations are not automatically invited people.

For a requested standardized rate, obtain the relevant dispositions (complete interviews, partial interviews, eligible noninterviews, unknown eligibility and ineligible cases), survey mode/sample design, and selected published definition. Do not assign unknown eligibility or treat a recorded reply as a complete interview. Do not substitute an invitation ratio for the requested standardized result. This note supplies no AAPOR formula: applying one requires the relevant report/definition supplied locally and its required inputs. If the selected definition or required inputs are missing, state that the requested standardized rate remains unresolved and identify the missing inputs. Provide a separately labelled descriptive ratio only when its numerator and denominator are supported and it is useful to the request; do not present it as the requested standardized result.
