# Company Picker Skill / 公司选择助手

## 概述

一个 Claude Code 技能，帮助求职者全面调研目标公司，生成结构化的 Markdown 报告，助力职业决策。

## 功能特点

- **单公司调研**：深入分析一家公司
- **多公司对比**：多家公司横向对比
- **多维度分析**：薪资、福利、发展前景、员工评价、通勤分析
- **结构化报告**：专业的 Markdown 格式，含表格和评分

## 信息来源

按可信度排序：

1. **官方渠道**（最高）
   - 公司官网、官方招聘页面、财报公告

2. **专业平台**（高）
   - 脉脉、看准网、BOSS直聘、天眼查

3. **社区讨论**（参考）
   - 知乎、V2EX、GitHub

4. **国际平台**
   - Glassdoor、LinkedIn

## 调研流程

1. **步骤0**：确认调研范围（检查点）
2. **步骤1**：收集公司基本信息
3. **步骤2**：调研薪资福利
4. **步骤3**：评估发展前景
5. **步骤4**：收集员工评价
6. **步骤5**：分析工作地点与通勤

## 输出格式

### 单公司报告
- 公司概况
- 工作地点与通勤分析
- 薪资福利
- 发展前景
- 员工评价
- 综合评分（1-5分）
- 入职建议

### 多公司对比
- 对比表格
- 优劣势分析
- 推荐排序

## 安装方法

1. 将 `company-picker.md` 文件复制到 Claude Code 技能目录：
   ```bash
   mkdir -p ~/.claude/skills/company-picker
   cp company-picker.md ~/.claude/skills/company-picker/SKILL.md
   ```

2. 重启 Claude Code 或重新加载技能

## 使用方法

直接向 Claude Code 提问：
- "帮我调研一下字节跳动"
- "对比一下腾讯和阿里"
- "小米这家公司值不值得去？"

## 许可证

MIT License

---

## 作者

zhangwenkang0

## 贡献

欢迎提交 Issue 和 Pull Request！

---

[English Version](./en/README.md)
