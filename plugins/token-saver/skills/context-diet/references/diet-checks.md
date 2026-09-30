# Diet checks

Twelve checks for what a chat or coding setup sends with every request. The mechanism behind each is stated in the host documentation named in `host-commands.md`; the plugin does not add numbers of its own.

| Id | Check | Applies when | Why it costs | Typical change |
|---|---|---|---|---|
| DC-01 | Long always-loaded instruction file | an instruction file loads at session start and is long | it travels with every request | keep essentials only; the host's own guidance on length is in `host-commands.md` |
| DC-02 | Workflow-specific instructions loaded always | the file holds steps for one workflow (reviews, migrations, releases) | paid even during unrelated work | move them into an on-demand skill or a separate file read when needed |
| DC-03 | Rules duplicated | the same rule appears twice within one loaded file or across loaded files | paid twice | keep one copy |
| DC-04 | Tool definitions the user does not use here | the user marks enabled tools, servers or plugins as unused in this workflow | their listings load with requests | the user decides whether to turn them off for this workflow |
| DC-05 | Verbose tool output in the main conversation | test runs, logs or large listings land in the conversation | every later request carries them | filter output to failures or counts; hand bulky work to a helper where the host offers one |
| DC-06 | No clearing between unrelated tasks | one session covers several unrelated tasks | old context rides along with every new request | clear or start fresh between tasks; use a handoff note when continuity matters |
| DC-07 | Resuming after long breaks | the user returns to a long session after a break longer than the host's cache lifetime | the first request reprocesses the whole context | hand off to a fresh session before the break |
| DC-08 | Compaction where a fresh start fits | the user compacts often although the next task is unrelated | compaction reads the whole conversation it summarizes | start fresh with a handoff note instead |
| DC-09 | Model or effort heavier than the task | a large model or high effort is used for simple edits or lookups | reasoning is billed as output | the user picks a lighter model or effort for simple steps |
| DC-10 | Scheduled or recurring tasks on a long session | a recurring task fires inside a long session | each run sends the full context | run recurring tasks from a short, dedicated session |
| DC-11 | Large pasted logs or documents | whole logs or documents are pasted into the chat | they stay in history | paste the failing lines or the relevant section |
| DC-12 | Images kept in history | screenshots stay in a long session after they were used | they ride along with later requests | start fresh once the image has served its purpose |
