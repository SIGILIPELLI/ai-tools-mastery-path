# 07 · Cost-Benefit Analysis of AI Tool Adoption

Not every AI tool subscription pays for itself, and "it feels useful" is
not a cost-benefit analysis. This module builds a simple, durable model
for deciding whether an AI tool is actually worth paying for — for
yourself or for a team.

## 1. What actually counts as cost

| Cost category | Examples | Often overlooked? |
|---|---|---|
| Direct subscription/usage fees | Monthly seat price, per-token/API usage | No — this is the obvious one |
| Time to learn the tool | Onboarding, prompt trial-and-error, workflow rebuilding | Yes |
| Verification overhead | Time spent checking AI output for correctness | Yes — often the largest hidden cost |
| Integration/maintenance | Connecting the tool to existing workflows, keeping that working | Yes |
| Switching cost if it doesn't work out | Data export, retraining habits, undoing dependencies | Yes |
| Risk cost | Exposure from a data leak, a bad AI output shipped externally | Yes — usually the least visible until it happens once |

## 2. What actually counts as benefit

| Benefit category | How to measure it |
|---|---|
| Time saved per task | Time before minus time after, measured on the same real task, not a demo |
| Output quality improvement | Would the without-AI version have been rejected, revised, or scored lower? |
| Throughput increase | Same time budget, more output produced at an acceptable quality bar |
| Capability unlocked | Something that wasn't feasible at all before (a small team doing work that needed a specialist) |
| Reduced error rate | Fewer mistakes reaching a customer, reviewer, or downstream system |

Time saved is the easiest benefit to measure and the easiest to overstate —
always net out verification time (cost) against raw drafting time saved
(benefit); the honest number is the difference, not the gross time saved.

## 3. A simple ROI model

| Step | Calculation |
|---|---|
| 1. Estimate baseline time/cost | How long did the task take, or cost, without the tool? |
| 2. Estimate new time/cost with tool | Include learning curve (amortized) and verification overhead every time |
| 3. Estimate tool cost | Subscription/usage fees over the same period |
| 4. Net benefit | (Baseline cost − New cost including tool fees) over a representative period |
| 5. Payback period | How long until cumulative net benefit exceeds any one-time setup/switching cost? |

| Signal | Interpretation |
|---|---|
| Net benefit clearly positive after 2-4 weeks of real use | Good candidate for continued/expanded use |
| Net benefit marginal or negative after accounting for verification time | Reconsider — the tool may not fit this task even if it "feels" helpful |
| Net benefit strongly positive but concentrated in one narrow use case | Fine — narrow, high-value use is a legitimate outcome, don't force broader adoption |

## 4. Common measurement traps

| Trap | What happens | Fix |
|---|---|---|
| Measuring only drafting time | Ignores verification/editing overhead, overstates savings | Always measure end-to-end, from prompt to accepted final output |
| Demo-task bias | Time savings measured on an easy showcase task, not real work | Measure on your own representative task mix |
| Sunk-cost continuation | Keep paying for a tool because you already invested time learning it | Re-evaluate on current, forward-looking numbers only |
| Ignoring team-wide seat costs vs. individual usage | A team license priced per-seat may cost far more than actual usage justifies | Track actual usage per seat before renewing team-wide plans |

## 5. When to walk away

| Signal | Action |
|---|---|
| Net benefit negative after a fair trial period with real tasks | Cancel; don't keep it "just in case" |
| Verification overhead consistently exceeds time saved | The tool doesn't fit this task type — try a different tool or drop AI assistance here |
| A cheaper or free tool produces comparable results for your task set | Downgrade; don't pay for capability you don't use |
| Tool cost has scaled with usage well beyond original estimate | Recompute ROI at current cost before renewing |

## Worked example

A solo consultant pays for an AI writing tool at $20/month. After a month
of real client work, she tracks that it saves roughly 45 minutes per
proposal draft but adds about 15 minutes of fact-checking and voice-editing
per draft — a net 30-minute saving across the six proposals she wrote that
month, or 3 hours total. At her billing rate, 3 hours comfortably clears
the $20 cost, so she keeps the subscription. She also notes the tool added
no measurable value on her invoicing emails, so she stops using it for
that task specifically rather than assuming it's worth using everywhere.

## How It Actually Works

Understanding how AI tools are actually priced explains several of the
"often overlooked" costs in the table. Most providers meter usage in
tokens — the same word-piece units the model predicts one at a time
internally — and charge separately (usually at a lower rate) for tokens
you send in versus tokens the model generates back, because generating
each output token costs meaningfully more compute than reading an input
token: input tokens are processed largely in parallel in one pass, while
output tokens are produced one at a time, each new token requiring another
full forward pass through the network conditioned on everything generated
so far. This asymmetry is why usage-based pricing tiers input and output
differently, and why tasks that produce long output (long-form drafting,
extensive code generation) cost more per request than tasks with similar
input length but short output (classification, yes/no answers) — a
distinction worth knowing when estimating usage-based costs for a new
workflow rather than pricing every request as if it were the same shape.

The "hidden" costs in the table — verification time, workflow disruption,
retraining — also trace back to mechanism rather than being generic
"change is hard" friction. Verification time is structurally required, not
optional caution, because (per Module 9) nothing in the generation process
itself checks output against ground truth; that check has to happen
somewhere, and if the tool doesn't do it, a human must. And retraining cost
is real because effective prompting is a learned skill specific to how
these models respond to structure and context (Module 8), not a
transferable, tool-agnostic interface skill the way, say, learning one
spreadsheet application transfers cleanly to another — which is exactly
why switching tools has a real relearning cost worth weighing against
whatever marginal capability gain motivated the switch.

## Exercise

Pick one AI tool you currently pay for (or are considering). Using the
section 3 model, estimate baseline cost, new cost including verification
time, tool subscription cost, and net benefit over a real month of your
own usage — not a hypothetical. Decide, with the numbers in front of you,
whether to keep, expand, or cancel it.
