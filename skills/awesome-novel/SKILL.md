---
name: "awesome-novel"
description: "7个agent协作完成从设定到归档的小说创作工作流系统"
---

# Novel — 小说创作工作流

和 AI 协作写小说的工作流系统。7 个 agent 协作完成从设定到归档的完整写作流程。

## 核心架构
- **novel-agent**（总指挥）— 调度所有子 agent
- **volume-planner** — 规划卷纲
- **chapter-planner** — 生成章纲
- **prompt-crafter** — 组装提示词
- **writer** — 写正文
- **reader** — 深度评审（可选）
- **updater** — 归档 + lore-keeping

## 检测流程
- `story.yaml` 存在 → 旧版 2.x → 自动迁移
- `story.md` 不存在 → 询问后运行 `init.py`
- `story.md` 存在 → 已有项目 → 检查同步后交给 novel-agent

## 初始化
`python tools/init.py [project-path] [--genre <编号>]` — 创建项目骨架、agent 定义、知识库。

## 项目目录结构
```
{project-name}/
├── story.md              # 项目索引
├── settings/             # 世界观/风格/题材/角色
├── volumes/              # 卷纲
├── chapters/             # 章纲
├── prompts/              # 提示词
├── archives/             # 定稿/草稿
├── .agent/               # 状态追踪 + agent间通信
└── .claude/agents/       # Agent 定义
```

## Agent 协作
novel-agent 是唯一调度者，通过 `.agent/task/*-order.md` 文件通信。子 agent 完成任务后清理 order 文件。

## 设定讨论
novel-agent 与作者讨论后，由 updater 写入 `settings/` 文件。novel-agent 不得直接写设定文件。
