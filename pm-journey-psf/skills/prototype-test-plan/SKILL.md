---
name: prototype-test-plan
description: "Plan and execute a prototype test — from selecting the right fidelity level through writing a test script to synthesizing results. Covers paper prototypes, wireframes, mockups, and clickable prototypes with metrics guidance and sample size recommendations."
---

## Prototype Test Plan

A comprehensive framework for planning, running, and synthesizing prototype tests. Use this when you need to validate a solution concept with real users before investing in development.

### Domain Context

Prototype testing is the fastest way to learn whether a solution works for users. The key principle: **test at the lowest fidelity that answers your question.** Higher fidelity costs more time and money but yields more detailed feedback. Match fidelity to your learning goals.

### Fidelity Selection Guide

Choose the right prototype fidelity based on what you need to learn:

#### Paper Prototype

- **Cost**: Very low (hours)
- **Best for**: Early concept validation, information architecture, basic flow
- **What it tests**: Whether the core concept resonates, whether the mental model makes sense
- **Limitations**: Cannot test visual design, interactions, or performance
- **When to use**: You have multiple competing concepts and need to narrow down quickly; you are unsure if the basic approach is right

#### Low-Fidelity Wireframe (Clickable)

- **Cost**: Low (1-2 days)
- **Tools**: Balsamiq, Figma (low-fi), whimsical
- **Best for**: Testing user flows, navigation, task completion
- **What it tests**: Whether users can complete core tasks, where they get stuck, navigation mental model
- **Limitations**: Users may focus on visual polish rather than functionality
- **When to use**: You have a concept direction and need to validate the flow and information hierarchy

#### High-Fidelity Mockup

- **Cost**: Medium (3-5 days)
- **Tools**: Figma, Sketch, Adobe XD
- **Best for**: Testing visual design, content clarity, brand perception
- **What it tests**: Visual hierarchy, readability, emotional response, perceived quality
- **Limitations**: Not interactive; users cannot test real workflows
- **When to use**: The flow is validated but you need to test visual design decisions, or stakeholders need a realistic preview

#### Clickable Prototype (Interactive)

- **Cost**: Higher (1-2 weeks)
- **Tools**: Figma (prototype mode), ProtoPie, Framer, InVision
- **Best for**: Testing full interaction patterns, complex workflows, realistic user experience
- **What it tests**: End-to-end task completion, micro-interactions, error handling, perceived performance
- **Limitations**: Development effort approaches a basic MVP; risk of over-investing before validation
- **When to use**: Core flow is validated at lower fidelity; you need to test specific interaction details or convince stakeholders

### Fidelity Decision Matrix

| Question to Answer | Recommended Fidelity |
|--------------------|---------------------|
| Does the concept resonate? | Paper prototype |
| Can users complete the core task? | Low-fi wireframe |
| Does the visual design communicate value? | High-fi mockup |
| Does the full experience work end-to-end? | Clickable prototype |
| Is this better than the current solution? | Clickable prototype |

### Test Script Template

Use this structure for each test session:

#### 1. Introduction (2-3 minutes)

- Thank the participant
- Explain the purpose: "We are testing the design, not you. There are no wrong answers."
- Get consent for recording (if applicable)
- Remind them to think aloud: "Please tell me what you are thinking as you go through this."
- Clarify: "This is a prototype, not a finished product. Some things may not work."

#### 2. Warm-Up (3-5 minutes)

- Ask about their current behavior related to the problem space
- "Tell me about the last time you [relevant activity]."
- "How do you currently handle [the problem]?"
- "What frustrates you most about [current process]?"

#### 3. First Impression (1-2 minutes)

- Show the prototype without instructions
- "What is your first impression? What do you think this is for?"
- "What would you do first?"

#### 4. Core Tasks (15-20 minutes)

Design 3-5 tasks that test the key interactions. For each task:

```
Task [N]: [Task Name]
Scenario: "[Realistic context for why they would do this task]"
Instruction: "[What to ask them to do — keep it goal-oriented, not step-by-step]"
Success criteria: [What counts as successful completion]
Observe: [What to watch for — confusion points, workarounds, errors]
Follow-up: "[Question to ask after they attempt the task]"
```

**Task design principles:**
- Frame tasks as realistic goals, not UI instructions ("Find a flight to Tokyo" not "Click the search button")
- Order tasks from simple to complex
- Include at least one task that tests error recovery
- Include at least one task that tests the primary value proposition

#### 5. Debrief (5-10 minutes)

