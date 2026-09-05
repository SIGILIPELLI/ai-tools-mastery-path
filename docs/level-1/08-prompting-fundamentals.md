# 08 · Prompting Fundamentals That Work Across Tools

Every category covered so far responds to the same underlying prompting
principles, even though the tools differ wildly in what they produce. This
module is deliberately tool-agnostic: the techniques here apply whether
you're talking to a chat assistant, describing a coding task, or writing an
image prompt, and they'll keep working as specific products change.

## 1. The five elements of a well-formed prompt

| Element | What it does | Missing it looks like |
|---|---|---|
| **Task** | States what you actually want, as a concrete action | "Tell me about marketing" (vague) vs. "Write three subject lines for a re-engagement email" (concrete) |
| **Context** | Gives the background the tool needs but doesn't already have | Omitting that the audience is lapsed customers, not new leads |
| **Constraints** | Format, length, tone, things to avoid | Getting a 500-word answer when you needed three bullet points |
| **Examples** | Shows the shape of a good answer when words alone are ambiguous | Getting a technically-correct but stylistically-wrong result |
| **Success criteria** | States how you'll judge the output | Not knowing whether "good enough" was actually met |

Not every prompt needs all five explicitly — a quick brainstorming question
doesn't need constraints — but for anything you'll actually use, checking
which elements you left implicit is the fastest way to diagnose a
disappointing result.

## 2. Iteration beats one perfect prompt

The most common beginner mistake is trying to write one flawless prompt
upfront. In practice, a short first prompt followed by targeted follow-ups
usually beats a long, over-engineered first attempt.

| Instead of | Try |
|---|---|
| One giant prompt trying to specify everything | A reasonable first prompt, then "make it shorter" / "more formal" / "add an example" as follow-ups |
| Starting over when a result is close but not right | Pointing at exactly what's wrong: "keep the structure, but the second paragraph is too technical for a general audience" |
| Assuming the tool "should have known" something | Stating it explicitly next time — the tool has no memory of what you consider obvious unless told |

## 3. Being specific about format and constraints

Format instructions are cheap to give and dramatically reduce rework.

| Constraint type | Example phrasing |
|---|---|
| Length | "In 3 sentences" / "Under 150 words" / "One page" |
| Structure | "As a table" / "As a numbered list" / "As three labeled sections" |
| Tone/audience | "For a non-technical executive" / "Casual, for a team Slack message" |
| Exclusions | "Without jargon" / "Don't include a conclusion paragraph" |
| Role framing | "Review this as a skeptical editor" — useful for critique, less useful for generation |

## 4. Common prompting mistakes and their fixes

| Mistake | Why it hurts | Fix |
|---|---|---|
| Asking a compound question | Answers to the least important part crowd out the important one | Split into separate prompts, or explicitly rank what matters most |
| Not stating the audience | Output defaults to a generic register that fits nobody well | State the audience directly, every time it's not obvious |
| Accepting the first answer for anything reused often | Small phrasing issues compound if copy-pasted repeatedly | Iterate at least once before reusing a prompt as a template |
| Treating a prompt like a search query (keywords only) | Undersells what these tools can actually do with full sentences and context | Write in full sentences with real context, not fragments |

## Worked example

A manager wants a status update email for stakeholders. Her first prompt:
"write a project status update" produces something generic and too long.
Rather than starting over, she adds the missing elements from section 1 as
follow-ups: "the audience is non-technical executives, keep it under 200
words, and the key news is that we're two weeks behind schedule but the
budget is on track — lead with that, don't bury it." The second version is
close but too apologetic in tone; her third prompt is a single targeted
fix: "same content, but more matter-of-fact, less apologetic." Three short
prompts, each fixing one specific gap, got her a usable result faster than
trying to write one perfect instruction upfront.

## How It Actually Works

Every element in the five-part framework works because it changes the
literal input sequence the model conditions its next-token predictions on
— there's no separate "intent recognition" stage that interprets what you
*meant*; the model only ever sees the text of the prompt itself and
predicts what plausibly follows it. This is why specificity and structure
have an outsized, almost mechanical effect on output quality. A vague
prompt like "write about dogs" sits in a huge, diffuse region of the
model's learned probability space — many wildly different continuations
are all roughly equally likely, so the output is generic almost by
definition. A detailed prompt (audience, format, constraints, examples)
narrows that region dramatically, because it makes many plausible
continuations far *less* statistically likely than the few that satisfy all
the stated constraints simultaneously.

Providing examples ("few-shot prompting") works through the same mechanism
as everything else — the model isn't "learning" in the sense of updating
its weights; it's using the examples already sitting in its context window
as extremely strong evidence about the pattern the *next* generated text
should follow, the same way it uses everything else in the conversation.
This is also why instructions placed at the very start or very end of a
long prompt are often followed more reliably than ones buried in the
middle — a widely observed property sometimes called "lost in the middle,"
where a transformer's attention mechanism, despite in principle being able
to weigh any position equally, empirically tends to attend more strongly to
content near the boundaries of its context window. Structuring a prompt
with the most important constraints first or last, rather than sandwiched
in a long paragraph, is a direct, practical consequence of that mechanism.

## Exercise

Pick a real task and write a deliberately underspecified first prompt (task
only, no context/constraints). Note what's disappointing about the result.
Then add exactly one missing element from section 1 per follow-up prompt,
in sequence, and note which single addition produced the biggest
improvement. Write one sentence naming which element you personally tend to
skip most often.
