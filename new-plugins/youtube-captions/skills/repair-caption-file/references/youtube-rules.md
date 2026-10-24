# YouTube caption rules and timed-text syntax

Verified loaded 2026-10-11 (read 2026-10-11). Recheck before the planned 2026-10-15 submission if these rules decide release. Help pages show no update date; retrieval date is not a publication date.

## YouTube file support

https://support.google.com/youtube/answer/2734698?hl=en — official Help, no update date shown. Basic SRT and SBV require plain UTF-8; their styling is ignored. Their examples distinguish comma milliseconds plus arrow (SRT) from period milliseconds plus comma between times (SBV). WebVTT positioning is supported, styling is limited to b/i/u. SAMI and RealText support simple markup but no positioning. TTML support is partial; DFXP is interpreted as TTML, and iTT is supported. SCC is preferred for CEA-608 features; STL and several binary broadcast types also exist. `.cap` names more than one format. Apply these support rules only to YouTube, not every subtitle player.

## Upload choice

https://support.google.com/youtube/answer/2734796?hl=en — official Help, no update date shown. Initial canonical fetch timed out; content loaded through https://support.google.com/youtube/answer/6054623?hl=en which redirected to the canonical article. Studio's upload route offers With timing / Without timing. Auto-sync requires the spoken language and transcript language to match; timing is set automatically. Use With timing for a supplied translated timed file. This supports workflow advice, not an account integration.

## WebVTT syntax

https://www.w3.org/TR/webvtt1/ — W3C Candidate Recommendation Draft dated 2026-05-20; work in progress, not a claim about YouTube's full implementation. UTF-8, WEBVTT header, cue blocks separated by blank lines, period milliseconds; timestamps use minutes/seconds or hours/minutes/seconds. Cue starts are nondecreasing; ends exceed starts; overlaps are permitted. Cue payload cannot contain the literal arrow substring. In §§4.1 and 4.2.2 raw payload arrows are prohibited; §6.4 decodes character references. Encode payload `-->` as `--&gt;`, literal `<` as `&lt;` and literal `&` as `&amp;`, preserving existing references and real tags. The timing arrow stays raw. This preserves displayed technical text. Preserve valid settings and identifiers. These rules explain file syntax; YouTube Help governs its narrower feature support.

## Supplied API errors, not Studio UI labels

https://developers.google.com/youtube/v3/docs/captions — official developer documentation, updated 2026-09-16 UTC. failureReason distinguishes processingFailed (processing failure), unknownFormat (not recognized) and unsupportedFormat (not supported). A processing failure does not identify encoding or a bad timecode as its cause. The page's old isAutoSynced example still mentions sync; the notice says sync was deprecated on 2024-03-13. Do not advise that deprecated API parameter. There is no API client in this package.

## Editorial decisions

Timing lock, cue preservation, glossary precedence, conflict handling and no invented meaning are authored workflow rules, not YouTube upload requirements. No fixed CPS, line-length, cue-duration or file-size threshold is asserted. Pasted text cannot establish original byte encoding or audio alignment. Unknown timing stays unresolved. Readability suggestions must not erase protected scope or technical meaning.
