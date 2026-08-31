# 01 · Comparing AI Tools Systematically

Level 1 taught you to pick a reasonable tool for a task. This module builds
the habit of comparing tools rigorously when the choice actually matters —
when you're about to commit real time, money, or workflow dependency to
one option over another. Casual choices don't need this. Recurring or
expensive ones do.

## 1. Why ad-hoc comparison fails

Most people compare tools by vibes: which one "felt" smarter in a quick
test, which one a colleague mentioned, which one showed up first in a
search. This produces decisions that don't hold up once the task set
changes, and it leaves you unable to explain the choice later — to a
teammate, a manager, or your future self re-evaluating in six months.

## 2. A durable comparison framework

| Dimension | Question to answer | Why it matters |
|---|---|---|
| Fit for task | Does it handle your actual, specific use cases — not the generic demo case? | Generic capability doesn't guarantee task-specific quality |
| Output quality | Across 5-10 real prompts from your own work, how good and how consistent is the output? | One good answer isn't a pattern; consistency is |
| Integration | Does it fit your existing tools (files, browser, IDE, chat apps) without extra friction? | A better tool you won't actually use loses to a good-enough tool you will |
| Cost structure | Free tier limits, per-seat pricing, usage-based pricing — modeled against your real usage volume | Costs that look small per-query can compound fast at real volume |
| Data handling | What happens to your inputs — training use, retention, sharing? | Determines what you can safely put into the tool at all (Module 6) |
| Learning curve | How long until a typical user is productive, not just an expert? | A powerful tool with a steep curve may lose to a simpler one for a team |
| Switching cost | How hard is it to leave later — export formats, lock-in, embedded workflows? | Cheap to switch now can prevent an expensive trap later |

## 3. Running a structured comparison

| Step | Action |
|---|---|
| 1. Define the task set | Pick 5-10 real examples from your actual work, not invented demo prompts |
| 2. Run the same task set through each candidate tool | Identical inputs — this is the only way outputs are comparable |
| 3. Score each dimension from section 2 | Use a simple 1-5 scale per dimension per tool; don't skip the ones that feel "obviously fine" |
| 4. Weight the dimensions | Not all dimensions matter equally for your case — decide weights before scoring, not after |
| 5. Compute and sanity-check | If the winner surprises you, re-examine your weights and scores rather than overriding the result on instinct |

## 4. Common scoring traps

| Trap | What happens | Fix |
|---|---|---|
| Recency bias | The tool you tried most recently scores better because it's fresh in memory | Re-run all tools in the same session, back to back |
| Demo bias | Vendor-provided example prompts make every tool look great | Only score against your own task set |
| Single-run luck | One great or one bad output skews the whole score | Run each task 2-3 times and average, especially for anything with randomness |
| Feature-list bias | Counting features instead of testing whether you'd use them | Score only capabilities relevant to your defined task set |

## Worked example

A freelance editor is deciding between two AI writing-assistant tools for
client work. Instead of picking based on a demo, she assembles eight real
excerpts from recent client drafts spanning different tones (technical,
casual, marketing). She runs all eight through both tools, scores each on
output quality, consistency, and turnaround time using a 1-5 scale, and
weights output quality double since that's what clients actually notice.
Tool A wins on quality but has a per-word cost that, modeled against her
actual monthly volume, is triple Tool B's flat subscription. She picks
Tool B for routine work and keeps Tool A for the small number of
high-stakes, quality-critical projects — a split decision the ad-hoc
approach would never have surfaced.

## Exercise

Pick two AI tools that could plausibly serve the same purpose in your own
work (e.g., two chat assistants, two image generators, two automation
platforms). Assemble a task set of five real examples from your own
recent work. Score both tools on the seven dimensions in section 2 using
a 1-5 scale, assign weights that reflect what actually matters to you, and
compute a final score. Write one sentence explaining any place the result
surprised you.
