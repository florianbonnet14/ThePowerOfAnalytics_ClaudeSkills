# KPI Tree Examples

Detailed worked examples using the clean output format without method labels in the tree structure.

## Example 1: SaaS Upselling

### Complete Tree

```
# North Star Metric: Upselling Rate
**Definition**: Percentage of customers who upgrade to higher-tier plans
**Formula**: (# Customers Buying Higher Tier / Total # Customers) × 100
**Current**: 8.5% | **Target**: 12%

## KPI Tree

Upselling Rate
├─ # Customers Buying Higher Tier
│  ├─ # Visits to Upgrade Page
│  │  ├─ # Email Campaign Visits
│  │  │  ├─ # Emails Sent
│  │  │  ├─ Email Open Rate (%)
│  │  │  └─ Click-Through-Open Rate (%)
│  │  │     └─ 🔍 Email subject line quality, send time optimization
│  │  └─ # Organic Visits
│  │     ├─ # In-App Prompt Clicks
│  │     │  └─ 🔍 In-app prompt placement, feature comparison clarity
│  │     └─ # Direct Navigation
│  └─ Conversion Rate from Visit to Purchase
│     ├─ % Who Click "Upgrade" CTA
│     │  └─ 🔍 Button design and copy, pricing page layout
│     └─ % Who Complete Checkout
│        └─ 🔍 Payment method options, form field simplicity
└─ Total # Customers

## Decomposition Explanation

**Level 1 - Numerator & Denominator:**
- Method: Mathematical
- Rationale: Rate naturally decomposes into numerator and denominator
- Formula: Upselling Rate = (# Customers Buying Higher Tier / Total # Customers) × 100

**Level 2 - Numerator breakdown:**
- Method: Process (multiplication)
- Rationale: Customers must visit the upgrade page AND convert
- Formula: # Customers Buying = # Visits × Conversion Rate

**Level 3 - Visits breakdown:**
- Method: Segmentation (addition)
- Rationale: Visits come from distinct sources
- Formula: Total Visits = Email Campaign Visits + Organic Visits

**Level 4 - Email Campaign:**
- Method: Process (multiplication)
- Rationale: Sequential funnel from send to click
- Formula: Email Visits = # Sent × Open Rate × Click-Through-Open Rate

**Level 3 - Conversion breakdown:**
- Method: Process (multiplication)
- Rationale: Two-step conversion process
- Formula: Overall Conversion = CTA Click Rate × Checkout Completion Rate

## MECE Validation

**Level 1:**
- ✓ Mutually Exclusive: Numerator and denominator don't overlap
- ✓ Collectively Exhaustive: Together they form complete rate
- ✓ Formula check: Verified

**Level 2:**
- ✓ Mutually Exclusive: Visits and conversion rate are distinct
- ✓ Collectively Exhaustive: Visits × Conversion = Total conversions
- ✓ Formula check: Verified

**Level 3 - Visits:**
- ✓ Mutually Exclusive: Email vs Organic are distinct sources
- ✓ Collectively Exhaustive: All visits accounted for
- ✓ Formula check: Verified

## Key Insights

1. **Primary leverage point**: Email Click-Through-Open Rate - small improvements have multiplicative effect
2. **Quick wins**: In-app prompt placement (easy to test)
3. **Data gaps**: Need to track "Direct Navigation" separately
4. **Strategic implications**: Email campaign is primary driver
```

## Example 2: E-commerce Delivery Time

### Complete Tree

```
# North Star Metric: Average Delivery Time
**Definition**: Hours from order placement to customer receipt
**Formula**: Sum of all process stage durations
**Current**: 48 hours | **Target**: 36 hours

## KPI Tree

Average Delivery Time
├─ Pick List Generation Time
│  ├─ Order Queue Wait Time
│  │  └─ 🔍 Order volume patterns, system capacity
│  └─ System Processing Time
│     └─ 🔍 Order complexity, system performance
├─ Item Picking Time
│  ├─ Time per Item
│  │  └─ 🔍 Warehouse layout efficiency, item location optimization
│  └─ # Items per Order
├─ Packing Time
│  ├─ Standard Packing Time
│  └─ Special Handling Time
│     └─ 🔍 Packing materials availability, staff training level
└─ Shipping Time
   ├─ Carrier Pickup Time
   │  └─ 🔍 Pickup schedule optimization
   └─ Transit Time
      ├─ Distance-Based Duration
      └─ 🔍 Carrier selection rules

## Decomposition Explanation

**Level 1 - Process stages:**
- Method: Process (addition)
- Rationale: Total time is sum of sequential stages
- Formula: Total Time = Pick List Gen + Picking + Packing + Shipping

**Level 2 - Each stage breakdown:**
- Method: Process (addition or multiplication depending on stage)
- Rationale: Each stage has distinct sub-components
- Examples: 
  - Picking Time = Time per Item × # Items
  - Packing = Standard + Special Handling
  - Shipping = Pickup Wait + Transit

## MECE Validation

**Level 1:**
- ✓ Mutually Exclusive: Each process stage distinct, no overlap
- ✓ Collectively Exhaustive: Covers complete delivery lifecycle
- ✓ Formula check: Sum equals total delivery time

**Level 2:**
- ✓ Each stage's components are MECE within that stage
- ✓ All sub-processes accounted for

## Key Insights

1. **Primary leverage point**: Item Picking Time (28% of total) - warehouse layout optimization high-impact
2. **Quick wins**: Carrier pickup scheduling (reduce wait time by 2-3 hours)
3. **Data gaps**: Need granular tracking of packing times by order type
4. **Strategic implications**: Operational efficiency focus, not just carrier speed
```

