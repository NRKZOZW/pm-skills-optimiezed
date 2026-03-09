---
description: "Run a full Product Market Fit cycle — measure PMF, design growth experiments, deepen core value, and optimize for self-sustaining growth"
argument-hint: "<product name and current metrics>"
---

# /run-pmf -- Product Market Fit Cycle

Run a comprehensive PMF assessment and improvement cycle. Measure your current PMF state, design experiments to strengthen it, deepen your core value, and optimize pricing — all in one guided workflow.

## Invocation

```
/run-pmf B2B analytics dashboard with 500 DAU, 15% D30 retention, NPS 35
/run-pmf Consumer fitness app — 10k signups, 8% D30 retention, no revenue yet
/run-pmf [upload SPF outputs, KPI baselines, or user feedback data]
```

## Workflow

### Step 1: Understand Context

Accept SPF outputs (MVP, KPI baselines, feedback) or gather product context:

Ask:
- What is the product and who is it for?
- What stage are you at? (launched MVP, iterating, growing)
- What metrics do you have? (retention, NPS, engagement, revenue)
- Do you have Sean Ellis survey data? If not, we will design one.
- What does your retention curve look like? (flattening, declining, unknown)
- What user feedback themes have emerged?

### Step 2: Set North Star Metric

Before measuring PMF, ensure you have a clear North Star metric that captures the core value your product delivers. If the user does not have one, suggest they explore the North Star Metric framework from pm-marketing-growth to define one. The North Star should be the single metric that best predicts long-term success.

### Step 3: Measure PMF

Apply the **pmf-measurement** skill:

- Score each of the five PMF dimensions (Sean Ellis, Retention, NPS, Engagement, Revenue)
- Complete the PMF Scorecard with available data
- Identify which dimensions are strong and which are weak
- Flag any dimensions where data is missing and recommend how to collect it

### Step 4: Design PMF Survey

Apply the **pmf-survey** skill:

- If survey data exists: analyze results using the Superhuman PMF Engine
- If no survey data: design a customized PMF survey for the product
  - Tailor questions to the product context
  - Recommend deployment strategy (timing, channel, sample size)
  - Provide analysis template for when results come in

### Step 5: Analyze Retention and Cohorts

Deep-dive into retention patterns. For detailed cohort analysis, the user can explore the cohort analysis capabilities from pm-data-analytics. In this step:

- Assess retention curve shape (flattening vs declining)
- Identify which user segments retain best
- Compare retention by acquisition channel, feature usage, and onboarding path
- Recommend retention improvement priorities

### Step 6: Design Growth Experiments

Apply the **growth-hacking** skill:

- Identify the primary growth bottleneck (onboarding, activation, retention, virality)
- Generate 10-15 experiment ideas across growth categories
- ICE-score and rank all experiments
- Detail the top 3 experiments with hypothesis, metric, and implementation plan
- For growth loop design, the user can also explore the growth loops framework from pm-go-to-market

### Step 7: Deepen Core Value

Apply the **core-value-deepening** skill:

- Identify the core value through feature-retention correlation
- Conduct a feature audit (amplify, promote, maintain, kill)
- Recommend deepening vs widening strategy
- Prioritize improvements using Opportunity Score
- Ensure roadmap is focused on strengthening what drives PMF

### Step 8: Optimize Pricing

Assess pricing alignment with core value. For detailed pricing strategy work, the user can explore the pricing strategy framework from pm-product-strategy. In this step:

- Evaluate current value metric alignment
- Assess whether pricing tiers match user segments
- Recommend pricing adjustments that reinforce PMF
- Ensure free/starter tier demonstrates core value effectively

### Step 9: Decision Gate

Based on the PMF Scorecard total, recommend the path forward:

| PMF Score | Decision | Action |
|-----------|----------|--------|
| 20-25 | **SCALE** | PMF achieved. Proceed to GTM and growth at scale. |
| 15-19 | **ITERATE** | Emerging PMF. Run the top growth experiments and re-assess in 4-6 weeks. |
| 10-14 | **PIVOT** | Weak PMF. Major product changes needed — revisit core value and target segment. |
| Below 10 | **STEP BACK** | No PMF. Revisit solution-problem fit. Consider running `/run-spf` again. |

### Step 10: Generate PMF Assessment Document

```
## PMF Assessment: [Product Name]
Date: [Date]
Stage: [Current Stage]

### Executive Summary
[1-2 paragraph summary of PMF state and recommended path]

### North Star Metric
[Metric and current value]

### PMF Scorecard
| Dimension              | Score (1-5) | Evidence                  |
|------------------------|-------------|---------------------------|
| Sean Ellis Test        |             |                           |
| Retention Curve        |             |                           |
| NPS                    |             |                           |
| Engagement Depth       |             |                           |
| Revenue Signals        |             |                           |
| **TOTAL**              | **__/25**   |                           |

### Decision: [SCALE / ITERATE / PIVOT / STEP BACK]
[Rationale for decision]

### Core Value Analysis
[What the core value is, evidence, and recommendations]

### Feature Audit Results
| Feature | Usage | Core Value Impact | Recommendation |
|---------|-------|-------------------|----------------|

### Growth Experiment Backlog (Top 10)
| Rank | Experiment | ICE Score | Target Metric |
|------|-----------|-----------|---------------|

### Top 3 Experiment Details
#### Experiment 1: [Name]
- Hypothesis: [If we X, then Y, because Z]
- Metric: [Primary metric to move]
- Implementation: [What to build/change]
- Timeline: [Duration]
- Success criteria: [Specific threshold]

### PMF Survey Plan
[Survey design, deployment strategy, and analysis template]

### Pricing Assessment
[Current alignment and recommendations]

### 30-60-90 Day Plan
| Timeframe | Actions | Expected Outcome |
|-----------|---------|-----------------|
| 30 days | [actions] | [outcome] |
| 60 days | [actions] | [outcome] |
| 90 days | [actions] | [outcome] |
```

Save as markdown.

### Step 11: Offer Next Steps

Based on the decision gate:

**If SCALE (20-25)**:
- "PMF achieved! Run `/run-gtm` to bring your product to market at scale."
- "Want me to design growth loops for scaling acquisition?"
- "Should I help define your ideal customer profile for targeted growth?"

**If ITERATE (15-19)**:
- "Let's run the top growth experiments. Want me to detail the implementation plan?"
- "Should I design a PMF survey to gather more data?"
- "Want me to do a deeper retention analysis?"

**If PIVOT (10-14)**:
- "Let's revisit the core value. Want me to run a feature-retention analysis?"
- "Should we re-examine the target segment?"
- "Want me to help redesign the onboarding experience?"

**If STEP BACK (below 10)**:
- "Consider running `/run-spf` to revisit solution-problem fit."
- "Want me to help analyze user feedback to identify what's missing?"
- "Should we revisit the problem definition with discovery research?"

## Notes

- PMF is not binary — it exists on a spectrum and can strengthen or weaken over time
- PMF can exist for one segment but not another — always segment your analysis
- The PMF Scorecard should be re-run quarterly to track trajectory
- Data gaps are expected in early stages — use qualitative signals to fill in
- PMF measurement is not a one-time event but an ongoing practice
