---
name: gtm-builder
display_name: B2B SaaS Go-To-Market Builder
description: Build complete Go-To-Market strategies for B2B SaaS products through a structured 9-dashboard sequence plus a 10-slide GTM Walkthrough Deck.
version: 3.1.0
author: Custom
triggers:
  - GTM strategy
  - go-to-market
  - GTM for
  - build GTM
  - ICP definition
  - pricing strategy
  - competitive analysis
  - positioning strategy
  - customer journey
  - marketing assets
  - outbound strategy
  - B2B SaaS launch
  - value proposition
  - buying committee
---

# B2B SaaS Go-To-Market Builder Skill

## SKILL OVERVIEW

This skill builds a complete Go-To-Market strategy through a structured 9-dashboard sequence, culminating in a 10-slide GTM Walkthrough Deck. Each step uses specific prompts that Claude executes sequentially.

**Dashboards Produced (9):**
1. Product Feature Matrix Dashboard
2. Competitive Market Analysis Dashboard
3. Positioning Dashboard
4. ICP Dashboard
5. Buying Committee Dashboard
6. Value Proposition Dashboard
7. Customer Journey Funnel Dashboard
8. Assets & Collaterals Library Dashboard
9. Pricing & Packaging Dashboard

**Final Output:** 10-slide GTM Walkthrough Deck (Markdown for Gamma AI)

**Additional Deliverables:**
- Lead Magnet Specification (ScoreApp scorecard spec - not a dashboard)

---

## EXTERNAL RESEARCH STEPS

⚠️ **Three steps require external deep research.** Claude provides research scope, user executes externally using tools like Perplexity, Browse AI, or manual research, then returns findings to Claude.

| Step | Phase | Research Needed | User Tools |
|------|-------|-----------------|------------|
| **Step 1.1** | Product Feature Matrix | Competitor feature analysis + customer reviews | Perplexity, competitor websites, G2, Capterra |
| **Step 2.1** | Competitive Analysis | Competitor website crawling + customer reviews | Perplexity, Browse AI, G2, Capterra, Trustpilot |
| **Step 2.7** | Competitive Analysis | G2 reviews deep analysis (4-5 star + 1-3 star breakdown) | G2.com manual review |

---

## OUTPUT FORMAT MAPPING

| Dashboard | Primary Output | File Format | Tool |
|-----------|---------------|-------------|------|
| Product Feature Matrix | Tables + Scatter Plot Data | XLSX | Excel/Sheets |
| Competitive Market Analysis | Tables | XLSX | Excel/Sheets |
| Positioning | Statements + Summary | DOCX | Google Docs |
| ICP | Tables | XLSX | Excel/Sheets |
| Buying Committee | Tables | XLSX | Excel/Sheets |
| Value Proposition | Pillars + 9 Copy Drills | DOCX | Google Docs |
| Customer Journey Funnel | Table | XLSX | Excel/Sheets |
| Assets & Collaterals Library | Table | XLSX | Excel/Sheets |
| Pricing & Packaging | Tables + ROI Calculators | XLSX | Excel/Sheets |
| **Lead Magnet Spec** | Scorecard Spec | XLSX + DOCX | Excel + Docs |
| **GTM Walkthrough Deck** | Markdown slides | MD | Gamma AI |

---

## REQUIRED INPUTS (COLLECT BEFORE STARTING)

```
DISCOVERY INPUTS CHECKLIST:

□ 1. PROJECT INFORMATION
   - Project name: _______________
   - Project website: _______________
   - Category name: _______________
   - Niche focus: _______________
   - One-liner description: _______________

□ 2. COMPETITORS LIST (5-6)
   - Competitor 1: _______________ (website: ___)
   - Competitor 2: _______________ (website: ___)
   - Competitor 3: _______________ (website: ___)
   - Competitor 4: _______________ (website: ___)
   - Competitor 5: _______________ (website: ___)
   - Competitor 6: _______________ (website: ___)

□ 3. PRODUCT FEATURES LIST
   - Feature 1: _______________
   - Feature 2: _______________
   - Feature 3: _______________
   - Feature 4: _______________
   - Feature 5: _______________
   (Add more as needed)

□ 4. BUSINESS CONTEXT
   - Current team structure
   - Monthly burn rate
   - Runway remaining
   - Channels tried (and results)
```

---

# ═══════════════════════════════════════════════════════════════
# PHASE 1: PRODUCT FEATURE MATRIX DASHBOARD
# ═══════════════════════════════════════════════════════════════

## Step 1.1: Research Scope for Feature Analysis

⚠️ **DEEP RESEARCH STEP - USER EXECUTES EXTERNALLY**

**PROMPT (Claude provides scope):**
```
I need to conduct feature analysis research for {project_name} in the {category_name} category.

═══════════════════════════════════════════════════════════════
RESEARCH SCOPE FOR EXTERNAL EXECUTION
═══════════════════════════════════════════════════════════════

For each competitor below, gather:
□ List of features from website (features page, pricing page)
□ Customer reviews mentioning features (G2, Capterra)
□ What features customers praise most
□ What features customers complain about or wish existed

COMPETITORS TO RESEARCH:
1. {competitor_1} - {website_1}
2. {competitor_2} - {website_2}
3. {competitor_3} - {website_3}
4. {competitor_4} - {website_4}
5. {competitor_5} - {website_5}

OUR FEATURES TO VALIDATE:
1. {feature_1}
2. {feature_2}
3. {feature_3}
4. {feature_4}
5. {feature_5}

SOURCES TO CHECK:
- Competitor websites (features, pricing pages)
- G2.com reviews
- Capterra reviews
- Product Hunt discussions

═══════════════════════════════════════════════════════════════
Please conduct this research and return findings.
═══════════════════════════════════════════════════════════════
```

**USER ACTION:** Execute research externally and return findings to Claude.

---

## Step 1.2: Feature Demand & Competitiveness Analysis

**PROMPT (after receiving research):**
```
You're an expert B2B SaaS Go-To-Market Strategist.
You are building a GTM Strategy for {project_website} with our workflow that starts with the Product Feature Matrix.

Using the research provided, analyze each feature for demand and competitiveness.

DEMAND SCALE:
- Wanted by one
- Wanted by some
- Wanted by most
- Wanted by all

COMPETITIVENESS SCALE:
- Commodity: Should be free
- Most Vendors can do this
- A few others can do this
- Unique to us: Only we can do this

COMPETITORS RESEARCHED:
1. {competitor_1}
2. {competitor_2}
3. {competitor_3}
4. {competitor_4}
5. {competitor_5}

PRODUCT FEATURES:
1. {feature_1}
2. {feature_2}
3. {feature_3}
4. {feature_4}
5. {feature_5}

Put the result in a table.
Features in the vertical axis.
Demand and Competitiveness in columns.
```