## Example 3: Content Platform Engagement

### Complete Tree

```
# North Star Metric: Time Spent per User per Week
**Definition**: Average minutes spent on platform per user per week
**Formula**: # Sessions per User × Avg Time per Session
**Current**: 105 minutes | **Target**: 150 minutes

## KPI Tree

Time Spent per User per Week
├─ # Sessions per User
│  ├─ % Users with 1 Session × 1
│  │  └─ 🔍 Onboarding quality, initial value delivery
│  ├─ % Users with 2-5 Sessions × Avg(3.5)
│  │  └─ 🔍 Content recommendation quality, notification strategy
│  └─ % Users with 6+ Sessions × Avg(8)
│     └─ 🔍 Habit formation mechanics, content freshness
└─ Avg Time per Session
   ├─ # Content Pieces per Session
   │  ├─ First Content View (entry point)
   │  └─ Additional Content Views
   │     └─ 🔍 Recommendation algorithm quality, autoplay settings
   └─ Avg Time per Content Piece
      ├─ Video Content Duration
      │  └─ 🔍 Video quality, loading speed
      ├─ Article Content Duration
      │  └─ 🔍 Article length and quality
      └─ Interactive Content Duration
         └─ 🔍 Interactivity design, engagement mechanics

## Decomposition Explanation

**Level 1 - Frequency × Intensity:**
- Method: Mathematical (multiplication)
- Rationale: Total time = how often they come × how long they stay
- Formula: Total Time = # Sessions × Time per Session

**Level 2 - Sessions breakdown:**
- Method: Segmentation (weighted average)
- Rationale: Different user types have different session patterns
- Formula: Avg Sessions = Sum(% Users in Segment × Sessions per Segment)

**Level 2 - Time per session breakdown:**
- Method: Mathematical (multiplication)
- Rationale: Session time = pieces viewed × time per piece
- Formula: Session Time = # Pieces × Avg Time per Piece

**Level 3 - Content type segmentation:**
- Method: Segmentation
- Rationale: Different content types have different consumption times
- Formula: Avg Time = Weighted avg across content types

## MECE Validation

**Level 1:**
- ✓ Mutually Exclusive: Frequency and duration are independent
- ✓ Collectively Exhaustive: Together capture total time
- ✓ Formula check: Verified

**Level 2 - Sessions:**
- ✓ Mutually Exclusive: User segments don't overlap (1, 2-5, 6+)
- ✓ Collectively Exhaustive: All users categorized
- ✓ Formula check: Weighted average correct

**Level 2 - Duration:**
- ✓ Mutually Exclusive: # pieces and time per piece distinct
- ✓ Collectively Exhaustive: Together determine session length
- ✓ Formula check: Verified

## Key Insights

1. **Primary leverage point**: Additional Content Views (recommendation algorithm) - drives both session length and frequency
2. **Quick wins**: Autoplay settings optimization for video content
3. **Data gaps**: Need better content type classification and viewing completion tracking
4. **Strategic implications**: Focus on 2-5 session users to drive them to power user segment
```

## Example 4: B2B Sales Pipeline

### Complete Tree

