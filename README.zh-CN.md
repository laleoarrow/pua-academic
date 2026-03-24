# pua-academic

### 学术压力引擎 — 让 AI 像赶 Deadline 一样努力

一个 AI Coding Agent 技能插件，使用学术研究压力话术（Deadline、同行评审、导师反馈、发表压力）驱动 AI 穷尽所有方案才允许放弃。支持 **Claude Code**、**OpenAI Codex CLI**、**Cursor** 等平台。

<p>
  <img src="https://img.shields.io/badge/Claude_Code-black?style=flat-square&logo=anthropic&logoColor=white" alt="Claude Code">
  <img src="https://img.shields.io/badge/OpenAI_Codex_CLI-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI Codex CLI">
  <img src="https://img.shields.io/badge/Cursor-000?style=flat-square&logo=cursor&logoColor=white" alt="Cursor">
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="MIT License">
</p>

## 什么是 pua-academic？

与原版 **pua** 使用大厂 PUA 话术（阿里 361、字节、PIP）不同，**pua-academic** 使用学术研究压力来激励 AI：

- **Deadline 压力**："论文投稿截止就是明天。必须搞定。"
- **同行评审**："审稿人 #2 不会接受这个方案。找更严谨的方法。"
- **导师反馈**："你的导师期望看到更好的方法论。展示完整的分析。"
- **发表压力**："这需要达到会议论文级别的质量。"

## 核心特性

1. **学术话术** — 让 AI 不敢提交不完整的工作
2. **严谨方法论** — 赋予 AI 产出发表级质量的能力
3. **自审机制** — AI 声称完成前必须自我审查

## 安装

### Claude Code

```bash
# 手动安装
git clone https://github.com/tanweai/pua-academic.git ~/.claude/plugins/pua-academic
```

### OpenAI Codex CLI

```bash
mkdir -p ~/.codex/skills/pua-academic
curl -o ~/.codex/skills/pua-academic/SKILL.md \
  https://raw.githubusercontent.com/tanweai/pua-academic/main/codex/pua-academic/SKILL.md
```

### Cursor

```bash
mkdir -p .cursor/rules
curl -o .cursor/rules/pua-academic.mdc \
  https://raw.githubusercontent.com/tanweai/pua-academic/main/cursor/rules/pua-academic.mdc
```

## 快速开始

1. 使用上述方法之一安装技能
2. 技能会在以下情况自动激活：
   - 任务连续失败 2 次以上
   - AI 即将放弃
   - 用户表达沮丧
3. 或手动触发：输入 `/pua-academic`

## 与原版 PUA 的区别

| 方面 | PUA（原版） | PUA-Academic |
|------|------------|--------------|
| 话术风格 | 大厂 PUA（阿里、PIP） | 学术压力（Deadline、同行评审） |
| 压力升级 | L1-L4 企业级别 | 研究里程碑阶段 |
| 关键短语 | "3.25"、"毕业"、"PIP" | "Deadline"、"审稿人 #2"、"导师" |
| 目标场景 | 调试、实现 | 研究、分析、文档 |
| 语气 | 企业压力 | 学术严谨 |

## 使用场景

- **使用 PUA（原版）**：调试、代码实现、部署问题
- **使用 PUA-Academic**：研究任务、文献综述、文档撰写、分析报告

## License

MIT
