---
title: "Final Quiz"
description: "Test what you have learned across all four levels of AI Tools Mastery Path with a 20-question final quiz."
---

# Final Quiz

20 questions drawn from all four levels of this course. You need **70% (14 out of 20)** to pass —
you can retake it as many times as you like. Your best result is saved in this browser.

<div id="mp-quiz-root"></div>

<script type="application/json" id="mp-quiz-data">
[
  {
    "question": "You need a one-off brainstorm of blog titles. What verification fits?",
    "options": [
      "Light: low stakes, so a quick read and pick",
      "Legal review",
      "None needed ever",
      "Trace every title to a source"
    ],
    "correctIndex": 0,
    "explanation": "Stakes determine verification effort."
  },
  {
    "question": "An AI summary says '73.2% of firms report X' with no source. What do you do?",
    "options": [
      "Use it",
      "Round it",
      "Treat it as a hallucination red flag and trace it to a primary source before using it",
      "Cite the AI"
    ],
    "correctIndex": 2,
    "explanation": "Oddly specific numbers without sources are a classic sign."
  },
  {
    "question": "You must research a topic accurately. What's the right workflow?",
    "options": [
      "Skip gathering",
      "Ask the AI to recall facts and cite them",
      "Ask twice",
      "Scope, gather primary sources yourself, have AI synthesise those sources, then verify claims against originals"
    ],
    "correctIndex": 3,
    "explanation": "AI is an accelerant for supplied text, an unreliable oracle for recalled facts."
  },
  {
    "question": "A support lead wants to paste customer account numbers into a free chat tool. What's your answer?",
    "options": [
      "Fine, it's quick",
      "Fine if anonymised by hand",
      "No: regulated/PII data needs a tool specifically approved for it; check the data policy and tier first",
      "Fine on weekends"
    ],
    "correctIndex": 2,
    "explanation": "Free tiers usually have weaker protections."
  },
  {
    "question": "Someone pastes an API key into an AI tool 'just to debug'. What's the rule?",
    "options": [
      "Fine if rotated yearly",
      "Credentials and secrets never go into AI tools, no exception",
      "Fine if it's a test key",
      "Fine in private chats"
    ],
    "correctIndex": 1,
    "explanation": "Classify data before pasting."
  },
  {
    "question": "An automation drafts and sends customer emails with no human step. What's the problem?",
    "options": [
      "A terminal AI step triggering an irreversible external action: add human review (and a fallback for low-confidence output)",
      "Nothing",
      "Too slow",
      "Too many emails"
    ],
    "correctIndex": 0,
    "explanation": "Automation errors reach customers directly."
  },
  {
    "question": "A tool saves 30 minutes drafting a report but you spend 25 checking it. What's the honest benefit?",
    "options": [
      "About 5 minutes net: always net out verification time",
      "55 minutes",
      "30 minutes",
      "25 minutes"
    ],
    "correctIndex": 0,
    "explanation": "The honest number is the difference."
  },
  {
    "question": "Which is the best way to compare two tools for recurring work?",
    "options": [
      "Run the same 5–10 real tasks from your work through both and score fixed dimensions",
      "Pick the one that felt smarter",
      "Pick the newest",
      "Ask a colleague"
    ],
    "correctIndex": 0,
    "explanation": "Vibes don't hold up when the task set changes."
  },
  {
    "question": "A chain of tools produces a wrong final figure. Which design lapse is likely?",
    "options": [
      "The final tool was too fast",
      "Missing verification checkpoints: an early error compounded silently down the chain",
      "Too many tools",
      "Wrong colour"
    ],
    "correctIndex": 1,
    "explanation": "Place checkpoints after steps whose errors cost most downstream."
  },
  {
    "question": "A team pilot is declared a success because everyone's excited. What was missing?",
    "options": [
      "A longer demo",
      "A bigger team",
      "More enthusiasm",
      "Success criteria defined in writing beforehand, and evaluation against them rather than enthusiasm"
    ],
    "correctIndex": 3,
    "explanation": "Time-box the pilot and evaluate honestly."
  },
  {
    "question": "A vendor's marketing page claims no training on your data, but the contract says otherwise. Which governs?",
    "options": [
      "The salesperson",
      "The marketing page",
      "Reviews",
      "The contract: verify data/security terms against the actual agreement (DPA), not marketing"
    ],
    "correctIndex": 3,
    "explanation": "Contractual terms are what bind."
  },
  {
    "question": "Which AI integration pattern adds central logging, rate limiting and policy checks for many teams?",
    "options": [
      "Plugins only",
      "A middleware/gateway layer",
      "Embedded widgets",
      "Direct API calls in each app"
    ],
    "correctIndex": 1,
    "explanation": "A gateway also lets you swap providers later."
  },
  {
    "question": "Adoption of a licensed tool is 15% after six months despite access for all. What's the likely gap?",
    "options": [
      "More licences",
      "Training: access alone doesn't work; use tiered, role-specific training and measure adoption",
      "A new logo",
      "Cheaper pricing"
    ],
    "correctIndex": 1,
    "explanation": "Most people use 10–20% of capability unaided."
  },
  {
    "question": "A guideline document is 40 pages and ignored. What's the fix?",
    "options": [
      "Make it longer",
      "Email it again",
      "Remove it",
      "A one-page quick reference plus detail doc, with compliant/non-compliant examples and a named owner"
    ],
    "correctIndex": 3,
    "explanation": "Keep guidelines usable, not just complete."
  },
  {
    "question": "Which approval path fits a single-user, low-spend, no-sensitive-data tool?",
    "options": [
      "Full committee review",
      "Tier 1: self-serve from a pre-approved catalog",
      "Legal deep dive",
      "Ban it"
    ],
    "correctIndex": 1,
    "explanation": "Tiered by spend and risk to avoid bottlenecks."
  },
  {
    "question": "Rolling out AI to hiring screens: which control is mandatory?",
    "options": [
      "Human-in-the-loop with an impact assessment and bias audits, since it's a high-stakes decision",
      "Nothing",
      "Spot checks only",
      "Standard governance only"
    ],
    "correctIndex": 0,
    "explanation": "Aggregate bias can compound across many decisions."
  },
  {
    "question": "Your org scored: governance L3, adoption L3, measurement L1. What's the binding constraint and what should you do?",
    "options": [
      "Adoption",
      "Measurement is the binding constraint: advance it one level rather than averaging scores",
      "Aim for level 4 everywhere",
      "Governance"
    ],
    "correctIndex": 1,
    "explanation": "The lowest dimension usually limits overall maturity."
  },
  {
    "question": "A pilot team succeeded, and a manager wants to roll out to 20 teams next week. What's the risk?",
    "options": [
      "None",
      "Skipping systematisation: without a repeatable rollout kit it depends on people who can't be everywhere",
      "Too cheap",
      "Too fast to measure"
    ],
    "correctIndex": 1,
    "explanation": "Prove, systematise, scale, sustain."
  },
  {
    "question": "A strategy names three specific vendors throughout. Why is that fragile?",
    "options": [
      "It's fine",
      "It's illegal",
      "It's too long",
      "Vendors change frequently; write policy in vendor-agnostic risk and process terms and keep exit rights"
    ],
    "correctIndex": 3,
    "explanation": "Fast-changing items should be inputs, not baked in."
  },
  {
    "question": "Which signals say an AI Centre of Excellence is warranted?",
    "options": [
      "No sponsor",
      "One team piloting",
      "Multiple teams solving the same problems, a governance committee swamped by repeat questions, no organic knowledge sharing",
      "Small organisation"
    ],
    "correctIndex": 2,
    "explanation": "Too early means overhead with no constituency."
  }
]
</script>
