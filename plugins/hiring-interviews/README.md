# Build hiring interview kits and match interview notes to approved role requirements

Show the source for each point and where evidence is missing.
For hiring managers and HR panels. For a role map or kit, supply an approved role brief or job description and any available employer rubric: the criteria and rating definitions interviewers use. Add panel constraints for a kit. For a debrief, supply the approved rubric and notes you are allowed to share, with unnecessary personal details removed. No applicant tracking system (ATS) accounts or paid APIs are required. Use an AI host that can read the supplied material.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

## Skills

| Skill | What you get | Example request |
|---|---|---|
| `map-role-requirements` | Must-haves and preferences, their sources, matching rubric items and conflicts | “Separate must-haves from preferences in this approved role brief.” |
| `build-structured-interview` | Questions tied to the role, follow-ups, panel owners, timing and approved answer anchors (what interviewers should listen for) | “Build a panel interview from these requirements and our rubric.” |
| `prepare-interview-debrief` | Observations with sources, human ratings with who gave them, disagreements and missing evidence | “Map these notes to our rubric and show what was not assessed.” |

Paste text you are allowed to share or provide readable files/exports with source labels. For scans, the AI app must be able to extract text from images. A person must check uncertain passages. A missing rubric does not block a requirement map or question draft. A common rubric can apply to every criterion without additional answer anchors. Candidate ratings remain for people to enter. No live ATS connection is provided.

For employer-side hiring preparation. Applicant coaching, resumes and customer research interviews are outside this package.

Humans apply ratings, approve accommodations and make hiring decisions. Missing evidence is not failure. Routine preparation does not require an HR-review notice or jurisdiction field. Specific problematic criteria, adjustments or legal issues may need review. Debriefs compare recorded evidence with rubric definitions without assigning candidate scores. No candidate rankings, recommendations to hire or reject anyone, guesses about personal traits or certification of legal compliance.

## Data and network

Fetches: none. Uses only the material supplied for the task. The package collects no usage data, runs no service and requires no additional accounts. It does not send, publish, change ATS records or monitor activity in the background. The AI host processes conversations and files under its own terms; these instructions do not make processing local or anonymous. Minimize records and use candidate IDs. See [PRIVACY.md](PRIVACY.md).

## Package

These skills provide instructions for compatible Claude and Codex apps. Both manifests and a local icon are included. The `.claude-plugin/` and `.codex-plugin/` directories contain platform metadata, not executable runtimes or servers. Licensed under [MIT](LICENSE).
