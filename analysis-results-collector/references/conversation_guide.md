# Conversation Patterns for Results Collection

This reference provides guidance on how to conduct effective conversations to gather analysis results.

## Core Principles

### 1. Progressive Disclosure
Don't overwhelm users with all questions at once. Gather information in logical phases:
- Phase 1: Understand which hypotheses were analyzed
- Phase 2: Determine which were validated/invalidated
- Phase 3: Collect detailed findings for each analyzed hypothesis
- Phase 4: Gather recommendations and next steps

### 2. Adaptive Questioning
Tailor follow-up questions based on:
- Whether hypothesis was validated or invalidated
- Complexity of the analysis performed
- Amount of detail already provided

### 3. Extract, Don't Transcribe
Transform raw analytical findings into communication-ready content:
- Remove jargon and technical details unless necessary
- Focus on "so what" - business implications
- Quantify impact wherever possible
- Translate data into decisions

## Phase 1: Hypothesis Triage

**Objective:** Quickly understand the scope of analysis completed

**Approach:**
- Present list of all hypotheses from the plan
- Ask user to identify which were analyzed vs not analyzed
- For "not analyzed" items, capture brief reason why

**Example questions:**
- "Looking at your analysis plan, I can see 8 hypotheses (H1-H8). Which of these did you actually analyze?"
- "For the hypotheses you didn't analyze (like H5, H6, H7), what was the reason? Was it that earlier hypotheses explained the issue, or something else?"

**What to capture:**
- Analyzed: [List of hypothesis IDs]
- Not analyzed: [List with brief reasons]

## Phase 2: Validation Status

**Objective:** Determine which analyzed hypotheses were proven true vs false

**Approach:**
- For each analyzed hypothesis, ask for validation status
- Use simple language: "Did this turn out to be true or false?"
- Accept nuanced answers ("partially validated")

**Example questions:**
- "For H1 (Account Setup Completion Rate Dropped), did your analysis validate this hypothesis or invalidate it?"
- "Was this hypothesis proven, disproven, or somewhere in between?"

**What to capture:**
- Status: Validated | Invalidated | Partially Validated
- Confidence level: High | Medium | Low
- Impact contribution: X% of total decline

## Phase 3: Detailed Findings Collection

**Objective:** Gather crisp, communication-ready summaries of what was found

**Critical distinction:** We're not asking users to paste raw data or reproduce their analysis. We're asking them to summarize findings in a way that can be communicated to stakeholders.

### For VALIDATED Hypotheses

**What we need:**
1. **Core finding** (2-3 sentences): What actually happened?
2. **Supporting evidence** (3-5 key data points): What proves this?
3. **Impact quantification**: How much did this contribute?
4. **Business implication**: Why does this matter?

**Example questions:**
- "You validated that account setup completion dropped. Can you summarize what you found in 2-3 sentences that I could share with leadership?"
- "What are the 3-4 most important data points that support this finding?"
- "Can you quantify the impact? For example, did setup completion drop from X% to Y%, and how much of the overall 15% decline does this explain?"
- "Why does this matter to the business? What's the implication?"

**Adaptive follow-ups based on detail level:**
- If user provides raw numbers only → Ask for interpretation
- If user provides technical jargon → Ask for plain language version
- If user provides long explanation → Ask for executive summary version
- If user provides conclusion without evidence → Ask for key supporting data points

### For INVALIDATED Hypotheses

**What we need:**
1. **What was ruled out** (1-2 sentences): What did we learn wasn't the cause?
2. **Key evidence** (1-2 data points): What disproved this?
3. **Value of ruling this out**: Why was this useful to test?

**Example questions:**
- "You invalidated the user mix hypothesis. In plain language, what did you learn?"
- "What specific evidence showed this wasn't the cause?"
- "Was this hypothesis worth testing, or should it have been skipped?"

### For PARTIALLY VALIDATED Hypotheses

**What we need:**
1. **What was true vs false**: Which parts validated?
2. **Partial impact**: How much did the validated portion contribute?
3. **Remaining questions**: What's still unclear?

**Example questions:**
- "You said this was partially validated. Which aspects were true and which weren't?"
- "For the parts that were validated, what's the impact?"
- "What questions remain unanswered?"

## Phase 4: Recommendations

**Objective:** Capture actionable next steps with clear prioritization

**What we need:**
1. **Recommendation title**: Clear, action-oriented name
2. **Root cause addressed**: Which finding does this fix?
3. **Expected impact**: Projected improvement
4. **Effort required**: Resource/time estimate
5. **Specific actions**: 3-5 concrete steps
6. **Success metrics**: How to measure if it worked

**Example questions:**
- "Based on these findings, what are your top 3-5 recommendations?"
- "For each recommendation, what's the expected impact on the North Star Metric?"
- "What are the specific action items for [Recommendation 1]?"
- "How will you measure success for this recommendation?"

**Prioritization questions:**
- "If you could only implement one recommendation, which would it be and why?"
- "Which recommendations are quick wins vs longer-term investments?"

## Handling Common Scenarios

### Scenario: User Provides Too Much Detail
**Response:** "That's helpful technical detail. For the final document, can you distill this into 2-3 key points that would resonate with leadership?"

### Scenario: User Provides Too Little Detail
**Response:** "Can you elaborate a bit more? For example, what specific data points support this finding?"

### Scenario: User Is Uncertain About Impact
**Response:** "Even a rough estimate is helpful. Would you say this contributed roughly X% to the decline, or is it more/less than that?"

### Scenario: User Jumps Around Topics
**Response:** "Great information! Let me make sure I capture this properly. Let's finish discussing [current hypothesis] first, then we can move to [other topic]."

### Scenario: User Wants to Paste Entire Analysis
**Response:** "I appreciate you have detailed analysis. Rather than paste everything, let's work through the key findings together so I can capture them in a format that's ready for communication. What was the single most important thing you learned from this hypothesis?"

## Output Quality Standards

Before moving to next hypothesis, ensure you have captured:
- ✅ Clear, jargon-free summary of finding
- ✅ 3-5 specific data points or evidence
- ✅ Quantified impact where possible
- ✅ Business implication stated
- ✅ Information is communication-ready (not raw data dump)

## Progressive Writing Approach

After gathering information for 2-3 hypotheses:
- Pause to write up those sections
- Show user draft sections for feedback
- Refine based on their input
- Then continue with remaining hypotheses

This allows:
- Early validation of format and style
- Course correction if needed
- Avoids losing information in long conversations
- Keeps user engaged with tangible progress
