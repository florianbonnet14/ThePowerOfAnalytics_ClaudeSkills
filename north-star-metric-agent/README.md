# North Star Metric Advisor - Agent & Skill

This package contains a conversational agent that helps teams identify and validate their North Star Metric - the single most important metric that captures customer value delivery and predicts business success.

## What's Included

### Core Skill (SKILL.md)
The main instruction set for the agent, providing:
- The 4 Properties framework for validating metrics
- Conversational workflow (4 phases)
- Common patterns by product type
- Key pitfalls to avoid

### Reference Files
Detailed supporting documentation loaded as needed:
- **examples.md** - Product-specific North Star examples across 10+ industries
- **evaluation-framework.md** - Detailed scoring guide for the 4 properties
- **output-template.md** - Structured template for documenting the final metric
- **advanced-faq.md** - Advanced scenarios, FAQs, and pitfall deep-dives

## How It Works

The agent guides users through a natural conversation:

1. **Understand Context** (1-2 questions)
   - What does your product help customers achieve?
   - What journey does your team own?

2. **Identify Candidates** (2-3 questions)
   - List observable value-indicating actions
   - Define potential metrics
   - Narrow to top 3-5 candidates

3. **Evaluate** (1-2 questions)
   - Score against 4 properties
   - Validate total score ≥15/20

4. **Document**
   - Create North_Star_Metric.md using template

## Key Principles

- **One question at a time** - Keep conversation focused
- **5-7 questions total** - Reach recommendation quickly
- **No jargon** - Use simple, clear language
- **Validate rigorously** - All 4 properties must be strong

## The 4 Properties

Every North Star metric must:
1. **Reflect Customer Value** - Correlates with customer success
2. **Measurable** - Trackable with existing/achievable infrastructure
3. **Actionable** - Team controls 70%+ of drivers
4. **Tied to Revenue/Cost** - Improves business financially

## Usage

Simply start a conversation with the agent by describing your product or asking for help finding your North Star metric. The agent will guide you through the process conversationally.

Example starter: "I'm working on a SaaS tool for project management and need help defining our North Star metric."

## Based on "The Power of Analytics"

This agent implements the framework from Chapter 2 of "The Power of Analytics" by Florian Bonnet.
