# 05 · Automation Platforms & AI Integration

Automation platforms (workflow/integration tools that connect apps and
trigger actions) become far more capable once an AI step is inserted —
turning rigid if-this-then-that logic into workflows that can read,
summarize, classify, and generate. This module covers how to design that
integration soundly.

## 1. What an AI step adds to automation

| Without AI step | With AI step |
|---|---|
| Route email to a folder by fixed sender rule | Classify email intent/urgency and route accordingly |
| Copy form data verbatim into a record | Extract and normalize structured fields from free-text input |
| Send a fixed template message | Generate a personalized message from variable inputs |
| Trigger only on exact keyword match | Trigger on semantic meaning ("customer sounds frustrated") |

The shift is from deterministic rules to probabilistic judgment — powerful,
but it introduces a new class of failure the platform itself won't catch.

## 2. Where AI steps fit in a workflow

| Position | Typical use | Risk profile |
|---|---|---|
| Early (classification/routing) | Decide which branch a workflow takes | Medium — a misroute is usually recoverable downstream |
| Middle (transformation) | Reformat, summarize, extract fields | Medium — errors propagate to everything after |
| Late (generation before an external action) | Draft a message, document, or response | High if the output goes out with no review — mistakes become externally visible |
| Terminal (fully autonomous send/post/execute) | AI output directly triggers an irreversible action | Highest — no human checkpoint before consequences land |

## 3. A design checklist before shipping an AI-integrated workflow

| Check | Why it matters |
|---|---|
| Is there a human review step before any externally visible or irreversible action? | AI errors in automated pipelines scale silently until someone notices |
| What happens on a malformed or low-confidence AI output? | Undefined failure paths cause workflows to silently do the wrong thing |
| Is there a fallback to a deterministic rule when AI is uncertain? | Not every case needs judgment; deterministic paths are cheaper and more reliable |
| Are inputs to the AI step logged? | Without logs, a bad outcome is nearly impossible to diagnose after the fact |
| What data is sent to the AI provider, and is that allowed under your data policy? | Automation platforms often pass more context than a single chat prompt would |
| Is there a kill switch / easy way to pause the workflow? | Automated workflows fail at scale and speed; you need to be able to stop them fast |

## 4. Common integration patterns

| Pattern | Description |
|---|---|
| Classify-then-branch | AI labels the input; deterministic rules take over from there | 
| Extract-then-validate | AI pulls structured fields; a validation step checks them against expected types/ranges before use |
| Draft-then-approve | AI generates content; a human approves or edits before it is sent |
| Summarize-then-notify | AI condenses a long input; a person is notified with the summary and a link to the source |

## 5. Common failure modes

| Failure | Cause | Fix |
|---|---|---|
| Silent drift | AI classification quality degrades over time as input patterns shift | Periodically sample and review actual classifications, not just at launch |
| Runaway automation | A terminal AI-generation step with no human gate causes a bad message to reach many recipients | Never wire AI generation directly to an irreversible send/post at high volume without a review step |
| Cost surprise | Every workflow run consumes AI usage, and volume scales with trigger frequency | Model cost against expected trigger volume before deployment, not after the first bill |
| Context leakage | Automation platforms may pass more upstream data into the AI step than intended | Explicitly define what fields are sent, don't pass whole records by default |

## Worked example

A support team automates first-response triage: incoming tickets are
classified by urgency and topic using an AI step, then routed to the right
queue with a deterministic rule. Early on, the team wired AI-drafted
replies to auto-send for "low urgency" tickets to save time. After two
drafts went out with factually wrong account details, they changed the
workflow so AI drafts always land in an agent's queue for one-click
approval rather than auto-sending — keeping the speed benefit of
drafting while removing the risk of unreviewed sends.

## Exercise

Take one recurring manual task you or your team does with an automation
platform (or would like to). Sketch the workflow with an AI step inserted
at the right position from section 2, and answer every question in the
section 3 checklist for it in writing before considering it ready to
build.
