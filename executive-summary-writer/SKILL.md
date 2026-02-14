---
name: executive-summary-writer
description: Transform analysis findings into clear, actionable executive summaries using the MAIN framework (Motive, Answer, Impact, Next steps) and Pyramidal Principle. Use when completing any analysis that needs stakeholder buy-in, preparing for leadership meetings, documenting investigation findings, writing business reviews, creating post-mortems, proposing initiatives based on data, or communicating insights to executives.
---

# Executive Summary Writer

Transform complex analysis into clear, actionable executive summaries that drive decision-making.

## Workflow

### Phase 1: Understand the Context

Ask the user:

**"Do you have an analysis file that contains the context and results of your analysis?"**

**If YES:**
- Request the file
- Read and analyze the content
- Extract: business context, key findings, data/metrics, recommendations (if any)
- Proceed to Phase 2 with extracted information

**If NO:**
- Explain you'll gather information through questions
- Proceed to Phase 2 with interactive questioning

### Phase 2: Gather MAIN Components

Collect information for each component in order. If information was extracted from a file, confirm/clarify missing pieces. If no file, ask targeted questions:

#### M - Motive (2-4 sentences, 50-100 words)
Ask:
- "What business problem or context triggered this analysis?"
- "What recent changes or trends prompted this investigation?"
- "Who is affected and what's at stake?"

**Confirm you have:**
- Business context
- Triggering event
- Scope/focus

#### A - Answer (3-5 sentences, 75-125 words)
Ask:
- "What did you find? (Main findings in 1-2 sentences)"
- "What do you recommend should be done?"
- "What outcome do you expect if this recommendation is followed?"

**Validate with "So What?" test:**
- Can someone act on this without reading further?
- Is it clear what success looks like?
- Would a busy executive understand the takeaway?

#### I - Impact (3-5 sentences, 75-150 words)
Ask:
- "What business metrics are affected? (revenue, users, costs)"
- "What's the magnitude? (specific numbers)"
- "What's the timeline for impact?"
- "What happens if no action is taken?"

**Ensure you have:**
- Quantified positive impact (with numbers and units)
- Quantified negative impact/risk
- Timeline and confidence level

#### N - Next Steps (3-7 items, 100-200 words)
Ask:
- "What specific actions need to happen?"
- "Who owns each action?"
- "What are the timelines/ETAs?"
- "How will success be measured?"

**Each action must have:**
- Specific action (not vague)
- Owner (name, not team)
- ETA (date)
- Success criteria

### Phase 3: Draft & Review

1. **Generate the executive summary** using the MAIN structure
2. **Present draft to user** for review
3. **Iterate based on feedback**

### Phase 4: Quality Check

Before finalizing, verify:

**Content Quality:**
- [ ] Answer appears in first 3 sentences
- [ ] "So What?" is crystal clear
- [ ] All impacts quantified with units ($, %, numbers)
- [ ] Recommendations specific and actionable
- [ ] Owners and dates assigned to all actions
- [ ] Can be understood without further sections
- [ ] Under 1 page for executive summary section

**Writing Quality:**
- [ ] Active voice (not passive)
- [ ] Short sentences and paragraphs
- [ ] No jargon without explanation
- [ ] Numbers formatted consistently
- [ ] Specific numbers over vague terms ("40%" not "many")

### Phase 5: Deliver

Create a clean document with:
1. Executive Summary (MAIN format)
2. Optional: Supporting sections if user requests them

Save to `/mnt/user-data/outputs/executive-summary.md`

## Key Principles

**Answer First**: Always state findings and recommendations upfront, then support with context.

**Quantify Everything**: Use specific numbers with units. "15% drop (from 40% to 34%)" not "significant decrease."

**Be Specific**: "Design 3 new onboarding flows by Nov 30 - Owner: Jane" not "Improve onboarding."

**Pass the "So What?" Test**: Executive must understand what to do without reading further.

**Keep It Brief**: Executive summary = 1 page maximum. Details go in appendix.

## Framework Reference

For detailed guidance on each MAIN component, see:
- `references/main-framework.md` - Complete framework with examples
- `references/templates.md` - Templates for different scenarios
- `references/examples.md` - Good vs bad examples

## Output Format

```markdown
# [Topic] - Executive Summary

## Motive
[2-4 sentences on context and why this matters]

## Answer
[3-5 sentences: findings, recommendation, expected outcome]

## Impact
[3-5 sentences: quantified business implications]

## Next Steps
1. [Action] - Owner: [Name] - ETA: [Date] - Success: [Metric]
2. [Action] - Owner: [Name] - ETA: [Date] - Success: [Metric]
3. [Action] - Owner: [Name] - ETA: [Date] - Success: [Metric]
```

## Common Pitfalls to Avoid

- **Burying the lede**: Don't save the answer for later. State it upfront.
- **Vague recommendations**: "Improve UX" → "Add 3-step interactive tutorial by Dec 15"
- **No quantification**: "Big impact" → "$500K annual revenue at risk"
- **Too much detail upfront**: Save detailed analysis for appendix
- **No "So What?"**: Always explain implications and required actions

## User Interaction Guidelines

- **Be conversational**: Ask one question at a time, don't overwhelm
- **Show progress**: Let user know which component you're working on
- **Confirm understanding**: Repeat back key points for validation
- **Offer examples**: If user is stuck, provide examples to clarify
- **Stay focused**: Keep gathering info for MAIN, resist tangents
- **Validate completeness**: Before drafting, confirm you have all pieces
