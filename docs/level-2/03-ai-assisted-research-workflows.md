# 03 · AI-Assisted Research Workflows

Research is one of the highest-leverage uses of AI tools, and one of the
easiest to get wrong. This module builds a repeatable workflow for using AI
to accelerate research without letting it quietly corrupt your conclusions.

## 1. What AI is good and bad at in research

| Task | AI strength | Risk |
|---|---|---|
| Summarizing a long document you provide | Strong — grounded in given text | Can still drop caveats or nuance |
| Explaining an unfamiliar concept | Strong — good first pass | May oversimplify or miss edge cases |
| Finding facts, dates, statistics, citations | Weak — prone to fabrication | Confident-sounding wrong answers ("hallucination") |
| Generating search queries and angles to explore | Strong — good for breadth | Won't know what's actually been published recently |
| Synthesizing across multiple sources you supply | Strong | Quality caps at the quality of what you fed it |
| Evaluating source credibility | Weak on its own | Needs your judgment, not the model's confidence |

The pattern: AI is a strong accelerant for working *with* text you supply or
retrieve, and an unreliable oracle for facts it has to recall from memory.

## 2. A four-stage research workflow

| Stage | What you do | AI's role |
|---|---|---|
| 1. Scope | Write one sentence: what question are you answering, and what would a good answer let you do next? | Optional — ask AI to help sharpen a vague question into a specific one |
| 2. Gather | Collect primary sources yourself (search engines, databases, docs) rather than asking AI to recall facts | Generate search queries and angles; summarize sources you paste in |
| 3. Synthesize | Feed AI the sources you gathered and ask for a structured synthesis, not new facts | Compare, contrast, and organize — grounded in what you gave it |
| 4. Verify | Spot-check every claim that would matter if wrong, against the original sources | None — this step is yours by design |

## 3. The verification discipline

| Claim type | Verification bar |
|---|---|
| Numbers, dates, statistics | Always trace to a primary source before using |
| Named quotes or attributions | Always verify the exact source — a common fabrication pattern |
| General conceptual explanations | Spot-check against one reputable source |
| Your own synthesis of provided material | Re-read the AI's summary against the source it was given |

A useful habit: ask the AI to cite *which of the sources you gave it*
supports each claim in its synthesis. This doesn't stop fabrication of
external facts, but it does make grounded claims traceable and exposes
ungrounded ones — an answer with no traceable source in your material is a
signal to verify manually.

## 4. Common failure modes

| Failure | Cause | Fix |
|---|---|---|
| Hallucinated citations | Model asked to recall specific sources from memory | Never ask AI to produce citations it wasn't given; only cite what you supplied |
| False confidence | Fluent, well-structured prose reads as authoritative regardless of accuracy | Treat fluency and accuracy as unrelated; verify independently of tone |
| Source laundering | AI summary loses the caveats/uncertainty in the original source | Explicitly ask it to preserve stated uncertainty and limitations |
| Search-then-stop | Treating the first AI summary as the final answer | Always compare against at least one independent source for anything consequential |

## Worked example

A product manager needs to understand competitor pricing models before a
planning meeting in two hours. Instead of asking an AI assistant "what do
competitors charge," which risks fabricated numbers, she visits each
competitor's actual pricing page, saves the text, and pastes all four into
an AI tool asking it to synthesize a comparison table of tiers, limits, and
price points — a task the AI is strong at because it's working from
supplied text, not memory. She spot-checks the table against the original
pages before the meeting and catches one row where the AI merged two
tiers incorrectly.

## Exercise

Pick a question you genuinely need to answer. Run it through the four-stage
workflow: write the one-sentence scope, gather three primary sources
yourself, ask an AI tool to synthesize them into a structured summary, and
verify the three most consequential claims against the original sources.
Note any claim the AI made that wasn't traceable to what you gave it.
