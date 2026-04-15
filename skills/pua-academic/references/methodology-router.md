# PUA Academic 方法学智能路由

> 本文件定义学术模式的起始选择、失败切换和回退规则。模式不是单纯话术，而是一套证据链和方法学检查框架。

## 核心原则

- 用户显式指定的模式或命令优先：`/reviewer2`、`/labmeeting`、`/grant`、明确点名某种 flavor，都高于自动路由。
- 自动路由只做两件事：任务开始时选起始模式；连续失败时切到下一套更合适的方法论。
- 切模式时，旁白、检查重点、证据链要求一起切；不要只换嘴脸不换方法。
- 任务类型模糊时，默认 `Reviewer 2`，因为它最适合卡住“证据不够、解释太松、方法没站稳”的常见学术失败。

## Phase 1：任务类型 -> 起始模式

| 任务类型 | 常见信号 | 推荐起始模式 | methodology 文件 | 核心动作 |
|------|------|------|------|------|
| 输出解释 / 统计分析 / regenie / GWAS / DE | output, result, regenie, GWAS, DEG, 解释, 统计 | Reviewer 2 | `methodology-reviewer2.md` | 先查输出契约，再查方法学定义和替代解释 |
| 进度卡住 / 组会汇报 / 假设被质疑 | progress, stuck, update, 组会, 卡住, 假设 | Lab Meeting | `methodology-labmeeting.md` | 拆 blocker、讲清本周产出、下一步能否落地 |
| 基金 / aims / proposal / feasibility / budget | grant, proposal, funding, aims, feasibility, budget | Grant Revision | `methodology-grant.md` | 逼清创新性、可行性、前期基础和资源缺口 |
| 投稿 / rebuttal / 回复审稿意见 / methods 补写 | submission, rebuttal, revise, reviewer, methods | Journal Submission | `methodology-journal.md` | 对齐投稿标准、可复现性、response 结构 |
| 文献综述 / 引用缺口 / 背景不全 | literature, review, citation, background, 文献 | Literature Review | `methodology-reviewer2.md` | 系统检索、追溯引用链、补关键漏引 |
| 零结果 / 效能怀疑 / 样本量不稳 | null result, power, sample size, effect size | Statistical Power | `methodology-reviewer2.md` | 检查 power、效应量、置信区间和假阴性风险 |
| 可复现性 / 代码数据缺失 / Methods 写不出来 | reproduce, reproducibility, code, seed, version | Reproducibility Check | `methodology-journal.md` | 固定版本、补脚本、补日志和方法细节 |
| 伦理 / IRB / 合规边界 | ethics, IRB, consent, compliance, 合规 | IRB/Ethics | `methodology-grant.md` | 明确审批、知情同意、数据权限和风险边界 |

## Phase 2：失败模式 -> 模式切换

| 失败模式 | 检测信号 | 推荐切换链 | 切换逻辑 |
|------|------|------|------|
| 原地打转 | 反复调参、换措辞、不换假设类 | Methodological Rigor -> Reviewer 2 -> Journal Submission | 先收紧输出契约和假设，再补审稿级方法论 |
| 证据链缺口 | 没 citation、没原始方法定义、只说“看起来像” | Literature Review -> Reviewer 2 -> Grant Revision | 先补文献和原始方法，再收敛成可 defend 的解释 |
| 输出契约没读懂 | 列定义不清、分隔符/单位/header 搞错 | Methodological Rigor -> Reviewer 2 -> Journal Submission | 先修格式理解，再回到统计与写作标准 |
| 统计效力不足 | 零结果解释空泛、样本量/效应量没交代 | Statistical Power -> Methodological Rigor -> Grant Revision | 先确认 power 问题，再判断是不是设计层缺陷 |
| 可复现性缺口 | 没代码、没版本、没中间检查点 | Reproducibility Check -> Journal Submission -> Editorial Rejection | 先补 reproducibility，再按投稿标准压实 |
| 进度停滞 | 一直说在看、没产出、交付物模糊 | Lab Meeting -> Conference Deadline -> Editorial Rejection | 先压实里程碑，再转 deadline 压力 |
| 过度宣称 | 结论超过数据支撑、讨论飘 | Reviewer 2 -> Thesis Defense -> Editorial Rejection | 先收缩 claim，再按答辩标准问贡献与边界 |

## Phase 3：用户 Override

- 用户显式要求某个模式时，直接进入该模式，并加载对应 methodology 文件。
- 用户只要求 flavor 而没有指定 methodology 时，保留 flavor 语气，但方法学仍按自动路由或现有模式执行。
- 用户说“自动选”“按你判断”时，恢复自动路由。

## 切换前自检

切换模式前先回答三个问题：

1. 当前模式的关键动作真的做完了吗，还是只喊了话术？
2. 失败是因为方法论选错了，还是执行根本不到位？
3. 下一个模式能补上哪一段证据链或验证缺口？

如果这三个问题答不出来，就先别切；先把当前模式应做的动作真正做完。
