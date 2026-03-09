---
name: core-value-deepening
description: "Framework for identifying and strengthening a product's core value. Covers feature-retention correlation analysis, value amplification, feature auditing, deepening vs widening strategies, opportunity scoring for prioritization, and pricing alignment."
---
# Core Value Deepening

## Overview
Every product that achieves product-market fit does so because of a specific core value — the primary reason users keep coming back. This skill provides a structured framework for identifying that core value, amplifying it, removing distractions, and ensuring your entire product strategy is aligned around deepening it.

## When to Use
- After identifying initial PMF signals to strengthen them
- When retention is flattening but not yet at target levels
- During product strategy planning to focus the roadmap
- When the product has grown complex and needs re-focusing
- Before pricing changes to ensure value-price alignment

## 1. Core Value Identification

### Feature-Retention Correlation Analysis
Identify which features and behaviors correlate most strongly with long-term retention:

1. **Define retained users**: Users active at Day 30+ (or your relevant retention window)
2. **Compare behaviors**: What do retained users do that churned users do not?
3. **Rank features by correlation**: For each feature, calculate the retention rate of users who used it vs those who did not
4. **Identify the core action**: The single feature or behavior with the highest retention correlation

### Power User Analysis
Study your most engaged users to understand what drives deep engagement:
- What features do they use most frequently?
- What workflows have they built around your product?
- How do they describe the product to others?
- What would they miss most if the product disappeared?
- What did they do in their first week that others did not?

### Core Value Statement
Synthesize findings into a clear core value statement:
> "[Product] helps [specific users] achieve [specific outcome] by [specific mechanism], which no alternative delivers as well because [unique advantage]."

## 2. Value Amplification

Once you know the core value, make it more prominent, accessible, and delightful.

### Reduce Friction to Core Experience
- **Audit the path**: Map every step from login to core value delivery. Remove or simplify every step that is not essential.
- **Pre-load value**: Show the core value immediately on login (dashboards, notifications, content feeds) rather than requiring users to navigate to it
- **Eliminate setup barriers**: Auto-configure defaults, import data from other tools, pre-populate templates
- **Speed optimization**: Make the core experience faster — every 100ms of latency reduces engagement

### Make Core Value More Prominent
- **Default to core**: Ensure the product opens to the core experience, not a settings page or empty state
- **Visual hierarchy**: The core value should occupy the most prominent screen real estate
- **Notifications and digests**: Proactively surface core value through notifications, emails, and summaries
- **Remove distractions**: Secondary features should not compete for attention with the core experience

### Delight and Polish
- **Micro-interactions**: Add satisfying feedback for core actions (animations, sounds, progress indicators)
- **Exceed expectations**: Find small ways the core experience can surprise and delight
- **Reliability**: The core experience must be the most reliable part of the product — zero downtime, zero bugs

## 3. Feature Audit

Categorize every feature by its relationship to core value and usage data.

### Feature Categorization Matrix
| | High Usage | Low Usage |
|---|-----------|-----------|
| **High Core Value Impact** | **Amplify**: Invest heavily, make even better | **Promote**: Users don't know about it — improve discoverability |
| **Low Core Value Impact** | **Maintain**: Users like it but it's not driving PMF — keep but don't invest | **Kill/Sunset**: Adding complexity without value — remove it |

### Kill/Sunset Criteria
A feature should be considered for removal if:
- Less than 5% of active users engage with it monthly
- It does not correlate with retention
- It adds complexity to onboarding or navigation
- It requires ongoing maintenance or support resources
- Removing it would simplify the core experience

### Process for Sunsetting Features
1. Analyze usage data and identify candidates
2. Communicate with affected users (the 5%) to understand their use case
3. Determine if the use case can be served by the core experience or an integration
4. Announce deprecation with timeline (30-90 days)
5. Remove and measure impact on core metrics

## 4. Deepening vs Widening Strategies

Two paths for growing after initial PMF — choose based on your situation.

### Go Deeper (More Capability in Core Area)
**When to choose**:
- Core value is clear but users want more power, speed, or sophistication
- Competitors are catching up on your core capability
- Power users are hitting limitations and requesting advanced features
- The core use case has untapped depth

**Examples**:
- Figma adding auto-layout, components, and design systems (deeper design capability)
- Notion adding databases, relations, and formulas (deeper knowledge management)
- Linear adding cycles, projects, and roadmaps (deeper project tracking)

