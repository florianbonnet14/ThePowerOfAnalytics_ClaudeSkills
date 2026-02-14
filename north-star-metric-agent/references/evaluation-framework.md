# North Star Metric Evaluation Framework

## Detailed Scoring Guide

### 1. Reflects Customer Value (1-5)

**5 - Perfect Correlation**
- Metric directly measures the "aha moment" or core value proposition
- When this metric goes up, customers are definitively better off
- Example: Time spent watching for YouTube, Nights booked for Airbnb

**4 - Strong Correlation**
- Metric strongly indicates value delivery
- Minor gap between metric and actual value
- Example: # messages sent for Slack (proxy for communication value)

**3 - Moderate Correlation**
- Metric somewhat reflects value but has notable gaps
- Could be gamed without delivering real value
- Example: # page views (could be clickbait vs. valuable content)

**2 - Weak Correlation**
- Metric only loosely connected to customer outcomes
- Multiple steps removed from actual value
- Example: # sign-ups (doesn't show if product delivered value)

**1 - No Clear Correlation**
- Vanity metric with unclear connection to customer success
- Example: # app downloads (doesn't indicate usage or value)

**Red flags:**
- Metric can improve while customer satisfaction decreases
- Gaming the metric doesn't require improving product
- Metric measures inputs rather than outcomes

### 2. Measurable (1-5)

**5 - Already Tracking**
- Data currently collected in production
- Reliable, consistent measurement
- Low/no technical debt

**4 - Easy to Implement**
- Can add tracking within 1 sprint
- Uses existing infrastructure
- Minimal engineering effort

**3 - Moderate Effort**
- Requires new event tracking (2-4 weeks)
- May need new data pipeline
- Reasonable engineering investment

**2 - Significant Challenge**
- Requires major infrastructure changes (1-2 months)
- Complex data integration
- High engineering cost

**1 - Not Feasible**
- Impossible to measure directly
- Requires reading minds or predicting future
- Depends on untrackable offline behavior

**Red flags:**
- Relies on user self-reporting
- Requires third-party data unavailable to you
- Based on internal mental states vs. observable behavior

### 3. Actionable (1-5)

**5 - Full Control**
- Team directly influences 80-100% of metric drivers
- Can run experiments and see results quickly
- Leading indicator shows impact within days/weeks

**4 - Strong Control**
- Team influences 60-80% of drivers
- Some dependency on other teams, but minimal
- Leading indicator with reasonable feedback loop

**3 - Moderate Control**
- Team influences 40-60% of drivers
- Shared ownership with other teams
- Mix of leading and lagging indicators

**2 - Limited Control**
- Team influences 20-40% of drivers
- Heavy dependency on external factors
- Mostly lagging indicator (months to see impact)

**1 - No Control**
- Team influences <20% of drivers
- Dominated by market forces or other teams
- Pure lagging indicator

**Key Questions:**
- What % of this metric's drivers are in our team's control?
- If we ship a new feature, how long until we see impact?
- Are we dependent on other teams to move this metric?

**Span of Control Examples:**
- **High:** # Files shared (for Dropbox sharing team)
- **Medium:** # Active users (influenced by growth, product, retention)
- **Low:** Revenue (influenced by pricing, sales, market, product)

### 4. Tied to Revenue/Cost (1-5)

**5 - Direct Link**
- Metric is revenue or directly drives revenue/cost
- 1:1 relationship or well-established conversion rate
- Example: # Purchases, Subscription renewals

**4 - One Step Removed**
- Clear, data-backed connection to revenue
- Established correlation with business outcomes
- Example: # Active users → Paid conversions (if you know conversion rate)

**3 - Two Steps Removed**
- Reasonable hypothesis connecting to revenue
- Some data supporting connection
- Example: # Engagements → Retention → LTV

**2 - Weak/Indirect Connection**
- Logical but unproven connection to business
- Multiple assumptions required
- Example: # Social shares → Brand awareness → Growth

**1 - No Clear Connection**
- No plausible path to revenue/cost impact
- Pure vanity metric
- Example: # Page views (without engagement or conversions)

**Connection Patterns:**
- **Direct:** Transaction value, subscription revenue
- **One-step:** Active users → Paid conversions
- **Two-steps:** Engagement → Retention → LTV
- **Three-steps:** Usually too indirect for North Star

**Questions to Ask:**
- If this metric doubles, what happens to revenue?
- Can we trace a clear path from this metric to money?
- Would investors care about this metric?
- Has our data shown correlation between this metric and revenue?

## Total Score Interpretation

**18-20: Excellent North Star**
- Ready to use as primary success metric
- All properties strongly satisfied
- High confidence in metric choice

**15-17: Good North Star**
- Acceptable with minor weaknesses
- Consider if weaknesses are addressable
- Document limitations

**12-14: Needs Refinement**
- Missing key properties
- Revise metric or choose alternative
- Don't proceed without improvement

**<12: Poor Choice**
- Major gaps in multiple properties
- Return to candidate identification phase
- Consider different customer journey focus

## Special Cases

### Multi-Product Companies
- **Company North Star:** Unifying metric across products
- **Product North Stars:** Specific to each product
- All product North Stars should ladder up to company North Star

**Example - Google:**
- Company: # Queries per user
- Gmail: # Emails sent/received
- YouTube: Time spent watching

### Multi-Sided Marketplaces
- **Option 1 - Unified metric:** # Successful transactions (serves both sides)
- **Option 2 - Composite metric:** Balanced scorecard of supply + demand
- **Option 3 - Primary + Secondary:** One North Star + one critical constraint

**Example - Uber:**
- Primary: # Rides completed
- Critical constraint: Supply-demand balance (wait times <5 min)

### Freemium Products - Progression
- **Early stage:** # Active free users (finding PMF)
- **Growth stage:** % Free to paid conversion (scaling)
- **Mature stage:** Revenue per customer (optimizing)

## When to Change Your North Star

Change your North Star when:
- ✓ Product strategy fundamentally shifts
- ✓ Entering new markets with different value propositions
- ✓ Current metric sustained >80% of target for 2+ quarters
- ✓ Company stage changes (startup → growth → mature)

Don't change your North Star when:
- ✗ Metric hasn't moved in months (investigate root causes first)
- ✗ Leadership wants different metric (educate, don't capitulate)
- ✗ Metric is hard to improve (that's the point - North Star should be challenging)
