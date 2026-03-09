---
name: unit-economics
description: "Deep analysis framework for business KPIs and unit economics. Covers CAC, LTV, LTV:CAC ratio, payback period, contribution margin, and channel ROI with calculation methods, benchmarks, and a dashboard template for tracking financial health at scale."
---

## Unit Economics

Analyze and optimize the financial building blocks of your business so that every customer acquired creates sustainable value. Unit economics tell you whether your business model works at the individual customer or transaction level — if the unit economics are broken, scaling only accelerates losses.

### Domain Context

Unit economics is the foundation of growth-stage financial discipline. After achieving product-market fit, the critical question shifts from "do people want this?" to "can we acquire and serve customers profitably?" This skill provides the calculation methods, benchmarks, and diagnostic frameworks to answer that question rigorously.

### Context

You are helping the user analyze unit economics for **$ARGUMENTS**.

If the user provides files (financial data, metrics dashboards, pricing models, channel reports), read them first and incorporate the actual numbers into the analysis.

### Instructions

#### Step 1: Gather Business Context

Ask the user:
- What is your business model? (SaaS, marketplace, e-commerce, transactional, advertising)
- What is your current pricing and packaging?
- How long have you been in market? (pre-revenue, early revenue, growth stage, mature)
- What data do you have available? (revenue, costs, churn, acquisition spend by channel)
- What is your primary concern? (CAC too high, churn too high, unclear profitability, preparing for fundraising)

#### Step 2: Customer Acquisition Cost (CAC)

Calculate CAC using multiple views to identify the true cost of growth:

**Blended CAC**:
```
Blended CAC = Total Sales & Marketing Spend / Number of New Customers Acquired
```
This is the simplest view but hides important details.

**CAC by Channel**:

| Channel | Spend | Customers Acquired | CAC | % of Total Customers |
|---------|-------|-------------------|-----|---------------------|
| Paid Search | $ | # | $ | % |
| Paid Social | $ | # | $ | % |
| Content/SEO | $ | # | $ | % |
| Sales Outbound | $ | # | $ | % |
| Referral | $ | # | $ | % |
| Organic/Direct | $ | # | $ | % |
| **Total** | **$** | **#** | **$** | **100%** |

**Paid vs. Organic CAC**:
- Paid CAC = Paid acquisition spend / Paid-attributed customers
- Organic CAC = Non-paid S&M costs (salaries, tools, content creation) / Organic customers
- Healthy businesses see organic CAC decrease over time as brand and word-of-mouth compound

**CAC Trend Analysis**:
- Is CAC increasing, stable, or decreasing quarter over quarter?
- Increasing CAC signals channel saturation, increased competition, or inefficient spend
- Track CAC alongside growth rate — rising CAC with rising growth can be acceptable; rising CAC with flat growth is a red flag

#### Step 3: Customer Lifetime Value (LTV)

Calculate LTV using the method most appropriate to the business stage:

**Method 1: Historical (Simple)**
```
LTV = Average Revenue Per User (ARPU) × Average Customer Lifespan (months)
```
Best for: Mature businesses with stable churn and pricing. Limitation: backward-looking, may not reflect recent changes.

**Method 2: Predictive (Standard)**
```
LTV = ARPU / Monthly Churn Rate
```
Or with gross margin:
```
LTV = (ARPU × Gross Margin %) / Monthly Churn Rate
```
Best for: SaaS and subscription businesses with measurable churn. This is the most commonly used method.

**Method 3: Cohort-Based (Most Accurate)**
```
LTV = Sum of (Monthly Revenue per Cohort × Discount Factor) over customer lifetime
```
Track revenue per cohort month by month. The sum of discounted future revenue gives the most accurate LTV. Best for: Businesses with variable usage, expansion revenue, or seasonal patterns.

**When to use which method**:

| Business Stage | Best Method | Why |
|---------------|-------------|-----|
| Pre-revenue / <6 months | Estimate from pricing model | Not enough data for historical |
| 6-18 months | Predictive (Method 2) | Enough churn data for basic calculation |
| 18+ months | Cohort-based (Method 3) | Enough cohort data for accurate picture |
| Mature / fundraising | All three, cross-referenced | Show rigor and consistency |

**LTV Expansion Levers**:
- Reduce churn (highest impact)
- Increase ARPU through upsell/cross-sell
- Improve gross margin through operational efficiency
- Increase usage/engagement (leading indicator)

#### Step 4: LTV:CAC Ratio

The single most important unit economics metric for growth-stage businesses:

```
LTV:CAC Ratio = Customer Lifetime Value / Customer Acquisition Cost
```

**Interpretation**:

| Ratio | Signal | Action |
|-------|--------|--------|
| < 1:1 | Losing money on every customer | Stop scaling. Fix product (churn), pricing (ARPU), or acquisition (CAC) immediately |
| 1:1 – 3:1 | Unsustainable | Profitable in theory but no margin for error. Optimize before scaling |
| 3:1 – 5:1 | Healthy | Sustainable growth. This is the target range for most businesses |
| > 5:1 | Underinvesting in growth | You can afford to spend more on acquisition. Increase investment in proven channels |

