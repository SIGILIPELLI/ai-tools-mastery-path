# 06 · Data Privacy & Security When Using AI Tools

Every prompt, upload, and pasted document is data leaving your control to
some degree. This module builds a durable framework for deciding what's
safe to put into an AI tool and what isn't — one that survives any
specific tool's changing terms of service.

## 1. What actually happens to your data

| Question | Why it matters |
|---|---|
| Is this input used to train future models? | Determines whether your data could resurface, in some form, to other users later |
| How long is it retained, and by whom? | Retention windows and third-party processors both extend exposure |
| Is it processed by the vendor only, or shared with sub-processors? | More hops means more parties with access and more potential failure points |
| Does an enterprise/business tier change these defaults? | Many vendors do not train on paid/business-tier data by default — but "default" isn't the same as "guaranteed," read the actual terms |
| Where is data stored/processed geographically? | Matters for regulatory compliance (e.g., data residency requirements) |

Never assume; check the specific tool's current data-handling terms before
sending anything sensitive, and re-check periodically since terms change.

## 2. A data sensitivity classification

| Class | Examples | AI tool default |
|---|---|---|
| Public | Published content, marketing copy, public docs | Generally safe with any tool |
| Internal, low-sensitivity | Draft internal docs, non-confidential process notes | Safe with reputable tools under a no-training policy |
| Confidential | Financial figures, strategy, unreleased product details | Only with vetted enterprise-tier tools under contract terms; never free consumer tiers |
| Regulated/PII | Health records, SSNs, financial account data, biometric data | Only with tools specifically compliant for that data class (e.g., BAA-covered for health data), and often not at all |
| Credentials/secrets | Passwords, API keys, tokens | Never — no exception |

## 3. A pre-input checklist

| Check | Action if it fails |
|---|---|
| Do I know this tool's data retention/training policy? | Look it up before pasting; don't assume based on the vendor's reputation alone |
| Is this the free/consumer tier or the enterprise/business tier? | Free tiers usually have weaker data guarantees — downgrade what you're willing to input accordingly |
| Does this input contain regulated data (health, financial, biometric, government ID)? | Do not input it unless the tool has explicit, contracted compliance for that data class |
| Does this input contain someone else's private information, not just my own? | Get consent or redact before inputting third-party personal data |
| Could this input alone, or combined with other public info, identify a specific person? | Redact identifying details even from otherwise-low-sensitivity text |

## 4. Practical mitigations

| Technique | How it helps |
|---|---|
| Redaction before input | Replace names, account numbers, and identifiers with placeholders before pasting |
| Use enterprise/business tiers for work data | These typically carry contractual no-training and data-handling guarantees consumer tiers don't |
| Local/offline models for the most sensitive work | Removes the network transmission risk entirely, at a capability cost |
| Least-privilege tool access | Don't grant an AI browser/agent tool more account or file access than the task requires |
| Periodic policy re-check | Vendor data policies change; re-verify at least twice a year for tools you use regularly |

## 5. Common pitfalls

| Pitfall | Why it happens | Fix |
|---|---|---|
| Pasting a full document to summarize "just the top section" | Assuming the tool only sees what it responds about | Redact or trim the input itself, not just the ask |
| Trusting a screenshot doesn't count as data input | Vision-capable tools process image content the same as text | Treat images with sensitive content the same as sensitive text |
| Assuming "it's just for a quick check" lowers the risk bar | Retention/training policies don't care about your intent | Apply the same classification rules regardless of how minor the use feels |
| Confusing "the vendor is reputable" with "this specific tier has strong data terms" | Reputation and contractual guarantees are different things | Always check the terms for the specific tier you're actually using |

## Worked example

An HR coordinator wants AI help drafting a performance review summary from
her notes. Her notes contain the employee's name, salary figure, and a
health-related accommodation detail. Running the sensitivity
classification, salary and health information fall into confidential/
regulated territory. Rather than pasting the raw notes into a general
consumer AI chat tool, she redacts the name and health detail, replaces
the salary with a placeholder range, drafts the generic structure with AI,
and manually reinserts the specific figures into the final document
herself — getting the drafting speedup without exposing regulated data.

## How It Actually Works

What "training on your data" technically means matters for evaluating this
risk honestly. Training a model means adjusting the billions of numeric
weights in its neural network so that, in aggregate across enormous amounts
of text, its next-token predictions get statistically better. Your specific
input, if included in a training run, becomes one of an enormous number of
examples nudging those weights very slightly — it is not stored anywhere
as a retrievable file, and in the overwhelming majority of cases could not
be extracted verbatim afterward, because training compresses patterns
across the whole dataset rather than memorizing individual documents.
That said, memorization is not theoretically impossible: text that is
highly repeated, distinctive, or appears with very little surrounding
variation across a training corpus can occasionally be reproduced close to
verbatim by a trained model — which is the real, if narrow, technical basis
behind "could my data resurface" concerns, distinct from vaguer fears about
the model somehow "remembering" everything it was ever shown.

Separately, and more immediately relevant day to day, is inference-time
data handling — what happens to a specific message the moment you send
it, regardless of whether it's ever used for training. That message
typically transits the vendor's servers, may be logged for abuse
monitoring or debugging, and may be retained for some contractual period
even where the vendor states "not used for training." This is a data
handling and retention question, governed by a provider's terms of service
and (where applicable) contractual agreements — not a fact about the
model's architecture — which is exactly why a durable privacy habit
("never paste this class of data into this class of tool") has to be
based on what a vendor's contract actually commits to, not on the vendor's
"how the AI works" marketing copy.

## Exercise

Take a real piece of text you might otherwise paste into an AI tool.
Classify it using the section 2 table, run it through the section 3
checklist, and write down what — if anything — you'd need to redact or
change about which tool you use before it's actually safe to input.
