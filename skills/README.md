# Dao Skills

每个目录都是一个独立 skill。安装时应保留该目录内的 `SKILL.md` 及其 `references/`、协议文件或数据文件；不要只复制 `SKILL.md`，否则模板、样例或 Dao Commit 的卦象数据会丢失。

## 推荐接入顺序

1. 先安装 `dao-grill`、`dao-handoff`、`dao-review`，跑通一轮真实任务。
2. 只在 `feature -> dev` 或 `dev -> main` 合并 / squash 收口时接入 `dao-commit`。
3. 当主线失焦或经验需要判断归属时，再接入 `dao-role-map`、`dao-return-dao`。

## 使用边界

- skill 负责帮助人和 AI 做局部判断，不取代项目自身规范、测试、review 或最终决策。
- 目录可按使用的 AI 工具要求复制或软链接到其 skill 目录。
- `dao-commit` 需要 AI 先读取 Git 事实；最终锚点仍由人确认。详见 [dao-commit/SETUP.md](dao-commit/SETUP.md)。

完整流程见 [开发运行流程](../docs/02-开发运行流程.md) 和 [Skills 协作地图](../docs/04-Skills协作地图.md)。
