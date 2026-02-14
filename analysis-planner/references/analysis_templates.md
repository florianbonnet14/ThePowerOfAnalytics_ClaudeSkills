# Analysis Templates by Type

## Template 1: Root Cause Investigation

```markdown
# [Metric] Investigation - Analysis Plan

**Analysis Date:** [Date]
**Status:** Planning Complete - Ready for Execution

---

## Executive Summary

**Problem Statement:**
[The metric/KPI] changed by [X%] in [time period].

**Primary Question:**
Why did [metric] change by [X%], and what actions should we take?

**Decision to be Made:**
[What will stakeholders decide based on findings]

**Timeline:** [X days]
**Expected Deliverable:** Root cause analysis, impact sizing, and prioritized action plan

---

## Success Criteria

### A successful analysis will:
1. Identify the primary driver(s) causing the change
2. Quantify how much each driver contributes
3. Recommend specific, actionable interventions
4. Provide timeline estimates for implementation

### We'll know we're done when:
- We can explain at least 80% of the change
- We have validated findings with data
- Stakeholders agree the root cause is clear
- We have a prioritized action plan

### The answer will enable us to:
- Allocate resources to highest-impact fixes
- Set realistic expectations
- Prevent similar issues in the future

---

## Context

### Metric Definition
**Metric:** [Full definition]

### KPI Tree
```
[Show how metric breaks down into components]
```

### Recent Changes
- [Change 1]
- [Change 2]
- [Change 3]

---

## Hypotheses (Prioritized)

### TIER 1 - Highest Priority

#### H1: [Hypothesis Statement]
- **Driver:** [Which KPI component]
- **Hypothesis:** [What we think happened]
- **Expected Contribution:** [X-Y% of total change]
- **Priority Score:** [X/10] (Probability × Impact × Actionability)

**Data to Collect:**
- [Data point 1: e.g., "Number of users completing step X, by day, for last 8 weeks"]
- [Data point 2: e.g., "Time spent at each stage, segmented by user type"]
- [Data point 3: e.g., "Drop-off rates at each funnel step"]
- [Segmentation: By acquisition channel, device type, geography]

**How to Analyze:**

*Analysis 1: Trend Analysis*
- **Chart type:** Line chart
- **X-axis:** Time (daily or weekly for last 8 weeks)
- **Y-axis:** [Metric] rate or absolute number
- **Lines to plot:** 
  - Overall metric
  - Each component/step if applicable
- **Add reference line:** Average from previous stable period
- **Annotations:** Mark any product releases or changes

*Analysis 2: Breakdown Comparison*
- **Chart type:** Grouped bar chart or comparison table
- **Structure:** Before period vs After period
- **Segments to show:** [Dimension 1, Dimension 2, Dimension 3]
- **Highlight:** Segments with largest changes

*Analysis 3: Detailed Funnel*
- **Chart type:** Funnel visualization or step-by-step table
- **Show:** Conversion rate at each step
- **Compare:** Previous period vs current period
- **Calculate:** Percentage point change at each step

**What to Look For:**

*To VALIDATE this hypothesis:*
- [Metric/component] decreased by [X+] percentage points
- The decrease is concentrated in [specific area]
- Timing of decrease correlates with [event/change]
- Effect is visible across multiple segments (not isolated)
- [Additional validation criterion]

*To INVALIDATE this hypothesis:*
- [Metric] remained stable (change <2 percentage points)
- Decrease is evenly distributed (no clear driver)
- Timing doesn't match any changes
- Only one narrow segment affected (suggests different cause)
- [Additional invalidation criterion]

**Proposed Deep-Dives if Validated:**

1. **[Deep-dive 1 title]**
   - Drill into [specific aspect]
   - Analyze [specific data]
   - Look for [specific patterns]

2. **[Deep-dive 2 title]**
   - Compare [segment A] vs [segment B]
   - Measure [additional metric]
   - Validate [specific hypothesis refinement]

3. **[Deep-dive 3 title]**
   - Review qualitative data (user feedback, support tickets)
   - Conduct [specific analysis]
   - Confirm [mechanism]

---

#### H2: [Next Hypothesis]
[Same detailed structure as H1]

---

### TIER 2 - Medium Priority

#### H3: [Hypothesis]
[Same structure]

---

### TIER 3 - Lower Priority

#### H4: [Hypothesis]
[Same structure]

---

## Analysis Strategy

**Approach:** [e.g., "Progressive funnel investigation - work through KPI tree sequentially"]

**Testing Order:**
1. Test H1 first (highest priority)
2. If H1 explains >50% of change, deep-dive there
3. If H1 explains <50%, test H2
4. Continue until 80%+ of change explained

**Decision Points:**
- After testing each tier, decide whether to continue or deep-dive
- If multiple hypotheses validated, quantify contribution of each
- Stop when 80% of change explained or all major hypotheses tested

---

## Success Metrics for This Analysis

- [ ] Root cause identified with >80% confidence
- [ ] At least 80% of change quantitatively explained
- [ ] 3-5 prioritized recommendations with impact estimates
- [ ] Stakeholder alignment on findings
- [ ] Analysis completed within [X] days
- [ ] Data-driven findings (not speculative)
- [ ] Clear action items with owners

---

## Recommendations Template (To be filled post-analysis)

### Recommendation 1: [Title]
- **Problem:** [What's broken]
- **Root Cause:** [Why it's broken]
- **Proposed Fix:** [What to do]
- **Expected Impact:** [Quantified improvement]
- **Effort:** [Estimated effort]
- **Timeline:** [When implementable]
- **Priority:** [High/Medium/Low]
- **Owner:** [Who will do it]

### Recommendation 2: [Title]
[Same structure]

### Recommendation 3: [Title]
[Same structure]
```

