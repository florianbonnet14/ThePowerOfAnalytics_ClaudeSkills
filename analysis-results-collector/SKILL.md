---
name: analysis-results-collector
description: Transform completed analysis work into structured, communication-ready documentation by conducting guided conversations that extract key findings, evidence, and recommendations. Use when a user has completed an analysis (typically following an analysis plan created by the analysis-planner skill) and needs to document results, create findings summaries, build executive reports, or prepare analysis outcomes for stakeholder communication. This skill systematically gathers what was tested, what was found, and what should be done next, then generates a professional markdown document ready for distribution.
---

# Analysis Results Collector

This skill helps you transform completed analytical work into clear, actionable documentation by conducting structured conversations that extract findings and build comprehensive results documents.

## When to Use This Skill

Use this skill when:
- User has completed an analysis and needs to document results
- User mentions finishing hypothesis testing or investigation work  
- User has an analysis plan (from analysis-planner or similar) and completed analyses
- User needs to create executive summaries or findings reports
- User asks to "document findings," "write up results," or "create analysis report"

## Overview of Process

The skill guides users through a 4-phase conversation:

1. **Hypothesis Triage** - Identify which hypotheses were analyzed vs not analyzed
2. **Validation Status** - Determine which were validated, invalidated, or partially validated
3. **Detailed Findings** - Gather communication-ready summaries for each hypothesis
4. **Recommendations** - Capture prioritized, actionable next steps

After gathering information, generate a structured markdown document using the template.

## Step 1: Parse the Analysis Plan

**Action:** Read the uploaded analysis plan to understand the structure and hypotheses.

**Extract from the plan:**
- Problem statement and North Star Metric
- List of all hypotheses (with their IDs like H1, H2, etc.)
- Hypothesis tier structure (Tier 1, 2, 3)
- Original timeline and scope
- Success criteria

**Present to user:**
- Confirm you've reviewed their plan
- Show the list of hypotheses you identified
- Ask if this matches their understanding

**Example:**
> "I've reviewed your analysis plan for the 15% decline in 7-Day Publish Rate. I see 8 hypotheses organized into 3 tiers:
> 
> Tier 1 (High Priority):
> - H1: Account Setup Completion Rate Dropped
> - H2: First Prompt Submission Rate Declined
> - H3: User Mix Shifted to Lower-Quality Signups
> 
> Tier 2 (Medium Priority):
> - H4: Project Start Rate Decreased
> - H5: Preview-to-Publish Conversion Dropped
> - H6: Time-to-First-Prompt Increased Beyond 7 Days
> 
> Tier 3 (Lower Priority):
> - H7: Help Feature Usage Changed with Different Outcomes
> - H8: External/Seasonal Factor
> 
> Does this match your plan?"

## Step 2: Hypothesis Triage Phase

**Objective:** Quickly map out which hypotheses were analyzed.

**Approach:**
- Ask user to identify analyzed vs not-analyzed hypotheses
- For not-analyzed items, get brief reason (optional but helpful)
- Keep this phase quick - just a checklist\
- Use the askquestion tool to facilitate input from the user

**Example questions:**
- "Which of these hypotheses did you actually analyze? You can just list the IDs like 'H1, H2, H3' or tell me which ones you skipped."
- "For the ones you didn't analyze, was it because earlier findings explained everything, or another reason?"

**What to capture:**
```
Analyzed: [List of hypothesis IDs]
Not analyzed: [List of IDs with optional brief reason]
```

**Don't:** Ask for detailed findings yet. Just get the map of what was done.

## Step 3: Validation Status Phase

**Objective:** Understand which analyzed hypotheses were proven vs disproven.

**For each analyzed hypothesis:**
- Ask for validation result: Validated | Invalidated | Partially Validated
- Request confidence level: High | Medium | Low
- Get rough impact estimate if validated (e.g., "contributes X% to the decline")
- Must use the askquestion tool to facilitate input from the user on these 2 items (validation, confidence) and free text for the impact

**Example questions:**
- "For H1 (Account Setup Completion Rate Dropped), did your analysis validate or invalidate this hypothesis?"
- "How confident are you in this finding - high, medium, or low?"
- "If validated: Can you estimate how much this contributed to the overall problem? For example, if the overall decline was 15%, did this hypothesis explain 5%, 10%, or some other amount?"