**Nuance**: LTV:CAC should be calculated per segment and per channel, not just blended. A healthy blended ratio can hide an unprofitable segment or channel.

#### Step 5: Payback Period

How quickly you recover the cost of acquiring a customer:

```
Payback Period (months) = CAC / Monthly Gross Profit per Customer
```

Where Monthly Gross Profit = ARPU × Gross Margin %

**Benchmarks by business model**:

| Model | Target Payback | Why |
|-------|---------------|-----|
| SaaS (SMB) | < 12 months | High churn risk; need fast payback |
| SaaS (Enterprise) | < 18 months | Longer sales cycles but lower churn |
| Marketplace | < 18 months | Network effects compound over time |
| E-commerce | < 3 months | Low switching costs; must recover fast |
| Consumer subscription | < 6 months | High churn; low ARPU |

**Why payback matters**: Even with a great LTV:CAC ratio, a long payback period means you need significant working capital to fund growth. Payback period directly affects cash flow and fundraising needs.

#### Step 6: Contribution Margin

Revenue minus all variable costs at the unit level:

```
Contribution Margin = Revenue per Unit - Variable Costs per Unit
Contribution Margin % = Contribution Margin / Revenue per Unit × 100
```

**Variable costs to include**:
- Hosting/infrastructure per user
- Payment processing fees
- Customer support cost per user
- Third-party API/data costs per user
- Sales commission (if variable)

**Gross margin benchmarks by model**:

| Model | Target Gross Margin |
|-------|-------------------|
| SaaS | 70-85% |
| Marketplace | 60-75% (of take rate) |
| E-commerce | 40-60% |
| Fintech | 50-70% |
| Hardware + Software | 40-60% |

**Contribution margin vs. gross margin**: Gross margin covers COGS. Contribution margin includes all variable costs, giving a more complete picture of unit-level profitability.

#### Step 7: Channel ROI Analysis

Evaluate each acquisition channel on a fully loaded basis:

| Channel | CAC | Conversion Rate | LTV of Customers | LTV:CAC | Payback (mo) | Verdict |
|---------|-----|-----------------|-------------------|---------|-------------|---------|
| Paid Search | $ | % | $ | x:1 | # | Scale/Maintain/Cut |
| Paid Social | $ | % | $ | x:1 | # | Scale/Maintain/Cut |
| Content/SEO | $ | % | $ | x:1 | # | Scale/Maintain/Cut |
| Sales Outbound | $ | % | $ | x:1 | # | Scale/Maintain/Cut |
| Referral | $ | % | $ | x:1 | # | Scale/Maintain/Cut |
| Partnerships | $ | % | $ | x:1 | # | Scale/Maintain/Cut |

**Channel decisions**:
- **Scale**: LTV:CAC > 3:1 and not yet saturated
- **Maintain**: LTV:CAC 2:1-3:1 or at efficient scale
- **Optimize**: LTV:CAC 1:1-2:1 but with clear improvement levers
- **Cut**: LTV:CAC < 1:1 with no clear path to improvement

#### Step 8: Unit Economics Dashboard

Produce a comprehensive dashboard the user can track over time:

### Anti-Patterns to Avoid

- **Blended-only analysis** — blended metrics hide underperforming segments and channels; always decompose
- **Ignoring time value** — a dollar today is worth more than a dollar in 18 months; use discounted LTV for long payback periods
- **Vanity LTV** — calculating LTV without gross margin overstates value; always use gross-margin-adjusted LTV
- **CAC without fully loaded costs** — include salaries, tools, and overhead, not just ad spend
- **Static analysis** — unit economics change monthly; build tracking systems, not one-time snapshots
- **Scaling before unit economics work** — growth amplifies both good and bad economics; fix the unit before scaling the volume

### Output Format

```
## Unit Economics Analysis

**Product**: [name]
**Business Model**: [type]
**Analysis Period**: [dates]
**Data Confidence**: [High/Medium/Low — based on data completeness]

### Key Metrics Summary
| Metric | Current | Target | Trend | Status |
|--------|---------|--------|-------|--------|
| Blended CAC | $ | $ | [arrow] | [R/Y/G] |
| LTV (gross-margin adjusted) | $ | $ | [arrow] | [R/Y/G] |
| LTV:CAC | x:1 | 3:1+ | [arrow] | [R/Y/G] |
| Payback Period | # mo | # mo | [arrow] | [R/Y/G] |
| Contribution Margin | % | % | [arrow] | [R/Y/G] |
| Monthly Churn | % | % | [arrow] | [R/Y/G] |
| ARPU | $ | $ | [arrow] | [R/Y/G] |

### Channel Performance
[Channel ROI table from Step 7]

### Diagnosis
[What is working, what is broken, and why]

### Optimization Recommendations
1. [Highest-impact recommendation with expected effect on metrics]
2. [Second recommendation]
3. [Third recommendation]

### Next Steps
- Track these metrics weekly/monthly in a dashboard
- Use the **scaling-roadmap** skill to plan growth investments
- Re-run this analysis monthly to track trends
```
