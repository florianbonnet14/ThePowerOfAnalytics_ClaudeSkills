---
name: analysis-planner
description: Structure analysis investigations before diving into data, preventing wasted time and ensuring thoroughness. Use when users need to plan any significant analysis, investigate KPI changes, respond to stakeholder questions, plan feature/experiment analysis, or when previous analyses were unfocused. Helps define clear goals, generate testable hypotheses, create systematic analysis roadmaps, identify required data, estimate timelines, and prevent analysis paralysis.
---

# Analysis Planner

Structure investigations before diving into data to prevent wasted time, ensure thoroughness, and deliver actionable insights.

## Core Planning Framework

### Phase 1: Define the Question

Start with: "What decision needs to be made?"

**Quality checklist:**
- [ ] Specific (not vague)
- [ ] Answerable with available data
- [ ] Tied to a decision or action
- [ ] Has clear success criteria
- [ ] Time-bounded

**Good vs Bad:**
- ✓ "Should we prioritize mobile app performance or new features next quarter?"
- ✓ "Which customer segment should we focus retention efforts on?"
- ✗ "Tell me about our users" (too broad)
- ✗ "Find something interesting" (no direction)

### Phase 2: Define Success Criteria

Ask: "What would a good answer look like?"

**Template:**
```
A successful analysis will:
1. [Specific outcome]
2. [Specific outcome]

We'll know we're done when:
- [Criterion]
- [Criterion]

The answer will enable us to:
- [Decision/action that will be taken]
```

### Phase 3: Generate Hypotheses

**Process:**
1. List potential drivers from KPI Tree
2. Add business context (recent changes, events)
3. Combine into testable hypotheses

**Hypothesis quality criteria:**
- [ ] Testable with available data
- [ ] Specific (not "something changed")
- [ ] Has clear validation method
- [ ] Mutually exclusive from others
- [ ] Collectively exhaustive

**Prioritize by:**
1. **Probability:** How likely?
2. **Impact:** How much does it explain?
3. **Actionability:** Can we do something about it?

### Phase 4: Design Analysis Approach

For each hypothesis, provide detailed analysis steps in descriptive language (NOT SQL):

**For each hypothesis:**
1. **Data to Collect** - Describe in words what data points are needed (e.g., "number of sign-ups by day, with their marketing channel, time from sign-up to first action")
2. **How to Analyze** - Detail the visualization approach:
   - Type of chart/table (line chart, bar chart, histogram, table, etc.)
   - What data goes on which axis
   - What lines/bars/segments to plot
   - Any comparisons to show (before/after, segment A vs B)
3. **What to Look For** - Describe the patterns that would validate or invalidate the hypothesis:
   - Changes in trend lines
   - Differences in values between segments
   - Timing of changes
   - Magnitude of differences
4. **Proposed Deep-Dives** - Suggest follow-up analyses if hypothesis is validated

**Critical:** Never include SQL queries or code. Always describe analysis in plain language that any analyst can translate to their own tools.

### Phase 5: Structure Output

Organize the analysis plan with:
- Executive Summary (problem, question, decision, timeline)
- Success Criteria (what done looks like)
- Context (metric definition, KPI tree, recent changes)
- Hypotheses (prioritized tiers with scores)
- Analysis Approach for each hypothesis

**Do NOT include:**
- Analysis Roadmap & Timeline section
- Data Requirements section with SQL
- Roles & Responsibilities section
- Technical implementation details

## Analysis Types

### Type 1: Root Cause Investigation
**When:** KPI changed, need to know why
**Timeline:** 1-3 days
**Key techniques:** KPI tree navigation, segmentation, timeline correlation
**Agents needed:** 🔍 Root Cause Investigator, 👥 Segmentation Expert (to identify which customer groups drove the change)

**When to use Segmentation Expert:**
- KPI changed but don't know which customers drove it
- Need to understand "who" behind the "what"
- Investigating whether it's a mix effect or performance effect

### Type 2: Opportunity Sizing
**When:** Evaluating potential initiative
**Timeline:** 2-5 days
**Key techniques:** Market sizing, segment analysis, conversion math
**Agents needed:** 👥 Segmentation Expert (to identify target segments and their potential), 📊 Chart Advisor