---

## Step 1.3: Scatter Plot Scoring

**PROMPT:**
```
We need to visualize the features on a Scatter Plot.

Give each feature a score on the two axes:
- Demand: -20 to +20
- Competitiveness: -20 to +20

RULE: The numbers need definitive distribution with decimals.
NOT 10, 15, 20
USE 7.3, 8.5, 9.1, 12.4, -3.7, etc.

Put the results in a table:
| Feature | Demand Score | Competitiveness Score |
```

---

## Step 1.4: Quadrant Assignment

**PROMPT:**
```
Split the results into two tables:

TABLE 1: Features with scores
| Feature | Demand Score | Competitiveness Score |

TABLE 2: Feature quadrant assignment
| Feature | Quadrant | Rationale |

QUADRANT REFERENCE:
```
                    HIGH COMPETITIVENESS (+20)
                           │
         QUADRANT 2        │        QUADRANT 1
      "Differentiators"    │      "Hero Features"
      Low Demand,          │      High Demand,
      High Competitive     │      High Competitive
      Advantage            │      Advantage
                           │
LOW DEMAND ─────────────────┼─────────────────── HIGH DEMAND
(-20)                      │                        (+20)
                           │
         QUADRANT 3        │        QUADRANT 4
        "Commodities"      │       "Table Stakes"
      Low Demand,          │      High Demand,
      Low Competitive      │      Low Competitive
      Advantage            │      Advantage
                           │
                    LOW COMPETITIVENESS (-20)
```

---

## Step 1.5: Entry Validation Rules

**PROMPT:**
```
VALIDATION RULES - Review and troubleshoot:

If "Wanted by some" → EXCLUDE "Most vendors can do this"
If "Wanted by all" → EXCLUDE "Unique to us: Only we can do it"
If "Wanted by one" → EXCLUDE "Commodity should be free"

Review all feature categorizations and flag any violations.
Adjust categorization where needed to maintain logical consistency.
```

---

## Step 1.6: Demand Driver Identification

**PROMPT:**
```
Identify ONE demand driver from the features list (or propose a new one) that can be a top-of-funnel entry for users.

RULES - This demand driver must:
1. Give immediate value to the user
2. Reveal a problem that can only be solved by {project_name}

OUTPUT TABLE:
| Attribute | Description |
|-----------|-------------|
| What it is | |
| Immediate value | |
| How it helps in problem identification | |
| How it exposes the need to use {project_name} | |
| ICP fit | |
| Leverage for conversion | |
| Top-of-funnel use case | |
```

---

## Step 1.7: Demand Driver Variants

**PROMPT:**
```
For the demand driver, create a variety of demand drivers that differ on a sliding scale:

SCALE DIMENSIONS:
1. Perceived Value & Impact (Low → High)
2. Ease of Delivery (Hard → Easy)

DELIVERY TYPE OPTIONS:
- Service-based white glove
- Light tool
- Value using the software itself
- Self-assessment scorecard (to be built on ScoreApp.com)

OUTPUT TABLE:
| Variant Name | Perceived Value (Low/Med/High) | Ease of Delivery (Hard/Med/Easy) | Delivery Type | Description | TOFU Use Case |
|--------------|-------------------------------|----------------------------------|---------------|-------------|---------------|

Note: The self-assessment scorecard option will be developed fully in the Lead Magnet Specification deliverable.
```

**OUTPUT FORMAT:** XLSX with sheets: Scoring, Quadrants, Demand_Drivers

---

# ═══════════════════════════════════════════════════════════════
# PHASE 2: COMPETITIVE MARKET ANALYSIS DASHBOARD
# ═══════════════════════════════════════════════════════════════

## Step 2.1: Competitor Research Scope

⚠️ **DEEP RESEARCH STEP - USER EXECUTES EXTERNALLY**

**PROMPT (Claude provides scope):**
```
I need to conduct competitive research for the {category_name} category with focus on {niche}.

═══════════════════════════════════════════════════════════════
RESEARCH SCOPE FOR EXTERNAL EXECUTION
═══════════════════════════════════════════════════════════════

For each competitor below, gather the following information:

□ Website URL
□ Tagline (from homepage)
□ Sub-tagline (secondary headline)
□ Full description (from homepage/about page)
□ Strengths (from customer reviews, testimonials, G2, Capterra)
□ Weaknesses (from customer reviews, complaints, negative feedback)

COMPETITORS TO RESEARCH:
1. {competitor_1} - {website_1}
2. {competitor_2} - {website_2}
3. {competitor_3} - {website_3}
4. {competitor_4} - {website_4}
5. {competitor_5} - {website_5}
6. {project_name} (our product) - {project_website}

SOURCES TO CHECK:
- Company websites (homepage, about, features, pricing pages)
- G2.com reviews
- Capterra reviews
- Trustpilot
- LinkedIn company pages
- Product Hunt

═══════════════════════════════════════════════════════════════
Please conduct this research using Perplexity, Browse AI, or manual research.
Return findings in a structured format matching the attributes above.
═══════════════════════════════════════════════════════════════
```

**USER ACTION:** Execute research externally and return findings to Claude.

---

## Step 2.2: Competitor Summary Table

**PROMPT (after receiving research):**
```
Using the research provided, create the competitor summary table.

OUTPUT TABLE:
Put companies in the horizontal axis (first row as headers).
Put {project_name} in the FIRST column.

| Attribute | {project_name} | {competitor_1} | {competitor_2} | {competitor_3} | {competitor_4} | {competitor_5} |
|-----------|----------------|----------------|----------------|----------------|----------------|----------------|
| Website | | | | | | |
| Tagline | | | | | | |
| Sub Tag | | | | | | |
| Description | | | | | | |
| Strengths | | | | | | |
| Weaknesses | | | | | | |
```

---

## Step 2.3: Core Offering Vectors

**PROMPT:**
```
Describe in bullet points what each product offers at the core.

RULE: Each bullet point = ONE WORD only.
You can use multiple bullet points to represent the product's complete core offering.

