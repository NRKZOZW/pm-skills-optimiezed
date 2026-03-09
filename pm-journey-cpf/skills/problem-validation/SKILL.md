---
name: problem-validation
description: "Score a problem hypothesis using the Problem Validation Canvas — five dimensions (Frequency, Intensity, Willingness to Pay, Current Alternatives, Switching Cost) scored 1-5. Produces a CPF score with evidence requirements and a GO/PIVOT/KILL recommendation."
---

## Problem Validation Canvas

A structured scoring framework to determine whether a problem is real, frequent, and painful enough to warrant building a solution. Use this after customer discovery interviews to make an evidence-based GO / PIVOT / KILL decision.

### Domain Context

Customer Problem Fit (CPF) means you have validated that a specific group of customers truly has a problem worth solving. This is **not** about whether they like your solution idea — it's about whether the problem is significant enough that they would actively seek, adopt, and pay for a solution. The Problem Validation Canvas quantifies this assessment across five dimensions.

### Context

You are scoring a problem hypothesis for **$ARGUMENTS**.

If the user provides interview summaries, research data, or a problem statement, read them first and extract evidence for each dimension.

### Instructions

1. **Confirm the problem hypothesis**

   Ensure you have a clear problem statement to score. If the user hasn't defined one, ask them to provide:
   - Who is the target customer?
   - What is the problem?
   - What evidence do you have? (interviews, data, observations)

2. **Score each dimension (1-5)**

   Present the Problem Validation Canvas and ask the user to provide evidence for each dimension. Score based on the evidence quality, not assumptions.

   ---

   ### Dimension 1: Frequency

   *How often does the problem occur?*

   | Score | Level | Description |
   |-------|-------|-------------|
   | 1 | Rare | Happens once a year or less; participants struggle to recall a recent instance |
   | 2 | Occasional | Happens a few times a year; participants can recall an instance with prompting |
   | 3 | Regular | Happens monthly; participants bring it up without prompting |
   | 4 | Frequent | Happens weekly; it's part of their regular workflow |
   | 5 | Constant | Happens daily or multiple times per day; it's an ever-present friction |

   **Evidence required**: Specific quotes or data showing how often participants encounter this problem. "Walk me through the last time..." responses are your primary input.

   ---

   ### Dimension 2: Intensity

   *How painful is the problem when it occurs?*

   | Score | Level | Description |
   |-------|-------|-------------|
   | 1 | Trivial | Minor annoyance; participants shrug it off |
   | 2 | Noticeable | Causes frustration but doesn't derail work; they move on quickly |
   | 3 | Significant | Causes meaningful delays, errors, or stress; they complain about it |
   | 4 | Severe | Causes major disruption; they've escalated it or asked for help |
   | 5 | Critical | Blocks their work entirely or causes serious financial/reputational harm |

   **Evidence required**: Emotional language from interviews ("it drives me crazy", "I dread this", "it costs us deals"), measurable impact (hours lost, revenue affected, error rates).

   ---

   ### Dimension 3: Willingness to Pay

   *Would they pay (time, money, or effort) to solve this?*

   | Score | Level | Description |
   |-------|-------|-------------|
   | 1 | None | "It's fine, I don't need a solution" — no purchase intent |
   | 2 | Low | "That would be nice" — polite interest but no action |
   | 3 | Moderate | "I've looked for solutions" — active search behavior |
   | 4 | High | "I've tried [competitor/workaround] and spent $X" — money already allocated |
   | 5 | Urgent | "I'd pay right now" — pre-order, LOI, or active budget approval |

   **Evidence required**: Past spending on alternatives, time invested in workarounds, explicit budget mentions, letters of intent, pre-orders, or "shut up and take my money" moments.

   ---

   ### Dimension 4: Current Alternatives

   *What do they do today, and how adequate is it?*

   | Score | Level | Description |
   |-------|-------|-------------|
   | 1 | Adequate | Current solution works well; they're satisfied and not looking for change |
   | 2 | Functional | Current solution is okay; some gaps but nothing urgent |
   | 3 | Makeshift | Using cobbled-together tools (spreadsheets, email, manual processes); functional but fragile |
   | 4 | Poor | Current workaround is painful, error-prone, or time-consuming; they actively dislike it |
   | 5 | None | No workaround exists; they simply endure the problem or avoid the task entirely |

   **Evidence required**: Descriptions of current tools and workflows, time spent on workarounds, complaints about existing solutions, number of tools stitched together.

   ---

   ### Dimension 5: Switching Cost

   *How easy would it be for them to adopt a new solution?*

   | Score | Level | Description |
   |-------|-------|-------------|
   | 1 | Prohibitive | Massive switching costs (data migration, retraining, contracts); nearly impossible |
   | 2 | High | Significant effort required; they'd need executive buy-in and a migration plan |
   | 3 | Moderate | Some effort required but manageable; they've switched tools before |
   | 4 | Low | Easy to try; could run in parallel with current approach |
   | 5 | Trivial | No switching cost; they could start using a new solution today |

   **Evidence required**: Interview responses about past tool changes, contract lock-in mentions, data portability concerns, IT approval requirements.

   ---

