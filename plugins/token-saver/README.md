# Token Saver Kit

## What it does

Five skills that lower token use in AI chat and coding sessions without dropping what matters.

## Skills

| Skill | Give it | You get |
|---|---|---|
| prompt-trim | an instruction file or system prompt | rule ledger, change table, trimmed text, check that every rule is present |
| context-diet | usage numbers, instruction files, tool list | load table, findings against 12 checks, top 5 changes |
| session-handoff | a long session or a pasted work state | a fixed-field note a fresh session can resume from |
| read-less | a coding task | a reading plan with the cheapest source for each question |
| terse-mode | "shorter answers, please" | short but safe answers: commands, numbers, warnings and confirmations stay, even when asked to drop them |

## Examples

1. Trim this instruction file, keep every rule: 'Always run tests. ALWAYS run tests before commit. Be nice. Use pnpm, never npm.'
2. My context report: instruction file 9k tokens, tool definitions 22k, chat history 140k. What should I cut first?
3. Handoff note: goal auth refactor; done token refresh; failing logout test '401 expected 200'; tried cookie domain fix, no luck.

## How it works

Each skill follows fixed steps and prints a fixed output. Nothing on the printed never-cut list is shortened.

## What to expect

Shorter replies trim explanation, not code. One published measurement found about 8.5% fewer output tokens and about 10% lower cost per task with no measurable quality change ([JetBrains, July 2026](https://blog.jetbrains.com/ai/2026/07/speak-to-ai-agents-like-cavemen-tosave-tokens/)). Larger savings usually come from short always-loaded instructions, starting fresh with a handoff note, and reading less. This plugin does not change how the host counts or limits usage.

## When not to use it

Learning a new topic, legal or medical text, answers you will forward.

## Data and network

Network scope: this plugin fetches nothing and sends nothing. It works only on text the user pastes or files the user names in the current workspace, and it runs nothing and changes no files or settings unless the user asks. If the assistant has a code tool, it may use it to count words.

## Troubleshooting

- Terse mode stopped: the host may have cleared or compacted the conversation. Ask again.
- A rule seems lost after trimming: check the "Rules present" line.

## Support

[GitHub Issues](https://github.com/grayskripko/marketing-skills/issues)

## License

MIT
