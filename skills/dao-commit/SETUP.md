# Dao Commit Skill · 接入指南

本目录包含 Dao Commit 的通用 AI Skill 文件，兼容多种 AI CLI 工具。

## 文件说明

| 文件 | 用途 |
|------|------|
| `SKILL.md` | 核心规则文件，定义 AI 如何辅助生成 Dao Commit |
| `core-protocol.md` | 完整工程协议，补充格式、选卦和写作规则 |
| `trigrams.json` | 卦象结构与丰富工程参考；不提供机械卦名推荐 |
| `references/64卦选择检查.md` | 64 卦首轮确认的整体处境选择检查，运行时选卦入口 |

## 支持的 AI CLI

### OpenCode

将 skill 挂载到 OpenCode 的 skills 目录：

```bash
mkdir -p ~/.config/opencode/skills/dao-commit
cp SKILL.md ~/.config/opencode/skills/dao-commit/SKILL.md
cp core-protocol.md ~/.config/opencode/skills/dao-commit/core-protocol.md
cp trigrams.json ~/.config/opencode/skills/dao-commit/trigrams.json
```

### Claude Code

将 skill 挂载到 Claude Code 的 skills 目录：

```bash
mkdir -p ~/.claude/skills/dao-commit
cp SKILL.md ~/.claude/skills/dao-commit/SKILL.md
cp core-protocol.md ~/.claude/skills/dao-commit/core-protocol.md
cp trigrams.json ~/.claude/skills/dao-commit/trigrams.json
```

### Windsurf

将规律文件放在项目根目录的 `.windsurf/` 或通过全局配置引用：

```bash
mkdir -p .windsurf/skills/dao-commit
cp SKILL.md .windsurf/skills/dao-commit/SKILL.md
cp core-protocol.md .windsurf/skills/dao-commit/core-protocol.md
cp trigrams.json .windsurf/skills/dao-commit/trigrams.json
```

### 其他 AI CLI

大多数 AI CLI 支持以下方式之一：
1. 项目根目录的 `.opencode/skills/`、`.claude/skills/`、`.cursor/rules/` 等
2. 全局用户目录的对应路径

如 CLI 不支持 skill 机制，可将 `SKILL.md` 内容直接粘贴到对话中作为系统提示。

## 使用方式

当提交代码时，对 AI 说：

> 帮我写一个 Dao Commit，这次改动是 [描述你的改动]

AI 会按 SKILL.md 中定义的流程：
1. 先确认真实变化
2. 起草 subject
3. 推荐 type 和 scope
4. 给出 1-2 个卦象候选
5. 判断是否需要 body 和 footer

## 手动安装到当前项目

如果要在当前仓库启用本 skill（提交时让 AI 辅助生成）：

```bash
# 使用项目自带的 OpenCode skill 目录
mkdir -p .opencode/skills/dao-commit
cp skills/dao-commit/SKILL.md .opencode/skills/dao-commit/SKILL.md
cp skills/dao-commit/core-protocol.md .opencode/skills/dao-commit/core-protocol.md
cp skills/dao-commit/trigrams.json .opencode/skills/dao-commit/trigrams.json
```
