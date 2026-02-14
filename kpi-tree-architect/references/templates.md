# KPI Tree Output Templates

Reusable templates for documenting KPI trees using the clean format (no method labels in tree structure).

## Template 1: Standard Complete Tree

Use for most KPI trees. Provides clear structure with separate decomposition explanation.

```markdown
# North Star Metric: [Metric Name]
**Definition**: [Clear definition of what this metric measures]
**Formula**: [Mathematical formula if applicable]
**Current**: [Current value] | **Target**: [Target value]
**Measurement Frequency**: [Daily/Weekly/Monthly]

## KPI Tree

[Metric Name]
├─ [Component A]
│  ├─ [Sub-component A.1]
│  │  ├─ [Sub-component A.1.a]
│  │  └─ 🔍 [Influential factor description]
│  └─ [Sub-component A.2]
│     └─ 🔍 [Influential factor description]
├─ [Component B]
│  ├─ [Sub-component B.1]
│  └─ [Sub-component B.2]
└─ [Component C]
   └─ 🔍 [Influential factor description]

Legend:
├─ = Decomposition branch
└─ = Final component or leaf
🔍 = Influential factor (not a KPI)

## Decomposition Explanation

**Level 1 - [Component A, B, C]:**
- Method: [Mathematical/Process/Segmentation]
- Rationale: [Why this decomposition approach was chosen]
- Formula: [Metric] = [Component A] [operator] [Component B] [operator] [Component C]
- Example: Revenue = # Customers × Average Order Value

**Level 2 - [Component A breakdown]:**
- Method: [Mathematical/Process/Segmentation]
- Rationale: [Why this approach for this component]
- Formula: [Component A] = [Sub A.1] [operator] [Sub A.2]
- Example: # Customers = New Customers + Returning Customers

**Level 2 - [Component B breakdown]:**
- Method: [Mathematical/Process/Segmentation]
- Rationale: [Why this approach]
- Formula: [If applicable]

[Continue for each level and branch]

## MECE Validation

**Level 1:**
- ✓ Mutually Exclusive: [Explain why components don't overlap]
- ✓ Collectively Exhaustive: [Explain why components cover everything]
- ✓ Formula check: [Verification that math works]

**Level 2 - Component A:**
- ✓ Mutually Exclusive: [Explanation]
- ✓ Collectively Exhaustive: [Explanation]
- ✓ Formula check: [Verification]

**Level 2 - Component B:**
[Same validation structure]

[Continue for each level]

## Measurement Requirements

### Currently Tracked:
- ✓ [Metric Name]: [Data source, update frequency, owner]
- ✓ [Metric Name]: [Data source, update frequency, owner]

### Needs Implementation:
- [ ] [Metric Name]: [What needs to be built, estimated effort, priority]
- [ ] [Metric Name]: [What needs to be built, estimated effort, priority]

### Data Quality Notes:
- [Any caveats about current data]
- [Known gaps or limitations]

## Dashboard Mapping

**Dashboard 1: [Dashboard Name]**
- Covers: [Which KPIs from tree - list specific components]
- Audience: [Who uses this dashboard]
- Update frequency: [Real-time/Hourly/Daily/Weekly]
- Link: [URL if applicable]

**Dashboard 2: [Dashboard Name]**
- Covers: [Which KPIs from tree]
- Audience: [Who uses this dashboard]
- Update frequency: [Real-time/Hourly/Daily/Weekly]
- Link: [URL if applicable]

## Key Insights

1. **Primary leverage point**: [Which driver has most impact and why]
2. **Quick wins**: [Which drivers are easiest to improve with significant impact]
3. **Data gaps**: [What's not currently measured that should be]
4. **Strategic implications**: [What this tree reveals about the business]
5. **Bottlenecks identified**: [Any constraints or limiting factors]

## Next Steps

1. [ ] [Specific action with owner and deadline]
2. [ ] [Specific action with owner and deadline]
3. [ ] [Specific action with owner and deadline]
4. [ ] [Specific action with owner and deadline]

## Version History
- [Date]: [Changes made]
- [Date]: Initial tree created
```

## Template 2: Collaborative Progress View

Use during collaborative building to show current state.

```markdown
# KPI Tree: [Metric Name] (In Progress)
**Status**: Building collaboratively
**Last Updated**: [Date]

## Current Tree State

[North Star Metric]
├─ [Component A] ✓ Fully decomposed
│  ├─ [Sub-component A.1]
│  │  ├─ [Sub A.1.a]
│  │  └─ 🔍 [Influential factors]
│  └─ [Sub-component A.2]
│     └─ 🔍 [Influential factors]
├─ [Component B] ← Currently working on this
│  └─ (To be decomposed)
└─ [Component C] (To be decomposed)

## Components Completed
- ✓ Component A - Fully decomposed to Level 3
- ⏳ Component B - Selected for decomposition
- ⏹ Component C - Not started

## Next Session Focus
- [ ] Decompose Component B
- [ ] Review Component B decomposition
- [ ] Decide on Component C approach

## Decisions Made So Far

**Component A decomposition:**
- Method: [Process]
- Rationale: [Sequential funnel made sense]
- Validated: [Date]

## Questions to Address
1. [Question about business process]
2. [Question about data availability]
```

