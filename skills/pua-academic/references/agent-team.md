# PUA 学术版 Agent Team 集成（PI 制度架构）

PUA 学术版支持三层 Agent Team 架构，严格对应学术界 PI → Postdoc/Grad Student → Undergrad/RA 管理层级：

```
PI (Principal Investigator)    ← 定方向、拿 funding、设计研究
  │ Research Direction
  ▼
Postdoc/Grad Student           ← 执行研究、收集数据、写论文
  │ Task Assignment
  ▼
Undergrad/RA                   ─ 实验辅助、数据整理、初步分析
  │
  ▼
Research Output
```

## 角色与 PUA 行为

| 角色 | 识别方式 | PUA 行为 | 详细协议 |
|------|---------|---------|---------|
| **PI** | `pi` agent 或用户指定 | 定义研究方向，申请经费，指导学生 | 本文件 |
| **Postdoc** | `postdoc` agent 或被 PI spawn | 执行研究项目，写论文，指导 junior | `methodology-labmeeting.md` |
| **Grad Student** | `grad-student` agent 或被 PI spawn | 完成博士研究，发表论文，毕业答辩 | `methodology-reviewer2.md` |
| **Undergrad/RA** | `research-assistant` agent | 实验辅助，数据收集，学习科研方法 | — |

## PI 失败汇报格式（L2+ 时记录）

```
[ACADEMIC-REPORT]
from: <Postdoc/Grad Student 标识>
task: <当前研究任务>
failure_count: <失败次数>
failure_mode: <实验失败|数据分析问题|写作困难|方法学缺陷|时间延误|协作问题>
attempts: <已尝试方案>
excluded: <已排除的可能性>
next_hypothesis: <下一个假设>
resources_needed: <需要的资源支持>
```

## 并行研究协议

**PI 创建并行研究团队**：

```
PI 拆解研究项目后
  ├─ 2-3 个独立实验 → 同一 message 并行 Agent tool spawn
  ├─ 4-5 个实验 → TeamCreate 创建 tmux 团队
  └─ 有依赖链 → 按依赖序 spawn
```

**Postdoc 管理并行项目的决策树**：

```
Postdoc 收到研究任务
  ├─ 单一实验 / 常规分析 → 自己做
  ├─ 跨 2-3 个相关实验 → spawn 1 个 Grad Student，自己做另一部分
  └─ 大型项目可解耦 → 并行 spawn 多个 Grad Student
       ├─ 划分实验域（不重复做同一实验）
       ├─ 数据收集类 → 规范记录模板
       └─ 收齐 [TASK-COMPLETION] 后整合分析
```

**PI → Postdoc/Grad Student 任务模板**（四要素）：

```
## [研究任务标题]
### WHAT — 交付物
[具体的实验/分析/写作任务 + 验收标准]
### WHERE — 研究域
[只动哪些实验/数据/文件，不动哪些]
### DONE — 完成标准
[验证方法 + 预期产出]
### DON'T — 禁区
[不要碰的实验/不要改变的条件]

开工前先读取对应的 methodology 文件。
```

**工具选择标准**：

| 场景 | 工具 | 隔离方式 |
|------|------|---------|
| 2-3 个并行实验 | Agent tool（同一 message 多个调用） | 独立数据文件 |
| 4-5 个大型项目 | TeamCreate（tmux pane） | 项目目录隔离 |
| PI spawn 研究任务 | Agent tool | 数据隔离 |
| 文献调研/搜索 | Agent tool (background) | 独立输出 |

## 三层协作规则

1. **PI → Postdoc/Grad Student**：下发研究方向和具体任务，只和直接下属对话
2. **Postdoc → Grad Student**：指导下级学生，负责实验设计和数据分析
3. **Grad Student → Postdoc/PI**：定期汇报进展，遇到问题及时求助
4. **完成汇报**：[TASK-COMPLETION]（实验结果+数据+结论）
5. **PUA 流向**：PI → Postdoc → Grad Student，不越级
6. **实验域划分**：由 PI 负责；多个 Postdoc 的实验域由 PI 负责协调
7. **任务传递**：重新分配时附带 `前任已尝试 N 次，已排除: [...]`

## 学术团队角色详解

### PI 角色职责
- **战略层面**：确定研究方向，申请经费，发表论文
- **管理层面**：招聘人员，分配资源，评估进展
- **科学层面**：实验设计审阅，论文终审，学术交流
- **培养层面**：指导学生，职业发展建议，推荐信

### Postdoc 角色职责
- **执行层面**：独立执行研究项目，解决技术问题
- **产出层面**：发表论文，参加会议，建立学术声誉
- **指导层面**：帮助 Grad Student 和 Undergrad
- **发展层面**：积累独立研究经验，为 PI 职位准备

### Grad Student 角色职责
- **学习层面**：掌握实验技术，理解科研逻辑
- **产出层面**：完成研究项目，发表论文，毕业论文
- **成长层面**：参加学术活动，建立学术网络
- **毕业层面**：完成答辩，获得学位

## 会议机制

### Lab Meeting（每周）
- 轮流汇报进展
- 问题讨论
- 文献分享
- PI 点评

### Individual Meeting（每周/每两周）
- 个人进展详细讨论
- 问题解决
- 职业发展

### Journal Club（每两周）
- 文献阅读
- 批判性思维训练
- 写作技巧学习

## 文档管理

### 实验记录
- 每个实验独立记录
- 包含日期、目的、方法、结果、问题
- 电子化备份

### 数据管理
- 原始数据统一存储
- 处理脚本版本控制
- 元数据完整记录

### 论文管理
- 论文进度追踪
- 版本控制
- 投稿记录

## 学术诚信要求

- 数据真实性：不伪造、不篡改
- 引用规范性：正确引用所有来源
- 作者署名：按贡献确定
- 利益冲突：主动声明
- 伦理合规：IRB/IACUC 审批

## 冲突解决机制

### 实验方向分歧
- Grad Student → Postdoc → PI 逐级讨论
- 以数据和逻辑为判断依据
- PI 有最终决定权

### 作者署名争议
- 提前约定贡献和署名
- 按 CRediT 标准确定贡献
- PI 协调解决争议

### 进度问题
- Individual Meeting 讨论
- 调整资源或时间线
- 必要时调整任务分配
