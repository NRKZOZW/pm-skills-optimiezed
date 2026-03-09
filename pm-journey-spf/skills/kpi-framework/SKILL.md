---
name: kpi-framework
description: "Set KPIs for MVP success using North Star Metrics, input metrics, and health guardrails. Includes judgment criteria with GO/ITERATE/PIVOT thresholds and common MVP KPI benchmarks by product type."
---

## KPI Framework

Define and measure MVP success with a structured KPI hierarchy. The right metrics tell you whether users are finding real value — not just whether they showed up once.

### Domain Context

Most MVPs fail not because the product was bad, but because the team measured the wrong things or had no criteria for what "good" looks like. This framework establishes a North Star Metric (the single best proxy for user value), supporting input metrics (levers you can pull), and health guardrails (things that must not break). Together, they form a measurement system that drives clear GO/ITERATE/PIVOT decisions.

### Context

You are helping the user define KPIs for **$ARGUMENTS**.

If the user provides files (MVP scope documents, product strategy, prior analytics), read them first and incorporate relevant data.

### Instructions

#### Step 1: Understand the Product and MVP

Ask the user:
- What does the MVP do? What is the core value proposition?
- Who is the target user? How will they find the product?
- What does "success" look like in plain language? (e.g., "Users come back weekly to do X")
- What is the riskiest assumption the MVP is testing?
- What data infrastructure exists? (analytics tools, event tracking, database access)

#### Step 2: Select the North Star Metric

The North Star Metric (NSM) is the single metric that best captures the core value your product delivers to users. It should be:

- **Value-aligned**: Goes up only when users get real value
- **Leading**: Predicts long-term success, not just short-term activity
- **Actionable**: The team can influence it through product decisions
- **Understandable**: Everyone on the team can explain what it measures

**Common North Star Metrics by product type:**

| Product Type | Example NSM | Why |
|-------------|-------------|-----|
| SaaS / Productivity | Weekly active users completing core action | Measures habitual value delivery |
| Marketplace | Transactions per week | Measures liquidity and match quality |
| Consumer / Social | Daily active users (DAU) | Measures engagement and habit formation |
| Content / Media | Total reading/viewing time | Measures content value |
| E-commerce | Purchases per active buyer per month | Measures repeat purchase intent |
| Developer Tools | API calls per week | Measures integration depth |

#### Step 3: Define Input Metrics

Identify 3-5 metrics that directly drive the North Star. These are the levers the team works on daily.

| Input Metric | Definition | Relationship to NSM |
|-------------|-----------|-------------------|
| **Activation Rate** | % of new users who complete the core action within [timeframe] | Users who activate are [X]x more likely to become regular users |
| **Feature Adoption** | % of active users using [key feature] per [period] | Core feature usage drives the value that retains users |
| **Session Frequency** | Average sessions per user per [period] | More frequent use indicates habit formation |
| **Time to Value** | Minutes from signup to first successful core action | Faster time to value increases activation |
| **Referral Rate** | % of users who invite others | Organic growth signals genuine satisfaction |

Customize these to the specific product. Not every product needs all five.

#### Step 4: Set Health Metrics (Guardrails)

Health metrics are not goals to optimize — they are boundaries that must not be crossed. If a health metric goes red, stop and fix it before optimizing input metrics.

| Health Metric | Threshold | Why It Matters |
|--------------|-----------|----------------|
| **Error Rate** | < [X]% | Broken product cannot deliver value |
| **Page/Screen Load Time** | < [X]s (p95) | Slow product drives users away before they see value |
| **Support Ticket Volume** | < [X] per [Y] users | High support load signals UX failures |
| **Unsubscribe / Delete Rate** | < [X]% per [period] | Users actively leaving is a red alert |

#### Step 5: Build the KPI Card

For each metric, fill in:

| Field | Detail |
|-------|--------|
| **Metric Name** | [name] |
| **Definition** | Exactly how it is calculated (numerator / denominator, time window) |
| **Data Source** | Where the data comes from (analytics tool, database query, manual count) |
| **Baseline** | Current value, or "TBD — establish in first 2 weeks" |
| **Target** | What "good" looks like for the MVP phase |
| **Measurement Frequency** | Daily / Weekly / Monthly |
| **Owner** | Who is responsible for tracking and acting on this metric |

#### Step 6: Define Judgment Criteria

Establish clear thresholds for the GO/ITERATE/PIVOT decision after the MVP measurement window (typically 4-8 weeks):

| Decision | Criteria | Action |
|----------|----------|--------|
| **GO (Scale)** | NSM meets or exceeds target AND activation rate > [X]% AND retention curve flattens | Invest in growth, proceed to PMF stage |
| **ITERATE** | NSM shows positive trend but below target OR activation is strong but retention drops | Identify the weakest input metric, run targeted experiments, re-measure in 2-4 weeks |
| **PIVOT** | NSM is flat or declining AND activation < [X]% AND retention drops to near zero by week 4 | Revisit core assumptions, consider different solution approach or different user segment |
| **KILL** | No meaningful engagement after 4+ weeks despite iteration, or fundamental assumption disproven | Stop investment, capture learnings, redirect resources |

#### Step 7: Common MVP KPI Benchmarks

Provide relevant benchmarks so the user can calibrate targets:

**SaaS Products**
- Activation rate: 20-40% is typical, 60%+ is strong
- DAU/MAU ratio: 10-20% is average, 25%+ is strong engagement
- Week 1 retention: 35-45% is typical, 50%+ is strong
- Month 1 retention: 15-25% is typical for MVP stage

**Marketplaces**
- Liquidity: 30-50% of listings should result in a transaction
- Time to first transaction: under 7 days is strong
- Repeat transaction rate: 20-30% within 30 days

**Consumer Apps**
- D1 retention: 25-35% is average, 40%+ is strong
- D7 retention: 10-15% is average, 20%+ is strong
- D30 retention: 5-8% is average, 10%+ is strong
- Session length: highly category-dependent

### Anti-Patterns to Avoid

- **Vanity metrics** — signups, page views, and downloads feel good but do not measure value delivery
- **Too many metrics** — if everything is a KPI, nothing is; keep the total under 10
- **No baseline** — you cannot judge "good" without knowing where you started
- **Moving the goalposts** — set targets before you see the data, not after
- **Ignoring qualitative data** — metrics tell you what is happening; user feedback tells you why

### Output Format

```
## KPI Framework

**Product**: [name]
**MVP Phase**: [dates or sprint range]
**Measurement Window**: [X weeks]

### North Star Metric
**[Metric Name]**: [definition]
- Baseline: [value or TBD]
- Target: [value]
- Frequency: [daily/weekly]

### Input Metrics
| Metric | Definition | Baseline | Target | Frequency | Owner |
|--------|-----------|----------|--------|-----------|-------|
| [name] | [definition] | [value] | [value] | [freq] | [who] |

### Health Guardrails
| Metric | Threshold | Data Source |
|--------|-----------|-------------|
| [name] | [limit] | [source] |

### Judgment Criteria
| Decision | Trigger | Action |
|----------|---------|--------|
| GO | [criteria] | [action] |
| ITERATE | [criteria] | [action] |
| PIVOT | [criteria] | [action] |
| KILL | [criteria] | [action] |

### Next Steps
- Implement event tracking for all KPIs before launch
- Establish baselines during the first 1-2 weeks
- Schedule weekly KPI review meetings
- Set up the **feedback-loop** skill to pair quantitative data with qualitative insights
```
