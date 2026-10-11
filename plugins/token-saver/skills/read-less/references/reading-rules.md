# Reading rules

Five rules for gathering context in a coding session without filling it.

1. **Use the cheapest informative source.** Search first when an exact name, message or string is known. Without an anchor, inspect a bounded project index, overview or relevant test. Read whole small files when cheaper than fragmented reads.
2. **Read ranges, not files.** Read the lines around a hit, then widen only if the answer is not there.
3. **Filter command output.** Show failures only, counts, or the last lines. A full test run or build log rarely needs to be in the conversation.
4. **Never paste whole logs back.** Quote the failing lines and the exact error text.
5. **Bound speculative reads.** First inspect cheap likely sources. Ask the user when missing intent, unavailable evidence or a consequential ambiguity blocks safe progress; otherwise the agent performs a bounded evidence search and widens only for an unresolved question.

## Cheapest source, by question type

| Question | Cheapest source |
|---|---|
| Where is X defined or used? | a search for the exact name |
| What does this function do? | the line range of that function |
| Why does this test fail? | the test output filtered to the failure and its stack lines |
| Which config value is used? | a search for the key, then the line range |
| Why was this built this way? | relevant README, architecture decision record or supplied history; ask the user if evidence is missing |
