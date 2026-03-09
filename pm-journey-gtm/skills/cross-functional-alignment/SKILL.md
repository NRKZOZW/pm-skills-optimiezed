---
name: cross-functional-alignment
description: "Framework for aligning all departments for a successful market launch and ongoing scaling. Covers stakeholder communication plans, launch readiness checklists, internal announcements, and ongoing alignment cadence to ensure every team is prepared and synchronized."
---

## Cross-Functional Alignment

Align every department around a shared launch plan so that marketing, sales, support, engineering, and leadership move in lockstep. A brilliant product with poor cross-functional alignment launches into chaos — missed handoffs, conflicting messages, and surprised stakeholders erode both customer trust and team morale.

### Domain Context

Cross-functional alignment is the connective tissue between product strategy and market execution. After achieving product-market fit, the challenge shifts from "does anyone want this?" to "can every part of the organization deliver on the promise at scale?" This skill provides the communication structures, readiness gates, and cadences that prevent the most common launch failures.

### Context

You are helping the user build a cross-functional alignment plan for **$ARGUMENTS**.

If the user provides files (GTM strategies, launch plans, organizational charts, PMF outputs), read them first and incorporate relevant context.

### Instructions

#### Step 1: Map Stakeholders and Information Needs

Ask the user:
- What are you launching? (new product, major feature, market expansion, pricing change)
- Which teams are involved? (marketing, sales, support, engineering, legal, finance, leadership)
- What is the launch timeline?
- Have any teams already been briefed, or is this the first alignment effort?

Then build a Stakeholder Communication Plan. For each team, define what information they need, when they need it, and in what format.

**Marketing**:
- Positioning statement and messaging framework
- Target audience definition and segmentation
- Competitive differentiation talking points
- Content calendar with pre-launch, launch, and post-launch phases
- Brand guidelines and approved assets
- Campaign briefs with channel-specific messaging

**Sales**:
- Product feature overview and key benefits by persona
- Pricing structure, packaging, and discounting guidelines
- Objection handling playbook (top 10 objections with responses)
- Demo scripts and talk tracks for different buyer personas
- Competitive battlecards for top 3-5 competitors
- Customer qualification criteria and lead scoring updates

**Customer Support / Success**:
- FAQ document covering expected customer questions
- Known issues and limitations with workarounds
- Escalation paths and severity definitions
- Onboarding guides and setup documentation
- Support ticket tagging and routing updates
- Customer health score adjustments for new features

**Engineering**:
- Post-launch monitoring plan (metrics, alerts, thresholds)
- Incident response protocol with on-call rotation
- Feature flag and rollout strategy (phased vs. big-bang)
- Performance benchmarks and scalability targets
- Bug triage process and severity classification for launch issues
- Feature pipeline visibility for post-launch iterations

**Legal / Compliance**:
- Terms of service updates
- Privacy policy changes
- Regulatory compliance requirements
- Data processing agreements
- Marketing claim approvals

**Leadership / Executives**:
- One-page launch summary (what, why, when, expected impact)
- Key risks and mitigation strategies
- Success metrics and reporting cadence
- Resource requirements and budget impact

#### Step 2: Launch Readiness Checklist

Score each area as Red (not ready, blocks launch), Yellow (in progress, manageable risk), or Green (ready).

| Area | Checklist Items | Status |
|------|----------------|--------|
| **Product** | All P0 bugs resolved; performance meets SLAs; scalability tested for projected load; feature flags configured; rollback plan documented | R/Y/G |
| **Marketing** | Website updated; launch content created; campaigns scheduled; press/analyst briefings done; social media posts queued | R/Y/G |
| **Sales** | Sales materials distributed; team trained on demo and objection handling; pricing live in CRM; territory/account assignments updated | R/Y/G |
| **Support** | Documentation published; FAQ live; support team trained; escalation paths tested; ticket routing configured | R/Y/G |
| **Legal** | Terms of service updated; privacy policy current; compliance sign-off received; marketing claims approved | R/Y/G |
| **Analytics** | Tracking implemented and QA'd; dashboards built; alerts configured; baseline metrics captured; reporting cadence defined | R/Y/G |

