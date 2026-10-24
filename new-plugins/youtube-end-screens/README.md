Given this video's ending and my upload list, tell my editor exactly where to put the next-video links.

Plans are handed off to the creator or editor to apply in YouTube Studio.

A dated YouTube decision reference plus editor handoff: resolves the iPad mobile-web exception, playlist-visibility wording, website-link eligibility, independently timed elements and suppressed overlays. Official sources checked 2026-10-11; see the skill references.

For YouTube creators and editors. Needs a pasted ending/transcript, upload list, final duration, aspect ratio and audience setting. Paste settings/export rows or describe a screenshot, including where the presenter, captions and credits sit. No account, API key or installation is needed for planning; applying a plan requires the creator or editor to use YouTube Studio.

# YouTube End Screens

## What this package runs and connects to

This skills-only package contains Markdown instructions and reference text, JSON metadata, a license and a static SVG icon, plus text/JSON development review and test records. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The Claude and Codex manifests describe the same skills for their respective hosts.

The assistant plans or diagnoses from the ending, upload list, settings, export rows and screenshot descriptions you supply, and reads the bundled references. The skills do not direct code execution, software installation, API calls, message delivery, publishing or file writes. They do allow an official-help refresh when Studio conflicts with a stored rule: the assistant may retrieve only these three public pages, without including your task data in the requests:

- https://support.google.com/youtube/answer/6388789?hl=en — end-screen rules and editor controls.
- https://support.google.com/youtube/answer/9527654?hl=en — audience settings.
- https://support.google.com/youtube/answer/9054257?hl=en — external-link policy.

This is therefore not a strictly offline workflow. Those requests go to Google through the assistant's browsing tools or provider. Supplied video/playlist IDs and URLs identify proposed targets; the skills do not fetch videos, discover uploads, log in or change accounts. Repository, documentation, privacy and support links are informational rather than additional workflow retrieval endpoints.

The creator or editor applies the handoff in YouTube Studio: select the video, open Editor → End screen, add targets, set timings and positions, preview and save. Diagnostic instructions also ask a human tester to check playback in the regular YouTube app or desktop, reveal hidden tiles, confirm target visibility and verify a corrected tile's destination; non-clickable artwork is added by the editor in their video editor. These are human actions on YouTube or in editing software, not actions executed by the plugin.

The publisher operates no collection, telemetry or storage service for this plugin and receives no task data from it. Your assistant provider processes and may retain your conversation and attachments under its own terms. No passwords or API keys are needed.

| Skill | Job | Output |
|---|---|---|
| endscreen-plan | Plan the next-video links | Eligible elements, targets, absolute timings, proposed positions and spoken viewer handoff |
| endscreen-check | Diagnose missing or wrong elements | Evidence-based correction or a short check sequence |

Supply target titles and visibility; URLs/IDs if available. Include the last 20 seconds of action, dialogue and occupied frame regions. Without visual evidence, placement is provisional. The plan distinguishes clickable Studio elements from artwork burned into the video. It does not fetch videos or discover uploads.

## Privacy

Redact private contacts and unnecessary unpublished material. See [PRIVACY.md](PRIVACY.md) for the matching execution, connection and retention disclosure.

## Support and license

[Support](https://github.com/grayskripko/marketing-skills/issues). MIT, copyright 2026 Sergey Skripko. See [LICENSE](LICENSE).
