---
name: value-proposition-canvas
description: "Design and evaluate value propositions using the Value Proposition Canvas (Strategyzer). Maps customer jobs, pains, and gains to your products, pain relievers, and gain creators to achieve fit between what customers need and what you offer."
---

## Value Proposition Canvas

A structured framework for designing value propositions that customers actually want. Based on the Value Proposition Canvas by Alexander Osterwalder (Strategyzer). Use this to ensure your solution maps directly to validated customer needs.

### Domain Context

The Value Proposition Canvas is a tool for designing, testing, and iterating value propositions. It zooms into the relationship between the customer segment and the value proposition — the two most critical building blocks of any business model.

The canvas has two sides that must achieve **FIT**:
- **Customer Profile** (right side) — What matters to the customer
- **Value Map** (left side) — How your solution delivers value

This framework builds on Jobs-to-Be-Done (JTBD) concepts. The customer profile captures the "jobs" customers are trying to get done, while the value map describes how your solution helps them accomplish those jobs better than alternatives.

### Customer Profile

#### Customer Jobs

What the customer is trying to get done in their work or life. There are three types:

**Functional Jobs**: The practical tasks and problems customers are trying to solve.
- "I need to track my team's progress across multiple projects"
- "I need to find flights that fit my budget and schedule"
- "I need to file my quarterly taxes accurately"

**Social Jobs**: How customers want to be perceived by others.
- "I want to look competent in front of my team"
- "I want to be seen as innovative by my peers"
- "I want my manager to see I deliver results"

**Emotional Jobs**: How customers want to feel.
- "I want to feel in control of my finances"
- "I want to feel confident about my product decisions"
- "I want to feel less stressed about deadlines"

**Ranking**: Not all jobs are equal. Rank by importance (how critical to the customer) and frequency (how often they face this job).

#### Pains

The negative outcomes, obstacles, and risks customers experience related to their jobs.

**Undesired outcomes**: Things that go wrong or feel wrong.
- "I waste 2 hours per week in status meetings that could be async"
- "I lose track of decisions made in Slack threads"

**Obstacles**: Things that prevent customers from getting started or completing jobs.
- "I do not have access to real-time data"
- "The tool is too complex for non-technical team members"

**Risks**: Potential negative consequences customers worry about.
- "I might make a decision based on outdated information"
- "I might miss a critical bug before launch"

**Ranking**: Rate pains by severity (how much it hurts) and frequency (how often it occurs). Focus on extreme pains first.

#### Gains

The positive outcomes, benefits, and expectations customers desire.

**Required gains**: Minimum expectations that must be met.
- "The tool must be accessible from mobile"
- "Reports must be accurate"

**Expected gains**: What customers anticipate based on experience with alternatives.
- "I expect to see progress dashboards similar to Jira"
- "I expect onboarding to take less than a day"

**Desired gains**: Things customers would love but do not expect.
- "I wish I could get AI-generated status updates"
- "I wish the tool could predict delivery risks"

**Unexpected gains**: Things customers have not imagined but would value.
- "What if the tool could automatically detect scope creep?"
- "What if it could suggest optimal team composition?"

**Ranking**: Rate gains by relevance (how much customers care) and frequency (how often they would benefit). Distinguish between must-haves and nice-to-haves.

### Value Map

#### Products & Services

The specific products, services, and features you offer that help customers get their jobs done.

List all the components of your offering:
- Core features and functionality
- Supporting services (onboarding, support, training)
- Content and resources
- Integrations and ecosystem

**Ranking**: Rate by importance to the value proposition. Not all features contribute equally.

#### Pain Relievers

How your products and services specifically alleviate customer pains.

For each pain identified in the Customer Profile, describe:
- **Which pain it addresses**: Map directly to a specific pain
- **How it relieves the pain**: The mechanism of relief
- **How much it relieves**: Does it eliminate the pain or just reduce it?

Example:
- Pain: "I waste 2 hours/week in status meetings"
- Pain Reliever: "Automated async status updates pull from work tools, eliminating the need for status meetings entirely"

#### Gain Creators

How your products and services create customer gains.

For each gain identified in the Customer Profile, describe:
- **Which gain it creates**: Map directly to a specific gain
- **How it creates the gain**: The mechanism of creation
- **How much it creates**: Does it fully deliver the gain or partially?

Example:
- Gain: "I wish I could predict delivery risks"
- Gain Creator: "ML model analyzes historical sprint data and flags at-risk items 1 week before deadline"

### Achieving FIT

