# Sources and editorial choices

Read 2026-10-09.

- [YouTube Help: View video transcripts](https://support.google.com/youtube/answer/15930243?hl=en). Captioned videos expose Show transcript in the description; transcript lines jump to their video position. Caption availability is not universal.
- [youtube-transcript-api maintainer documentation](https://github.com/jdepoix/youtube-transcript-api). Documents installation, list/fetch, snippet start/duration, languages, caption types and proxies. No API key is required. It describes cloud-IP blocking and warns that the community-supported interface can change. Proxy use is an optional choice, not the default here.
- [YouTube Data API: captions.download](https://developers.google.com/youtube/v3/docs/captions/download). Download requires authorization and permission to edit the video. An API key alone is not public-transcript access.

Editorial rules of thumb: search formulations follow the user's language and date scope; select by relevance rather than views; deduplicate by video ID; preserve excerpt boundaries; treat repeated appearances of one speaker as one perspective; do not invent timestamps or consensus; stop after an access block and switch to supplied text. These are this plugin's rules of thumb, not claims from a study or platform.
