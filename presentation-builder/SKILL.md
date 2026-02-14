---
name: presentation-builder
description: Transform analysis documents into structured presentation slide plans. Use when users need to convert markdown analysis documents into presentation decks, create slide-by-slide breakdowns with specific slide types and content structure, or plan presentation flow from analytical content. Outputs detailed slide specifications including slide types (Cover, Executive Summary, Text, Chart, Section) and all required content elements for each slide.
---

# Presentation Builder Skill

Transform analysis documents (in markdown format) into structured presentation slide plans with detailed content specifications for each slide.

## Overview

This skill takes an analysis document and produces a slide-by-slide presentation plan that follows presentation best practices. It does NOT create PowerPoint files - instead, it outputs a clear specification of what each slide should contain, including slide type and all content elements.

## Supported Slide Types

### 1. Cover Slide
- Title of analysis
- Date of analysis  
- Name of analyst

### 2. Executive Summary Slide
Uses the existing executive summary .md file (ask th suer about it). If no file, use the executive-summary-writer to write an executive summary and take the content of the resulting file to produce this slide

### 3. Text Slide (Bullet Points)
- Action Title (insight-driven, complete sentence)
- Bullet points (2-4 maximum)

### 4. Simple Chart Slide
- Action Title (insight-driven, complete sentence)
- Bullet points (1-2 key takeaways)
- Chart specification: [Metric | x-axis | chart type]

### 5. Double Chart Slide
- Action Title (insight-driven, complete sentence)
- Chart 1 specification: [Metric | x-axis | chart type]
- Chart 2 specification: [Metric | x-axis | chart type]
- Callout (key insight connecting both charts)

### 6. Section Slide
- Section number
- Section title

## Presentation Structure

Follow the pyramidal principle:
1. Cover slide
2. Executive Summary (MAIN framework)
3. Section dividers + content slides organized by theme
4. Next steps/recommendations
5. Q&A slide (optional)

## Output Format

For each slide, output:

```
SLIDE [number]: [Slide Type]

[Content specifications based on slide type]

---
```

### Example Output

```
SLIDE 1: Cover Slide

Title: Q3 Conversion Rate Analysis: Root Causes & Recovery Plan
Date: October 15, 2024
Analyst: Sarah Chen

---

SLIDE 2: Executive Summary

MOTIVE:
• Q3 conversion rate dropped 15pp (from 18% to 15%), missing target by 12%

Supporting points:
• Represents ~$1.2M annual recurring revenue at risk
• Urgent investigation conducted to identify root cause

ANSWER:
• Root cause: New onboarding flow (launched Sept 15) added friction at step 3

Supporting points:
• Drop isolated to new users (<7 days); returning users unaffected
• Recommend reverting flow immediately, redesigning with user feedback

IMPACT:
• Reverting flow should recover 10pp within 1 week (to 16%)

Supporting points:
• Full recovery to 18% expected within 3 weeks after redesign
• If not addressed, expect $300K Q4 revenue shortfall

NEXT-STEPS:
• Revert onboarding flow → Dev Team → Oct 2 (Tomorrow)

Supporting points:
• User research on friction points → UX Team → Oct 9
• Redesigned flow tested → Product Team → Oct 23
• Rollout decision meeting → Leadership → Oct 30

---

SLIDE 3: Section Slide

Section: 1
Title: Current Performance Analysis

---

SLIDE 4: Simple Chart Slide

Action Title: New Users Convert 30% Less Than Historical Cohorts

Bullet points:
• September cohort shows steepest decline vs. August baseline
• Drop appears immediately after onboarding flow change

Chart: [Conversion Rate by Cohort | Week | Line chart]

---

SLIDE 5: Double Chart Slide

Action Title: Mobile Users Drive 60% of Traffic But Show Lowest Conversion

Chart 1: [Traffic by Device | Month | Stacked bar chart]
Chart 2: [Conversion Rate by Device | Month | Line chart]

Callout: Mobile represents our biggest opportunity - fixing mobile experience could recover 8pp of lost conversion

---
```

## Guidelines

### Slide Titles
- Use complete sentences that state the insight
- NOT just topic names (✗ "Conversion Analysis" ✓ "New Users Convert 30% Less")
- Front-load the key message
- Keep to 8-12 words maximum

### Content Principles
- One message per slide
- Maximum 6 bullet points per slide
- Maximum 6 words per bullet point (guideline)
- Support every claim with data where possible
- Every slide should answer "So What?"

### Chart Specifications
Format: [Metric name | x-axis variable | chart type]

Common chart types:
- Line chart (trends over time)
- Bar chart (comparisons)
- Stacked bar chart (composition)
- Column chart (vertical comparisons)
- Area chart (cumulative trends)
- Scatter plot (correlations)
- Waterfall chart (sequential changes)

### Presentation Flow
1. Start with answer (Executive Summary)
2. Group related insights into sections
3. Use section dividers for major transitions
4. Build narrative logically
5. End with clear next steps

## Processing Steps

When given an analysis document:

1. **Extract key elements:**
   - Main question/objective
   - Key findings and insights
   - Supporting data and evidence
   - Recommendations
   - Next steps

2. **Structure the narrative:**
   - Create Executive Summary using MAIN framework
   - Identify 3-5 main themes/sections
   - Determine logical flow of insights
   - Plan section breaks

3. **Design each slide:**
   - Choose appropriate slide type
   - Write action-oriented title
   - Select supporting content
   - Specify chart requirements (if applicable)

4. **Output specification:**
   - Number slides sequentially
   - Format each slide according to type
   - Include all required content elements
   - Maintain consistent structure

## Quality Checks

Before finalizing output, verify:
- [ ] Executive Summary captures all MAIN elements
- [ ] Slide titles are insights, not topics
- [ ] Each slide has clear "So What?"
- [ ] Charts are specified with metric, axis, and type
- [ ] Flow is logical and builds narrative
- [ ] Section breaks mark major transitions
- [ ] Total slide count is appropriate (typically 12-20 for main deck)

## Flexibility

Adapt the structure based on:
- **Analysis type:** Root cause analysis, performance review, strategy recommendation
- **Audience:** Executive (fewer slides, high-level) vs. Technical (more detail)
- **Purpose:** Decision-making (focus on recommendations) vs. Informational (comprehensive)
- **Time available:** Adjust depth and number of slides accordingly

Default to 15-18 slides for a standard presentation unless specified otherwise.
