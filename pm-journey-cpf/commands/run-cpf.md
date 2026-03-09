---
description: Run a full Customer Problem Fit (CPF) validation cycle — from problem hypothesis through customer discovery to evidence-based GO/PIVOT/KILL decision
argument-hint: "<product idea or problem hypothesis>"
---

# /run-cpf -- Customer Problem Fit Validation

Run a structured CPF validation process that takes you from a raw product idea or problem hypothesis to an evidence-based decision about whether the problem is worth solving. This command chains multiple skills into a single end-to-end workflow.

## Invocation

```
/run-cpf AI-powered meeting summarizer for remote teams
/run-cpf "Enterprise PMs can't prioritize feature requests effectively"
/run-cpf                    # asks what you're exploring
```

## Workflow

### Step 1: Understand the Context

Determine the starting point:
- **Raw idea** — the user has a product concept but no validated problem
- **Problem hypothesis** — the user has a specific problem statement to test
- **Post-interview** — the user has already done interviews and needs to score

Ask the user:
- What product idea or problem area are you exploring?
- What do you already know? (prior research, customer feedback, data, gut instinct)
- What stage are you at? (just starting, mid-discovery, post-interviews)
- What decisions will this validation inform? (build/kill, funding, prioritization)

Accept context from uploaded files (research, transcripts, feedback, data), links, or conversation.

### Step 2: Define the Problem Hypothesis

Apply the **problem-statement** skill:

- Help the user articulate a testable problem hypothesis
- Use the structured template: [Target customer] experiences [problem] when [context], which causes [negative outcome]. Currently they [workaround], which fails because [limitation].
- Run the validation checklist to ensure the hypothesis is observable, behavior-based, specific, testable, solution-free, outcome-linked, and has evidence of workarounds
- Iterate until the hypothesis passes the checklist

**Checkpoint**: "Here's your problem hypothesis. Does this capture the core of what you want to validate? I can refine it before we proceed."

### Step 3: Market Research & Competitive Landscape

Before talking to customers, understand the broader landscape:

- Use the competitor analysis approach from pm-market-research to identify who else is solving this problem or adjacent problems
- Use the market sizing approach from pm-market-research to estimate the addressable market (TAM/SAM/SOM)
- Identify existing solutions, workarounds, and their limitations
- Map the competitive landscape to understand white space

Output a brief market context summary that informs your customer discovery questions.

**Checkpoint**: "Here's the competitive landscape. This will help us ask smarter questions in interviews. Ready to define target segments?"

### Step 4: Identify Target Customer Segments

Narrow down who to talk to:

- Use the market segmentation approach from pm-market-research to identify and prioritize customer segments
- For each segment, define: who they are, why they might have this problem, how to find them
- Select the 1-2 most promising segments to focus discovery on
- Define screening criteria for interview participants

### Step 5: Create Personas & Empathy Maps

Build a detailed picture of the target customer:

- Use the user personas approach from pm-market-research to create initial personas based on available data
- Apply the **empathy-map** skill to create empathy maps for each persona
- If the user has existing interview data, fill the empathy maps from real evidence
- If no interviews yet, create hypothesis-based empathy maps to be validated later

**Checkpoint**: "Here are your personas and empathy maps. These are hypothesis-based — we'll validate and refine them through customer discovery. Ready to plan the discovery sprint?"

### Step 6: Plan Customer Discovery

Apply the **customer-discovery-plan** skill:

- Define discovery objectives and success criteria
- Identify target participants (minimum 5, target 12-15)
- Set up recruitment channels and outreach templates
- Design the question framework following The Mom Test principles
- Create a 1-2 week sprint plan with daily activities
- Prepare per-interview and cross-interview synthesis templates

**Checkpoint**: "Here's your discovery sprint plan. You'll need 1-2 weeks to complete the interviews. Come back with your findings and I'll help you analyze them."

*--- Pause point: The user goes and conducts interviews ---*

### Step 7: Analyze Interview Results

When the user returns with interview data:

- Accept transcripts, notes, or summaries in any format
- Use the interview summarization approach from pm-product-discovery to structure each interview
- Synthesize across all interviews to identify patterns:
  - Recurring themes and pain points
  - Frequency and intensity patterns
  - Common workarounds and their limitations
  - Segments that feel the problem most acutely
  - Surprise findings and contradictions
