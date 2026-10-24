# Podcast Transcripts

Check podcast transcripts and upload settings for Apple Podcasts and Spotify. Get route, display, file and timestamp corrections from supplied settings and exports.
For podcast creators, editors and producers preparing episodes for publication.
Supply settings and warning text to troubleshoot a missing transcript. Supply transcript text or a VTT/SRT file when you want file corrections. This package checks transcripts; audio transcription is outside its scope. No account or API key is needed for these checks.

## Skills

- **transcript-route** — Choose the ingestion route and resolve eligibility, display and overwrite settings.
- **transcript-preflight** — Check supplied VTT/SRT content and return file, timestamp and coverage corrections.

For a combined request, get the relevant route and file corrections together in the format you ask for. Paste the host, target platforms, public RSS or subscriber route, episode language, duration, transcript settings, file size and any warning. Supply whatever you have; missing details appear beside the finding they control.

Example request: “Can Apple and Spotify ingest this VTT? Here are the file, RSS fragment, transcript settings and export size.”

The output identifies the route, applicable eligibility, observed defects and exact next corrections. Timing alignment needs evidence from the matching audio version. A pasted excerpt establishes only what that excerpt contains.

## Data and network

The skills read text you paste and local exports you select. Runtime network fetches: none. Official source summaries are bundled with dates and URLs in each skill's references. No telemetry, credentials, account reads or platform writes. The hosting assistant processes your supplied material under its own data settings. See [PRIVACY.md](PRIVACY.md).

Version 0.1.0. MIT license.
