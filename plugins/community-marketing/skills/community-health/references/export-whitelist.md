# Export column whitelist

The skill reads only these columns. Any other column is ignored, named once in the gate ("ignored: message_text, email"), and the user is asked to leave it out next time.

| Column | Meaning |
|---|---|
| member_id | a pseudonymous id; handles are replaced with M1, M2 ... in every output |
| join_date | date the member joined |
| post_id | id of the post or message |
| thread_id | id of the thread or channel conversation |
| created_at | timestamp of the post, with time zone if known |
| reply_to | post_id this post answers; empty for a thread starter |
| is_question | 1 if a thread starter asks for help (the user's own rule if the column is missing) |
| is_staff | 1 if written by staff, moderators acting for the company, or contractors |
| is_bot | 1 if written by a bot, integration or automated reply |

Counts instead of rows are fine ("300 questions, 48 unanswered").

Tell the user, once per answer:
- remove message text, display names, emails, IP addresses and avatars before pasting;
- use the platform's own admin export or analytics, never user-token or self-bot exporters (P-DSC14);
- the community owner decides whether members' data may be used this way (D-OWNER).