**When to use Segmentation Expert:**
- Sizing opportunity by customer segment
- Understanding which segments would benefit most
- Estimating addressable market by segment

### Type 3: Segment Deep Dive
**When:** Understanding specific customer group
**Timeline:** 3-7 days
**Key techniques:** Behavioral analysis, cohort tracking, feedback synthesis
**Agents needed:** 👥 Segmentation Expert (primary), 📅 Cohort Analyst (to see how segment evolves), 💬 Feedback Synthesizer

**When to use both Segmentation and Cohort Analysis:**
- Understanding how different segments perform over time
- Comparing retention across customer segments
- Identifying which segments have best/worst long-term value

### Type 4: Feature Performance Review
**When:** Evaluate feature success
**Timeline:** 2-4 days
**Key techniques:** Adoption funnel, user feedback, cohort comparison
**Agents needed:** 📅 Cohort Analyst (to compare cohorts pre/post launch), 🔬 Influential Factors Detective

**When to use Cohort Analysis Specialist:**
- Comparing user cohorts before and after feature launch
- Tracking feature adoption over time by cohort
- Understanding if newer users adopt feature faster

### Type 5: Experiment Analysis
**When:** Evaluate A/B test
**Timeline:** 1-2 days
**Key techniques:** Statistical testing, segment analysis, guardrail checks
**Agents needed:** 🧪 A/B Testing Advisor, 👥 Segmentation Expert (to understand if effect varies by segment)

**When to use Segmentation Expert:**
- Checking if experiment effect consistent across segments
- Identifying which segments benefit most from change
- Understanding heterogeneous treatment effects

### Type 6: Retention Analysis
**When:** Understanding why customers stay or leave
**Timeline:** 3-5 days
**Key techniques:** Cohort retention tables, segment comparison, leading indicators
**Agents needed:** 📅 Cohort Analysis Specialist (primary), 👥 Segmentation Expert (to compare segments)

**When to use Cohort Analysis Specialist:**
- Measuring retention rates over time
- Comparing new vs old user behavior
- Identifying early warning signals in recent cohorts
- Calculating lifetime value by cohort
- Understanding maturation patterns

## Analysis Approach Format

For each hypothesis, provide a detailed, step-by-step analysis plan using this structure:

### Example: H1 - Setup Completion Dropped

**Data to Collect:**
- Number of sign-ups per week for the last 8 weeks
- Number of users who completed each step of setup (name entry, company entry, job entry, goal selection)
- Time spent at each setup step
- Drop-off points (which step users abandoned)
- Segmented by: acquisition channel, device type (desktop/mobile), geography

**How to Analyze:**

*Analysis 1: Setup Funnel Trends*
- **Chart type:** Multi-line chart
- **X-axis:** Week (last 8 weeks)
- **Y-axis:** Completion rate (%)
- **Lines to plot:** 
  - Overall setup completion rate
  - Completion rate for each individual step (name, company, job, goal)
- **Comparison:** Overlay a reference line showing the average from 2 months ago

*Analysis 2: Step-by-Step Micro-Funnel*
- **Chart type:** Table with color-coded cells
- **Rows:** Each week
- **Columns:** Each setup step with completion percentage
- **Color coding:** Green for improvements, red for declines >5pp

*Analysis 3: Segment Comparison*
- **Chart type:** Grouped bar chart
- **X-axis:** Segments (acquisition channels, device types)
- **Y-axis:** Setup completion rate (%)
- **Bars:** Two bars per segment (previous month average vs last month)
- **Highlight:** Segments with largest drops

**What to Look For:**

*To VALIDATE this hypothesis:*
- Setup completion rate decreased by 5+ percentage points in last month
- The decrease is visible in one specific step (not distributed equally)
- The timing of the decrease correlates with a product change
- Multiple segments show the decrease (not just one channel or device)

*To INVALIDATE this hypothesis:*
- Setup completion rate remained stable or increased
- The decrease is <2 percentage points (within normal variance)
- Only one specific segment affected (suggests mix effect, not product issue)
- The decline started before any product changes

**Proposed Deep-Dives:**

*If hypothesis is validated:*
1. **Specific Step Analysis:** Deep-dive into the exact step showing drop-off
   - Time distribution at that step (did users spend more time?)
   - Error logs or failed attempts at that step
   - Session recordings of users abandoning at that step
   
