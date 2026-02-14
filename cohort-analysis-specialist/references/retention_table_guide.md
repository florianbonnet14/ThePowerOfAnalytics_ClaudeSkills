# Retention Table Creation Guide

## Step-by-Step Process

### Step 1: Define Cohort Boundaries

**Monthly Cohorts:**
- Group users by month of signup
- Example: All users who signed up in January 2024 = "Jan 24 cohort"
- Use first day of month as cohort identifier

**Weekly Cohorts:**
- Group users by week of signup (typically Monday start)
- Example: All users who signed up week of Jan 1-7 = "W1 2024 cohort"
- More granular but more cohorts to track

**Daily Cohorts:**
- Group users by exact signup date
- Use for high-volume products or short-term analysis
- Many cohorts, harder to see patterns

**Recommendation:** Start with monthly for strategic view, use weekly for operational monitoring

### Step 2: Define "Active"

**Common definitions:**

**Logged In:**
- Simplest definition
- User opened app or visited site
- Pros: Easy to track, clear
- Cons: May not indicate real engagement

**Performed Key Action:**
- Used core feature (e.g., sent message, created document)
- Pros: More meaningful than just login
- Cons: Must define "key action"

**Met Engagement Threshold:**
- Multiple actions (e.g., >3 sessions, >10 minutes)
- Pros: Captures quality engagement
- Cons: More complex to calculate

**Transaction-Based:**
- Made purchase or payment
- Best for: E-commerce, marketplaces, subscription businesses
- Pros: Directly tied to revenue
- Cons: May miss engaged non-buyers

**Choose based on your North Star metric and business model.**

### Step 3: Calculate Time Periods

**For each user in each cohort:**
- Determine which period they're in relative to signup
- Period 0 (M0): Same month as signup
- Period 1 (M1): One month after signup
- Period 2 (M2): Two months after signup
- etc.

**Example:**
- User signed up: Jan 15, 2024
- Analyzing March 2024
- User is in Period 2 (M2)

**Edge case handling:**
- User signs up Jan 31, next month is Feb (28 days)
- Use calendar months, not 30-day windows
- Be consistent in implementation

### Step 4: Calculate Retention Rates

**For each cohort and period:**

Retention Rate = (Active Users in Period) / (Total Cohort Size) × 100%

**Example:**
- Jan 2024 cohort: 1,000 users
- Active in March 2024 (M2): 520 users
- M2 Retention = 520 / 1,000 = 52%

**Important notes:**
- Always divide by original cohort size, not previous period
- M0 is always 100% by definition (active in signup period)
- Use same "active" definition consistently

### Step 5: Create the Table

**Table structure:**
```
         M0   M1   M2   M3   M4   M5   M6   M7   M8
Jan 24   100% 65%  52%  45%  41%  38%  36%  34%  33%
Feb 24   100% 68%  55%  48%  44%  40%  38%  36%  --
Mar 24   100% 70%  58%  51%  46%  42%  --   --   --
Apr 24   100% 72%  60%  53%  48%  --   --   --   --
May 24   100% 74%  62%  55%  --   --   --   --   --
Jun 24   100% 75%  63%  --   --   --   --   --   --
Jul 24   100% 76%  --   --   --   --   --   --   --
Aug 24   100% --   --   --   --   --   --   --   --
```

**Layout:**
- Rows: Cohorts (chronological, oldest to newest)
- Columns: Time periods (M0, M1, M2, etc.)
- Cells: Retention rate as percentage
- Diagonal: Most recent complete data
- Mark incomplete data: Use "--" or gray out

### Step 6: Add Color Coding (Optional)

**Heat map scale:**
- 🔴 Red: 0-40% (Critical - immediate action needed)
- 🟠 Orange: 40-60% (Concerning - investigate)
- 🟡 Yellow: 60-75% (Acceptable - monitor)
- 🟢 Green: 75-100% (Good - maintain)

**Customize thresholds based on:**
- Industry benchmarks
- Historical performance
- Product lifecycle stage
- Business goals

