# Sources

Every URL below was opened on 2026-10-12 and the stated passage was checked on the page. The package makes no network requests at runtime; these are build-time references. NIST pages are the NIST/SEMATECH e-Handbook of Statistical Methods, chapter 5 (Process Improvement). The hosted handbook pages carry no revision date; the date below is the date read.

## Design selection and blocking

- **NIST §5.3.3 How do you select an experimental design?** https://www.itl.nist.gov/div898/handbook/pri/section3/pri33.htm — read 2026-10-12. Guideline: 2–4 factors, screening by full or fractional factorial, response surface by central composite or Box-Behnken; 5+ factors, screening by fractional factorial or Plackett-Burman, response surface after screening.
- **NIST §5.3.3.2 Randomized block designs.** https://www.itl.nist.gov/div898/handbook/pri/section3/pri332.htm — read 2026-10-12. "Block what you can, randomize what you cannot."
- **NIST §5.3.3.3.2 Full factorial example.** https://www.itl.nist.gov/div898/handbook/pri/section3/pri3332.htm — read 2026-10-12. Randomize runs as much as possible; keep standard order for re-sorting; replication gives a dispersion estimate per setting.
- **NIST §5.3.3.3.3 Blocking of full factorial designs.** https://www.itl.nist.gov/div898/handbook/pri/section3/pri3333.htm — read 2026-10-12. 2^3 in two blocks of four via the X1·X2·X3 column; the three-factor interaction is confounded with blocks. Use one or a combination of high-order interaction columns to build blocks.
- **NIST §5.3.3.7 Adding centerpoints.** https://www.itl.nist.gov/div898/handbook/pri/section3/pri337.htm — read 2026-10-12. Purposes: process stability/inherent variability and curvature check. About 3–5 centre runs for factorials; 2 ≤ nc ≤ 5 best for response surface designs. Not randomized; dispersed through the matrix, beginning and end. Discrete factors at standard settings with continuous factors at centre count as centre points.

## Fractional factorials and aliasing

- **NIST §5.3.3.2.4 Design resolution.** https://www.itl.nist.gov/div898/handbook/pri/section3/pri3324.htm — read 2026-10-12. Resolution = length of shortest word in the defining relation. III: main effects aliased with 2FIs; IV: main effects clear of 2FIs, 2FIs aliased with each other; V: main effects and 2FIs clear of each other. Defining relation is not unique (alternative generator sets give the same design).
- **NIST §5.3.3.4.3 Confounding (aliasing).** https://www.itl.nist.gov/div898/handbook/pri/section3/pri3343.htm — read 2026-10-12. I = 123 gives 1 = 23, 2 = 13, 3 = 12; positive generators give the principal fraction.
- **NIST §5.3.3.4.4 Design specifications and resolution.** https://www.itl.nist.gov/div898/handbook/pri/section3/pri3344.htm — read 2026-10-12. p generators; the defining relation has 2^p − 1 words.
- **NIST §5.3.3.4.7 Summary tables.** https://www.itl.nist.gov/div898/handbook/pri/section3/pri3347.htm — read 2026-10-12. Design labels, runs and resolution for 3–11, 15 and 31 factors (see design-tables.md).
- **NIST §5.3.3.5 Plackett-Burman designs.** https://www.itl.nist.gov/div898/handbook/pri/section3/pri335.htm — read 2026-10-12. Run counts are multiples of 4; 12 runs for up to 11 factors, 20 for 19, 24 for 23, 28 for 27; resolution III, saturated main-effect designs; no defining relation; an interaction column is correlated with every other main-effect column.
- **NIST §5.3.3.8.1 Mirror-image foldover.** https://www.itl.nist.gov/div898/handbook/pri/section3/pri3381.htm — read 2026-10-12. Reverse all signs; a resolution III design plus its mirror image becomes resolution IV; never used to follow up a resolution IV design.
- **NIST §5.3.3.8.2 Alternative foldover.** https://www.itl.nist.gov/div898/handbook/pri/section3/pri3382.htm — read 2026-10-12. Reversing one column de-aliases that factor and its 2FIs; combined 2^(7−4) example: 16 runs, 14 effects, one degree of freedom for a block; remains resolution III for other factors.
- **JMP 19.1 Structure of definitive screening designs** (SAS Institute, publication date 2026-01-13). https://www.jmp.com/support/help/en/19.1/jmp/structure-of-definitive-screening-designs.shtml — read 2026-10-12. Minimum runs 2k+1 (k even) or 2k+3 (k odd) for continuous factors; categorical: 2k+2 / 2k+4; foldover removes main-effect/2FI confounding; next-larger conference matrix may raise run count. Vendor documentation of a published construction.

## Response surface designs