```
# North Star Metric: Quarterly Contract Value (QCV)
**Definition**: Total value of deals closed per quarter
**Formula**: # Deals Closed × Average Deal Size
**Current**: $2.4M | **Target**: $3.5M

## KPI Tree

Quarterly Contract Value
├─ # Deals Closed
│  ├─ # Leads Generated
│  │  ├─ Inbound Leads
│  │  │  ├─ Content Marketing Leads
│  │  │  ├─ Event/Webinar Leads
│  │  │  └─ Referral Leads
│  │  │     └─ 🔍 Referral program design, incentive structure
│  │  └─ Outbound Leads
│  │     ├─ SDR-Generated Leads
│  │     │  └─ 🔍 SDR talk tracks, targeting criteria
│  │     └─ Marketing-Generated Leads
│  ├─ Lead-to-Opportunity Conversion (%)
│  │  └─ 🔍 Lead qualification criteria, SDR training
│  └─ Opportunity-to-Close Conversion (%)
│     └─ 🔍 Demo quality, pricing negotiation, competitive positioning
└─ Average Deal Size
   ├─ Enterprise Deals (>$100K)
   │  ├─ % of Total Deals
   │  └─ Average Enterprise Value
   │     └─ 🔍 Upsell strategy, multi-year contracts
   ├─ Mid-Market Deals ($25K-$100K)
   │  ├─ % of Total Deals
   │  └─ Average Mid-Market Value
   └─ SMB Deals (<$25K)
      ├─ % of Total Deals
      └─ Average SMB Value
         └─ 🔍 Package design, tiering strategy

## Decomposition Explanation

**Level 1 - Volume × Value:**
- Method: Mathematical (multiplication)
- Rationale: Revenue = how many deals × how much per deal
- Formula: QCV = # Deals Closed × Average Deal Size

**Level 2 - Deal volume breakdown:**
- Method: Process (multiplication)
- Rationale: Sales funnel with conversion rates
- Formula: # Closed = # Leads × Lead-to-Opp % × Opp-to-Close %

**Level 3 - Lead generation:**
- Method: Segmentation (addition)
- Rationale: Distinct lead sources
- Formula: Total Leads = Inbound + Outbound

**Level 2 - Deal size breakdown:**
- Method: Segmentation (weighted average)
- Rationale: Customer segments with different values
- Formula: Avg Deal Size = Sum(% Deals in Segment × Segment Avg Value)

## MECE Validation

**Level 1:**
- ✓ Mutually Exclusive: Volume and size are independent
- ✓ Collectively Exhaustive: Together determine total value
- ✓ Formula check: Verified

**Level 2 - Pipeline:**
- ✓ Mutually Exclusive: Funnel stages are sequential
- ✓ Collectively Exhaustive: Complete conversion path
- ✓ Formula check: Verified

**Level 3 - Lead sources:**
- ✓ Mutually Exclusive: Inbound vs Outbound clearly defined
- ✓ Collectively Exhaustive: All lead sources categorized
- ✓ Formula check: Verified

## Key Insights

1. **Primary leverage point**: Opportunity-to-Close % (currently 28%, target 35%) - demo quality and competitive positioning
2. **Quick wins**: Optimize referral program (high-quality leads, lower volume)
3. **Data gaps**: Need better deal size tracking by initial vs expansion revenue
4. **Strategic implications**: Should focus on Mid-Market segment (best volume/value balance)
```

## Example 5: Subscription Retention

### Complete Tree

```
# North Star Metric: 12-Month Retention Rate
**Definition**: % of cohort still active after 12 months
**Formula**: (Customers Active at Month 12 / Initial Cohort) × 100
**Current**: 65% | **Target**: 75%

## KPI Tree

12-Month Retention Rate
├─ Early Retention (M1-3 Survival)
│  ├─ Onboarding Completion Rate
│  │  └─ 🔍 Onboarding flow design, time-to-value
│  ├─ First Value Achievement Rate
│  │  └─ 🔍 Feature discoverability, aha moment clarity
│  └─ Initial Feature Adoption Rate
│     └─ 🔍 In-app guidance quality
├─ Mid Retention (M4-6 Survival)
│  ├─ Feature Usage Frequency
│  │  └─ 🔍 Feature utility, user workflows
│  ├─ Support Ticket Resolution Rate
│  │  └─ 🔍 Support quality, response times
│  └─ Value Realization Score
│     └─ 🔍 Customer success outreach, ROI communication
├─ Late Retention (M7-9 Survival)
│  ├─ Advanced Feature Adoption Rate
│  │  └─ 🔍 Feature education, power user programs
│  ├─ Integration Usage Rate
│  │  └─ 🔍 Integration quality, setup ease
│  └─ Team Expansion Rate
│     └─ 🔍 Viral mechanics, invite flows
└─ Mature Retention (M10-12 Survival)
   ├─ Renewal Process Completion Rate
   │  └─ 🔍 Renewal UX, pricing changes
   └─ Value Expansion Rate
      └─ 🔍 Upsell effectiveness, feature value demonstration

## Decomposition Explanation

**Level 1 - Temporal stages:**
- Method: Process (multiplication of survival rates)
- Rationale: Overall retention is cumulative survival through stages
- Formula: 12M Retention = Early × Mid × Late × Mature retention rates

**Level 2 - Stage-specific factors:**
- Method: Hybrid (process and segmentation)
- Rationale: Each lifecycle stage has distinct retention drivers
- Note: Each stage's factors combine to determine survival probability

## MECE Validation

**Level 1:**
- ✓ Mutually Exclusive: Time periods don't overlap
- ✓ Collectively Exhaustive: Covers full 12-month period
- ✓ Formula check: Cumulative survival model correct

**Level 2:**
- ✓ Each stage's factors are distinct within that stage
- ✓ Factors comprehensively cover key retention drivers
- ✓ Formula check: Verified for each stage

## Key Insights

1. **Primary leverage point**: Early Retention (M1-3) - sets foundation, 85% of users who survive M3 reach M12
2. **Quick wins**: Onboarding completion (currently 72%, increase to 85%)
3. **Data gaps**: Need better tracking of "aha moment" achievement
4. **Strategic implications**: Front-load customer success investment in first 90 days
```

## Usage Notes

These examples demonstrate:
- **Clean tree structure**: No method labels cluttering the visualization
- **Separate explanation section**: Methods and rationale clearly documented
- **Influential factors**: Integrated naturally at leaf nodes
- **Complete validation**: MECE checks at each level
- **Actionable insights**: Specific leverage points and next steps

When building your own trees, follow this format for clarity and professional presentation.
