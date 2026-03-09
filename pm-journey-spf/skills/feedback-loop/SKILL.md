---
name: feedback-loop
description: "Build systematic user feedback collection and analysis processes. Covers channel setup, collection cadence, theme coding, pain-frequency analysis, and a feedback-to-action pipeline that turns insights into prioritized backlog items."
---

## Feedback Loop

Build a systematic process for collecting, analyzing, and acting on user feedback after MVP launch. Raw feedback is noise — a structured feedback loop turns it into signal that drives product decisions.

### Domain Context

Launching an MVP is not the finish line; it is the starting line for learning. Quantitative metrics (from the **kpi-framework** skill) tell you what is happening. User feedback tells you why. A strong feedback loop pairs both data types to produce confident decisions about what to build next, what to fix, and whether the product is on track toward product-market fit.

### Context

You are helping the user build a feedback loop for **$ARGUMENTS**.

If the user provides files (KPI data, survey results, support tickets, user interview notes), read them first and incorporate relevant findings.

### Instructions

#### Step 1: Understand Current State

Ask the user:
- What product or MVP are you collecting feedback for?
- How many active users do you have (rough order of magnitude)?
- What feedback channels already exist? (support inbox, in-app surveys, analytics, etc.)
- What are your top 2-3 questions about user behavior right now?
- Do you have anyone dedicated to user research, or is this PM-led?

#### Step 2: Set Up Feedback Channels

Recommend a mix of channels appropriate to the product's stage and user base:

| Channel | When to Use | Setup Effort | Signal Quality |
|---------|------------|-------------|----------------|
| **In-app Surveys** (trigger-based) | After key moments (first core action, day 7, after task completion) | Medium | High — captures context in the moment |
| **NPS / CSAT** | At regular intervals (monthly NPS, post-interaction CSAT) | Low | Medium — trend data, but lacks detail |
| **User Interviews** | Ongoing cadence (2-4 per week during MVP phase) | High | Very high — deep qualitative insight |
| **Support Ticket Analysis** | Continuous | Low (if support exists) | High — reveals real friction points |
| **Usage Analytics** (behavioral) | Continuous event tracking | Medium-High | High — objective behavioral data |
| **App Store Reviews / Social Media** | Continuous monitoring | Low | Medium — biased toward extremes |
| **Session Recordings** | When investigating specific flows | Medium | High — shows exact user behavior |

**For early MVP (< 100 users)**: Focus on user interviews and behavioral analytics. Volume is too low for meaningful survey data.

**For growing MVP (100-1000 users)**: Add in-app surveys and NPS. You have enough volume for quantitative signals.

**For scaling MVP (1000+ users)**: Use all channels. Segment feedback by user cohort, acquisition source, and usage level.

#### Step 3: Define Collection Cadence

| Frequency | Activity | Owner |
|-----------|----------|-------|
| **Continuous** | Behavioral analytics tracking, support ticket tagging | Engineering / Support |
| **2-4x per week** | User interviews (20-30 minutes each) | PM / Researcher |
| **Weekly** | Review support ticket themes, check analytics dashboards | PM |
| **Bi-weekly** | In-app survey pulse (1-3 questions, triggered contextually) | PM |
| **Monthly** | NPS survey, full feedback synthesis report | PM |
| **Quarterly** | Deep-dive analysis, trend comparison, strategy review | PM + Leadership |

#### Step 4: Analyze Feedback — Theme Coding

Group all feedback (qualitative and quantitative) into themes:

1. **Collect** — Gather all feedback from all channels into a single repository (spreadsheet, Airtable, Productboard, or similar)
2. **Tag** — Assign each item one or more theme tags:
   - Feature requests (grouped by area)
   - Pain points / friction (grouped by user journey stage)
   - Positive feedback (what users love — protect this)
   - Confusion / UX issues
   - Bugs / reliability
3. **Count** — Tally frequency of each theme
4. **Quote** — Save the best verbatim quotes for each theme (useful for stakeholder communication)

