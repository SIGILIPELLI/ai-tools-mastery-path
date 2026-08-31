# 05 · Measuring ROI of AI Tool Adoption

Level 2's cost-benefit analysis worked for one person's time. At team
scale, ROI measurement needs to account for variable adoption, indirect
effects, and the risk of measuring the wrong thing entirely. This module
extends that model to team and organizational scale.

## 1. What changes at team scale

| Individual ROI | Team ROI |
|---|---|
| One person's time saved | Aggregate time saved, but adoption is rarely uniform across the team |
| Simple before/after comparison | Needs a control or baseline group, since other factors also change over time |
| Personal judgment of quality | Needs a shared quality metric the team agrees on |
| Cost is one subscription | Cost includes seats, training time, integration/maintenance, and management overhead |

## 2. A team ROI measurement framework

| Metric type | Example | Data source |
|---|---|---|
| Efficiency | Time per task, cycle time, throughput | Existing project tracking / time tracking tools |
| Quality | Error rate, revision cycles, customer-facing defect rate | Existing QA/review data |
| Adoption | % of team actively using it, frequency of use | Usage logs, surveys |
| Cost | Subscription + training + integration + verification time | Finance records + time estimates |
| Satisfaction | Team-reported usefulness, friction points | Structured survey, not just anecdote |

## 3. Building a fair baseline

| Approach | When to use |
|---|---|
| Before/after on the same team | Simplest; works when task volume and composition are stable across the comparison period |
| Pilot vs. non-pilot group (same time period) | Stronger; controls for external factors like seasonal workload changes |
| Historical trend extrapolation | Useful when a true control group isn't feasible; compare against the pre-existing trend line, not just the prior period's raw number |

Avoid comparing a single month post-adoption against a single month
pre-adoption without checking whether anything else changed in that window
(headcount, project mix, deadlines) — those confounds are easy to miss and
will bias the result in either direction.

## 4. Common measurement traps at team scale

| Trap | What happens | Fix |
|---|---|---|
| Averaging over uneven adoption | Heavy users' gains get diluted by non-users, understating true per-user impact | Report both team-wide and per-active-user metrics separately |
| Counting time saved without counting new review overhead | Overstates net benefit | Include verification/review time as a cost, same as Level 2 Module 7 |
| Cherry-picking the success stories | A few impressive anecdotes stand in for a real aggregate measurement | Use the structured metrics in section 2, and report the full distribution, not just highlights |
| Ignoring switching/ramp-up cost in the ROI window | Early-period ROI looks artificially poor, causing premature cancellation | Model a fair ramp-up period before judging steady-state ROI |

## 5. Reporting ROI to stakeholders

| Audience | What to emphasize |
|---|---|
| Budget owner / finance | Net cost vs. benefit in dollar or hour terms, payback period |
| Team members | Quality and workload impact, not just efficiency numbers |
| Leadership / governance committee | Aggregate impact plus adoption rate and risk posture (ties to Module 7) |

## Worked example

A support organization pilots an AI-assisted response drafting tool with
half of its agents over one quarter, keeping the other half as a
comparison group handling a similar ticket mix. Team-wide time-per-ticket
drops only modestly when averaged across all agents, but the per-active-
user metric for agents actually using the tool regularly shows a much
larger reduction — revealing that adoption, not tool capability, is the
binding constraint. The team invests in more training (Module 8) rather
than concluding the tool doesn't work, and re-measures the following
quarter with adoption tracked explicitly.

## Exercise

Design a team-scale ROI measurement plan for an AI tool your team uses or
is considering. Specify the baseline approach from section 3 you'd use,
list at least one metric from each row of section 2, and identify one
confound that could bias your measurement if left unchecked.
