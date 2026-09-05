# 05 · AI for Coding Assistance

You don't need to be a programmer to understand this module — it's written
for anyone who might use an AI tool to write, fix, or understand code,
including complete beginners building a first small script or webpage. The
category of "AI coding assistant" covers several genuinely different modes
of help, and knowing which mode you're in changes what to expect and how to
check the result.

## 1. The three general modes of coding assistance

| Mode | What it does | Best fit |
|---|---|---|
| **Autocomplete-style** | Suggests the next few lines as you type, inline in an editor | Experienced coders who can quickly judge and accept/reject suggestions |
| **Chat-based** | You describe a problem or paste code; it responds with an explanation, fix, or new code in a conversation | Debugging, learning, one-off scripts, explaining unfamiliar code |
| **Agentic** | The tool can read multiple files, make edits across a project, and run commands somewhat autonomously toward a goal you describe | Larger, multi-step coding tasks; requires more oversight since it takes more independent action |

A beginner writing a first script will usually get the most value from
chat-based help, since it explains reasoning along the way. Agentic tools
are powerful but amplify mistakes faster if you can't yet read the code
well enough to catch a bad edit.

## 2. What these tools are generally good at

| Strength | Why |
|---|---|
| Explaining existing code | Reading and summarizing code is a strong general capability |
| Writing small, well-specified functions | Clear spec in, clear code out — the easiest case |
| Translating code between languages | Pattern-matching across syntaxes is a strong fit |
| Generating boilerplate | Repetitive, well-established patterns (setup code, common structures) |
| Suggesting likely causes of an error message | Broad exposure to common error patterns |

## 3. Where they generally struggle

| Weakness | Practical implication |
|---|---|
| Correctness on non-trivial logic | Code that *runs* is not the same as code that's *correct* — test it |
| Security-sensitive code | Don't trust AI-generated code handling passwords, payments, or user data without a knowledgeable review |
| Understanding your full project context | Chat-based tools without direct file access may miss constraints elsewhere in your codebase |
| Outdated library/API knowledge | Fast-moving libraries change; verify a suggested method or package still exists and works as described |
| Silent over-confidence on bugs | It will usually offer a fix even when it hasn't actually diagnosed the real cause — test the fix, don't just accept the explanation |

## 4. A verification checklist before trusting AI-generated code

| Check | Why it matters |
|---|---|
| Did you run it? | Code that looks right can still fail to execute at all |
| Did you test it against a case you know the answer to? | Confirms actual correctness, not just plausible appearance |
| Do you understand what it does, at least at a high level? | If you can't explain it, you can't debug or maintain it later |
| Does it touch sensitive data, money, or security? | If yes, get a knowledgeable human review regardless of how confident the tool sounded |
| Is any library or API it used one you can verify still exists? | Guards against confidently invented package names or outdated methods |

## Worked example

A small-business owner with no coding background wants a script to rename a
folder of invoice files consistently. She uses a chat-based coding
assistant, describing exactly what she wants in plain language. The tool
produces a short script and explains each line. Following the checklist:
she runs it on a *copied test folder* first (not her real invoices),
confirms the files renamed correctly, and only then runs it on the real
folder. When one edge case (a file with no extension) broke the script, she
described the failure back to the tool, got a corrected version, and tested
that one too before trusting it — never running an untested version on data
she couldn't afford to lose.

## How It Actually Works

Coding assistants use the same next-token-prediction transformer as chat
assistants, trained on a corpus weighted heavily toward source code,
documentation, and forums like Stack Overflow — which is why they're
fluent in common patterns and idioms but shakier on anything rare or
project-specific. The three modes map to three different amounts of
*context* the model is given before it generates:

Autocomplete-style suggestion typically only sees the current file (or a
small window around your cursor) plus perhaps a few related files the tool
guesses are relevant — it's predicting "what code plausibly comes next
here" the same way a chat model predicts the next word, with no real
understanding of your whole codebase's architecture or business rules.
Chat-style code explanation and generation gets a larger context: the
files you've opened or pasted in, sometimes a summary of your repo
structure. It can reason more, but everything it says about your code is
still bounded by what fits in its context window — ask about a file it was
never shown and it will guess, often confidently and wrong. Agentic coding
tools add a loop on top of the same model: it can call functions to read
files, run a linter or test suite, see the (real, factual) output, and
generate its next step based on that output — which is precisely why
agentic tools catch more of their own mistakes than plain chat-based
suggestion. The model isn't smarter in agent mode; it's been given tools to
check its own work against ground truth instead of only against its
internal sense of what "looks right."

This is also why AI-generated code can look syntactically perfect while
being subtly wrong: the model is pattern-matching against code that
*looks like* correct code for this kind of task, not executing your logic
or reasoning about your specific data step by step the way a compiler or
interpreter does — which is exactly why running the result is
non-negotiable, not optional caution.

## Exercise

Think of one small, well-defined task an AI coding assistant could plausibly
help with (a script, a formula, a simple webpage element) — it's fine if
you're a complete beginner. Describe the task to an AI tool of your choice,
get a result, and run through the five-item checklist in section 4
explicitly, writing a yes/no and one sentence for each item. If any item
comes back "no," describe what you'd need to do before trusting the result.
