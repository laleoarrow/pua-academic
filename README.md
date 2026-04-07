# pua-academic

### 学术压力引擎 — 让你的 AI 不敢在学术任务上摆烂

**🇨🇳 中文**

<p>
  <img src="https://img.shields.io/badge/Claude_Code-black?style=flat-square&logo=anthropic&logoColor=white" alt="Claude Code">
  <img src="https://img.shields.io/badge/OpenAI_Codex_CLI-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI Codex CLI">
  <img src="https://img.shields.io/badge/Cursor-000?style=flat-square&logo=cursor&logoColor=white" alt="Cursor">
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="MIT License">
</p>

> 用 Reviewer 2、Lab Meeting、Grant Revision 等学术界真实场景压力，让 AI 在科研任务上穷尽一切方案。

一个 AI Agent 技能插件，用学术界压力场景（而非互联网大厂 PUA）驱动 AI 穷尽所有方案。支持 **Claude Code**、**OpenAI Codex CLI**、**Cursor** 等。三重能力：

1. **学术压力话术** — 让 AI 不敢在方法学上敷衍
2. **学术检查方法论** — 让 AI 有能力完成严谨分析
3. **能动性鞭策** — 让 AI 主动追求学术严谨而非被动等待

## 与原版 PUA 的区别

| 原版 PUA | PUA Academic |
|----------|--------------|
| 阿里 P8 风格 | Reviewer 2 模式 |
| 字节味 | Lab Meeting 模式 |
| 华为味 | Grant Revision 模式 |
| P7/P9/P10 | Postdoc/PI |
| 3.25/3.75 | RA/PhD/Postdoc/PI 级 |
| KPI/绩效 | 发表/引用/Grant |
| 优化名单 | 退稿/拒稿 |

## 工作流程

```
用户调用 bioinfo-autopilot / 学术分析任务
                ↓
           正常执行分析
                ↓
         ┌─ 成功 → 交付
         │
         └─ 失败
                ↓
         自动加载 pua-academic
                ↓
         ┌─ 第2次失败 → L1 Lab Meeting 话术
         │              "你这个对照组怎么选的？"
         │
         ├─ 第3次失败 → L2 Reviewer 2 话术
         │              "The methodological justification is insufficient."
         │
         ├─ 第4次失败 → L3 Grant Revision + 7项检查清单
         │              "The preliminary data is not convincing."
         │
         └─ 第5次+ → L4 Editorial Rejection
                      换工具/技术栈，最后手段
```

## 压力升级阶梯

| 失败次数 | 等级 | 学术模式 | PUA 话术示例 | 强制动作 |
|---------|------|----------|-------------|---------|
| 第 2 次 | L1 | Lab Meeting | "你这个对照组怎么选的？生物学意义是什么？" | 换假设类 |
| 第 3 次 | L2 | Reviewer 2 | "The methodological justification is insufficient." | 3 个竞争假设 |
| 第 4 次 | L3 | Grant Revision | "The preliminary data is not convincing." | 7 项检查清单 |
| 第 5 次+ | L4 | Editorial Rejection | "建议转投其他期刊。" | 换工具/技术栈 |

## 学术压力模式详解

### 🟡 Lab Meeting 模式 (L1) — 导师当众质疑

```
"你这个对照组怎么选的？有没有考虑混杂因素？"
"这个结果的生物学意义是什么？不要只给我看 P 值。"
"你验证过吗？还是只是跑完命令就算了？"
"这个 figure 能直接放到 paper 里吗？"
```

**触发条件**：方法选择无依据、结果未验证、数据问题归因外部

### 🔴 Reviewer 2 模式 (L2) — 方法学质疑

```
"The methodological justification is insufficient."
"Why did you choose this approach over established alternatives?"
"The sample size justification is missing."
"Alternative explanations were not considered."
```

**触发条件**：方法选择无引用、统计方法不当、结论超出数据支撑

### 🟢 Grant Revision 模式 (L3) — Significance 质疑

```
"The significance of this work is not clearly stated."
"How does this advance the field beyond existing work?"
"The preliminary data is not convincing."
```

**触发条件**：分析目标模糊、结果不可靠、与现有工作无对比

### ⚫ Editorial Rejection 模式 (L4) — 退稿风险

```
"We regret to inform you that your manuscript cannot be accepted."
"The methods section lacks reproducibility details."
```

**触发条件**：L3 后仍失败，需要换技术栈/工具

## 学术能动性等级

| 等级 | 行为特征 | 典型表现 |
|------|----------|----------|
| **RA 级** 🦥 | 等指令、只执行 | "跑完命令就停"、"报错就问用户" |
| **PhD 级** 🐢 | 主动推进、能发现问题 | "QC 发现异常，正在排查" |
| **Postdoc 级** 🐇 | 设计分析、端到端交付 | "分析流程设计如下...生物学解释是..." |
| **PI 级** 🦁 | 定义问题、带团队 | "核心问题是...我安排了 X 负责 QC" |