2. **A/B Test Analysis:** If there was a recent change
   - Compare users who saw old version vs new version
   - Measure the exact impact of the change
   
3. **Device-Specific Investigation:** If mobile shows bigger drop
   - Mobile UI issues or bugs
   - Screen size rendering problems
   - Touch interaction issues

### Type 6: Retention Analysis
**When:** Understanding why customers stay or leave
**Timeline:** 3-5 days
**Key techniques:** Cohort retention tables, segment comparison, leading indicators
**Agents needed:** 📅 Cohort Analysis Specialist (primary), 👥 Segmentation Expert (to compare segments)

**When to use Cohort Analysis Specialist:**
- Measuring retention rates over time
- Comparing new vs old user behavior
- Identifying early warning signals in recent cohorts
- Calculating lifetime value by cohort
- Understanding maturation patterns

## Combining Segmentation & Cohort Analysis

Many of the most powerful analyses use BOTH segmentation and cohort analysis together:

### Pattern 1: Segment-Specific Cohort Analysis
**Question:** "Do enterprise customers retain better than SMBs over time?"

**Approach:**
1. Use 👥 Segmentation Expert to define segment rules (Enterprise: >500 employees, SMB: <500)
2. Use 📅 Cohort Analysis Specialist to build retention table for each segment separately
3. Compare retention curves between segments

**Data to Collect:**
- Cohort (signup month) for all users
- Company size for each user
- Activity data for retention calculation

**How to Analyze:**
- Create two retention tables: one for Enterprise, one for SMB
- Plot retention curves on same chart (different colored lines)
- Compare M1, M3, M6 retention rates between segments

**What to Look For:**
- Does one segment consistently retain better?
- Do gaps widen or narrow over time?
- Are recent cohorts improving in both segments?

### Pattern 2: Cohort-Specific Segmentation
**Question:** "Has the mix of customer segments changed over time?"

**Approach:**
1. Use 📅 Cohort Analysis Specialist to define cohorts (monthly)
2. Use 👥 Segmentation Expert to analyze segment distribution within each cohort
3. Track how segment mix evolves across cohorts

**Data to Collect:**
- Cohort for all users
- Segment classification for all users
- Size of each segment within each cohort

**How to Analyze:**
- Create stacked bar chart with cohorts on X-axis
- Stack shows % of each segment within cohort
- Track how segment composition changes

**What to Look For:**
- Is one segment growing as % of new signups?
- Does segment mix correlate with overall metric changes?
- Are certain channels bringing different segment mixes?

### Pattern 3: Explaining Overall KPI Changes
**Question:** "Our retention dropped 10pp - is it because of segment mix or performance?"

**Approach:**
1. Use 📅 Cohort Analysis Specialist to confirm retention drop in recent cohorts
2. Use 👥 Segmentation Expert to check if segment mix changed
3. Use 🎯 Mix Effect Analyzer to quantify mix vs performance contribution

**Analysis Steps:**
1. Build retention table to confirm drop
2. Check segment distribution: Did low-retention segments grow?
3. Check within-segment retention: Did retention drop within segments too?
4. Calculate: Mix effect + Performance effect = Total effect

**Possible Outcomes:**
- **Pure mix effect:** Segment performance stable, but more low-retention segments
- **Pure performance effect:** Segment mix stable, but all segments performing worse
- **Combined effect:** Both mix shifted AND performance declined

### Pattern 4: Predictive Segmentation from Cohort Behavior
**Question:** "Which early behaviors predict long-term retention?"

**Approach:**
1. Use 📅 Cohort Analysis Specialist to identify mature cohorts with good retention
2. Look back at their Week 1 behavior patterns
3. Use 👥 Segmentation Expert to create behavioral segments (e.g., "High Engagers")
4. Apply to new cohorts for early prediction

**Data to Collect:**
- Mature cohorts (6+ months old) with retention outcomes
- Week 1 behavior for all users in those cohorts
- Same behavior data for recent cohorts

**How to Analyze:**
- For retained users in mature cohorts, identify common Week 1 behaviors
- Create behavioral segments based on these patterns
- Track % of new cohorts falling into "high retention" behavioral segments
- Predict their likely long-term retention