- **NIST §5.3.3.6 Response surface designs.** https://www.itl.nist.gov/div898/handbook/pri/section3/pri336.htm — read 2026-10-12. Centre points added to a two-level design confound all quadratic effects with each other: curvature is detected, individual pure quadratic effects are not estimated.
- **NIST §5.3.3.6.1 Central composite designs.** https://www.itl.nist.gov/div898/handbook/pri/section3/pri3361.htm — read 2026-10-12. CCC star points set new extremes (5 levels); CCI for true limits, CCC scaled by 1/α (5 levels); CCF α = 1 (3 levels), not rotatable. Rotatable α = (factorial runs)^(1/4); Table 3.23: 1.414, 1.682, 2.000, 2.000 (2^(5−1)), 2.378 (2^5), 2.378 (2^(6−1)), 2.828 (2^6). α also depends on orthogonal blocking.
- **NIST §5.3.3.6.2 Box-Behnken designs.** https://www.itl.nist.gov/div898/handbook/pri/section3/pri3362.htm — read 2026-10-12. Three levels, points at edge midpoints and centre, no embedded factorial, rotatable or near rotatable, limited orthogonal blocking.
- **NIST §5.3.3.6.3 Comparisons of response surface designs.** https://www.itl.nist.gov/div898/handbook/pri/section3/pri3363.htm — read 2026-10-12. Table 3.28 run counts; Table 3.27 pros and cons (CCC needs feasibility check of settings beyond original ranges; CCF poor precision for pure quadratic coefficients; Box-Behnken avoids extreme combinations, poor prediction regions).

## Mixture designs

- **NIST §5.5.4 What is a mixture design?** https://www.itl.nist.gov/div898/handbook/pri/section5/pri54.htm — read 2026-10-12. Proportions sum to one; standard designs simplex-lattice and simplex-centroid; extra bounds call for constrained (extreme vertices) designs.
- **NIST §5.5.4.2 Simplex-lattice designs.** https://www.itl.nist.gov/div898/handbook/pri/section5/pri542.htm — read 2026-10-12. Points (q+m−1)!/(m!(q−1)!), equal to terms in the canonical polynomial; {3,3} = 10 runs; add interior points for interior prediction.
- **NIST §5.5.4.3 Simplex-centroid designs.** https://www.itl.nist.gov/div898/handbook/pri/section5/pri543.htm — read 2026-10-12. 2^q − 1 points; supports quadratic (q = 2) and special cubic (q = 3).
- **NIST §5.5.4.4 Constrained mixture designs.** https://www.itl.nist.gov/div898/handbook/pri/section5/pri544.htm — read 2026-10-12. Pseudo-components x*ᵢ = (xᵢ − Lᵢ)/(1 − L), L = ΣLᵢ < 1; example bounds 0.3/0.4/0.1, centroid maps to (0.3667, 0.4667, 0.1667); D-optimal or extreme vertices for other constrained regions.

## Execution: experimental unit and restricted randomization

- **Penn State STAT 502, Lesson 7, §7.1 Experimental unit and replication.** https://online.stat.psu.edu/stat502/Lesson07 — read 2026-10-12. Experimental unit receives the treatment; sampling units are where observations are recorded; treating sampling units as experimental units is pseudo-replication, inflating error degrees of freedom and the F statistic. Note: the server's TLS chain is incomplete for strict command-line clients; the page loads (HTTP 200) when the chain is completed, as browsers do.
- **Stat-Ease Design-Expert v25 documentation, Randomized vs. split-plot designs.** https://www.statease.com/docs/v25.0/contents/design/randomized-vs-split-plot/ — read 2026-10-12. Split-plot designs control how often a hard-to-change factor is reset; analysis takes the restriction into account; power and precision are worse for hard-to-change factors. Vendor documentation.

## Pharmaceutical design space

- **ICH Q8(R2) Pharmaceutical Development, FDA guidance copy, November 2009 (Revision 2).** https://www.fda.gov/media/71535/download — read 2026-10-12. Design space definition; working within it is not a change; proposed by the applicant, subject to regulatory assessment and approval; small/pilot-scale design space relevance to production scale must be justified (2.4.4); a combination of proven acceptable ranges does not constitute a design space (2.4.5).

## Calculation conventions used without a separate source

These are arithmetic, not rules from a standard: coded = (actual − centre)/half-range; full quadratic term count p = (k+1)(k+2)/2 (intercept + k linear + k quadratic + k(k−1)/2 interactions); error degrees of freedom = runs − p; alias by multiplying with each word and cancelling squares (as in NIST §5.3.3.4.3); with 4 blocks the product of the two block columns is also confounded (column product).

## This plugin's rules of thumb

Not from a standard, chosen for safety and clarity: refuse actual settings without approved bounds; never place a run outside approved bounds; never present a hand-made run order as random; no optimum claim at the design stage.
