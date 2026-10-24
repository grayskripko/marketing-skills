# Google rubric rules: verified source register

All URLs below loaded with readable current official documentation on 2026-10-11 (read 2026-10-11). Rules are paraphrased. Check these pages again before the planned 2026-10-19 submission. No future verification is implied.

## Classroom interface and export provenance

URL: https://support.google.com/edu/classroom/answer/9335069?hl=en
Page: Create or reuse a rubric for an assignment. No publication/update date displayed.

Sections Create a rubric, Share rubrics with export and import, Edit an assignment's rubric: at most 50 criteria and 10 levels each; assignment title needed; scored levels sort by points. Standard Sheets import uses a Classroom-created export; editing that spreadsheet or changing its format breaks the supported path. Edit the imported rubric in Classroom instead. A failed save can be recovered by exporting/importing again. UI edit/delete stops after grading begins. Separate Convert from Drive functionality must not be confused with standard import. Reuse/import edits affect the new assignment, not the source. Export instructions contain no pre-grading restriction; the grading lock applies to editing/deleting. For destination-only recovery, export the original unchanged and edit the imported destination, including when the original is graded.

## API structure and eligibility

URL: https://developers.google.com/workspace/classroom/rubrics/limitations
Last updated 2026-09-03 UTC.

Sections Rubrics structure, Limitations during grading, Third-party coursework, License requirements: one rubric per coursework; at least one criterion/level; rubric-wide scored or unscored mode; unique numeric scores per criterion, decimals/zero accepted, null rejected; unscored points omitted. A sole zero-point level in a sole criterion is invalid. Criteria and levels have meaningful order. Only the creating Cloud project manages rubrics, excluding UI-created coursework. After grading, API text edits and within-criterion level reordering are allowed; points/structure changes are not. Stable API write eligibility requires Education Plus for requester and course owner. Preview V1_20260316_PREVIEW removes that license requirement for Education users; do not assume stable eligibility changed. API rubric grades on submissions are read-only, and teacher overrides are possible.

## Field schema

URL: https://developers.google.com/workspace/classroom/reference/rest/v1/courses.courseWork.rubrics
Last updated 2026-08-20 UTC.

Sections Rubric, Criterion, Level: criterion title/description and levels; level title/description and optional numeric points; an unscored level needs a title. Criterion/level IDs are assigned at creation. sourceSpreadsheetId is input-only/immutable in the resource schema and refers to formatted rubric settings; its use requires Sheets read or write scope. Preview learningGoal must already be attached to the assignment; preserve supplied links, do not add guessed goals. Do not invent character limits absent from this schema.

## Patch semantics and error meanings

URL: https://developers.google.com/workspace/classroom/reference/rest/v1/courses.courseWork.rubrics/patch
Last updated 2026-06-10 UTC.

Sections error codes, updateMask: mask is necessary despite the parameter's Optional label; use updateMask=criteria for criteria replacement. previewVersion must be set to access preview capabilities. criteria and sourceSpreadsheetId are alternative rubric-definition sources. criteria replacement deletes omitted items; retained IDs preserve existing identity. INVALID_ARGUMENT includes RubricCriteriaInvalidFormat. PERMISSION_DENIED includes project mismatch, modification/access failure or grading started. NOT_FOUND includes missing resources or inaccessible coursework. INTERNAL is also documented when grading has started. Do not map every server error to a retry. The patch method permits sourceSpreadsheetId in its mask even though the resource schema calls it immutable; use method-specific documentation for a supplied patch draft.

## Additional official error reference

URL: https://developers.google.com/workspace/classroom/troubleshooting/common-errors
Loaded through official redirect from https://developers.google.com/workspace/classroom/reference/Request.Errors on 2026-10-11. Publication date not captured.

General error meanings depend on method and state. FAILED_PRECONDITION may represent a limit or a state such as CourseNotModifiable. For rubric patch diagnosis, prefer the patch method's specific list rather than inferring a cause from HTTP status alone.

## Local workflow choices

Preserving supplied exports unchanged, returning manual Classroom edits, and asking for a disputed score rather than inventing it are authored workflow choices. Total available points = sum of criterion maxima follows the distinction between level, criterion and rubric totals; do not sum every possible level. The official schema is not a published spreadsheet cell template.

## Fix verification — read 2026-10-11

The builder reopened all five official pages during bfix-classroom-rubrics. The limitations license section, patch query parameters and Help import/edit/export sections directly support the revised inline decisions. Displayed developer update dates remain as listed above; Help displays no update date.
