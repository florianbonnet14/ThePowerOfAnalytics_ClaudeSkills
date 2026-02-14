---
name: influential-factors-detective
description: Identify and analyze qualitative factors that influence KPIs but can't be measured as numbers. Use when users need to find non-quantifiable drivers affecting metrics (like copy quality, design aesthetics, timing), plan A/B tests for subjective elements, bridge the gap between data and design/content decisions, understand why quantitative analysis is incomplete, optimize messaging or UX elements, or identify the actual levers to pull for improving KPIs at the leaf nodes of a KPI tree.
---

# Influential Factors Detective

Systematically identify and test qualitative factors that drive KPI performance but can't be directly measured.

## Core Concept

**Influential Factors** = Elements you can change that affect KPIs, but whose "quality" can't be directly measured—only their impact on downstream metrics.

**Location in KPI Tree:**
```
North Star Metric
├─ Quantifiable KPI
│  └─ Quantifiable KPI
│     └─ 🔍 Influential Factor (qualitative leaf node)
```

**Key insight:** Quantitative analysis tells you WHERE the problem is. Influential factors tell you WHAT to change.

## When to Use This Skill

Trigger this skill when:
- User asks to identify influential factors for a KPI
- KPI changed but quantitative drivers don't explain why
- User needs to optimize subjective elements (copy, design, UX)
- User wants to plan A/B tests
- User asks "what can we change?" after reaching KPI tree leaf nodes
- User needs to bridge analytics and creative decisions

## Six Categories of Influential Factors

### 1. Copy & Messaging
Word choice, tone, length, clarity, emotional appeal, value prop framing, CTA phrasing, urgency language

**Example:** Email subject line—can't measure "quality" but can test which one drives higher open rates

### 2. Visual Design
Layout, colors, typography, visual hierarchy, images, icons, button design, white space

**Example:** CTA button color—can't measure "effectiveness" but can test which color drives more clicks

### 3. User Experience
Navigation, form fields, progress indicators, error messages, loading states, micro-interactions

**Example:** Form length—can't measure "optimal length" but can test 5 vs 10 vs 15 fields

### 4. Timing & Frequency
Time of day, day of week, contact frequency, delay periods, pacing, response expectations

**Example:** Email send time—can't measure "best time" universally but can test 8am vs 12pm vs 6pm

### 5. Content & Media
Format (image/video/text), storytelling approach, depth, technical level, personalization

**Example:** Product demo format—can't measure "best format" but can test video vs screenshots vs interactive

### 6. Positioning & Placement
Above/below fold, sidebar vs main content, modal vs banner, navigation placement, feature prominence

**Example:** CTA placement—can't measure "ideal position" but can test top vs bottom vs sticky

## Four Methods to Identify Influential Factors

### Method 1: KPI Tree Leaf Analysis

**When:** Working with an existing KPI tree

**Process:**
1. Navigate to bottom-level quantifiable KPIs
2. Ask: "What elements can I change that affect this metric?"
3. List all changeable but non-measurable elements
4. Document as 🔍 influential factors

**Template:**
```
For KPI: [Name]

Influential Factors:
1. [Factor] - [How it affects KPI] - [Current state] - [Alternatives]
2. [Factor] - [How it affects KPI] - [Current state] - [Alternatives]
```

### Method 2: Comparison Analysis

**When:** Two similar things perform differently

**Process:**
1. Identify comparable elements (Feature A vs B, Page X vs Y)
2. List quantitative differences (traffic, engagement)
3. List qualitative differences (copy, design, placement)
4. Hypothesize which qualitative differences drive performance gap

**Example:**
```
Landing Page A: 15% conversion | Landing Page B: 8% conversion
Qualitative differences:
- Headline (benefit vs feature)
- Hero image (people vs product)
- CTA color, Form length, Social proof placement
→ Test these factors systematically
```

### Method 3: User Research Insights

**Sources:** Interviews, usability tests, session recordings, support tickets, surveys

**Process:**
1. Collect qualitative feedback ("confusing," "overwhelming," "unclear")
2. Map feedback to potential factors
3. Form hypotheses about improvements

**Example:**
```
Feedback: "Wasn't sure if plan included X feature"
→ Factors: Feature list completeness, description clarity, comparison design
→ Hypothesis: Adding use case examples will increase conversion
```

### Method 4: Best Practice Benchmarking

**Process:**
1. Research industry best practices
2. Compare your implementation
3. Identify gaps as testable factors

## Four Testing Approaches

### A/B Testing (sufficient traffic)
- Test one factor at a time
- Create control + variant(s)
- Run to statistical significance
- Document and implement winner

