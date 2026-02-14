# Good vs Bad Examples

## Common Mistakes & How to Fix Them

### Mistake 1: Burying the Lede

**❌ Bad Example:**
```
"We analyzed data from Q3 across multiple segments including enterprise,
SMB, and self-serve, looking at various metrics including retention,
activation, and revenue. We also examined cohort trends and seasonal
patterns. After extensive investigation using statistical methods and
consulting with multiple stakeholders, we discovered several interesting
patterns in the data..."

[Answer finally appears on page 2]
```

**✓ Good Example:**
```
"New enterprise customers convert 40% better than SMBs because they 
have dedicated onboarding support. We should offer paid onboarding 
packages to SMBs, projecting 15% conversion improvement ($500K annual 
revenue).

Context: We analyzed Q3 data across customer segments to identify 
conversion drivers..."
```

**Why it's better:** Answer comes first. Reader knows the conclusion and recommendation immediately.

---

### Mistake 2: Vague Recommendations

**❌ Bad Example:**
```
"We should improve the user experience."
"The team needs to focus on quality."
"We recommend further investigation."
```

**✓ Good Example:**
```
"We should add a 3-step interactive tutorial shown on first login,
similar to what Slack does. Owner: Jane (Product). ETA: Dec 15.
Success: 80% of new users complete tutorial, Week 1 retention +10pp."
```

**Why it's better:** Specific action, clear owner, deadline, and measurable success criteria.

---

### Mistake 3: No Quantification

**❌ Bad Example:**
```
"This will significantly improve revenue."
"Customers will be much happier."
"It's a big opportunity."
```

**✓ Good Example:**
```
"Based on 900 affected customers per month at $50 AOV and 15% 
conversion, this represents $81K annual recurring revenue at risk.
Recovery should happen within 2-4 weeks of fix deployment."
```

**Why it's better:** Specific numbers with units. Timeline provided. Impact is calculable.

---

### Mistake 4: Too Much Detail Upfront

**❌ Bad Example:**
```
[Executive Summary includes:]
- 3 pages of charts
- Detailed methodology
- Statistical significance calculations
- Complete segmentation breakdown
- Full SQL queries
- Every data point collected
```

**✓ Good Example:**
```
[Executive Summary = 1 page MAIN]
[Supporting Insights = 3-4 charts with brief explanation]
[Detailed Analysis = Appendix with methodology, queries, etc.]

Let stakeholders drill down if interested.
```

**Why it's better:** Respects reader's time. Enables progressive disclosure.

---

### Mistake 5: No "So What?"

**❌ Bad Example:**
```
"40% of customers are in Segment A.
30% are in Segment B.
Segment A uses Feature X 2.3x more than Segment B.
Load times for Feature X are 4.2 seconds."

[Presents facts but doesn't explain implications or actions]
```

**✓ Good Example:**
```
"Segment A (40% of users) drives 65% of engagement through Feature X,
but experiences the slowest load times (4.2s). Optimizing Feature X
performance should disproportionately benefit our most engaged users,
likely improving overall retention by 8-12 percentage points.

Recommendation: Prioritize Feature X performance sprint next quarter."
```

**Why it's better:** Connects data to business impact. States clear action. Explains "why it matters."

---

### Mistake 6: Death by Bullet Points

**❌ Bad Example:**
```
Key Findings:
• Metric A changed
• Metric B also changed  
• We noticed C
• D is interesting
• E might be relevant
• F could be important
• G is worth mentioning
• H is related
• I shows something
• J indicates another thing
[20+ bullets that should be a narrative]
```

**✓ Good Example:**
```
Three insights drive our recommendation:

1. Metric A dropped 15% because onboarding flow changed, affecting 
   900 new customers per month

2. This was caused by removing the tutorial in the Sept 15 release, 
   which we validated through session recordings showing 40% drop-off
   at step 3

3. We can fix this by restoring the tutorial and simplifying the flow,
   recovering $81K ARR within 4 weeks

Supporting data in Appendix A.
```

**Why it's better:** Narrative flow. Three clear points. Each point tells a story.

---

## Complete Before/After Examples

### Example 1: Conversion Analysis

