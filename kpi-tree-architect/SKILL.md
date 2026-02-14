---
name: kpi-tree-architect
description: Build comprehensive KPI trees from North Star metrics. Use when users need to decompose metrics into hierarchical driver structures, create MECE (Mutually Exclusive, Collectively Exhaustive) breakdowns, identify leverage points, map performance drivers, or prepare for root cause analysis. Essential for setting up analytical foundations after defining a North Star metric.
---

# KPI Tree Architect

Build hierarchical KPI structures that decompose North Star metrics into actionable drivers using MECE principles.

## Core Principle: MECE Decomposition

**Mutually Exclusive & Collectively Exhaustive**

- **Mutually Exclusive**: No overlapping drivers (no double-counting)
- **Collectively Exhaustive**: No missing drivers (sum of parts = whole)

Visual analogy: Tangram puzzle pieces that don't overlap and cover the entire area.

## Three Decomposition Methods

### 1. Mathematical Decomposition
Use when metric has clear mathematical formula.

**Example**: Upselling Rate = # Customers Buying Higher Tier / Total # Customers
- Decomposes to numerator and denominator
- Common patterns: Rate = Numerator/Denominator, Average = Sum/Count

### 2. Process Decomposition
Use when metric depends on sequential steps (funnels, workflows).

**Example**: # Customers Buying = Visits × Click Rate × Checkout Completion
- Decomposes by funnel stages
- Common patterns: Conversion funnels, customer journeys

### 3. Segmentation Decomposition
Use when metric varies significantly by groups.

**Example**: Total Visits = Organic + Email Campaign + Other Channels
- Decomposes by segments
- Common patterns: Customer types, product categories, regions, channels

## Workflow Choice

