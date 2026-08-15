---
name: "xiaohongshu"
description: "小红书内容工具：搜索、推荐、帖子详情、评论、用户主页、热点跟踪"
---

# 小红书 MCP Skill

基于 xiaohongshu-mcp 封装的小红书内容工具。

## 使用场景
- 搜索小红书内容
- 获取首页推荐列表
- 获取帖子详情（包括互动数据和评论）
- 发表评论到帖子
- 获取用户个人主页
- 热点跟踪、话题报告、舆情分析

## 快速开始
```bash
cd scripts/
./install-check.sh   # 检查依赖
./start-mcp.sh       # 启动 MCP 服务
./status.sh          # 检查登录状态
./search.sh "关键词"  # 搜索内容
```

## MCP 工具
check_login_status, search_feeds, list_feeds, get_feed_detail, post_comment_to_feed, reply_comment_in_feed, user_profile, like_feed, favorite_feed, publish_content, publish_with_video

## 热点跟踪
```bash
./track-topic.sh "话题" --limit 5 --output report.md
```

## 长图导出
搜索结果或帖子详情导出为带文字注释的 JPG 长图。

## 注意事项
- 首次运行会下载 headless 浏览器（~150MB）
- 发布限制：标题≤20字符，正文≤1000字符，日发布≤50条
