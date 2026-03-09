---
name: solution-validation
description: "Score and validate whether a proposed solution truly solves the customer's problem using a structured Solution Validation Scorecard. Evaluates alignment, desirability, willingness to pay, usability, and differentiation across 5 dimensions."
---

## Solution Validation Scorecard

A structured framework for assessing whether a solution has achieved Problem-Solution Fit. Use this after prototype testing or solution experiments to make evidence-based GO/NO-GO decisions.

### Domain Context

Problem-Solution Fit means you have evidence that your proposed solution solves a real customer problem in a way they value. This scorecard moves beyond gut feeling by requiring evidence for each dimension. It bridges the gap between "we think this works" and "we have proof this works."

### The 5 Dimensions

Score each dimension from 1 (no evidence / poor fit) to 5 (strong evidence / excellent fit).

#### 1. Problem-Solution Alignment (1-5)

Does the solution directly address the validated pain points?

| Score | Meaning |
|-------|---------|
| 5 | Solution addresses the top 3 validated pains; users confirm it solves their problem |
| 4 | Addresses 2-3 pains well; minor gaps remain |
| 3 | Addresses the primary pain but misses secondary pains |
| 2 | Partially addresses the problem; users see some value |
| 1 | Solution does not meaningfully address the validated problem |

**Evidence sources**: Prototype test feedback, user interviews post-test, task completion data, direct quotes from users confirming the solution solves their problem.

**Key question**: "After using this, do you feel your [validated problem] is solved?"

#### 2. Desirability (1-5)

Would customers actively choose this solution over alternatives (including doing nothing)?

| Score | Meaning |
|-------|---------|
| 5 | Users express strong intent to switch; spontaneous positive reactions |
| 4 | Users prefer this over current alternatives; would recommend to others |
| 3 | Users see value but are not compelled to switch from current behavior |
| 2 | Users are lukewarm; "nice to have" reactions |
| 1 | Users prefer existing alternatives or doing nothing |

**Evidence sources**: Preference tests (A vs. B vs. current), Net Promoter intent questions, landing page conversion rates, sign-up intent surveys, spontaneous sharing behavior.

**Key question**: "Would you switch from [current solution] to this? Why or why not?"

#### 3. Willingness to Pay (1-5)

Would customers pay for this solution (or invest significant time/effort to adopt it)?

| Score | Meaning |
|-------|---------|
| 5 | Users commit to a price point; pre-orders or deposits received |
| 4 | Users state a specific price they would pay; it aligns with the business model |
| 3 | Users acknowledge value but are uncertain about price |
| 2 | Users would only use it if free or heavily discounted |
| 1 | Users see no monetary value; would not pay anything |

**Evidence sources**: Van Westendorp pricing survey, fake door pricing tests, pre-order landing pages, concierge MVP payments, direct pricing questions in interviews.

**Key question**: "At what price would this be too expensive? A bargain? What would you expect to pay?"

#### 4. Usability Signal (1-5)

Can customers understand and use the solution without extensive guidance?

| Score | Meaning |
|-------|---------|
| 5 | 90%+ task completion; users navigate intuitively; minimal errors |
| 4 | 75-90% task completion; minor confusion points easily fixable |
| 3 | 50-75% task completion; several usability issues but core flow works |
| 2 | Below 50% task completion; users struggle with fundamental interactions |
| 1 | Users cannot complete core tasks; fundamental UX rethink needed |

**Evidence sources**: Prototype usability tests (task completion rate, time-on-task, error rate), System Usability Scale (SUS) scores, think-aloud observations, heatmaps and click tracking.

**Key question**: "Can you show me how you would [core task] using this?"

#### 5. Differentiation (1-5)

How does the solution compare to existing alternatives in the customer's mind?

| Score | Meaning |
|-------|---------|
| 5 | Users identify clear, unique value no alternative provides |
| 4 | Users see meaningful advantages over most alternatives |
| 3 | Users see it as comparable to alternatives with slight improvements |
| 2 | Users see marginal differences; easily substitutable |
| 1 | Users see no meaningful difference from existing alternatives |

**Evidence sources**: Competitive preference tests, "what makes this different?" interview questions, feature comparison exercises, unique value proposition recall tests.

**Key question**: "How is this different from [top alternative]? What would you miss if this didn't exist?"

### Total Score Interpretation

| Total Score | Assessment | Recommended Action |
|-------------|------------|-------------------|
| 20-25 | **Strong PSF** | Proceed to Solution-Product Fit. Build the MVP. |
| 15-19 | **Promising** | Iterate on weak dimensions. Run targeted experiments to close gaps. |
| 10-14 | **Weak PSF** | Pivot the solution approach. Keep the validated problem, try a fundamentally different solution. |
| Below 10 | **No PSF** | Step back. Re-examine the problem. The problem may not be significant enough, or you may be solving the wrong problem. |

### Instructions

You are helping a product team validate their solution for **$ARGUMENTS**.

### Input Requirements

- A description of the proposed solution
- The validated customer problem it aims to solve
- Evidence from prototype tests, interviews, experiments, or other validation activities

### Process

1. **Review the evidence** — Examine all available validation data (test results, user feedback, experiment outcomes).

2. **Score each dimension** — For each of the 5 dimensions, assign a score (1-5) with explicit justification citing specific evidence.

3. **Identify evidence gaps** — Flag any dimension where evidence is insufficient. Recommend specific activities to fill the gap.

4. **Calculate total score** — Sum the 5 dimension scores and determine the overall PSF assessment.

5. **Provide recommendations** — Based on the total score, recommend specific next steps:
   - For strong dimensions: what to preserve and build on
   - For weak dimensions: specific experiments or changes to improve the score
   - Overall: GO / ITERATE / PIVOT / STEP BACK decision with rationale

6. **Document the scorecard** — Present the complete scorecard in a clear format:

```
## Solution Validation Scorecard

**Solution**: [name]
**Problem**: [validated problem statement]
**Date**: [today]

| Dimension | Score | Evidence | Gaps |
|-----------|-------|----------|------|
| Problem-Solution Alignment | /5 | | |
| Desirability | /5 | | |
| Willingness to Pay | /5 | | |
| Usability Signal | /5 | | |
| Differentiation | /5 | | |
| **Total** | **/25** | | |

**Assessment**: [Strong PSF / Promising / Weak / No PSF]
**Recommendation**: [GO / ITERATE / PIVOT / STEP BACK]
```

Think step by step. Save as markdown if substantial.

---

### Further Reading

- [Problem-Solution Fit: What It Is and How to Achieve It](https://www.productcompass.pm)
- [The Lean Product Playbook](https://leanproductplaybook.com/) by Dan Olsen
- [Testing Business Ideas](https://www.strategyzer.com/library/testing-business-ideas) by David Bland & Alex Osterwalder
