# Legal Citations

Compare a legal draft's citations, quotations and factual claims with source documents you supply.
For lawyers and legal teams preparing material for qualified lawyer review. Give it the draft and full opinions, statutes or record documents as pasted text or readable files. No accounts or paid APIs are required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

Both platform manifest directories contain metadata only. Supplied-file reading and page-image inspection use the assistant provider’s existing tools; calculations show formulas and supplied inputs without instructions to execute code.

## What it does

| Skill | Give it | You get |
|---|---|---|
| check-authority-identity | draft citations and supplied authorities | mismatched names, courts, dates, versions and missing sources |
| check-quotations-and-pincites | draft quotations and authority pages | exact wording differences and corrected page references |
| map-claims-to-record | draft facts and record documents | claim-to-passage map, contradictions and missing evidence |

## Citation scope

The implemented workflows compare citations, quotations and record claims with supplied sources. Jurisdiction/style-specific citation formatting and authority-list preparation are scope gaps recorded for follow-up. Current-law validation and treatment by later courts require authoritative research access; this package performs supplied-source comparison.

## Examples

- “Check these citations against the opinions I supplied. Is each citation for the right document?”
- “Verify the quoted words and page references. Keep printed pages separate from PDF pages.”
- “Check this motion against the appendix. Which factual claims lack support?”

A quotation saying “all applications” is flagged when the source says “some applications.” An invoice's due date does not establish when it was paid. A source that is missing is marked unresolved, rather than called false.

## How to use it

Supply documents you are authorized to process, with stable file or exhibit names. Include the court/jurisdiction, relevant date, and source version if known. Missing context is noted only when it affects a finding or how you can use the comparison. Preserve printed page labels. The assistant can read files directly when the host provides a reader. Scans need host OCR or readable page images. If a passage cannot be read, supply that page as clearer text or an image; other findings can still proceed. Paste text to start without setup.

Findings start with the discrepancy, source passage and proposed correction or missing item. Entries that match are listed only when you request a full inventory. If no discrepancy is found, you get a short result naming what was compared. Unnecessary personal details are redacted even in quoted passages. Printed/reporter pages, numbered paragraphs and file pages stay separate. Proposed edits do not alter originals.

## Review limits

The findings prepare material for a lawyer’s review in the stated jurisdiction. They do not provide legal representation or advice to file. Matching a supplied document does not prove that the document is authentic. A correct quotation can support a narrower claim, and a real case may no longer be valid law. Missing sources, incomplete excerpts and OCR errors can leave specific checks unresolved. The results do not promise complete research or a full check of the source’s status or how later authorities treat it. They do not approve a filing or certify legal accuracy. Have jurisdiction-specific conclusions reviewed by a qualified lawyer.

## Data and network

Network scope: none. No URLs, robots.txt, public cases or databases are fetched. No telemetry, account access, paid API, sending, publishing, filing or background monitoring. The package contains instructions and reference text; it runs no service and stores no documents itself. The chosen AI host processes supplied data under its own terms and may retain conversations or requested output files. Host file reading or OCR may require its own tools; model use may cost money.

Minimize personal data before supplying documents. Keep unrelated contact details and sensitive information out of shareable findings. Uploading a document does not create or guarantee privilege.

README.md and PRIVACY.md in this package contain the same documentation and privacy information as the manifest links.

## Support and license

Issues: https://github.com/grayskripko/marketing-skills/issues

MIT. See LICENSE.
