# Sources for flare record rules

Every rule in the skills comes from the US Code of Federal Regulations, Title 40, Part 63, except one EPA interpretation letter noted under section 1. Each source below was opened and its text read on 2026-10-13. The current text was read from the eCFR database (Title 40 up to date as of 2026-10-08) through its official API; equations, which eCFR shows as images, were read from the 2025 annual edition PDF on govinfo.gov and match the current text. The eCFR page links are the human-readable copies of the same text; eCFR may show a browser check to scripted clients. The package makes no network requests at run time; these notes were embedded when it was built. The site's permit, monitoring plan and any approved alternative limits take precedence for a given flare.

## 1. Refinery flares — 40 CFR 63.670 (Subpart CC)

https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-63/subpart-CC/section-63.670 — read 2026-10-13 (current text, last amended 89 FR 23860, 4 April 2024). Equations: https://www.govinfo.gov/content/pkg/CFR-2025-title40-vol12/pdf/CFR-2025-title40-vol12-sec63-670.pdf — read 2026-10-13.
- (b) Pilot flame at all times when regulated material is routed; each 15-minute block with at least one minute of regulated material and no pilot flame is a deviation; blocks from one event count separately. Cross-lit stages of pressure-assisted flares: at least two pilots per stage.
- (c) No visible emissions except a total of 5 minutes in any 2 consecutive hours, when regulated material is routed and flow is below smokeless design capacity.
- (d) Tip velocity, when regulated material is routed for at least 15 minutes and flow is below smokeless capacity: Vtip < 60 ft/s, or Vtip < 400 ft/s and < Vmax, log10(Vmax) = (NHVvg + 1,212)/850. Pressure-assisted flares: no tip velocity limit; header pressure and staging-valve position monitoring instead.
- (e) NHVcz on a 15-minute block basis when regulated material is routed for at least 15 minutes: 270 Btu/scf, pressure-assisted 800 Btu/scf.
- (f), (n) NHVdil ≥ 22 Btu/ft² for flares actively receiving perimeter assist air; NHVdil = Qvg × Diam × NHVvg / (Qvg + Qs + Qa,premix + Qa,perimeter); Diam = 2 × √(Area/π). Air only entrained in steam with effective diameter ≥ 9 in: NHVcz only.
- (h) Initial 2-hour Method 22 observation; then a daily 5-minute observation on each day regulated material is routed, extended to 2 hours (or until 5 minutes of visible emissions) if emissions are seen for more than one continuous minute; or continuous video at least one frame every 15 seconds. (h)(1): visible emissions seen at any time while regulated material is routed require an immediate 5-minute Method 22 observation, even if that day's observation is already done.
- (i) Flow monitors corrected to 20 °C (68 °F) and 1 atm; Qvol = Qmass × 385.3 / MW; MW 18 for steam, 29 for air.
- (j) Composition: continuous (at least once every 15 minutes), grab samples at least every 8 hours of regulated flow, or a calorimeter (optional hydrogen analyser). Pipeline natural gas may be taken as 920 Btu/scf.
- (k) Fixed blocks from midnight (00:00–00:15 … 23:45–24:00); Vtip = Qcum / (Area × 900). (k)(2): for blocks with regulated flow, cumulative flow may cover only the periods when regulated material is sent, or the entire block, as the owner elects.
- (l) NHVvg = Σ xi × NHVi (Table 12); with a calorimeter and hydrogen analyser NHVvg = NHVmeasured + 938 × xH2. Direct method: average of results that become available during the block, by availability time. Direct-method exception (l)(5)(ii)(A): if the first sample of a periodic event is not available until after the second block starts, it is used for the first block. Feed-forward: most recent result available before the block; first sample of a periodic event covers the first block (and the second, if late). One elected method per flare at all times; a change in method needs notice to the Administrator 30 days in advance; pressure-assisted flares direct only (from 4 April 2024). Grab samples by collection time. Several streams: flow-weighted average.
- (m) NHVcz = Qvg × NHVvg / (Qvg + Qs + Qa,premix); no steam or premix air: NHVcz = NHVvg. Feed-forward with metered supplemental gas: [(Qvg − QNG2 + QNG1) × NHVvg + (QNG2 − QNG1) × NHVNG] / (Qvg + Qs + Qa,premix), QNG1 = QNG2 in the first block of an event.
- (n)(2) Feed-forward with representative vent-gas composition or NHV monitoring and directly metered supplemental gas uses the (m)(2) corrected numerator multiplied by Diam over the dilution denominator; first event block QNG1 = QNG2.
- (o)(5) Record completed corrective actions or the basis for taking none within 45 days; outstanding actions need an implementation schedule with proposed commencement and completion dates.
- (o)(3)–(4) Root-cause and corrective-action analysis within 45 days for a flow event above smokeless capacity with visible emissions over 5 minutes in 2 consecutive hours, or with Vtip above Vmax.
- (r) An approved site-specific limit replaces (d)–(f).

