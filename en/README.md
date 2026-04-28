# Company Picker Skill

## Overview

A Claude Code skill that helps job seekers comprehensively research target companies and generate structured markdown reports for informed career decisions.

## Features

- **Single Company Research**: Deep dive into one company with detailed analysis
- **Multi-Company Comparison**: Side-by-side comparison of multiple companies
- **Multi-dimensional Analysis**: Salary, benefits, development prospects, employee reviews, commute analysis
- **Structured Reports**: Professional markdown format with tables and ratings

## Information Sources

Priority by credibility:

1. **Official Channels** (Highest)
   - Company website, official recruitment pages, financial reports

2. **Professional Platforms** (High)
   - Maimai, Kanzhun, BOSS Zhipin, Tianyancha

3. **Community Discussions** (Reference)
   - Zhihu, V2EX, GitHub

4. **International Platforms**
   - Glassdoor, LinkedIn

## Research Workflow

1. **Step 0**: Confirm research scope (checkpoint)
2. **Step 1**: Collect company basic information
3. **Step 2**: Research salary and benefits
4. **Step 3**: Evaluate development prospects
5. **Step 4**: Collect employee reviews
6. **Step 5**: Analyze work location and commute

## Output Format

### Single Company Report
- Company overview
- Work location & commute analysis
- Salary & benefits
- Development prospects
- Employee reviews
- Comprehensive scoring (1-5 scale)
- Joining recommendations

### Multi-Company Comparison
- Comparison table
- Pros/cons analysis
- Recommended ranking

## Installation

1. Copy the `company-picker.md` file to your Claude Code skills directory:
   ```bash
   mkdir -p ~/.claude/skills/company-picker
   cp company-picker.md ~/.claude/skills/company-picker/SKILL.md
   ```

2. Restart Claude Code or reload skills

## Usage

Simply ask Claude Code:
- "Help me research ByteDance"
- "Compare Tencent and Alibaba"
- "Is Xiaomi worth joining?"

## License

MIT License

---

## Author

zhangwenkang0

## Contributing

Issues and Pull Requests are welcome!

---

[中文版本](../README.md)
