# Sources

Every URL below was opened on 2026-10-12 and the stated content checked on the page. The package makes no network requests at run time; these are build-time references. Where a page states no edition date, the date given is the date read. Anything not traced to a source here is labelled as this plugin's rule of thumb.

## Standard

**ISO 7870-2:2023 Control charts — Part 2: Shewhart control charts.** Edition 2, published 2023-03, replaces ISO 7870-2:2013 (withdrawn). Scope limited to Shewhart charts; also covers warning limits, trend patterns and process capability briefly. Full text is paid; only the catalogue entry was read.
https://committee.iso.org/standard/78859.html — read 2026-10-12.

## NIST/SEMATECH e-Handbook of Statistical Methods (current hosted pages, undated)

- **§6.3.1 What are control charts?** ±3σ limits are typical; basing limits on a multiple of the standard deviation is acceptable practice whether or not X is normal; skew changes the false-alarm risk.
  https://www.itl.nist.gov/div898/handbook/pmc/section3/pmc31.htm — read 2026-10-12.
- **§6.3.2 Variables control charts.** Western Electric rules: 1 point beyond 3σ; 2 of last 3 beyond 2σ; 4 of last 5 beyond 1σ; 8 consecutive on one side; also 6 trending and 14 alternating. Average run length to a false alarm: 371 for 3σ only, about 91.75 with Western Electric rules (Champ and Woodall 1987), under a normal model with known parameters; limits from limited data can behave quite differently. Recalculate limits only for a valid, compelling reason, such as a major process change or at least 30 more points with no known process change. Control limits judge statistical control; specification limits judge whether product will function.
  https://www.itl.nist.gov/div898/handbook/pmc/section3/pmc32.htm — read 2026-10-12.
- **§6.3.2.1 Xbar-R and Xbar-S charts.** Formulas with A2, D3, D4 (table n = 2–10) and c4. Range method satisfactory up to n ≈ 10; standard deviation preferable for larger subgroups. Use the S chart first to judge stability of spread.
  https://www.itl.nist.gov/div898/handbook/pmc/section3/pmc321.htm — read 2026-10-12.
- **§6.3.2.2 Individuals control charts.** MRᵢ = |xᵢ − xᵢ₋₁|; limits x̄ ± 3·MR̄/1.128, d2 = 1.128 for n = 2. Worked example: x̄ = 50.81, MR̄ = 1.8778, UCL 55.8041, LCL 45.8159. MR-chart D4 = 3.267 is taken from the §6.3.2.1 table at n = 2.
  https://www.itl.nist.gov/div898/handbook/pmc/section3/pmc322.htm — read 2026-10-12.
- **§6.3.2.4 EWMA control charts.** λ usually 0.2–0.3 (a somewhat arbitrary choice); for t not small, approximate limits EWMA₀ ± k·s·√(λ/(2−λ)). Reference only; the skills do not set up EWMA charts.
  https://www.itl.nist.gov/div898/handbook/pmc/section3/pmc324.htm — read 2026-10-12.
- **§6.3.3 Attributes control charts.** c chart for counts of defects, p chart for proportion defective, u chart for defects per unit.
  https://www.itl.nist.gov/div898/handbook/pmc/section3/pmc33.htm — read 2026-10-12.
- **§6.3.3.1 Counts control charts.** c̄ ± k√c̄, k usually 3; if LCL is negative there is no lower control limit; Poisson assumptions.
  https://www.itl.nist.gov/div898/handbook/pmc/section3/pmc331.htm — read 2026-10-12.
- **§6.3.3.2 Proportions control charts.** p ± 3√(p(1−p)/n); p̄ = ΣDᵢ/(mn).
  https://www.itl.nist.gov/div898/handbook/pmc/section3/pmc332.htm — read 2026-10-12.
- **§6.1.6 Process capability.** Cp, Cpk, Cpm formulas, with sample estimators using s; capability applies to an in-control process; indices assume normality; about 50 independent values for index estimates; at least 25 for confidence-interval approximations; generally n ≥ 100 for capability studies; Box-Cox or nonparametric indices for nonnormal data.
  https://www.itl.nist.gov/div898/handbook/pmc/section1/pmc16.htm — read 2026-10-12.

## SAS/QC User's Guide (software documentation)

