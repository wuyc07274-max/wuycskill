# Claude Skills 技能库

一套适用于 Claude 桌面版 / Claude Code 的 **Claude Skills** 集合，覆盖文档处理、AI 绘图、小红书内容创作、学术论文转化、数学/化学教学、视频生成、浏览器自动化等场景。

每个技能是一个独立目录，包含 `SKILL.md`（技能说明与使用指南）以及所需的辅助脚本、模板或资源文件。

## 目录

| 技能 | 说明 |
|---|---|
| [awesome-novel](skills/awesome-novel/SKILL.md) | 7 个 agent 协作完成从设定到归档的小说创作工作流系统 |
| [chemistry-preview](skills/chemistry-preview/SKILL.md) | 苏教版高中化学双模式工具：预习文档生成 + 试卷/作业生成 |
| [chinese-novelist](skills/chinese-novelist/SKILL.md) | 分章节创作中文小说，支持长篇创作、中断续写、自动校验 |
| [consolidate-memory](skills/consolidate-memory/SKILL.md) | 反思式整理记忆文件：合并重复、修正过期事实、精简索引 |
| [frontend-design](skills/frontend-design/SKILL.md) | 前端界面视觉设计指导（Apache 2.0 授权） |
| [knowledge-2-web](skills/knowledge-2-web/SKILL.md) | 将知识文章内容转换为精美的交互式网页，自动生成配图 |
| [manimgl-best-practices](skills/manimgl-best-practices/SKILL.md) | ManimGL（3Blue1Brown 的 OpenGL 动画引擎）最佳实践 |
| [math-preview-doc](skills/math-preview-doc/SKILL.md) | 人教版高中数学：生成预习文档（含配图知识点和习题）+ 跨章节搜题组卷 |
| [midjourney](skills/midjourney/SKILL.md) | Midjourney 提示词工程与图片评分助手（V8.1/V7/niji 7） |
| [notebooklm](skills/notebooklm/SKILL.md) | 查询 Google NotebookLM 笔记本，获取基于来源、带引用的回答 |
| [opencli-adapter-author](skills/opencli-adapter-author/SKILL.md) | 为网站编写 OpenCLI 适配器，或为已有站点添加命令 |
| [opencli-autofix](skills/opencli-autofix/SKILL.md) | OpenCLI 适配器命令失败时自动修复 |
| [opencli-browser](skills/opencli-browser/SKILL.md) | 通过 OpenCLI 驱动真实 Chrome 窗口：检查、填表、点击流程、提取数据 |
| [opencli-usage](skills/opencli-usage/SKILL.md) | OpenCLI 总览：发现适配器、通用参数、输出格式 |
| [paper-2-web](skills/paper-2-web/SKILL.md) | 将学术论文转化为交互式网站、演示视频和会议海报 |
| [planning-with-files](skills/planning-with-files/SKILL.md) | Manus 风格基于文件的复杂多步任务规划 |
| [pro-deck-builder](skills/pro-deck-builder/SKILL.md) | 创建精致的 HTML 幻灯片和可打印 PDF 咨询交付物 |
| [qiuzhi-skill-creator](skills/qiuzhi-skill-creator/SKILL.md) | 引导用户一步步创建 Claude Skill 的交互式 SOP |
| [remotion](skills/remotion/SKILL.md) | Remotion（React 编程化视频创作）最佳实践 |
| [schedule](skills/schedule/SKILL.md) | 创建或更新自动运行的计划任务 |
| [seedance-20](skills/seedance-20/SKILL.md) | Seedance 2.0 文生视频/图生视频/视频转视频/参考图转视频/音频与 API |
| [setup-cowork](skills/setup-cowork/SKILL.md) | Cowork 引导式设置：安装匹配插件、试用技能、连接工具 |
| [skill-creator](skills/skill-creator/SKILL.md) | 创建新技能、改进现有技能并评估技能表现 |
| [xiaohongshu](skills/xiaohongshu/SKILL.md) | 小红书内容工具：搜索、推荐、帖子详情、评论、用户主页、热点跟踪 |
| [xiaohongshu-cover-generator](skills/xiaohongshu-cover-generator/SKILL.md) | 根据用户主题生成小红书风格封面图 |
| [xiaohongshu-images](skills/xiaohongshu-images/SKILL.md) | 将 Markdown/HTML 转换为小红书 3:4 比例的样式化图片 |
| [xiaohongshu-note-analyzer](skills/xiaohongshu-note-analyzer/SKILL.md) | 全面分析小红书笔记：内容质量、关键词优化、标题吸引力、敏感内容风险 |

## 安装方法

### 在 Claude 桌面版中安装

将技能目录复制到 Claude 的技能目录中（具体路径取决于你的 Claude 应用安装位置），或在 Claude 中通过技能管理界面导入。

### 在 Claude Code 中安装

```bash
# 克隆本仓库
git clone https://github.com/wuyc07274-max/wuycskill.git

# 复制需要的技能（以 midjourney 为例）
cp -r claude-skills/skills/midjourney ~/.claude/skills/
```

重启 Claude 后，对应技能即可在会话中生效。

## 许可证

本仓库中的技能遵循各自目录内的许可证：

- `frontend-design/` — [Apache License 2.0](skills/frontend-design/LICENSE.txt)
- 其余技能无附带许可证，作者保留所有权利。使用前请与作者联系获得授权。

## 致谢与声明

- 部分技能依赖第三方服务或 API（如 Midjourney、Google NotebookLM、Seedance、小红书等），请遵守相应服务的条款。
- 本仓库由 [Yusheng](https://github.com/wuyc07274-max) 维护，欢迎通过 Issue 或 Pull Request 贡献技能。
