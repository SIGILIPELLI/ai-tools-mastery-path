# 07 · Data Governance for AI Tool Usage

Once a team routes real work through AI tools, the question stops being
"is this tool good" and becomes "what data are we putting into it, and
who is accountable for what comes back out." This module builds a
governance model for that.

## 1. Data flows to map before rollout

| Flow | Question to answer |
|---|---|
| Input data | What data types (customer PII, source code, financials, health data) will realistically be pasted or uploaded into the tool? |
| Retention | Does the vendor retain inputs/outputs, and for how long? Is retention configurable? |
| Training use | Can the vendor use submitted data to train models, and can that be contractually disabled? |
| Sub-processors | Does the vendor pass data to other companies (e.g., a third-party model provider)? |
| Output storage | Where do generated outputs live afterward, and who can access them? |

Skipping this mapping is the single most common governance failure: teams
approve a tool based on its capabilities and only discover the data flow
questions after an incident.

## 2. A data classification approach

| Class | Examples | AI tool policy |
|---|---|---|
| Public | Marketing copy, published docs | Any approved tool, no restrictions |
| Internal | Internal process docs, non-sensitive code | Approved tools with enterprise/no-train terms |
| Confidential | Customer data, contracts, unreleased financials | Only tools with a signed data processing agreement and no-train guarantee; consider on-prem/private-instance options |
| Regulated | Health, payment, government-restricted data | Default to prohibited unless a compliance review explicitly approves a specific tool and configuration |

Publish this table where employees can see it before they need it — this
mirrors the tiered risk classification introduced in Level 2's privacy
module, now formalized as policy rather than personal judgment.

## 3. Governance roles

| Role | Responsibility |
|---|---|
| Data owner (per system/dataset) | Decides which classification applies and approves or denies AI tool use against it |
| IT/Security | Vets vendor security posture, manages access provisioning, monitors for shadow AI use |
| Legal/Compliance | Reviews contracts, retention terms, and regulatory exposure |
| Tool champions (Level 3 Module 1) | Surface real usage patterns so policy reflects reality, not assumptions |

## 4. Handling shadow AI usage

Employees will use unapproved tools if approved ones are slow, restrictive,
or absent — this is the AI-era version of shadow IT.

| Signal | Response |
|---|---|
| Survey/anecdotal reports of unapproved tool use | Investigate what need it's filling before banning it |
| Network/DLP logs showing traffic to unapproved AI domains | Treat as a data incident review, not just a policy violation |
| Repeated requests for a specific unapproved tool | Fast-track an evaluation (Level 3 Module 3) instead of only enforcing the ban |

A pure ban without a fast, viable alternative reliably fails — the fix is
converting demand into a supported option, not just enforcement.

## 5. Incident response for AI-related data exposure

| Step | Action |
|---|---|
| Contain | Identify what was submitted, to which tool, and whether retention/training was in effect |
| Assess | Determine data classification involved and whether it triggers a breach-notification obligation |
| Remediate | Request deletion from vendor where contractually possible; revoke tool access if needed |
| Prevent recurrence | Update policy, training, or tool approval based on the root cause |

## Worked example

A product manager pastes an unreleased pricing sheet into a general-purpose
AI chat tool to reformat it, not realizing the tool's free tier retains
inputs for model training. Data governance review classifies the pricing
sheet as confidential, triggers vendor deletion request, and the incident
becomes the forcing function for publishing the classification table in
section 2 company-wide, plus provisioning an enterprise tier with no-train
terms for the whole team.

## How It Actually Works

Mapping input data flows matters mechanically because, as covered in
Module 6, anything sent to a model provider's API generally transits and
may be logged on that provider's infrastructure the moment it's
submitted — this is a property of how these services are architected (a
remote API call, not local processing) rather than a configurable setting
most end users can see or control from inside a chat interface. A
governance model that only reviews *which tools* are approved but doesn't
map *what data classes* realistically flow into them at the point of use
(customer PII typed into a support-response drafting tool, proprietary
code pasted into a public coding assistant for a quick fix) is auditing
the wrong layer — approval happens at the vendor-contract level, but real
exposure happens at the individual-request level, and those two levels can
diverge badly without a deliberate flow-mapping exercise like the one this
module describes.

Output flows deserve equal scrutiny for a related but distinct reason:
generated content can encode patterns from a model's training data in ways
that are not always obvious from the output alone — a generated image can
echo stylistic elements of training images (Module 1.6), and generated
text can reproduce phrasing patterns statistically common in training
data without any explicit citation marking that connection, which is
exactly why governance frameworks generally require a human review step
before AI-generated content is published externally, distinct from (and in
addition to) checking that its factual claims are accurate. The
"accountable for what comes back out" framing in the module's intro is
really pointing at this: because nothing in the generation mechanism itself
tracks provenance for you, an organization's accountability structure has
to supply the check the technology doesn't provide on its own.

## Exercise

Take a real (or realistic) dataset your team works with. Classify it using
the section 2 table, and write the specific AI tool policy that
classification implies — including which currently-used tools would pass
or fail that policy.