## Template 2: Experiment Analysis Plan

```markdown
# Experiment Analysis: [Name]

## Hypothesis
[What we're testing and expected outcome]

## Success Metrics
- **Primary:** [Metric] - Need [X%] lift at 95% confidence
- **Secondary:** [Metric] - Monitor for regression
- **Guardrail:** [Metric] - Must not degrade >X%

## Sample Size
- **Needed:** [N per variant]
- **Current traffic:** [N per day]
- **Test duration:** [X days]

## Analysis Plan

### During test:
- [ ] Daily checks for:
  - Conversion rate trends
  - Guardrail metrics
  - Sample ratio mismatch
  
### At test end:
- [ ] Statistical significance test
- [ ] Segment analysis (power users, new users, etc.)
- [ ] Secondary metric check
- [ ] Guardrail metric check

## Decision Criteria
- Ship if: Primary metric +X% at p<0.05, no guardrail degradation
- Iterate if: Directionally positive but not significant
- Kill if: Negative or guardrails degraded

## Timeline
- Launch: [Date]
- Interim check: [Date]
- Final analysis: [Date]
- Decision: [Date]
```

## Template 3: Quarterly Planning Analysis

```markdown
# Q[X] Planning Analysis

## Questions to Answer
1. What should our goals be for Q[X]?
2. Which initiatives should we prioritize?
3. What resources do we need?

## Data to Review
- [ ] Previous quarter performance
- [ ] YoY trends
- [ ] Cohort health
- [ ] Segment performance
- [ ] Competitive landscape
- [ ] Customer feedback themes

## Analysis Approach

### Week 1: Performance Review
- Analyze Q[X-1] vs goals
- Identify what worked/didn't
- Calculate ROI of initiatives

### Week 2: Opportunity Sizing
- Size potential initiatives
- Estimate impact of each
- Rank by expected value

### Week 3: Resource Planning
- Map team capacity
- Identify constraints
- Balance portfolio

### Week 4: Synthesis
- Draft Q[X] goals
- Prioritize initiatives
- Create roadmap
- Present to leadership

## Deliverables
1. Q[X-1] Retrospective deck
2. Q[X] Opportunity analysis
3. Q[X] Goals & roadmap
4. Q[X] Resource plan

## Timeline
- Start: [4 weeks before quarter]
- Draft goals: [2 weeks before quarter]
- Final plan: [1 week before quarter]
```

## Template 4: Feature Post-Launch Analysis

