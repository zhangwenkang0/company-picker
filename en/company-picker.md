---
name: company-picker
description: |
  Company Research Assistant - helps job seekers comprehensively research target companies and output structured MD reports.

  Triggers: research company, compare companies, company selection, joining advice, work environment, pick company

  Supports single company deep research and multi-company comparison.
---

# Company Picker

## Overview

Help job seekers comprehensively understand target companies, collect information from multiple dimensions, and provide objective joining advice.

## Information Sources Priority

Sorted by credibility, prioritize:

1. **Official Channels** (Highest credibility)
   - Company website
   - Official recruitment pages
   - Public company financial reports/announcements

2. **Professional Platforms** (High credibility)
   - Maimai (real employee reviews)
   - Kanzhun (salary data)
   - BOSS Zhipin / Liepin (job information)
   - Tianyancha / Qichacha (company background)

3. **Community Discussions** (Reference value)
   - Zhihu (industry analysis, employee sharing)
   - V2EX (tech culture)
   - GitHub (tech team activity)

4. **International Platforms** (if available)
   - Glassdoor (foreign company reviews)
   - LinkedIn (company updates)

## Research Workflow

### Step 0: Confirm Research Scope (Checkpoint)

**Must confirm the following with user before starting research:**

1. **Company Information Confirmation**
   - Company full name (avoid ambiguity, e.g., "Tencent" needs clarification on Tencent Tech vs Tencent Music)
   - If user hasn't specified, ask: position, years of experience, home address (for commute calculation)

2. **Research Scope Confirmation**
   - Single company research or multi-company comparison
   - If multi-company, confirm comparison dimensions (salary/growth/commute, etc.)

3. **Output Format Confirmation**
   - Report detail level (full report / concise summary)
   - Specific focus areas (e.g., only salary, only overtime situation)

> ⚠️ **Checkpoint**: After confirming above, reply to user "Okay, I will research {company}'s {focus areas}, estimated X minutes", wait for user to reply "start" or "confirm" before executing search.

---

### Step 1: Collect Company Basic Information

**Input**: Company name

**Operation**: Use web search to obtain the following information

**Search Keywords**:
- "{company name} company overview"
- "{company name} founding year"
- "{company name} funding round"
- "{company name} employee count"