**Create a summary table:**
```
| Hypothesis | Status | Result | Confidence | Impact |
|-----------|--------|--------|------------|--------|
| H1 | Analyzed | Validated | High | 8% of 15% |
| H2 | Analyzed | Invalidated | High | 0% |
```

**Present this table to the user for confirmation before proceeding.**

## Step 4: Detailed Findings Collection

**Read the conversation guide for comprehensive patterns:** [references/conversation_guide.md](references/conversation_guide.md)

**Read the writing guide for quality standards:** [references/writing_guide.md](references/writing_guide.md)

**Core approach:**
- Work through hypotheses ONE AT A TIME
- Gather information using SEBI framework: Statement, Evidence, Business Impact, Insight
- Focus on communication-ready content, not raw data dumps
- Adapt questions based on whether hypothesis was validated or invalidated

### For VALIDATED Hypotheses

**Information to gather:**
1. **Core finding** (2-3 sentences): What actually happened?
2. **Supporting evidence** (3-5 data points): What proves it?
3. **Impact quantification**: How much did this contribute?
4. **Business implication**: Why does this matter?

**Example conversation flow:**

> **Claude:** "Let's dive into H1 - Account Setup Completion Rate Dropped. You validated this hypothesis. Can you summarize what you found in 2-3 sentences that could be shared with leadership?"

> **User:** [Provides summary]

> **Claude:** "Great. What are the 3-4 most important data points that support this finding?"

> **User:** [Provides data points]

> **Claude:** "Can you quantify the impact more precisely? For example, did setup completion drop from X% to Y%? And how much of the overall 15% decline in the North Star Metric does this explain?"

> **User:** [Provides quantification]

> **Claude:** "Why does this matter to the business? What's the specific implication - like users lost per month, revenue impact, etc.?"

> **User:** [Provides business impact]

**Adaptive follow-ups:**
- If answer too technical → "Can you explain that in simpler terms for a non-technical stakeholder?"
- If answer too vague → "Can you be more specific? What exact metric or number shows this?"
- If answer too long → "That's great detail. For the executive summary, what are the top 2-3 key points?"

### For INVALIDATED Hypotheses

**Information to gather:**
1. **What was ruled out** (1-2 sentences)
2. **Key evidence** (1-2 data points that disproved it)
3. **Value of testing** (Why was this useful to check?)

**Keep this brief** - invalidated hypotheses need less space in the final document.

### For PARTIALLY VALIDATED Hypotheses

**Information to gather:**
1. **What parts were true vs false**
2. **Impact of validated portions**
3. **Remaining questions** (optional)

**These often require more nuanced discussion** - be patient and help user articulate the complexity.

### Progressive Writing Approach

**After gathering 2-3 hypotheses:**
- Pause the information gathering
- Draft those sections using the template structure
- Show the user your draft
- Get feedback and refine
- Then continue with remaining hypotheses

**Benefits:**
- Validates format and style early
- Catches misunderstandings quickly
- Keeps user engaged
- Prevents information loss in long conversations

**Example:**

> **Claude:** "I've gathered findings for H1, H2, and H3. Let me draft those sections now so you can review before we continue with the remaining hypotheses. One moment..."
> 
> [Generate draft sections]
> 
> "Here's my draft of the first three findings. Does this capture what you found accurately? Any changes needed before we continue?"

## Step 5: Recommendations Collection

**Objective:** Capture prioritized, actionable next steps with clear success metrics.

**For each recommendation (aim for 3-5 total):**

**Information to gather:**
1. **Title** - Action-oriented, clear name
2. **Root cause addressed** - Which finding does this fix?
3. **Expected impact** - Projected improvement in North Star Metric
4. **Effort required** - High/Medium/Low
5. **Timeline** - Implementation timeframe
6. **Action items** - 3-5 specific, concrete steps
7. **Success metrics** - How to measure if it worked

**Example questions:**

> "Based on your findings, what are your top 3-5 recommendations for addressing this problem?"

> "For each recommendation, let's capture some details. Starting with [Recommendation 1]:
> - What root cause or finding does this address?
> - What impact do you expect on the North Star Metric?
> - What's the effort required - high, medium, or low?
> - How long to implement?
> - What are the specific action items?
> - How will you measure success?"