## Template 3: Executive Summary Tree

Use for senior leadership presentations. High-level with key insights first.

```markdown
# Executive Summary: [North Star Metric]

## Performance Overview

**Metric**: [Name]
**Current**: [Value] | **Target**: [Value] | **Trend**: [↑/→/↓]
**Status**: [On track / At risk / Behind]

**One-line summary**: [Current state and primary finding]

## Critical Insights

### 🎯 Primary Driver: [Component Name]
- **Impact**: [X% of total metric, or why this matters most]
- **Current Status**: [Performing well / At risk / Underperforming]
- **Action**: [What we're doing about it]
- **Owner**: [Team/Person]

### ⚠️ Area of Concern: [Component Name]
- **Issue**: [What's wrong in one sentence]
- **Business Impact**: [Revenue/user/operational impact]
- **Root Cause**: [Brief explanation]
- **Mitigation Plan**: [Action being taken]
- **Owner**: [Team/Person]

### ✨ Opportunity: [Component Name]
- **Finding**: [What we discovered]
- **Potential**: [Quantified upside if addressed]
- **Recommendation**: [Specific action recommended]
- **Effort Required**: [Low/Medium/High]

## Simplified Tree View

```
[North Star: Value]
│
├─ Primary Driver (70% impact) - [Status: ✓/⚠/✗]
│  └─ Key insight: [One line]
│
├─ Secondary Driver (20% impact) - [Status: ✓/⚠/✗]
│  └─ Key insight: [One line]
│
└─ Tertiary Driver (10% impact) - [Status: ✓/⚠/✗]
   └─ Key insight: [One line]
```

## Strategic Implications

1. **[Implication Title]**: [Description and what it means for strategy]
2. **[Implication Title]**: [Description and what it means for strategy]
3. **[Implication Title]**: [Description and what it means for strategy]

## Decisions Required

| Decision | Options | Recommendation | Expected Impact | Deadline |
|----------|---------|----------------|-----------------|----------|
| [Topic] | [A / B / C] | [Choice] - [Why] | [Quantified] | [Date] |
| [Topic] | [A / B / C] | [Choice] - [Why] | [Quantified] | [Date] |

## Resource Requirements

**To achieve target:**
- Budget: [$X] for [specific purpose]
- Headcount: [#] [roles] for [specific purpose]
- Timeline: [Duration] to [achieve what specifically]
- Dependencies: [What needs to happen first]
```

## Template 4: Operational Team Tree

Use for day-to-day operational management. Focus on ownership and actions.

```markdown
# Operational KPI Tree: [North Star Metric]

## North Star: [Metric Name]
- **Owner**: [Team/Person]
- **Current**: [Value] | **Target**: [Value] | **Status**: [On/At risk/Behind]
- **Review Frequency**: [Daily/Weekly]
- **Dashboard**: [Link]

## Tree with Ownership

[North Star Metric]
├─ [Component A] - Owner: [Team]
│  ├─ [Sub-component A.1] - Owner: [Person]
│  │  └─ 🔍 [Influential factors] - Experiments: [Link]
│  └─ [Sub-component A.2] - Owner: [Person]
│     └─ Current: [Value] | Target: [Value]
├─ [Component B] - Owner: [Team]
│  ├─ [Sub-component B.1] - Owner: [Person]
│  └─ [Sub-component B.2] - Owner: [Person]
│     └─ Status: ⚠️ Behind target, action needed
└─ [Component C] - Owner: [Team]

## Component Details

### Component A: [Name]
- **Owner**: [Team/Person]
- **Current**: [Value]
- **Target**: [Value]
- **Status**: [On/At risk/Behind]
- **Tracking**: [Dashboard link, update frequency]
- **Actions in Progress**:
  - [ ] [Action] - Owner: [Person] - Due: [Date] - Status: [In progress/Blocked]
  - [ ] [Action] - Owner: [Person] - Due: [Date] - Status: [In progress/Blocked]
- **Blockers**: [Any impediments]
- **Last Reviewed**: [Date]

### Component B: [Name]
[Same structure]

## Influential Factors Status

### Factor: [Name]
- **Influences**: [Which KPIs]
- **Owner**: [Team/Person]
- **Current State**: [Description]
- **Experiments Running**:
  - [Experiment name] - [Status] - [Results summary]
- **Next Tests Planned**:
  - [Test description] - [Expected impact] - [Launch date]

## Weekly Review Checklist

**Review Date**: [Every Monday 10am]
**Participants**: [List]

- [ ] North Star: On track vs target?
- [ ] Component A: Review status and actions
- [ ] Component B: Review status and actions
- [ ] Component C: Review status and actions
- [ ] Blockers: Any new blockers?
- [ ] Escalations: What needs leadership attention?
- [ ] Next Week: Top 3 priorities

## Escalation Triggers

| Situation | Threshold | Escalate To | Action |
|-----------|-----------|-------------|--------|
| North Star off track | >10% below target for 2 weeks | [VP] | Emergency strategy review |
| Component stalled | No movement for 2 weeks | [Director] | Blocker removal |
| Data quality issue | Measurement suspected incorrect | [Data Team] | Urgent audit |
| Ownership gap | Component unowned >1 week | [Manager] | Assign owner immediately |
```

