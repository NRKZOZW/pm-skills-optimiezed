---
name: empathy-map
description: "Create empathy maps to deepen customer understanding. Six quadrants (See, Hear, Think, Feel, Say, Do) centered on Goals and Pains. Filled from interview data to build shared team understanding of the customer's world."
---

## Empathy Map

Build a rich, evidence-based picture of your target customer using the empathy map framework. This tool transforms interview data into a shared understanding of how customers experience their world — what they see, hear, think, feel, say, and do.

### Domain Context

An empathy map is a collaborative visualization that articulates what a team knows about a particular type of user. It externalizes knowledge about users in order to create a shared understanding, aid in decision making, and surface gaps in research. Empathy maps work best when filled with **real data from interviews and observations**, not assumptions.

### Context

You are creating an empathy map for **$ARGUMENTS**.

If the user provides interview transcripts, summaries, personas, or research data, read them first and extract evidence for each quadrant.

### Instructions

1. **Identify the subject**

   Ask the user:
   - Who is this empathy map for? (specific persona, segment, or interview participant)
   - What context or scenario should we focus on? (e.g., "when they're trying to prioritize features")
   - What data sources are available? (interview transcripts, observation notes, survey responses)

2. **Fill the six quadrants**

   For each quadrant, extract evidence from interviews and observations. Use direct quotes and specific behaviors wherever possible.

   ---

   ### SEE — What does the customer see in their environment?

   *Their physical and digital environment when the problem occurs.*

   - What tools and interfaces are on their screen?
   - What does their workspace look like?
   - What do they see competitors or peers doing?
   - What market trends or offers are they exposed to?
   - What information are they bombarded with?

   **Prompt for interviews**: "Describe what your screen/desk looks like when you're dealing with [problem area]."

   ---

   ### HEAR — What does the customer hear from others?

   *Influences from colleagues, managers, media, and social circles.*

   - What do their managers or executives say about this problem area?
   - What do colleagues or peers recommend?
   - What are industry analysts or thought leaders saying?
   - What do their customers or end-users tell them?
   - What media or social channels influence their thinking?

   **Prompt for interviews**: "What do your colleagues/boss say about how you handle [problem area]?"

   ---

   ### THINK — What occupies the customer's thoughts?

   *Internal monologue, worries, aspirations — things they may not say out loud.*

   - What keeps them up at night about this problem?
   - What do they really care about (even if they don't say it)?
   - What are their aspirations related to this area?
   - What fears or anxieties do they have?
   - What mental models or beliefs shape their thinking?

   **Prompt for interviews**: Inferred from emotional language, hesitations, and recurring themes across the conversation.

   ---

   ### FEEL — What emotions does the customer experience?

   *Emotional landscape when dealing with the problem.*

   - Frustrated? By what specifically?
   - Anxious? About what outcomes?
   - Overwhelmed? By what volume or complexity?
   - Confident? About which parts?
   - Excited? About what possibilities?

   **Prompt for interviews**: Watch for emotional language: "it drives me crazy", "I dread this", "I love when", "it's embarrassing".

   ---

   ### SAY — What does the customer actually say?

   *Verbatim quotes and stated positions — what they express to others.*

   - What do they say about the problem in meetings?
   - How do they describe the problem to peers?
   - What do they say when asked about their current solution?
   - What language and terminology do they use?
   - What do they say vs. what they actually do? (Note contradictions.)

   **Prompt for interviews**: Capture direct quotes. Pay attention to the specific words they choose — these become your product's language.

   ---

   ### DO — What actions and behaviors are observable?

   *Actual behavior, not stated intentions.*

   - What steps do they take when the problem occurs?
   - What workarounds have they built?
   - How do they interact with current tools?
   - What do they spend time on that they shouldn't have to?
   - What behaviors contradict what they say?

   **Prompt for interviews**: "Walk me through exactly what you did the last time this happened."

   ---

3. **Define the center: Goals and Pains**

   **Goals** (what they're trying to achieve):
   - Primary goal: [the main job to be done]
   - Secondary goals: [related outcomes they care about]
   - Success metrics: [how they measure whether they're succeeding]

   **Pains** (obstacles and frustrations):
   - Primary pain: [the biggest barrier to achieving their goal]
   - Secondary pains: [other frustrations]
   - Fear: [what they're afraid will happen if the problem persists]

4. **Identify patterns and insights**

   After filling all quadrants, analyze:

   - **Say-Do gaps**: Where does stated behavior differ from actual behavior? These gaps are gold — they reveal unmet needs the customer may not articulate.
   - **Think-Feel tension**: Where are internal conflicts? (e.g., they think they should use data but feel overwhelmed by analytics tools)
   - **Recurring themes**: What shows up across multiple quadrants? These are the strongest signals.
   - **Surprise findings**: What contradicts your prior assumptions?

5. **Output the empathy map**

   ```
   ## Empathy Map: [Persona / Segment Name]

   **Context**: [Scenario or situation being mapped]
   **Based on**: [N] interviews, [other sources]
   **Date**: [today]

   ┌─────────────────────┬─────────────────────┐
   │        SEE          │        HEAR          │
   │                     │                      │
   │ • [observation]     │ • [influence]        │
   │ • [observation]     │ • [influence]        │
   │ • [observation]     │ • [influence]        │
   │                     │                      │
   ├─────────────────────┼──────────────────────┤
   │       THINK         │        FEEL          │
   │                     │                      │
   │ • [thought]         │ • [emotion]          │
   │ • [thought]         │ • [emotion]          │
   │ • [thought]         │ • [emotion]          │
   │                     │                      │
   ├─────────────────────┼──────────────────────┤
   │        SAY          │         DO           │
   │                     │                      │
   │ • "[quote]"         │ • [behavior]         │
   │ • "[quote]"         │ • [behavior]         │
   │ • "[quote]"         │ • [behavior]         │
   │                     │                      │
   └─────────────────────┴──────────────────────┘

               ┌─────────────────────┐
               │    GOALS & PAINS    │
               │                     │
               │ Goals:              │
               │ • [goal]            │
               │ • [goal]            │
               │                     │
               │ Pains:              │
               │ • [pain]            │
               │ • [pain]            │
               └─────────────────────┘

   ### Key Insights
   1. **[Insight]** — [evidence from quadrants]
   2. **[Insight]** — [evidence from quadrants]
   3. **[Insight]** — [evidence from quadrants]

   ### Say-Do Gaps
   - [Gap and what it might mean]

   ### Implications for Problem Validation
   - [How this empathy map informs your problem hypothesis]
   - [What to probe further in follow-up interviews]
   ```

6. **Connect to next steps**

   - If the empathy map reveals a different pain than hypothesized, suggest refining the problem statement
   - If multiple empathy maps exist (different segments), suggest comparing them to find the strongest CPF
   - Recommend using the empathy map as a reference during solution design

### Tips for High-Quality Empathy Maps

- **Use real data.** An empathy map filled from assumptions is just a fancy guess. Fill it from interview transcripts.
- **One persona per map.** Don't mix segments — create separate maps for each.
- **Update as you learn.** The empathy map is a living artifact. Add to it after every interview.
- **Use the customer's language.** Direct quotes are more powerful than paraphrased summaries.
- **Look for contradictions.** The most valuable insights often come from gaps between quadrants.
