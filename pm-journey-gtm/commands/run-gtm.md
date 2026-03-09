---
description: "Run a full Go To Market cycle — from GTM strategy through organizational alignment, launch execution, and business scaling"
argument-hint: "<product with PMF or PMF assessment outputs>"
---

# /run-gtm -- Go To Market Cycle

Run the complete Go To Market journey — the final stage of the Fit Journey framework (CPF > PSF > SPF > PMF > GTM). This command takes a product with validated product-market fit and guides you through GTM strategy, organizational alignment, unit economics, and scaling roadmap creation.

## Invocation

```
/run-gtm B2B analytics platform with validated PMF among mid-market e-commerce companies
/run-gtm [upload PMF assessment, ICP definition, or GTM strategy docs]
/run-gtm Consumer fintech app ready to scale beyond early adopters
```

## Workflow

### Step 1: Understand Context

Accept and review inputs from the PMF stage or gather product context:

Ask:
- What product are you taking to market?
- What evidence of product-market fit do you have? (retention curves, Sean Ellis score, NPS, revenue growth, user engagement data)
- Who is your Ideal Customer Profile (ICP)?
- What is the core value your product delivers?
- What is your current pricing model?
- What growth levers have you identified?
- What is your timeline and resource availability?

If the user provides PMF outputs or strategy documents, read them first and use them as the foundation for all subsequent steps.

### Step 2: Design GTM Strategy

Develop the go-to-market strategy using established GTM frameworks. Consider using the GTM strategy skill from pm-go-to-market for a comprehensive strategy covering marketing channels, messaging, success metrics, and launch timeline. Also consider the GTM motions skill from pm-go-to-market to identify the right go-to-market motions (product-led, sales-led, community-led, or hybrid).

Key outputs:
- GTM motion selection and rationale
- Channel strategy with prioritization
- Launch timeline with phases
- Success metrics and targets

### Step 3: Define Positioning and Messaging

Craft positioning and messaging that resonates with your validated ICP. Consider using the positioning ideas skill from pm-marketing-growth for positioning framework exploration and the value prop statements skill from pm-marketing-growth for compelling value proposition development.

Key outputs:
- Positioning statement
- Messaging framework by persona
- Key differentiators and proof points

### Step 4: Create Competitive Materials

Build sales enablement materials for competitive situations. Consider using the competitive battlecard command from pm-go-to-market to create detailed competitive battlecards for top competitors.

Key outputs:
- Competitive landscape overview
- Battlecards for top 3-5 competitors
- Win/loss analysis framework

### Step 5: Align the Organization

Apply the **cross-functional-alignment** skill:

- Build stakeholder communication plans for every team (marketing, sales, support, engineering, legal)
- Create the launch readiness checklist and score each area Red/Yellow/Green
- Draft internal launch communications (all-hands and team-specific briefings)
- Define ongoing alignment cadence (weekly sync, monthly review, quarterly planning)

### Step 6: Set Business KPIs

Apply the **unit-economics** skill:

- Calculate Customer Acquisition Cost (CAC) — blended and by channel
- Calculate Customer Lifetime Value (LTV) — using the most appropriate method for the business stage
- Evaluate LTV:CAC ratio and payback period
- Analyze contribution margin and channel ROI
- Produce the unit economics dashboard with targets and tracking plan

### Step 7: Plan Scaling Roadmap

Apply the **scaling-roadmap** skill. Also consider using the outcome roadmap command from pm-execution for outcome-based roadmap creation and the brainstorm OKRs command from pm-execution for defining scaling-phase OKRs.

- Define roadmap philosophy (outcome-based, time horizons with confidence levels)
- Map scaling dimensions: market expansion, product expansion, revenue expansion
- Prioritize initiatives using RICE at scale
- Create roadmap views for different audiences (executive, team, customer-facing)
- Set review cadence

### Step 8: Launch Decision Gate

Based on the launch readiness checklist from Step 5, make a launch recommendation:

| Decision | Criteria | Action |
|----------|----------|--------|
| **LAUNCH** | All areas Green or Yellow, no Red blockers | Proceed with full launch on target date |
| **SOFT LAUNCH** | Some Yellow areas, manageable risk | Launch to a limited segment first, expand as Yellow items resolve |
| **DELAY** | Any Red areas that block launch | Resolve Red items before proceeding; set revised target date |

### Step 9: Generate GTM Execution Plan

Produce the comprehensive output document:

```
## GTM Execution Plan: [Product Name]

**Stage**: Go To Market (Fit Journey Stage 5/5)
**PMF Evidence**: [summary of PMF validation]
**Launch Decision**: [LAUNCH / SOFT LAUNCH / DELAY]
**Target Date**: [date]

### GTM Strategy Summary
**Motion**: [product-led / sales-led / hybrid]
**Beachhead Segment**: [segment]
**ICP**: [profile summary]
**Positioning**: For [who] who [need], [product] is [category] that [benefit].

### Channel Strategy
| Channel | Priority | Expected CAC | Rationale |
|---------|----------|-------------|-----------|

### Launch Readiness
| Area | Status | Owner | Notes |
|------|--------|-------|-------|
| Product | [R/Y/G] | | |
| Marketing | [R/Y/G] | | |
| Sales | [R/Y/G] | | |
| Support | [R/Y/G] | | |
| Legal | [R/Y/G] | | |
| Analytics | [R/Y/G] | | |

### Unit Economics Targets
| Metric | Current | 90-Day Target | 12-Month Target |
|--------|---------|--------------|----------------|
| CAC | $ | $ | $ |
| LTV | $ | $ | $ |
| LTV:CAC | x:1 | x:1 | x:1 |
| Payback | # mo | # mo | # mo |
| Contribution Margin | % | % | % |

### Scaling Roadmap
**Now (This Quarter)**: [top 3 initiatives]
**Next (Next Quarter)**: [top 3 planned initiatives]
**Later (2-4 Quarters)**: [strategic themes]

### Post-Launch Cadence
- Weekly: Cross-functional sync
- Monthly: Business review with unit economics
- Quarterly: Roadmap review and reprioritization

### Risks and Mitigations
| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|-----------|
```

Save as markdown.

### Step 10: Offer Next Steps

This is the final stage of the Fit Journey. Suggest continued use of individual skills for ongoing optimization:

- "Want me to **deep-dive into unit economics** with your actual business data? Use `/check-unit-economics`"
- "Need to create competitive battlecards for your sales team? Try the battlecard command in pm-go-to-market"
- "Want to design growth loops for sustainable traction? Try the growth strategy command in pm-go-to-market"
- "Need detailed OKRs for the scaling phase? Try the brainstorm OKRs command in pm-execution"
- "Want to build a metrics dashboard for ongoing tracking? Try the analytics skills in pm-data-analytics"

## Notes

- This command works best with PMF validation outputs as input — the stronger the PMF evidence, the more targeted the GTM plan
- GTM is not a one-time event but an ongoing cycle of strategy, execution, measurement, and optimization
- The launch readiness checklist is a living document — update it daily in the weeks before launch
- Unit economics should be re-evaluated monthly during the scaling phase
- The scaling roadmap should be reviewed quarterly and adjusted based on market feedback
- Cross-functional alignment requires ongoing investment — the weekly sync is non-negotiable
