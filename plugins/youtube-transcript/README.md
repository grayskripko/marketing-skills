# YouTube Transcript

Summarize YouTube video transcripts, pull key takeaways, answer questions with timestamps, or compare transcripts. Pasted captions work without setup.

For researchers and teams who need to see which passage supports an answer.
Use pasted captions, exports or public video links. Finding public videos needs the assistant's existing browsing. Pasted text needs no account, paid API or installation.

## Skills

| Skill | Give it | You get |
|---|---|---|
| youtube-find-videos | question, optional language and date window | short list with checked links or supplied labels, and supporting caption passages when available when available |
| youtube-summary-questions | question and one transcript or public link | summary, takeaways or answers with times or paragraph references |
| youtube-compare-transcripts | question and several transcripts or links | comparison showing agreements, differences and missing text |

## Try it

- “Summarize these pasted captions and list key takeaways.”
- “Find Spanish talks about warehouse inventory accuracy.”
- “What does this excerpt recommend? [02:10] Check the bin label before picking.”
- “Compare these two caption exports on when manual counts are still needed.”

## No setup

Paste text or attach TXT, SRT, VTT or JSON captions. Include a video link if you want clickable timestamps. On a captioned public video, open the description and choose Show transcript. An agent with public browsing can attempt access itself. When access fails, it can still analyze your pasted text. Text without times gets paragraph citations. Times are never guessed.

## Optional direct retrieval

Ask the agent to help retrieve public captions with Python. It can check Python, create a project-local virtual environment, install `youtube-transcript-api` from PyPI, and fetch one chosen caption track following its [maintainer documentation](https://github.com/jdepoix/youtube-transcript-api). It needs no API key. It uses a community-supported interface. Cloud IPs may be blocked, and platform changes can break it. Caption quality varies; translated or automatic text can alter meaning.

A proxy is optional only if you choose it. It can cost money and receives connection metadata and video requests. Configure its credentials locally, never in chat. It does not guarantee access or authorize bypassing restrictions. You can paste captions instead, with no setup. The official caption-download API needs authorization and video-edit permission; an API key does not unlock other people's caption tracks.

## Data and network

Pasted-text work makes no requests. Public research sends topic queries to the assistant's search provider. It fetches selected public YouTube watch pages, channel details needed to name sources, caption-track lists and caption text on YouTube/Google video hosts. It also fetches relevant robots.txt. Only user-linked or search-selected videos are fetched. No arbitrary linked sites, comments, login, audio/video downloads, telemetry, paid transcript services or extra model APIs. Explicit setup work may fetch PyPI package metadata, distributions and required dependencies and the linked package or platform documentation. An optional user-selected proxy routes video requests through that provider. Direct page fetching respects robots.txt.

This package is instructions and reference text, with no service or bundled executable. It stores nothing itself. The assistant and optional tools process material under their own terms; files saved by a user-authorized tool remain until deleted. Redact personal contact details before pasting. See PRIVACY.md.

## Limits

Search returns a selected set of videos. It does not find every relevant video. A title can suggest relevance but cannot prove what was said. The answer names missing captions and blocked pages, and says which parts an excerpt covers. Captions do not show visuals or independently prove a speaker's claim. This package does not publish, send, operate accounts or plan channel growth.

## Support and license

https://github.com/grayskripko/marketing-skills/issues

MIT. See LICENSE.

The manifest documentation and privacy URLs are intended publication locations and currently return 404; use the bundled README.md and PRIVACY.md until those files are published.
