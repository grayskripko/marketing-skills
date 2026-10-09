# Content checks (pre-send)

Status per row: PASS, FIX or ASK. Evidence is a quote from the email or the row.

| Id | Check | FIX when |
|---|---|---|
| CC-01 | Merge fields | A malformed field (`[[…]]`, `%…%`, `{…}` mixed with `{{…}}`), or a supplied row that leaves a field empty with no fallback. With no rows, or all rows filled: PASS with the note "add a fallback before using more rows" |
| CC-02 | Past contact | Phrases such as "as discussed", "following our call", "great meeting you" that the user has not confirmed |
| CC-03 | Proof | A superlative that can have no source ("leading", "#1"). A number or customer reference with no source in the user's material is ASK: ask where it comes from; no marker in the email |
| CC-04 | One ask | More than one ask, or none |
| CC-05 | First-email weight | More than one link, any image or attachment, or a calendar link plus a deck |
| CC-06 | Subject honesty | "Re:"/"Fwd:" on a first message, or a subject that misstates the body |
| CC-07 | Urgency | A deadline, discount or limited stock that the user has not confirmed as real |
| CC-08 | Stock phrasing | Three or more patterns from `stock-phrasing-cold.md` (one or two: PASS with a note) |
| CC-09 | Sender identity | No real sender name and company, and no footer slot for them (ground rule 8) |
| CC-10 | Opt-out line | Missing, hidden or phrased so the reader cannot easily act on it |

ASK is used when the answer depends on something only the user knows, for example whether a meeting really happened.

Fact lock for fixes: when the check rewrites text to clear FIX rows, numbers, names, dates and product claims are copied unchanged, never altered or added; the user's own numbers stay as given, with no marker (same rules as the review skill). Merge fields stay, with a fallback. A per-row claim the check cannot verify becomes an ASK row, not a deletion. A fix never introduces a stock pattern such as a sender-first opener. A few plain lines on what changed follow the fixed text. Ids are never shown to the user.
