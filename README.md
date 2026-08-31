# Dao Skills

面向人类与 AI 协作的软件开发 skills：在真正需要判断的节点，帮助团队对齐目标、保留交接、验证收口，并把成熟经验带回可复用的规范。

> `Dao` 是母体；`Dao-is-Coding` 是它在工程领域的验证线；本仓是稳定 skills 的开源分发包。

这不是另一套强制开发流程，也不替代项目自己的规范、测试、代码 review 或人的最终决定。每个 skill 只服务一个高频协作节点。

## 快速开始

1. 先选择当前需要的 skill，不必一次安装全部。
2. 复制或软链接完整的 `skills/<skill>/` 目录到所用 AI 工具支持的 skills 目录。
3. 让 AI 工具读取该目录的 `SKILL.md`；若目录含 `references/`、协议或数据文件，必须一并保留。
4. 用一件真实任务验证它，而不是先把所有文档读完。

```bash
git clone https://github.com/Fridolph/Dao-skills.git

# 示例：按你的 AI 工具要求，复制完整目录
cp -R Dao-skills/skills/dao-grill /path/to/your-ai-tool/skills/dao-grill
```

不同 AI 工具的目录约定不同。`dao-commit` 的已知接入方式见 [接入指南](skills/dao-commit/SETUP.md)；其余 skill 遵循所用工具的标准 skills 安装方式。

## 选择一个 Skill

| Skill | 解决什么 | 详细说明 |
| --- | --- | --- |
| `dao-intro` | 新伙伴、新项目或上下文丢失后的传承与归位 | [阅读文档](docs/skills/dao-intro.md) |
| `dao-role-map` | 多条学习、项目与表达线争主位时的身份归位 | [阅读文档](docs/skills/dao-role-map.md) |
| `dao-grill` | 开工前把目标、边界、风险与验收压清 | [阅读文档](docs/skills/dao-grill.md) |
| `dao-handoff` | 换窗口、换模型或换协作者时留下最小接棒包 | [阅读文档](docs/skills/dao-handoff.md) |
| `dao-review` | 收口前核验交付条件与提交路径 | [阅读文档](docs/skills/dao-review.md) |
| `dao-commit` | 为合并 / squash 后的集成净变化起语义锚点 | [阅读文档](docs/skills/dao-commit.md) |
| `dao-return-dao` | 判断经验留在项目、候选观察，还是可以归母 | [阅读文档](docs/skills/dao-return-dao.md) |

完整目录与比较见 [Skills 文档索引](docs/skills/README.md)。

## 推荐使用路径

```text
新伙伴 / 新项目？ -> dao-intro
主线失焦？ -> dao-role-map（按需）
任务尚未对齐？ -> dao-grill
实现 / 测试 / 交接（中断时 dao-handoff）
准备收口？ -> dao-review
跨过集成边界？ -> dao-commit
发现跨项目经验？ -> dao-return-dao
```

这张图不是线性流水线。项目原有的设计、编码、测试、CI、PR 与发布始终是主体；需要判断时，才调用对应 skill。

## 文档导航

- [Dao 与 Dao-is-Coding](docs/00-Dao与Dao-is-Coding.md)：这套方法尝试解决什么，以及当前边界。
- [阅读与学习路径](docs/01-阅读与学习路径.md)：新协作者与已有项目的最短进入方式。
- [开发运行流程](docs/02-开发运行流程.md)：状态链、验证与收口路径。
- [复杂模块组织法](docs/03-复杂模块组织法.md)：一个已验证的局部工程方法。
- [Skills 协作地图](docs/04-Skills协作地图.md)：skills 在一轮任务中的关系。
- [实践与验证](docs/05-实践与验证.md)：如何基于证据采用、调整或停止使用。
- [同步与采用协议](docs/06-同步与采用协议.md)：项目采用与问题回提的边界。
- [Skill 分发与版本台账](docs/07-Skill分发与版本台账.md)：规范源、分发包与已知例外。

## 开源与演进

本仓采用 [MIT License](LICENSE)。欢迎通过 issue、讨论或可复现样本反馈，但请把“在某个项目里有效”与“已跨项目成立”区分开来。

稳定规则的单向路径是：实践来源与项目样本 → `Dao-is-Coding` 归母定规范 → 本仓打包分发 → 项目选择性采用。详见 [同步与采用协议](docs/06-同步与采用协议.md)。
