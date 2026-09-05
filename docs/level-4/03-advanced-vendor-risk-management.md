# 03 · Advanced Vendor Risk Management for AI Tools

Level 3 Module 3 covered evaluating a single vendor. At organizational
scale, the challenge shifts to managing risk across a portfolio of
vendors over time, including risks that only appear after the contract is
signed.

## 1. Risk categories beyond initial evaluation

| Risk category | Description | Why it's missed at initial evaluation |
|---|---|---|
| Concentration risk | Too many critical workflows depend on one vendor | Only visible when you map dependencies across the whole portfolio |
| Silent model/policy changes | Vendor changes underlying model, training data policy, or terms post-signing | Contracts rarely guarantee against this; requires ongoing monitoring |
| Fourth-party risk | Your vendor relies on subprocessors you never evaluated | Initial DPA review often stops at the primary vendor |
| Regulatory drift | New regulation applies retroactively to an existing tool's data handling | Wasn't a risk at signing; becomes one as law changes |
| Vendor viability decline | Vendor's business weakens post-signing (acquisition, funding issues) | Financial health assessed once, rarely re-checked |

## 2. A continuous vendor risk framework

| Stage | Activity | Frequency |
|---|---|---|
| Onboarding | Full evaluation (Level 3 Module 3 scorecard) plus fourth-party subprocessor list | Once, at signing |
| Monitoring | Track vendor terms-of-service changes, security disclosures, funding/ownership news | Ongoing (quarterly check minimum) |
| Periodic re-scoring | Re-run the scorecard against current terms and usage | Annually or at renewal |
| Concentration review | Map which business processes depend on which vendors | Annually, portfolio-wide |
| Incident response readiness | Confirm the org knows what to do if this vendor has a breach or outage | At onboarding and annually |

## 3. A vendor risk register (template)

| Field | Purpose |
|---|---|
| Vendor name and tier | Identifies criticality |
| Data classes handled | What's actually exposed if this vendor fails |
| Subprocessors known | Fourth-party exposure |
| Last re-score date | Flags overdue reviews |
| Concentration flag | Whether this vendor is a single point of failure for a critical process |
| Owner | Who is accountable for monitoring this vendor |
| Exit plan status | Whether a documented, tested exit/migration path exists |

## 4. Common advanced-risk failure modes

| Failure mode | Consequence | Fix |
|---|---|---|
| Treating evaluation as a one-time gate | Risk profile drifts unnoticed post-signing | Institute the periodic re-scoring cadence |
| No fourth-party visibility | A subprocessor breach is discovered only after it hits the news | Require subprocessor disclosure in every DPA and track it |
| No concentration mapping | A single vendor outage takes down multiple "independent" workflows | Run the annual concentration review across the whole portfolio |
| Exit plans exist only on paper | Migration takes months longer than expected when actually needed | Test the exit/export path at least once per critical vendor, not just document it |
| Risk register not owned by anyone | Register goes stale within a year | Assign a named owner per vendor, reviewed at the same cadence as re-scoring |

## Worked example

An organization's annual concentration review reveals that three
"independent" AI tools used across customer support, sales, and internal
analytics all route through the same underlying model provider as a
subprocessor — a fact none of the three onboarding evaluations had
surfaced because each was reviewed in isolation. The risk register is
updated to flag this as a portfolio-level concentration risk, and the
governance committee (Module 2) commissions a review of whether any single
provider now represents an unacceptable single point of failure, leading
to a deliberate diversification decision for the highest-criticality
workflow.

## How It Actually Works

Concentration risk has a technical dimension beyond the contractual one:
because prompts, integrations, and fine-tuned behavior are built against
one vendor's specific API conventions and one specific model's
particular response patterns (Module 3, Level 3), an organization with
many workflows built on a single vendor has also accumulated a large body
of vendor-specific engineering work that doesn't transfer cleanly if that
vendor becomes unavailable, changes its pricing drastically, or
deprecates the model version those workflows were tuned against. This
compounds the more obvious business-continuity risk of single-vendor
dependency — it's not just "we'd need to find a replacement vendor," it's
"every prompt, integration, and staff habit built around this vendor's
specific behavior needs re-engineering," which is a materially larger and
slower undertaking than switching most other categories of SaaS vendor.

Model deprecation and silent version changes — a risk category that's
largely unique to this vendor category — deserve explicit ongoing
monitoring because providers routinely retire older model versions or
quietly update a "stable" endpoint's underlying weights as part of normal
product maintenance, and either event can change output behavior on
workflows that were validated and approved against a specific version's
characteristics. A vendor risk framework built for conventional software
(where the underlying logic mostly only changes via an explicit, versioned
release you opt into) misses this category of risk entirely unless
adapted for it — which is exactly the adaptation "advanced" vendor risk
management for AI tools, as distinct from generic vendor risk management,
actually has to add.

## Exercise

Build a vendor risk register (section 3 template) for 3-5 real or
plausible AI vendors your organization might use. For each, note whether a
fourth-party subprocessor list exists and whether a concentration risk
appears once you look across all of them together.
