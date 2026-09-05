# 08 · Future-Proofing an AI Tool Strategy

Everything built so far — strategy, governance, vendor management, CoE —
risks becoming obsolete as the tool landscape shifts. This module covers
designing for change rather than for the current tool generation.

## 1. What tends to change (and what doesn't)

| Changes frequently | Changes slowly |
|---|---|
| Specific vendors and products | The categories of risk (data exposure, bias, vendor lock-in) |
| Underlying model capabilities and pricing | The need for human accountability on consequential decisions |
| Which tasks AI can reliably do well | The value of a documented, evidence-based evaluation process |
| Regulatory specifics | The general direction of increasing scrutiny on automated decisions |

A durable strategy is written in terms of the slow-changing column —
principles and processes — with the fast-changing column treated as
inputs that get re-evaluated regularly, not baked into the strategy
itself.

## 2. Designing for change

| Principle | Application |
|---|---|
| Vendor-agnostic policy language | Guardrails and governance describe risk categories and data classes, not named products |
| Modular tool architecture | Favor integration patterns that allow swapping a tool without rearchitecting workflows |
| Contractual exit rights | Every vendor contract preserves a real, tested path to migrate away |
| Built-in review cadence | Strategy, governance thresholds, and vendor risk are all reassessed on a fixed schedule (Modules 1, 3, 6) |
| Capability-based workforce training | Train people on underlying skills (prompt evaluation, critical review of AI output) rather than one tool's specific UI |
| Scenario planning | Periodically ask "what if this capability got 10x better/cheaper" or "what if this vendor disappeared" |

## 3. A future-proofing review checklist

| Check | Frequency |
|---|---|
| Does any policy language name a specific vendor unnecessarily? | Annual policy review |
| Can we actually execute our documented exit plan for each critical vendor? | Annual, tested for at least one vendor per cycle |
| Has a new capability emerged that changes our risk tiering (Module 5) assumptions? | Ongoing, flagged at quarterly governance review |
| Is training still tied to a specific tool's interface rather than transferable skill? | Reviewed at each training refresh |
| Has regulation changed in a way that affects existing approvals? | Ongoing legal monitoring, reviewed quarterly |

## 4. Common future-proofing failure modes

| Failure mode | Consequence | Fix |
|---|---|---|
| Policy hard-codes a specific vendor's name | Policy needs a rewrite every vendor change | Write in terms of risk categories and data classes |
| No tested exit plan | Migration takes far longer than planned when actually triggered | Test exits proactively, not only when forced |
| Training tied to one tool's UI | Retraining cost spikes on any tool change | Teach transferable evaluation and critical-review skills |
| Strategy treated as finished once written | Strategy silently drifts out of date | Enforce the review cadence from Module 1 |
| No mechanism to notice capability shifts | Organization reacts late to major landscape changes | Assign someone (or the CoE, Module 7) to actively monitor and report shifts |

## Worked example

A company's original AI policy specifically named one vendor's product in
its data-handling clause. When that vendor is acquired and its terms
change unfavorably eighteen months later, legal has to rewrite policy
language across multiple documents before any new tool can be evaluated
under it — delaying an otherwise straightforward switch by weeks. The
rewritten policy instead defines guardrails purely in terms of data
classification and risk tier, with vendor names living only in the
separate, easily updated risk register (Module 3). The next vendor change,
a year later, requires only a risk-register update, not a policy rewrite.

## How It Actually Works

The changes-quickly/changes-slowly split in this module's table holds up
because it tracks a real architectural distinction: specific vendors,
specific model versions, and specific pricing are all *implementation*
details sitting on top of a much more stable set of mechanisms — the
transformer-based generation process, its structural strengths (text
transformation grounded in supplied data, pattern-matching over
well-represented tasks) and its structural weaknesses (no built-in
truth-verification, sensitivity to training data biases, sequential,
latency-bearing token generation). A strategy built around "we use Vendor
X's Model Y" is betting on an implementation detail with a shelf life
measured in months; a strategy built around "our workflows account for the
technology's mechanistic strengths and weaknesses, and place verification
where the mechanism can't provide it" is betting on properties that have
held steady since well before this program's Level 1 and show no sign of
disappearing with the next model generation.

This is precisely why "the need for human accountability on consequential
decisions" belongs in the changes-slowly column rather than the
changes-quickly one: it isn't a stopgap measure that better models will
eventually make unnecessary — it's a structural consequence of a
mechanism, next-token prediction with no internal truth-check, that
improving model quality makes more *fluent* and convincing without
addressing the underlying architectural gap at all. A future-proof
strategy plans for that gap persisting indefinitely across model
generations, and designs verification and accountability structures
accordingly, rather than provisionally, on the assumption that "the next
version will finally fix hallucination" — which is a bet this program's
own Level 1 material already gives good reason to be skeptical of.

## Exercise

Review a real or plausible AI tool policy document. Identify any language
that names a specific vendor or tool unnecessarily, and rewrite it in
vendor-agnostic, risk-category terms using the section 2 principles.