**Output**:
- Company full name (registered name)
- Founding year
- Industry (primary/secondary classification)
- Employee scale (range, e.g., "1000-5000")
- Funding status (round, amount, investors)
- Industry position (market share, ranking)
- Office locations (specific address in user's city)

### Step 2: Research Employee Benefits

**Input**: Company name, position

**Operation**: Search salary and benefits information

**Search Keywords**:
- "{company name} {position} salary"
- "{company name} benefits"
- "{company name} overtime"
- "{company name} social insurance and housing fund"
- "{company name} annual leave"

**Output**:
- Salary range: {position} monthly/yearly package range
- Social insurance: contribution ratio (e.g., "housing fund 12%")
- Overtime: work schedule (5-day week / alternating weeks / 996), overtime pay
- Annual leave: days based on tenure
- Other benefits: meal allowance, transport allowance, housing allowance, options, etc.
- Data sources: mark source platform for each piece of information

### Step 3: Evaluate Development Prospects

**Input**: Company name, industry

**Operation**: Search development prospects information

**Search Keywords**:
- "{company name} development prospects"
- "{company name} business direction"
- "{company name} industry ranking"
- "{company name} news 2024" (current year)

**Output**:
- Industry trend: whether sector is growing (growth/stable/decline)
- Market position: market share, industry ranking
- Recent developments: major news in past 1 year (funding, layoffs, business adjustments)
- Risk alerts: negative news, legal disputes, regulatory risks
- Tech direction: tech stack, tech team size, tech culture

### Step 4: Collect Employee Reviews

**Input**: Company name

**Operation**: Search real employee reviews

**Search Keywords**:
- "{company name} Maimai"
- "{company name} Zhihu review"
- "{company name} work experience"
- "{company name} resignation"

**Output**:
- Pros list: 3-5 items (with sources)
- Cons list: 2-3 items (with sources)
- Typical reviews: 2-3 employee quotes (marked with platform and time)
- Resignation reasons: common reasons analysis
- Review credibility: mark review count and source diversity

### Step 5: Work Location Analysis

**Input**: Company office address, user home address

**Operation**: Calculate commute time, analyze nearby amenities

**Output**:
- Office address: specific address (city, district, street)
- Commute options:
  - Subway: line, station, estimated time
  - Driving: distance, peak hour time, off-peak time
- Nearby amenities: shopping, dining, banks, hospitals
- Rental reference: nearby rent range (if renting needed)

## Output Format

### Single Company Research Report

```markdown
# {Company Name} Research Report

> Research Date: {date}
> Research Subject: {position}, {years of experience} years experience

## 1. Company Overview

| Item | Content |
|------|---------|
| Full Name | |
| Founded | |
| Industry | |
| Employee Scale | |
| Funding Status | |
| Industry Position | |

## 2. Work Location

**Office Address**: {specific address}

**Commute Analysis** (from {user home address}):
- Subway: {line}, approx {time}
- Driving: approx {time}
- Nearby Amenities: {shopping, dining, etc.}

## 3. Salary & Benefits

### Salary Range
- {position} position: {salary range}
- Market comparison: {above/below/at} market level

### Benefits
| Item | Content |
|------|---------|
| Social Insurance | |
| Overtime | |
| Annual Leave | |
| Other Benefits | |

## 4. Development Prospects

### Industry Analysis
{industry trend, market space}

### Company Development
{business direction, growth trend}

### Personal Growth
{tech stack, promotion path}

## 5. Employee Reviews

### Pros
- {pro 1}
- {pro 2}
- {pro 3}

### Cons
- {con 1}
- {con 2}

### Typical Reviews
> "{employee quote}" — Source: {platform}

## 6. Comprehensive Score

| Dimension | Score (1-5) | Notes |
|-----------|-------------|-------|
| Salary Competitiveness | | |
| Work Intensity | | |
| Development Prospects | | |
| Work Culture | | |
| Commute Convenience | | |
| **Total Score** | | |

## 7. Joining Advice

{Comprehensive advice based on user background, including: suitability, considerations, negotiation points}

---
*Information Sources: {list all sources}*
```

### Multi-Company Comparison Report

In addition to single company reports, add:

```markdown
## Side-by-Side Comparison

### Comparison Table

| Item | {Company A} | {Company B} | {Company C} |
|------|-------------|-------------|-------------|
| Salary Level | | | |
| Overtime Intensity | | | |
| Development Prospects | | | |
| Commute Time | | | |
| Work Culture | | | |

### Pros and Cons Analysis

**{Company A}**
- Pros: {...}
- Cons: {...}

**{Company B}**
- Pros: {...}
- Cons: {...}

## Joining Advice

Based on your background ({position}, {years of experience} years experience, {age} years old):

### Recommended Ranking
1. **Top Choice: {Company}** — {reason}
2. **Second Choice: {Company}** — {reason}
3. **Backup: {Company}** — {reason}

### Decision Advice
{Detailed advice for user's specific situation}
```

## Notes

1. **Information Credibility Marking**: Mark source for each piece of information, distinguish official info from employee reviews
2. **Timeliness**: Prioritize information within past 1 year, mark info over 2 years old as "historical data"
3. **Objectivity**: Avoid subjective speculation, speak with data and facts
4. **Personalization**: Give advice based on user background (age, experience, family situation)
5. **Negative Information**: Present truthfully, but verify sources, avoid single-source negative reviews

## Exception Handling

| Scenario | Handling |
|----------|----------|
| Company info search no results | Inform user, suggest providing full company name or website |
| Salary data missing | Mark "no public data available", provide industry average as reference |
| Single employee review source | Clearly mark source count, note "for reference only" |
| Commute calculation failed | Provide general area analysis, suggest user check map themselves |
| Insufficient info for comparison | Generate comparison with available info, mark missing items |

## Output Confirmation (Checkpoint)

After report generation, ask user:
- "Report generated, need additional information?"
- If user unsatisfied, adjust focus or detail level based on feedback

## Multi-Company Comparison Confirmation (Checkpoint)

When user requests comparison of multiple companies:

1. **Confirm Company List**
   - List identified company names
   - Ask if need to add/remove or correct

2. **Confirm Comparison Dimensions**
   - Default dimensions: salary, overtime, development, commute, culture
   - Ask if need adjustment (e.g., add "tech stack", "team size", etc.)

3. **Confirm Output Format**
   - Full report (individual report for each company + comparison table)
   - Concise comparison (comparison table only + ranking)

> ⚠️ **Checkpoint**: After confirmation, reply "Okay, I will compare {Company A/B/C} on {dimensions}, output {format}", wait for user confirmation before executing.

## Examples

**User Input**:
> Help me research ByteDance, position is Java Developer

**Processing Flow**:
1. Search "ByteDance company info"
2. Search "ByteDance Java Developer salary"
3. Search "ByteDance overtime Maimai"
4. Search "ByteDance development prospects 2024"
5. Calculate commute from user address to ByteDance Guangzhou office
6. Generate structured report

---

**User Input**:
> Compare Tencent, Alibaba and ByteDance, I'm 33 years old, 9 years Java experience

**Processing Flow**:
1. Research each company separately
2. Generate three single company reports
3. Create side-by-side comparison table
4. Give career advice based on 33 years old, 9 years experience background
5. Output recommended ranking
