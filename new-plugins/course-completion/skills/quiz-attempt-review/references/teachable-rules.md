# Teachable source register

Verified live/read 2026-10-11. Scope: current public Teachable web-course documentation, not a promise about every mobile client. Dates below are the dates displayed by the articles. Reopen these official pages before submission around 2026-10-18 and update any changed rules. No future verification is claimed.

| Official source | Displayed date | Deciding sections |
|---|---|---|
| [Course Compliance](https://support.teachable.com/en/articles/11682463-course-compliance) | 2026-06-27 | Enforce lesson order; Enforce video watching; Enforce quiz completion; Reset Course Compliance; autoplay defaults. Numeric gates: 90% uploaded coverage, 99 maximum retakes, zero score floor means completed quiz. |
| [Add Lesson Content](https://support.teachable.com/en/articles/11682455-add-lesson-content) | 2025-11-26 | Video Upload versus Embed; Embed Media; Quizzes; Custom Code. Grading defaults and one-block limit. |
| [Student Progress Reports](https://support.teachable.com/en/articles/11682571-student-progress-reports) | 2025-10-22 | Lesson progress; Video heatmaps; View and reset quiz scores; Mark lessons as complete; Reset lesson or course progress. |
| [Course Reporting Tools](https://support.teachable.com/en/articles/11682570-course-reporting-tools) | 2026-01-22 | Export report data; Quiz Scores. Quiz export has Attempt, Submitted At, Question #, Quiz Score and Is Correct; these fields serve different purposes. |
| [Navigate and View Course Content](https://support.teachable.com/en/articles/11682425-navigate-and-view-course-content) | 2025-11-03 | Dripped and locked lessons; marking progress; adjusting video settings; playback troubleshooting. |

## Report interpretation
Heatmaps describe segments, not a single elapsed-time total. Green means viewed once, yellow twice, and orange/red three or more times. Separate watching sessions can produce separate heatmaps. The quiz-result detail highlights a learner's selected option in green. The two uses of green describe different things.

## Export field rules
Quiz Score is the quiz percentage; Is Correct is a question-level boolean. Attempt counts quiz-taking occurrences, not necessarily remaining retakes. Question # distinguishes questions within an attempt; several rows may describe one attempt. Group supplied learner/course/lesson and Attempt within known reset boundaries. Submitted At is an answer timestamp, not a required shared quiz-attempt timestamp; different question times do not mean different attempts. The documented Quiz Scores column list does not explicitly list a quiz ID; request an alias when identity is ambiguous. Lesson Completion uses Lecture ID, Lecture Order and Complete; the latter may reflect manual owner completion. Video Stats is not available as a CSV export. Aggregate Engagement is an average video-watching percentage, not an individual learner's coverage.

## Documentation conflict
The student navigation guide says to view the entire video for a locked lesson; the dedicated compliance article specifies 90%. Use the dedicated, newer compliance article for that numeric gate. The navigation/progress pages describe Complete and Continue as required while navigation also describes autocomplete. Diagnose against the learner's actual preference and observed lesson status; do not assert that automatic completion cannot happen.

## Diagnostic conventions
Merging overlapping watched intervals, preserving reset boundaries, requesting ambiguous attempt labels, and proposing the narrowest recovery are this plugin's rules of thumb, not additional Teachable settings. Supplied evidence is needed to establish any learner's actual state. The docs do not define how an ambiguous export counts initial attempts, aggregate all videos into one gate, or which result is active after a later conflicting attempt; do not fill those gaps with invented field rules.

## Access verification
All five listed official URLs loaded with the titles and deciding sections above on 2026-10-11.
