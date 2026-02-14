# Writing Effective Analysis Findings

This guide provides standards and examples for transforming analytical results into clear, actionable communication.

## The SEBI Framework for Findings

Every finding should include:
- **S**tatement: What happened (the finding itself)
- **E**vidence: What proves it (data points)
- **B**usiness impact: Why it matters (implications)
- **I**nsight: What to do about it (leads to recommendations)

## Writing Style Guidelines

### Tone and Language
- **Use active voice:** "Setup completion dropped" not "A drop was observed in setup completion"
- **Be definitive when evidence supports it:** "The data shows" not "It appears that possibly"
- **Quantify everything possible:** Use percentages, absolutes, and comparisons
- **Eliminate jargon:** Write for an executive who isn't in the data daily
- **Focus on change:** Emphasize what's different, not just current state

### Structure
- **Lead with the finding:** Don't bury the lede in data details
- **Support with evidence:** Then provide proof points
- **End with implication:** Connect to business impact

## Examples of Well-Written Findings

### Example 1: Validated Hypothesis

**GOOD:**
> Account setup completion dropped from 78% to 61%, explaining 8 percentage points of the 15% decline in our North Star Metric. The drop occurred specifically at the "company name" step, where abandonment increased from 12% to 29%. This change coincided with the introduction of a new company verification feature that added 2-3 additional form fields. Mobile users were particularly affected, with completion rates 18 points lower than desktop users. This friction point is preventing roughly 2,000 additional users per month from experiencing our core product value.

**Why it works:**
- Opens with specific quantified finding (78% to 61%)
- Connects to overall problem (8pp of 15% decline)
- Identifies exact failure point (company name step)
- Provides supporting evidence (abandonment 12% to 29%)
- Links to likely cause (new verification feature)
- Segments by important dimension (mobile vs desktop)
- Quantifies business impact (2,000 users/month)

**BAD:**
> We found that users are having trouble with account setup. The data shows that completion rates went down. This appears to be related to some product changes. Mobile users seem particularly affected. This is having a negative impact on the business.

**Why it fails:**
- Vague ("having trouble", "went down")
- No specific numbers
- Weak language ("appears", "seem")
- No clear evidence or quantification
- Generic business impact statement

### Example 2: Invalidated Hypothesis

**GOOD:**
> User acquisition mix did not change meaningfully over the analysis period. Traffic from all channels maintained consistent proportions (±2%), and new user quality indicators (like time-to-first-action) remained stable across all sources. While this hypothesis seemed plausible given recent marketing campaigns, the data clearly shows the decline wasn't driven by lower-quality signups flooding the funnel. This allows us to focus resources on product friction points rather than acquisition strategy.

**Why it works:**
- Clearly states what was ruled out
- Provides specific evidence (±2% channel mix)
- Acknowledges why it was worth testing
- Quantifies stability (time-to-first-action stable)
- Ends with actionable implication (focus elsewhere)

**BAD:**
> The user mix hypothesis was wrong. We checked the data and it didn't show what we expected. So we moved on to other hypotheses.

**Why it fails:**
- No evidence provided
- Doesn't explain what was checked
- No value statement (why was this useful to test?)
- Wastes the negative finding

### Example 3: Partially Validated Hypothesis

**GOOD:**
> First prompt submission rates declined, but for different reasons than hypothesized. While we expected the help feature redesign to reduce submission rates, the data shows help feature users actually saw improved conversion (+8%). The decline came entirely from non-help users, where prompt submission dropped from 71% to 52%—a 19 percentage point decrease. This segment represents 65% of all users and contributed 9 percentage points to the overall 15% decline. The root cause appears to be unrelated to the help feature redesign: a new empty-state prompt template that users find confusing or overwhelming.

**Why it works:**
- Acknowledges partial validation clearly
- Separates what was wrong from what was right
- Provides specific numbers for both segments
- Quantifies overall impact (9pp of 15%)
- Identifies true root cause (prompt template)
- Shows sophisticated analysis thinking

## Evidence Presentation

### Effective Data Points

**Use these types of evidence:**
1. **Before/after comparisons:** "Dropped from 78% to 61%"
2. **Segment differences:** "Mobile users 18 points lower than desktop"
3. **Time correlations:** "Coincided with Oct 15 product release"
4. **Absolute impacts:** "Affecting 2,000 users per month"
5. **Statistical significance:** "95% confidence this isn't random variance"

### Avoid These Pitfalls

