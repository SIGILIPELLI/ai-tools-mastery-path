# 01 · Organizational AI Strategy

Level 3 built adoption skill at the team level. Level 4 operates at the
level of the whole organization, where the questions shift from "which
tool" to "what is our overall position on AI tools, and who decides."

## 1. What an organizational AI strategy actually covers

| Component | Question it answers |
|---|---|
| Scope and ambition | Which functions/processes is AI meant to touch, and to what degree? |
| Guardrails | What is never allowed regardless of tool (e.g., certain data classes, certain decisions) |
| Decision rights | Who approves new tools, at what spend/risk threshold? |
| Investment posture | Build vs. buy vs. wait, and how much budget is committed |
| Talent and enablement | How will the workforce be trained and supported? |
| Risk tolerance | What level of experimentation risk is acceptable, and where? |
| Review cadence | How often is the strategy itself revisited? |

## 2. Strategy maturity levels

| Level | Description | Typical symptom |
|---|---|---|
| Ad hoc | Individual teams adopt tools independently, no coordination | Shadow IT, duplicate spend, inconsistent data handling |
| Reactive | Central policy exists but only responds to incidents | Guidelines written after a near-miss, not ahead of one |
| Coordinated | Central governance with team-level autonomy inside guardrails | Teams self-serve within a vetted tool catalog |
| Strategic | AI capability is an explicit part of business strategy, resourced and measured | Investment tied to named business outcomes, reviewed quarterly |

Most organizations are between "ad hoc" and "reactive" and should aim for
"coordinated" before attempting "strategic" — skipping straight to a
strategic-sounding document with no coordinated foundation produces a
strategy nobody can execute.

## 3. A strategy-drafting framework

| Step | Action |
|---|---|
| 1. Inventory current state | What tools are actually in use today, officially and unofficially? |
| 2. Identify highest-value opportunities | Where does AI tooling address a real, sized business problem? |
| 3. Set explicit guardrails | Data classes, decision types, and use cases that are off-limits regardless of tool |
| 4. Define decision rights | Who can approve what, tied to spend and risk thresholds |
| 5. Commit investment and timeline | Budget, headcount, and a realistic multi-quarter timeline |
| 6. Define success metrics | Business-level outcomes, not just usage counts |
| 7. Set a review cadence | Quarterly or semi-annual, tied to a named owner |

## 4. Common strategy failure modes

| Failure mode | Why it happens | Fix |
|---|---|---|
| Strategy document with no decision rights attached | Written by a committee with no authority to enforce it | Tie every guardrail to a named approver |
| Strategy frozen at time of writing | No review cadence set | Bake in a mandatory review date |
| Strategy that ignores existing shadow usage | Inventory step skipped | Always start from actual current state, not the desired one |
| All guardrails, no enablement | Overcorrects for risk, kills legitimate adoption | Pair every guardrail with a sanctioned path to get the same value safely |
| Metrics measure activity, not outcomes | Easiest thing to measure, not the useful thing | Tie metrics to the business opportunities identified in step 2 |

## Worked example

A mid-size company discovers, through an inventory, that six different
departments have independently subscribed to AI writing and coding tools,
with no shared data policy. Rather than banning tools outright, the
strategy team runs the section 3 process: guardrails are set (no customer
PII in any tool without a signed DPA), a lightweight approval tier is
created for sub-$50/seat tools, larger commitments route through a
governance review, and $200K is committed over two quarters to a vetted
tool catalog plus training. A quarterly review is scheduled from the start.
Eighteen months later the review finds usage now concentrated in the
sanctioned catalog with negligible shadow spend, and the review cadence
becomes the mechanism that keeps the strategy current as new tools emerge.

## Exercise

Draft a one-page organizational AI strategy for a real or plausible
company using the section 3 steps. Explicitly name the decision rights
(who approves what) and the review cadence — a strategy without both is
incomplete for this exercise.
