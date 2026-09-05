# 10 · Project — Build a Personal AI Toolkit

This capstone pulls together every module in Level 1 into a single
deliverable: a personal AI toolkit of 3-5 tools, each chosen deliberately
and justified in writing, plus the verification habits you'll actually use
with each one. This is not a theoretical exercise — the template below
produces something you can keep using after this course.

## Why a written toolkit, and why now

Most people accumulate AI tools accidentally — whatever they tried first,
whatever a colleague mentioned. A deliberately built toolkit, chosen against
your actual recurring tasks (Module 1) using a real decision process
(Module 2), with matched verification habits (Module 9) already built in,
outperforms an accidental collection because you already know *why* each
tool is there and *how much* to trust each one's output.

## The toolkit template

### 1. Task inventory (Module 1)

| Recurring task | Category | Frequency |
|---|---|---|
| | | |
| | | |
| | | |
| | | |
| | | |
| | | |

### 2. Tool selection (Module 2)

For each category represented above, name the tool (or type of tool if
undecided) you'll use, and run the four-question framework:

| Category | Chosen tool | Stakes level | One-off or recurring? | Context needed |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

### 3. Per-tool verification habit (Module 9)

For each tool in your toolkit, state the specific verification step you
commit to using every time, matched to the stakes level from section 2.

| Tool | Verification habit | Trigger for extra scrutiny |
|---|---|---|
| | | |
| | | |
| | | |

### 4. Prompting notes (Module 8)

For your two most-used tools, write one example prompt that worked well for
you, and one lesson learned about what to include (context, constraints,
examples) to get better results from that specific tool going forward.

### 5. Boundaries — what you will NOT use AI for (Module 2 & 9)

List at least two tasks or situations, specific to your own life or work,
where you've decided AI tools are not appropriate — because the stakes are
too high, verification isn't feasible, or a policy prohibits it.

## Worked example (filled toolkit, abbreviated)

A small-business owner's filled excerpt:

- **Task inventory**: customer email replies (writing, daily), social
  media graphics (image, weekly), monthly bookkeeping summary (data
  analysis, monthly), website copy edits (writing, occasional).
- **Tool selection**: a general chat assistant for email replies (low
  stakes, recurring, minimal context needed beyond the customer's message);
  an image generation tool for social graphics (low-medium stakes,
  recurring, needs brand style context); a data-analysis-capable assistant
  for the bookkeeping summary (medium stakes since numbers feed real
  decisions, monthly, needs the actual spreadsheet as context).
- **Verification habits**: email replies get a 10-second read before
  sending (low stakes, fast check); the bookkeeping summary gets every
  number cross-checked against the source spreadsheet before she trusts a
  total (medium-high stakes, full check every time); social graphics get
  checked against the tool's commercial-use terms before public posting.
- **Prompting notes**: for email replies, including the customer's exact
  wording plus "match a warm but brief tone, 3 sentences max" consistently
  outperformed a generic "write a polite reply."
- **Boundaries**: she will not use AI to draft responses to formal
  complaints or anything mentioning a refund dispute — those get a fully
  human-written reply, since the stakes and nuance are too high for a
  quick-check verification habit to catch every problem; she also will not
  use an AI tool to generate final numbers for her tax filing without a
  human accountant's review.

## How It Actually Works

Choosing tools by category rather than by brand — the approach this
project asks you to formalize in writing — holds up well precisely because
category maps to underlying mechanism, and mechanism is what actually
determines a tool's strengths and blind spots. A "writing assistant" and
a "research assistant" might be running the exact same base model under
the hood, wrapped in different system prompts, different default
temperature settings, and different amounts of retrieval — but knowing
*that* is what tells you where each is trustworthy without re-testing
every tool from scratch. Your toolkit document is, in effect, a personal
map of which mechanism you're relying on for which task: pure generation
from training data (treat with skepticism), generation grounded in
something you supplied (trust much more, but still check), or generation
plus a tool-use loop that checked its own work against real output (trust
proportionally to how much of the work that loop actually verified).

Writing this down matters because these underlying mechanisms are far more
stable than the branded products sitting on top of them. A product you
chose can be discontinued, repriced, or have its system prompt changed
overnight by its provider — but the reasoning "I trust this category of
tool for grounded tasks and verify anything it recalls from memory alone"
survives every one of those changes, because it's a statement about how the
technology works, not about which vendor currently implements it best. That
durability is the entire point of building the toolkit as a document with
reasoning attached, rather than as a bare list of app names.

## Exercise (the deliverable)

Fill out all five sections of the template above completely, using your own
real tasks, tools, and habits — not hypothetical ones. Where you genuinely
haven't picked a tool yet, write "Undecided — trying [option] and
[option] next" rather than leaving it blank. Keep this filled-out toolkit;
Level 2's capstone (an AI-augmented workflow design) builds directly on it.
