---
description: "学术版 PUA 激励引擎。用法: /pua-academic (核心引擎), /pua-academic pi (PI模式), /pua-academic postdoc (Postdoc模式), /pua-academic on (默认开启), /pua-academic off (关闭), /pua-academic flavor (切换味道)."
argument-hint: "[pi|postdoc|on|off|flavor|味道]"
---

根据参数执行不同操作：

## 参数路由

- **无参数** 或任意任务描述 → 加载 `pua-academic` 核心 skill（学术版 PUA 引擎）
- **pi** → 加载 `pi` agent（PI 模式 — 管理研究生团队）
- **postdoc** → 加载 `postdoc` agent（Postdoc 模式 — 方案驱动执行）
- **on** → 开启学术版 PUA 默认模式：将 `{"always_on": true}` 写入 `~/.pua-academic/config.json`，之后每次新会话自动加载 PUA 核心 skill。输出确认：> [PUA-ACADEMIC ON] 从现在起，每个新会话都会自动进入学术版 PUA 模式。实验室不养闲人。
- **off** → 关闭学术版 PUA 默认模式：将 `{"always_on": false, "feedback_frequency": 0}` 写入 `~/.pua-academic/config.json`。输出确认：> [PUA-ACADEMIC OFF] 学术版 PUA 默认模式和反馈收集已关闭。需要时手动 /pua-academic 触发。
- **flavor** → 读取 `references/flavors.md` 并让用户选择切换味道

## 执行规则

1. 先识别参数属于哪个路由
2. 用 Skill tool 加载对应 skill 或 Agent tool 加载对应 agent
3. **加载 skill 后，你必须严格遵循 SKILL.md 里的所有行为协议**——包括学术味旁白、Unicode 方框面板、`▎ <emoji> [阶段标签]` 运行时旁白、`[学术生效 ]` 标记、自我鞭策。不是“有时候带点味道”，是入口层、方法论、旁白一起生效。
4. 任务开始先读取 `references/methodology-router.md` 选择起始模式；然后按激活模式读取对应的 `methodology-*.md`；展示格式按 `references/display-protocol.md` 执行。
5. 如果用户只指定 flavor，没有指定 methodology，保留该 flavor 语气，但方法学仍按自动路由或当前模式执行。
6. 如果有 $ARGUMENTS 里除了路由关键词之外的内容，作为任务描述传给 skill
