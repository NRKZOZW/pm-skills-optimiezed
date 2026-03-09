---
name: scaling-roadmap
description: "Framework for creating a scaling-phase product roadmap. Covers outcome-based planning across market expansion, product expansion, and revenue expansion dimensions with prioritization, communication templates, and anti-patterns to avoid during the growth stage."
---

## Scaling Roadmap

Create a roadmap designed for the scaling phase — where the goal shifts from finding product-market fit to capturing the market opportunity you have validated. A scaling roadmap is outcome-based, not feature-based: every initiative must connect to a business result, and confidence levels determine commitment levels.

### Domain Context

Scaling-phase roadmapping is fundamentally different from early-stage planning. You are no longer exploring whether you have a viable product — you know you do. The challenge now is expanding reach, deepening value, and growing revenue while maintaining the quality and focus that earned product-market fit in the first place. This skill provides the frameworks to plan that expansion thoughtfully.

### Context

You are helping the user build a scaling roadmap for **$ARGUMENTS**.

If the user provides files (PMF evidence, OKRs, business metrics, strategy documents, GTM plans), read them first and incorporate relevant data.

### Instructions

#### Step 1: Understand the Scaling Context

Ask the user:
- What evidence do you have for product-market fit? (retention curves, NPS, Sean Ellis score, revenue growth)
- What are your current business OKRs or top-level goals?
- What is your current market position? (market leader, fast follower, niche player, new entrant)
- What resources are available for scaling? (team size, budget, timeline)
- What constraints exist? (technical debt, organizational capacity, regulatory, geographic)

#### Step 2: Define the Roadmap Philosophy

Establish the planning principles before diving into specifics:

**Outcome-Based, Not Feature-Based**:
- Every roadmap item must answer: "What business or customer outcome does this drive?"
- Features are the how, not the what — the roadmap communicates outcomes, and teams determine the best features to achieve them

**Time Horizons with Confidence Levels**:

| Horizon | Timeframe | Confidence | Commitment | Detail Level |
|---------|-----------|------------|------------|-------------|
| **Now** | This quarter | High (80%+) | Committed — teams are executing | Detailed: specific initiatives, owners, milestones |
| **Next** | Next quarter | Medium (50-80%) | Planned — scoped but flexible | Moderate: defined outcomes, candidate approaches |
| **Later** | 2-4 quarters out | Low (<50%) | Exploratory — directionally aligned | Light: strategic themes and hypotheses |

**Alignment to Business OKRs**:
- Every Now item maps to a current OKR
- Every Next item maps to a planned OKR
- Later items map to strategic themes or vision

#### Step 3: Map Scaling Dimensions

Explore three dimensions of scaling and identify opportunities in each:

**Market Expansion**:

*Adjacent Segments (Bowling Pin Strategy)*:
- Identify your current beachhead segment (the one where you have strongest PMF)
- Map adjacent segments that share characteristics with your beachhead
- Rank adjacencies by: similarity to beachhead, market size, ease of entry, reference potential
- Strategy: dominate one segment completely, then use it as a reference and proof point to enter the next
- Each new segment should require minimal product changes and maximum leverage from existing customers

*Geographic Expansion*:
- When to expand: strong domestic PMF, clear international demand signals, product can be localized
- Localization requirements: language, payment methods, compliance, cultural adaptation
- Go-to-market: partner-led vs. direct entry vs. PLG/self-serve
- Warning: premature internationalization is a common scaling mistake

*New Use Cases*:
- Identify use cases adjacent to your core that existing users are already attempting
- Evaluate: does this use case strengthen the core value or dilute it?
- Validate with existing user data before building

**Product Expansion**:

*Platform Play*:
- When to evolve from product to platform: you have a stable core product, multiple integration requests, potential ecosystem partners
- API strategy: what to expose, pricing, developer experience
- Ecosystem development: marketplace, app store, partner program

*Integrations and Ecosystem*:
- Prioritize integrations by: customer demand, strategic value, implementation effort
- Build vs. partner decision: core differentiators are built, commodity integrations are partnered

*New Product Lines*:
- Adjacent products that serve the same ICP
- Complementary products that increase switching costs
- Evaluate: does this warrant a new product or an extension of the existing one?

**Revenue Expansion**:

*Upsell and Cross-Sell Paths*:
- Identify natural expansion triggers (usage limits, team growth, new departments)
- Design upgrade paths that align with increasing customer value
- Track Net Revenue Retention (NRR) — target >110% for SaaS

*New Pricing Tiers*:
- Enterprise tier: advanced features, security, compliance, SLAs, dedicated support
- Usage-based components: align price with value delivered
- Vertical-specific packaging: bundle features for specific industries

