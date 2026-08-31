# 10 · Project — An AI Tool Adoption Proposal for a Team

This capstone project pulls together every Level 3 module — evaluation,
guidelines, integration, ROI, change management, data governance, and
training — into a single deliverable: a written proposal you could actually
hand to a decision-maker to adopt an AI tool for your team.

## 1. What the proposal must contain

| Section | Draws from | Content |
|---|---|---|
| Problem statement | — | The specific team pain point or opportunity, not "AI is useful" |
| Tool recommendation | Module 3 (vendor evaluation) | The chosen tool plus 1-2 alternatives considered and rejected, with reasons |
| Evaluation evidence | Module 3 scorecard | Filled-in scorecard, ideally backed by a real pilot |
| Fit with existing stack | Module 4 | How it integrates (or doesn't) with current tools and workflows |
| Data governance impact | Module 7 | What data the tool touches, classification, and any policy exceptions needed |
| Rollout plan | Module 6 | Phases, pilot group, timeline, rollback trigger |
| Training plan | Module 8 | How the team will actually learn to use it well |
| ROI case | Module 5 | Expected costs and benefits, using the Module 5 framework, with stated assumptions |
| Success metrics | Module 5 | What will be measured post-launch, and by when |
| Risks and mitigations | Modules 2, 3, 7 | Named risks (vendor, data, adoption) and the specific mitigation for each |

## 2. A proposal-quality checklist

| Check | Why it matters |
|---|---|
| Every claim about the tool is backed by evidence, not vendor marketing | Decision-makers approve real evaluations, not sales pitches restated |
| Costs include the full picture (license, integration, training time) | Underestimating adoption cost is the most common proposal failure |
| Rollback trigger is stated, not implied | A proposal with no "what if it doesn't work" is a proposal for a permanent commitment, which is a harder ask |
| Data governance section names the actual data classification | Vague data language is a common reason proposals stall in review |
| Success metrics are specific and time-bound | "Improve productivity" isn't measurable; "reduce review time by 20% within 60 days" is |
| Alternatives considered are named, not hand-waved | Shows the recommendation survived comparison, not that it was the only option looked at |

## 3. Common reasons proposals get rejected

| Reason | Fix |
|---|---|
| No pilot data, only vendor claims | Run even a small pilot before writing the proposal; cite it explicitly |
| Cost estimate ignores integration/training time | Use the Module 5 full-cost framework, not just the license price |
| No answer to "what data does this touch" | Complete the Module 7 classification before submitting |
| Proposal reads as enthusiasm rather than analysis | Lead with the scorecard and metrics, not the pitch |
| No rollback or review checkpoint | Add an explicit 30/60/90-day review trigger |

## Worked example

A team lead wants to adopt an AI code-review assistant. Rather than writing
"this tool will make reviews faster," the proposal states: a two-week pilot
with three engineers showed average review turnaround dropping from 18
hours to 6 hours on a sample of 40 PRs; the tool's DPA was reviewed and
approved for the team's non-regulated repositories only; total cost
including onboarding time is $340/seat/year against an estimated 5
engineer-hours/week saved; the rollout is phased across three sprints with
a defined 60-day review checkpoint and a stated rollback trigger (false
positive rate above 15%). The proposal is approved on the first pass
because every claim in it is checkable.

## Exercise

Write a full adoption proposal for a real or plausible AI tool for your
team, using the section 1 template. Run it against the section 2 checklist
and the section 3 rejection-reasons list before considering it done.
