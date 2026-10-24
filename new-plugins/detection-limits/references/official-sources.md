# Sources for the MDL rules

Every page below was opened and read on 2026-10-13. The package makes no network requests at run time; these notes were embedded when it was built. The deciding rules are inline in each SKILL.md; this file records where they come from.

## 1. MDL procedure, Revision 2 (EPA stand-alone text)

https://www.epa.gov/sites/default/files/2016-12/documents/mdl-procedure_rev2_12-13-2016.pdf — read 2026-10-13. EPA 821-R-16-006, December 2016, "Definition and Procedure for the Determination of the Method Detection Limit, Revision 2"; the text of 40 CFR 136 Appendix B in stand-alone form.
- Scope and Application: spiked-sample MDLs may not be appropriate for all gravimetric methods (e.g. residue, total suspended solids); an MDL based on method blanks can be determined instead.
- Definition: minimum measured concentration reportable with 99% confidence that it is distinguishable from method blank results. Not applicable to non-continuous results (toxicity, presence/absence, colony counts) or to BOD, color, pH, conductance, many titrations.
- §2(a): spike level typically 2–10 times the estimated MDL; higher for very poor recovery.
- §2(b): at least 7 spiked samples and 7 method blanks through all steps; at least three batches on three separate calendar dates, analyzed on three separate calendar dates; preparation and analysis may be on the same day; existing data within 24 months allowed; most recent data must be used; no statistical outlier removal; documented gross failures may be excluded if 7 + 7 remain, with rationale on file. (i) multiple instruments: analyses distributed across all; (ii) at least two spikes and two blanks per instrument on different dates; (iii) one extract may run on several instruments if seven preparations in three batches are kept.
- §2(c): any spike result failing qualitative identification or not greater than zero → repeat at a higher level.
- §2(d): S from all instruments; MDLs = t(n−1, 0.99) × Ss; MDLb cases A (no numerical blanks: not applicable; ND is not numerical, negatives are), B (some numerical: highest; ≥100 blanks: rank n × 0.99 rounded, worked example 164 blanks → 162nd), C (all numerical: mean + t × Sb, mean zero if negative; note, printed p. 3: with 100 or more blanks MDLb may optionally be the concentration at or above the 99th percentile, as in B).
- §2(e): MDL = greater of MDLs and MDLb.
- §3(a): each quarter with sample analyses, at least two spikes per instrument in separate batches at the initial spike level; routine method blanks form the blank population. §3(b): 7 spikes and 7 blanks for the annual verification; one instrument may draw spikes from two years. §3(c)(i): more than 5% of spikes without a positive identified result → raise spike level and redo the initial MDL. §3(d): method change affecting sensitivity → redo initial MDL. §3(e): new instrument → two spikes and two blanks; MDLb validated if both blanks below the existing MDL; MDLs validated if within the §4(f) factor.
- §4(a): recalculate at least once every thirteen months. §4(b): last 24 months, same spike level only; gross-failure exclusions only; recent-data option if sensitivity changed, keeping 7 replicates in 3 batches on 3 days. §4(c): include initial spikes within 24 months. §4(d): only acceptable calibrations and batch QC; all routine data except rejected and reanalyzed batches. §4(e): all blanks of 24 months ideally; option of last six months or 50 most recent, whichever gives more. §4(f): verified MDL = greater of MDLs and MDLb; existing MDL may stay if verified MDL is within 0.5–2.0× and fewer than 3% of blank results are numerical above the existing MDL; otherwise adjust. Application to tables: when both conditions pass, the adopted MDL may differ from the newest calculated value, so a new calculation alone is not a table mismatch.
- Addendum: matrix-specific MDL; signal-to-noise about 5–20 without spiking, below 5 spike to about 10–20, above about 20 likely biased high; MDLb from method blanks, not the matrix. Table 1 one-tailed 99% t values for n = 7–100.
- Documentation: method identified, MDL in method reporting units, matrix identified, data reconstructable, mean spiked and recovered levels documented, outlier rationale on file.

## 2. Current regulatory text

https://www.ecfr.gov/current/title-40/chapter-I/subchapter-D/part-136/appendix-Appendix%20B%20to%20Part%20136 — read 2026-10-13 (via the eCFR renderer). Appendix B to Part 136 is titled Revision 2 and carries the same §2–§4 text quoted above (thirteen months, 24 months, fifty blanks, 0.5–2.0 and 3%, ND not numerical). The eCFR version history lists the last substantive amendment on 2017-09-27; later versions to 2024-06-03 are non-substantive.

## 3. EPA explanations

https://www.epa.gov/cwa-methods/method-detection-limit-frequent-questions — read 2026-10-13 (page last updated 8 September 2026).
- Revision 1.11 defined the MDL as 99% confidence that the concentration is greater than zero; Revision 2 adds method blanks (MDLb), year-round representative data, and pooling across instruments.
- The calculation is required once a year; spikes are run every quarter the method is used. No sample analyses in a quarter → no spikes needed; one batch → one spike in it; two or more batches → one spike in at least two of them.
- Fewer than 7 spikes available over two years → a new initial MDL, which may use the available samples.
- 100 or more blanks: the single highest blank is not used; rejected-batch data are not used.
- Initial MDL batch QC: an initial MDL run without client samples does not need most batch QC (MS/MSD not required); method calibrations still precede analysis; ongoing MDL samples run with client samples and carry normal batch QC.
- The implied Revision 1.11 requirement that the MDL be no less than one tenth of the spike value was removed in Revision 2.

https://www.epa.gov/cwa-methods/methods-update-rule-2017 — read 2026-10-13 (page last updated 16 December 2025). The 2017 Methods Update Rule (final rule 28 August 2017) revised the MDL procedure and added Methods 608.3, 624.1 and 625.1.

## 4. Water Quality Portal reporting

https://www.epa.gov/system/files/documents/2025-09/wqxdetectionlimitsbestpracticesguide_final.pdf — read 2026-10-13. EPA "WQX User Guidance: Detection Limits", August 2025, pp. 5–6. In the WQP legacy version the FullPhysicalChemical results profile returns one detection limit type per observation, chosen by a ranked hierarchy (Lower Quantitation Limit rank 2, Lower Reporting Limit rank 10, Method Detection Level rank 15); the beta version returns two. Other limits are in WQX Web, the Result Detection Limit profile or the ResultDetectionQuantitationLimitUrl field and can be joined by ResultIdentifier. Which WQP version is in production changes; check before relying on it.

## Rules of thumb of this plugin (no external source)

- Ratio and 3% blank tests are both required to keep an existing MDL (stated in §4(f)); the list of common lab errors in each skill is this plugin's own experience-based checklist, not an EPA list.
- The 3% denominator is taken as all blank results used for the analyte, ND included, reading "fewer than 3% of the method blank results … have numerical results above the existing MDL".
- t values for n not printed in EPA Table 1 (12–15, 17–20, 22–25, 27–30, 40, 60) were computed as the one-tailed 99% Student t quantile with n − 1 degrees of freedom; the same computation reproduces every value in Table 1 to three decimals.
- Units are converted only when printed; a likely 1000× slip is shown both ways. Analyte names are merged only when identity is certain; CAS number decides when present.
- Wet versus dry weight basis for solids is checked before comparing MDLs.
- An EPA MDL is kept separate from ICH Q2 detection and quantitation limits and from reporting limits; the plugin does not set reporting limits.
