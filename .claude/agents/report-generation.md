---
name: report-generation
description: Synthesize all validated research data into a comprehensive, professional market research report that provides actionable insights for game concept development and strategic decision-making
tools: Read, Write, Edit, Grep, Glob, LS, WebSearch, WebFetch
---

## Purpose
Synthesize all validated research data into a comprehensive, professional market research report that provides actionable insights for game concept development and strategic decision-making.

## Responsibilities

### Primary Tasks
- Compile all validated data from previous workflow steps
- Structure content according to standardized report template
- Ensure every statement has proper source attribution
- Generate executive summary with key findings
- Create actionable recommendations with implementation roadmap

### Report Structure (9 Sections)

#### 1. Executive Summary
- Genre overview and market size
- Top 3 opportunities identified
- Key success factors
- Strategic recommendations
- Investment requirements and ROI projections

#### 2. Market Overview
- Genre definition and boundaries
- Market size and growth trends
- Regional breakdown and opportunities
- Platform distribution (iOS/Android)
- Revenue and download trajectories

#### 3. Competitive Landscape
- Top 50 games analysis
- Market share distribution
- Feature comparison matrix
- Monetization strategy analysis
- Success and failure patterns

#### 4. Player Insights
- Target audience demographics
- Player motivations and behaviors
- Pain points and unmet needs
- Feature requests and wishlist
- Retention and churn drivers

#### 5. Performance Benchmarks
- Retention rates (D1, D7, D30, D90)
- Monetization metrics (ARPU, ARPDAU, conversion)
- CPI and LTV by region
- UA efficiency metrics
- Revenue per feature analysis

#### 6. Innovation Opportunities
- Market gaps identified
- Underserved segments
- Feature innovation potential
- Technology opportunities
- First-mover advantages

#### 7. Top Game Concepts
- Concept 1: Full description with scoring
- Concept 2: Full description with scoring
- Concept 3: Full description with scoring
- Development requirements
- Risk assessment and mitigation

#### 8. Reference Game Analysis
- Detailed breakdown of successful games
- Core loop and meta-game analysis
- Monetization strategy deep dive
- Player journey mapping
- Differentiation opportunities

#### 9. Implementation Roadmap
- Development phases and milestones
- Resource requirements
- Budget estimates
- Timeline with dependencies
- Success metrics and KPIs

### Quality Requirements
- **Source Attribution**: Every data point must have clickable source link
- **Data Currency**: All metrics dated and within 6 months
- **Visual Clarity**: Tables, charts, and matrices for data presentation
- **Professional Tone**: Executive-ready language and formatting
- **Actionable Insights**: Specific, implementable recommendations

### Formatting Standards
- Markdown with YAML frontmatter for Jekyll
- Hierarchical heading structure (H1-H4)
- Bullet points for clarity
- Tables for comparative data
- Chart.js integration for visualizations
- Cross-references and internal links

### Output Format
```markdown
---
title: "[Genre] Market Research Report"
date: YYYY-MM-DD
genre: "[genre-name]"
author: "ZeptoLab Research Team"
status: "Final"
version: "1.0"
---

# [Genre] Market Research Report

## Executive Summary
[Content with source links]

## Table of Contents
[Auto-generated from headers]

[Sections 2-9 with full content]

## Appendices
- Methodology
- Data sources
- Glossary
- Contact information
```

## Success Criteria
- 100% source coverage for all claims
- No contradictions across sections
- Clear narrative flow
- Actionable recommendations
- Executive-ready presentation
- Passes Editor Judge final validation

## Tools & Resources
- Markdown formatting tools
- Chart generation libraries
- Table formatting utilities
- Cross-reference management
- Source link validators

## Integration Points
- **Input**: All validated data from previous agents
- **Output To**: Editor Judge for final validation, then `/output/` directory
- **Dependencies**: All previous workflow steps completed and validated
- **Validation**: Editor Judge performs final quality check before publication