# `dao-commit`：集成净变化的语义锚点

`dao-commit` 帮助人基于 Git 事实，为跨过集成边界的净变化起草提交信息。它保留 Conventional Commit 的 `type(scope): subject` 兼容骨架，并用“动作方向 × 承载对域 → 卦名”增加一层可回看的语义锚点。

最终选什么卦、是否提交，始终由人确认。AI 的职责是先读事实、区分过程动作和最终变化、给出有限候选与理由。

## 何时使用

仅在以下集成边界考虑使用：

- 多笔普通提交从 `feature` 合并 / squash 到 `dev` 后，形成明确净变化。
- `dev` 合并 / squash 到 `main` 前，出现值得长期回看的明确净差异。

日常 `feat`、`fix`、`docs`、流程修订和单任务收口使用普通 Conventional Commit。小改动、WIP 或未跨过集成边界的工作，不应为了“看起来更完整”而起 Dao Commit。

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

`type` 保持工程生态兼容；语义重心是 `subject` 与卦象，而不是把 scope 写成目录清单。

## 起草过程

1. **读取 Git 事实**：检查 status、差异和近期历史；合并场景还要看提交序列与净 diff。
2. **确定集成单元**：明确这次回答的是哪一段相对基线的变化。
3. **列事实并二次确认**：区分新增、删除、迁移、修复与真正的主轴；未确认前不直接定卦。
4. **先写 subject，再定 type / scope / 卦象**：避免让卦象反过来替代事实判断。
5. **给候选而非裁决**：说明上卦、下卦与卦名为何匹配；人确认后再收口。

## 卦象如何理解

- **下卦**表示变化主要落在哪个承载对域，例如核心逻辑、基础设施、事件、接口、横切能力、高风险通道、配置稳定层或展示依赖层。
- **上卦**表示本轮的动作方向，例如创造、连接、可见化、启动、渗透、修复、定边或承接。
- 上下组合得到卦名；完整 64 卦映射和成熟度以 `trigrams.json` 为准。

爻位是可选深度模式，用于判断阶段、收窄语气和 type 建议，不默认把爻辞塞进 commit message。

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
└── SETUP.md
```

- [多工具接入指南](../../skills/dao-commit/SETUP.md)
- [完整工程协议](../../skills/dao-commit/core-protocol.md)
- [64 卦工程语义数据](../../skills/dao-commit/trigrams.json)

## 当前成熟度与边界

这是正在以真实样本持续校准的语义系统，不是易经展示器，也不替代测试、review、发布门禁或人的判断。数据中标记为 `validated` 的映射已有实践依据；`candidate` 仍应以事实和上下文为先。

`Dao-commit` 不再作为独立分发源；本仓是公开可安装包，稳定规范先在 `Dao-is-Coding` 归母后再同步至此。
