---
name: cohort-analysis-specialist
description: Track customer behavior over time by grouping customers based on shared characteristics or experiences. Use when measuring retention rates, understanding how customers evolve over time, comparing new vs old user behavior, evaluating product changes by cohort, identifying at-risk cohorts early, or calculating LTV by cohort. Essential for understanding retention, lifecycle patterns, and how product changes affect different user vintages.
---

# Cohort Analysis Specialist

Track customer behavior over time by grouping customers into cohorts for temporal analysis. Essential for understanding retention, lifecycle patterns, and product evolution.

## Core Framework: Understanding Cohorts

### What is a Cohort?
A group of users who share a common characteristic or experience within a defined time period.

**Most common:** Acquisition cohort (when they signed up)

**Why Cohorts Matter:**
Overall metrics can hide important trends. Example:
- Overall retention: 60%
- But actually: 2023 cohorts 75%, 2024 cohorts 45%
- Without cohorts, you wouldn't know new users perform worse!

## Cohort Types

### Type 1: Acquisition Cohorts
**Definition:** Grouped by signup/first purchase date

**Time granularity:**
- Daily (high volume, short analysis)
- Weekly (most common, balances detail/manageability)
- Monthly (strategic analysis, lower volume)
- Quarterly (very long-term trends)

**Best for:** Retention analysis, lifecycle understanding, LTV calculation

### Type 2: Behavioral Cohorts
**Definition:** Grouped by specific action

**Examples:** Activated cohort, Converters, Feature adopters, Engagement level

**Best for:** Feature impact analysis, engagement optimization

### Type 3: Attribute Cohorts
**Definition:** Grouped by characteristic at acquisition

**Examples:** Acquisition channel, Plan tier, Geographic, Segment

**Best for:** Channel quality, segment performance, market analysis

## Key Analysis: The Retention Table

### Classic Cohort Retention Table

**Structure:**
```
         M0   M1   M2   M3   M4   M5   M6
Jan 24   100% 65%  52%  45%  41%  38%  36%
Feb 24   100% 68%  55%  48%  44%  40%  38%
Mar 24   100% 70%  58%  51%  46%  42%  --
Apr 24   100% 72%  60%  53%  48%  --   --
May 24   100% 74%  62%  55%  --   --   --
Jun 24   100% 75%  63%  --   --   --   --
Jul 24   100% 76%  --   --   --   --   --
```

**How to read:**
- **Rows:** Each cohort (signup month)
- **Columns:** Time since signup
- **Cells:** % of original cohort still active
- **M0:** Always 100%
- **Diagonal:** Most recent data

**Key insights:**
1. Vertical: Compare same period across cohorts (M1 improving: 65%→76%)
2. Horizontal: See retention curve shape (steep drop early, then gradual)
3. Trends: Draw lines through columns to see improvement/decline

### Building a Retention Table (Descriptive)

**Data to Collect:**
- User signup dates grouped into cohorts (weekly or monthly)
- Activity data for each user in each subsequent period
- Definition of "active" (logged in, made purchase, used core feature)
- Time periods to track (typically 6-12 months)

**How to Analyze:**

*Analysis 1: Create Retention Table*
- **Format:** Table with cohorts as rows, time periods as columns
- **Calculate:** For each cohort and period, % of original cohort active
- **Color coding:** Use heat map (red <40%, orange 40-60%, yellow 60-75%, green >75%)
- **Mark:** Incomplete data (recent cohorts) clearly

*Analysis 2: Cohort Retention Curves*
- **Chart type:** Line chart
- **X-axis:** Time periods (M0, M1, M2, etc.)
- **Y-axis:** Retention rate (%)
- **Lines:** One line per cohort
- **Look for:** Separation between cohorts, curve shapes

*Analysis 3: Period-Specific Trends*
- **Chart type:** Line chart showing trends over time
- **X-axis:** Cohort (chronological)
- **Y-axis:** Retention rate
- **Lines:** Separate line for M1, M2, M3 retention
- **Look for:** Improvement or decline in specific periods

**What to Look For:**

*Good patterns:*
- Recent cohorts performing better than old (product improving)
- Curves plateau after M3-M6 (stable long-term retention)
- M1 retention >40%, M3 retention >30%

*Bad patterns:*
- Recent cohorts worse than old (product degrading)
- No plateau, continuous decline (no loyal base forming)
- Steep early drop that never recovers

## Key Metrics from Cohort Analysis

### D1/D7/D30 Retention
**Definition:** % active on specific day after signup

**Milestones:**
- D1 (Next Day): Immediate value delivery (target >40%)
- D7 (Week 1): Habit formation (target >30%)
- D30 (Month 1): Product stickiness (target >20%)

**Analysis:**
- Compare D1/D7/D30 across cohorts
- Track trends over time
- Identify which milestone is weakening

### Retention Curve Shape Analysis
**Question:** How does retention decay over time?

