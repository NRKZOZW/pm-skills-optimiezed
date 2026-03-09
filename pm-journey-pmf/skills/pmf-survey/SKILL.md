---
name: pmf-survey
description: "Design, deploy, and analyze a PMF survey using the Sean Ellis Test and Superhuman PMF Engine. Covers survey questions, deployment timing, sample sizing, segmentation analysis, and a structured action framework for improving product-market fit."
---
# PMF Survey

## Overview
A well-designed PMF survey is the fastest way to measure whether your product has achieved product-market fit. This skill covers the full lifecycle: crafting the right questions, deploying at the right time to the right users, analyzing results by segment, and turning insights into prioritized actions.

## When to Use
- After users have experienced the product's core value (post-activation)
- As a quarterly or monthly PMF tracking mechanism
- When deciding whether to invest in growth vs product improvements
- Before major strategic decisions (pivot, scale, fundraise)
- When onboarding a new PM who needs to understand current PMF state

## Sean Ellis Survey Questions

### The Core Question
> "How would you feel if you could no longer use [product]?"
> - Very disappointed
> - Somewhat disappointed
> - Not disappointed
> - N/A (I no longer use [product])

### Essential Follow-Up Questions

**For all respondents**:
1. "What type of people do you think would benefit most from [product]?"
   - Reveals how users perceive your target audience — often more accurate than your own assumptions
2. "What is the main benefit you receive from [product]?"
   - Surfaces the core value proposition in the user's own words
3. "How can we improve [product] for you?"
   - Identifies gaps between current experience and ideal experience

**For "Very disappointed" respondents**:
4. "What would you use as an alternative if [product] were no longer available?"
   - Maps the competitive landscape from the user's perspective
5. "Have you recommended [product] to anyone? If so, how did you describe it?"
   - Reveals organic positioning and word-of-mouth messaging

**For "Somewhat disappointed" respondents**:
6. "What is the one thing that would make [product] a must-have for you?"
   - Identifies the gap between "nice to have" and "essential"

## The Superhuman PMF Engine

Rahul Vohra's systematic approach to improving PMF, adapted from Superhuman's journey to product-market fit.

### Step 1: Segment by "Very Disappointed" Users
- Identify the users who said "Very disappointed" — these are your superfans
- Analyze their common characteristics: role, company size, use case, acquisition channel
- Build a persona profile of your highest-fit users

### Step 2: Find What They Love
- Analyze the "main benefit" answers from "Very disappointed" users
- Identify the 2-3 themes that appear most frequently
- These themes ARE your product-market fit — the core value you must protect and amplify

### Step 3: Build for Superfans
- Prioritize features and improvements that deepen the experience for "Very disappointed" users
- Double down on what they love rather than fixing what others dislike
- Every roadmap item should pass the test: "Will this make our superfans even more delighted?"

### Step 4: Convert the "Somewhat Disappointed"
- Among "Somewhat disappointed" users, filter for those whose answer to "What type of people benefit most?" matches your target segment
- Analyze their "How can we improve?" responses for the single most common theme
- Address that theme while preserving everything the superfans love
- This expands your PMF without diluting it

### Step 5: Politely Ignore the Rest
- Users who said "Not disappointed" are not your market — do not build for them
- Users whose "type of people" answer does not match your target are not your market
- Resist the urge to be everything to everyone — focus wins

### Step 6: Track Progress
- Re-run the survey monthly or quarterly
- Plot the "Very disappointed" percentage over time
- Target: move from current % toward 40%+ through focused iteration

## Survey Deployment

### When to Send
- **After the Aha Moment**: Users must have experienced the core value at least once
- **Not too early**: New signups who haven't activated will skew results toward "Not disappointed"
- **Not too late**: Long-tenured users may have Stockholm syndrome — balance with newer cohorts
- **Ideal timing**: 2-4 weeks after activation, or after completing the core workflow 3+ times

