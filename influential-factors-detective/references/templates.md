# Documentation Templates

## Factor Documentation Template

Use this template to document each influential factor identified:

```markdown
# Influential Factor: [Name]

## Definition
[Clear description of what this factor is]

## Location in KPI Tree
**Parent KPI:** [Which KPI this affects]
**Position:** Leaf node of KPI tree

## Current State
[Description of current implementation]

## Hypothesis
We believe that [changing this factor in this way]
will [impact this metric by this much]
because [rationale]

## Tested Variations

| Variation | Description | Test Date | Result | Impact |
|-----------|-------------|-----------|--------|--------|
| Control | [Current implementation] | - | Baseline | - |
| Variant A | [Description] | [Date] | [Win/Loss/Neutral] | [+X%] |
| Variant B | [Description] | [Date] | [Win/Loss/Neutral] | [+X%] |

## Winning Variation
[Which performed best and by how much]

## Key Learnings
- [Key insight 1]
- [Key insight 2]
- [Recommendation for future]

## Related Factors
[Other factors that interact with this one]

## Next Tests
[Follow-up variations to test]
```

---

## Factor Testing Log Template

Track all tests in one central log:

```markdown
# Influential Factor Testing Log

## Active Tests

| Factor | KPI Impact | Start Date | Est. End | Owner | Status |
|--------|------------|------------|----------|-------|--------|
| [Name] | [KPI] | [Date] | [Date] | [Person] | Running |
| [Name] | [KPI] | [Date] | [Date] | [Person] | Analysis |

## Completed Tests - Last Quarter

| Factor | Result | Impact | Date | Status |
|--------|--------|--------|------|--------|
| Hero image | Win | +12% CTR | Sep 15 | Implemented |
| Form length | Win | +8% completion | Sep 1 | Implemented |
| Email timing | Neutral | 0% | Aug 20 | No change |
| CTA color | Loss | -3% CTR | Aug 10 | Reverted |

## Planned Tests - Next Quarter

| Factor | Priority | Hypothesis | Est. Impact | Quarter |
|--------|----------|------------|-------------|---------|
| Onboarding flow | High | Reduce steps → +15% activation | High | Q1 |
| Pricing layout | Medium | Clearer comparison → +10% conversion | Medium | Q1 |
| Feature naming | Low | Better names → +5% adoption | Low | Q2 |

## Test Velocity Metrics

**Current Quarter:**
- Tests launched: [#]
- Tests completed: [#]
- Win rate: [%]
- Average test duration: [days]
- Avg improvement (winners): [%]

**Goals:**
- Target tests per month: 2-4
- Target win rate: >40%
- Target avg duration: <21 days

## Learnings Repository
[Link to detailed test results and insights]
```

---

## Test Brief Template

Plan each test thoroughly before launching:

```markdown
# Test Brief: [Factor Name]

## Context
**Date Created:** [Date]
**Owner:** [Person]
**Business Context:** [Why this test matters now]

## Factor Details
**Category:** [Copy/Design/UX/Timing/Content/Placement]
**Parent KPI:** [Which metric this affects]
**Current State:** [How it currently works]

## Hypothesis
**What we're changing:** [Specific change]
**Expected impact:** [Direction and magnitude]
**Rationale:** [Why we think this will work]

**Confidence Level:** [Low/Medium/High]
**Impact Estimate:** [1-5 scale]
**Effort Estimate:** [1-5 scale]

## Test Design

**Method:** [A/B / Sequential / Multivariate / Qualitative]

**Variations:**
- **Control:** [Current implementation]
- **Variant A:** [First alternative]
- **Variant B:** [Second alternative - if applicable]

**Success Metrics:**
- **Primary:** [Main KPI to measure]
- **Secondary:** [Additional metrics]
- **Guardrails:** [Metrics that shouldn't degrade]

## Implementation Plan

**Technical Requirements:**
- [ ] [Requirement 1]
- [ ] [Requirement 2]

**Tracking Setup:**
- [ ] Events instrumented
- [ ] Dashboard created
- [ ] Alerts configured

**QA Checklist:**
- [ ] All variations display correctly
- [ ] Tracking fires properly
- [ ] Mobile responsive
- [ ] Cross-browser tested

## Sample Size & Duration

**Traffic Available:** [visits/day or emails/week]
**Minimum Detectable Effect:** [% change]
**Required Sample Size:** [# per variant]
**Expected Duration:** [days/weeks]
**Statistical Significance:** [typically 95%]

## Analysis Plan

**When to check results:**
- Early peek: [Date - optional]
- Final analysis: [Date]

**Decision criteria:**
- If primary metric improves by [X%] with [Y%] confidence → Ship variant
- If no significant difference → Keep control
- If guardrail metric degrades → Stop test

**Segment analysis:**
- [ ] New vs returning users
- [ ] Mobile vs desktop
- [ ] [Other relevant segments]

## Rollout Plan

**If variant wins:**
1. [Step 1 - e.g., verify metrics stable]
2. [Step 2 - e.g., document learning]
3. [Step 3 - e.g., implement for 100%]

**If variant loses:**
1. [Step 1 - e.g., document why it failed]
2. [Step 2 - e.g., identify follow-up tests]

## Risks & Mitigations

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| [Risk description] | [H/M/L] | [H/M/L] | [How to handle] |

## Next Tests

**If this wins:** [Follow-up tests to run]
**If this loses:** [Alternative approaches to try]
```

---

## Quick Factor Capture Template

For rapid brainstorming sessions, use this lightweight format:

```markdown
# Quick Factor Capture: [KPI Name]

**Date:** [Date]
**Context:** [Brief situation]

| Factor | Category | Current | Alternative | Impact Est. | Effort Est. | Priority |
|--------|----------|---------|-------------|-------------|-------------|----------|
| [Name] | [Type] | [Now] | [Idea] | [1-5] | [1-5] | [Score] |
| [Name] | [Type] | [Now] | [Idea] | [1-5] | [1-5] | [Score] |

**Top 3 to Test:**
1. [Factor] - [Why first]
2. [Factor] - [Why second]
3. [Factor] - [Why third]
```

---

## Learning Summary Template

After completing several tests, synthesize learnings:

```markdown
# Learning Summary: [Area/Quarter]

**Period:** [Date range]
**Tests Completed:** [#]
**Win Rate:** [%]

## Key Learnings

### What Worked
1. **[Pattern/Insight]**
   - Evidence: [Test results]
   - Implication: [How to apply]
   
2. **[Pattern/Insight]**
   - Evidence: [Test results]
   - Implication: [How to apply]

### What Didn't Work
1. **[Pattern/Insight]**
   - Evidence: [Test results]
   - Learning: [What we know now]

### Surprising Results
1. **[Unexpected finding]**
   - What happened: [Result]
   - Theory: [Why it happened]
   - Follow-up: [What to test next]

## Principles Established

Based on our tests, we now believe:
- [Principle 1]
- [Principle 2]
- [Principle 3]

## Application to Future Work

**Design Decisions:**
- [How learnings inform design]

**Copy Guidelines:**
- [How learnings inform messaging]

**Product Priorities:**
- [How learnings inform roadmap]

## Open Questions

1. [Question we still need to answer]
2. [Question we still need to answer]

## Recommended Reading

For the team:
- [Test result 1 - link]
- [Test result 2 - link]
```