**What to Look For:**
- Strong correlations between early behavior and retention (e.g., 3+ sessions in Week 1 → 75% M6 retention)
- Behavioral segments that are predictive and actionable
- Early warning when new cohorts show worse early behavior patterns

## Common Mistakes & Fixes

### Mistake 1: No Hypotheses Upfront
**Problem:** Jump straight to data, get lost
**Fix:** List 3-5 hypotheses before touching data. Use KPI Tree + recent events.

### Mistake 2: Trying to Answer Everything
**Problem:** Analysis paralysis, never finishes
**Fix:** Prioritize top 3 hypotheses. Focus on 80/20. Set time limits per phase.

### Mistake 3: No Decision Criteria Upfront
**Problem:** Analysis complete but "Is this good enough?"
**Fix:** Define minimum improvement threshold upfront. Define decision criteria. Identify decision maker.

### Mistake 4: Not Involving Right People
**Problem:** Wasted effort, no trust
**Fix:** Involve engineer (validate data), PM (business context), stakeholders (alignment) early.

### Mistake 5: Over-Scoping Timeline
**Problem:** Silence for weeks, stakeholder frustration
**Fix:** Break into phases with checkpoints. Share interim findings. Set realistic timelines (2x initial estimate).

## Time-Boxing Strategies

### The 80/20 Rule
Total 10 hours budget:
- Phase 1 (2h): Quick exploration → 80% of answer
- Phase 2 (4h): Deep dive → 95% of answer
- Phase 3 (2h): Validation → 100% confidence
- Phase 4 (2h): Presentation prep

### Progressive Elaboration
- Hour 1: Look at everything (dashboard scan)
- Hour 2: Focus on what's interesting
- Hour 3: Go deep on root cause
- Hour 4: Document findings

### Check-in Cadence
**Daily:** 15-min standup (learned, analyzing today, blockers)
**Every 2-3 days:** Stakeholder checkpoint (interim findings, feedback, adjust)

## Quality Checklist

**Before starting:**
- [ ] Clear question defined
- [ ] Success criteria established
- [ ] Hypotheses prioritized (top 3-5)
- [ ] Data sources identified and accessible
- [ ] Timeline estimated and communicated
- [ ] Stakeholders aligned on plan
- [ ] Resources allocated

**During analysis:**
- [ ] Checking hypotheses in priority order
- [ ] Documenting findings as you go
- [ ] Checkpointing with stakeholders
- [ ] Staying on timeline (or updating it)
- [ ] Avoiding scope creep

**Before sharing results:**
- [ ] Question fully answered
- [ ] Recommendations clear and actionable
- [ ] Supporting data is solid
- [ ] Alternative explanations considered
- [ ] "So What?" is obvious
- [ ] Ready for tough questions

## Related Agents & Skills

**Use before starting:**
- 🌳 KPI Tree Architect - Framework for hypotheses
- 📍 North Star Metric Advisor - Ensure analysis ties to strategy

**Use during:**
- 🔍 Root Cause Investigator - Execute investigation
- 👥 **Segmentation Expert** - Analyze performance differences across customer segments, identify which segments drove changes
- 📅 **Cohort Analysis Specialist** - Track behavior over time, compare user vintages, measure retention
- 🎯 Mix Effect Analyzer - Separate mix vs performance
- 🔬 Influential Factors Detective - Qualitative factors
- 💬 Customer Feedback Synthesizer - Customer voice

**Use after:**
- 📊 Chart & Visualization Advisor - Create compelling visuals
- 📝 Executive Summary Writer - Document findings
- 🎬 Presentation Architect - Share results

## Key Principles

From "The Power of Analytics" book:
- "Running an analysis by jumping into the data is not the right approach and is doomed for failure"
- "Take the time to list down your hypotheses before collecting data"
- "Use your KPI tree to zero in on the most probable area where to dig"
- "Come up with a list of 3 to 5 main hypotheses about the drivers worth exploring"

## Success Metrics

Planning is effective when:
- ✅ Analyses finish on time
- ✅ Findings are actionable
- ✅ Stakeholders don't say "but did you check..."
- ✅ No analysis paralysis
- ✅ High confidence in results
- ✅ Team can plan analyses independently
- ✅ Minimal do-overs or scope changes

## Additional Resources

See references/roadmap_template.md for complete analysis roadmap template
See references/analysis_templates.md for templates by analysis type
