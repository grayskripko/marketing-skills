# Teachable scheduling source register

All pages below loaded and were read 2026-10-11. Dates shown by the pages are recorded separately. These are the live official texts checked for this build. Reopen these URLs during preparation for the planned 2026-10-20 submission and update this register if their rules change.

## Drip Content

URL: https://support.teachable.com/en/articles/11682465-drip-content
Page date: 2025-07-01. Scope: course sections, fixed-date and enrollment-relative drip.

Deciding facts: section-level release, midnight UTC; automatic announcements 15 hours later. Fixed dates require 48 hours' lead time. Announcements need activation 48 hours before release and a nonempty subject. Enrollment-relative drip uses first course enrollment. Full access stops announcements; restoring drip reuses the original anchor and resumes scheduled announcements. Disabling a section's drip opens it immediately and stops its announcements.

Evidence locations: Drip by date; Drip by days after enrollment; Set up email announcements; Grant students full access; Restore drip schedule; Turn off drip; FAQ release time and section granularity.

The page does not specify how enrollment timestamps close to UTC midnight become a date, whether a missed activation leads to a delayed send, or whether restoration resends past announcements. Keep those outcomes unresolved rather than inventing behavior. A UTC date derived from a UTC export is a stated calculation assumption unless the original course enrollment date is confirmed.

## Course Reporting Tools

URL: https://support.teachable.com/en/articles/11682570-course-reporting-tools
Page date: 2026-01-22. Scope: course Reports and Leaderboards CSV.

Leaderboards displays Enrollment Date as first course enrollment. Its export documents Enrollments Created At as UTC. Export CSV is available from the chosen report. Lecture Start Date and school sign-up are not documented as drip anchors. Identify user/course pairs and preserve field names; the export is not a record of drip settings.

Evidence locations: Leaderboards; Export report data, Leaderboards fields.

## Email Opt-in/Opt-out

URL: https://support.teachable.com/en/articles/11682447-email-opt-in-opt-out
Page date: 2025-07-14. Scope: school email preferences.

Email Opt Out=Yes and Unsubscribe from Marketing Emails=TRUE mean opted out. The explicit opt-out list names custom messages from Emails > Compose; it does not name drip announcements. Do not apply custom-message suppression to automatic drip without specific evidence. School-level notification controls are separate.

Evidence locations: Check student opt-in status; Which emails can users opt out of?

## Email Templates

URL: https://support.teachable.com/en/articles/11682446-email-templates
Page date: 2026-02-12. Scope: automatic templates.

The Drip Content Release template exists, and the page recommends editing drip messages within course Curriculum. Some student notifications have separate Emails > Settings controls. A generic template change is not proof of section announcement activation.

Evidence locations: Student emails, Drip Content Release; student notification controls.

## Python zoneinfo

URL: https://docs.python.org/3/library/zoneinfo.html
Page last updated: 2026-10-10 21:37 UTC. Scope: local calculation with IANA zone data.

ZoneInfo and datetime.astimezone use date-specific offsets; UTC conversion selects the correct side of a daylight-saving transition. Unknown zone keys or unavailable zone data raise ZoneInfoNotFoundError. Preserve UTC values and ask for a valid zone rather than inventing local times. No dependency download is part of the shipped workflow.

Evidence locations: Using ZoneInfo; Data sources; Exceptions and warnings.

## Calculation conventions

These are package calculation choices, not additional Teachable policies: derive release_date = confirmed original enrollment date + calendar day count; attach 00:00 UTC, then convert each event separately. For a UTC timestamp, derive its UTC date only with an explicit assumption if the date anchor is unconfirmed. Use release instant minus 48 hours as the conservative setup deadline. Exactly 48 hours meets the documented at-least-48-hour threshold. Arithmetic eligibility and successful account acceptance are separate facts; ask about acceptance only for requested, conflicting or unconfirmed settings, not merely for equality. Negative, fractional or blank counts are unresolved inputs, not invented vendor errors. Do not claim a maximum day count, guaranteed inbox delivery or historical catch-up sends.

## Fix verification — read 2026-10-11

Reopened all four official Teachable URLs above during bfix. Page dates remain as recorded. Drip by date requires at least 48 hours before date selection/save; Set up email announcements independently requires activation at least 48 hours before release. No equality exception is documented. An unsaved target cannot establish account acceptance. That last distinction is evidence handling, not a new vendor timing restriction.

The manual-remedy paths above are supported by Drip by date, Set up email announcements, Grant students full access, Restore drip schedule and Turn off drip. Choosing a later date is a workflow recommendation. Custom-message fallback opt-out scope is supported by Which emails can users opt out of? in Email Opt-in/Opt-out. Export-only mapping is supported by Leaderboards and Export report data in Course Reporting Tools.