OUTPUT:
{project_name}: • [word] • [word] • [word] • [word]
{competitor_1}: • [word] • [word] • [word] • [word]
{competitor_2}: • [word] • [word] • [word] • [word]
{competitor_3}: • [word] • [word] • [word] • [word]
{competitor_4}: • [word] • [word] • [word] • [word]
{competitor_5}: • [word] • [word] • [word] • [word]
```

---

## Step 2.4: Target Audience Extraction

**PROMPT:**
```
For each company, identify target audiences from:
- Website copy
- Product descriptions
- Social media bios
- Pricing page language

OUTPUT TABLE:
| Company | Target Audience #1 | Target Audience #2 |
|---------|-------------------|-------------------|
| {project_name} | | |
| {competitor_1} | | |
| {competitor_2} | | |
| {competitor_3} | | |
| {competitor_4} | | |
| {competitor_5} | | |
```

---

## Step 2.5: Value Proposition Extraction

**PROMPT:**
```
Find the core value propositions for each product.

RULE: Value Proposition = What the product offers at the core to the ICP at each level of engagement.
RULE: Value proposition is a crisp 3-4 words max sentence.

THREE LEVELS:
- Value Proposition #1 (User level)
- Value Proposition #2 (Manager level)
- Value Proposition #3 (Decision Maker level)

OUTPUT TABLE:
| Company | VP #1 (User) | VP #2 (Manager) | VP #3 (Decision Maker) |
|---------|--------------|-----------------|------------------------|
| {project_name} | | | |
| {competitor_1} | | | |
| {competitor_2} | | | |
| {competitor_3} | | | |
| {competitor_4} | | | |
| {competitor_5} | | | |
```

---

## Step 2.6: Feature Extraction

**PROMPT:**
```
For each company, extract the list of features as described on website pages and pricing tiers.

RULE: Extract all features and write them exactly as described by the company.

List all features under each company (no table yet):

{project_name}:
- Feature 1
- Feature 2
- ...

{competitor_1}:
- Feature 1
- Feature 2
- ...

(Repeat for each competitor)
```

---

## Step 2.7: G2 Reviews Deep Analysis

⚠️ **DEEP RESEARCH STEP - USER EXECUTES EXTERNALLY**

**PROMPT (Claude provides scope):**
```
I need G2 review analysis to define positioning vectors.

═══════════════════════════════════════════════════════════════
RESEARCH SCOPE FOR EXTERNAL EXECUTION
═══════════════════════════════════════════════════════════════

For each competitor's G2 page, analyze ALL published reviews:

4 & 5 STAR REVIEWS (What users love):
- Extract repeated positive themes
- Identify what each company is leading in
- Count frequency of each theme
- These represent what competitors currently lead in

1, 2 & 3 STAR REVIEWS (What users dislike/wish for):
- Extract repeated complaints
- Identify gaps and wishes
- Count frequency of each theme
- These represent opportunities we can capture

COMPETITORS TO ANALYZE:
1. {competitor_1} - G2 URL: [find URL]
2. {competitor_2} - G2 URL: [find URL]
3. {competitor_3} - G2 URL: [find URL]
4. {competitor_4} - G2 URL: [find URL]
5. {competitor_5} - G2 URL: [find URL]

OUTPUT NEEDED:
For each competitor:
- Top 3 positive themes from 4-5 star reviews (with frequency)
- Top 3 negative themes from 1-3 star reviews (with frequency)

═══════════════════════════════════════════════════════════════
Please conduct this research on G2.com manually.
Return findings in a structured format.
═══════════════════════════════════════════════════════════════
```

**USER ACTION:** Execute G2 research and return findings to Claude.

---

## Step 2.8: Positioning Vectors Definition

**PROMPT (after receiving G2 research):**
```
Using the G2 analysis, define 4 positioning vectors:

VECTOR CREATION RULES:
- First 2 vectors: From 4-5 star reviews (what competitors currently lead in)
- Last 2 vectors: Reverse of 1-3 star complaints (what we can lead in)

EXAMPLE:
1-star complaint: "confusing interface" 
→ Our Vector: "Intuitive User Experience"

SCORING:
Score each company 0-10 per vector.
Use fractions: 9.3, 6.5, 7.8, etc.

OUTPUT TABLE:
| Positioning Vector | {project_name} | {comp_1} | {comp_2} | {comp_3} | {comp_4} | {comp_5} |
|--------------------|----------------|----------|----------|----------|----------|----------|
| [Vector 1 - They Lead] | | | | | | |
| [Vector 2 - They Lead] | | | | | | |
| [Vector 3 - We Lead] | | | | | | |
| [Vector 4 - We Lead] | | | | | | |

GOAL: Create a scenario where {project_name} is the obvious choice for a selected segment at our current stage.
```

---

## Step 2.9: Feature Consolidation

**PROMPT:**
```
Shortlist the features by merging features that have the same core concept.

RULES:
- No two features should have similar or proximate characteristics
- If any features are similar, merge them under one name
- The shortlist should include all features across all products with no repetition

OUTPUT: Consolidated feature list with no duplicates.
```

---

## Step 2.10: Feature Presence Table

**PROMPT:**
```
Put the consolidated features in a table.

Companies on the horizontal axis.
Features in the vertical axis.

Use ✓ or ✗ symbols to indicate presence or absence.

OUTPUT TABLE:
| Feature | {project_name} | {comp_1} | {comp_2} | {comp_3} | {comp_4} | {comp_5} |
|---------|----------------|----------|----------|----------|----------|----------|
| [Feature 1] | ✓/✗ | ✓/✗ | ✓/✗ | ✓/✗ | ✓/✗ | ✓/✗ |
| [Feature 2] | ✓/✗ | ✓/✗ | ✓/✗ | ✓/✗ | ✓/✗ | ✓/✗ |
```

---

## Step 2.11: Features to Benefits

**PROMPT:**
```
Turn each feature into a benefit.

RULE: The benefit is the second and third level effect from the customer's point of view after using the feature. What does the customer gain when they use the feature?

List the benefits in the same structure as features.
```

---

## Step 2.12: Benefits Potency Scoring

**PROMPT:**
```
For the benefits table, replace ✓/✗ with potency scores.

Score each benefit 1 to 5 stars based on how powerfully each company delivers that benefit.