- Update the empathy maps with real evidence
- Refine the personas based on what you learned

### Step 8: Validate the Problem

Apply the **problem-validation** skill:

- Score the problem across 5 dimensions (1-5 each):
  - **Frequency**: How often does the problem occur?
  - **Intensity**: How painful is it?
  - **Willingness to Pay**: Would they pay to solve it?
  - **Current Alternatives**: What do they do today?
  - **Switching Cost**: How easy to adopt a new solution?
- Calculate the total CPF Score (out of 25)
- Generate a detailed scorecard with evidence for each dimension
- Identify strengths, weaknesses, and evidence gaps

### Step 9: Decision Gate

Based on the CPF Score, provide a clear recommendation:

| Score | Decision | Action |
|-------|----------|--------|
| 20-25 | **GO** | Problem is validated. Proceed to Problem Solution Fit (PSF). |
| 15-19 | **PIVOT** | Problem shows promise but needs refinement. Refine hypothesis, narrow segment, or do more interviews. |
| 10-14 | **RECONSIDER** | Weak signal. Major pivot needed — different problem, different segment, or kill this direction. |
| 5-9 | **KILL** | No Customer Problem Fit. Move on to a different problem or segment. |

### Step 10: Generate CPF Assessment Document

Compile everything into a comprehensive document:

```
## CPF Assessment: [Product Idea / Problem Area]

**Date**: [today]
**Phase**: Customer Problem Fit (Stage 1 of Fit Journey)
**Decision**: [GO / PIVOT / KILL]
**CPF Score**: [X/25]

### Problem Hypothesis
[Final validated problem statement]

### Market Context
- Market size: [TAM/SAM/SOM estimates]
- Key competitors: [list]
- White space: [opportunity]

### Target Customer
- **Segment**: [primary segment]
- **Persona**: [summary]
- **Empathy Map**: [key insights from See/Hear/Think/Feel/Say/Do]

### Discovery Summary
- **Interviews conducted**: [N]
- **Key patterns**: [top 3 themes]
- **Strongest signal**: [most compelling evidence]
- **Biggest surprise**: [unexpected finding]

### Problem Validation Scorecard
| Dimension | Score | Evidence |
|-----------|-------|----------|
| Frequency | [1-5] | [summary] |
| Intensity | [1-5] | [summary] |
| Willingness to Pay | [1-5] | [summary] |
| Current Alternatives | [1-5] | [summary] |
| Switching Cost | [1-5] | [summary] |
| **Total** | **[X/25]** | |

### Strengths
- [What's strong and why]

### Risks & Gaps
- [What's weak or unknown]

### Recommendation
[Detailed rationale for GO/PIVOT/KILL]

### Next Steps
[Specific actions based on the decision]
```

Save the assessment as a markdown file to the user's workspace.

### Step 11: Offer Next Steps

Based on the decision:

**If GO (20+)**:
- "Ready for the next phase? Run `/run-psf` to define and validate your solution."
- "Want me to draft initial solution hypotheses based on what customers told you?"
- "Should I create a PRD outline for the top solution idea?"

**If PIVOT (15-19)**:
- "Want me to refine the problem hypothesis based on what we learned?"
- "Should I help plan a follow-up discovery sprint with a narrower segment?"
- "Want me to re-score after adjusting the target customer?"

**If KILL (below 15)**:
- "Want me to analyze your interview data for a different problem that emerged?"
- "Should we explore a different customer segment for the same problem area?"
- "Want to start fresh with a new problem hypothesis?"

## Notes

- This is a multi-session workflow — Steps 1-6 happen in the first session (30-45 min), Steps 7-11 happen after interviews (20-30 min)
- At each checkpoint, the user can redirect, skip, or go deeper
- If the user already has interview data, skip to Step 7
- If the user already has a problem statement, skip to Step 2 validation
- The CPF Assessment Document should be a living document — offer to update it as new evidence comes in
- A KILL decision is a good outcome — it saves months of building the wrong thing
- Emphasize evidence over opinions throughout the process
