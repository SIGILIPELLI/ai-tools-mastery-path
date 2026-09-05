# 09 · Evaluating AI Output Critically

Every earlier module has referenced verification in passing. This module
makes it the whole subject: the specific failure modes of AI-generated
output, and the habits that catch them before they cause a problem. This is
arguably the single most important skill in the entire program — tool
capability will keep changing, but the discipline of checking before
trusting doesn't.

## 1. The core failure modes

| Failure mode | What it looks like | Why it's dangerous |
|---|---|---|
| **Hallucination** | Confidently stated facts, citations, or details that are simply invented | Sounds identical to a correct answer — confidence is not a signal of accuracy |
| **Bias** | Output that reflects skewed patterns from training data (e.g., stereotyped assumptions, uneven treatment of groups or viewpoints) | Can be subtle and easy to miss if it matches your own unexamined assumptions |
| **Sycophancy** | Agreeing with or flattering the user's stated view rather than giving an independent assessment | Undermines exactly the "second opinion" value you often want from the tool |
| **Staleness** | Confidently answering with outdated information as if current | Especially risky for prices, current events, current best practices |
| **Overreach** | Answering a question outside what the tool can actually know or verify, without flagging the uncertainty | Creates false confidence in areas requiring real expertise (legal, medical, financial specifics) |

## 2. A verification habit for every output

Before using any AI output for something that matters, run this sequence:

| Step | Question |
|---|---|
| 1. Identify the claims | What specific facts, numbers, names, or citations does this contain? |
| 2. Classify each claim | Is it verifiable-and-checked, verifiable-but-unchecked, or a subjective/creative choice? |
| 3. Verify what needs it | For anything you'll repeat, cite, or act on: check it against an independent source |
| 4. Check for the failure modes above | Does anything sound suspiciously confident, one-sided, or agreeable given what you actually asked? |
| 5. Decide proportionally | Match your verification effort to the stakes (Module 2, section 3) — not every output needs the full sequence |

## 3. Spotting hallucination specifically

| Red flag | Example |
|---|---|
| Oddly specific numbers with no source given | "73.2% of companies report..." with nothing to check it against |
| Citations that don't resolve when you look them up | A paper title, author, or URL that doesn't actually exist |
| Confident detail about very recent or very obscure topics | The rarer the information, the higher the hallucination risk |
| Internal inconsistency | The answer contradicts something it said two paragraphs earlier |

## 4. Spotting bias and sycophancy

| Technique | How it works |
|---|---|
| Ask the same question with opposite framing | "Why is X a good idea" vs. "Why is X a bad idea" — compare the two answers for a tool that just agrees with whichever framing you used |
| Ask for a counter-argument explicitly | A tool that struggles to produce a genuine counter-argument to your stated view may have been agreeing rather than assessing |
| Check who/what is represented in generated examples | For image generation or scenario-writing, notice if certain groups or perspectives are consistently defaulted to or omitted |
| Request the answer without revealing your own opinion first | Reduces the tool's tendency to shape its answer around a view you've already signaled |

## Worked example

Someone drafting a business plan asks an AI assistant "Is my idea to open a
plant-based bakery in my neighborhood a good idea?" and gets an
enthusiastic, encouraging answer. Recognizing the sycophancy risk from
section 1, they ask a second, reframed question: "What are the three
biggest reasons a plant-based bakery in a residential neighborhood might
fail?" The second answer surfaces real concerns — foot traffic patterns,
niche demand size, ingredient costs — that the first, opinion-shaped
question never got at. Neither answer alone was reliable; asking both and
comparing gave a much more honest picture. They also independently verify
one specific claim from the first answer (a stated average bakery profit
margin) against an outside industry source, and find the AI's number was
noticeably out of date — an example of the staleness failure mode from
section 1.

## How It Actually Works

Every failure mode in the table above traces back to one structural fact:
a language model has no separate mechanism for verifying truth — it has
only one mechanism, next-token prediction based on patterns learned from
training data, applied identically whether the output happens to be
correct or not. There is no internal "confidence check" that fires
before a wrong statement is produced, because confidence, as expressed in
the model's tone, is generated the same way every other word is: as
whatever phrasing was statistically typical in similar contexts in the
training data. Confident, authoritative-sounding writing is common in the
training data for *correct* statements, so the model reproduces that same
register for incorrect ones — it isn't lying or guessing sneakily, it
simply has no internal signal that distinguishes "I derived this from solid
evidence" from "this is the most fluent-sounding completion available."

This is also why the same tool can be excellent at one task and unreliable
at a superficially similar one: reliability tracks how well-represented
and consistent a pattern was in training data plus how much of the
necessary information is actually present in the current context window,
not some general notion of "intelligence." Summarizing a document you
pasted in is reliable because the correct answer is sitting directly in the
input; answering "what happened in [recent event]" from memory alone is
unreliable because it depends on the model's compressed, sometimes stale
or sparse recollection of training data. Concretely, this means the
single highest-leverage verification habit is checking whether a claim
was *generated from what you gave the model* versus *recalled from
training* — the former deserves real trust, the latter deserves the same
skepticism you'd apply to an uncited claim from a stranger.

## Exercise

Take one piece of AI output you've generated recently (or generate a new
one on a topic you know well). Run the five-step sequence in section 2
against it explicitly, writing one line per step. Then apply the reframing
technique from section 4: ask the same question with the opposite framing
and compare the two answers side by side. Note any place the two answers
contradicted each other, and which one you'd actually trust more, and why.