### Go Wider (Adjacent Use Cases)
**When to choose**:
- Core value is strong and well-defended
- Users are already using the product for adjacent tasks (hacking workarounds)
- Adjacent use cases share the same user and data model
- Market size of core use case is limited

**Examples**:
- Slack expanding from messaging to workflows and app platform
- Zoom expanding from meetings to phone, chat, and events
- Shopify expanding from storefront to payments, shipping, and capital

### Decision Framework
| Factor | Go Deeper | Go Wider |
|--------|-----------|----------|
| Core value defensibility | Weak — need to strengthen | Strong — well-defended |
| User requests | "Make it more powerful" | "I wish it also did X" |
| Competitive pressure | On core capability | On adjacent capabilities |
| Core market size | Large and underserved | Nearing saturation |
| Data/infra reuse | High for depth features | High for adjacent features |

## 5. Prioritization for Core Value

Use Opportunity Score to prioritize improvements that deepen the core experience.

### Opportunity Score Formula
**Opportunity Score = Importance x (1 - Satisfaction)**

Where:
- **Importance** (0-1): How important is this job/outcome to the user? (Survey data or inferred from behavior)
- **Satisfaction** (0-1): How satisfied are users with the current solution? (Survey data, NPS for feature, support tickets)

### Process
1. List all jobs-to-be-done related to the core value
2. Survey users on importance and satisfaction for each
3. Calculate Opportunity Score
4. Prioritize: High importance + Low satisfaction = Biggest opportunity

### Example Scoring
| Job-to-be-Done | Importance | Satisfaction | Opportunity Score |
|----------------|------------|--------------|-------------------|
| [Job 1] | 0.9 | 0.3 | 0.63 |
| [Job 2] | 0.8 | 0.7 | 0.24 |
| [Job 3] | 0.7 | 0.2 | 0.56 |
| [Job 4] | 0.5 | 0.4 | 0.30 |

**Interpretation**: Job 1 and Job 3 represent the highest-opportunity improvements — important to users but poorly served today.

## 6. Pricing Alignment

Ensure pricing reflects and reinforces the core value delivered.

### Value Metric Selection
The pricing metric should correlate with the value users receive:
- **Good value metrics**: Seats, active users, messages sent, storage used, projects created — things that scale with value
- **Bad value metrics**: Flat pricing regardless of usage, features that don't correlate with value, arbitrary tier boundaries

### Alignment Checklist
- [ ] Users who get more value pay more (value-price correlation)
- [ ] Free/starter tier delivers enough core value to demonstrate PMF
- [ ] Upgrade triggers align with deepening engagement (not arbitrary limits)
- [ ] Pricing tiers map to distinct user segments with different needs
- [ ] Price increases are justified by increased value delivery

### Pricing Tier Structure
| Tier | Target Segment | Core Value Access | Value Metric |
|------|---------------|-------------------|-------------|
| Free/Starter | Individual/trial | Limited core experience | [metric] up to [limit] |
| Growth | Small team/regular use | Full core experience | [metric] up to [limit] |
| Business | Team/power users | Core + advanced features | [metric] up to [limit] |
| Enterprise | Organization-wide | Full platform | Unlimited or custom |

## Input Format
Use $ARGUMENTS to pass:
- Product name and description
- Core value hypothesis (if known)
- Feature usage data (which features are used by what % of users)
- Retention data (overall and by feature usage)
- Current pricing structure
- User feedback themes

## Output
A core value deepening plan including:
- Identified core value with supporting evidence
- Value amplification recommendations
- Feature audit results with kill/invest/promote recommendations
- Deepening vs widening strategy recommendation
- Opportunity-scored prioritization of core value improvements
- Pricing alignment assessment and recommendations

## Tips
- The core value is often not what you think it is — let the data speak
- Removing features can improve PMF by reducing complexity and focusing attention
- Power user interviews are the richest source of core value insights
- Pricing should feel fair to users — if they complain about price, the value-price alignment is off
- Re-evaluate core value annually — it can shift as the market and product evolve

---

### Further Reading

- [Product-Market Fit: The Ultimate Guide with a New Framework](https://www.productcompass.pm/p/product-market-fit-guide-framework)
- [How to Design a Value Proposition Customers Can't Resist?](https://www.productcompass.pm/p/how-to-design-value-proposition-template)