### Sample Size Requirements
- **Minimum**: 40 responses for directional insights
- **Recommended**: 100+ responses for statistically meaningful segmentation
- **For segment analysis**: 30+ responses per segment you want to analyze independently
- **Response rate**: Expect 10-20% for in-app surveys, 5-10% for email

### Channel Selection (Ranked by Effectiveness)
1. **In-app survey**: Highest response rate, catches users in context
2. **In-app prompt linking to external survey**: Good balance of UX and flexibility
3. **Email survey**: Lower response rate but can reach inactive users
4. **Customer success conversations**: Qualitative depth, small sample size

### Frequency
- **Monthly**: For early-stage products actively iterating toward PMF
- **Quarterly**: For products with established PMF tracking trajectory
- **After major releases**: To measure impact of significant product changes

## Analysis Template

### Summary Metrics
```
Total responses: [N]
Very disappointed: [N] ([%])
Somewhat disappointed: [N] ([%])
Not disappointed: [N] ([%])
N/A: [N] ([%])
```

### Segmentation Analysis
Break down "% Very disappointed" by:
- User persona / role
- Company size
- Acquisition channel
- Usage frequency (power users vs casual)
- Subscription tier
- Geography

### Benefit Theme Analysis
From "What is the main benefit?" responses:
| Theme | Count | % of VD Users | % of SD Users |
|-------|-------|---------------|---------------|
| [Theme 1] | | | |
| [Theme 2] | | | |
| [Theme 3] | | | |

### Improvement Theme Analysis
From "How can we improve?" responses:
| Theme | Count | Mentioned by VD | Mentioned by SD |
|-------|-------|----------------|----------------|
| [Theme 1] | | | |
| [Theme 2] | | | |
| [Theme 3] | | | |

### Target Segment Alignment
From "What type of people benefit most?" responses:
| Described Segment | Count | Matches Target? |
|-------------------|-------|----------------|
| [Segment 1] | | Yes/No |
| [Segment 2] | | Yes/No |

## Action Framework

### If < 40% Very Disappointed
1. **Identify convertible "Somewhat Disappointed" users**: Filter SD respondents whose "type of people" answer matches your target segment
2. **Find the gap**: What do these SD users say would make the product a must-have?
3. **Protect the core**: Ensure improvements for SD users do not compromise what VD users love
4. **Prioritize**: Address the single most common improvement theme from convertible SD users
5. **Re-measure**: Run the survey again in 4-6 weeks after shipping improvements

### If >= 40% Very Disappointed
1. **Document your PMF**: Record the specific segment, use case, and value proposition that achieved PMF
2. **Deepen**: Use the **core-value-deepening** skill to strengthen what's working
3. **Expand carefully**: Look for adjacent segments where the same core value applies
4. **Prepare to scale**: PMF achieved — shift focus to growth and distribution

## Input Format
Use $ARGUMENTS to pass:
- Product name and description
- Target user segment
- Current Sean Ellis survey results (if available)
- Number of active users and activation criteria
- Any previous survey data for comparison

## Output
A complete PMF survey plan including:
- Customized survey questions for the specific product
- Deployment strategy (timing, channel, sample size targets)
- Analysis framework with segmentation plan
- Action priorities based on current or expected results
- Timeline for survey execution and follow-up

## Tips
- The exact wording of the core question matters — do not modify "How would you feel if you could no longer use [product]?"
- Open-ended follow-ups yield richer insights than multiple-choice alternatives
- Avoid leading questions or suggesting answers in the follow-ups
- Survey fatigue is real — keep total survey length under 5 minutes (5-7 questions max)
- Always close the loop: share what you learned and what you are changing with respondents

---

### Further Reading

- [How Superhuman Built an Engine to Find Product/Market Fit](https://review.firstround.com/how-superhuman-built-an-engine-to-find-product-market-fit)
- [Product-Market Fit: The Ultimate Guide with a New Framework](https://www.productcompass.pm/p/product-market-fit-guide-framework)
