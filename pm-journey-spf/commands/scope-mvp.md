---
description: "Define MVP scope with core features, priorities, and success criteria — a focused scoping exercise"
argument-hint: "<solution concept or feature list>"
---

# /scope-mvp -- MVP Scoping Exercise

A focused 10-minute exercise to define your MVP scope. Takes a solution concept or feature list and produces a clear scope document with must-have features, priorities, and success criteria.

## Invocation

```
/scope-mvp AI-powered meeting summarizer that sends action items to Slack
/scope-mvp We have 12 feature ideas for our scheduling tool — need to cut to MVP
/scope-mvp [upload a solution concept, feature list, or PSF outputs]
```

## Workflow

### Step 1: Capture the Solution Concept

Accept $ARGUMENTS as the solution concept. If the input is a feature list, treat it as candidate features to prioritize. If it is a high-level concept, help break it into candidate features first.

Ask only the essentials:
1. Who is the target user?
2. What is the single most important thing this product must do?
3. What is your biggest unknown or risk?

### Step 2: Apply MVP Scoping

Use the **mvp-scoping** skill to:
- Map the user journey and identify the walking skeleton
- Run the Riskiest Assumption Test
- Prioritize with MoSCoW (Must / Should / Could / Won't)
- Decide MVP vs MLP approach
- Define success criteria

### Step 3: Output the Scope Document

Deliver a clean, actionable MVP scope document the user can share with their team immediately.

Include:
- Target user and core JTBD
- Must-have features (max 3-5) with rationale
- Explicitly out-of-scope items
- Success criteria with measurable targets
- Recommended approach (MVP or MLP) with rationale
- Estimated effort (T-shirt size)

### What's Next?

- Set KPIs for your MVP using `/run-spf` (which includes the **kpi-framework** skill)
- Write a PRD for the scoped features using the PRD writing command from pm-execution
- Break features into user stories using the user stories skill from pm-execution