**Help with prioritization:**
- "If you could only implement one, which would have the biggest impact?"
- "Which are quick wins vs longer-term investments?"
- "Which are prerequisites for others?"

## Step 6: Generate the Final Document

**Action:** Use the template to create a complete, polished markdown document.

**Template location:** [assets/analysis_results_template.md](assets/analysis_results_template.md)

**Required sections:**
1. Executive Summary (from synthesized findings)
2. Analysis Overview (from plan + actual scope)
3. Hypotheses Tested (summary table)
4. Detailed Findings (one section per analyzed hypothesis)
5. Hypotheses Not Analyzed (brief listing)
6. Impact Quantification (breakdown of contributions)
7. Recommendations (prioritized with details)
8. Implementation Roadmap (timeline of actions)
9. Appendix (methodology, data sources, limitations)

**Writing quality standards:**
- Use active voice and definitive language
- Lead each finding with the core conclusion
- Quantify everything possible
- Eliminate jargon
- Focus on business implications
- Keep findings to 3-5 paragraphs each
- Make it ready to share with executives

**Reference the writing guide for style and examples:** [references/writing_guide.md](references/writing_guide.md)

## Step 7: Review and Refine

**Present the complete document to the user:**
- Clearly show it's a draft for their review
- Ask for specific feedback on any sections
- Offer to revise as needed

**Common refinements:**
- Adjusting tone or detail level
- Adding or removing sections
- Reordering recommendations
- Clarifying ambiguous points
- Adding executive summary emphasis

**Once approved:**
- Save the final document as a .md file in the outputs directory
- Use a clear, descriptive filename like `Analysis_Results_7Day_Publish_Decline_2025-11-26.md`
- Provide the user with the link

## Critical Principles

### 1. Extract, Don't Transcribe
Users should not paste raw analyses. Your job is to extract communication-ready insights through guided questions.

### 2. One Hypothesis at a Time
Don't overwhelm users. Complete one hypothesis fully before moving to the next.

### 3. Focus on "So What"
Every finding should answer: "Why does this matter?" Business implications are mandatory.

### 4. Quantify Everything
Push for specific numbers, percentages, and metrics. Vague findings are weak findings.

### 5. Make It Distribution-Ready
The final document should be shareable with stakeholders immediately, with no additional polishing needed.

### 6. Use the References
The conversation_guide.md and writing_guide.md contain detailed patterns and examples. Consult them when stuck or when quality seems low.

## Handling Edge Cases

### User has no analysis plan
- Ask about the problem they investigated
- Get them to list the questions/hypotheses they explored
- Build structure from their verbal description
- Proceed with results collection

### User wants to paste entire analysis
- Politely redirect: "Rather than paste everything, let's work through the findings together so I can format them properly"
- Guide through the conversation structure
- Extract the key points

### User provides inconsistent information
- Acknowledge the confusion politely
- Ask clarifying questions
- Summarize your understanding and ask for confirmation
- Don't proceed until clarity is reached

### User is uncertain about impacts
- Accept rough estimates: "Even a ballpark figure is helpful"
- Offer ranges: "Would you say it's roughly 5-10% or more like 20-30%?"
- Document uncertainty: "Estimated impact: 5-10% (medium confidence)"

### Document is very long (>20 pages)
- Consider splitting into main report + appendices
- Focus on executive summary being comprehensive
- Detailed findings can be briefer
- Move supporting details to appendix

## Quality Checklist

Before finalizing the document, verify:
- [ ] All analyzed hypotheses have detailed findings
- [ ] Each finding has 3+ specific data points
- [ ] Impacts are quantified where possible
- [ ] Business implications are clear
- [ ] Recommendations are prioritized and actionable
- [ ] Document is free of jargon
- [ ] Writing uses active voice
- [ ] Executive summary stands alone
- [ ] Document is ready to share with stakeholders
- [ ] File is saved in outputs directory with clear name

## Success Metrics

This skill succeeds when:
- User can share the document directly with leadership
- Findings are clear to non-technical readers
- Recommendations are actionable and prioritized
- Document comprehensively answers the original question
- Process feels collaborative, not like an interrogation
- User feels their analytical work is well-represented
