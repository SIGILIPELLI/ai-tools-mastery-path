# 02 · Building Internal AI Tool Guidelines

A guideline document turns individual judgment calls (Level 2) into a
shared standard a team can actually follow consistently. This module
covers what belongs in one and how to keep it usable rather than a policy
nobody reads.

## 1. What a guideline document must answer

| Question | Why it must be explicit |
|---|---|
| Which tools are approved, for which purposes? | Prevents ad-hoc adoption of tools with unvetted data terms |
| What data classes may and may not be input? | Directly extends the Level 2 data classification to a team-shared standard |
| What requires human review before use externally? | Prevents unreviewed AI output from reaching customers or the public |
| Who approves a new tool request, and how? | Without a clear path, people either wait indefinitely or go around the policy |
| What's the consequence of a violation, and is it enforced consistently? | An unenforced policy is worse than no policy — it creates false confidence |

## 2. A guideline document skeleton

| Section | Content |
|---|---|
| Purpose | One paragraph: why this exists and what it protects |
| Approved tools list | Tool, approved use cases, approved data classes, tier required |
| Data handling rules | Extension of Level 2's classification, made mandatory rather than advisory |
| Review requirements | What output requires human review before use, by task type |
| Request process | How to propose a new tool or use case |
| Incident process | What to do if sensitive data was input incorrectly, or bad AI output was published |
| Review cadence | When this document itself gets revisited |

## 3. Keeping guidelines usable, not just complete

| Anti-pattern | Fix |
|---|---|
| A 40-page policy no one reads | A one-page quick-reference plus a longer detail doc for edge cases |
| Guidelines that lag actual tool capability by a year | Set a mandatory revisit cadence (quarterly is reasonable) |
| Rules with no examples | Pair every rule with one concrete example of compliant and non-compliant use |
| A document owned by no one | Name a specific owner responsible for updates and questions |

## 4. Calibrating strictness to risk

| Context | Appropriate strictness |
|---|---|
| Internal brainstorming, low-stakes drafts | Light guidance, mostly about data classification |
| Customer-facing communication | Mandatory human review before send, every time |
| Regulated industries (health, finance, legal) | Formal sign-off process, possibly restricted tool list, audit trail |
| Code that ships to production | Mandatory review process matching existing code review standards, not a lighter bar just because AI wrote it |

## 5. Common pitfalls

| Pitfall | Symptom | Fix |
|---|---|---|
| Copy-pasting a generic policy template | Doesn't match the team's actual tools or workflows | Base it on Module 1's pilot findings and real usage patterns |
| Treating the guideline as a one-time deliverable | Goes stale as tools and team practices evolve | Bake in the review cadence from section 2 and actually honor it |
| No enforcement mechanism | Guidelines become optional in practice | Tie compliance to existing review processes (code review, publishing sign-off) rather than a separate honor system |
| Overly restrictive default | Blocks legitimate low-risk use, driving people to unofficial/unapproved tools ("shadow AI") | Calibrate strictness by actual risk (section 4), not blanket caution |

## Worked example

A mid-size marketing team writes its first AI tool guideline after an
incident where a contractor pasted an unreleased campaign brief into a
free consumer chat tool. The resulting one-page document: an approved
tools list with required tiers, a rule that any customer-facing copy
needs human sign-off before publishing, a simple request form for new
tool proposals, and a named owner (the marketing ops lead) responsible for
quarterly review. They pair the data-handling rule with two concrete
examples — one compliant, one not — because the first draft's abstract
wording had been ambiguous to several team members in testing.

## Exercise

Draft a one-page AI tool guideline for a team you're part of (or a
hypothetical one matching your actual work), using the skeleton in
section 2. Include at least one concrete compliant/non-compliant example
pair for the data handling rule, and name a specific owner and review
cadence.
