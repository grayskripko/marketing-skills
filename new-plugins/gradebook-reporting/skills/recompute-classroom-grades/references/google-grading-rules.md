# Google Classroom grading source register

These eight official pages were checked without login on 2026-10-11. Help pages display no absolute update date.

| Source and URL | Scope and deciding facts |
|---|---|
| [Set up grading](https://support.google.com/edu/classroom/answer/9184995?hl=en) | Teacher settings: points, weighted categories, excused exclusion and weights totaling 100%. The weighted example uses equal maximum points; it does not settle unequal-point averaging. |
| [View or update your gradebook](https://support.google.com/edu/classroom/answer/9199710?hl=en) | Teacher Grades page: entered grades remain drafts until returned; unenrollment removes grades. |
| [Grade and return an assignment](https://support.google.com/edu/classroom/answer/6020294?hl=en) | Computer downloads: one-assignment CSV, all-class CSV, or all grades copied to Sheets. Returned ungraded work shows Done, not a numeric score. Grade history is available for turned-in and graded work. |
| [Create or edit grading periods](https://support.google.com/edu/classroom/answer/13138449?hl=en) | Education Plus / Teaching and Learning Upgrade. Automatic placement uses due date, or publish date only when no due date is set; preserve explicit individual placement. Names unique, dates nonoverlapping. Due dates outside the selected period can cause SIS export errors. |
| [Grades concepts](https://developers.google.com/workspace/classroom/guides/key-concepts/grades) | Updated 2026-09-03 UTC. API missing-work draft defaults to zero but is configurable; complete clears it. API cannot distinctly identify complete/missing/excused. Categories absent from coursework trigger weight normalization. Ungraded maxPoints is zero or absent. |
| [StudentSubmissions resource](https://developers.google.com/workspace/classroom/reference/rest/v1/courses.courseWork.studentSubmissions) | Updated 2026-06-10 UTC. API export fields: absent grade is unset, not zero. draftGrade is pending; assignedGrade is assigned. Grades nonnegative, rounded to two decimal places. submissionHistory tracks changes including maximum points. |
| [Course resource](https://developers.google.com/workspace/classroom/reference/rest/v1/courses) | Read 2026-10-11. gradebookSettings separates calculationType from displaySetting; hiding a grade does not establish a zero score. |
| [CourseWork resource](https://developers.google.com/workspace/classroom/reference/rest/v1/courses.courseWork) | Read 2026-10-11. gradingPeriodId records membership, including no association; assignment at creation uses dueDate or scheduledTime. assigneeMode and individualStudentsOptions identify individual assignment scope. |

## Boundaries that change the calculation

API fields describe API-shaped supplied exports, not guaranteed native CSV columns. Use a separate teacher-provided state table when excused states are absent. The missing-work default does not authorize turning a blank CSV cell into zero.

Normalization example derived from the Grades concepts rule: absent category weight 10%; active weights 20% and 70%; active weight sum=90%; adjusted percentage weights=100*20/90 and 100*70/90; equivalent contribution fractions are 20/90 and 70/90. Do not extend absence-of-coursework behavior automatically to a learner whose entire category is excused or ungraded.

Reconciliation conventions (local workflow choices, not platform rules): for overall percentages, subtract reported from recomputed in percentage points. For raw scores, use points; convert each score using its own supplied maximum before comparing percentages; retain raw precision until display; use source row keys and aliases; keep hypotheses separate from verified causes; use two scenarios where the category-average definition is not established. No documented overall-display rounding rule or general unequal-point category formula was found in these sources. A matching number alone does not identify the cause.
