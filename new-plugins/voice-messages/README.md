# Voice Messages

Clean up voice notes and dictated transcripts and turn them into replies, emails, posts or interview answers without adding claims.
For people who speak their first draft and want readable text that still sounds like them.
Paste text or provide a TXT/SRT/VTT transcript export. You need no extra accounts, keys, paid APIs or transcription software to use these skills in your assistant. The skills do not transcribe audio.

## Skills

| Skill | Give it | You get |
|---|---|---|
| clean-voice-note | messy dictation or a transcript | complete readable text, not a summary |
| voice-note-to-message | dictated thoughts and a channel or recipient | a chat reply, email or post ready to paste |
| dictation-to-interview-answer | a career story and, optionally, the interview question | a clear answer that keeps what you did and the limits of your experience |

## Try it

- “Clean up my voice note: we tested only the draft. It might help; we have no results yet.”
- “Turn this dictation into a reply: the sample arrived. Can you ask whether the final version is ready?”
- “Make this interview answer readable: I wrote the checks. The team ran them in staging, not production.”

## Input and limits

Paste the words directly, or provide a text export your assistant can read. For SRT/VTT files, timestamps can be removed unless you need them. Keep speaker labels when they show who said what. An export cannot recover words the recorder missed. Names, numbers, technical terms and speaker changes may need your confirmation. Unclear meaning is marked, not guessed. Shortening must not silently drop facts. You can explicitly choose a narrower topic or facts to leave out.

For an audio recording, use an existing transcript in your assistant if available, or copy/export text from your recorder. For help exporting, provide the recorder name and the menu options you can see. The assistant uses those details without guessing the current menus. You can always paste a rough manual transcript instead. Review a recorder's own privacy and upload settings before using it; this package does not select or connect a transcription service.

## Data and network

These skills request no network access. They tell the assistant not to fetch URLs, search the web, access accounts or use extra services. The plugin has no network connection and collects no usage data. It contains instructions and reference text, with no executable scripts or service. It does not send, publish or store data itself. Your assistant processes the text and any supplied files under its own terms. Redact private contact details and unrelated personal information before sharing; private addresses and credentials are replaced with markers in the output.

## Support

https://github.com/grayskripko/marketing-skills/issues

## License

MIT. See LICENSE.