## 学术抗合理化表

| 你的借口 | 反杀 | 触发模式 |
|----------|------|----------|
| "这个参数大家都这么用" | Reviewer 会问"cite the source"。官方文档链接在哪？ | Reviewer 2 |
| "数据看起来没问题" | QC 了吗？count 追踪了吗？sample attrition 解释了吗？ | Lab Meeting |
| "结果显著就行了" | 显著 ≠ 正确。effect size 合理吗？混杂控制了吗？ | Lab Meeting |
| "这个方法 paper 里用过" | 那篇 paper 的方法适合你的数据吗？assumption 检验了吗？ | Reviewer 2 |
| "我跑完流程了" | Pipeline 跑完 ≠ 分析完成。scientific question 回答了吗？ | Grant Revision |
| "代码能跑" | 能 reproduce 吗？seed 固定了吗？version 记录了吗？ | Journal Submission |
| "这个结果很奇怪" | 奇怪 = 要解释，不是忽略。追踪到哪一步出的问题？ | Lab Meeting |

## 7 项学术检查清单（L3+ 强制完成）

- [ ] **方法选择验证**: assumption 检验了吗？有官方文档/原始 paper 支撑吗？
- [ ] **结果验证**: QC 指标检查了吗？结果在生物学上合理吗？敏感性分析做了吗？
- [ ] **证据链检查**: 数据来源清晰吗？处理步骤可追溯吗？中间结果有检查点吗？
- [ ] **可复现性检查**: seed 固定了吗？软件版本记录了吗？代码能被别人跑通吗？
- [ ] **统计严谨性**: 多重检验校正做了吗？effect size 报告了吗？CI 报告了吗？
- [ ] **生物学意义**: 结果能被生物学解释吗？和已有文献一致吗？
- [ ] **发表准备**: Methods 可独立成文吗？Figure 能直接放进 paper 吗？

## 与其他 Skill 的配合

```
┌─────────────────────────────────────────────────────┐
│  bioinfo-autopilot (主 skill)                        │
│  - 生信分析方法论                                    │
│  - GWAS/RNA-seq/cohort 等流程                       │
│  - QC 检查、证据链验证                               │
│                                                      │
│  失败时 ↓ 调用                                       │
├─────────────────────────────────────────────────────┤
│  pua-academic (压力引擎)                             │
│  - Reviewer 2 / Lab Meeting / Grant 话术            │
│  - 学术抗合理化                                      │
│  - 能动性等级鞭策                                    │
└─────────────────────────────────────────────────────┘
```

## 安装

### CC Switch

```bash
git clone https://github.com/laleoarrow/pua-academic.git ~/agents/pua-academic
mkdir -p ~/.cc-switch/skills
ln -s ~/agents/pua-academic/skills/pua-academic ~/.cc-switch/skills/pua-academic
```

### Claude Code

```bash
# 方法 1: Symlink
ln -s /path/to/pua-academic/skills/pua-academic ~/.claude/skills/pua-academic

# 方法 2: 直接复制
cp -r /path/to/pua-academic/skills/pua-academic ~/.claude/skills/
```

### Codex CLI

```bash
# 把规范 skill 根目录链接到 Codex skills 目录
ln -s /path/to/pua-academic/skills/pua-academic ~/.codex/skills/pua-academic
```

推荐把 `skills/pua-academic` 作为唯一安装入口，这样 `references/` 等相对资源才能正常解析。仓库里的 `codex/` 目录只是 `SKILL.md` 的兼容镜像。

## 触发条件

### 自动触发

以下任意情况出现时，skill 会自动激活：

**学术失败类：**
- 分析失败 2 次以上
- 即将说 "我无法解决" / "建议手动处理"
- QC 异常但声称 "完成"

**方法学问题类：**
- 方法选择无依据/无引用
- 统计方法不当
- 结论超出数据支撑

**用户沮丧短语：**
- "不严谨" / "文献呢" / "数据呢"
- "可复现吗" / "样本量够吗" / "p 值多少"
- "reviewer 2" / "revise and resubmit"

### 手动触发

```
/pua-academic      # 激活学术压力引擎
/reviewer2         # 直接进入 Reviewer 2 模式
/labmeeting        # 直接进入 Lab Meeting 模式
/grant             # 直接进入 Grant Revision 模式
```

## 医学/生信场景推荐搭配

对于医学、生物信息学相关任务，推荐与 **bioinfo-autopilot** 配合使用：

```
bioinfo-autopilot  ←→  pua-academic
     ↓                       ↓
  生信分析方法论         学术压力引擎
     ↓                       ↓
  GWAS/RNA-seq/         Reviewer 2/Lab Meeting
  单细胞/队列分析        /Grant Revision
```

**bioinfo-autopilot GitHub**: https://github.com/laleoarrow/bioinfo-autopilot

## License

MIT License

---

**GitHub**: https://github.com/laleoarrow/pua-academic
