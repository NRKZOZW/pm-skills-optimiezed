---
description: "Score a problem hypothesis against the Problem Validation Canvas — a quick CPF health check"
argument-hint: "<problem hypothesis or description>"
---

# /validate-problem -- Quick Problem Validation Scorecard

A lightweight, 5-minute workflow that takes a problem statement and produces a scored Problem Validation Canvas. Use this when you want a quick CPF health check without running the full `/run-cpf` cycle.

## Invocation

```
/validate-problem "Mid-market PMs can't prioritize feature requests when they receive conflicting stakeholder input"
/validate-problem [paste problem hypothesis]
/validate-problem                    # asks for the problem statement
```

## Workflow

### Step 1: Accept the Problem Statement

If the user provides a problem statement via `$ARGUMENTS`, use it directly. Otherwise, ask:
- What is the problem you want to validate?
- Who is the target customer?
- What evidence do you have? (interviews, observations, data, gut feel)

If the problem statement is vague, briefly suggest a sharper version using the **problem-statement** skill format before scoring.

### Step 2: Score the Problem

Apply the **problem-validation** skill:

Walk through each of the 5 dimensions and ask the user to provide evidence:

1. **Frequency** (1-5): How often does this problem occur?
2. **Intensity** (1-5): How painful is it when it happens?
3. **Willingness to Pay** (1-5): Have they spent time/money trying to solve it?
4. **Current Alternatives** (1-5): How adequate are their current workarounds?
5. **Switching Cost** (1-5): How easy would it be to adopt a new solution?

For each dimension:
- Ask the user what evidence they have
- If they have interview data, help them extract the right signals
- If they're estimating, note it as an assumption (not validated evidence)
- Assign the score and record the rationale

### Step 3: Generate the Scorecard

```
## Problem Validation Scorecard

**Problem**: [statement]
**Date**: [today]
**Evidence basis**: [interviews / assumptions / mixed]

| Dimension | Score | Evidence |
|-----------|-------|----------|
| Frequency | [1-5] | [brief evidence or assumption] |
| Intensity | [1-5] | [brief evidence or assumption] |
| Willingness to Pay | [1-5] | [brief evidence or assumption] |
| Current Alternatives | [1-5] | [brief evidence or assumption] |
| Switching Cost | [1-5] | [brief evidence or assumption] |
| **Total** | **[X/25]** | |

### Verdict: [Strong CPF / Promising / Weak / No CPF]

### Key Strengths
- [Strongest dimensions and why]

### Key Risks
- [Weakest dimensions and what to investigate]

### Evidence Gaps
- [Dimensions scored on assumptions rather than evidence]

### Recommendation
[GO / PIVOT / KILL] — [one-sentence rationale]
```

### Step 4: Suggest Next Steps

Based on the score:

- **20-25 (Strong CPF)**: "This problem scores well. Consider running `/run-cpf` for a complete assessment, or move to `/run-psf` to validate your solution."
- **15-19 (Promising)**: "There's signal here but gaps remain. I'd recommend conducting 5-10 customer interviews to strengthen the weak dimensions. Run `/run-cpf` for a guided discovery sprint."
- **10-14 (Weak)**: "The problem may not be painful enough as defined. Consider narrowing the customer segment or reframing the problem. Use `/run-cpf` to do structured discovery."
- **5-9 (No CPF)**: "This doesn't look like a problem worth solving for this segment. Consider a different problem area or a different customer segment."

## Notes

- This is a 5-minute quick check, not a substitute for real customer discovery
- If the user scores entirely on assumptions (no interview data), flag that the score is hypothesis-grade and recommend interviews
- Encourage honesty — an inflated score helps no one
- This command is useful for quickly comparing multiple problem hypotheses before deciding which one to invest discovery time in