Historical editions 13.1 and 14.1 are cited; the publisher lists SAS/QC 15.4 and SAS/QC on SAS Viya as the most recent releases (https://support.sas.com/en/software/sas-qc-support.html, read 2026-10-13).

- **Standard tests for special causes (SAS/QC 13.1).** Eight tests in Nelson numbering; test 2 is 9 in a row on one side by default; for c, np, p and u charts only tests 1–4 are recommended, and test 2 only if the distribution is near symmetric. By default tests are not applied when limits vary with subgroup size; the LIMITN= or TESTNMETHOD= options allow it.
  https://support.sas.com/documentation/cdl/en/qcug/66857/HTML/default/qcug_shewhart_sect540.htm — read 2026-10-12.
- **p charts (SAS/QC 14.1).** p̄ = Σ(nᵢpᵢ)/Σnᵢ; LCL = max(p̄ − k√(p̄(1−p̄)/nᵢ), 0); UCL = min(p̄ + k√(…), 1); k defaults to 3.
  https://support.sas.com/documentation/cdl/en/qcug/68161/HTML/default/qcug_shewhart_sect221.htm — read 2026-10-12.
- **u charts (SAS/QC 13.1).** ū = Σcᵢ/Σnᵢ; LCL = max(ū − k√(ū/nᵢ), 0); UCL = ū + k√(ū/nᵢ).
  https://support.sas.com/documentation/cdl/en/qcug/66857/HTML/default/qcug_shewhart_sect348.htm — read 2026-10-12.

## Minitab Statistical Software support (software documentation)

- **Tests for special causes.** Eight tests (test 2: nine in a row on one side). For R, S and moving range charts only tests 1–4; attribute charts tests 1–4; adding tests raises false signals.
  https://support.minitab.com/minitab/help-and-how-to/quality-and-process-improvement/control-charts/supporting-topics/basics/using-tests-for-special-causes/ — read 2026-10-12.
- **I-MR chart data considerations.** Time order; at least 100 observations, else preliminary; correlated observations make limits too narrow.
  https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/control-charts/how-to/variables-charts-for-individuals/i-mr-chart/before-you-start/data-considerations/ — read 2026-10-12.
- **Xbar-R chart data considerations.** Subgroups of 8 or fewer (9 or more: Xbar-S); minimum observations 100 / 80 / 70 / 60 by subgroup size; non-rational subgroups make limits too wide; correlated observations make them too narrow.
  https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/control-charts/how-to/variables-charts-for-subgroups/xbar-r-chart/before-you-start/data-considerations/ — read 2026-10-12.
- **P chart data considerations.** Too few subgroups: preliminary; over- and underdispersion distort a traditional p chart; Laney P' chart.
  https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/control-charts/how-to/attributes-charts/p-chart/before-you-start/data-considerations/ — read 2026-10-12.
- **Normal capability analysis data considerations.** Process must be stable; normal distribution; at least 100 data points; rational subgroups.
  https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/capability-analysis/how-to/capability-analysis/normal-capability-analysis/before-you-start/data-considerations/ — read 2026-10-12.
- **Normal capability analysis key results.** Cpk = potential capability, Ppk = overall capability; approximately equal in statistical control; many industries use a 1.33 benchmark; verify stability with a control chart first; Between/Within capability analysis for processes with natural variation between subgroups.
  https://support.minitab.com/minitab/help-and-how-to/quality-and-process-improvement/capability-analysis/how-to/capability-analysis/normal-capability-analysis/interpret-the-results/key-results — read 2026-10-12.
- **How Cpk and Ppk are calculated, part 1 (Minitab Blog, 2014-12-08, updated 2024-04-29).** Ppk uses the overall standard deviation, Cpk the within-subgroup one; Minitab defaults to the pooled standard deviation for subgroups larger than 1.
  https://blog.minitab.com/en/how-cpk-and-ppk-are-calculated2c-part-1 — read 2026-10-12.

## This plugin's rules of thumb (no external source)

- Default to rounding limits to one more decimal than the measurement resolution; retain more digits when distinct limits or boundary crossings would be obscured, or follow specified reporting precision. Use unrounded limits for signals.
- A tie breaks a trend run (common software convention; check the user's software).
- Pattern-to-cause hints in control-chart-signals (tool wear, alternating sources, mixed streams) are investigation leads, not sourced rules.
- Lag-1 correlation as a quick autocorrelation check; the listed signs of autocorrelation and the remedies (sampling less often, charting residuals) are investigation suggestions.
- Checking repeated identical ranges or permutations against records and gauge resolution is an investigation heuristic.
