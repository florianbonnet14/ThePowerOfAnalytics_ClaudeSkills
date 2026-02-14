---
name: segmentation-expert
description: Identify, analyze, and act on customer segments to uncover hidden patterns and understand behavior differences. Use when investigating KPI changes to understand which customers drove them, planning targeted initiatives, building customer personas, or analyzing performance differences across groups. Helps select meaningful segmentation dimensions, create actionable segments, analyze performance differences, calculate segment contributions, and generate segment-specific recommendations.
---

# Segmentation Expert

Identify and analyze customer segments to uncover hidden patterns, understand behavior differences, and tailor strategies for maximum impact.

## Core Framework: The Segmentation Process

### Phase 1: Define Segmentation Dimensions

**Main Dimension Categories:**

**1. Demographic** (B2C: age, gender, location; B2B: company size, industry, funding stage)
**2. Behavioral** (usage level, feature adoption, session frequency, purchase patterns)
**3. Acquisition** (channel, campaign, referrer, first touchpoint)
**4. Lifecycle** (tenure, cohort, stage, product tier, upgrade history)
**5. Psychographic** (job to be done, use case, goals, pain points)
**6. Firmographic** (B2B: industry, revenue, employee count, tech stack)

### Phase 2: Select Relevant Dimensions

**Selection Criteria (Score 1-5 each):**

1. **Actionability:** Can you do something different for this segment?
2. **Measurability:** Can you identify segment membership easily?
3. **Size/Viability:** Is segment large enough (typically >5%)?
4. **Stability:** Does definition remain consistent over time?
5. **Differentiation:** Do segments behave differently (>20% performance difference)?

**Selection Process:**
1. Brainstorm all possible dimensions (10-20)
2. Score each on 5 criteria (max 25 points)
3. Select top 3-5 dimensions (score >15/25)
4. Validate with data (check if differences exist)

### Phase 3: Create Segments

**Methods:**

**Rules-Based:** Explicit rules define membership
- Example: "Power Users = >20 sessions/month AND use >5 features"
- Best for: Operational segmentation, clear behavioral groups

**Value-Based:** Segment by value delivered/generated
- Example: "High-Value = Top 20% by LTV"
- Best for: Prioritization, resource allocation

**RFM (Recency, Frequency, Monetary):** Classic for transaction businesses
- Champions: Recent, Frequent, High-Value
- At-Risk: Previously high-value, now less recent
- Best for: E-commerce, SaaS with usage tiers

**Clustering (Statistical):** Algorithm finds natural groupings
- K-means, hierarchical clustering, DBSCAN
- Best for: Exploratory analysis, persona development

**Persona-Based:** Segments based on goals, use cases, JTBD
- Best for: Product strategy, positioning

### Phase 4: Analyze Segment Performance

**For each segment, describe analysis in words:**

**Data to Collect:**
- Segment size (number of users, % of total)
- Key metrics per segment (conversion, retention, engagement, LTV)
- Time trends for each segment
- Overlap with other segmentation dimensions

**How to Analyze:**

*Analysis 1: Segment Size and Composition*
- **Chart type:** Pie chart or stacked bar
- **Show:** % of total users or revenue per segment
- **Compare:** Current period vs previous period

*Analysis 2: Performance Comparison*
- **Chart type:** Grouped bar chart or comparison table
- **X-axis:** Segments
- **Y-axis:** Key metric (conversion rate, LTV, retention, etc.)
- **Show:** Performance difference between segments
- **Highlight:** Best and worst performing segments

*Analysis 3: Trend Over Time*
- **Chart type:** Multi-line chart
- **X-axis:** Time (weeks or months)
- **Y-axis:** Key metric
- **Lines:** One line per segment
- **Look for:** Divergence or convergence of segments

**What to Look For:**

*Segment differences:*
- Which segments perform significantly better/worse (>20% difference)?
- Is the difference consistent over time?
- Are differences statistically significant?

*Segment contribution:*
- Which segments drive most of the overall metric change?
- Calculate contribution: (Segment size × Performance difference)

*Actionable patterns:*
- What characteristics define high-performing segments?
- Can low-performing segments be improved or high-performing ones scaled?

### Phase 5: Generate Recommendations

**Framework:**

For each segment, specify:
- **Current Performance:** What metrics show
- **Root Cause:** Why this segment performs this way
- **Opportunity:** What could be improved
- **Action:** Specific, testable intervention
- **Expected Impact:** Quantified improvement estimate
- **Priority:** Based on impact × feasibility

## Segmentation Patterns

### Pattern 1: Acquisition Channel Segmentation

**Use when:** Understanding marketing effectiveness

**Dimensions:** Organic, Paid, Referral, Partnership, Direct

**Analysis approach:**
- Compare conversion, retention, LTV by channel
- Calculate CAC and payback period by channel
- Identify highest quality channels

### Pattern 2: Usage Level Segmentation

