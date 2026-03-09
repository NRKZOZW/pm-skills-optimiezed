---
name: mvp-scoping
description: "Define MVP scope using user story mapping, riskiest assumption testing, and MoSCoW prioritization. Helps PMs draw the line between what must ship now and what can wait, producing a clear scope document with success criteria."
---

## MVP Scoping

Define the Minimum Viable Product scope so your team builds just enough to test the riskiest assumptions and deliver core value. A well-scoped MVP avoids both under-building (shipping something too thin to learn from) and over-building (wasting months on features nobody asked for).

### Domain Context

MVP scoping sits at the intersection of strategy and execution. You have a validated solution concept — now you need to decide exactly what to build first. The goal is not to build the smallest thing possible; it is to build the smallest thing that produces reliable learning about whether users find real value.

### Context

You are helping the user scope an MVP for **$ARGUMENTS**.

If the user provides files (PSF outputs, solution concepts, value propositions, prototype results), read them first and incorporate relevant evidence.

### Instructions

#### Step 1: Understand the Solution Concept

Ask the user:
- What solution are you building? What problem does it solve?
- Who is the target user? What is their core Job to Be Done (JTBD)?
- What assumptions have already been validated (e.g., through PSF)?
- What is the biggest remaining unknown?

#### Step 2: User Story Mapping

Walk through the user journey to identify the minimum end-to-end flow:

1. **List Activities** — the high-level things the user does (e.g., "Discover product," "Set up account," "Complete core task," "See results")
2. **Break into Tasks** — the steps within each activity
3. **Write Stories** — specific user stories for each task
4. **Draw the Walking Skeleton** — identify the minimum set of stories that enable a complete end-to-end flow from first touch to value delivery

```
Activities:   [Activity 1]    [Activity 2]    [Activity 3]    [Activity 4]
              ─────────────   ─────────────   ─────────────   ─────────────
Tasks:        Task A          Task D          Task G          Task J
              Task B          Task E          Task H          Task K
              Task C          Task F          Task I          Task L
              ─────────────────────────────────────────────────────────────
Walking       Story A1        Story D1        Story G1        Story J1
Skeleton:     Story B1        Story E1                        Story K1
```

The walking skeleton is your MVP candidate. Everything below the line is future scope.

#### Step 3: Riskiest Assumption Test (RAT)

Identify and rank the top assumptions that must hold true for the product to succeed:

| # | Assumption | Risk Level | How MVP Tests It |
|---|-----------|------------|------------------|
| 1 | [Riskiest assumption] | Critical | [How this MVP validates or invalidates it] |
| 2 | [Second riskiest] | High | [How this MVP tests it] |
| 3 | [Third riskiest] | Medium | [How this MVP tests it] |

**The MVP must test assumption #1.** If your walking skeleton does not address the riskiest assumption, adjust scope until it does.

#### Step 4: MoSCoW Prioritization

Categorize every candidate feature:

| Priority | Features | Rationale |
|----------|----------|-----------|
| **Must-have** | [3-5 features max] | Without these, the product cannot deliver core value or test the riskiest assumption |
| **Should-have** | [Features for v1.1] | Important for a good experience but not essential for initial learning |
| **Could-have** | [Nice differentiators] | Would delight users but can be added once core value is proven |
| **Won't-have** | [Explicitly out of scope] | Avoid scope creep — write these down so the team knows they are intentionally excluded |

#### Step 5: MVP vs MLP Decision

Help the user decide which approach fits their situation:

| Factor | MVP (Minimum Viable Product) | MLP (Minimum Lovable Product) |
|--------|------------------------------|-------------------------------|
| **Goal** | Learn fast, validate assumptions | Delight users, compete on experience |
| **Best for** | New markets, novel problems, high uncertainty | Crowded markets, known problems, experience-driven categories |
| **Quality bar** | Functional, usable, reliable enough to learn | Polished, delightful, feels like a finished product |
| **Risk** | Users churn because experience is too rough | Over-invest before validating core assumptions |
| **Timeline** | Weeks | Weeks to low months |

**Decision rule**: If the riskiest assumption is "Will users find this valuable?" use MVP. If the riskiest assumption is "Will users choose this over existing alternatives?" lean toward MLP.

#### Step 6: Produce the Scope Document

Output the final MVP scope in the following format.

### Anti-Patterns to Avoid

- **"Let's just add one more feature"** — scope creep is the MVP killer; if it is not Must-have, it waits
- **"We need feature parity with competitors"** — you are not building a competitor, you are testing an assumption
- **"Users won't understand it without X"** — if X is not core to the value test, ship without it and explain with onboarding copy
- **"It's only two more days of work"** — two more days times ten features is two more months

### Output Format

```
## MVP Scope Document

**Product**: [name]
**Target User**: [specific segment]
**Core JTBD**: [job to be done]
**Problem Being Solved**: [validated problem statement]

### Riskiest Assumption
[The #1 assumption this MVP must test]

### Must-Have Features (MVP)
1. [Feature] — [why it's essential]
2. [Feature] — [why it's essential]
3. [Feature] — [why it's essential]

### Explicitly Out of Scope
- [Feature] — [why it's excluded for now]
- [Feature] — [why it's excluded for now]

### Success Criteria
- [Metric]: [target] (e.g., "40% of users complete core flow in first session")
- [Metric]: [target]
- [Metric]: [target]

### Estimated Effort
[T-shirt size or sprint count]

### User Story Map
[Walking skeleton from Step 2]

### Approach
[MVP / MLP] — [rationale]

### Next Steps
- Write a PRD for the Must-have features
- Break Must-haves into user stories
- Set KPIs using the **kpi-framework** skill
```
