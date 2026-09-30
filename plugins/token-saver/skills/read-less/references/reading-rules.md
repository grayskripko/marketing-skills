# Reading rules

Five rules for gathering context in a coding session without filling it.

1. **Search before reading whole files.** Look for the exact name, message or string first. Open a file only where a hit points.
2. **Read ranges, not files.** Read the lines around a hit, then widen only if the answer is not there.
3. **Filter command output.** Show failures only, counts, or the last lines. A full test run or build log rarely needs to be in the conversation.
4. **Never paste whole logs back.** Quote the failing lines and the exact error text.
5. **Stop and ask before a large, speculative read.** If the next read is big and you are not sure it holds the answer, ask the user where to look.

## Cheapest source, by question type

| Question | Cheapest source |
|---|---|
| Where is X defined or used? | a search for the exact name |
| What does this function do? | the line range of that function |
| Why does this test fail? | the test output filtered to the failure and its stack lines |
| Which config value is used? | a search for the key, then the line range |
| Why was this built this way? | ask the user |
