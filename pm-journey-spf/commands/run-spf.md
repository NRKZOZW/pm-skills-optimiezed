---
description: "Run a full Solution Product Fit cycle — from MVP scoping through development planning, launch, and user validation"
argument-hint: "<validated solution concept or PSF outputs>"
---

# /run-spf -- Solution Product Fit Cycle

Run a complete SPF cycle to build your MVP, launch it, and validate that users find real value. This command chains together scoping, planning, building, and measurement into a structured workflow with decision gates.

## Invocation

```
/run-spf B2B scheduling tool validated through PSF — users want async meeting coordination
/run-spf [paste your PSF assessment or solution concept]
/run-spf [upload PSF outputs, prototype results, or value proposition docs]
```

## Workflow

### Step 1: Understand Context

Accept the user's input. This can be:
- PSF outputs (validated solution, value proposition, prototype test results)
- A solution concept with supporting evidence
- Uploaded documents from prior stages

If the input is sparse, ask:
1. What solution are you building? What problem does it solve?
2. Who is the target user and what is their core JTBD?
3. What validation have you done so far? What assumptions are confirmed?
4. What is the biggest remaining risk?

> **Checkpoint**: Confirm understanding of the solution concept and validated assumptions before proceeding.

### Step 2: Define Product Vision

Help the user articulate a clear product vision that will guide MVP decisions. Consider using the product vision skill from pm-product-strategy to craft a compelling vision statement that aligns the team on where this product is headed long-term.

The vision should answer: If this product succeeds wildly, what does the world look like for our users in 2-3 years?

> **Checkpoint**: Confirm the product vision before moving to scoping.

### Step 3: Scope the MVP

Apply the **mvp-scoping** skill to define exactly what to build:
- Map the user journey and draw the walking skeleton
- Identify the riskiest assumption and ensure the MVP tests it
- Prioritize features using MoSCoW
- Decide MVP vs MLP approach
- Produce a clear scope document with success criteria

> **Checkpoint**: Review the MVP scope document. Confirm Must-have features and what is explicitly out of scope.

### Step 4: Write the PRD

With the MVP scope locked, create a Product Requirements Document. Consider using the PRD writing command from pm-execution to produce a comprehensive PRD that covers problem statement, user stories, requirements, constraints, and success metrics.

The PRD should reference the MVP scope document and stay within the Must-have boundaries.

> **Checkpoint**: Review and approve the PRD before breaking it into stories.

### Step 5: Create User Stories and Backlog

Break the PRD into development-ready user stories. Consider using the user stories skill from pm-execution to create stories following the 3 C's (Card, Conversation, Confirmation) and INVEST criteria.

Ensure every Must-have feature from the MVP scope maps to at least one user story.

### Step 6: Set KPIs

Apply the **kpi-framework** skill to define how you will measure MVP success:
- Select the North Star Metric
- Define input metrics and health guardrails
- Set targets and measurement frequency
- Establish GO/ITERATE/PIVOT/KILL criteria

> **Checkpoint**: Review KPIs and confirm that the team can actually measure them with existing (or planned) infrastructure.

### Step 7: Plan the Initial Sprint

With stories and KPIs defined, plan the first development sprint. Consider using the sprint planning capability from pm-execution to organize the backlog into a focused sprint with clear goals.

Sprint goal should tie directly to the walking skeleton — get the end-to-end flow working first, then layer in quality and edge cases.

### Step 8: Run a Pre-Mortem

Before development begins, imagine the MVP has failed. Consider using the pre-mortem skill from pm-execution to identify risks and create mitigation plans.

Focus on:
- Technical risks that could delay launch
- Assumptions that might be wrong
- User adoption risks
- Measurement risks (can you actually collect the data you need?)

> **Checkpoint**: Review pre-mortem findings and decide if any risks require scope adjustment.

### Step 9: Post-Launch — Analyze and Collect Feedback

After the MVP launches and has been live for the agreed measurement window:

Apply the **feedback-loop** skill to:
- Set up feedback channels appropriate to your user base
- Collect and code qualitative feedback by theme
- Build the pain-frequency matrix
- Create the feedback-to-action pipeline

Pair this with quantitative analysis. Consider using cohort analysis from pm-data-analytics to understand retention patterns and user behavior over time.

Produce a combined quantitative + qualitative assessment.

### Step 10: Decision Gate

Based on KPI results and feedback analysis, make the SPF decision:

| Decision | Signal | Action |
|----------|--------|--------|
| **SCALE** | North Star on target, activation strong, retention curve flattening, positive user feedback | Proceed to PMF stage. Invest in growth. |
| **ITERATE** | Mixed signals — some metrics strong, others weak. Users see value but experience friction. | Identify weakest input metric, run targeted experiments, re-measure in 2-4 weeks. |
| **PIVOT** | Weak engagement, low activation, poor retention. Users do not find expected value. | Revisit core assumptions. Try a different solution approach or target segment. |
| **KILL** | No meaningful engagement after multiple iterations. Core assumption disproven. | Stop investment. Capture learnings. Redirect resources. |

## Output

Produce an **SPF Assessment Document**:

```
## SPF Assessment

**Product**: [name]
**Assessment Date**: [date]
**MVP Launch Date**: [date]
**Measurement Window**: [duration]

### Product Vision
[Vision statement]

### MVP Summary
- Core features shipped: [list]
- Out of scope: [list]
- Approach: [MVP / MLP]

### KPI Results
| Metric | Target | Actual | Status |
|--------|--------|--------|--------|
| [North Star] | [target] | [actual] | [on track / behind / ahead] |
| [Input metric 1] | [target] | [actual] | [status] |
| [Input metric 2] | [target] | [actual] | [status] |
| [Health guardrail] | [threshold] | [actual] | [green / red] |

### User Feedback Summary
- Total feedback items: [count]
- Top 3 themes: [themes]
- Key user quotes: [quotes]
- Pain-frequency highlights: [summary]

### Riskiest Assumption Status
- Assumption: [what it was]
- Result: [validated / partially validated / invalidated]
- Evidence: [data points]

### Decision
**[SCALE / ITERATE / PIVOT / KILL]**

Rationale: [explanation based on KPI results, feedback, and assumption validation]

### Next Steps
[Specific actions based on the decision]
```

### What's Next?

Ready to find product-market fit? Run `/run-pmf` to measure and achieve PMF.
