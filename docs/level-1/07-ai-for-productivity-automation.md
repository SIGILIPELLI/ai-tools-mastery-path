# 07 · AI for Productivity & Automation

Beyond generating content directly, a large and growing category of AI
tools works *around* your existing tasks — summarizing what happened,
organizing what's coming up, and triggering actions automatically. This
module covers that category: what it's built to do, how it differs from
the generative tools in earlier modules, and how to evaluate whether an
automation is actually saving you time.

## 1. The sub-categories of productivity/automation tools

| Sub-category | What it does | Example use |
|---|---|---|
| Summarization tools | Condense long content into key points | Meeting recordings, long email threads, lengthy documents |
| Scheduling assistants | Help coordinate calendars and time | Finding meeting times, drafting scheduling replies |
| Inbox/communication triage | Categorize, prioritize, or draft responses to incoming messages | Email sorting, suggested replies |
| Workflow automation platforms | Connect trigger → action across apps, sometimes with an AI step in the middle | "When a form is submitted, summarize it and post to a channel" |
| Task/note organization | Extract action items or structure from unstructured notes | Turning a meeting transcript into a task list |

## 2. Generative vs. automation tools — a key distinction

| | Generative tools (Modules 3-6) | Automation tools (this module) |
|---|---|---|
| Primary output | New content (text, image, code, audio) | An organized summary, or a triggered action |
| Where it sits | Usually a destination you go to | Usually running in the background, connected to other tools |
| Main risk | Wrong or fabricated content | Wrong trigger conditions, or acting on bad summarized information |
| Evaluation focus | Output quality | Reliability and correctness of the trigger → action chain |

## 3. Evaluating whether an automation is worth setting up

Not every repetitive task is worth automating — setup and maintenance have
a real cost. A simple threshold framework:

| Factor | Question | Leans toward automating |
|---|---|---|
| Frequency | How often does this happen? | Weekly or more |
| Time per occurrence | How long does it take manually? | 10+ minutes each time |
| Stability | Does the process change often? | Rarely changes |
| Error cost | What happens if the automation gets it wrong? | Low-to-medium (a bad summary is easy to catch; a wrongly-sent message is not) |

A rough rule of thumb: if (frequency × time saved) doesn't clearly exceed
the time to set up and occasionally maintain the automation within a few
months, do it manually for now and revisit later.

## 4. A checklist before trusting a summarization tool

Summarization deserves special caution because a bad summary can silently
propagate into decisions.

| Check | Why |
|---|---|
| Spot-check one summary against the full source | Confirms the tool isn't dropping key caveats or context |
| Check how it handles disagreement or nuance | Summaries can flatten "we debated X and didn't resolve it" into a false-confident single answer |
| Confirm action items are actually stated in the source | Some tools infer action items that weren't explicitly agreed to |
| Know who else sees the summary and whether they'll skip the source entirely | Higher-stakes if the summary becomes the only record anyone reads |

## Worked example

A team lead sets up a tool that automatically summarizes weekly team
meetings and posts action items to a shared channel. Applying section 3:
frequency is weekly, each summary previously took him 20 minutes to write
by hand, the meeting format is stable, and the error cost is moderate (a
missed action item could cause real confusion) — a reasonable candidate for
automation.

Before trusting it fully, he runs the section 4 checklist for two weeks:
each time, he compares the auto-summary against his own memory of the
meeting. In week one, he catches the tool listing an idea that was raised
and explicitly rejected as if it were an agreed action item — a case of
flattening disagreement into false confidence. He adjusts his process to
always do a 60-second read-through before posting, rather than trusting the
automation to post directly and unreviewed. That single review step
preserves most of the time savings while catching the failure mode that
actually showed up.

## Exercise

Identify one recurring task in your week that feels like a candidate for
summarization or automation. Run it through the four-factor table in
section 3 and decide whether it's actually worth automating right now. If
yes, set it up (or describe exactly how you would) and run the section 4
checklist against its first real output, noting anything it got wrong or
oversimplified.