EPA interpretation of (d) and (e): letter from EPA OAQPS to the American Petroleum Institute, 3 April 2019, https://www.epa.gov/sites/default/files/2020-07/documents/ri_ritter_api_refinery_flaring_events_4.3.19.pdf — read 2026-10-13. Compliance with the velocity and NHVcz requirements is demonstrated starting with the block that contains the fifteenth minute of a flaring event; the earlier block in which the event started is not assessed. Agency interpretation, not rule text; it does not address NHVdil (f).

## 2. Flare monitoring systems — 40 CFR 63.671

https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-63/subpart-CC/section-63.671 — read 2026-10-13; also https://www.govinfo.gov/content/pkg/CFR-2025-title40-vol12/pdf/CFR-2025-title40-vol12-sec63-671.pdf.
- (a)(3) Each monitor completes at least one cycle in each 15-minute period.
- (c) The out-of-control procedure covers every CPMS installed under §63.670 except pilot-flame monitoring. (c)(1) Out of control: calibration drift above twice the Table 13 accuracy. (c)(2) The period begins in the hour the failing performance check is conducted and ends in the hour following completed corrective action and a successful demonstration; its data must not be used in averages or calculations.
- (d) Data may be rounded to the significant digits of the limit; periods of process non-operation and out-of-control periods are excluded from 15-minute block averages.

## 3. Definitions — 40 CFR 63.641

https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-63/subpart-CC/section-63.641 — read 2026-10-13; also https://www.govinfo.gov/content/pkg/CFR-2025-title40-vol12/pdf/CFR-2025-title40-vol12-sec63-641.pdf.
- Flare vent gas includes waste gas, unrecovered sweep gas, purge gas and supplemental gas, not pilot gas, steam or assist air. Perimeter versus premix assist air. Regulated material: streams required to be controlled under the subpart or a cross-referencing subpart.

## 4. Records and reports — 40 CFR 63.655

https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-63/subpart-CC/section-63.655 — read 2026-10-13; also https://www.govinfo.gov/content/pkg/CFR-2025-title40-vol12/pdf/CFR-2025-title40-vol12-sec63-655.pdf.
- (g)(11) Periodic report: pilot-deviation blocks; 2-hour periods with more than 5 minutes of visible emissions; blocks not meeting (d)–(f) with date, time, type and calculated value; root-cause events.
- (i)(9) Records: 15-minute block flows and calculated parameters; periods outside limits; periods without monitoring (viii); periods of vent gas with no regulated material, with start and stop times (ix); periods above smokeless capacity (x); visible-emission records with estimated minutes (ii)(C).

## 5. Component heating values — Table 12 to Subpart CC

https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-63/subpart-CC/appendix-Table%2012%20to%20Subpart%20CC%20of%20Part%2063 — read 2026-10-13 through the eCFR API; also https://www.govinfo.gov/content/pkg/CFR-2025-title40-vol12/xml/CFR-2025-title40-vol12-part63-subpartCC.xml.
- NHVi (Btu/scf): acetylene 1,404; benzene 3,591; 1,3-butadiene 2,690; iso-butane 2,957; n-butane 2,968; trans-butene 2,826; CO 316; ethane 1,595; ethylene 1,477; hydrogen 1,212; H2S 587; methane 896; C5+ 3,655; propane 2,281; propylene 2,150; CO2, N2, O2, water 0.
- Note a: the theoretical net heating value of hydrogen is 274 Btu/scf, but 1,212 Btu/scf is used for the flare requirements.

## 6. HON flares — 40 CFR 63.108 (Subpart F)

https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-63/subpart-F/section-63.108 — read 2026-10-13; also https://www.govinfo.gov/content/pkg/CFR-2025-title40-vol11/pdf/CFR-2025-title40-vol11-sec63-108.pdf.
- Applies §§63.670–63.671 with changes: "pilot flame or flare flame" (b); velocity and NHVcz judged from the block containing the fifteenth minute of a flaring event, not the earlier partial block (c); §63.670(o)(3)(ii) does not apply and the maximum tip velocity applies at all times (f); pressure-assisted multi-point flares: no tip velocity, NHVcz 800 Btu/scf, direct method only (i).

## 7. Ethylene production flares — 40 CFR 63.1103(e)(4) (Subpart YY)

https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-63/subpart-YY/section-63.1103 — read 2026-10-13; also https://www.govinfo.gov/content/pkg/CFR-2025-title40-vol12/pdf/CFR-2025-title40-vol12-sec63-1103.pdf.
- Same changes as the HON for the pilot wording (xii), the fifteenth-minute block (xiii), tip velocity at all times (iv) and pressure-assisted multi-point flares (vii).

## Rules of thumb of this plugin (no external source)

- Records disagreeing by a whole number of hours are first treated as a time-zone question.
- Near-match identifiers are never linked automatically; the latest stated revision of a record replaces earlier ones.
- Mole fractions that do not sum to about 1 are shown with their sum before any normalisation.
