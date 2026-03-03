# Obsidian Native CLI Skill

一个面向 Codex 的 Obsidian 技能：在维护 Obsidian 笔记时，优先使用官方原生 `obsidian` CLI，而不是自造脚本或非官方命令。

## 能力范围

- 覆盖 Obsidian CLI 官方文档中的命令（按快照整理）
- 支持日常笔记维护：创建、读取、移动、重命名、搜索、标签、任务、属性
- 支持恢复与发布：`history`、`sync`、`publish` 相关命令
- 支持开发调试：`dev:*`、`eval`、插件与主题管理

## 仓库结构

- `SKILL.md`：技能主说明（触发语义 + 操作流程）
- `agents/openai.yaml`：UI 元信息
- `references/command-index.md`：命令/参数/flags 快速索引
- `references/commands.json`：结构化命令清单（可供脚本消费）
- `references/obsidian-cli-official.md`：官方文档快照（来源：<https://help.obsidian.md/cli>）

## 在 Codex 中使用

在对话里提到该技能或相关任务，例如：

- “用 obsidian CLI 批量整理我的 daily notes”
- “读取今天日志并追加待办，使用原生 obsidian 命令”
- “检查孤立笔记和无效链接”

如果你的环境支持技能路径触发，也可直接引用：

`[$obsidian-native-cli](<skill_path>/SKILL.md)`

> 将 `<skill_path>` 替换为本地实际技能目录。

## 维护与更新

当 Obsidian CLI 官方文档更新后，建议同步更新这 3 个文件：

1. `references/obsidian-cli-official.md`（官方文档快照）
2. `references/commands.json`（结构化命令）
3. `references/command-index.md`（面向人读的索引）

并确保 `SKILL.md` 的流程说明与新命令保持一致。

## 校验

可用 skill-creator 自带脚本校验：

```bash
python "$HOME/.codex/skills/.system/skill-creator/scripts/quick_validate.py" .
```

通过后再提交与推送。