3. **Calculate the CPF Score**

   ```
   CPF Score = Frequency + Intensity + Willingness to Pay + Current Alternatives + Switching Cost
   ```

   | Total Score | Rating | Interpretation | Recommendation |
   |-------------|--------|----------------|----------------|
   | 20-25 | Strong CPF | The problem is real, frequent, painful, and solvable. Customers are actively looking for a solution. | **GO** — Proceed to Problem Solution Fit (PSF) |
   | 15-19 | Promising | The problem exists but some dimensions are weak. Worth refining the hypothesis or narrowing the segment. | **PIVOT** — Refine hypothesis, do more interviews, or narrow the target |
   | 10-14 | Weak | The problem is either not painful enough, not frequent enough, or the market is too hard to reach. | **RECONSIDER** — Major pivot needed or kill this direction |
   | 5-9 | No CPF | There is no meaningful problem to solve for this customer segment. | **KILL** — Move on to a different problem or segment |

4. **Generate the scorecard**

   ```
   ## Problem Validation Scorecard

   **Problem Hypothesis**: [statement]
   **Date**: [today]
   **Based on**: [N] customer interviews, [other evidence sources]

   ### Scores

   | Dimension | Score | Evidence Summary |
   |-----------|-------|-----------------|
   | Frequency | [1-5] | [key evidence] |
   | Intensity | [1-5] | [key evidence] |
   | Willingness to Pay | [1-5] | [key evidence] |
   | Current Alternatives | [1-5] | [key evidence] |
   | Switching Cost | [1-5] | [key evidence] |
   | **Total** | **[X/25]** | |

   ### Rating: [Strong CPF / Promising / Weak / No CPF]

   ### Strengths
   - [Dimensions scoring 4-5 and why]

   ### Weaknesses
   - [Dimensions scoring 1-2 and why]

   ### Evidence Gaps
   - [Dimensions where evidence is thin or based on assumptions]

   ### Recommendation
   [GO / PIVOT / KILL] — [detailed rationale]

   ### If PIVOT, suggested actions:
   - [Specific refinements to the hypothesis]
   - [Additional interviews needed and with whom]
   - [Questions to add to the next discovery round]

   ### If GO, next steps:
   - Proceed to Problem Solution Fit (PSF)
   - Define solution hypotheses to test
   - Run `/run-psf` to begin solution validation
   ```

5. **Discuss the results**

   - Highlight where the score is strong and where it's weak
   - If there are evidence gaps, recommend specific interview questions to fill them
   - If the score is borderline (14-16), discuss whether a refined segment might score higher
   - Remind the user that a KILL is a good outcome — it saves months of building the wrong thing

### Scoring Principles

- **Score based on evidence, not hope.** If you don't have interview data for a dimension, score it conservatively and flag the gap.
- **Multiple interviews > single interviews.** A theme across 5 interviews is more reliable than one enthusiastic participant.
- **Behavior > words.** "I would definitely pay" (score 2) is weaker than "I already pay $200/month for a half-solution" (score 4).
- **Be honest.** The purpose of CPF validation is to avoid wasting months on a problem nobody cares about. A false positive here is expensive.