OUTPUT TABLE:
| Benefit | {project_name} | {comp_1} | {comp_2} | {comp_3} | {comp_4} | {comp_5} |
|---------|----------------|----------|----------|----------|----------|----------|
| [Benefit 1] | ★★★★☆ | ★★★☆☆ | ★★★★★ | ★★☆☆☆ | ★★★☆☆ | ★★★★☆ |
```

---

## Step 2.13: Competitive Advantage

**PROMPT:**
```
Pick ONE competitive advantage for each company.

RULES:
- Competitive advantage = Unique differentiation
- Could be: company focus, positioning, unique feature, USP, market advantage, or a combination
- Make it crisp: 3-4 words maximum

OUTPUT TABLE:
| Company | Competitive Advantage |
|---------|----------------------|
| {project_name} | |
| {competitor_1} | |
| {competitor_2} | |
| {competitor_3} | |
| {competitor_4} | |
| {competitor_5} | |
```

---

## Step 2.14: Competitive Advantage Explanation

**PROMPT:**
```
Add an "Explanation" row where you expand on how each company differentiates by capitalizing on their competitive advantage.

OUTPUT TABLE:
| Company | Competitive Advantage (3-4 words) | Explanation |
|---------|-----------------------------------|-------------|
| {project_name} | | |
| {competitor_1} | | |
| {competitor_2} | | |
| {competitor_3} | | |
| {competitor_4} | | |
| {competitor_5} | | |
```

---

## Step 2.15: Category Summary

**PROMPT:**
```
Create a category summary with:

1. Four headlines (one per positioning vector)
2. The company leading each vector
3. A content summary of how this core offering affects customer acquisition for that company

OUTPUT:
Four summary blocks, one per vector:

**Vector 1: [Vector Name]**
Leader: [Company]
Impact: [How this affects their customer acquisition]

**Vector 2: [Vector Name]**
Leader: [Company]
Impact: [How this affects their customer acquisition]

**Vector 3: [Vector Name]**
Leader: [Company - should be us]
Impact: [How this affects customer acquisition]

**Vector 4: [Vector Name]**
Leader: [Company - should be us]
Impact: [How this affects customer acquisition]
```

---

## Step 2.16: Positioning Summary

**PROMPT:**
```
Summarize {project_name} positioning and differentiation.

Write how {project_name} can theoretically lead the category if we focus on delivering unique features that focus on:
- {positioning_vector_3} (our vector)
- {positioning_vector_4} (our vector)

Cover:
- How that affects customer acquisition
- Market growth potential
- Defensibility

FORMAT: Two small paragraphs maximum. Crisp and concise.
```

**OUTPUT FORMAT:** XLSX with multiple sheets + DOCX for positioning summary

---

# ═══════════════════════════════════════════════════════════════
# PHASE 3: POSITIONING DASHBOARD
# ═══════════════════════════════════════════════════════════════

## Step 3.1: Positioning Statements

**PROMPT:**
```
Create positioning statements for {project_name}.

TEMPLATE FORMAT:
**Against [Competitor Category]:**
Not "[what they think we are]"—[what we actually are]. [Differentiation statement].

CREATE THREE STATEMENTS:
1. Against direct competitors (same category)
2. Against indirect competitors (alternative solutions)
3. Against status quo (manual processes/doing nothing)

OUTPUT: Three positioning statements in the template format above.
```

**OUTPUT FORMAT:** DOCX

---

# ═══════════════════════════════════════════════════════════════
# PHASE 4: ICP DASHBOARD
# ═══════════════════════════════════════════════════════════════

## Step 4.1: Two-Level ICP Definition

**PROMPT:**
```
Build {project_name} Ideal Customer Profile.

Create TWO ICP levels:
- ICP Level 1: MVP to PMF Stage
- ICP Level 2: Growth Stage

For each ICP, populate the following:

OUTPUT TABLE:
| Attribute | ICP Level 1 (MVP-PMF) | ICP Level 2 (Growth) |
|-----------|----------------------|---------------------|
| Segment | | |
| Sub-industries | | |
| Location | | |
| Revenue, $ | | |
| Team Size | | |
| Business Maturity | | |
| Business Model | | |
| Best Engagement Model | | |
| Organization Challenges and Pain Points | | |
| Why Should They Choose Us (Value Proposition Hypothesis) | | |
| Strategic Goals Related to Our Product/Service | | |
| Triggers | | |
```

**OUTPUT FORMAT:** XLSX

---

# ═══════════════════════════════════════════════════════════════
# PHASE 5: BUYING COMMITTEE DASHBOARD
# ═══════════════════════════════════════════════════════════════

## Step 5.1: Purchasing Committee Personas

**PROMPT:**
```
For BOTH ICPs, build Purchasing Committee Personas.

THREE PERSONA LEVELS:
1. User (day-to-day operator)
2. Manager (team lead/supervisor)
3. Decision Maker (budget holder)

FOR EACH PERSONA, POPULATE:

OUTPUT TABLE (create one per ICP):
| Attribute | User | Manager | Decision Maker |
|-----------|------|---------|----------------|
| Possible Job Titles | | | |
| Responsibility Area | | | |
| Purchasing Influence | | | |
| Core Customer Journey Stages | | | |
| Potential Reasons to Block | | | |
| Drivers | | | |
| Assets to Get Buy-In | | | |
| Channels to Find Them | | | |

Create TWO tables: one for ICP Level 1, one for ICP Level 2.
```

---

## Step 5.2: Design Partner Profile

**PROMPT:**
```
Build an Early Adopter/Design Partner profile.

These are people who have:
- Highest affinity to try the first prototype
- Risk tolerance to be early adopters
- Time to contribute feedback

OUTPUT TABLE:
| Attribute | Specification |
|-----------|---------------|
| Design Partner Attributes | |
| Job Titles | |
| Demographics | |
| Responsibility Areas | |
| Current Tools | |
| Key Pain Points | |
| Critical Triggers | |
| Goals & Motivations | |
| Decision Criteria | |
| Influence Level | |
| Barriers to Purchase | |
| Information Sources | |
| Success Metrics | |
| Early Adopter Characteristics | |
```

**OUTPUT FORMAT:** XLSX with sheets: ICP1_Personas, ICP2_Personas, Design_Partners

---

# ═══════════════════════════════════════════════════════════════
# PHASE 6: VALUE PROPOSITION DASHBOARD
# ═══════════════════════════════════════════════════════════════

## Step 6.1: Brand Promise & Positioning

**PROMPT:**
```
Build Value Proposition for {project_name} starting with these definitions:

