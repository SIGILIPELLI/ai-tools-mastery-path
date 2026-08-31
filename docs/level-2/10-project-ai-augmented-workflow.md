# 10 · Project — Design an AI-Augmented Personal Workflow

This capstone project for Level 2 asks you to apply everything from
modules 1-9 to design, build, and run one real, complete AI-augmented
workflow for a task you actually do — not a hypothetical exercise.

## 1. Project requirements

| Requirement | What it means |
|---|---|
| Real task | Choose a task you genuinely do at least weekly, not an invented example |
| Tool comparison | Apply the Module 1 framework to justify your tool choice(s), even briefly |
| Multi-step design | Design it as a workflow with distinct stages (Module 2), not a single prompt |
| Data check | Classify the sensitivity of any data involved and confirm the tool fits (Module 6) |
| Review checkpoint | Include an explicit human review step before any output is used or sent (Module 8) |
| Cost-benefit estimate | Estimate time/cost saved versus tool cost and verification overhead (Module 7) |
| Documented failure mode | Identify at least one way this workflow could go wrong and what would catch it |

## 2. Suggested project structure

| Section | Content |
|---|---|
| 1. Task definition | One paragraph: what the task is, how often it recurs, and current (pre-AI) time/cost |
| 2. Tool selection | Which tool(s) you chose, and the comparison that justified it |
| 3. Workflow design | A step-by-step diagram or table: trigger → stages → review checkpoint → output |
| 4. Data handling | Sensitivity classification of inputs and confirmation the chosen tool is appropriate |
| 5. Cost-benefit estimate | Baseline cost, new cost including tool and verification time, net benefit |
| 6. Risk and mitigation | The most likely failure mode and the check that catches it |
| 7. Trial results | After running it for at least one real cycle: what worked, what you'd change |

## 3. Evaluation rubric

| Dimension | Weak | Strong |
|---|---|---|
| Task reality | Hypothetical or overly simple example | A real, recurring task with real stakes |
| Tool justification | "I picked the one I already use" | A comparison against at least one alternative, even brief |
| Workflow structure | A single undifferentiated prompt | Clear distinct stages with a defined review checkpoint |
| Data handling | Not addressed | Sensitivity classified and matched to an appropriate tool tier |
| Cost-benefit | Vague impression ("it feels faster") | An actual estimate with numbers, even rough ones |
| Risk awareness | Not addressed, or addressed only in the abstract | A specific, plausible failure mode with a concrete catch mechanism |

## 4. Common project mistakes

| Mistake | Fix |
|---|---|
| Choosing a task too trivial to show meaningful design decisions | Pick something with at least one place review or data-handling actually matters |
| Skipping the trial run and only describing the design | Actually run it once; note what you learn — designs always look better on paper than in practice |
| Treating "review checkpoint" as a formality rather than a real check | Describe specifically what you check for, not just that a check exists |
| Ignoring the cost-benefit section because the numbers are "obviously good" | Write the numbers down anyway — the discipline of estimating is the point |

## Worked example

A graduate student designs a workflow for turning weekly lab notes into a
structured research log entry. Task: recurring weekly, currently taking
40 minutes of manual formatting. Tool selection: compares a general chat
assistant against a note-specific AI tool using the Module 1 framework,
picks the general assistant since her lab notes format is simple and
idiosyncratic. Workflow: raw notes → AI structures into the lab's required
template → she reviews for accuracy against her actual bench observations
→ appends to the shared log. Data check: notes contain no regulated data,
low sensitivity, any reputable tool is fine. Cost-benefit: new process
takes about 15 minutes including review, saving 25 minutes weekly against
a free tool. Risk: AI might infer a result she didn't actually observe;
her review step specifically checks every stated result against her raw
notes before appending.

## Exercise

Complete the project using the structure in section 2. Run your designed
workflow for at least one real cycle before submitting, and include what
you'd change based on that trial — a workflow that survives contact with
real use is worth more than one that only looks good in the design
document.
