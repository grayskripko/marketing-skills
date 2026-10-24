# Canvas grade rules — source register

All four URLs opened successfully on 2026-10-11 (read 2026-10-11). These are current official pages as observed, not a claim about 2026-10-17. No publication/update date was exposed in the retrieved article text. Refresh the deciding rules before submission and whenever a supplied preview conflicts. Scope: Canvas LMS instructor Gradebook CSV, not SIS imports or Learning Mastery.

## Import
https://community.instructure.com/en/kb/articles/660862-how-do-i-import-grades-in-the-gradebook

Sections: Notes, Create CSV File, Upload New Data, Save Changes. Supports the inline import decisions. Reopened and rechecked during repair on 2026-10-11. Complete/incomplete imports convert full/partial credit to complete and zero to incomplete; exports represent those outcomes as full/no credit. Reserved assignment-title phrases are Current Score, Current Points, Current Grade, Final Score, Final Points, Final Grade, Override Score, Override Grade, Override Status. Exact reserved column names: Student, ID, SIS User ID, SIS Login ID, Section, Integration ID, Root Account. Hidden/deleted custom columns are ignored. New-file order is Student Name, Student ID, optional SIS User ID and SIS Login ID when SIS is used, Section, assignments. Retain native export headers when editing an export. Discussion Checkpoints add overall, Reply to Topic and Replies Required columns; preserve distinct IDs rather than merging their titles. Classic Quiz grade edits may appear as fudge points. New assignments default to Assignments group, No submission, Everyone due-date scope.

## Export
https://community.instructure.com/en/kb/articles/660866-how-do-i-export-grades-in-the-gradebook

Sections: Notes, Export Scores, View Read-Only Columns. Supports inline coverage and points rules. Use Export Entire Gradebook when all periods are needed; Export Current Gradebook View can be filtered. CSV uses the latest submission. Current totals omit unsubmitted work; final totals count it as zero. Unposted variants include hidden grades. Posting policy is displayed but cannot be edited in CSV. Export files are also saved to the instructor's Unfiled user-files folder.

Final override conflict: this page says override grades appear when the feature is enabled and changes appear in import confirmation. The import page lists Override Score/Grade/Status among unrecognized assignment-name text. Ask for exact headers, feature setting and preview before classifying an override edit. Never treat an override column as an ordinary assignment.

## Gradebook History UI
https://community.instructure.com/en/kb/articles/660864-how-do-i-view-the-history-of-all-grading-changes-in-the-gradebook

Sections: opening Notes, View Gradebook History, View Filters. Read-only history covers the last 365 days and includes edits under manual posting policies. It shows before, after and current grades, date, grader and artifact. Filters include student, grader, artifact and dates; section-limited instructors see their own section. Anonymous grading omits student names; automatic quizzes can show Not Available for grader. Absence from a filtered history is not proof that a change never happened.

## Gradebook History data supplied by the user
https://developerdocs.instructure.com/services/canvas/resources/gradebook_history

Sections: SubmissionVersion and List uncollated submission versions. The version object includes user_id, assignment_id, previous_grade, new_grade and current_grade plus grading times. The feed omits previous_/new_ grade keys and uses grade instead; do not fabricate a pair from one feed item. This package reads supplied data only and makes no API call.

## Authored comparison conventions

ID-first joins, intended-change allowlists, preserving raw cells, separate corrected files and predicted/observed status labels are this plugin's rules of thumb. They do not claim Canvas enforces those audit conventions. Blank imports, EX acceptance, ambiguous student matching and novel error causes need actual preview or a refresh of the four allowlisted official sources; no acceptance behavior is asserted here.