OUTPUT TABLE:
| Element | Definition |
|---------|------------|
| Brand Promise | What does your brand promise on a basic level? What is the point? The deliverable? |
| Positioning | What is your brand's unique claim? What can only you do? |
```

---

## Step 6.2: Value Proposition Pillars + Copy Drills

**PROMPT:**
```
Generate Value Proposition Pillars and Copy Drills.

THE RESULT IS 10 TABLES TOTAL:

═══════════════════════════════════════════════════════════════
TABLE 1: VALUE PROPOSITION PILLARS
═══════════════════════════════════════════════════════════════

| Value Prop | Description | Reason to Believe #1 | Reason to Believe #2 | Reason to Believe #3 |
|------------|-------------|---------------------|---------------------|---------------------|
| VP 1 | [Description] | [RTB 1.1] | [RTB 1.2] | [RTB 1.3] |
| VP 2 | [Description] | [RTB 2.1] | [RTB 2.2] | [RTB 2.3] |
| VP 3 | [Description] | [RTB 3.1] | [RTB 3.2] | [RTB 3.3] |

═══════════════════════════════════════════════════════════════
TABLES 2-10: COPY DRILLS (one per Reason to Believe)
═══════════════════════════════════════════════════════════════

COPY DRILL TEMPLATE (repeat 9 times, once per RTB):

**Copy Drill for [VP Name] - [RTB Name]**

| Element | Content |
|---------|---------|
| Reason to Believe | [RTB statement] |
| Headline (Rational) | |
| Headline (Emotional) | |
| Headline (Social Proof) | |
| Subhead | |
| Body Copy (25 words max) | |
| CTA | |
| Supporting Proof Point | |

Create all 9 copy drill tables:
- VP1-RTB1, VP1-RTB2, VP1-RTB3
- VP2-RTB1, VP2-RTB2, VP2-RTB3
- VP3-RTB1, VP3-RTB2, VP3-RTB3
```

**OUTPUT FORMAT:** DOCX

---

# ═══════════════════════════════════════════════════════════════
# PHASE 7: CUSTOMER JOURNEY FUNNEL DASHBOARD
# ═══════════════════════════════════════════════════════════════

## Step 7.1: Full Funnel Mapping

**PROMPT:**
```
Create Customer Journey Funnel for {project_name}.

OUTPUT TABLE:
| Funnel Stage | Buyer Mindset & Trigger | Key Questions They Ask | {project_name} Touch-points & Assets (channel) | Internal Goal / KPI | State After Stage (Desired Outcome) | Function |
|--------------|------------------------|------------------------|-----------------------------------------------|---------------------|-------------------------------------|----------|
| 1. Problem Awareness | "[Quote representing mindset]" | • Q1 • Q2 • Q3 | • Asset 1 (channel) • Asset 2 (channel) | • KPI 1 • KPI 2 | [State after completing stage] | Marketing |
| 2. Solution Discovery | "[Quote]" | • Questions | • Assets | • KPIs | [Outcome] | Marketing/Sales |
| 3. Vendor Evaluation | "[Quote]" | • Questions | • Assets | • KPIs | [Outcome] | Sales |
| 4. Trial/Purchase Decision | "[Quote]" | • Questions | • Assets | • KPIs | [Outcome] | Sales/CS |
| 5. Value Realization | "[Quote]" | • Questions | • Assets | • KPIs | [Outcome] | CS |
| 6. Expansion & Advocacy | "[Quote]" | • Questions | • Assets | • KPIs | [Outcome] | CS/Marketing |
| 7. Renewal & Loyalty | "[Quote]" | • Questions | • Assets | • KPIs | [Outcome] | CS/Product |

ADD SECTION - Key Journey Insights:
- Critical Success Factors (4 bullets)
- Primary Journey Blockers (4 bullets)
- Acceleration Opportunities (4 bullets)
```

**OUTPUT FORMAT:** XLSX

---

# ═══════════════════════════════════════════════════════════════
# PHASE 8: ASSETS & COLLATERALS LIBRARY DASHBOARD
# ═══════════════════════════════════════════════════════════════

## Step 8.1: Full-Funnel Asset Mapping

**PROMPT:**
```
Create Assets & Collaterals Library for {project_name}.

For each campaign/channel, populate the following table:

COLUMNS:
- Funnel Stage
- Asset/Collateral
- Description
- Format
- Content Outline
- Content Specifications and Quality Assurance
- Contributors
- Inputs Required
- Estimated Timeframe
- Notes

CAMPAIGNS TO COVER:
1. LinkedIn Outreach (HeyReach)
2. Cold Email Outreach (Instantly)
3. LinkedIn Ads

FUNNEL STAGES PER CAMPAIGN:
- Top of Funnel
- Middle of Funnel
- Bottom of Funnel

IMPORTANT:
- Highlight the value driver (from Phase 1) as TOFU asset with different formats per channel
- Expand on ALL funnel levels for ALL channels

OUTPUT TABLE:
| Funnel Stage | Asset/Collateral | Description | Format | Content Outline | Content Specs & QA | Contributors | Inputs Required | Timeframe | Notes |
|--------------|------------------|-------------|--------|-----------------|-------------------|--------------|-----------------|-----------|-------|
| **LINKEDIN OUTREACH** | — | — | — | — | — | — | — | — | — |
| Top of Funnel | [Asset 1] | | | | | | | | |
| Top of Funnel | [Asset 2] | | | | | | | | |
| Middle of Funnel | [Asset 3] | | | | | | | | |
| Bottom of Funnel | [Asset 4] | | | | | | | | |
| **COLD EMAIL** | — | — | — | — | — | — | — | — | — |
| Top of Funnel | [Asset 1] | | | | | | | | |
| ... | | | | | | | | | |
| **LINKEDIN ADS** | — | — | — | — | — | — | — | — | — |
| Top of Funnel | [Asset 1] | | | | | | | | |
| ... | | | | | | | | | |
```

**OUTPUT FORMAT:** XLSX

---

# ═══════════════════════════════════════════════════════════════
# PHASE 9: PRICING & PACKAGING DASHBOARD
# ═══════════════════════════════════════════════════════════════

## Step 9.1: Value Metric Selection

**PROMPT:**
```
Select optimal pricing value metric using SaaS North methodology.

