---
description: "Design a validation experiment for a solution hypothesis — with success criteria, timeline, and decision framework"
argument-hint: "<solution hypothesis to validate>"
---

# /design-experiment -- Design a Validation Experiment

Design a focused validation experiment for a specific solution hypothesis. Produces a complete experiment brief with setup steps, success/failure criteria, timeline, sample size, and a decision framework for what to do with the results.

## Invocation

```
/design-experiment "If we add AI-generated meeting summaries, remote teams will reduce meeting time by 30%"
/design-experiment "Users will pay $15/month for automated expense categorization"
/design-experiment "A drag-and-drop interface will increase task completion rate by 50% vs. the current form-based flow"
/design-experiment                    # asks for a hypothesis
```

## Workflow

### Step 1: Clarify the Hypothesis

If $ARGUMENTS contains a clear hypothesis, parse it. Otherwise, help the user formulate one.

A good solution hypothesis follows this structure:

**"We believe that [solution/change] will [expected outcome] for [target users] because [rationale]."**

Ask:
- What is the solution or change you want to validate?
- What outcome do you expect? (be specific and measurable)
- Who is the target user?
- Why do you believe this will work? (what evidence or intuition)

Restate the hypothesis in the structured format and confirm with the user.

### Step 2: Select Experiment Type

Based on the hypothesis, recommend the most appropriate experiment type:

| Experiment Type | Best For | Effort | Timeline | Evidence Strength |
|----------------|---------|--------|----------|------------------|
| **Landing page / Fake door** | Testing demand and willingness to engage | Low | 1-2 weeks | Medium (intent, not behavior) |
| **Concierge MVP** | Testing whether the value proposition works when delivered manually | Medium | 2-4 weeks | High (real behavior) |
| **Wizard of Oz** | Testing the UX with a real frontend but manual backend | Medium | 2-3 weeks | High (real behavior) |
| **Prototype usability test** | Testing whether users can use the solution effectively | Low-Medium | 1-2 weeks | Medium (simulated behavior) |
| **A/B test** | Comparing a change against the current experience | Medium-High | 2-4 weeks | Very high (real behavior, statistical) |
| **Pre-order / Letter of intent** | Testing willingness to pay | Low | 1-2 weeks | Very high (skin in the game) |
| **Survey / Interview** | Testing preferences and perceptions | Low | 1 week | Low (stated, not revealed) |
| **Data analysis** | Validating assumptions with existing behavioral data | Low | 1 week | High (real past behavior) |
| **Customer co-creation** | Testing whether users find value in a concept they help shape | Low-Medium | 1-2 weeks | Medium (collaborative bias) |

Explain why the recommended type is the best fit. Offer alternatives if the user has constraints.

### Step 3: Design the Experiment

Produce a complete experiment brief:

```
## Experiment Brief

### Hypothesis
We believe that [solution/change] will [expected outcome] for [target users] because [rationale].

### Experiment Type
[Selected type] — [why this type was chosen]

### Setup Steps
1. [Step 1 with specific details]
2. [Step 2 with specific details]
3. [Step 3 with specific details]
...

### Success Criteria
- **Primary metric**: [metric name] reaches [threshold] (currently [baseline])
- **Secondary metric**: [metric name] reaches [threshold]
- **Guardrail metric**: [metric name] does not drop below [threshold]

### Failure Criteria
- **Primary metric** below [threshold] after [duration/sample size]
- **Qualitative signal**: [what negative feedback would look like]

### Sample Size & Duration
- **Minimum sample**: [N participants/users]
- **Statistical power**: [if applicable — 80% power, 95% confidence]
- **Duration**: [X days/weeks]
- **Rationale**: [why this sample size is sufficient]

### Timeline
| Week | Activity |
|------|----------|
| Week 1 | [Setup and preparation] |
| Week 2 | [Run experiment] |
| Week 3 | [Collect and analyze data] |
| Week 4 | [Decision and next steps] |

### Resources Needed
- **People**: [who needs to be involved]
- **Tools**: [what tools or platforms are needed]
- **Budget**: [estimated cost, if any]

### Decision Framework
| Result | Interpretation | Next Action |
|--------|---------------|-------------|
| Success criteria met | Hypothesis validated | [Proceed to X — be specific] |
| Partial success | Mixed signals | [Run follow-up experiment targeting the gap] |
| Failure criteria met | Hypothesis invalidated | [Pivot to Y or test alternative Z] |
| Inconclusive | Insufficient data | [Extend experiment or redesign with larger sample] |

### Risks & Mitigations
| Risk | Likelihood | Mitigation |
|------|-----------|-----------|
| [Risk 1] | [Low/Med/High] | [How to handle] |
| [Risk 2] | [Low/Med/High] | [How to handle] |
```

### Step 4: Review and Refine

Present the experiment brief and ask:
- "Does this experiment test what matters most to you?"
- "Are the success criteria ambitious enough but realistic?"
- "Do you have the resources and timeline for this?"
- "Any constraints I should factor in?"

Iterate on the brief based on feedback.

### Step 5: Offer Next Steps

- "Want me to design additional experiments for other hypotheses?"
- "Should I create a full prototype test plan for this?" (if prototype test was selected — reference the **prototype-test-plan** skill)
- "Ready to validate the full solution? Run `/run-psf` for the complete PSF cycle."
- "Want me to score the results after you run this experiment?" (reference the **solution-validation** skill)

## Notes

- One hypothesis per experiment. If the user has multiple hypotheses, design separate experiments.
- Prefer experiments that capture real behavior over stated preferences ("skin in the game" tests).
- Always include a decision framework — the experiment is useless without pre-committed decisions.
- Encourage the user to define success criteria BEFORE running the experiment to avoid post-hoc rationalization.
- If the hypothesis is too vague, push back. "Users will like it" is not testable. "Users will complete the checkout flow in under 2 minutes" is.
- Reference Alberto Savoia's pretotyping principles: test the "it" before building "it."
