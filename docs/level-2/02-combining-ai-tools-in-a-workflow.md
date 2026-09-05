# 02 · Combining AI Tools in a Workflow

No single AI tool is best at everything. The intermediate skill isn't
picking one tool — it's chaining several into a workflow where each does
the part it's actually strong at, with a human checking the seams.

## 1. Why chaining beats single-tool workflows

A single tool used for an entire multi-step task inherits that tool's
weakest capability across every step. Chaining lets you route each step to
whichever tool handles it best, and it forces natural checkpoints between
steps — which is also where verification happens.

## 2. A framework for designing a chain

| Step | Question |
|---|---|
| 1. Decompose the task | What are the distinct sub-tasks, and what does each one actually require (research, drafting, structuring, visual output, code)? |
| 2. Match tool to sub-task | Which tool category (Level 1, Module 2) is strongest for each sub-task specifically? |
| 3. Define the handoff format | What exact output from step N does step N+1 need as input — plain text, structured data, an image file? |
| 4. Place verification checkpoints | After which steps does a wrong output cause the most downstream damage if uncaught? Put a human check there. |
| 5. Decide what stays manual | Some steps are faster or safer done by hand — don't force AI into every link in the chain |

## 3. Common workflow patterns

| Pattern | Example chain | Where it's used |
|---|---|---|
| Research → draft → polish | Research assistant gathers sources → chat assistant drafts → same or different tool refines tone | Content and writing work |
| Draft → critique → revise | One tool produces a draft, a second tool (or the same one in a fresh session) critiques it against a rubric | Reducing sycophancy in self-review |
| Generate → structure → automate | Chat assistant generates content → structured into a spreadsheet/table → automation platform routes it | Repeatable content or data pipelines |
| Code → test → explain | Coding assistant writes code → test runner/second tool checks it → assistant explains failures | Software work (Level 1, Module 5) |

## 4. Risks specific to chains

| Risk | What happens | Mitigation |
|---|---|---|
| Error compounding | A mistake in step 1 flows silently into every later step | Verify outputs at defined checkpoints (section 2, step 4), not just at the end |
| Format mismatches | Step 2's tool can't parse what step 1 produced | Specify the exact handoff format explicitly rather than assuming compatibility |
| Loss of context | Tool 2 doesn't know why Tool 1 made certain choices | Carry forward a short rationale note, not just the raw output |
| False efficiency | The chain takes longer to babysit than doing the task manually would have | Only chain tasks that are repeated often enough or complex enough to justify the setup cost |

## Worked example

A small nonprofit needs a monthly donor newsletter. Instead of asking one
chat assistant to do everything, the coordinator builds a chain: a research
tool pulls a summary of the month's program updates from internal
documents; a chat assistant drafts the newsletter copy from that summary;
a human editor checks facts and tone (the checkpoint, placed here because a
factual error in a donor communication is costly); an automation platform
then formats the approved copy into the email template and schedules the
send. Each tool does the part it's strongest at, and the one verification
checkpoint sits exactly where an uncaught error would do the most damage.

## How It Actually Works

Chaining tools works because it exploits a real, structural property of
these systems: a model's reliability on a given sub-task tracks how well
that sub-task matches what dominated its training and tuning, and every
product optimizes those choices differently. A research tool wired up to
live web retrieval is architecturally built to ground its output in
fetched documents before generating; a writing tool with no such retrieval
step is architecturally built only to transform text already given to it.
Asking one tool to do both jobs at once doesn't just risk lower quality —
it forces a single model instance to implicitly switch between two
different reliability regimes (grounded-in-retrieved-fact vs.
pattern-matched-from-training) within one continuous generation, with
nothing forcing a clean handoff between them.

Chaining also creates natural checkpoints for a structural reason: each
tool's output becomes the *next* tool's input, which is to say each
handoff is a fresh, bounded context window that a human can inspect before
it's consumed by the next stage. This is meaningfully different from a
single long conversation with one tool, where an early undetected error
sits inside the context and can silently distort every subsequent turn,
because the model conditions each new response on its own prior output as
much as on your instructions — a phenomenon sometimes called
self-reinforcement or drift. Breaking a task into a shorter pipeline with
human review between named stages interrupts that drift at defined points
instead of letting it compound invisibly across one long session.

## Exercise

Take a multi-step task you do regularly (a report, a content piece, a data
summary). Decompose it into sub-tasks using section 2's framework, assign
each sub-task to the tool category best suited for it, and specify the
exact handoff format between each pair of steps. Mark the one checkpoint
in the chain where a human must verify before continuing, and explain why
you chose that point over any other.
