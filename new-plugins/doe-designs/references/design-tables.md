# Design tables

Detail behind the rules in the three SKILL.md files. Sources and read dates: [sources.md](sources.md). Factors are numbered 1…k as in the NIST tables; 1 = A, 2 = B and so on.

## Two-level fractional factorials (NIST §5.3.3.4.7 and its linked design files)

Defining relations are copied from the NIST design files (read 2026-10-12). Other generator sets can give designs of the same resolution; report whichever the user actually runs.

| Factors | Design | Runs | Defining relation (NIST file) |
|---|---|---|---|
| 3 | 2^(3−1)_III | 4 | I = 123 |
| 4 | 2^(4−1)_IV | 8 | I = 1234 |
| 5 | 2^(5−1)_V | 16 | I = 12345 |
| 5 | 2^(5−2)_III | 8 | I = 124 = 135 = 2345 |
| 6 | 2^(6−1)_VI | 32 | I = 123456 |
| 6 | 2^(6−2)_IV | 16 | I = 1235 = 2346 = 1456 |
| 6 | 2^(6−3)_III | 8 | I = 124 = 135 = 236 = 456 = 2345 = 1346 = 1256 |
| 7 | 2^(7−2)_IV | 32 | I = 12346 = 12457 = 3567 |
| 7 | 2^(7−3)_IV | 16 | I = 1235 = 2346 = 1347 = 1456 = 2457 = 1267 = 3567 |
| 7 | 2^(7−4)_III | 8 | I = 124 = 135 = 236 = 347 = 257 = 167 = 456 = … (15 words) |
| 8 | 2^(8−2)_V | 64 | I = 12347 = 12568 = 345678 |
| 8 | 2^(8−3)_IV | 32 | I = 1236 = 1247 = 23458 = 3467 = 14568 = 13578 = 25678 |
| 8 | 2^(8−4)_IV | 16 | I = 2345 = 1346 = 1237 = 1248 = … (15 words, shortest length 4) |

Further rows in the NIST summary (runs, resolution): 2^(7−1)_VII 64; 2^(8−1)_VIII 128; 2^(9−2)_VI 128; 2^(9−3)_IV 64; 2^(9−4)_IV 32; 2^(9−5)_III 16; 2^(10−3)_V 128; 2^(10−4)_IV 64; 2^(10−5)_IV 32; 2^(10−6)_III 16; 2^(11−4)_V 128; 2^(11−5)_IV 64; 2^(11−6)_IV 32; 2^(11−7)_III 16; 2^(15−11)_III 16; 2^(31−26)_III 32.

Reading a row: in 2^(5−2)_III, I = 124 means 4 = 12 (factor 4 is aliased with the 1×2 interaction); I = 135 means 5 = 13.

## Plackett-Burman (NIST §5.3.3.5)

| Runs | Up to factors |
|---|---|
| 12 | 11 |
| 20 | 19 |
| 24 | 23 |
| 28 | 27 |

Resolution III, no defining relation; interactions are partially correlated with other main-effect columns.

## Definitive screening (JMP 19.1)

| Factor types | k even | k odd |
|---|---|---|
| All continuous (minimum) | 2k + 1 | 2k + 3 |
| With categorical factors | 2k + 2 | 2k + 4 |

May need more runs where a conference matrix of the needed size is not known.

## Central composite α for rotatability (NIST Table 3.23)

| Factors | Factorial portion | α |
|---|---|---|
| 2 | 2^2 | 1.414 |
| 3 | 2^3 | 1.682 |
| 4 | 2^4 | 2.000 |
| 5 | 2^(5−1) | 2.000 |
| 5 | 2^5 | 2.378 |
| 6 | 2^(6−1) | 2.378 |
| 6 | 2^6 | 2.828 |

## Response surface run counts (NIST Table 3.28)

| Factors | Central composite | Box-Behnken |
|---|---|---|
| 2 | 13 (5 centre) | — |
| 3 | 20 (6 centre) | 15 (3 centre) |
| 4 | 30 (6 centre) | 27 |
| 5 | 33 (fractional) or 52 (full) | 46 |
| 6 | 54 (fractional) or 91 (full) | 54 |

Full quadratic terms p = (k+1)(k+2)/2: 2 factors 6, 3 factors 10, 4 factors 15, 5 factors 21, 6 factors 28.

## Mixture designs (NIST §5.5.4)

| Design | Points |
|---|---|
| Simplex-lattice {q, m} | (q+m−1)! / (m!(q−1)!) — {3,2} = 6, {3,3} = 10, {4,2} = 10 |
| Simplex-centroid, q components | 2^q − 1 — q = 3: 7, q = 4: 15 |

Pseudo-components for lower bounds: x*ᵢ = (xᵢ − Lᵢ)/(1 − L), L = ΣLᵢ < 1. NIST example: bounds 0.3, 0.4, 0.1 (L = 0.8); pseudo centroid (1/3, 1/3, 1/3) → actual (0.3667, 0.4667, 0.1667).
