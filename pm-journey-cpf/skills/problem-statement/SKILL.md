---
name: problem-statement
description: "Create a testable problem hypothesis using a structured template. Helps PMs articulate the target customer, problem, context, negative outcome, current workaround, and its limitations — then validate the statement against a quality checklist."
---

## Problem Statement

Craft a clear, testable problem hypothesis that anchors your Customer Problem Fit work. A good problem statement is the foundation for everything that follows — interviews, validation, and solution design.

### Domain Context

A problem hypothesis is **not** a solution. It describes a pain that exists in the world today, independent of any product you might build. The goal is to write something specific enough to test through customer discovery, yet broad enough that you don't accidentally constrain the solution space.

### Context

You are helping the user create a problem hypothesis for **$ARGUMENTS**.

If the user provides files (market research, customer feedback, prior hypotheses), read them first and incorporate relevant evidence.

### Instructions

1. **Gather initial input**

   Ask the user:
   - Who is the target customer? (role, segment, or persona)
   - What problem or pain area are you exploring?
   - What do you already know? (prior research, gut instinct, customer quotes)
   - How did you become aware of this problem?

2. **Draft the problem hypothesis** using this template:

   ```
   [Target customer] experiences [problem] when [context/trigger],
   which causes [negative outcome].
   Currently they [workaround], which fails because [limitation].
   ```

   **Example**:
   > Mid-market SaaS product managers experience difficulty prioritizing feature
   > requests when they receive conflicting input from sales, support, and
   > executives, which causes roadmap churn and missed quarterly goals.
   > Currently they use spreadsheets and gut feel to triage requests, which fails
   > because it lacks transparency and cannot scale beyond 50 open requests.

3. **Run the Validation Checklist**

   Score each criterion as Pass / Partial / Fail:

   | # | Criterion | Question | Score |
   |---|-----------|----------|-------|
   | 1 | **Observable** | Can you see this problem happening in the real world (not just imagine it)? | |
   | 2 | **Behavior-based** | Is the statement rooted in what people actually do, not what they say they'd do? | |
   | 3 | **Specific** | Is the target customer narrow enough to find and interview? | |
   | 4 | **Testable** | Could you design a 5-question interview to confirm or reject this? | |
   | 5 | **Solution-free** | Does the statement avoid prescribing how to fix the problem? | |
   | 6 | **Outcome-linked** | Is the negative outcome real and measurable (time, money, frustration)? | |
   | 7 | **Workaround exists** | Do people actively work around this today? (If not, the pain may be low.) | |

   - **7/7 Pass** — Strong hypothesis, ready to test
   - **5-6 Pass** — Promising, tighten the weak areas before testing
   - **Below 5** — Rethink the hypothesis; it may be too vague or solution-shaped

4. **Refine if needed**

   If any criterion scores Partial or Fail, suggest a revised statement that addresses the gap. Iterate until the user is satisfied.

5. **Output the final problem hypothesis** in a clean format the user can paste into a discovery brief or PRD.

### Anti-Patterns to Avoid

- **"Users need a better X"** — this is a solution, not a problem
- **"Everyone has this problem"** — if the target is everyone, it's no one
- **"Customers would love it if..."** — hypothetical desire is not a problem
- **"The problem is that we don't have feature Y"** — internal framing, not customer pain

### Output Format

```
## Problem Hypothesis

**Target Customer**: [who]
**Problem**: [what]
**Context / Trigger**: [when]
**Negative Outcome**: [so what]
**Current Workaround**: [how they cope today]
**Workaround Limitation**: [why the workaround falls short]

### Full Statement
[Target customer] experiences [problem] when [context/trigger],
which causes [negative outcome].
Currently they [workaround], which fails because [limitation].

### Validation Checklist
[Table from step 3]

### Confidence Level
[Strong / Promising / Weak] — [rationale]

### Next Steps
- Test this hypothesis through customer discovery interviews
- Identify 5-15 target customers who match this profile
- Prepare an interview script focusing on the problem area
```
