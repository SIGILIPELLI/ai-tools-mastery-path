# 08 · Building Personal AI-Assisted Routines

A routine is a workflow you run often enough that it deserves to be
designed once and reused, rather than improvised each time. This module
covers how to turn ad-hoc AI usage into a small set of durable personal
routines.

## 1. Why routines beat ad-hoc prompting

Ad-hoc prompting re-derives the same context, the same constraints, and
the same quality bar every single time — and it's inconsistent because
each session starts from a slightly different prompt. A routine fixes the
steps, the inputs, and the checks once, so the outcome is more consistent
and takes less thought each time you run it.

## 2. Anatomy of a good personal routine

| Component | Purpose |
|---|---|
| Trigger | What starts this routine — a day of the week, an inbox state, a recurring task |
| Fixed inputs | What you always supply (a template, a set of files, a standing set of constraints) |
| AI step(s) | What the AI tool actually does, ideally one clear job at a time |
| Review checkpoint | Where you check the output before it's used or sent |
| Output destination | Where the finished result goes (a doc, an email, a task list) |

A routine you can't describe in these five parts isn't a routine yet — it's
still an improvisation, even if you do it every week.

## 3. Candidate routines worth building

| Recurring task | Why it's a good routine candidate |
|---|---|
| Weekly status update drafting | Repetitive structure, fixed inputs (what you did that week), low risk if reviewed |
| Meeting notes → action items | Clear transformation task with a verifiable output format |
| Inbox triage / first-pass email drafts | High frequency, benefits heavily from consistent categorization |
| Reading list summarization | Time-consuming manually, well-suited to AI's summarization strength |
| Recurring report formatting | Structural transformation with little judgment required — a strong AI fit |

## 4. Designing the review checkpoint

| Output destination | Review bar |
|---|---|
| Personal notes / private draft | Light — skim for obvious errors |
| Shared internal document | Medium — check facts and tone before sharing |
| External or high-stakes communication | Full read-through, always, no exceptions |
| Automated downstream action (e.g. auto-filed record) | Spot-check periodically even if not reviewed every run — routines drift silently |

## 5. Common pitfalls

| Pitfall | Symptom | Fix |
|---|---|---|
| Building a routine before you've done the task manually a few times | The routine encodes a bad process | Do the task manually 2-3 times first to understand what "good" looks like |
| Removing the review checkpoint once the routine "feels reliable" | Errors resume silently after weeks of fine output | Keep at least a light review step permanently, especially for anything reaching other people |
| Over-automating low-frequency tasks | Time spent designing the routine exceeds time it will ever save | Reserve routine-building for genuinely recurring tasks |
| Letting routines calcify | The underlying task changes but the routine's fixed inputs don't | Revisit routines periodically, especially after a change in role or tools |

## Worked example

A team lead spends 30 minutes every Friday writing a status update by
reviewing scattered notes and Slack messages. She builds a routine: she
keeps a running plain-text log of what she did each day (fixed input),
feeds the week's log to an AI tool with a fixed prompt asking for a
structured update in her team's standard format (AI step), reads the draft
against her own memory of the week before sending (review checkpoint), and
posts it to the team channel (output destination). The task now takes
about 10 minutes weekly, and the format is more consistent than her manual
version because the template never drifts.

## How It Actually Works

A saved, reusable prompt template works mechanically for the same reason
few-shot examples and detailed prompts improve one-off results (Module 8):
it fixes the constraints, format, and framing that would otherwise vary
prompt-to-prompt, which narrows the model's space of plausible completions
to the same tight region every time it runs. Ad-hoc prompting is
inconsistent specifically because casually re-typing "summarize this" or
"draft a reply" each time produces slightly different wording, which
shifts which region of the model's learned probability space gets
activated — sometimes only slightly, but enough to change tone, length, or
structure in ways that feel arbitrary. A saved template removes that
variance at the source: the input sequence conditioning the model's output
is, by construction, nearly identical every time you run it, which is why
routines feel more "reliable" than the same task prompted freshly — not
because the model changed, but because the input stopped varying.

This also explains why a good routine template usually encodes more than
just the instruction — it typically embeds a worked example of the
desired output format, explicit constraints (length, tone, what to exclude),
and sometimes a placeholder structure to fill in. Each of those elements is
doing real conditioning work on the model's next-token predictions, not
just serving as a readability aid for the human reusing the template. A
routine that degrades over time (starts producing worse output for no
apparent reason) is almost always a sign the underlying model version
changed on the provider's end — since your template's wording didn't
change, the shift means the same input sequence is now landing in a
subtly different learned probability space, which is worth checking before
assuming you did something wrong.

## Exercise

Pick one task you do at least weekly that has a fairly repeatable shape.
Design it as a routine using the five components in section 2. Run it for
two weeks, keeping the review checkpoint every time, and note any place
the AI output would have been wrong if you hadn't checked it.
