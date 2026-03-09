---
name: pmf-measurement
description: "Comprehensive PMF measurement framework. Combines the Sean Ellis Test, retention curve analysis, NPS, engagement depth, and revenue signals into a unified PMF Scorecard. Use when assessing whether a product has achieved product-market fit."
---
# PMF Measurement

## Overview
Measure product-market fit across multiple dimensions using a structured scorecard approach. Rather than relying on a single metric, this framework combines five proven PMF signals into a comprehensive assessment that reveals both the strength and gaps in your product-market fit.

## When to Use
- After launching an MVP and collecting initial user data
- During quarterly PMF health checks
- Before deciding to scale marketing spend
- When evaluating whether to pivot, iterate, or double down
- As input to investment decisions or board updates

## 1. Sean Ellis Test (40% Rule)

The gold standard PMF survey question:

> "How would you feel if you could no longer use [product]?"

**Response options**:
- Very disappointed
- Somewhat disappointed
- Not disappointed
- N/A (I no longer use [product])

**Interpretation**: If 40%+ of respondents select "Very disappointed," you have a strong PMF signal.

### Survey Design Tips
- Target users who have experienced the core value (not brand-new signups)
- Require a minimum of 40 responses for statistical validity; 100+ is ideal
- Exclude users who signed up but never activated
- Segment results by acquisition channel, user persona, and usage frequency
- Run the survey quarterly to track trajectory over time

### Scoring
| % Very Disappointed | Score |
|---------------------|-------|
| 50%+                | 5     |
| 40-49%              | 4     |
| 30-39%              | 3     |
| 20-29%              | 2     |
| Below 20%           | 1     |

## 2. Retention Curve Analysis

A flattening retention curve is one of the strongest PMF indicators. If users keep coming back after the initial drop-off, the product delivers lasting value.

### What Good Looks Like
- **Strong PMF**: Curve flattens after initial drop — a stable cohort continues using the product indefinitely
- **Weak PMF**: Curve continues declining toward zero — users gradually abandon the product
- **No PMF**: Steep decline with no flattening — nearly all users churn within weeks

### Retention Benchmarks by Product Type
| Product Type | Day 1 | Day 7 | Day 30 | PMF Threshold (D30) |
|-------------|-------|-------|--------|---------------------|
| SaaS (B2B)  | 80%+  | 60%+  | 40%+   | > 20%               |
| Consumer App| 50%+  | 30%+  | 15%+   | > 10%               |
| Marketplace | 70%+  | 50%+  | 35%+   | > 25%               |
| E-commerce  | 40%+  | 20%+  | 10%+   | > 8%                |

### Scoring
| D30 Retention vs Benchmark | Score |
|---------------------------|-------|
| 2x+ above threshold       | 5     |
| 1.5-2x above threshold    | 4     |
| At or slightly above       | 3     |
| Below threshold but stable | 2     |
| Declining toward zero      | 1     |

## 3. NPS as PMF Proxy

Net Promoter Score provides a quick proxy for product-market fit sentiment.

- **NPS > 50**: Strong PMF signal — users are actively promoting the product
- **NPS 30-50**: Moderate PMF — product is liked but not yet loved
- **NPS 0-30**: Weak PMF — users are indifferent
- **NPS < 0**: No PMF — more detractors than promoters

### Relationship Between NPS and Growth
High NPS correlates with organic growth through word-of-mouth. Products with NPS > 50 typically see 20-40% of new users coming from referrals.

### Scoring
| NPS Range | Score |
|-----------|-------|
| 70+       | 5     |
| 50-69     | 4     |
| 30-49     | 3     |
| 10-29     | 2     |
| Below 10  | 1     |

## 4. Engagement Depth

Engagement metrics reveal whether users are integrating the product into their routines.

### Key Metrics
- **DAU/MAU Ratio**: Measures daily engagement intensity
  - > 25% is strong (indicates daily habit)
  - 15-25% is moderate
  - < 15% suggests weak engagement
- **Session Frequency**: How often users return per week
- **Feature Breadth Usage**: Percentage of core features used by average user
- **Time in Product**: Average session duration (context-dependent)

### Scoring
| DAU/MAU | Score |
|---------|-------|
| 30%+    | 5     |
| 25-29%  | 4     |
| 20-24%  | 3     |
| 15-19%  | 2     |
| Below 15%| 1    |

## 5. Revenue-Based PMF Signals

Revenue patterns are the ultimate PMF validation for monetized products.

### Key Indicators
- **Expansion Revenue**: Existing customers spending more over time (upsells, cross-sells, seat expansion)
- **Negative Net Churn**: Revenue gained from expansion exceeds revenue lost from churn — the holy grail of SaaS
- **Organic Growth Rate**: Percentage of new revenue from non-paid channels (word-of-mouth, referrals, inbound)
- **Willingness to Pay**: Customers accept price increases without significant churn
- **Short Sales Cycles**: Deals close faster as product reputation grows

### Scoring
| Revenue Signal Strength | Score |
|------------------------|-------|
| Negative net churn + strong expansion | 5 |
| Positive expansion revenue, low churn | 4 |
| Stable revenue, moderate churn        | 3 |
| Flat or declining revenue             | 2 |
| High churn, no expansion              | 1 |

## PMF Scorecard

Combine all five signals into a single scorecard for a holistic PMF assessment.

```
## PMF Scorecard: [Product Name]
Date: [Assessment Date]

| Dimension              | Score (1-5) | Evidence / Notes          |
|------------------------|-------------|---------------------------|
| Sean Ellis Test        |             |                           |
| Retention Curve        |             |                           |
| NPS                    |             |                           |
| Engagement Depth       |             |                           |
| Revenue Signals        |             |                           |
| **TOTAL**              | **__/25**   |                           |

### Interpretation
- 20-25: Strong PMF — ready to scale
- 15-19: Emerging PMF — iterate and strengthen
- 10-14: Weak PMF — major product changes needed
- Below 10: No PMF — revisit problem-solution fit

### Key Strengths
- [What's working well]

### Key Gaps
- [Where PMF is weakest]

### Recommended Actions
1. [Top priority action]
2. [Second priority]
3. [Third priority]
```

## Input Format
Use $ARGUMENTS to pass:
- Product name and description
- Current metrics (retention rates, NPS, DAU/MAU, revenue data)
- Sean Ellis survey results (if available)
- Target user segment
- Stage of product (early, growth, mature)

## Output
A completed PMF Scorecard with:
- Score for each of the five dimensions with supporting evidence
- Total score and interpretation
- Key strengths and gaps identified
- Prioritized recommendations for improving PMF
- Comparison to benchmarks for the product category

## Tips
- Not all dimensions apply equally to every product — pre-revenue products can skip Revenue Signals and weight other dimensions more heavily
- Track the scorecard over time to see trajectory, not just a snapshot
- Segment the scorecard by user persona — PMF may exist for one segment but not another
- The Sean Ellis Test is the single most reliable signal if you can only measure one thing
- Combine quantitative scores with qualitative user feedback for the fullest picture

---

### Further Reading

- [Product-Market Fit: The Ultimate Guide with a New Framework](https://www.productcompass.pm/p/product-market-fit-guide-framework)
- [The Superhuman Product/Market Fit Engine](https://review.firstround.com/how-superhuman-built-an-engine-to-find-product-market-fit)