## Template 5: Formula-Focused Technical Tree

Use when mathematical relationships are central. Good for data/analytics teams.

```markdown
# Mathematical KPI Tree: [North Star Metric]

## Level 0: North Star Definition

```
[North Star] = f([Driver A], [Driver B], [Driver C])
```

**Specific Formula**:
```
[Metric Name] = [Component A] [operator] [Component B] [operator] [Component C]
Example: Revenue = # Orders × Average Order Value
```

**Current Calculation**:
```
[Metric] = [Actual values plugged in]
Example: Revenue = 10,000 orders × $75 AOV = $750,000
```

## Tree with Formulas

[North Star Metric]
├─ [Component A] = [Formula]
│  ├─ [Sub A.1] = [Formula]
│  │  ├─ [Sub A.1.a] = [Elementary metric]
│  │  └─ [Sub A.1.b] = [Elementary metric]
│  └─ [Sub A.2] = [Elementary metric]
├─ [Component B] = [Formula]
│  └─ [Sub B.1] = [Elementary metric]
└─ [Component C] = [Elementary metric]

## Detailed Formulas by Level

### Level 1 Formulas

**Component A**: [Name]
```
[Component A] = [Sub A.1] + [Sub A.2] + [Sub A.3]
Current: [X] + [Y] + [Z] = [Total]
```

**Component B**: [Name]
```
[Component B] = [Sub B.1] / [Sub B.2]
Current: [X] / [Y] = [Ratio]
```

**Component C**: [Name]
```
[Component C] = Constant value = [X]
```

### Level 2 Formulas

**Sub-component A.1**: [Name]
```
[Sub A.1] = [Sub A.1.a] × [Sub A.1.b]
Current: [X] × [Y] = [Product]
```

**Sub-component A.2**: [Name]
```
[Sub A.2] = Elementary metric (no further breakdown)
Current: [Value]
```

[Continue for all components]

## Formula Validation

### Rollup Verification
```
Calculated North Star = [Show full calculation with all values]
Measured North Star = [Actual measured value]
Match: [✓ / ✗]
Variance: [If any, percentage and explanation]
```

### Data Source Mapping
| Metric | Formula | Data Source | Update Frequency | Owner |
|--------|---------|-------------|------------------|-------|
| [Metric] | [Formula] | [Database.table.field] | [Real-time/Daily] | [Team] |
| [Metric] | [Formula] | [Database.table.field] | [Real-time/Daily] | [Team] |

### Sensitivity Analysis

**Formula**: 
```
∂[North Star]/∂[Component] = [Mathematical sensitivity]
```

**Practical Impact**:
| Component | Current | +10% Change | Impact on North Star | Rank |
|-----------|---------|-------------|----------------------|------|
| [A] | [X] | [X × 1.1] | [Y%] | #1 (Highest) |
| [B] | [X] | [X × 1.1] | [Y%] | #2 |
| [C] | [X] | [X × 1.1] | [Y%] | #3 (Lowest) |

**Interpretation**: Focus optimization efforts on [Component A] for maximum ROI.

## Mathematical Properties

### Additivity
```
Components that add: [Component A] + [Component B] = [Total]
Property: Can improve components independently
```

### Multiplicativity
```
Components that multiply: [Component A] × [Component B] = [Total]
Property: Bottleneck effect - weakest component limits total
```

### Ratios
```
Efficiency ratios: [Output] / [Input] = [Efficiency]
Property: Can improve by increasing output OR decreasing input
```

## SQL Queries for Calculation

```sql
-- North Star Metric
SELECT 
    [calculation]
FROM [tables]
WHERE [conditions]
GROUP BY [dimensions];

-- Component A
SELECT 
    [calculation]
FROM [tables]
WHERE [conditions];

-- Component B
[Continue for each component]
```
```

## Template Selection Guide

| Use Case | Best Template | Why |
|----------|---------------|-----|
| Initial documentation | Standard Complete | Comprehensive structure |
| Building with stakeholders | Collaborative Progress | Shows work in progress |
| Executive presentation | Executive Summary | High-level strategic focus |
| Day-to-day operations | Operational Team | Ownership and action-oriented |
| Technical/data team | Formula-Focused Technical | Mathematical rigor |

## Template Customization Tips

1. **Mix templates**: Combine sections from different templates as needed
2. **Adjust depth**: Show only relevant levels for your audience
3. **Add visuals**: Include charts for trends, comparisons
4. **Keep updated**: Treat as living document, not one-time artifact
5. **Link resources**: Connect to dashboards, documentation, tools

## Common Template Additions

Consider adding to any template:
- **Glossary**: Define domain-specific terms
- **Assumptions**: Document calculation assumptions
- **Historical trends**: Show how metrics evolved
- **Benchmarks**: Include industry comparisons
- **Related trees**: Link to alternative decompositions
- **Change log**: Track tree evolution over time