**❌ Bad Version:**
```
# Conversion Analysis

## Background
Over the past few months, we've been monitoring various metrics and 
noticed some trends that seemed concerning. The team decided to do a 
deep dive to understand what's happening with our funnel.

## Methodology
We looked at data from the past 90 days, segmented by various 
dimensions including channel, device, user type, geography, and time 
of day. We used SQL queries to extract the data and Python for analysis.

## Findings
- Overall conversion is down
- Some segments are doing better than others
- Mobile seems different from desktop
- New users behave differently than returning users
- Weekends show different patterns
[Continues for 3 more pages before getting to the point]
```

**✓ Good Version:**
```
# Conversion Drop Analysis - Executive Summary

## Motive
Our Q3 conversion rate dropped 15% vs. Q2 (from 40% to 34%), threatening 
our annual growth target. This analysis identifies the root cause and 
proposes immediate corrective actions.

## Answer
The drop is entirely driven by new mobile users, whose conversion fell 
30% after we redesigned the mobile checkout flow on Sept 15. Returning 
users and desktop users show normal conversion rates. We recommend 
immediately rolling back the mobile checkout changes and A/B testing a 
simplified 3-step flow. This should recover 10 percentage points within 
2 weeks.

## Impact
At current traffic (3,000 mobile signups/day), this represents 900 lost 
conversions daily. At $50 AOV and 15% conversion to paid, we're losing 
$6,750 in daily revenue ($2.5M annually). Quick rollback should recover 
70% of this loss within one week. Full recovery expected after flow 
optimization.

## Next Steps
1. Rollback mobile checkout to Aug version - Owner: Dev Team - ETA: Tomorrow
   Success: Mobile conversion returns to 38%+
   
2. Design simplified 3-step mobile flow - Owner: Sarah (Product) - ETA: Nov 27
   Success: Designs approved by stakeholders
   
3. Build and launch A/B test - Owner: Dev Team - ETA: Dec 6
   Success: 50/50 test live to new mobile users
   
4. Analyze and decide on rollout - Owner: Data Team - ETA: Dec 20
   Success: Clear recommendation with statistical significance
```

**What makes it good:**
- Answer in first paragraph
- Quantified impact with specific numbers
- Clear timeline and actions
- Specific owners and dates
- Passes "So What?" test

---

### Example 2: Feature Proposal

**❌ Bad Version:**
```
# New Feature Idea

## Overview
We've been thinking about ways to improve the product and had some 
interesting discussions with the team. There seems to be potential in 
adding some new capabilities.

## What We're Thinking
We could potentially add features that might help users accomplish 
their goals better. Some customers have mentioned this could be useful.

## Next Steps
We should probably investigate this further and see what others think.
Maybe we could do some research and come back with more details.
```

**✓ Good Version:**
```
# Proposal: Paid Onboarding Service

## Opportunity
65% of our SMB customers (1,200 companies) struggle with initial setup, 
taking 14+ days to first value vs. 2 days for enterprise customers with 
dedicated support. This slow activation drives 40% Month-1 churn in SMB 
segment.

## Proposal
Launch tiered onboarding service: (1) Self-serve free, (2) Guided setup 
$499, (3) White-glove $1,999. Based on enterprise customer data, guided 
onboarding should reduce time-to-value by 60% and cut Month-1 churn from 
40% to 20%.

## Expected Impact
At 25% attach rate (300 customers/month), this generates $150K monthly 
revenue ($1.8M annually). Additionally, improved activation should reduce 
SMB churn by 10 percentage points, retaining an additional 120 customers 
monthly ($400K annual LTV impact). Total impact: $2.2M annually.

## Required Investment
- 2 Customer Success hires: $200K/year
- Training materials development: 1 month, $50K
- CRM integration: 2 weeks engineering time
- Total first-year cost: $250K (8.8x ROI)

## Next Steps to Approve
1. Finalize pricing and service tiers - Owner: Sarah (Product) - ETA: Nov 30
2. Get exec approval and budget - Owner: Sarah - ETA: Dec 5
3. Hire and train CS team - Owner: Jane (HR) - ETA: Jan 15
4. Build booking system - Owner: Dev Team - ETA: Jan 15
5. Launch to 10% of new SMB signups - Owner: Sarah - ETA: Jan 20
6. Analyze results and scale - Owner: Data Team - ETA: Feb 15
```

**What makes it good:**
- Clear opportunity with data
- Specific proposal with pricing
- Quantified ROI
- Investment requirements stated
- Actionable next steps with timeline

---

### Example 3: Weekly Business Review

