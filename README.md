# Dao Skills

`Dao Skills` 是 `Dao-is-Coding` 当前可安装、可阅读的协作工具包。

它不把 Dao 变成又一套“强制流程”，而是帮助人和 AI 在真实软件开发中看清：现在该先判断什么、怎样不断棒、何时可以收口，以及哪些经验已经值得留下。

> `Dao` 是母体；`Dao-is-Coding` 是它在工程领域的验证线；skills 是让这条线进入日常协作的器。

## 从哪里开始

如果你是第一次进入，请按下面顺序阅读：

1. [Dao 与 Dao-is-Coding](docs/00-Dao与Dao-is-Coding.md)
2. [阅读与学习路径](docs/01-阅读与学习路径.md)
3. [开发运行流程](docs/02-开发运行流程.md)
4. [复杂模块组织法](docs/03-复杂模块组织法.md)
5. [Skills 协作地图](docs/04-Skills协作地图.md)
6. [实践与验证](docs/05-实践与验证.md)

若你已在一个具体任务里，先看项目自己的 `README`、当前任务或交接包，再按需回来看本仓文档；不要先把整套理论读完才开始接棒。

## 当前 Skills

| Skill | 解决的节点 | 何时使用 |
| --- | --- | --- |
| `dao-role-map` | 多条线的身份与主位 | 学习、项目、表达都在争主线时 |
| `dao-grill` | 开工前最小对齐 | 目标、边界、风险或验收尚不清楚时 |
| `dao-handoff` | 中断续跑与接棒 | 换窗口、模型或协作者时 |
| `dao-review` | 收口前过门 | 实现和自测后，准备交付或提交时 |
| `dao-commit` | 集成净变化的语义锚点 | `feature -> dev` 或 `dev -> main` 的合并 / squash 时 |
| `dao-return-dao` | 经验是否归母 | 某条规则是否已经跨项目成熟时 |

完整关系与推荐组合见 [Skills 协作地图](docs/04-Skills协作地图.md)。

## 最小运行链

```text
主线失焦？ -> dao-role-map（按需）
任务未对齐？ -> dao-grill
实现 / 测试 / 交接（中断时 dao-handoff）
收口前？ -> dao-review
真实变化成立？ -> dao-commit
跨项目经验成熟？ -> dao-return-dao
```

这不是必须逐格执行的线性流水线。日常开发持续流转；需要判断时才过门，发生值得回看的真实变化时才定锚。

## 安装与使用

每个 skill 都是独立目录，可按所用 AI 编程工具的 skill 目录安装或软链接。建议先从 `dao-grill`、`dao-handoff`、`dao-review` 三件套开始，再按需要接入 `dao-commit` 和两条旁路 skill。

`dao-commit` 的多工具接入说明见 [skills/dao-commit/SETUP.md](skills/dao-commit/SETUP.md)。其余 skill 可直接复制或链接整个目录，并让 AI 工具读取其中的 `SKILL.md`。

## 当前边界

这不是一套已经定型的 AI Native 范式产品。当前目标仍是：在真实项目中持续验证“判断、流转、验证、收口、沉淀”能否减少协作黑盒，再把被反复证明有效的部分稳定下来。

使用 skill 的价值、未使用时容易暴露的成本，以及如何做对照验证，见 [实践与验证](docs/05-实践与验证.md)。

## 许可

本仓采用 [MIT License](LICENSE)。
