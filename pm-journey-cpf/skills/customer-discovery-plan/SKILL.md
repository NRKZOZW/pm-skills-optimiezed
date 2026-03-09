---
name: customer-discovery-plan
description: "Plan a customer discovery sprint: who to talk to, how to recruit, what to ask (following The Mom Test principles), how to synthesize findings, and when you have enough signal. Includes a 1-2 week sprint template."
---

## Customer Discovery Plan

Design a structured customer discovery sprint that moves you from hypothesis to evidence in 1-2 weeks. This skill covers participant recruitment, question design, synthesis, and signal detection.

### Domain Context

Customer discovery is the primary method for validating a problem hypothesis during the Customer Problem Fit phase. The goal is not to confirm your idea — it's to **learn whether the problem is real, frequent, and painful enough to warrant a solution**. You are looking for patterns across conversations, not individual opinions.

### Context

You are helping the user plan a customer discovery sprint for **$ARGUMENTS**.

If the user provides a problem hypothesis, personas, or prior research, read them first.

### Instructions

1. **Define discovery objectives**

   Ask the user:
   - What is the problem hypothesis you're testing?
   - What would make you confident the problem is real? What would make you walk away?
   - What do you already know (prior interviews, data, feedback)?
   - How much time can you dedicate to this sprint?

2. **Identify target participants**

   - **Minimum**: 5 interviews (enough to spot obvious patterns)
   - **Target**: 12-15 interviews (enough for pattern saturation)
   - **Maximum**: 20 interviews (diminishing returns beyond this)

   Define participant criteria:
   ```
   ## Participant Criteria

   **Must have** (screening requirements):
   - [Criterion 1 — e.g., "Has experienced the problem in the last 30 days"]
   - [Criterion 2 — e.g., "Currently uses a workaround"]
   - [Criterion 3 — e.g., "In the target role/segment"]

   **Nice to have** (diversity factors):
   - Mix of company sizes (startup, mid-market, enterprise)
   - Mix of experience levels (junior, senior, executive)
   - Mix of current solutions (manual, competitor tool, nothing)

   **Exclude**:
   - [People who would be biased — e.g., close friends, investors]
   - [People outside the target segment]
   ```

3. **Recruitment channels**

   Suggest 3-5 channels ranked by quality and speed:

   | Channel | Quality | Speed | Cost | Notes |
   |---------|---------|-------|------|-------|
   | Existing customer base | High | Fast | Free | Best if you have an existing product |
   | LinkedIn outreach | Medium-High | Medium | Free-Low | Personal messages, not InMail spam |
   | Community forums / Slack groups | Medium | Medium | Free | Find where your target hangs out |
   | User research platforms (UserTesting, Respondent) | Medium | Fast | $50-150/session | Good for hard-to-reach segments |
   | Warm introductions | High | Slow | Free | Ask advisors, investors, colleagues |
   | Conference / meetup networking | High | Slow | Free | Face-to-face builds trust |

   Provide a **recruitment message template**:
   ```
   Hi [Name],

   I'm researching how [target role] handles [problem area]. I'm not selling
   anything — just learning from people who deal with this regularly.

   Would you be open to a 20-minute conversation this week or next? I'd love
   to hear about your experience.

   Happy to share what I learn from the research as a thank-you.

   Best,
   [Your name]
   ```

