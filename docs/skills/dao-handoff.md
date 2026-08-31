# `dao-handoff`：最小接棒包

`dao-handoff` 用于窗口、模型或协作者切换，以及长任务中断续跑。它不做完整复盘，而是把下一位真正需要的最少信息交清，让续跑不依赖重新通读聊天记录或猜测工作树状态。

## 何时使用

- 当前窗口即将结束，需要让下一位继续。
- 人和多个 AI 伙伴轮流推进同一任务。
- 已经完成一部分实现，准备交给下一位 review。
- 上下文很长，继续前需要压缩出一个可靠锚点。

## 标准 Handoff Card

```text
【接棒】我接的是 X，我下一步先做 Y。

目标：
当前状态：
已完成：
下一步：
阻塞：
自测：
文档锚点：
集成锚点（如适用）：
```

“集成锚点”只在 `feature -> dev` 或 `dev -> main` 合并 / squash 的场景中填写 Dao Commit 候选；普通任务写“不适用”。

## 使用原则

- 下一步要写成接棒人的第一刀，而不是抽象的未来愿景。
- 未完成、未测或风险未清必须如实写出；“差不多”不是状态。
- 交当前单一主线，不把无关任务混入同一张卡。
- 路径、状态、证据优先于长篇叙述。

## 最小使用示例

```text
我要换一个模型继续修这个问题。请用 dao-handoff 输出一份接棒包：
包含当前工作树、已做验证、尚未确认的风险，以及下一位第一步该检查什么。
```

## 它不会替代什么

- 新任务的目标与验收对齐：用 [`dao-grill`](dao-grill.md)。
- 项目身份与传承接入：用 [`dao-intro`](dao-intro.md)。
- 是否可交付的收口判断：用 [`dao-review`](dao-review.md)。

## 进一步阅读

- 运行时入口：[`skills/dao-handoff/SKILL.md`](../../skills/dao-handoff/SKILL.md)
- 输出模板：[`references/output-templates.md`](../../skills/dao-handoff/references/output-templates.md)
- 示例：[`references/examples.md`](../../skills/dao-handoff/references/examples.md)