EVALUATE POTENTIAL DENOMINATORS:

| Denominator | Correlation to Value | Scalability | Ease of Measurement | Score (1-10) |
|-------------|---------------------|-------------|---------------------|--------------|
| /user | [Low/Med/High] | [Assessment] | [Assessment] | [Score] |
| /seat | [Low/Med/High] | [Assessment] | [Assessment] | [Score] |
| /usage (specify: ___) | [Low/Med/High] | [Assessment] | [Assessment] | [Score] |
| /outcome (specify: ___) | [Low/Med/High] | [Assessment] | [Assessment] | [Score] |
| /capability | [Low/Med/High] | [Assessment] | [Assessment] | [Score] |

RECOMMENDATION:
- Primary Value Metric: ___
- Secondary Usage Metric: ___
- Rationale: ___
```

---

## Step 9.2: Pricing Tiers

**PROMPT:**
```
Design pricing tiers using Decoy-Hero-Anchor structure.

OUTPUT TABLE:
| Plan | Price | [Primary Metric] Limit | [Secondary Metric] Limit | Position | Target % of Customers |
|------|-------|------------------------|-------------------------|----------|----------------------|
| [Tier 1 - Entry] | Free or Low | [Limit] | [Limit] | Decoy/Entry | 10-20% |
| [Tier 2 - Core] | $X/mo | [Limit] | [Limit] | Hero | 60-80% |
| [Tier 3 - Pro] | $Y/mo | [Limit] | [Limit] | Hero+ | 10-20% |
| [Tier 4 - Enterprise] | Custom | Unlimited | Unlimited | Anchor | 5-10% |

EXPANSION LEVERS (how customers upgrade):
1. ___
2. ___
3. ___
```

---

## Step 9.3: ROI Anchoring

**PROMPT:**
```
Create ROI anchoring framework.

═══════════════════════════════════════════════════════════════
ANCHOR 1: COST OF PROBLEM
═══════════════════════════════════════════════════════════════

| Problem Scenario | Cost Without Solution | Annual Subscription Cost | ROI Multiple |
|------------------|----------------------|-------------------------|--------------|
| [Scenario 1] | [Cost] | [Subscription] | [X times] |
| [Scenario 2] | [Cost] | [Subscription] | [X times] |

═══════════════════════════════════════════════════════════════
ANCHOR 2: ALTERNATIVE COMPARISON
═══════════════════════════════════════════════════════════════

| Alternative | Their Cost | Our Cost | Savings % |
|-------------|------------|----------|-----------|
| [Alt 1] | | | |
| [Alt 2] | | | |
| [Alt 3 - Manual/Status Quo] | | | |

═══════════════════════════════════════════════════════════════
ANCHOR 3: BREAKEVEN ANALYSIS
═══════════════════════════════════════════════════════════════

| Plan | Annual Cost | Value Needed to Break Even | Typical Customer Value | Payback Period |
|------|-------------|---------------------------|----------------------|----------------|
| [Tier 2] | | | | |
| [Tier 3] | | | | |

═══════════════════════════════════════════════════════════════
"ONE [OUTCOME] PAYS FOR X YEARS" CALCULATOR
═══════════════════════════════════════════════════════════════

| One [Outcome] Value | Plan | Years of Subscription Covered |
|---------------------|------|------------------------------|
| $X | [Tier 2] | [X] years |
| $X | [Tier 3] | [X] years |

MESSAGE: "One [outcome] at $[X] pays for [Y] years of [plan name]"
```

**OUTPUT FORMAT:** XLSX

---

# ═══════════════════════════════════════════════════════════════
# DELIVERABLE: LEAD MAGNET SPECIFICATION
# (Not a Dashboard - Separate Deliverable)
# ═══════════════════════════════════════════════════════════════

## Lead Magnet: Scorecard Funnel Specification

**PROMPT:**
```
Design Lead Magnet scorecard funnel for ScoreApp.com.

Reference the demand driver identified in Phase 1 (Product Feature Matrix).

═══════════════════════════════════════════════════════════════
SCORECARD OVERVIEW
═══════════════════════════════════════════════════════════════

| Element | Specification |
|---------|---------------|
| Scorecard Name | |
| Target ICP | |
| Problem it Reveals | |
| Immediate Value to User | |
| Conversion Path to {project_name} | |

═══════════════════════════════════════════════════════════════
QUESTIONS (5-7 questions)
═══════════════════════════════════════════════════════════════

| # | Question | Answer Options (4-5 options) | Scoring Logic | What It Reveals |
|---|----------|------------------------------|---------------|-----------------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

═══════════════════════════════════════════════════════════════
RESULTS TIERS
═══════════════════════════════════════════════════════════════

| Score Range | Tier Name | Message | CTA |
|-------------|-----------|---------|-----|
| 0-39 | [Low Risk/Beginner] | [Personalized message] | [Soft CTA] |
| 40-69 | [Medium Risk/Intermediate] | [Personalized message] | [Medium CTA] |
| 70-100 | [High Risk/Advanced] | [Personalized message] | [Strong CTA - Demo] |

═══════════════════════════════════════════════════════════════
POST-SCORECARD EMAIL SEQUENCE
═══════════════════════════════════════════════════════════════

| Email # | Day | Subject Line | Content Focus | CTA |
|---------|-----|--------------|---------------|-----|
| 1 | 0 | | Results delivery + interpretation | |
| 2 | 2 | | Deeper insight + case study | |
| 3 | 5 | | Solution introduction + demo offer | |
| 4 | 8 | | Final reminder + urgency | |
```

**OUTPUT FORMAT:** XLSX + DOCX (for ScoreApp implementation)

---

# ═══════════════════════════════════════════════════════════════
# FINAL OUTPUT: 10-SLIDE GTM WALKTHROUGH DECK
# ═══════════════════════════════════════════════════════════════

## Generate 10-Slide Deck

**PROMPT:**
```
You are an expert B2B SaaS Go-To-Market strategist.

Goal:
Create a 10-slide GTM Walkthrough Deck for {project_name} that only references the core dashboards and their role in the GTM workflow. This is designed to be pasted into Gamma AI or any slide generator.

Output rules:
1) Return plain Markdown only, no tables.
2) Separate slides with: ---
3) No design instructions.
4) Never use the em dash character. Use commas instead.
5) Keep content crisp, slide-ready, and specific to the project.
6) If any metric is unknown, keep it as {TBD} and do not invent numbers.