**❌ Bad Version:**
```
# Weekly Update

## This Week
- We did various things
- Some metrics went up
- Some metrics went down
- Team had meetings
- Working on stuff

## Next Week
- Will continue working
- Monitoring the situation
- Following up on things
```

**✓ Good Version:**
```
# Product Team - Weekly Business Review
Week of Nov 20-26, 2024

## Executive Summary

### Performance Overview
Conversion improved 3% WoW but remains 8% below target. Mobile activation 
reached 85% (above 80% target). Average session time dropped 15% due to 
performance issues identified and being fixed.

### Key Changes This Week
1. Mobile conversion +5%: New checkout flow deployed Wed, showing early 
   positive signal (needs full week for significance)
   
2. Session time -15%: Image loading bug introduced in v2.4.1, causing 
   3-5s delays. Fix deployed Friday, monitoring recovery
   
3. Paid conversion +2%: Promotional campaign ended, returning to baseline

### Actions Required
1. Monitor mobile checkout performance - Owner: Sarah - Check: Mon
   Decision: Rollout to 100% if positive trend continues
   
2. Verify session time recovery - Owner: Dev Team - Check: Mon
   If not recovered, escalate to engineering leadership

---

## Detailed Metrics

### North Star: Weekly Active Users
- Current: 45,200
- WoW: +2.1%
- MoM: +8.3%
- vs Target: 94% (target: 48,000) 🟡
- Analysis: Steady growth from SEO improvements, on track to hit target 
  next week

### Driver: New User Activation
- Current: 85%
- WoW: +3pp
- Target: 80% 🟢
- Analysis: Mobile flow improvement driving gains

### Driver: Paid Conversion
- Current: 12%
- WoW: -1pp
- Target: 15% 🔴
- Analysis: Below target due to promo ending, testing new pricing next week

---

## Looking Ahead

### Next Week Expectations
- Full week data on mobile checkout (decision Mon)
- New pricing test launch (targeting +2pp conversion)
- Black Friday prep (expecting 30% traffic spike)

### Risks to Watch
- Image loading fix may not fully resolve session time issue
- Black Friday traffic spike could expose other performance problems

### Opportunities
- If mobile checkout performs well, fast-track similar improvements to 
  desktop
```

**What makes it good:**
- Concise summary with numbers
- Clear explanation of changes
- Specific actions with owners
- Trends visible (WoW, MoM, vs Target)
- Forward-looking section
- Easy to scan and digest

---

## Writing Quality Examples

### Active vs Passive Voice

**❌ Passive:**
```
"It was determined that the conversion rate had been affected by the 
changes that were made to the onboarding flow. An improvement of 15% 
was observed after the fix was implemented."
```

**✓ Active:**
```
"We determined that onboarding flow changes affected conversion rate. 
We observed a 15% improvement after implementing the fix."
```

---

### Specific vs Vague Numbers

**❌ Vague:**
```
"Many customers complained about performance issues. This significantly 
impacted our business. We expect major improvements."
```

**✓ Specific:**
```
"1,200 customers (15% of user base) reported performance issues in past 
month. This contributed to 8% increase in churn ($240K annual revenue 
impact). We expect 60% reduction in performance complaints within 2 weeks 
of fix deployment."
```

---

### Direct vs Hedged Language

**❌ Hedged:**
```
"We think maybe this might potentially help possibly improve things 
somewhat if everything goes according to plan and assuming conditions 
remain favorable."
```

**✓ Direct (with honest uncertainty):**
```
"This will improve conversion by 10-15% (confidence: medium, based on 
similar past initiatives). Risk: If customer preferences have shifted, 
actual improvement may be lower (5-10%)."
```

---

## The One-Sentence Summary Test

Before writing any executive summary, try to answer in ONE sentence:

**"What is the single most important thing leadership needs to know?"**

### Example Scenarios:

**Q:** We did a conversion analysis. What should they know?
**A:** "New mobile users convert 30% worse than before because we removed 
the tutorial, costing us $2.5M annually, and we should rollback immediately."

**Q:** We're proposing a new feature. What should they know?
**A:** "Paid onboarding service will generate $2.2M annually with $250K 
investment and 9x ROI."

**Q:** Weekly update. What should they know?
**A:** "We're 8% below conversion target due to a performance bug that's 
now fixed, expecting recovery next week."

This one sentence becomes the foundation of your Answer section.
