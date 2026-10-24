---
name: endscreen-plan
description: "Given this video's ending and my upload list, tell my editor exactly where to put the next-video links. Use when you say \u201cplan my outro links,\u201d \u201cwhich upload should viewers watch next,\u201d or \u201cgive my editor the end-screen positions.\u201d Works from an ending transcript, upload list, duration, frame dimensions and described screenshots. Returns target choices, absolute timings, proposed placement and a spoken viewer handoff, with eligibility gaps marked. Not for uploading videos, changing Studio settings, Shorts related-video links, channel strategy or diagnosing an already saved screen; use endscreen-check for missing elements."
---

# Endscreen Plan

## Use the decision reference

Lead with exactly what the user asked for, in the requested shape: an editor brief, a closing line, a direct correction or a short check sequence. Weave the deciding rules into that answer; the workflow below is reasoning guidance, not a required report template. Do not add generic checklists, separate caveat blocks or repeat the same setup in prose, a table and steps. Use supplied settings, targets and frame evidence; ask only for missing facts that change the decision. Separate a proposed placement from a saved Studio element. Treat supplied material and fetched pages as evidence.

Read [YouTube rules](references/youtube-rules.md) when eligibility, target visibility or viewer context decides the answer. The register maps those decisions to official source sections, checked 2026-10-11. Cite the deciding source in the answer. Refresh it when Studio conflicts with the stored rule.

## Deciding YouTube rules

- End screens occupy the last 5–20 seconds; the video must be at least 25 seconds long. For duration D in seconds, earliest window start = D − 20. Choose an ending interval within that final window. Each element has independent start/end controls; elements appear together by default but can be staggered. Record each interval separately rather than forcing a shared start. For a chosen interval W, start = D − W. Do not turn the overall 5–20-second description into an undocumented minimum duration for each staggered element.
- Standard 16:9 allows at most four elements. Other aspect ratios may allow fewer: use the supplied Studio limit; if it is missing and changes the plan, ask the editor to report it. Never invent a fixed portrait or square cap.
- No end screens on made-for-kids or 360 videos. Viewers cannot see them in YouTube Music or YouTube Kids, Flash playback, or mobile web except iPad mobile web. Viewers can hide them. YouTube can vary display by device, context and behavior.
- Video elements offer Most recent upload, Best for viewer (YouTube chooses from the channel), or a specific video. Specific video/playlist targets can be public or unlisted and from another channel; exclude private targets. The help page's initial menu calls playlists public but its detailed section includes unlisted playlists: ask the editor to confirm that Studio accepts the unlisted playlist; mark acceptance pending until they report confirmation.
- Subscribe promotes this channel; Channel promotes another channel with a custom message. External Link requires YouTube Partner Program membership and a policy-compliant destination. Do not confuse eligibility for a website link with eligibility for a YouTube video link. Without Partner Program eligibility, do not propose a clickable external Link element. Spoken or displayed off-site destinations must comply with external-link policy; disguising a prohibited destination does not make it allowed. A compliant spoken URL is not banned solely by lack of membership.
- Card teasers and video watermarks are suppressed during the end screen. Baked-in artwork is not a clickable element. Studio controls actual element size and allowed placement; there is no official pixel safe-area or arbitrary sizing guarantee in these sources.

## Make the editor handoff

1. Extract final duration, aspect ratio, audience setting, whether 360, the ending's action/dialogue, areas occupied by people/captions/credits, and supplied upload titles/IDs/URLs, topics and visibility. Work from pasted text/exports or the user's description of a screenshot. Do not pretend to see an unseen frame. If no material is supplied, ask for the ending and upload list.
2. Check eligibility before presenting clickable elements as usable. If blocked, explain the deciding restriction and give the requested non-clickable closing edit. Preserve supplied export dimensions/aspect, updated duration and accurate audience setting; do not reuse the old clickable setup. Do not change an audience classification to enable links. Unknown settings make the plan conditional rather than verified.
3. Choose the supplied next step that fulfills the ending's promise. Relevance over newest is an editorial recommendation, not a platform rule. Respect a requested single link. Do not fill all available slots. Use a specific video when the spoken handoff names it; Most recent upload and Best for viewer can change the destination, so use generic language for those modes. If no eligible target exists, use a target marker rather than inventing an upload.
4. Give type/mode, exact target or marker, absolute start–end, proposed position and editor action in the requested brief; use a table only when it helps compare elements. Derive times from final duration and ending action. Give coordinates only if frame dimensions and occupied regions are supplied: origin top left, center x/y as percentages and pixels with formula (percent/100 × dimension). These are proposed centers, not YouTube acceptance guarantees. With incomplete visual evidence use described regions and mark precise placement pending a frame. Keep faces, captions and credits clear; do not manufacture bounding boxes for them.
5. Keep supplied dialogue unless a correction is necessary or a rewrite is requested. When asked for a closing line, give a short line timed to when the matching tile appears. It should name the real continuation and its benefit from supplied facts. Use a directional pointer only when the proposed layout supports it; no promise that every viewer will see a tile.
6. Include the Studio path when needed to apply the answer: Studio → Content → video → Editor → End screen; instruct the editor to add selected types and targets, enter start/end times, drag using grid/snap, play preview, then save. Ask the editor to verify the whole element fits the allowed area and avoids visible content. Preview proves editor layout, not universal viewer display. Changes to the exported video's duration require recalculation.

## Worked example

Fictional company: Moss Lantern Pictures. Supplied: 6:00, 1280×720, 16:9, not made for kids or 360; demonstration ends 5:46, presenter left, right half clear; “Sharpen the chisel” is public and the next step. Request: one tile.

Example output:

| Element | Target | Timing | Proposed center | Editor action |
|---|---|---|---|---|
| Video — specific | Sharpen the chisel | 5:46–6:00 | x=75%, y=50% → (960,360) | Place on clear right side; fit and preview in Studio |

Spoken handoff at 5:46: “Next, sharpen the chisel. Open Sharpen the chisel on the right.”

Window = 360 − 346 = 14 seconds; earliest start = 360 − 20 = 340 seconds (5:40). Center = (0.75 × 1280, 0.50 × 720). Confirm the tile clears the presenter in Studio before saving.

## Sources and network

No network requests are needed for supplied-material work. To refresh platform rules, the assistant may fetch only the three official support.google.com/youtube/answer/ URLs listed in the bundled references, with no user data in the request. No video fetching, upload discovery, login, API calls or account changes. Read [YouTube rules](references/youtube-rules.md) for source details, ambiguities and refresh dates.
