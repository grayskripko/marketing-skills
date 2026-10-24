# CSV Cleanup

Clean and merge Excel and CSV exports while keeping originals and tracing output rows to their sources.
For people who clean exports repeatedly and need a file they can review. Supply CSV/XLSX files you are authorized to use, or paste rows. Explain what each row represents, such as one order or one payment. Provide any agreed rules for interpreting dates, identifying duplicates and matching records.

| Skill | Give it | You get |
|---|---|---|
| inspect-export | unfamiliar files or rows | list of files and columns, import issues and proposed column mappings |
| clean-and-merge | files and approved cleanup rules | new cleaned copy, source-row references, issue list and saved cleanup steps |
| review-exceptions | flagged rows and supporting facts | decision table showing which rows each approval covers |
| repeat-cleanup | saved cleanup steps and next export | fresh copies, changed sheets or columns and new issues |

## Examples

- “Check these exports before combining them. Keep IDs as text.”
- “Stack these monthly files; keep repeated transactions unless the full row matches.”
- “Reuse this recipe on the next export and flag changed columns.”

## How it works

Originals stay unchanged. Each output row has references to the source records it came from. Unclear dates, possible duplicates and unmatched keys stay visible. Similar names are never silently merged. Cleaned records do not prove the underlying records are true or provide accounting conclusions.

The package contains instructions and reference text. Creating files requires the assistant’s local file and code tools. Python’s built-in CSV reader supports CSV work. XLSX work needs a local workbook reader/writer; openpyxl is one free option. If a required tool is missing, the assistant can guide setup where permitted. Small pasted tables offer a no-install route to a cleaned text table and proposed cleanup recipe. A text answer is not a downloadable workbook.

Text that looks like a formula stays text. For spreadsheet viewing, prefer XLSX with cells explicitly stored as text. CSV protection depends on the application that opens or imports the file. Protection can change values, and quotes alone are insufficient. A generated workbook must be reopened and checked. Checking appearance or how formulas behave requires the intended viewer. Reading the file with a parser does not prove those checks passed.

## Data and network

Network scope: none. No URLs are fetched. No telemetry, connector, accounts or paid APIs are required. The host processes your supplied files under its own terms and may charge for model use. Local tools create requested output copies and supporting files in your workspace. There is no background refresh or live account editing. Minimize personal data before uploading. Share a reduced cleaned copy, and keep originals and detailed logs in a location with restricted access.

## Support and license

Issues: https://github.com/grayskripko/marketing-skills/issues

MIT. See LICENSE.