Inputs:
Project = {project_name}
Category = {category_name}
Core claim = {positioning_statement}
One-liner = {one_liner}
Top differentiators = {differentiator_1}, {differentiator_2}, {differentiator_3}
Competitors included = {competitor_list}
Positioning vectors (4) = {vector_1}, {vector_2}, {vector_3}, {vector_4}
Our lead vectors = {our_vector_1}, {our_vector_2}
ICP summary = {primary_icp_summary}
Lead magnet = {lead_magnet_name}
Pricing summary = {pricing_model_summary}
Customer journey summary = {customer_journey_summary}
Assets library summary = {assets_library_summary}

Slide structure, must be exactly 10 slides:

1) Title, what the dashboard suite is for
2) Product Feature Matrix Dashboard, what we learned and what we lead with
3) Competitive Market Analysis Dashboard, competitor map and buying context
4) Positioning Dashboard, 4 vectors, current state vs projected state
5) ICP Dashboard, who we win first, and why
6) Buying Committee Dashboard, personas, blockers, drivers
7) Customer Journey Funnel Dashboard, stage progression and internal KPIs
8) Lead Magnet, scorecard funnel, what it reveals and why it converts
9) Assets and Collaterals Library Dashboard, channel coverage and TOFU to BOFU flow
10) Pricing and Packaging Dashboard, value metric, usage metric, tiers, expansion levers

Slide writing rules:
- Each slide starts with: "# SLIDE X, {Title}"
- Then 4 to 6 bullets max
- Each slide must include a short "So what" bullet tying the dashboard to customer acquisition
- Use the provided inputs only, do not add new dashboards
- Do not include roadmap, measurement plans, or additional strategy pages beyond the dashboards

Now generate the 10 slides in Markdown.
Use "---" as the separator between slides.
```

**OUTPUT FORMAT:** MD (for Gamma AI)

---

# ═══════════════════════════════════════════════════════════════
# CALLABLE FORMAT TEMPLATES
# ═══════════════════════════════════════════════════════════════

When user says "use [TEMPLATE_NAME]", apply these formats immediately:

---

### TEMPLATE: COMPETITOR_TABLE
```
| Attribute | {project} | {comp_1} | {comp_2} | {comp_3} | {comp_4} | {comp_5} |
|-----------|-----------|----------|----------|----------|----------|----------|
| Website | | | | | | |
| Tagline | | | | | | |
| Sub Tag | | | | | | |
| Description | | | | | | |
| Strengths | | | | | | |
| Weaknesses | | | | | | |
```

---

### TEMPLATE: FEATURE_SCORING
```
| Feature | Demand (Wanted by...) | Competitiveness | Demand Score (-20 to +20) | Comp Score (-20 to +20) | Quadrant |
|---------|----------------------|-----------------|---------------------------|-------------------------|----------|
```

---

### TEMPLATE: POSITIONING_VECTORS
```
| Positioning Vector | {project} | {comp_1} | {comp_2} | {comp_3} | {comp_4} | {comp_5} |
|--------------------|-----------|----------|----------|----------|----------|----------|
| [Vector 1 - They Lead] | | | | | | |
| [Vector 2 - They Lead] | | | | | | |
| [Vector 3 - We Lead] | | | | | | |
| [Vector 4 - We Lead] | | | | | | |
```

---

### TEMPLATE: ICP_TABLE
```
| Attribute | ICP Level 1 (MVP-PMF) | ICP Level 2 (Growth) |
|-----------|----------------------|---------------------|
| Segment | | |
| Sub-industries | | |
| Location | | |
| Revenue, $ | | |
| Team Size | | |
| Business Maturity | | |
| Business Model | | |
| Best Engagement Model | | |
| Organization Challenges and Pain Points | | |
| Why Should They Choose Us | | |
| Strategic Goals | | |
| Triggers | | |
```

---

### TEMPLATE: PERSONA_TABLE
```
| Attribute | User | Manager | Decision Maker |
|-----------|------|---------|----------------|
| Possible Job Titles | | | |
| Responsibility Area | | | |
| Purchasing Influence | | | |
| Core Customer Journey Stages | | | |
| Potential Reasons to Block | | | |
| Drivers | | | |
| Assets to Get Buy-In | | | |
| Channels to Find Them | | | |
```

---

### TEMPLATE: DESIGN_PARTNER
```
| Attribute | Specification |
|-----------|---------------|
| Design Partner Attributes | |
| Job Titles | |
| Demographics | |
| Responsibility Areas | |
| Current Tools | |
| Key Pain Points | |
| Critical Triggers | |
| Goals & Motivations | |
| Decision Criteria | |
| Influence Level | |
| Barriers to Purchase | |
| Information Sources | |
| Success Metrics | |
| Early Adopter Characteristics | |
```

---

### TEMPLATE: VALUE_PROP_PILLARS
```
| Value Prop | Description | RTB #1 | RTB #2 | RTB #3 |
|------------|-------------|--------|--------|--------|
| VP 1 | | | | |
| VP 2 | | | | |
| VP 3 | | | | |
```

---

### TEMPLATE: COPY_DRILL
```
| Element | Content |
|---------|---------|
| Reason to Believe | |
| Headline (Rational) | |
| Headline (Emotional) | |
| Headline (Social Proof) | |
| Subhead | |
| Body Copy (25 words) | |
| CTA | |
| Supporting Proof Point | |
```

---

### TEMPLATE: JOURNEY_TABLE
```
| Funnel Stage | Buyer Mindset & Trigger | Key Questions | Touch-points & Assets | Internal KPIs | Desired Outcome | Function |
|--------------|------------------------|---------------|----------------------|---------------|-----------------|----------|
| 1. Problem Awareness | | | | | | Marketing |
| 2. Solution Discovery | | | | | | Marketing/Sales |
| 3. Vendor Evaluation | | | | | | Sales |
| 4. Trial/Purchase | | | | | | Sales/CS |
| 5. Value Realization | | | | | | CS |
| 6. Expansion & Advocacy | | | | | | CS/Marketing |
| 7. Renewal & Loyalty | | | | | | CS/Product |
```

---

### TEMPLATE: SCORECARD_SPEC
```
| Element | Specification |
|---------|---------------|
| Scorecard Name | |
| Target ICP | |
| Problem it Reveals | |
| Immediate Value | |
| Conversion Path | |
```

---

### TEMPLATE: ASSETS_TABLE
```
| Funnel Stage | Asset/Collateral | Description | Format | Content Outline | Content Specs & QA | Contributors | Inputs Required | Timeframe | Notes |
|--------------|------------------|-------------|--------|-----------------|-------------------|--------------|-----------------|-----------|-------|
```

---

### TEMPLATE: PRICING_TIERS
```
| Plan | Price | Primary Metric Limit | Secondary Metric Limit | Position | Target % |
|------|-------|---------------------|----------------------|----------|----------|
| Entry | | | | Decoy | 10-20% |
| Core | | | | Hero | 60-80% |
| Pro | | | | Hero+ | 10-20% |
| Enterprise | Custom | Unlimited | Unlimited | Anchor | 5-10% |
```

---

### TEMPLATE: ROI_ANCHOR
```
| Scenario | Cost Without Solution | Subscription Cost | ROI Multiple |
|----------|----------------------|-------------------|--------------|
```

---

# ═══════════════════════════════════════════════════════════════
# EXECUTION CHECKLIST
# ═══════════════════════════════════════════════════════════════

```
GTM BUILD PROGRESS TRACKER:

□ PHASE 1: Product Feature Matrix Dashboard
  ⚠️ 1.1 Research scope (USER EXECUTES EXTERNALLY)
  □ 1.2 Demand & Competitiveness analysis
  □ 1.3 Scatter plot scoring (with decimals)
  □ 1.4 Quadrant assignment (two tables)
  □ 1.5 Entry validation rules
  □ 1.6 Demand driver identification
  □ 1.7 Demand driver variants
  → OUTPUT: product_feature_matrix.xlsx

□ PHASE 2: Competitive Market Analysis Dashboard
  ⚠️ 2.1 Research scope (USER EXECUTES EXTERNALLY)
  □ 2.2 Competitor summary table
  □ 2.3 Core offering vectors (one-word bullets)
  □ 2.4 Target audience extraction
  □ 2.5 Value proposition extraction
  □ 2.6 Feature extraction (per company)
  ⚠️ 2.7 G2 reviews analysis (USER EXECUTES EXTERNALLY)
  □ 2.8 Positioning vectors (4 vectors, scored)
  □ 2.9 Feature consolidation
  □ 2.10 Feature presence table (✓/✗)
  □ 2.11 Features to benefits
  □ 2.12 Benefits potency (1-5 stars)
  □ 2.13 Competitive advantage (3-4 words)
  □ 2.14 Competitive advantage explanation
  □ 2.15 Category summary (4 blocks)
  □ 2.16 Positioning summary (2 paragraphs)
  → OUTPUT: competitive_analysis.xlsx, positioning_summary.docx

□ PHASE 3: Positioning Dashboard
  □ 3.1 Positioning statements (3 statements)
  → OUTPUT: positioning_statements.docx

□ PHASE 4: ICP Dashboard
  □ 4.1 Two-level ICP definition
  → OUTPUT: icp_dashboard.xlsx

□ PHASE 5: Buying Committee Dashboard
  □ 5.1 Purchasing committee personas (2 ICPs × 3 personas)
  □ 5.2 Design partner profile
  → OUTPUT: buying_committee.xlsx

□ PHASE 6: Value Proposition Dashboard
  □ 6.1 Brand promise & positioning
  □ 6.2 Value proposition pillars (1 table)
  □ 6.3 Copy drills (9 tables)
  → OUTPUT: value_proposition.docx

□ PHASE 7: Customer Journey Funnel Dashboard
  □ 7.1 Full funnel mapping (7 stages)
  □ 7.2 Key journey insights
  → OUTPUT: customer_journey.xlsx

□ PHASE 8: Assets & Collaterals Library Dashboard
  □ 8.1 Full-funnel asset mapping (3 channels)
  → OUTPUT: assets_library.xlsx

□ PHASE 9: Pricing & Packaging Dashboard
  □ 9.1 Value metric selection
  □ 9.2 Pricing tiers
  □ 9.3 ROI anchoring
  → OUTPUT: pricing_dashboard.xlsx

□ DELIVERABLE: Lead Magnet Specification
  □ Scorecard overview
  □ Questions (5-7)
  □ Results tiers
  □ Post-scorecard email sequence
  → OUTPUT: lead_magnet_spec.xlsx, scorecard_spec.docx

□ FINAL: 10-Slide GTM Walkthrough Deck
  □ Generate 10 slides
  → OUTPUT: gtm_walkthrough.md (for Gamma AI)
```

---

# ═══════════════════════════════════════════════════════════════
# QUICK START
# ═══════════════════════════════════════════════════════════════

When user wants to build GTM, use this opening:

```
I'll help you build a complete 9-dashboard GTM strategy for your B2B SaaS product.

Before we start, please provide:

1. **Project:** Name + Website URL + One-liner description
2. **Category:** What market category are you in? What's your niche focus?
3. **Competitors:** List 5-6 main competitors with their websites
4. **Features:** List your key product features (5-10)

Once provided, we'll build these dashboards in sequence:

1. Product Feature Matrix Dashboard ⚠️ (requires external research)
2. Competitive Market Analysis Dashboard ⚠️ (requires external research)
3. Positioning Dashboard
4. ICP Dashboard
5. Buying Committee Dashboard
6. Value Proposition Dashboard
7. Customer Journey Funnel Dashboard
8. Assets & Collaterals Library Dashboard
9. Pricing & Packaging Dashboard
+ Lead Magnet Specification (ScoreApp scorecard)
→ Final: 10-slide GTM Walkthrough Deck

NOTE: Three steps require you to execute external research (I'll provide the scope).

Ready when you are.
```

---

# ═══════════════════════════════════════════════════════════════
# SKILL METADATA
# ═══════════════════════════════════════════════════════════════

- **Version:** 3.1
- **Last Updated:** March 2026
- **Dashboards:** 9
- **Additional Deliverables:** Lead Magnet Spec, GTM Walkthrough Deck
- **External Research Steps:** 3 (Product Feature Matrix @ 1.1, Competitor Crawl @ 2.1, G2 Reviews @ 2.7)
- **Output Files:** 7 XLSX, 4 DOCX, 1 MD
- **Callable Templates:** 13 format templates
- **Estimated Execution Time:** 5-6 hours across multiple sessions
- **Recommended Session Structure:** Complete one phase per session with user review