**Don't:** "The p-value was 0.03 and the confidence interval was [0.15, 0.23]"
**Do:** "We're highly confident (95%+) this is a real effect, not random noise"

**Don't:** "We ran a regression with 12 variables and the R² was 0.73"
**Do:** "Three factors together explain 73% of the variance: X, Y, and Z"

**Don't:** "The SQL query returned 45,382 rows with 23 columns"
**Do:** "Analysis of 45,000 user sessions showed..."

## Business Impact Statements

Every finding should answer: "So what?"

### Impact Formula
[Finding] → [Business consequence] → [Specific quantification]

**Example 1:**
"Account setup friction → Fewer users reaching core product → 2,000 lost activations per month → $150K monthly revenue impact at current LTV"

**Example 2:**
"Prompt submission delays → Longer time to first value → 23% of users abandoning before experiencing product → Direct hit to retention metrics"

### Bad Impact Statements
- "This is concerning" (No specifics)
- "This affects user experience" (Too vague)
- "This might hurt revenue" (Uncertain and unquantified)

### Good Impact Statements
- "At current conversion rates, this friction costs us 500 paid customers per quarter"
- "This explains why trial-to-paid conversion dropped 12 points in Q3"
- "Fixing this single issue could recover 60% of the North Star Metric decline"

## Confidence and Caveats

Be honest about certainty levels:

**High Confidence:**
"The data clearly shows..."
"We're confident this is the primary driver because..."

**Medium Confidence:**
"The evidence strongly suggests..."
"While not definitive, multiple indicators point to..."

**Low Confidence:**
"The available data hints at..."
"We saw directional trends indicating..."

**Always include caveats when relevant:**
- "This analysis covers only the past 8 weeks; longer-term trends may differ"
- "We couldn't directly measure X, so we used Y as a proxy"
- "Sample sizes for segment Z were small, making those findings less reliable"

## Common Mistakes to Avoid

### 1. Data Dump
**Bad:** "Users in cohort A had an average of 4.2 sessions with std dev 2.1, while cohort B had 3.8 sessions with std dev 1.9..."
**Good:** "Power users (cohort A) engage 11% more frequently than casual users"

### 2. Conclusion Without Evidence
**Bad:** "The new UI caused users to leave"
**Good:** "After the UI redesign, bounce rates increased from 15% to 31%, with session recordings showing confusion at the navigation menu"

### 3. Passive Voice and Hedging
**Bad:** "It was observed that there may have possibly been a reduction in the metric"
**Good:** "The metric dropped 15%"

### 4. Burying the Lede
**Bad:** "We analyzed 8 weeks of data across 12 segments using three different methodologies. The cohort analysis revealed interesting patterns. After controlling for various factors, we found that setup completion rates declined significantly."
**Good:** "Setup completion rates dropped 17 percentage points. Our analysis of 8 weeks of data identified..."

### 5. Missing the "So What"
**Bad:** "The button is now blue instead of green"
**Good:** "Changing the CTA button from green to blue reduced clicks by 23%, costing us 1,200 conversions per month"

## Checklist for Every Finding

Before finalizing each finding, verify:
- [ ] Finding stated clearly in first sentence
- [ ] At least 3 specific data points provided as evidence
- [ ] Impact quantified (%, absolute numbers, business metrics)
- [ ] Business implication explained
- [ ] Confidence level appropriate to evidence
- [ ] Written in active voice
- [ ] Jargon eliminated or explained
- [ ] Length is 3-5 paragraphs maximum
- [ ] Readable by non-analyst stakeholder
- [ ] Leads naturally to recommendations

## Template Structure for Each Finding

```markdown
### [HX: Hypothesis Name] - VALIDATED/INVALIDATED

**Status:** Analyzed
**Result:** Validated/Invalidated/Partially Validated
**Confidence Level:** High/Medium/Low
**Impact:** Contributes [X]% to the overall [Y]% decline

#### What We Found
[PARAGRAPH 1: Core finding with main quantification]
[PARAGRAPH 2-3: Supporting evidence and details]
[PARAGRAPH 4: Business implication]

#### Supporting Evidence
- **Data point 1:** [Specific metric or finding]
- **Data point 2:** [Specific metric or finding]  
- **Data point 3:** [Specific metric or finding]

#### Analysis Performed
[1-2 sentences: What analyses were done]

#### Why This Matters
[1-2 sentences: Business impact and implications]
```

This structure ensures consistency and completeness across all findings.