**Use when:** Understanding engagement

**Dimensions:** Power Users, Regular Users, Casual Users, Inactive

**Rules example:**
- Power: >20 sessions/month
- Regular: 10-20 sessions/month
- Casual: 1-9 sessions/month
- Inactive: 0 sessions/month

**Analysis approach:**
- Track distribution over time
- Analyze migration between segments
- Identify "aha moment" that moves users up

### Pattern 3: Lifecycle Stage Segmentation

**Use when:** Optimizing customer journey

**Dimensions:** Trial, Active, At-Risk, Churned, Resurrected

**Analysis approach:**
- Track stage transitions
- Measure time in each stage
- Identify interventions that move users forward

### Pattern 4: Value-Based Segmentation

**Use when:** Prioritizing retention/expansion

**Dimensions:** High-Value (top 20%), Medium-Value (middle 60%), Low-Value (bottom 20%)

**Analysis approach:**
- Calculate LTV per segment
- Analyze retention patterns by value tier
- Identify expansion opportunities

## Advanced Techniques

### Hierarchical Segmentation
Create segments within segments for deeper analysis

Example:
```
Level 1: Plan Tier
└─ Free Users
   └─ Level 2: By Engagement
      ├─ Active (target for conversion)
      └─ Inactive (nurture or ignore)
└─ Paid Users
   └─ Level 2: By Value
      ├─ High LTV (retain)
      ├─ Medium LTV (expand)
      └─ Low LTV (improve)
```

### Segment Migration Analysis
Track movement between segments over time

Example analysis:
- % of power users who become casual (churn risk)
- % of casual users who become power (growth opportunity)
- Identify triggers for positive/negative migrations

### Segment-Specific Funnels
Different conversion paths for different segments

Example:
- Enterprise: Demo → Trial → Negotiation → Contract
- SMB: Signup → Activation → Aha Moment → Paid

Analyze conversion rates separately for each segment.

## Common Mistakes & Fixes

**Mistake 1: Too Many Segments**
- Problem: 20 segments, can't act on all
- Fix: Start with 3-5 high-level segments, refine later

**Mistake 2: Segments Can't Be Targeted**
- Problem: "Users who will churn next month"
- Fix: Use leading indicators you can identify early

**Mistake 3: Static Segmentation**
- Problem: Never revisit definitions
- Fix: Review quarterly, evolve as business evolves

**Mistake 4: Equal Treatment of Unequal Segments**
- Problem: Focus on largest segment regardless of value
- Fix: Prioritize by strategic value × actionability

**Mistake 5: Confusing Correlation with Causation**
- Problem: "Enterprise customers convert better because they're enterprises"
- Fix: Identify mechanism (onboarding support, budget pressure, clear use case)

## Validation Checklist

**Definition Quality:**
- [ ] Each segment has clear, objective definition
- [ ] Segments are mutually exclusive (no overlap)
- [ ] Segments are collectively exhaustive (cover everyone)
- [ ] Can assign any user to segment programmatically

**Business Relevance:**
- [ ] Segments differ meaningfully (>20% on key metrics)
- [ ] Can take different actions for each segment
- [ ] Segments are large enough (typically >5%)
- [ ] Stakeholders understand segmentation

**Operational Feasibility:**
- [ ] Can identify segment membership in real-time
- [ ] Can report on segments in dashboards
- [ ] Can target segments in campaigns/product
- [ ] Team has resources to act on segments

**Analytical Validity:**
- [ ] Validated with sufficient data
- [ ] Differences are statistically significant
- [ ] Patterns persist over time
- [ ] Controls for confounding factors

## Related Agents & Skills

**Prerequisites:**
- 🌳 KPI Tree Architect - Segment KPIs from tree
- 📊 KPI Definition Specialist - Define metrics per segment

**Use together:**
- 🔍 Root Cause Investigator - Segment to find root cause
- 📅 Cohort Analysis Specialist - Segment + time = cohorts
- 🎯 Mix Effect Analyzer - Quantify segment contributions
- 📋 Analysis Planner - Plan segment analysis properly

**For outputs:**
- 📊 Chart & Visualization Advisor - Visualize segment differences
- 📝 Executive Summary Writer - Communicate insights

## Success Metrics

Segmentation is effective when:
- ✅ Can identify 3-5 actionable segments
- ✅ Team talks about segments in planning
- ✅ Product roadmap prioritizes by segment
- ✅ Marketing campaigns tailored by segment
- ✅ Segments drive meaningful decisions

## Key Principles

From "The Power of Analytics":
- "Segmentation allows you to drill down and extract hidden patterns"
- "Find segments that behave differently enough to warrant different treatment"
- "Always ask: can I do something different for this segment?"
- "Segmentation helps you move from 'what happened' to 'what happened to whom'"

See references/segmentation_dimensions.md for complete dimension catalog
See references/segmentation_methods.md for detailed method comparisons
