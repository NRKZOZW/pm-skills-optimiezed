---
description: "Run a full Problem Solution Fit cycle — from value proposition design through solution ideation and prototype validation"
argument-hint: "<solution idea or CPF outputs>"
---

# /run-psf -- Full Problem Solution Fit Cycle

Run a structured PSF process that takes a validated problem and guides you through designing, prototyping, and validating a solution. This command chains multiple skills into a single end-to-end workflow.

## Invocation

```
/run-psf AI-powered meeting summarizer for remote teams (validated problem: teams lose 5+ hrs/week to unnecessary meetings)
/run-psf [paste CPF outputs: validated problem, personas, insights]
/run-psf                    # asks for problem context
```

## Workflow

### Step 1: Understand the Context

Determine what inputs are available:

- **CPF outputs provided** — Extract the validated problem statement, target persona, key insights, and remaining hypotheses
- **Solution idea provided** — Ask clarifying questions about the validated problem behind it
- **Neither provided** — Ask the user to describe the customer problem and any validation done so far

Ask the user:
- What customer problem are you solving? (ideally validated)
- Who is the target customer? (persona or segment)
- What do you already know? (research, interviews, experiments, CPF outputs)
- What solution ideas have you considered?

Accept context from uploaded files (research, CPF outputs, interview transcripts, data), links, or conversation.

**Checkpoint**: "Here is my understanding of the validated problem and target customer. Is this accurate before we design solutions?"

### Step 2: Design Value Proposition

Apply the **value-proposition-canvas** skill:

- Build the Customer Profile: map functional, social, and emotional jobs; identify pains and gains
- Build the Value Map: define products/services, pain relievers, and gain creators
- Assess fit between the two sides
- Score the fit quality (target: 15+ out of 25 to proceed)

If fit score is below 15, recommend iterating on the value proposition before moving to ideation.

**Checkpoint**: "Here is your Value Proposition Canvas with a fit score of [X]/25. Should we proceed to ideation, or iterate on the value proposition first?"

### Step 3: Build Opportunity Solution Tree

Use the opportunity-solution-tree skill from pm-product-discovery to structure the solution space:

- Place the validated problem/outcome at the top
- Map customer opportunities from the value proposition canvas pains and gains
- Prioritize opportunities using Opportunity Score (Importance x (1 - Satisfaction))
- This creates the structure for generating solutions

Present the tree and let the user confirm the prioritized opportunities.

### Step 4: Brainstorm Solutions

Use the brainstorm-ideas-new or brainstorm-ideas-existing skill from pm-product-discovery based on product stage:

- Generate ideas from three perspectives:
  - **PM perspective**: What would maximize customer value and business impact?
  - **Designer perspective**: What would create the best user experience?
  - **Engineer perspective**: What is technically elegant and feasible?
- Present the top 10 ideas with brief rationale for each
- Ask the user to select 3-5 ideas to carry forward

**Checkpoint**: "Here are 10 solution ideas. Which 3-5 should we validate? Or should I generate more?"

### Step 5: Design Solution Experiments

Use the brainstorm-experiments-new or brainstorm-experiments-existing skill from pm-product-discovery:

- For each selected solution idea, design 1-2 validation experiments
- Include: hypothesis, method, success criteria, timeline, effort
- Sequence experiments by dependency and learning value
- Recommend which to run first

Types of experiments to consider:
- Concierge MVP (manually deliver the value)
- Wizard of Oz (fake the backend, real frontend)
- Landing page / fake door test
- Prototype usability test
- Customer co-creation session
- A/B test against current solution

### Step 6: Plan Prototype Test

Apply the **prototype-test-plan** skill:

- Select the appropriate prototype fidelity based on what needs validation
- Write a complete test script with introduction, warm-up, 3-5 core tasks, and debrief
- Define metrics to collect (task completion rate, time-on-task, satisfaction)
- Set sample size (recommend 5 users for first round)
- Provide a synthesis template for capturing findings

**Checkpoint**: "Here is the prototype test plan. Ready to run the test? After testing, we will score the solution."

### Step 7: Validate Solution

After the user has run the prototype test (or provides test results), apply the **solution-validation** skill:

- Score the solution across 5 dimensions (1-5 each):
  1. Problem-Solution Alignment
  2. Desirability
  3. Willingness to Pay
  4. Usability Signal
  5. Differentiation
- Calculate total score (out of 25)
- Provide evidence-based assessment

### Step 8: Decision Gate

Based on the Solution Validation Scorecard total score:

| Score | Decision | Action |
|-------|----------|--------|
| 20-25 | **GO** | Strong PSF achieved. Proceed to Solution-Product Fit. |
| 15-19 | **ITERATE** | Promising but gaps remain. Refine the solution and re-test weak dimensions. |
| 10-14 | **PIVOT** | Weak PSF. Keep the validated problem but try a fundamentally different solution approach. |
| Below 10 | **STEP BACK** | No PSF. Re-examine the problem itself. Consider running CPF again. |

### Step 9: Create PSF Assessment Document

Compile everything into a PSF Assessment Document:

```
## PSF Assessment: [Solution Name]

**Date**: [today]
**Problem**: [validated problem statement]
**Target Customer**: [persona/segment]
**Solution**: [solution description]

### Value Proposition Canvas Summary
- **Key Jobs**: [top 3]
- **Key Pains**: [top 3]
- **Key Gains**: [top 3]
- **Fit Score**: [X]/25

### Solutions Explored
| # | Solution Idea | Source | Selected |
|---|--------------|--------|----------|

### Experiments Run
| # | Experiment | Hypothesis | Result | Learning |
|---|-----------|-----------|--------|----------|

### Prototype Test Results
- **Fidelity**: [paper/low-fi/high-fi/clickable]
- **Participants**: [N]
- **Task Completion Rate**: [%]
- **Key Findings**: [top 3 findings]

### Solution Validation Scorecard
| Dimension | Score | Evidence |
|-----------|-------|----------|
| Problem-Solution Alignment | /5 | |
| Desirability | /5 | |
| Willingness to Pay | /5 | |
| Usability Signal | /5 | |
| Differentiation | /5 | |
| **Total** | **/25** | |

### Decision: [GO / ITERATE / PIVOT / STEP BACK]
**Rationale**: [why]

### Remaining Hypotheses
[List of unvalidated assumptions to carry forward]

### Next Steps
[Specific actions based on decision]
```

Save the assessment as a markdown file to the user's workspace.

### Step 10: Offer Next Steps

Based on the decision:

- **If GO**: "Ready to build? Run `/run-spf` to plan and develop your MVP."
- **If ITERATE**: "Want me to redesign the experiment for the weakest dimension?" or "Should we brainstorm alternative approaches to improve [weak dimension]?"
- **If PIVOT**: "Should we go back to Step 4 and brainstorm fundamentally different solutions?"
- **If STEP BACK**: "Consider re-running `/run-cpf` to re-examine the problem. Want me to help analyze what we learned?"

## Notes

- This is a multi-session workflow — the full cycle may take days or weeks as real tests are run
- At each checkpoint, the user can redirect, skip, or go deeper
- If the user already has test results, skip directly to Step 7 (Validate Solution)
- The PSF Assessment Document should be a living document — offer to update it as new evidence comes in
- Encourage the user to test with real target customers, not colleagues or friends
- Emphasize: PSF is about evidence, not opinions. Every score needs supporting data.
