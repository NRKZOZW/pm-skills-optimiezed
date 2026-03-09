---
description: "Quick PMF health check — score your product against the PMF Scorecard with improvement recommendations"
argument-hint: "<product name and available metrics>"
---

# /measure-pmf -- PMF Health Check

A lightweight, focused PMF assessment that scores your product against the PMF Scorecard in 5-10 minutes. Use this for quick health checks, board updates, or team alignment on PMF state.

## Invocation

```
/measure-pmf SaaS project management tool — 2k MAU, 22% D30, NPS 42, 5% monthly churn
/measure-pmf Consumer mobile app with 50k downloads and 12% D30 retention
/measure-pmf [paste your current product metrics]
```

## Workflow

### Step 1: Gather Metrics

Ask for available data across the five PMF dimensions:
- **Sean Ellis**: Do you have survey results? What % said "very disappointed"?
- **Retention**: What is your D1, D7, D30 retention? Is the curve flattening?
- **NPS**: What is your current NPS score?
- **Engagement**: What is your DAU/MAU ratio? Average session frequency?
- **Revenue**: What is your churn rate? Any expansion revenue? Organic growth %?

Accept whatever data is available — not all dimensions need to be populated.

### Step 2: Score the PMF Scorecard

Apply the **pmf-measurement** skill:

- Score each dimension where data is available (1-5)
- Mark dimensions without data as "N/A" and note what data is needed
- Calculate total score (out of 25, or adjusted for available dimensions)
- Compare against benchmarks for the product type

### Step 3: Generate Quick Assessment

```
## PMF Health Check: [Product Name]
Date: [Date]

### PMF Scorecard
| Dimension              | Score (1-5) | Key Data Point            |
|------------------------|-------------|---------------------------|
| Sean Ellis Test        |             |                           |
| Retention Curve        |             |                           |
| NPS                    |             |                           |
| Engagement Depth       |             |                           |
| Revenue Signals        |             |                           |
| **TOTAL**              | **__/25**   |                           |

### Verdict: [Strong PMF / Emerging PMF / Weak PMF / No PMF]

### Top Strength
[The dimension scoring highest and why it matters]

### Top Gap
[The dimension scoring lowest and what to do about it]

### Data Gaps
[Dimensions that could not be scored and how to collect the data]

### Quick Wins (Top 3 Recommendations)
1. [Most impactful improvement with expected outcome]
2. [Second priority]
3. [Third priority]
```

### Step 4: Offer Next Steps

- "Want a full PMF cycle? Run `/run-pmf` for growth experiments, core value analysis, and a complete action plan."
- "Need to collect Sean Ellis data? I can design a PMF survey for you."
- "Want to improve retention? I can help design growth experiments."

## Notes

- This is a quick assessment, not a deep analysis — use `/run-pmf` for the full cycle
- Missing data is expected — even a partial scorecard is valuable for identifying gaps
- Re-run monthly or quarterly to track PMF trajectory over time
- Best used as a team alignment tool: share the scorecard to create shared understanding of PMF state
