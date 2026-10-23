---
name: bid-poster
description: Designs one bid-document poster or cover visual at a time from 招标文件, 投标文件, or 技术方案. Use for 海报, 封面, 展板, and 宣传页. Generates the visual through the imagegen skill and keeps long text editable. Do not use for architecture, flowchart, topology, deployment, or technical diagrams.
---

# 招投标海报与封面

一张海报只服务一个用途：封面、章节隔页或展板。标题、项目名和主视觉以原文为准，不编写新的宣传承诺。

## 构图

竖版海报使用 `aspect_ratio` `3:4` 或 `9:16`，封面横图使用 `16:9`。主视觉占画面一侧，另一侧保留连续空白，供文档标题排版。

长标题、参与单位和日期不放进图像模型。用 HTML 或文档排版叠加到已生成的无字底图上。图像中最多保留一句已核对的短标题。

生成执行 `.cursor/skills/imagegen/SKILL.md`，用例 `stylized-concept` 或 `photorealistic-natural`。画面只包含原文中的项目对象，不加入无关城市、机器人群像和奖杯。

## 禁止

虚构获奖、资质、性能和客户标志。使用霓虹、粒子和强烈光斑。把架构图缩小后贴进海报冒充技术说明。多张海报共用同一背景只换标题。

## 校验

核对项目名称、主视觉对象和留白是否足够放置标题。底图与最终合成图分别保存到 `bid_images/generated/`，提示词写入 `bid_images/prompts/`。
