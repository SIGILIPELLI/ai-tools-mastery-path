# 01 · AI Tool Adoption for Teams

Level 2 built individual judgment. Level 3 shifts to teams: adopting an AI
tool across several people changes the problem — consistency, shared data
handling, and buy-in now matter as much as the tool's raw capability.

## 1. Why team adoption differs from individual adoption

| Individual adoption | Team adoption |
|---|---|
| One person's workflow and risk tolerance | Must fit the least-cautious and most-cautious team member both |
| Personal data handling judgment | Requires a shared, explicit policy (Module 2, 7) |
| Cost borne by one person | Requires budget owner sign-off and per-seat justification |
| Skill gap is one person's learning curve | Skill gaps vary widely across a team and must be planned for |
| Failure affects one person's output | Failure can affect a shared deliverable or reach customers |

## 2. A team adoption framework

| Phase | Key activity |
|---|---|
| 1. Pilot | Small group, real tasks, defined success criteria, time-boxed |
| 2. Evaluate | Compare pilot results against the criteria set beforehand, not against enthusiasm |
| 3. Guideline-setting | Write down what's approved, for what data, under what review process (Module 2) |
| 4. Rollout | Staged rollout with training, not a single announcement and access grant |
| 5. Monitor | Ongoing sampling of usage and output quality, not a one-time check |

## 3. Pilot design checklist

| Element | Guidance |
|---|---|
| Pilot group size | Small enough to manage closely, diverse enough to surface different use cases |
| Success criteria | Defined in writing before the pilot starts, ideally quantitative (Module 5's ROI approach) |
| Time box | A fixed end date to force an actual evaluation rather than indefinite "let's see" |
| Real tasks | Pilot on the team's actual current work, not a synthetic demo task |
| Feedback mechanism | A structured way to collect what worked and what didn't, not just informal chatter |

## 4. Sources of team adoption failure

| Failure mode | Cause | Mitigation |
|---|---|---|
| Champion-driven rollout | One enthusiastic person drives adoption; the rest use it inconsistently or not at all | Involve skeptical team members in the pilot design, not just the enthusiasts |
| No shared guidelines | Everyone uses the tool differently, with inconsistent data handling and quality bar | Write guidelines (Module 2) before wide rollout, not after problems appear |
| Mandate without training | Tool access granted, no time or structure given to actually learn it | Budget real training time (Module 8) as part of the rollout, not an afterthought |
| Ignoring the resisters | Dismissing concerns as "resistance to change" without examining if they're valid | Treat resistance as signal; some objections are legitimate risk concerns |

## 5. Buy-in tactics that actually work

| Tactic | Why it works |
|---|---|
| Start with the pain point, not the tool | People adopt things that solve a problem they already feel, not because a tool is impressive |
| Show real output on real team tasks | Demos on unrelated examples don't transfer trust to actual work |
| Let early adopters show peers, not just management | Peer-to-peer credibility often outweighs top-down mandate |
| Make the guideline visible and easy to follow | A policy no one can find or remember gets ignored regardless of quality |

## Worked example

An engineering manager wants her team of eight to adopt an AI coding
assistant. Instead of a blanket rollout, she runs a three-week pilot with
three volunteers of varying skepticism, working on real current tickets,
with success criteria set beforehand: measurable reduction in time-to-PR
without an increase in review comments per PR. The pilot shows a real but
modest time reduction and, notably, one team member's review comments
increased — surfacing that the tool worked well for boilerplate code but
poorly for the team's more idiosyncratic internal framework. She rolls out
with explicit guidance on where it helps most, rather than a blanket
"use it for everything" mandate.

## How It Actually Works

Several of the differences the table draws between individual and team
adoption stem from a mechanical fact about how most AI products are
licensed and configured: an individual subscription is a single account
with the vendor's default data-handling terms, while an organizational
deployment typically runs through a different plan or API tier that
carries a distinct contract, different default retention settings, and
often options individual plans don't expose at all — like a data
processing agreement, admin-controlled retention windows, or an option to
route requests through a "zero data retention" endpoint that the vendor
contractually commits not to log or use for training. An individual
signing up for the consumer product and a team's IT department provisioning
enterprise seats are not using "the same tool" in any legally or
operationally meaningful sense, even when the underlying model serving
both plans is identical — this is precisely why Module 2's internal
guidelines and Module 7's data governance work exist as separate,
necessary layers on top of individual tool competence.

The "shared, explicit policy" row also reflects something structural about
how these tools behave at the edges: because output is generated from
learned patterns rather than fixed rules, two people on the same team,
using the same tool for the same kind of task, can get meaningfully
different guidance from it depending on exactly how they phrase their
prompt — there's no single canonical "the tool's answer" to appeal to when
disagreements arise. A written team policy substitutes for that missing
canonical answer: it's the team's own explicit decision about acceptable
use, filling a gap the tool's own behavior can't reliably fill on its own
because the tool's output is inherently variable prompt to prompt and
person to person.

## Exercise

Design a two-to-four-week pilot for introducing (or re-evaluating) one AI
tool with a team you're part of. Write the pilot group, the time box, and
at least two measurable success criteria before you would consider running
it, using the checklist in section 3.
