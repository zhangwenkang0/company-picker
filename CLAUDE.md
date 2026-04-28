# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Claude Code skill project called **company-picker**. It helps job seekers research target companies and generate structured markdown reports for career decisions.

## Project Structure

- `company-picker.md` - The main skill definition file (SKILL.md format)
- `README.md` - Bilingual documentation (English/Chinese)

## Skill Installation

To install this skill locally:

```bash
mkdir -p ~/.claude/skills/company-picker
cp company-picker.md ~/.claude/skills/company-picker/SKILL.md
```

## Skill Workflow

The skill follows a structured research process:

1. **Step 0**: Confirm research scope with user (checkpoint)
2. **Step 1**: Collect company basic information
3. **Step 2**: Research salary and benefits
4. **Step 3**: Evaluate development prospects
5. **Step 4**: Collect employee reviews
6. **Step 5**: Analyze work location and commute

## Information Sources Priority

1. Official channels (company website, financial reports)
2. Professional platforms (Maimai, Kanzhun, BOSS Zhipin, Tianyancha)
3. Community discussions (Zhihu, V2EX, GitHub)
4. International platforms (Glassdoor, LinkedIn)

## Output Formats

- **Single Company Report**: Company overview, salary/benefits, development prospects, employee reviews, scoring (1-5), joining recommendations
- **Multi-Company Comparison**: Comparison table, pros/cons analysis, recommended ranking

## Making Changes

When modifying the skill:
- Edit `company-picker.md` directly
- Update `README.md` if workflow or features change
- Maintain bilingual support in README.md