```markdown
# Feature Post-Launch Analysis: [Feature Name]

## Context
- **Launch Date:** [Date]
- **Goal:** [What we hoped to achieve]
- **Success Metric:** [Primary metric]
- **Target:** [Specific target]

## Analysis Questions
1. Did we hit our adoption target?
2. Which segments are adopting?
3. Is the feature driving the intended outcome?
4. What are users saying?
5. What should we do next?

## Analysis Plan

### Week 1: Adoption Analysis
- [ ] Calculate adoption rate vs. target
- [ ] Segment adoption by user type
- [ ] Analyze adoption funnel
- [ ] Identify drop-off points

### Week 2: Impact Analysis
- [ ] Measure impact on success metric
- [ ] Check for unintended consequences
- [ ] Analyze power user behavior
- [ ] Review customer feedback

### Week 3: Insights & Recommendations
- [ ] Synthesize findings
- [ ] Identify opportunities
- [ ] Propose next steps
- [ ] Create presentation

## Deliverables
1. Adoption metrics dashboard
2. Impact analysis summary
3. User feedback synthesis
4. Recommendations deck

## Timeline
- 2 weeks post-launch: Initial metrics review
- 4 weeks post-launch: Full analysis complete
- 6 weeks post-launch: Recommendations implemented
```

## Template 5: Customer Segment Analysis

```markdown
# Customer Segment Analysis: [Segment Name]

## Objective
Understand [segment] behavior to inform product/marketing strategy

## Analysis Questions
1. Who are they? (Demographics, firmographics)
2. What do they do? (Behaviors, usage patterns)
3. How do they perform? (Conversion, retention, LTV)
4. What do they want? (Jobs to be done, pain points)
5. How should we serve them? (Product, pricing, messaging)

## Analysis Plan

### Phase 1: Segment Definition (1 day)
- [ ] Define segment criteria
- [ ] Size the segment
- [ ] Profile demographics
- [ ] Map to customer journey

### Phase 2: Behavioral Analysis (2-3 days)
- [ ] Usage patterns
- [ ] Feature adoption
- [ ] Engagement metrics
- [ ] Retention cohorts

### Phase 3: Performance Analysis (1-2 days)
- [ ] Conversion rates
- [ ] Revenue metrics
- [ ] Lifetime value
- [ ] Churn analysis

### Phase 4: Qualitative Research (2-3 days)
- [ ] Customer interviews
- [ ] Support ticket analysis
- [ ] Survey responses
- [ ] Feature requests

### Phase 5: Synthesis (1-2 days)
- [ ] Create segment persona
- [ ] Document insights
- [ ] Recommend actions
- [ ] Present findings

## Deliverables
1. Segment profile document
2. Behavioral analysis dashboard
3. Persona one-pager
4. Strategic recommendations

## Timeline
Total: 7-10 days
```

## Template 6: Retention Deep Dive

```markdown
# Retention Analysis: [Product/Feature]

## Objective
Understand retention patterns and identify improvement opportunities

## Analysis Questions
1. What is our current retention curve?
2. Which cohorts retain best/worst?
3. What behaviors predict retention?
4. What causes churn?
5. What can we do to improve retention?

## Analysis Plan

### Phase 1: Baseline Metrics (1 day)
- [ ] Calculate D1, D7, D30, D90 retention
- [ ] Create retention cohort table
- [ ] Identify retention benchmarks
- [ ] Track trends over time

### Phase 2: Cohort Analysis (2 days)
- [ ] Compare cohort retention curves
- [ ] Identify best/worst performing cohorts
- [ ] Analyze cohort characteristics
- [ ] Look for early signals

### Phase 3: Behavioral Drivers (2-3 days)
- [ ] Identify "aha moment" behaviors
- [ ] Correlate actions with retention
- [ ] Analyze feature usage patterns
- [ ] Build retention score model

### Phase 4: Churn Analysis (2 days)
- [ ] Interview churned users
- [ ] Analyze churn reasons
- [ ] Review support tickets
- [ ] Identify churn warning signs

### Phase 5: Recommendations (1 day)
- [ ] Prioritize improvement areas
- [ ] Design retention experiments
- [ ] Set improvement goals
- [ ] Create action plan

## Deliverables
1. Retention dashboard
2. Cohort analysis report
3. Behavioral driver analysis
4. Retention playbook
5. Experiment roadmap

## Timeline
Total: 8-10 days
```
