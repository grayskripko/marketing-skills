# YouTube Captions

Fix my translated YouTube captions while keeping my timestamps and technical terms. Return a repaired draft and flag upload blockers.

For creators and subtitle editors preparing translated YouTube caption files. Needs pasted SRT, SBV or WebVTT text, an export, or screenshot details you describe; a glossary and source captions help resolve meaning. No account, key, install or paid service is needed for draft repair.

## What this package runs and connects to

This is a skills-only package: Markdown instructions and reference text, JSON platform metadata, and a static SVG icon. It bundles no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. The `.claude-plugin` and `.codex-plugin` manifests describe the same skills for their respective hosts; neither supplies a runtime or connector. Installing the package does not run a program or connect an account. The current folder also contains development notes, evaluation records and a test screenshot; these are not runtime components and should be kept outside the submitted release folder.

Routine caption repair and terminology review use only text, attachments, selected local exports and screenshot details you explicitly supply. The skills do not instruct code execution, software installation, API calls, account access, message delivery or publishing. They can return a draft as an artifact or code block; any output file you explicitly request is created by your assistant's existing file tools at your chosen destination, not by a bundled program.

This is not a strictly offline workflow: both skills allow the assistant, only on an explicit rules-refresh request, to retrieve the official reference pages using its existing web tools, including redirects:

- `https://support.google.com/youtube/answer/2734698?hl=en` — caption formats.
- `https://support.google.com/youtube/answer/2734796?hl=en` and `https://support.google.com/youtube/answer/6054623?hl=en` — upload guidance and its documented redirect.
- `https://www.w3.org/TR/webvtt1/` — timed-text syntax.
- `https://developers.google.com/youtube/v3/docs/captions` — documentation for interpreting supplied API status exports; no API is called.

These requests disclose the requested URL and ordinary connection metadata to the contacted sites and the assistant's tool provider, including any redirect destination. Caption text and glossary content are not submitted to those sites. If retrieval is unavailable, supply the relevant rules as text. The skills also give optional instructions for you to save a UTF-8 draft and upload it yourself through YouTube Studio → Subtitles → video → Add language → Add → Upload file → With timing; they do not perform that upload or connect to your account.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain conversations, attachments and tool activity under its own terms. See [PRIVACY.md](PRIVACY.md).

- **Repair caption file:** returns a repaired timed-text draft and a terminology review. Keeps timing values, cue boundaries and protected terms. Flags defects that require a timing change.
- **Review caption terminology:** checks supplied source/translation pairs and glossary entries, returning a reviewed draft and cue-level decisions. Does not guess missing source meanings.

Basic SRT, SBV and WebVTT are the repair formats. Other supported YouTube formats receive format advice and an export request, rather than an untested rewrite of binary or frame-based captions. A screenshot description supports review of the described part; exact file repair needs complete text and timecodes.

Save the draft in the stated format and encoding. The agent can walk you through YouTube Studio → Subtitles → video → Add language → Add → Upload file → With timing. YouTube access is needed only for your own upload. Auto-sync can replace timing and is unsuitable for this locked-timing job.
