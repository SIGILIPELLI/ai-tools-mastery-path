# 08 · Training Teams to Use AI Tools Effectively

Tool access without training produces the exact adoption gap seen in the
ROI module: heavy users get real value, everyone else gets frustration or
ignores the tool entirely. This module covers how to close that gap
deliberately.

## 1. Why access alone doesn't work

| Assumption | Reality |
|---|---|
| "It's intuitive, they'll figure it out" | Most people use 10-20% of a tool's real capability without guided examples |
| One kickoff demo is enough | Skills decay without reinforcement; a single session rarely changes daily habits |
| Training is a one-time event | Tools and best practices change faster than a static curriculum can track |

## 2. A tiered training model

| Tier | Audience | Content |
|---|---|---|
| Foundational | Everyone with access | What the tool is for, what it isn't for, data governance rules (Module 7), basic prompting |
| Role-specific | Each function (support, sales, engineering, etc.) | Workflows specific to that role's actual tasks, using real examples from that team |
| Power user | Volunteers / tool champions | Advanced techniques, edge cases, how to help peers |

Foundational training without role-specific follow-up is the most common
gap — generic "how to prompt" sessions rarely translate into changed daily
behavior without role-specific worked examples.

## 3. Training formats and when to use them

| Format | Best for | Limitation |
|---|---|---|
| Live workshop with hands-on exercises | Building initial confidence, answering live questions | Doesn't scale well, hard to repeat for new hires |
| Recorded walkthroughs + internal docs | Onboarding new hires, reference material | No interactivity, can go stale |
| Office hours / async Q&A channel | Ongoing support after initial training | Requires a committed owner to stay responsive |
| Peer champions embedded in each team | Contextual, just-in-time help | Depends on champions having bandwidth and staying current |

The strongest programs combine at least one live/interactive format with
one persistent reference format, rather than relying on either alone.

## 4. Measuring whether training worked

| Metric | What it tells you |
|---|---|
| Adoption rate before/after training | Whether training actually changed behavior, not just satisfaction |
| Time-to-first-use for new hires | Whether onboarding materials are sufficient without live support |
| Support/question volume over time | Should decline as training and documentation mature |
| Self-reported confidence (survey) | Useful but should be checked against actual usage data, not trusted alone |

Tie this back to the adoption metric from Module 1's champion model and
Module 5's ROI framework — training is the lever that moves adoption, and
adoption is what determines whether ROI is realized.

## 5. Common training pitfalls

| Pitfall | Fix |
|---|---|
| Training on the tool's marketing use cases, not the team's real tasks | Build exercises from actual recent work examples |
| Training once at rollout and never updating it | Schedule a refresh cadence tied to major tool or policy changes |
| No path for ongoing questions after the initial session | Stand up the office-hours/champion model in section 3 |
| Ignoring skeptics instead of addressing their specific objections | Use Module 6's change management techniques alongside training |

## Worked example

A support team rolls out an AI drafting tool with a single all-hands demo.
Three months later, adoption is uneven and several agents report they
"tried it once and it didn't help." A follow-up role-specific workshop
built from the team's own recent tickets — showing exactly where the tool
saves time and where it doesn't — moves adoption from scattered to
consistent, and a lightweight peer-champion rotation keeps new hires
onboarded without repeating the full workshop each time.

## How It Actually Works

"Most people use 10-20% of a tool's real capability without guided
examples" is a specific, explainable consequence of how these tools
respond to input, not a vague generalization. Per Module 8, output quality
is highly sensitive to prompt structure and specificity — the gap between
a vague, unguided prompt and a well-structured one is often the entire
gap between mediocre and excellent output from the *same* underlying
model. Someone given access but no guided examples typically discovers only
the most obvious, minimal-effort way to phrase a request (roughly matching
however the tool's own marketing or onboarding screen phrased its demo
prompt) and never learns the structural techniques — providing examples,
specifying format and audience, breaking a large task into staged prompts
(Module 4) — that would unlock meaningfully better output from the exact
same tool they already have. This is a training gap, not a tool-capability
gap, which is why simply upgrading someone's tool tier rarely closes it on
its own.

Effective training also has to directly counter the trust-calibration
problem named in Module 6 (change management), because self-directed
exploration alone doesn't reliably build it: a person exploring a tool on
their own tends to develop trust based on how many times output happened
to look right in their limited testing, not on any principled
understanding of which task categories the tool is structurally reliable
or unreliable for (Module 9). Training that explicitly walks through real,
task-relevant examples of both — a case where AI output was fluent, wrong,
and needed catching, alongside a case where it was reliably strong —
teaches the underlying pattern (grounded vs. recalled, verified vs.
unverified) in a way self-directed trial and error usually never surfaces
on its own, however much time is given to it.

## Exercise

Design a two-tier training plan (foundational + role-specific) for an AI
tool your team uses. For each tier, specify the format, the audience, and
one metric from section 4 you'd track to know it worked.
