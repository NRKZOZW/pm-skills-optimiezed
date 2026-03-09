---
description: "Analyze business KPIs and unit economics — CAC, LTV, payback period, and channel ROI with optimization recommendations"
argument-hint: "<business metrics or product financials>"
---

# /check-unit-economics -- Unit Economics Analysis

Quick, focused analysis of your business unit economics. Get a clear picture of CAC, LTV, payback period, contribution margin, and channel ROI in about 10 minutes — with specific optimization recommendations.

## Invocation

```
/check-unit-economics SaaS product with $50 ARPU, 3% monthly churn, $200 blended CAC
/check-unit-economics [upload a metrics dashboard, financial spreadsheet, or P&L]
/check-unit-economics Marketplace with 15% take rate, $30 average order value
```

## Workflow

### Step 1: Gather Metrics

Ask the user for available data:

- **Revenue**: ARPU (monthly/annual), pricing tiers, revenue breakdown by segment
- **Costs**: Total S&M spend, spend by channel, COGS, variable costs per user
- **Customers**: Total customers, new customers per month, customers by channel
- **Retention**: Monthly/annual churn rate, net revenue retention, cohort data if available
- **Business model**: SaaS, marketplace, e-commerce, transactional, or other

Accept whatever data the user has — the analysis adapts to data completeness. Flag gaps and note assumptions where data is missing.

### Step 2: Run the Analysis

Apply the **unit-economics** skill to calculate and evaluate:

1. **CAC** — blended and by channel where data allows
2. **LTV** — using the most appropriate method for the business stage and available data
3. **LTV:CAC ratio** — with interpretation and benchmarking
4. **Payback period** — with benchmark for the business model
5. **Contribution margin** — with gross margin benchmarking
6. **Channel ROI** — if channel-level data is available

### Step 3: Diagnose

Identify what is healthy and what needs attention:

- Which metrics are in the healthy range vs. concerning?
- What is the single biggest lever to improve unit economics?
- Are there channel-level or segment-level issues hidden in the blended numbers?
- What trends should the user watch?

### Step 4: Recommend

Provide 3-5 specific, prioritized recommendations:

- Each recommendation should target a specific metric
- Include expected impact (e.g., "Reducing churn from 5% to 3% would increase LTV by 67%")
- Order by impact and feasibility

### Step 5: Output

```
## Unit Economics Health Check

**Product**: [name]
**Business Model**: [type]
**Data Confidence**: [High/Medium/Low]
**Date**: [analysis date]

### Scorecard
| Metric | Value | Benchmark | Status |
|--------|-------|-----------|--------|
| Blended CAC | $ | [model benchmark] | [healthy/warning/critical] |
| LTV | $ | [model benchmark] | [healthy/warning/critical] |
| LTV:CAC | x:1 | 3:1+ | [healthy/warning/critical] |
| Payback Period | # months | [model benchmark] | [healthy/warning/critical] |
| Contribution Margin | % | [model benchmark] | [healthy/warning/critical] |
| Monthly Churn | % | [model benchmark] | [healthy/warning/critical] |

### Diagnosis
[2-3 sentences on overall health and the key insight]

### Top Recommendations
1. **[Action]** — [expected impact on specific metric]
2. **[Action]** — [expected impact on specific metric]
3. **[Action]** — [expected impact on specific metric]

### Data Gaps
[What additional data would improve the analysis]

### Next Steps
- Track these metrics monthly
- Re-run this analysis in 30 days to measure progress
- Use `/run-gtm` for a complete GTM strategy including unit economics
```

Save as markdown.

## Notes

- This command is designed for a quick 10-minute analysis — for a full GTM strategy including unit economics, use `/run-gtm`
- The analysis is only as good as the input data — be honest about what you know vs. what you are estimating
- Unit economics should be tracked monthly at minimum during the scaling phase
- Blended metrics hide important details — always try to break down by channel and segment
- If LTV:CAC is below 1:1, stop scaling and fix the fundamentals before investing in growth
