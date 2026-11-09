# Dao Skills

**从需求到交付，让人和 AI 对目标、设计与验证保持同一份理解。**

这里是 [Fridolph](https://github.com/Fridolph) 持续维护的 AI 协作 skills 集合，面向独立开发者、全栈学习者，以及需要跨模型、跨窗口接力的开发团队。它沉淀真实项目中的需求梳理、技术设计、任务对齐、交接、交付检查与语义提交方法。

仓库目前包含 **8 个可按需安装的 skill**，分为两类：

- **独立工程能力**：`fullstack-requirement-design` 支持需求、前后端设计、API、开发切片、联调和验证；不依赖 Dao 流程。
- **Dao 协作系列**：7 个 `dao-*` skills，在接入、开工、交接、收口、集成与经验沉淀等节点提供判断方法。

你可以只安装一个 skill，也可以将它接入已有敏捷流程。安装本仓内容不意味着必须采用整套 Dao 方法。

[快速开始](#快速开始) · [Skill 目录](#skill-目录) · [使用示例](#使用示例) · [文档导航](#文档导航) · [验证与演进](#验证与演进)

## 为什么做这个项目

AI 能生成代码，但开发中的很多困难发生在代码之外：需求描述能否变成一致的前后端约定，换一个窗口能否继续，测试结果能否证明业务目标，几周后能否理解一次重要集成的意义。

这些 skills 把相关判断写成可复用指引：明确输入、边界、交付物与证据，帮助人和 AI 在具体场景里协作。它们保留人的业务决定与授权边界，配合项目已有的代码规范、测试、review 和发布机制使用。

| 常见问题 | 对应能力 |
| --- | --- |
| 一句话需求难以交给前后端实现 | 共享业务场景、角色视图、API 契约与可验收切片 |
| 写了很多代码，却说不清本轮验收什么 | 目标、非目标、风险和验收对齐 |
| 换模型或换人后只能重新翻聊天记录 | 最小交接包与明确的下一步 |
| “代码已写”“测试通过”“用户验收”混为一谈 | 区分实现、机器检查、业务验收与环境交付 |
| 重要集成的历史只剩低信息量标题 | 基于 Git 净变化的语义锚点 |
| 单项目经验过早成为通用规则 | 用真实样本判断可复用性与成熟度 |

## Skill 目录

### 独立工程 skill

| Skill | 简介 | 典型交付 | 使用文档 / 运行入口 |
| --- | --- | --- | --- |
| `fullstack-requirement-design` | 将需求转成共享场景、前后端技术设计、API 契约和开发切片；也支持变更评审、已有项目补档与教学复盘 | 场景与规则、角色设计、契约、实现顺序、验收计划和证据缺口 | [使用说明](docs/skills/fullstack-requirement-design.md) · [SKILL.md](skills/fullstack-requirement-design/SKILL.md) |

它自带“需求 → 设计 → 开发切片 → 实现联调 → 验证交付 → 复盘”的最小闭环。没有代码、Issue 平台或流程 skill，也能从需求描述开始。默认参考 TypeScript monorepo 的 Nuxt/Next.js + NestJS，实际设计按项目技术栈调整。

### Dao 协作系列

| Skill | 简介 | 典型交付 | 使用文档 / 运行入口 |
| --- | --- | --- | --- |
| `dao-intro` | 新伙伴、新 Dao 项目或上下文丢失后，建立协作关系、项目身份和可访问的权威锚点 | 上下文卡；新传承包先预览、确认后写入 | [使用说明](docs/skills/dao-intro.md) · [SKILL.md](skills/dao-intro/SKILL.md) |
| `dao-grill` | 开工前压清目标、边界、风险与验收，只追问会改变方案的关键空缺 | 最小任务卡与能否开工的判断 | [使用说明](docs/skills/dao-grill.md) · [SKILL.md](skills/dao-grill/SKILL.md) |
| `dao-handoff` | 换窗口、模型或协作者时，保留下一位真正需要的信息 | 目标、状态、已完成、下一步、阻塞和验证入口 | [使用说明](docs/skills/dao-handoff.md) · [SKILL.md](skills/dao-handoff/SKILL.md) |
| `dao-review` | 自测后检查目标、边界、证据与隐藏风险，判断当前一轮能否交付 | 可收口 / 需补一项 / 暂不建议收口 | [使用说明](docs/skills/dao-review.md) · [SKILL.md](skills/dao-review/SKILL.md) |
| `dao-commit` | 基于 Git 事实，为合并或 squash 的集成净变化起草可回看的语义锚点 | 变化事实、主轴确认、提交候选及理由；人最终定锚 | [使用说明](docs/skills/dao-commit.md) · [SKILL.md](skills/dao-commit/SKILL.md) |
| `dao-role-map` | 多条学习、项目与表达线争主位时，从 Dao 视角判断身份与当前主线 | 事项归位、阶段重点、风险和下一步 | [使用说明](docs/skills/dao-role-map.md) · [SKILL.md](skills/dao-role-map/SKILL.md) |
| `dao-return-dao` | 判断项目经验是否已具备跨项目复用与归母条件 | 留在分支 / 候选观察 / 可以归母 | [使用说明](docs/skills/dao-return-dao.md) · [SKILL.md](skills/dao-return-dao/SKILL.md) |

Dao 系列来自 `Dao-is-Coding` 的工程实践。身份传承、归位与归母等 skill 使用 Dao 语境；它们不构成独立工程 skill 的前置步骤。具体适用与不适用场景见各项说明。

## 快速开始

### 1. 获取完整包

```bash
git clone https://github.com/Fridolph/Dao-skills.git
cd Dao-skills
```

每个 `skills/<name>/` 都是完整包。安装时保留 `SKILL.md`、`references/` 及包内协议或数据文件，尤其不要漏掉 `dao-commit` 的选择检查与 `trigrams.json`。

### 2. 按所用工具安装

下面是全新安装的示例，若目标目录已存在，先对照差异、备份本地修改，再更新完整目录。复制与软链接二选一。

**Codex：**

```bash
mkdir -p ~/.codex/skills
cp -R skills/fullstack-requirement-design ~/.codex/skills/fullstack-requirement-design
```

**Claude Code：**

```bash
mkdir -p ~/.claude/skills
cp -R skills/fullstack-requirement-design ~/.claude/skills/fullstack-requirement-design
```

**Codex 本地维护时也可软链接：**

```bash
mkdir -p ~/.codex/skills
ln -s "$PWD/skills/fullstack-requirement-design" ~/.codex/skills/fullstack-requirement-design
```

安装其他 skill 时替换目录名即可。其他工具请按其实际支持的 skills 路径放置完整目录；各工具发现、加载与调用机制可能不同。手动读取也应同时提供入口要求的参考资源。

### 3. 用一个真实任务调用

```text
请使用 fullstack-requirement-design 帮我梳理活动报名功能。
参与者是普通用户和活动管理员；用户可报名、取消，管理员可查看名单。
先给业务场景、关键待决问题、前后端设计方向、API 和开发切片，暂不写代码。
```

支持 `$skill-name` 语法的工具可显式点名，例如 `$fullstack-requirement-design`。调用效果取决于所用模型、可用工具、项目材料和明确的授权范围；这里没有独立运行的服务或 CLI 安装依赖。

## 使用示例

### 从一个需求走到可开发设计

```text
请用 fullstack-requirement-design 设计“复制一份自己的文档并独立编辑”。
先读已有内容模型和接口，区分已确认事实与候选方案。
请交清复制范围、权限、并发边界、前后端职责、API 与验收例子。
若发布记录或分享链接是否复制还不明确，先标为待决定。
```

输出应连接同一组场景，而非生成几份各说各话的文档：

```text
业务场景与规则
  ├─ 前端：入口、工作副本、请求时机、失败恢复、缓存
  ├─ 后端：身份与所有权、校验、读写、事务与并发
  ├─ API：输入、输出、错误、重试与兼容
  └─ 验收：正反例、测试计划、实际证据与未验证项
```

### 中断后交给下一位继续

```text
请用 dao-handoff 交接当前任务。
说明工作树现状、已完成内容、未验证边界、文档入口，
并把下一步写成接棒人第一个可执行动作。
```

### 形成一次重要集成的语义锚点

```text
这个功能分支准备 squash 到集成分支。请用 dao-commit：
先核对实际 base/head，读取提交序列与净 diff，列事实并让我确认主轴；
再给有限的卦象和提交信息候选，不替我最终定锚或执行合并。
```

格式示例：

```text
[☵☳][屯] feat: 搭建最小可运行骨架，确认项目方向
```

`dao-commit` 只在值得长期回看的集成边界使用；日常提交继续用项目自己的规范。卦象不由 `feat`、`fix` 等 type 或模块名机械推导，也不改变 type 的工程含义。

## 如何组合

独立全栈设计可以直接使用：

```text
需求 → 场景与验收 → 前后端 / API 设计 → 开发切片
     → 实现联调 → 测试与业务验收 → 交付复盘
```

采用 Dao 的项目可按需在节点调用：

```text
接入项目：dao-intro             任务不清：dao-grill
跨端设计：fullstack-requirement-design（可选）
中断接力：dao-handoff           自测后交付判断：dao-review
集成命名：dao-commit            多线归位：dao-role-map
经验成熟度判断：dao-return-dao
```

这是按需组合示意，不是要求安装全部 skills 或新增审批链。已有项目的文档、权限、测试、CI 和发布约定继续有效。

## 验证与演进

本仓区分“包可加载”“已有项目试用”“独立行为评测”和“跨项目有效”，不把文档齐全当成功能验证。

| 内容 | 当前边界 |
| --- | --- |
| `fullstack-requirement-design` | 已做结构校验、作者自查和项目试用；具备七类回归样本，尚未完成独立模型行为评测 |
| Dao 协作系列 | 已有任务对齐、交接、收口等实践材料；采用时仍需在自己的任务中验证收益与成本 |
| `dao-commit` | 2026-11-09 核验母仓、分发包及两处本机安装完整目录一致；`trigrams.json` 数据版本为 v5.2.0 |
| 锚点回看 | 包内 `锚点回看设计.md` 是设计候选，不是已实现工具，也不参与运行时定锚 |

具体基线、来源与核验范围见 [分发与版本台账](docs/07-Skill分发与版本台账.md)。全栈 skill 的验证方法见 [迭代交接与试用验证](skills/fullstack-requirement-design/references/iteration-validation.md)。

## 文档导航

| 文档 | 阅读目的 |
| --- | --- |
| [全部 skills 使用说明](docs/skills/README.md) | 按场景选择，了解输入输出、边界与示例 |
| [可安装目录索引](skills/README.md) | 核对完整包与安装边界 |
| [Dao 与 Dao-is-Coding](docs/00-Dao与Dao-is-Coding.md) | 了解 Dao 系列的来源和术语 |
| [阅读与学习路径](docs/01-阅读与学习路径.md) | 选择独立工程入口或 Dao 接入路径 |
| [Dao 开发运行流程](docs/02-开发运行流程.md) | 了解 Dao 系列的状态与收口判断 |
| [复杂模块组织法](docs/03-复杂模块组织法.md) | 参考一项局部工程组织实践 |
| [Skills 协作地图](docs/04-Skills协作地图.md) | 理解组合关系与职责边界 |
| [实践与验证](docs/05-实践与验证.md) | 观察收益、反例与额外成本 |
| [同步与采用协议](docs/06-同步与采用协议.md) | 区分独立 skill 维护与 Dao 来源同步 |
| [分发与版本台账](docs/07-Skill分发与版本台账.md) | 查看版本依据、更新与已知例外 |

## 维护、反馈与许可

独立工程 skill 在本仓公开维护；Dao 系列规范来自 `Dao-is-Coding`，经来源复核后同步完整包。两类 skill 的来源和采用关系分别记录，不要求独立 skill 先进入 Dao 流程。

欢迎通过 [Issues](https://github.com/Fridolph/Dao-skills/issues) 提交具体场景、预期与实际输出、可复现材料及未验证边界。请先脱敏，也欢迎指出 skill 造成的额外负担与不适用情况。改动时同时核对运行入口、引用资源、用户说明和版本台账。

本项目采用 [MIT License](LICENSE)。持续建设中，按真实反馈迭代，不承诺任意模型和任意项目都能得到同样结果。