*Enterprise Features*:
- SSO/SAML, audit logs, role-based access, admin controls
- SLAs, dedicated support, custom integrations
- Compliance certifications (SOC 2, HIPAA, GDPR)

#### Step 4: Prioritize for Scale

Apply RICE at scale — a modified prioritization framework for growth-stage decisions:

| Initiative | Impact on North Star | Reach | Confidence | Effort | RICE Score | Priority |
|-----------|---------------------|-------|------------|--------|------------|----------|
| [Initiative 1] | 1-3 | # users affected | H/M/L | # person-weeks | Score | P0/P1/P2 |
| [Initiative 2] | 1-3 | # users affected | H/M/L | # person-weeks | Score | P0/P1/P2 |

**RICE Score** = (Impact × Reach × Confidence) / Effort

**Additional scaling-specific prioritization factors**:
- Does this initiative compound? (e.g., platform features enable partner-built solutions)
- Does this reduce CAC or increase LTV? (direct unit economics impact)
- Does this create a moat? (switching costs, network effects, data advantages)
- Is there a time window? (competitive pressure, market timing, partnership opportunity)

#### Step 5: Communicate the Roadmap

Different audiences need different views:

**Executive Summary** (1 page):
- 3-5 strategic themes for the year
- Key bets and expected outcomes
- Resource allocation across themes
- Risks and dependencies

**Team-Level Detail** (per team/squad):
- Specific initiatives in Now and Next horizons
- Success metrics per initiative
- Dependencies and handoffs
- Technical approach and architecture decisions

**Customer-Facing** (public or for sales):
- Themes and directions, not specific features or dates
- Focus on problems being solved, not solutions being built
- Never commit to dates publicly — use "we're investing in" language
- Update quarterly

**Board / Investor**:
- Strategic narrative: where are we, where are we going, why
- Market opportunity and competitive position
- Key metrics and growth trajectory
- Resource needs and capital allocation

#### Step 6: Define Review Cadence

**Quarterly Roadmap Review** (half-day):
- Review outcomes achieved vs. planned
- Update confidence levels across all horizons
- Reprioritize based on new data, market changes, and resource shifts
- Promote Next items to Now, Later items to Next
- Add new Later items based on strategy evolution

**Monthly Progress Check** (60 min):
- Are Now items on track? Any blockers?
- Has any new data changed our confidence in Next items?
- Quick wins or opportunities to accelerate

**Continuous Reprioritization**:
- New data (customer feedback, competitive moves, market shifts) can trigger immediate reprioritization
- Establish criteria for when to interrupt the current plan vs. when to wait for the next review cycle

### Anti-Patterns to Avoid

- **Feature Factory** — shipping features without measuring outcomes; the roadmap becomes a feature list instead of an outcome plan
- **Shiny Object Syndrome** — chasing every new opportunity instead of deepening what works; discipline is more valuable than creativity at scale
- **Premature Internationalization** — expanding geographically before the core market is dominated; localization costs compound and distract from the main growth engine
- **Scaling Before PMF** — adding go-to-market resources before product-market fit is confirmed; growth spending amplifies both fit and lack of fit
- **Roadmap as Promise** — treating the roadmap as a commitment rather than a plan; the roadmap should change as you learn
- **Peanut Butter Spreading** — distributing resources equally across all initiatives instead of concentrating on the highest-impact bets

### Output Format

```
## Scaling Roadmap

**Product**: [name]
**Planning Horizon**: [current quarter through +4 quarters]
**North Star Metric**: [metric and current value]
**Business OKRs**: [top 2-3 OKRs this roadmap serves]

### Strategic Themes
1. [Theme] — [one-sentence description and expected business impact]
2. [Theme] — [one-sentence description and expected business impact]
3. [Theme] — [one-sentence description and expected business impact]

### Now (This Quarter) — High Confidence, Committed
| Initiative | Theme | Outcome | Success Metric | Owner | Status |
|-----------|-------|---------|---------------|-------|--------|

### Next (Next Quarter) — Medium Confidence, Planned
| Initiative | Theme | Outcome | Success Metric | Dependencies |
|-----------|-------|---------|---------------|-------------|

### Later (2-4 Quarters) — Low Confidence, Exploratory
| Initiative | Theme | Hypothesis | Validation Needed |
|-----------|-------|-----------|------------------|

### Scaling Dimensions
**Market Expansion**: [summary of adjacent segments, geographic plans]
**Product Expansion**: [summary of platform, integrations, new lines]
**Revenue Expansion**: [summary of upsell, pricing, enterprise plans]

### Review Schedule
- Quarterly review: [date]
- Monthly check: [recurring day]
- Reprioritization triggers: [criteria]

### Next Steps
- Align teams on Now commitments
- Use the **unit-economics** skill to validate growth investments
- Use the **cross-functional-alignment** skill to coordinate execution
```