**First, always ask the user**: "Would you like me to:
1. **Generate the complete tree at once** (I'll build the full decomposition and present it), or
2. **Build it collaboratively** (we'll work through each level together with your input)?"

Then follow the appropriate workflow below.

## Workflow A: Complete Tree Generation

Use when user chooses option 1.

### Process:
1. Ask clarifying questions about the North Star metric and business context
2. Build the complete tree using MECE principles
3. Present the full tree with validation and insights
4. Discuss and refine based on feedback

### Steps:
1. **Understand North Star**: Ask about metric definition, formula, business context
2. **Choose decomposition methods**: Determine best approach for each level
3. **Build complete structure**: Decompose to 3-5 levels
4. **Validate MECE**: Check each level
5. **Identify influential factors**: Mark qualitative drivers
6. **Present the tree with insights**: Show full tree, validation, key findings

## Workflow B: Collaborative Iterative Building

Use when user chooses option 2. Build the tree level by level with user input.

### Iterative Process:

**For each metric to decompose:**

#### Step 1: Select Metric
Ask: "Which metric would you like to decompose next?"
- Start with North Star metric
- Then move to user-selected drivers from previous level

#### Step 2: Propose Decomposition Method
Based on the metric, propose 2-3 decomposition approaches:

**Template:**
"For [Metric Name], I see [2-3] possible decomposition approaches:

**Option 1: [Method Name]** (e.g., Mathematical)
- Break down as: [Component A] [operator] [Component B]
- Best for: [when to use]
- Example: [simple example]

**Option 2: [Method Name]** (e.g., Process)
- Break down by: [stages/steps]
- Best for: [when to use]
- Example: [simple example]

Which approach makes more sense for your business? Or would you like me to recommend one?"

#### Step 3: Ask Clarifying Questions
Before proposing the decomposition, ask 1-2 questions:
- About the business process or customer journey
- About how the metric is calculated
- About natural segments or stages
- About data availability

#### Step 4: Propose Specific Decomposition
Present the specific breakdown:

"Based on [your answers], here's how I'd break down [Metric]:

[Metric Name]
├─ Component A: [Name and brief definition]
├─ Component B: [Name and brief definition]
└─ Component C: [Name and brief definition]

**MECE Validation:**
- Mutually Exclusive: [Why no overlap]
- Collectively Exhaustive: [Why sum equals whole]

Does this breakdown make sense to you?"

#### Step 5: Validate with User
Ask: "Does this decomposition work for you? Any adjustments needed?"

If user approves → Move to next step
If user wants changes → Refine and re-validate

#### Step 6: Continue or Stop
Ask: "Would you like to decompose any of these components further, or shall we work on a different branch?"

Options:
- **Continue deeper**: Pick a component to decompose next
- **Switch branches**: Move to different part of tree
- **Stop this branch**: Mark current level as final (add influential factors if needed)
- **Complete tree**: Finish and present full tree

**Repeat Steps 1-6** until user is satisfied with tree depth and coverage.

#### Step 7: Finalize Branch
When stopping a branch, ask: "Are there any influential factors (qualitative elements) that affect [metric] but aren't measurable as KPIs?"

Mark these with 🔍 in the tree.

### Tracking Progress
During collaborative building, periodically show the current tree state:
"Here's our tree so far: [show current structure]"

## MECE Validation (Both Workflows)

At each level, validate:

**Mutually Exclusive test**:
- No component overlaps with others
- Each element clearly defined
- Moving one component doesn't necessarily move others

**Collectively Exhaustive test**:
- All components sum to parent metric
- No missing pieces
- Can explain 100% of parent

**Fix immediately** if MECE is violated.

## Common Patterns

### Pattern 1: Funnel/Conversion Flow
```
Conversion Rate
├─ Awareness (# saw opportunity)
├─ Interest (% engaged)
├─ Consideration (% explored)
├─ Intent (% started action)
└─ Purchase (% completed)
```

### Pattern 2: Frequency × Intensity
```
Total Usage
├─ # Active Users
│   ├─ New Users
│   └─ Returning Users
└─ Avg Usage per User
    ├─ Frequency (sessions/user)
    └─ Intensity (actions/session)
```

### Pattern 3: Segmented Contribution
```
Total Metric
├─ Segment A (Size × Performance)
├─ Segment B (Size × Performance)
└─ Segment C (Size × Performance)
```

### Pattern 4: Efficiency Metrics
```
Cost per Outcome
├─ Total Cost (Fixed + Variable)
└─ # Outcomes (Successful + Failed)
```

## Anti-Patterns to Avoid

### ❌ Overlapping Branches (not MECE)
**Bad**: Mobile Users + Desktop Users + New Visitors + Returning Visitors
- Dimensions overlap

**Good**: Choose one dimension per level, then subdivide
- Mobile → New/Returning
- Desktop → New/Returning

### ❌ Unmeasurable Components
**Bad**: "Product Quality", "Customer Happiness" (abstract)

**Good**: Use measurable proxies
- % Rating 4-5 Stars
- Net Promoter Score
- Churn Rate

### ❌ Too Deep or Too Shallow
- **Too shallow**: Not actionable
- **Too deep**: 10+ levels, unusable
- **Right depth**: 3-5 levels focusing on actionable insights

### ❌ Missing Components
Always verify components sum to 100% of parent.

## Output Format

Provide trees in clean format without method labels in the structure:

```
# North Star Metric: [Name]
**Definition**: [What it measures]
**Formula**: [If applicable]
**Current**: [Value] | **Target**: [Value]

## KPI Tree

[Metric Name]
├─ [Component A]
│  ├─ [Sub-component A.1]
│  │  ├─ [Sub-component A.1.a]
│  │  └─ 🔍 [Influential Factor description]
│  └─ [Sub-component A.2]
├─ [Component B]
│  ├─ [Sub-component B.1]
│  └─ [Sub-component B.2]
│     └─ 🔍 [Influential Factor description]
└─ [Component C]

Legend:
├─ = Decomposition branch
└─ = Final component or leaf
🔍 = Influential factor (not a KPI)

## Decomposition Explanation

**Level 1 - [Component A, B, C]:**
- Method: [Mathematical/Process/Segmentation]
- Rationale: [Why this decomposition approach]
- Formula (if applicable): [Metric] = [Component A] + [Component B] + [Component C]

**Level 2 - [Component A breakdown]:**
- Method: [Mathematical/Process/Segmentation]
- Rationale: [Why this decomposition approach]
- Formula (if applicable): [Component A] = [A.1] × [A.2]

[Continue for each level]

## MECE Validation

**Level 1:**
- ✓ Mutually Exclusive: [Explanation]
- ✓ Collectively Exhaustive: [Explanation]
- Formula check: ✓ [Verification]

**Level 2:**
[Repeat for each level]

## Key Insights

1. **Primary leverage point**: [Which driver has most impact and why]
2. **Quick wins**: [Which drivers easiest to improve]
3. **Data gaps**: [What's not currently measured]
4. **Strategic implications**: [What this reveals about the business]
```
Print the tree in a .md file when user is staisfied or stop the exploration

**For collaborative building**, show incremental progress:
```
## Current Tree State

[Metric Name]
├─ [Component A] ← Currently exploring this branch
│  ├─ [Sub-component A.1]
│  └─ [Sub-component A.2] (to be decomposed)
├─ [Component B] (to be decomposed)
└─ [Component C] (to be decomposed)
```

## Validation Checklist

Before finalizing:

**Structural**:
- [ ] Every level is MECE
- [ ] No more than 5 levels deep
- [ ] Each level has 2-7 branches
- [ ] Mathematical formulas correct
- [ ] All components measurable or influenceable

**Practical**:
- [ ] Team can understand the structure
- [ ] Can explain any branch in <2 minutes
- [ ] Identifies actual leverage points
- [ ] Each KPI can be tracked/reported

## Examples

See `references/examples.md` for detailed examples including:
- SaaS Upselling (mathematical + process decomposition)
- E-commerce Delivery Time (process decomposition)
- Content Platform Engagement (mathematical + segmentation)

## Next Steps

After building the tree:
1. Validate with data (do measured components sum to parent?)
2. Identify tracking gaps
3. Map tree to dashboard structure
4. Set baselines and targets
5. Use for root cause analysis

## Reference Material

For comprehensive examples, advanced techniques, and detailed guidance, see:
- `references/examples.md` - Complete worked examples
- `references/advanced-techniques.md` - Multiple trees, time-based, ratio decomposition
- `references/templates.md` - Reusable output templates
