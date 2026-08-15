---
name: "knowledge-2-web"
description: "将知识文章内容转换为精美的交互式网页，自动生成配图"
---

# Knowledge to Web - 知识文章网页生成器

将知识文章内容转换为精美的交互式网页，自动生成配图，适用于历史、科学、文化等各类知识主题。

## 使用场景
教学辅助材料制作、知识科普文章可视化、历史事件深度解析、科学概念图解说明、文化知识卡片展示。

## 使用方法

### 方式一：提供JSON文件
```bash
python scripts/knowledge-to-web.py <content.json> [api_key] [--images N] [--style STYLE]
```

### 方式二：直接在对话中提供文章
1. 用户提供文章内容或主题
2. 使用 WebSearch 搜索相关资料，补充背景信息
3. 使用 Gemini Image API 生成配图
4. 生成完整的交互式HTML网页

## 工作流程
1. 接收文章内容
2. 分析文章结构，提取关键信息
3. 规划配图位置和风格
4. 生成配图（使用 Gemini Image API）
5. 构建交互式HTML页面
6. 输出最终网页文件

## 输出
生成 self-contained 的 HTML 文件，包含配图和交互效果。
