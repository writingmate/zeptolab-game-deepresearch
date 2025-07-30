# Game Genre Market Research Pipeline
*AI Agent Linear Execution Framework*

## Overview

This pipeline executes comprehensive market research for any mobile game genre using a single AI agent with strict data validation requirements. Every data point must be backed by verifiable sources with working links.

**Input Required**: Genre name (e.g., "match-3", "idle games", "tower defense", "battle royale")

**Output**: Professional market research report in `/output/[Genre]_Market_Research_Report.md`

**Execution Time**: 4-6 hours depending on genre complexity and data availability

---

## Pipeline Steps

### Step 1: Market Intelligence Collection
**Objective**: Gather comprehensive market performance data for the target genre

**Data Sources**:
- Sensor Tower API/reports
- GameRefinery market analysis
- App Annie/data.ai industry insights
- Public company earnings reports

**Tasks**:
1. Search and collect top 50-100 games by revenue and downloads
2. Extract performance metrics: monthly revenue, download volumes, ranking positions
3. Identify market leaders and growth trends
4. Document regional performance variations

**Validation Requirements**:
- Each metric must include source URL + access date
- Cross-reference major claims with minimum 2 sources
- Archive screenshots of data dashboards when APIs unavailable

**Output**: `market_data.json` with complete source attribution

---

### Step 2: Competitive Feature Analysis
**Objective**: Map the competitive landscape through systematic feature analysis

**Data Sources**:
- App store pages (iOS/Android)
- Gameplay videos (YouTube, official channels)
- Developer websites and press releases
- Industry feature analysis reports

**Tasks**:
1. Analyze core gameplay mechanics across top games
2. Document meta-game systems (progression, monetization, social features)
3. Categorize features as Must-have/Nice-to-have/Optional
4. Identify common monetization patterns and live-ops cadence

**Validation Requirements**:
- Screenshot evidence for each claimed feature
- Source URLs for all feature descriptions
- Video timestamps for gameplay mechanic claims

**Output**: `feature_matrix.csv` with evidence links for every feature

---

### Step 3: Performance Benchmarking
**Objective**: Establish genre-specific KPI benchmarks and performance standards

**Data Sources**:
- GameRefinery benchmark reports
- Public analytics data from Sensor Tower/App Annie
- Industry benchmark studies
- Developer conference presentations

**Tasks**:
1. Collect retention rates (D1, D7, D30) for genre
2. Gather monetization metrics (ARPDAU, ARPU, conversion rates)
3. Document session length and engagement patterns
4. Establish CPI and LTV benchmarks by region

**Validation Requirements**:
- Minimum 3 sources per major benchmark metric
- Document methodology differences between sources
- Include confidence intervals and sample sizes when available

**Output**: `benchmarks.json` with comprehensive source attribution

---

### Step 4: Player Sentiment Analysis
**Objective**: Understand player preferences, pain points, and unmet needs

**Data Sources**:
- Reddit gaming communities
- YouTube game review comments
- App store reviews (iOS/Android)
- Discord gaming servers
- Gaming forums and communities

**Tasks**:
1. Analyze player complaints and feature requests
2. Document positive feedback patterns
3. Identify underserved player segments
4. Extract insights about preferred game mechanics and themes

**Validation Requirements**:
- Direct links to original posts/reviews for each insight
- Quote attribution with usernames and platforms
- Screenshots of representative comments/discussions

**Output**: `player_insights.md` with sourced quotes and patterns

---

### Step 5: Industry Context Research
**Objective**: Gather expert analysis and professional insights on the genre

**Data Sources**:
- GDC Vault presentations
- Naavik industry analysis
- Deconstructor of Fun articles
- Game Makers Toolkit videos
- Industry podcasts and interviews

**Tasks**:
1. Research design pattern evolution in the genre
2. Collect expert predictions and trend analysis
3. Document successful innovation examples
4. Analyze market timing and lifecycle stage

**Validation Requirements**:
- Full article URLs and publication dates
- Author credentials and expertise verification
- Video timestamps for specific claims

**Output**: `industry_analysis.md` with expert opinion summaries

---

### Step 6: Gap Analysis & Hypothesis Generation
**Objective**: Identify market opportunities and generate game concept hypotheses

