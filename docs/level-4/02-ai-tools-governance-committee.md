# 02 · Building an AI Tools Governance Committee

A strategy (Module 1) needs a body that actually operates it day to day.
This module covers how to structure a governance committee that makes
real decisions without becoming a bottleneck.

## 1. Who belongs on the committee

| Role | Contribution | Risk if missing |
|---|---|---|
| Security/IT | Assesses data handling, access, integration risk | Tools approved with unreviewed data exposure |
| Legal/compliance | Reviews contracts, DPAs, regulatory exposure | Signed terms nobody vetted |
| Finance | Tracks spend, ROI, renewal terms | Uncontrolled proliferation of paid seats |
| A representative end-user function | Grounds decisions in real workflow needs | Guardrails that block legitimate, valuable use |
| An executive sponsor | Gives the committee authority to act | Recommendations that get ignored |

A committee missing the end-user voice tends to produce guardrails that
are technically sound but unusable; a committee missing security or legal
tends to approve tools that later cause an incident.

## 2. Committee operating model

| Element | Design choice | Reasoning |
|---|---|---|
| Meeting cadence | Regular (e.g., biweekly) plus an expedited path | Regular cadence handles routine reviews; expedited path prevents urgent requests from waiting weeks |
| Decision thresholds | Tiered by spend/risk (e.g., auto-approve under $X, committee review above) | Keeps low-risk decisions fast, reserves committee time for real risk |
| Documentation | Every decision logged with rationale | Enables future re-evaluation and audit |
| Escalation path | Clear route for disagreement (e.g., to the executive sponsor) | Prevents deadlock from stalling all decisions |
| Sunset/review clause | Every approval has a review date | Prevents "approved forever" tools from evading later scrutiny |

## 3. A tiered approval framework

| Tier | Criteria | Approval path | Typical turnaround |
|---|---|---|---|
| Tier 1 | Low spend, no sensitive data, single-user | Self-serve from a pre-approved catalog | Immediate |
| Tier 2 | Team-level tool, moderate spend, internal data only | Manager + governance checklist sign-off | Days |
| Tier 3 | Org-wide or high spend, or touches regulated/customer data | Full committee review | Weeks |
| Tier 4 | Novel use case, unclear risk category | Committee review plus legal/security deep dive | Weeks to a month |

## 4. Common governance failure modes

| Failure mode | Symptom | Fix |
|---|---|---|
| Committee reviews everything at the same depth | Chronic backlog, shadow adoption to bypass it | Adopt the tiered model above |
| No documented rationale | Same debates repeat every renewal | Require a rationale log entry per decision |
| No end-user representation | Guardrails technically correct but ignored in practice | Add a rotating end-user seat |
| No expedited path | Urgent, legitimate requests wait for the regular cycle | Define and empower an expedited track with a lower quorum |
| Approvals never expire | Risk profile of an old tool goes unreviewed for years | Attach a mandatory review date to every approval |

## Worked example

A governance committee initially reviews every tool request at full depth,
producing a six-week backlog and driving teams to adopt tools without
asking. After adopting the tiered framework, 70% of requests (low-spend,
non-sensitive) are self-served against a pre-approved catalog immediately;
only the remaining 30% reach the committee, and an expedited two-day track
is added for time-sensitive Tier 3 requests. Backlog clears within a
quarter, and shadow adoption — measured via a follow-up inventory —
drops sharply because the sanctioned path is now faster than going around
it.

## How It Actually Works

Security/IT's seat on the committee exists because data-handling risk is
determined by account-tier contract terms and system architecture — where
requests are logged, whether retention is configurable, whether a
retrieval pipeline touches a sensitive internal document store — details
that are invisible from inside a product's user interface and only
assessable by someone who reviews the actual technical integration and
contract (Module 3, Level 3). Legal/compliance's seat exists for the
adjacent but distinct reason that a signed DPA is the only enforceable
constraint on what a vendor actually does with submitted data (Module 3
again) — a committee without either seat is approving tools based on
product demos and marketing claims, neither of which carries any
contractual or technical weight.

A less obvious but equally important seat is someone who understands the
mechanism well enough to evaluate whether a proposed use case sits in the
technology's reliable zone or its unreliable one — grounded generation
from supplied data versus unaided recall, a well-represented task versus a
rare edge case, a use case with a built-in verification loop (agentic
tool-use checking its own output against real feedback) versus one with
no check at all. Without this kind of technical literacy on the
committee, approval decisions default to evaluating tools by vendor
reputation or feature-list marketing rather than by the actual structural
risk of the specific use case being proposed — which is precisely the
gap this whole program has been building the vocabulary to close, and
exactly the gap a governance committee lacking that literacy will
predictably fall into.

## Exercise

Design a governance committee charter for a real or plausible
organization: name the roles from section 1, define at least three
approval tiers with concrete thresholds, and specify the escalation and
review-date rules from sections 2-3.