FIT occurs when customers get excited about your value proposition — when your pain relievers and gain creators match the jobs, pains, and gains that matter most to customers.

#### Three Levels of Fit

| Level | Name | Definition | Evidence |
|-------|------|-----------|----------|
| 1 | Problem-Solution Fit on Paper | Your value map addresses the most important jobs, pains, and gains | Customer interviews confirm alignment |
| 2 | Problem-Solution Fit in Market | Customers respond positively to your value proposition | Prototype tests, landing page conversions, letter-of-intent |
| 3 | Product-Market Fit | Your business model is scalable and profitable | Revenue growth, retention, unit economics |

#### Fit Scoring Criteria

Score the quality of fit between each side of the canvas:

| Criteria | Score 1 | Score 3 | Score 5 |
|----------|---------|---------|---------|
| Job coverage | Addresses <30% of important jobs | Addresses 50-70% of important jobs | Addresses >80% of important jobs |
| Pain relief | Relieves minor pains only | Relieves some severe pains | Relieves the top 3 most severe pains |
| Gain creation | Creates only expected gains | Creates expected + some desired gains | Creates unexpected gains that delight |
| Specificity | Generic value proposition | Targeted to a segment | Tailored to a specific persona |
| Differentiation | Similar to all alternatives | Better than most alternatives in 1-2 areas | Uniquely solves a pain no one else addresses |

**Total Fit Score (5-25)**:
- 20-25: Strong fit — proceed to prototype and test
- 15-19: Moderate fit — identify and close gaps
- 10-14: Weak fit — significant redesign needed
- Below 10: No fit — reconsider the value proposition entirely

### Iterating When Fit Is Weak

When fit is weak, follow this process:

1. **Identify the biggest gap** — Which pains are unaddressed? Which jobs are ignored?
2. **Challenge your assumptions** — Are the jobs/pains/gains based on real customer evidence or assumptions?
3. **Explore alternative solutions** — Can you address the same jobs/pains/gains differently?
4. **Narrow the segment** — Would fit improve with a more specific customer segment?
5. **Re-interview customers** — Go back to customers and test your updated value proposition
6. **Repeat** — Iterate until fit score reaches 15+ before investing in development

### Instructions

You are helping a product team design a value proposition for **$ARGUMENTS**.

### Input Requirements

- A description of the target customer segment or persona
- The customer problem or need (ideally validated through research)
- The proposed solution or product concept
- Optionally: existing customer research, interview transcripts, or survey data

### Process

1. **Build the Customer Profile** — Map the customer's functional, social, and emotional jobs. Identify their top pains and gains. Rank by importance and frequency.

2. **Build the Value Map** — List your products and services. For each customer pain, describe how you relieve it. For each customer gain, describe how you create it.

3. **Assess fit** — Score the fit between the two sides using the fit scoring criteria. Identify gaps where pains are unrelieved or gains are uncreated.

4. **Prioritize improvements** — For weak areas, suggest specific changes to the value proposition that would improve fit.

5. **Document the canvas** — Present the complete canvas in a clear format:

```
## Value Proposition Canvas

### Customer Profile

**Customer Segment**: [target segment/persona]

#### Jobs
| # | Job | Type | Importance | Frequency |
|---|-----|------|-----------|-----------|

#### Pains
| # | Pain | Severity | Frequency |
|---|------|----------|-----------|

#### Gains
| # | Gain | Type | Relevance |
|---|------|------|-----------|

### Value Map

**Solution**: [product/service name]

#### Products & Services
- [list]

#### Pain Relievers
| # | Pain Addressed | How Relieved | Relief Level |
|---|---------------|-------------|-------------|

#### Gain Creators
| # | Gain Created | How Created | Creation Level |
|---|-------------|-------------|---------------|

### Fit Assessment
| Criteria | Score (/5) | Evidence |
|----------|-----------|----------|
| Job coverage | | |
| Pain relief | | |
| Gain creation | | |
| Specificity | | |
| Differentiation | | |
| **Total** | **/25** | |

### Gaps & Recommendations
[Prioritized list of improvements]
```

Think step by step. Save as markdown if substantial.

---

### Further Reading

- [Value Proposition Design](https://www.strategyzer.com/library/value-proposition-design) by Alexander Osterwalder et al.
- [Jobs to Be Done: Theory to Practice](https://jobs-to-be-done-book.com/) by Anthony Ulwick
- [The Lean Product Playbook](https://leanproductplaybook.com/) by Dan Olsen
- [What Is Product Discovery? The Ultimate Guide Step-by-Step](https://www.productcompass.pm/p/what-exactly-is-product-discovery)
