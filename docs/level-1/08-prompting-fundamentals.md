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

## Exercise

Pick a real task and write a deliberately underspecified first prompt (task
only, no context/constraints). Note what's disappointing about the result.
Then add exactly one missing element from section 1 per follow-up prompt,
in sequence, and note which single addition produced the biggest
improvement. Write one sentence naming which element you personally tend to
skip most often.