**Process**:
1. Cross-reference data from Steps 1-5 to identify patterns
2. Map feature gaps and underserved market segments
3. Analyze successful outliers and innovation opportunities
4. Generate 5-10 specific game concept hypotheses

**Tasks**:
1. Identify white space in feature/theme combinations
2. Analyze underperforming areas with potential
3. Document successful cross-genre innovation examples
4. Formulate testable hypotheses with supporting evidence

**Validation Requirements**:
- Each hypothesis backed by specific data points from previous steps
- Reference successful comparable games with performance data
- Include risk assessment with supporting evidence

**Output**: `market_gaps.json` with complete evidence trails

---

### Step 7: Concept Scoring & Validation
**Objective**: Evaluate and prioritize game concepts using data-driven scoring

**Scoring Criteria** (1-3 scale each):
- **Market Size**: Large (3), Medium (2), Small (1)
- **Competition Gap**: Few rivals (3), Some (2), Many (1)  
- **CPI Estimate**: Low (3), Medium (2), High (1)
- **Development Difficulty**: Easy (3), Moderate (2), Hard (1)
- **Revenue Potential**: High (3), Medium (2), Low (1)

**Tasks**:
1. Score each concept against all criteria
2. Validate scores with comparable game data
3. Select top 3 concepts for detailed analysis
4. Document scoring rationale with sources

**Validation Requirements**:
- Each score supported by comparable game data with sources
- CPI estimates backed by genre-specific acquisition data
- Revenue potential validated against similar successful games

**Output**: `concept_scores.csv` with scoring justification links

---

### Step 8: Reference Game Deep Dive
**Objective**: Analyze successful reference games for each top concept

**Data Sources**:
- Sensor Tower performance data
- Gameplay analysis videos
- Developer interviews and case studies
- Monetization teardown reports

**Tasks**:
1. Select closest successful reference for each top concept
2. Analyze monetization strategy and revenue performance
3. Document progression systems and content pipeline
4. Extract key success factors and differentiation opportunities

**Validation Requirements**:
- Performance claims supported by Sensor Tower or equivalent data
- Gameplay mechanics verified through video evidence
- Monetization analysis backed by teardown reports or developer statements

**Output**: `reference_analysis.md` with comprehensive sourcing

---

### Step 9: Final Report Generation
**Objective**: Synthesize all research into professional market analysis report

**Report Structure**:
1. **Executive Summary** - Key findings and top opportunities
2. **Market Intelligence** - Size, growth, competitive landscape
3. **Performance Benchmarks** - Genre KPIs and success metrics
4. **Player Insights** - Sentiment analysis and unmet needs
5. **Industry Context** - Expert analysis and trend forecasts
6. **Market Opportunities** - Gap analysis and concept hypotheses
7. **Concept Evaluation** - Scored concepts with validation
8. **Reference Analysis** - Deep dive on successful comparables
9. **Recommendations** - Prioritized next steps and success criteria

**Quality Assurance**:
- Final validation that every statistic has working source link
- Cross-reference major claims across multiple sections
- Verify all URLs are accessible and archived
- Ensure consistent formatting and citation style

**Output**: `/output/[Genre]_Market_Research_Report.md`

---

## Critical Requirements

### Data Validation Standards
- **No Unsourced Claims**: Every data point must have verifiable source
- **Link Verification**: All URLs must be tested and functional
- **Multi-Source Validation**: Major metrics require minimum 2-3 sources
- **Archive Strategy**: Screenshot/archive key data to prevent link rot

### Quality Gates
- Pipeline halts if any step fails to meet sourcing requirements
- Minimum data thresholds must be met before proceeding to next step
- Final report only generates after comprehensive validation passes

### Source Hierarchy
**Tier 1 (Primary)**: Sensor Tower, GameRefinery, App Annie, company earnings
**Tier 2 (Secondary)**: Statista, industry analyst reports, major gaming press
**Tier 3 (Supporting)**: Community insights, expert opinions, gameplay analysis

---

## Execution Notes

- Single AI agent processes all steps sequentially
- Each step builds on validated outputs from previous steps
- Automatic halt if source validation fails at any point
- Final report includes complete methodology and source documentation
- All intermediate files saved for audit trail and future reference

This pipeline ensures comprehensive, verifiable market research that meets professional standards while leveraging AI automation for efficiency and consistency.