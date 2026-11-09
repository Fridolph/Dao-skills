# Skills 文档索引

本目录面向准备采用 Dao Skills 的开源读者。每篇文档说明一个 skill 的职责、适用边界、输入输出、最小使用方式和与其他 skills 的关系。

仓库同时收录独立工程能力与 Dao 系列。`fullstack-requirement-design` 可独立运行；选择它不要求先使用任何 `dao-*` skill。

## 先选节点，再读详情

| 你现在遇到的问题 | 建议 Skill | 说明 |
| --- | --- | --- |
| 需求需要展开成前后端设计、API、开发与验收；或已有项目需要补档 | [`fullstack-requirement-design`](fullstack-requirement-design.md) | 独立工程 skill，不依赖 Dao 或专用任务系统 |
| 新 AI、新项目，或已无法确认共同上下文 | [`dao-intro`](dao-intro.md) | 先完成传承与项目归位 |
| 多条项目、学习或表达线同时争主位 | [`dao-role-map`](dao-role-map.md) | 先判断身份和当前主线 |
| 目标、边界、风险或验收还不够清楚 | [`dao-grill`](dao-grill.md) | 开工前最小对齐 |
| 需要换窗口、模型、AI 或协作者 | [`dao-handoff`](dao-handoff.md) | 输出可续跑的最小接棒包 |
| 一轮工作完成，想判断能否交付 | [`dao-review`](dao-review.md) | 核验收口与提交路径 |
| 正在合并 / squash，想给净变化命名 | [`dao-commit`](dao-commit.md) | 为集成边界留下语义锚点；与 `type` 无关 |
| 项目里长出可能通用的规则或流程 | [`dao-return-dao`](dao-return-dao.md) | 判断应留项目、候选还是归母 |

## 文档约定

- 每篇的“何时不要用”与“不会替代什么”同样重要，避免 skill 被当成万能流程。
- 公开文档说明原则与可复现用法；运行时的完整指令、模板、示例及数据仍以对应 `skills/<skill>/` 目录为准。
- skills 不因被加载就获得写入权限。用户授权开发时，可按约定推进代码与验证；只要求设计时交付设计。涉及身份传承、不可逆操作或外部写入时遵守用户和项目的授权边界。

## 建议的第一轮

要体验全栈需求与设计，先选一个场景试用 `fullstack-requirement-design`，核对前后端约定是否一致、验收是否可执行。

要试用 Dao 协作系列，可先按需要使用三件套：

1. 任务模糊时用 `dao-grill`。
2. 发生中断或换人时用 `dao-handoff`。
3. 准备交付时用 `dao-review`。

在真实任务里验证三件套确实减少了猜测与上下文丢失后，再按需要引入传承、语义提交和归母判断。
