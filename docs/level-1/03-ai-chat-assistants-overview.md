# 03 · AI Chat Assistants Overview

Chat assistants are the most widely used category of AI tool and often the
first one people encounter, but treating "the chat assistant" as a single
undifferentiated thing leads to poor tool choices later. This module covers
what these tools generally do well, where they generally struggle, and the
evaluation criteria that distinguish one from another — without pinning
those criteria to specific products, since capabilities shift release to
release.

## 1. What chat assistants are generally good at

| Strength | Why it holds up across products |
|---|---|
| Drafting and rephrasing text | Core training task for essentially all conversational assistants |
| Explaining concepts at a chosen level of depth | Strong at adjusting register and detail when asked |
| Brainstorming and generating options | No single "correct" answer needed, so weaker guardrails don't matter as much |
| Structuring messy information | Good at turning a rough brain-dump into an outline or table |
| Answering general knowledge questions | Broad training data covers most non-specialized topics reasonably |

## 2. Where they generally struggle

| Weakness | Practical implication |
|---|---|
| Confident wrong answers ("hallucination") | Never trust a specific fact, number, date, or citation without checking it (Module 9) |
| Knowledge cutoffs / lack of live information | For anything current — prices, news, recent events — expect it to be wrong or missing unless it has live search |
| Math and precise counting | Double-check arithmetic and exact counts rather than assuming they're right |
| Long-running consistency | In very long conversations, tools can lose track of earlier constraints — restate key requirements periodically |
| Domain-specific accuracy at the edges | General assistants get shakier in highly specialized fields (niche legal, medical, or regulatory questions) — treat as a starting point, not an authority |

## 3. Evaluation criteria for comparing chat assistants

When comparing options, these criteria age better than any specific
capability claim:

| Criterion | What to check |
|---|---|
| Context window | How much text (a document, a long conversation) it can consider at once |
| Access to live information | Whether it can search the web or is limited to training data |
| File and image handling | Whether you can upload documents, spreadsheets, or images for it to work with |
| Customization / memory | Whether it can retain your preferences or a persistent instruction set across sessions |
| Integration options | Whether it connects to your other tools (calendar, docs, code) or is a standalone chat window |
| Cost structure | Free tier limits, subscription cost, usage-based pricing — checked at time of use since these shift often |

## 4. A simple mental model: assistant as a very well-read, overconfident collaborator

A durable way to calibrate trust: treat a chat assistant like a
knowledgeable colleague who has read an enormous amount but never says "I'm
not sure" unless pushed, and who can't independently verify anything
happening after their last update. You'd fact-check that colleague's
confident claim about a statistic; you wouldn't fact-check their suggestion
for how to phrase an awkward paragraph. The same split applies here.

| Ask this kind of question | Trust level |
|---|---|
| "How should I phrase this sentence more concisely?" | High — subjective, low-stakes, easy to judge yourself |
| "What's a reasonable structure for this proposal?" | High — you can evaluate the structure directly |
| "What was Company X's revenue last quarter?" | Low — verify independently, always |
| "Summarize the attached document" | Medium-high — check against the source for anything you'll rely on |

## Worked example

A student uses a chat assistant to prepare for an exam on a subject she's
weak in. She asks it to explain a concept three different ways (works well
— explanation and rephrasing are core strengths) and to quiz her with
practice questions (works well — generating varied questions is a good
fit). She also asks it for the exact publication date of a specific study
mentioned in her textbook to cite in an essay — and instead of trusting the
date it gives her, she looks it up in the textbook's own bibliography,
because a specific factual detail like a publication date is exactly the
kind of claim that's cheap for the assistant to get wrong and cheap for her
to verify directly.

## Exercise

Pick a chat assistant you have access to (any one). Ask it three questions
of different types from the table in section 4: one subjective/phrasing
question, one structural question, and one specific factual question with a
verifiable answer (a date, a statistic, a named source). Compare its
factual answer against an independent source. Write two sentences on
whether the pattern in section 4 held — was the factual answer actually
less reliable than the subjective one, and did you catch the difference
before or after checking?