**Launch Decision Rule**:
- All Green: Full launch
- Any Yellow, no Red: Launch with monitoring — assign owners to resolve Yellow items within first week
- Any Red: Delay launch until Red items are resolved, or descope to avoid Red areas

#### Step 3: Internal Launch Communication

Create templates for two types of internal communication:

**All-Hands Announcement** (company-wide):
```
Subject: [Launch Name] — Launching [Date]

What: [One-sentence description of what is launching]
Why: [Business impact and customer value]
When: [Exact date and time, with timezone]
Who it affects: [Which customers/segments]

Key talking points:
1. [Most important thing everyone should know]
2. [Second most important thing]
3. [Third most important thing]

What to do:
- [Action item for most employees, e.g., "Read the FAQ"]
- [Where to direct customer questions]
- [Who to contact with internal questions]

Resources: [Link to launch hub/wiki page]
```

**Team-Specific Briefing** (per department):
```
Subject: [Launch Name] — [Team Name] Briefing

Your role in this launch:
- [Specific responsibilities for this team]

Timeline for your team:
- [Date]: [Action required]
- [Date]: [Action required]
- [Date]: [Action required]

Materials:
- [Link to team-specific documents]
- [Link to training materials]

Questions? Contact: [Launch DRI name and channel]
```

#### Step 4: Ongoing Alignment Cadence

Define the recurring meetings and checkpoints that keep teams aligned after launch:

**Weekly Cross-Functional Sync** (30 min):
- Attendees: PM, Marketing lead, Sales lead, Support lead, Engineering lead
- Agenda: Launch metrics review, blockers, customer feedback themes, next-week priorities
- Output: Shared action items with owners and deadlines

**Monthly Business Review** (60 min):
- Attendees: Above + leadership, finance
- Agenda: Unit economics trends, channel performance, customer acquisition and retention, roadmap progress
- Output: Updated forecasts, resource allocation decisions

**Quarterly Planning** (half-day):
- Attendees: Cross-functional leadership team
- Agenda: OKR review, roadmap reprioritization, market landscape update, resource planning
- Output: Updated quarterly plan and OKRs

### Anti-Patterns to Avoid

- **"Build it and they will come"** — launching without sales enablement means deals stall on basic product questions
- **Last-minute briefings** — telling support about the launch the day before guarantees a bad customer experience
- **One-size-fits-all communication** — marketing needs messaging, engineering needs monitoring plans; each team needs information in their language
- **No single DRI** — if everyone owns the launch, nobody owns the launch; assign one Directly Responsible Individual
- **Alignment theater** — meetings without action items and owners create the illusion of coordination without the substance

### Output Format

```
## Cross-Functional Alignment Plan

**Launch**: [name]
**Date**: [target launch date]
**DRI**: [name and role]

### Stakeholder Communication Plan
| Team | Key Information | Delivery Date | Format | Owner |
|------|----------------|---------------|--------|-------|
| Marketing | [items] | [date] | [doc/meeting/async] | [name] |
| Sales | [items] | [date] | [doc/meeting/async] | [name] |
| Support | [items] | [date] | [doc/meeting/async] | [name] |
| Engineering | [items] | [date] | [doc/meeting/async] | [name] |
| Legal | [items] | [date] | [doc/meeting/async] | [name] |

### Launch Readiness Scorecard
| Area | Status | Blocker (if any) | Owner | Resolution Date |
|------|--------|-------------------|-------|-----------------|

### Launch Decision
[LAUNCH / DELAY / SOFT LAUNCH] — [rationale]

### Post-Launch Cadence
[Weekly sync, monthly review, quarterly planning details]
```
