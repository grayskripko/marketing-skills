# File source register

## W3C — WebVTT

URL: https://www.w3.org/TR/webvtt/
Version loaded: Candidate Recommendation Draft, 2026-05-20.
Dated version: https://www.w3.org/TR/2026/CRD-webvtt1-20260520/
Read 2026-10-11. Loaded full specification. Sections 4.1–4.2 and 6 cover UTF-8, optional BOM, WEBVTT signature, block syntax, unique optional cue identifiers, voice spans and timestamp grammar. Starts are nondecreasing, end exceeds start; overlap is allowed. Valid format syntax is separate from platform display support for styling/regions.

## Library of Congress — SRT

URL: https://www.loc.gov/preservation/digital/formats/fdd/fdd000569.shtml
Read 2026-10-11. Loaded format description. Header reports significant update 2025-05-27; footer reports update 2026-05-27. Preserve this distinction.

Conventional blocks: numeric counter, start/end separated by -->, hours:minutes:seconds,milliseconds, text, blank separator. Notes include an inline-counter variant. SRT has no single character-encoding standard. This is a format description, not Apple/Spotify ingestion policy. Its line-length and filename advice are not imported as platform blockers.

## Authored review choices

Preserve timing and words; ask for verified times rather than extrapolating. Duration comparison, byte-size evidence, unknown-boundary handling and UTF-8 SRT recommendation are review practices. Only actual supplied bytes establish original encoding/size. Text without corresponding audio evidence cannot establish alignment or speech coverage.