### Sequential Testing (low traffic)
- Measure baseline (2 weeks)
- Make change
- Measure new performance (2 weeks)
- Compare accounting for seasonality

### Multivariate Testing (high traffic, multiple factors)
- Test combinations of factors
- Requires 8x+ traffic vs simple A/B
- Reveals interaction effects
- Use sparingly

### Qualitative Testing (early exploration)
- Usability testing (5-10 users)
- Preference testing (side-by-side)
- 5-second tests (recall measurement)
- Inform quantitative test priorities

## Workflow

### Initial Assessment
1. Ask user about their KPI and context
2. Determine which method(s) to use for identifying factors
3. Clarify: leaf node analysis, comparison, user feedback, or benchmarking?

### Factor Identification
1. Apply chosen method(s)
2. List all potential influential factors
3. Categorize by type (copy, design, UX, timing, content, placement)
4. For each factor, document:
   - How it could affect the KPI
   - Current state
   - Alternative options to test

### Prioritization
Use Impact/Effort matrix:
- **High Impact, Low Effort** → Quick wins, test first
- **High Impact, High Effort** → Big bets, plan carefully
- **Low Impact, Low Effort** → Fill-ins, test if easy
- **Low Impact, High Effort** → Avoid

Score = Estimated Impact (1-5) / Effort to Test (1-5)

### Test Planning
For top-priority factors:
1. Choose testing approach (A/B, sequential, multivariate, qualitative)
2. Define success metrics and guardrails
3. Design variations
4. Plan implementation and documentation

### Documentation
Provide factor documentation using template in `references/templates.md`

## Output Format

```markdown
# Influential Factors for [KPI Name]

## Analysis Method(s) Used
[KPI Tree Leaf Analysis / Comparison / User Research / Benchmarking]

## Identified Factors

### Category: [Copy & Messaging / Visual Design / etc.]

#### Factor 1: [Name]
- **Parent KPI:** [Which KPI this affects]
- **Description:** [What this factor is]
- **Current State:** [How it's currently implemented]
- **Hypothesis:** [How changing this could improve the KPI]
- **Test Variations:** 
  - Control: [Current]
  - Variant A: [Option 1]
  - Variant B: [Option 2]

[Repeat for each factor]

## Prioritization

| Factor | Category | Impact (1-5) | Effort (1-5) | Priority Score | Recommendation |
|--------|----------|--------------|--------------|----------------|----------------|
| [Name] | [Category] | [#] | [#] | [Score] | [Quick Win/Big Bet/etc.] |

## Recommended Testing Sequence

1. **[Factor Name]** - [Testing approach] - [Why first]
2. **[Factor Name]** - [Testing approach] - [Why second]
3. **[Factor Name]** - [Testing approach] - [Why third]

## Next Steps

1. [Specific action]
2. [Specific action]
3. [Specific action]
```

## Common Patterns by Context

**Email Marketing:** Subject lines, from name, preview text, send time, content format, CTA count

**Landing Pages:** Headlines, hero images, social proof placement, form fields, trust signals

**In-Product:** Onboarding steps, empty states, feature discovery, notification frequency

**Checkout Flows:** Form fields, error messages, trust indicators, guest checkout, progress indication

See `references/common-factors.md` for comprehensive lists by context.

## Key Reminders

- Influential factors are the LEAF NODES of your KPI tree
- You can't measure their "quality" directly—only their impact on metrics
- Test systematically: one factor at a time (unless multivariate with sufficient traffic)
- Document all tests: winners, losers, and learnings
- Build institutional knowledge over time
- Target 2-4 tests per month minimum
- Win rate >40% indicates good hypothesis generation

## Reference Materials

- `references/templates.md` - Documentation templates for factors and test logs
- `references/common-factors.md` - Comprehensive lists of factors by business context
- `references/case-studies.md` - Detailed examples with results and learnings

## Integration with Other Skills

**Prerequisites:**
- **kpi-tree-architect** - Provides the KPI tree structure where factors live as leaf nodes
- Work with KPI Tree Architect to identify where in the tree to add 🔍 influential factors

**Complementary:**
- Use root cause analysis to identify which factors to test when KPIs change
- Use A/B testing advisors for proper test design
- Use dashboard designers to track test results

## Quality Checklist

Before testing an influential factor:

**Factor Definition:**
- [ ] Clear description
- [ ] Know which KPI it affects  
- [ ] Specific hypothesis
- [ ] Alternatives identified

**Test Design:**
- [ ] Success metric defined
- [ ] Sample size calculated
- [ ] Duration estimated
- [ ] Guardrail metrics identified

**Implementation:**
- [ ] Variations ready
- [ ] Tracking implemented
- [ ] QA completed
- [ ] Rollout plan defined
