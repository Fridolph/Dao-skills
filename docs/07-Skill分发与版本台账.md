# Skill 分发与版本台账

> 基线日期：2026-09-02。版本以母仓源包与本仓目录级一致性为准，不以本机安装副本为准。

## 权威路径

| 层 | 权威位置 | 职责 |
| --- | --- | --- |
| 实践来源 | `Dao-commit`、`dao-*` 项目 | 样本、问题与候选 |
| 归母规范 | `Dao-is-Coding/60-器-技能与构建/00-技能/` | 稳定定义与完整源包 |
| 分发包 | `Dao-skills/skills/` | 可安装完整包与对外版本 |
| 安装态 | 各 AI 工具的 skills 目录 | 本地使用，不是编辑源 |

## 当前 Skill 基线

| Skill | 母仓源包 | 分发状态 | 说明 |
| --- | --- | --- | --- |
| `dao-intro` | `00-技能/dao-intro/` | 已分发 | 初次传承先预览 `.dao/`，Owner 确认后才可写入 |
| `dao-grill` | `00-技能/dao-grill/` | 已分发 | 开工前最小对齐 |
| `dao-handoff` | `00-技能/dao-handoff/` | 已分发 | 使用“集成锚点（如适用）”而非日常 Dao Commit 候选 |
| `dao-review` | `00-技能/dao-review/` | 已分发 | 区分常规提交与集成 Dao Commit |
| `dao-commit` | `00-技能/dao-commit/` | 已分发 | `Dao-commit` 实践已归母；只在集成边界起锚 |
| `dao-role-map` | `00-技能/dao-role-map/` | 已分发 | 主线失焦时的旁路判断 |
| `dao-return-dao` | `00-技能/dao-return-dao/` | 已分发 | 判断经验留分支、候选或归母 |

## 已知例外

- `/Users/fri/.agents/skills/dao-commit`、`/Users/fri/.codex/skills/dao-commit` 与本基线曾存在差异；本轮不自动覆盖。后续安装前应按本仓完整包重新核验。
- `dao-sync` 目前是待验证的流程候选，不是正式 skill。

## 每次更新记录

| 日期 | Skill / 范围 | 来源与归母结论 | 分发校验 |
| --- | --- | --- | --- |
| 2026-08-31 | `dao-commit`、`dao-handoff`、`dao-review` | 将 `Dao-commit` 的完整实践归母；收窄为集成锚点，回补 flow skills | 母仓与分发包目录级一致 |
| 2026-08-31 | `dao-intro` | 作为新伙伴 / 新项目传承入口加入最小运行链 | 母仓与分发包目录级一致 |
| 2026-09-02 | `dao-commit`、`dao-intro` | 分发母仓最新 `dao-commit` 完整资料与字段说明；复核 `dao-intro` 完整包无漂移 | 两个完整目录均与母仓一致 |