- "What was the easiest part of using this?"
- "What was the most confusing or frustrating part?"
- "How does this compare to how you currently solve this problem?"
- "Would you use this? Why or why not?"
- "What is missing that you would expect to see?"
- "On a scale of 1-10, how likely would you be to recommend this to a colleague?"
- "Is there anything else you want to share?"

### Metrics to Collect

#### Quantitative Metrics

| Metric | How to Measure | Benchmark |
|--------|---------------|-----------|
| Task completion rate | % of participants who complete each task successfully | >80% for core tasks |
| Time-on-task | Seconds from task start to completion | Compare to current solution |
| Error rate | Number of wrong paths or mistakes per task | <2 errors per task |
| Satisfaction (SUS) | System Usability Scale (10-item questionnaire, 0-100) | >68 = above average |
| Satisfaction (CSAT) | "How satisfied are you?" (1-5 scale) | >4.0 for core experience |
| Net Promoter Intent | "How likely to recommend?" (0-10) | >7 average |

#### Qualitative Metrics

- **Confusion points**: Where users pause, ask questions, or express uncertainty
- **Workarounds**: Where users find alternative paths (indicates unclear primary path)
- **Spontaneous reactions**: Unprompted positive or negative comments
- **Mental model mismatches**: Where user expectations differ from the design
- **Feature requests**: What users say is missing

### Sample Size Guidance

Based on Jakob Nielsen's research on usability testing:

| Participants | Usability Issues Found | Recommended For |
|--------------|----------------------|-----------------|
| 5 | ~85% of issues | Standard usability test; best ROI |
| 8 | ~90% of issues | When you need higher confidence |
| 10-12 | ~95% of issues | When usability is critical (medical, financial) |
| 15+ | Diminishing returns | Only for quantitative benchmarking |

**Recommendation**: Run 5 sessions, synthesize, iterate, then run 5 more. Two rounds of 5 beats one round of 10.

### Recruitment Criteria

Define your participants carefully:

- **Must match**: Target persona characteristics (demographics, behavior, experience level)
- **Screener questions**: 3-5 questions to qualify participants
- **Exclude**: People who have seen the product before (unless testing iteration), UX professionals (unless they are your target), friends and family
- **Incentive**: Appropriate compensation for their time (gift cards, product credit, cash)

### Synthesis Template

After running all test sessions, compile findings:

#### Findings Matrix

| Finding | Task | Participants Affected | Severity | Evidence |
|---------|------|----------------------|----------|----------|
| [What you observed] | [Which task] | [e.g., 4/5] | [Critical/High/Medium/Low] | [Quotes, behaviors] |

#### Severity Scoring

| Severity | Definition | Action |
|----------|-----------|--------|
| Critical | Prevents task completion; users cannot achieve their goal | Must fix before any launch |
| High | Causes significant confusion or delay; users find workarounds | Fix before next test round |
| Medium | Causes minor frustration; users recover quickly | Fix in next iteration |
| Low | Cosmetic or minor; users barely notice | Fix when convenient |

#### Prioritized Recommendations

For each finding, provide:
1. **What to change** — Specific design recommendation
2. **Why** — Evidence from the test (participant count, quotes)
3. **Priority** — Based on severity and frequency
4. **Effort** — Estimated effort to fix (small/medium/large)

### Instructions

You are helping a product team plan a prototype test for **$ARGUMENTS**.

### Input Requirements

- A description of the solution to test (concept, wireframe, prototype, or mockup)
- The target user or persona
- Key questions or hypotheses to validate
- Optionally: available tools, timeline constraints, budget

### Process

1. **Determine fidelity** — Based on what needs to be learned, recommend the appropriate prototype fidelity level.

2. **Define test objectives** — Clarify the top 3-5 questions this test should answer.

3. **Write the test script** — Create a complete test script using the template above, including introduction, warm-up, 3-5 core tasks, and debrief questions.

4. **Specify metrics** — Select the most relevant quantitative and qualitative metrics for this test.

5. **Set sample size and recruitment** — Recommend participant count and define screener criteria.

6. **Plan logistics** — Timeline, tools needed, recording setup, note-taking template.

7. **Prepare synthesis framework** — Provide the findings matrix template customized for this test.

Think step by step. Save as markdown if substantial.

---

### Further Reading

- [Don't Make Me Think](https://sensible.com/dont-make-me-think/) by Steve Krug
- [Rocket Surgery Made Easy](https://sensible.com/rocket-surgery-made-easy/) by Steve Krug
- [Sprint: How to Solve Big Problems and Test New Ideas in Just Five Days](https://www.thesprintbook.com/) by Jake Knapp
- [Usability Testing 101](https://www.nngroup.com/articles/usability-testing-101/) by Nielsen Norman Group
