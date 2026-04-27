# Company Picker Skill / 公司选择助手

[English](#english) | [中文](#中文)

---

<a name="english"></a>
## English

### Overview

A Claude Code skill that helps job seekers comprehensively research target companies and generate structured markdown reports for informed career decisions.

### Features

- **Single Company Research**: Deep dive into one company with detailed analysis
- **Multi-Company Comparison**: Side-by-side comparison of multiple companies
- **Multi-dimensional Analysis**: Salary, benefits, development prospects, employee reviews, commute analysis
- **Structured Reports**: Professional markdown format with tables and ratings

### Information Sources

Priority by credibility:

1. **Official Channels** (Highest)
   - Company website, official recruitment pages, financial reports

2. **Professional Platforms** (High)
   - Maimai, Kanzhun, BOSS Zhipin, Tianyancha

3. **Community Discussions** (Reference)
   - Zhihu, V2EX, GitHub

4. **International Platforms**
   - Glassdoor, LinkedIn

### Research Workflow

1. **Step 0**: Confirm research scope (checkpoint)
2. **Step 1**: Collect company basic information
3. **Step 2**: Research salary and benefits
4. **Step 3**: Evaluate development prospects
5. **Step 4**: Collect employee reviews
6. **Step 5**: Analyze work location and commute

### Output Format

#### Single Company Report
- Company overview
- Work location & commute analysis
- Salary & benefits
- Development prospects
- Employee reviews
- Comprehensive scoring (1-5 scale)
- Joining recommendations

#### Multi-Company Comparison
- Comparison table
- Pros/cons analysis
- Recommended ranking

### Installation

1. Copy the `company-picker.md` file to your Claude Code skills directory:
   ```bash
   mkdir -p ~/.claude/skills/company-picker
   cp company-picker.md ~/.claude/skills/company-picker/SKILL.md
   ```

2. Restart Claude Code or reload skills

### Usage

Simply ask Claude Code:
- "Help me research ByteDance"
- "Compare Tencent and Alibaba"
- "Is Xiaomi worth joining?"

### License

MIT License

---

<a name="中文"></a>
## 中文

### 概述

一个 Claude Code 技能，帮助求职者全面调研目标公司，生成结构化的 Markdown 报告，助力职业决策。

### 功能特点

- **单公司调研**：深入分析一家公司
- **多公司对比**：多家公司横向对比
- **多维度分析**：薪资、福利、发展前景、员工评价、通勤分析
- **结构化报告**：专业的 Markdown 格式，含表格和评分

### 信息来源

按可信度排序：

1. **官方渠道**（最高）
   - 公司官网、官方招聘页面、财报公告

2. **专业平台**（高）
   - 脉脉、看准网、BOSS直聘、天眼查

3. **社区讨论**（参考）
   - 知乎、V2EX、GitHub

4. **国际平台**
   - Glassdoor、LinkedIn

### 调研流程

1. **步骤0**：确认调研范围（检查点）
2. **步骤1**：收集公司基本信息
3. **步骤2**：调研薪资福利
4. **步骤3**：评估发展前景
5. **步骤4**：收集员工评价
6. **步骤5**：分析工作地点与通勤

### 输出格式

#### 单公司报告
- 公司概况
- 工作地点与通勤分析
- 薪资福利
- 发展前景
- 员工评价
- 综合评分（1-5分）
- 入职建议

#### 多公司对比
- 对比表格
- 优劣势分析
- 推荐排序

### 安装方法

1. 将 `company-picker.md` 文件复制到 Claude Code 技能目录：
   ```bash
   mkdir -p ~/.claude/skills/company-picker
   cp company-picker.md ~/.claude/skills/company-picker/SKILL.md
   ```

2. 重启 Claude Code 或重新加载技能

### 使用方法

直接向 Claude Code 提问：
- "帮我调研一下字节跳动"
- "对比一下腾讯和阿里"
- "小米这家公司值不值得去？"

### 许可证

MIT License

---

## Author / 作者

zhangwenkang0

## Contributing / 贡献

Issues and Pull Requests are welcome!

欢迎提交 Issue 和 Pull Request！
