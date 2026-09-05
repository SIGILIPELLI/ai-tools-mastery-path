# 06 · Measuring Organizational AI Maturity

Strategy (Module 1) sets direction; this module gives you a way to
measure, concretely, how far an organization has actually progressed —
so progress is judged by evidence, not by how many tools have been
purchased.

## 1. A maturity model across dimensions

| Dimension | Level 1 (Ad hoc) | Level 2 (Coordinated) | Level 3 (Strategic) | Level 4 (Optimizing) |
|---|---|---|---|---|
| Governance | No formal review process | Tiered approval process exists (Module 2) | Governance tied to business risk tiers | Governance continuously refined against incident/outcome data |
| Vendor management | Ad hoc, per-team contracts | Centralized contracts, basic risk register | Continuous risk monitoring (Module 3) | Portfolio-level risk actively managed and diversified |
| Adoption | Isolated pilots | Systematized rollout kits (Module 4) | Org-wide adoption tracked centrally | Adoption self-sustaining, new use cases surfaced bottom-up |
| Measurement | No consistent metrics | Team-level ROI tracked | Org-wide comparable ROI framework | ROI tied directly to business strategy outcomes |
| Ethics/responsible use | No formal policy | Basic guidelines exist | Decision-tiering and audits in place (Module 5) | Audits proactively catch and fix issues before harm occurs |
| Talent/enablement | Self-taught, inconsistent | Formal training exists | Training tied to role-based competency | Internal AI capability seen as a competitive differentiator |

## 2. How to actually assess maturity

| Step | Action |
|---|---|
| 1. Score each dimension | Use evidence (documents, data, interviews), not self-report impressions |
| 2. Identify the binding constraint | The lowest-scoring dimension usually limits overall organizational capability, regardless of how advanced others are |
| 3. Avoid "average" scoring | A high average masking one very low dimension (e.g., strong adoption, zero governance) is a risk, not a strength |
| 4. Set a realistic target, not "level 4 everywhere" | Advancing one level in the binding-constraint dimension is usually higher value than a small gain across all dimensions |
| 5. Re-assess on a fixed cadence | Maturity assessment tied to the same review cadence as the strategy (Module 1) |

## 3. Common measurement pitfalls

| Pitfall | Fix |
|---|---|
| Measuring tool count or spend as a proxy for maturity | Spend and tool count reflect adoption, not capability or governance quality |
| Self-assessed scores with no evidence | Require documentation or data behind every dimension score |
| Treating maturity as a one-time audit | Tie it to a recurring cadence; maturity can regress as much as it can advance |
| Chasing the highest level on every dimension simultaneously | Prioritize the binding constraint; balanced-but-mediocre is often worse than uneven-but-addressing-the-real-gap |
| No link between the assessment and actual investment decisions | Feed maturity gaps directly into the next planning cycle's priorities |

## Worked example

An organization scores itself using the section 1 model and finds strong
adoption and reasonable measurement (both Level 3), but governance still
at Level 1 — approvals happen informally, with no tiering or logged
rationale. Despite the strong-looking average, the governance gap is
identified as the binding constraint: it's actively creating risk
(untracked data exposure across a growing number of tools) that the
strong adoption score is making worse, not better. The next planning
cycle prioritizes standing up the tiered governance model (Module 2)
before investing further in adoption breadth.

## How It Actually Works

A maturity model that measures governance, training, and outcome
tracking as separate dimensions (rather than a single "how much AI do we
use" score) reflects a real fact about how these systems fail: risk and
capability don't move together. An organization can have widespread, heavy
tool usage (high on a naive adoption-volume metric) while still being
governance-Level-1 and training-Level-1 — meaning nobody has mapped which
use cases rely on unreliable unaided recall (Module 9), nobody has audited
for aggregate bias effects (Module 5 of this level), and data may be
flowing into tools whose contract terms were never reviewed (Module 3,
Level 3). Heavy usage without maturity on the other dimensions isn't
organizational AI success — mechanistically, it's exposure at scale,
which is exactly why a maturity framework needs governance and outcome
measurement as independent axes rather than collapsing everything into one
adoption number.

"Governance continuously refined against incident/outcome data," the
highest maturity level in the table, matters because none of the risks
this program has covered are fully preventable through upfront policy
alone — confidently-wrong output (Module 9), aggregate bias (Module 5),
and silent model version changes (Module 3) are all properties that only
become visible through ongoing measurement of real outcomes, not
one-time review at initial tool approval. An organization at the highest
maturity level has built the feedback loop that catches these as they
emerge — outcome audits, incident tracking, and a live channel for that
data to actually update governance policy — rather than treating the
initial approval and guideline-writing process as a one-time task that's
"done" once completed, which is the structural difference this model is
really measuring between its lower and higher levels.

## Exercise

Score your own organization (or a plausible one) across the six section 1
dimensions, with a one-sentence evidence note per score. Identify the
binding constraint and state what a realistic one-level improvement there
would require.
