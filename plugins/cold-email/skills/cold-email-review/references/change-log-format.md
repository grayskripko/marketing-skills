# Change log format

Print the change log before the clean text so the user can reject any single change.

| # | Rule | Before | After | Reason |
|---|---|---|---|---|
| 1 | CE-02 | Subject "Re: our chat" | Subject "Invoice matching at Acme" | First message; a reply prefix misstates the history |
| 2 | CE-06 | "Book a call, see the deck or start a trial" | "Worth a look? Yes or no is fine." | One ask the reader can answer in a word |

Rules:
- One row per change; cite the CE check or the wrong-practice id it fixes.
- "Before" and "After" quote the exact text; "—" means removed or added.
- A cut locked fact is logged with its F id in the Reason column.
- Merge fields such as `{{firstName}}` are never deleted silently: either keep them with a fallback noted, or log the cut.