**Patterns:**
- **Smiling curve:** Dip then recovery (common in B2B, slow onboarding)
- **Flat after dip:** Initial drop then stable (good pattern)
- **Continuous decline:** No stickiness, churn risk
- **Plateau:** Healthy engaged user base

### Cohort Lifetime Value (LTV)
**Calculate:** Revenue per cohort over lifetime

**Analysis:**
- Compare LTV across cohorts (improving or declining?)
- Calculate time to 80% of LTV (payback period)
- Segment LTV (by channel, segment, etc.)

**Use for:** CAC targets, pricing strategy, prioritization

## Advanced Techniques

### Leading Indicator Analysis
**Method:** Identify early behaviors predicting long-term retention

**Process:**
1. For mature cohorts, identify who retained long-term
2. Look back at their Week 1 behavior
3. Find patterns predicting retention

**Example findings:**
- Users with 3+ sessions in Week 1: 75% retained at M6
- Users who invited teammate: 82% retained at M6
- Users with <3 sessions: 15% retained at M6

**Application:** Track leading indicators in new cohorts for early warning

### Segment Migration Analysis
**Track:** Movement between segments over time

**Example:**
- 80% of power users stay power users (good)
- 15% of power users become casual (warning)
- 20% of casual users become power (opportunity)

**Insight:** Understand what causes upgrades/downgrades

### Cohort Comparison
**Method:** Compare two cohorts directly

**Use for:**
- A/B test impact evaluation
- Channel quality comparison
- Feature launch impact assessment

**Analysis:**
- Side-by-side retention curves
- Statistical significance testing
- Quantify difference magnitude

## Common Pitfalls & Solutions

**Pitfall 1: Incomplete Cohorts**
- Problem: Recent cohorts have limited data
- Solution: Mark incomplete data clearly, focus on same maturity points

**Pitfall 2: Cohort Size Variation**
- Problem: Different sized cohorts make comparison hard
- Solution: Always use percentages, not absolutes

**Pitfall 3: Seasonality Confusion**
- Problem: Seasonal patterns mistaken for cohort differences
- Solution: Compare to same period prior year, adjust for seasonality

**Pitfall 4: Definition Changes**
- Problem: Changing "active" definition mid-analysis
- Solution: Lock definitions, clearly mark any changes

**Pitfall 5: Cherry-Picking Metrics**
- Problem: Only showing metrics that look good
- Solution: Report full retention curve, be transparent

## Analysis Templates

### Template: Cohort Retention Report

**Structure:**
1. Executive Summary (trends in 2-3 sentences)
2. Cohort Retention Table (with color coding)
3. Key Metrics (D1/D7/D30 trends)
4. Cohort Comparison (best vs worst, why)
5. Analysis (what's working, what's not, early warnings)
6. Recommendations (actions with owners)

### Template: Cohort LTV Analysis

**Structure:**
1. Summary table (cohort, size, age, actual LTV, projected LTV, maturity)
2. LTV trends (by vintage)
3. Time to 80% LTV
4. LTV components (ARPU trend, lifetime trend)
5. Recommendations

## Validation Checklist

**Data Quality:**
- [ ] Cohorts defined consistently
- [ ] "Active" definition clear and constant
- [ ] Tracking verified accurate
- [ ] No data gaps in period

**Analysis Quality:**
- [ ] Incomplete cohorts marked clearly
- [ ] Appropriate time horizons shown
- [ ] Statistical significance noted
- [ ] Comparisons are fair (same maturity)

**Presentation:**
- [ ] Retention table easy to read
- [ ] Color coding helpful
- [ ] Key insights called out
- [ ] Trends clearly visible

**Actionability:**
- [ ] "So What?" is clear
- [ ] Recommendations specific
- [ ] Next steps have owners

## Related Agents & Skills

**Prerequisites:**
- 📊 KPI Definition Specialist - Define retention properly
- 🌳 KPI Tree Architect - Retention in broader context

**Use together:**
- 👥 Segmentation Expert - Segment within cohorts
- 🎯 Mix Effect Analyzer - Separate cohort from performance
- 📋 Analysis Planner - Plan cohort analysis properly

**For insights:**
- 🔍 Root Cause Investigator - Explain cohort differences
- 📝 Executive Summary Writer - Communicate findings
- 📊 Chart & Visualization Advisor - Create cohort visuals

## Success Metrics

Mastered cohort analysis when:
- ✅ Can build retention table in <30 minutes
- ✅ Identify trends and outliers immediately
- ✅ Predict future performance from early cohorts
- ✅ Retention analysis drives product decisions
- ✅ Early warning system catches issues proactively

## Key Principles

From "The Power of Analytics":
- "Cohorts help you understand if improvements are real or just mix effects"
- "Track cohorts to see product evolution impact over time"
- "Early cohort behavior predicts long-term retention"
- "Cohort analysis is essential for comparing apples to apples"

See references/retention_table_guide.md for detailed table creation
See references/cohort_metrics.md for complete metrics catalog