4. **Design the question framework**

   Follow **The Mom Test** principles (Rob Fitzpatrick):

   **Rules**:
   - Ask about **their life**, not your idea
   - Ask about **the past**, not hypothetical futures
   - **Talk less, listen more** (aim for 20/80 split)
   - **Never pitch** — you are here to learn
   - **Compliments are noise** — "That sounds cool!" tells you nothing
   - Look for **strong emotions** — they signal real pain or delight
   - Get **commitments and advancement**, not just compliments

   **Core questions** (adapt to the specific problem area):

   | Category | Question | Why You're Asking |
   |----------|----------|-------------------|
   | Context | "Walk me through the last time you dealt with [problem area]." | Grounds the conversation in real behavior |
   | Frequency | "How often does this come up? Daily, weekly, monthly?" | Tests whether the problem is frequent enough to matter |
   | Impact | "What happens when this goes wrong? What does it cost you?" | Quantifies the negative outcome |
   | Current solution | "What do you do about it today?" | Reveals existing workarounds and their limits |
   | Effort | "How much time/money do you spend dealing with this?" | Tests willingness to invest in a solution |
   | Alternatives | "Have you looked for a better way? What did you try?" | Shows urgency and purchase intent |
   | Priority | "Where does this rank among your top 3 headaches right now?" | Tests relative importance |

   **Red flags** (signs you're getting bad data):
   - Participant says "I would definitely use that!" (hypothetical — ignore)
   - Participant can't recall a specific instance (problem may not be real)
   - Participant's description doesn't match the hypothesis at all (pivot signal)
   - You're talking more than the participant (you're pitching, not learning)

5. **Synthesis framework**

   After each interview, capture:
   ```
   ## Interview #[N] — [Participant ID]
   Date: [date]
   Duration: [minutes]

   **Problem confirmed?** Yes / Partially / No
   **Frequency**: [daily/weekly/monthly/rarely]
   **Intensity** (1-5): [score]
   **Current workaround**: [description]
   **Willingness to pay**: [yes/no/maybe — evidence]
   **Key quote**: "[verbatim quote]"
   **Surprise finding**: [anything unexpected]
   ```

   After every 5 interviews, run a **pattern check**:
   - What themes are repeating?
   - What's surprising or contradictory?
   - Do we need to adjust our questions?
   - Are we talking to the right people?

6. **Signal detection — when do you have enough?**

   | Signal | Meaning |
   |--------|---------|
   | 4+ out of 5 participants describe the same core pain | Strong pattern — problem is likely real |
   | Participants use similar language unprompted | Very strong signal — natural vocabulary for the problem |
   | Participants have spent money/time trying to solve it | High willingness to pay |
   | Participants can't recall a recent instance | Weak signal — problem may not be frequent |
   | Every interview surfaces a different problem | No pattern — hypothesis may be wrong |
   | Participants say "that would be nice" but haven't tried to solve it | Low intensity — not painful enough |

   **Saturation rule**: If you've done 8-10 interviews and the last 3 produced no new insights, you've reached saturation. Stop interviewing and synthesize.

7. **Output the Discovery Sprint Plan**

   ```
   ## Discovery Sprint Plan: [Topic]

   **Problem Hypothesis**: [statement]
   **Sprint Duration**: [1-2 weeks]
   **Target Interviews**: [number]
   **Decision Criteria**: [what constitutes GO / PIVOT / KILL]

   ### Week 1: Recruit & Interview
   - Day 1-2: Send recruitment messages (target 20 outreach for 12 interviews)
   - Day 2-3: Schedule first interviews
   - Day 3-5: Conduct interviews 1-5
   - Day 5: Pattern check #1 — adjust questions if needed

   ### Week 2: Interview & Synthesize
   - Day 6-8: Conduct interviews 6-12
   - Day 8: Pattern check #2 — assess saturation
   - Day 9: Cross-interview synthesis
   - Day 10: Write up findings and score the problem

   ### Participant Tracker
   | # | Name/ID | Channel | Status | Scheduled | Completed | Key Finding |
   |---|---------|---------|--------|-----------|-----------|-------------|

   ### Question Guide
   [Customized questions from step 4]

   ### Per-Interview Template
   [Template from step 5]

   ### Synthesis Template
   [Cross-interview pattern analysis]

   ### Decision Gate
   - **GO**: [criteria]
   - **PIVOT**: [criteria]
   - **KILL**: [criteria]
   ```

---

### Further Reading

- [The Mom Test](https://www.momtestbook.com/) by Rob Fitzpatrick
- [Continuous Product Discovery Masterclass (CPDM)](https://www.productcompass.pm/p/cpdm) (video course)
- [User Interviews: The Ultimate Guide](https://www.productcompass.pm/p/interviewing-customers-the-ultimate)
