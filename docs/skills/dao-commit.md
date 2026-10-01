# `dao-commit`：集成净变化的语义锚点

`dao-commit` 帮助人基于 Git 事实，为跨过集成边界的净变化起草提交信息。它保留 Conventional Commit 的 `type(scope): subject` 兼容骨架，并用完整卦义为集成单元增加一层可回看的语义锚点。

最终选什么卦、是否提交，始终由人确认。AI 的职责是先读事实、区分过程动作和最终变化、给出有限候选与理由。

## 何时使用

仅在以下集成边界考虑使用：

- 多笔普通提交从 `feature` 合并 / squash 到 `dev` 后，形成明确净变化。
- `dev` 合并 / squash 到 `main` 前，出现值得长期回看的明确净差异。

日常开发、流程修订和单任务收口使用普通 Conventional Commit。零散修改、WIP 或未跨过集成边界的工作，不应为了“看起来更完整”而起 Dao Commit。

### 锚点与 `type` 正交

是否起卦取决于**时机与净变化**，与 `type` 无关。任何 `type` 都能构成集成锚点：

- 一次全是老问题修复的发布，`type` 以 `fix` 为主；
- 一次以结构整理为主的集成，`type` 就是 `refactor`；
- 没有新功能，不影响这轮是否值得起卦。

`dao-commit` 只复用 Conventional Commit 的 `type` 骨架，不生成、不覆盖、也不推荐 `type`。卦象读的是这一轮开发的集中点与聚焦处，它不改变 `type` 的选择。这里排除的始终是**未跨过集成边界的零散提交**，不是某类 `type`。

## 提交格式

```text
[上卦下卦][卦名] type(scope): subject

背景：为什么这样动（可选）
判断：这轮真正成立的变化（可选）
停点：本轮止于哪里（可选）
Refs / Related / Closes（可选）
```

例如：

```text
[☵☳][屯] feat: 搭建最小可运行骨架，确认项目方向
```

`type` 始终按本次净变化的实际工程行为选择，`dao-commit` 不生成、不覆盖、也不推荐它；语义重心是 `subject` 与卦象，而不是把 scope 写成目录清单。

## 起草过程

1. **读取 Git 事实**：检查 status、差异和近期历史；合并场景还要看提交序列与净 diff。
2. **确定集成单元**：明确这次回答的是哪一段相对基线的变化。
3. **列事实并二次确认**：区分新增、删除、迁移、修复与真正的主轴；未确认前不直接定卦。
4. **先写 subject，再定 type / scope / 卦象**：避免让卦象反过来替代事实判断。
5. **给候选而非裁决**：说明上卦、下卦与卦名为何匹配；人确认后再收口。

## 卦象如何理解

- 先判断本次集成单元的整体处境、净变化和必要条件，再用近义卦复核。
- 选定卦名后，才用上卦和下卦解释结构；不能从动作、模块或文件类型机械反推卦名。
- 完整 64 卦选择检查见 [`64卦选择检查.md`](../../skills/dao-commit/references/64卦选择检查.md)。`trigrams.json` 保留卦象结构、经典锚点、工程投影、典型场景、误用警示、成熟度、适用面与 `type` 示例；这些字段帮助理解、核对与复盘，但不能机械反推卦名。
- 逐卦的 `commitApplicability` 说明该处境**多久出现一次、适合什么量级的集成节点**（`common` / `milestone` / `rare` / `not-recommended`，判据见 `applicabilityLevels`），与本次 `type` 无关。

爻位是可选深度模式，用于判断阶段与命名口气；它只作提醒，不生成 `type`，也不默认把爻辞塞进 commit message。

## 最小使用示例

```text
feature/export 即将 squash 到 dev。请用 dao-commit：
先读取合并范围的 Git 提交和净 diff，列出相对基线的事实；
等我确认主轴后，再给 1–2 个 header 候选及理由。
```

## 安装与资源

`dao-commit` 依赖完整目录中的入口、协议和数据文件，不能只复制 `SKILL.md`：

```text
dao-commit/
├── SKILL.md
├── core-protocol.md
├── trigrams.json
├── SETUP.md
├── 锚点回看设计.md          ← 设计候选，非运行时指令
└── references/64卦选择检查.md
```

- [多工具接入指南](../../skills/dao-commit/SETUP.md)
- [完整工程协议](../../skills/dao-commit/core-protocol.md)
- [64 卦选择检查](../../skills/dao-commit/references/64卦选择检查.md)
- [卦象结构数据](../../skills/dao-commit/trigrams.json)
- [锚点回看设计（候选）](../../skills/dao-commit/锚点回看设计.md)：锚点积累后的回看与觉知设计，**不属于运行时规则**

## 当前成熟度与边界

这是正在以真实样本持续校准的语义系统，不是易经展示器，也不替代测试、review、发布门禁或人的判断。首轮 64 卦整体义选择检查已确认，真实样本反照仍需持续积累。

`Dao-commit` 不再作为独立分发源；本仓是公开可安装包，稳定规范先在 `Dao-is-Coding` 归母后再同步至此。