#### Step 5: Pain-Frequency Matrix

Plot the top themes on a 2x2 matrix to prioritize:

```
            HIGH FREQUENCY
                 │
    ┌────────────┼────────────┐
    │  MONITOR   │  FIX NOW   │
    │            │            │
    │ Many users │ Many users │
    │ mild pain  │ real pain  │
LOW ├────────────┼────────────┤ HIGH
PAIN│            │            │ PAIN
    │  IGNORE    │ WATCH      │
    │            │            │
    │ Few users  │ Few users  │
    │ mild pain  │ real pain  │
    └────────────┼────────────┘
                 │
            LOW FREQUENCY
```

- **Fix Now** (high pain, high frequency): Top priority. These issues block value delivery for many users.
- **Watch** (high pain, low frequency): Painful for a subset. Monitor whether frequency grows as user base scales.
- **Monitor** (low pain, high frequency): Minor annoyances felt by many. Quick wins if easy to fix.
- **Ignore** (low pain, low frequency): Deprioritize. Revisit only if the pattern changes.

#### Step 6: Feedback-to-Action Pipeline

Turn insights into prioritized backlog items:

1. **Insight** — What did we learn? (State the finding, backed by data and quotes)
2. **Hypothesis** — Why is this happening? (Root cause analysis)
3. **Impact** — How does this affect our KPIs? (Link to North Star and input metrics from the **kpi-framework** skill)
4. **Proposed Action** — What should we build, fix, or change?
5. **Effort** — T-shirt size estimate (S/M/L/XL)
6. **Priority** — Score using Impact / Effort ratio
7. **Backlog Item** — Create a user story or task with context and acceptance criteria

| Insight | Hypothesis | KPI Impact | Action | Effort | Priority |
|---------|-----------|------------|--------|--------|----------|
| [finding] | [root cause] | [metric affected] | [what to do] | [S/M/L/XL] | [score] |

#### Step 7: Produce the Feedback Synthesis Report

Output a synthesis for the current period.

### Anti-Patterns to Avoid

- **Collecting without acting** — feedback that never reaches the backlog erodes user trust and wastes effort
- **Recency bias** — the loudest recent complaint is not necessarily the most important issue
- **Power user bias** — vocal power users do not represent the silent majority; segment your feedback
- **Survey fatigue** — do not survey users more than once per session or more than bi-weekly
- **Ignoring positive feedback** — knowing what users love is as important as knowing what they hate; protect what works

### Output Format

```
## Feedback Synthesis Report

**Product**: [name]
**Period**: [date range]
**Total Feedback Items**: [count]
**Sources**: [channels used]

### Top Themes
| # | Theme | Frequency | Pain Level | Priority |
|---|-------|-----------|------------|----------|
| 1 | [theme] | [count] | [High/Med/Low] | Fix Now |
| 2 | [theme] | [count] | [High/Med/Low] | [priority] |
| 3 | [theme] | [count] | [High/Med/Low] | [priority] |

### Key Quotes
- "[verbatim user quote]" — [user segment, context]
- "[verbatim user quote]" — [user segment, context]
- "[verbatim user quote]" — [user segment, context]

### Pain-Frequency Matrix
[Matrix visualization from Step 5]

### Recommended Actions
| # | Action | Expected KPI Impact | Effort | Priority |
|---|--------|-------------------|--------|----------|
| 1 | [action] | [metric + expected change] | [size] | [score] |
| 2 | [action] | [metric + expected change] | [size] | [score] |
| 3 | [action] | [metric + expected change] | [size] | [score] |

### KPI Update
- North Star Metric: [current value] vs [target] — [on track / behind / ahead]
- Key input metrics: [summary]
- Health guardrails: [all green / any red flags]

### Next Steps
- [Immediate actions for the next sprint]
- [Research questions to explore in upcoming interviews]
- [Changes to feedback collection process, if any]
```