### Step 7: Interpret the Table

**Vertical Analysis (Compare across cohorts):**
Look down columns to see if retention at specific periods improving/declining
- M1 column: Jan 65% → Jul 76% = M1 retention improving!
- M3 column: Jan 45% → Apr 53% = M3 retention also improving

**Horizontal Analysis (Retention curve shape):**
Look across rows to see retention decay pattern
- Steep drop M0→M1 (65% retention) then gradual decline
- Suggests: Critical to hook users in first month

**Diagonal Analysis (Latest data):**
Follow diagonal line for most recent retention data
- Each cohort's latest data point
- Shows current state

## Common Patterns and What They Mean

### Pattern 1: Improving Cohorts
```
Jan 24   100% 65%  52%  45%
Feb 24   100% 68%  55%  48%
Mar 24   100% 70%  58%  51%
Apr 24   100% 72%  60%  53%
```
**Meaning:** Recent cohorts performing better than old ones
**Cause:** Product improvements, better onboarding, higher quality users
**Action:** Continue current strategy, document what changed

### Pattern 2: Declining Cohorts
```
Jan 24   100% 75%  63%  55%
Feb 24   100% 72%  60%  52%
Mar 24   100% 68%  55%  48%
Apr 24   100% 65%  52%  45%
```
**Meaning:** Recent cohorts performing worse than old ones
**Cause:** Product issues, market changes, lower quality users
**Action:** Urgent investigation needed, identify what changed

### Pattern 3: Plateau Formation
```
Cohort   M0   M1   M2   M3   M4   M5   M6
Jan 24   100% 65%  52%  48%  46%  45%  45%
```
**Meaning:** Retention stabilizes after initial drop
**Cause:** Core user base forms, "true believers" remain
**Action:** Understand plateau level, focus on early retention

### Pattern 4: Continuous Decline (No Plateau)
```
Cohort   M0   M1   M2   M3   M4   M5   M6
Jan 24   100% 65%  52%  45%  38%  32%  27%
```
**Meaning:** No stable engaged base, continuous churn
**Cause:** Lack of stickiness, no habit formation
**Action:** Major product/market fit issue, needs attention

### Pattern 5: Resurrection (U-Shape)
```
Cohort   M0   M1   M2   M3   M4   M5   M6
Jan 24   100% 65%  52%  45%  48%  52%  55%
```
**Meaning:** Users coming back after initial drop
**Cause:** Delayed value realization, reactivation campaigns
**Action:** Understand triggers, accelerate time to value

## Data Requirements

**Minimum data needed:**
- User ID
- Signup date
- Activity dates (each time user was "active")

**Recommended additional data:**
- Acquisition channel
- User attributes (plan tier, segment, etc.)
- Feature usage
- Revenue data (for LTV analysis)

**Data quality checks:**
- No duplicate user IDs
- Signup dates accurate and complete
- Activity tracking consistent
- Test users excluded
- Time zones handled correctly

## Tools and Implementation

**Spreadsheet (Excel, Google Sheets):**
- Good for: Small datasets, manual analysis, sharing
- Limit: ~50,000 users before slow
- Formula: `=COUNTIFS(users, cohort, active_dates, period) / COUNTIF(users, cohort)`

**SQL Database:**
- Good for: Large datasets, automated reporting
- Use window functions and joins
- Can integrate with BI tools

**Business Intelligence Tools (Tableau, Looker, Mode):**
- Good for: Interactive dashboards, sharing, drilling down
- Most have cohort analysis templates
- Can refresh automatically

**Analytics Platforms (Mixpanel, Amplitude):**
- Good for: Pre-built cohort analysis
- Fastest to implement
- Limited customization

## Frequency of Analysis

**Daily:** Not recommended (too noisy, incomplete data)
**Weekly:** Good for operational monitoring
**Monthly:** Best for strategic review
**Quarterly:** Good for executive reporting, long-term trends

**Recommendation:** Monthly table update, weekly monitoring of latest cohort D7/D30
