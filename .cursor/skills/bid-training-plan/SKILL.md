---
name: bid-training-plan
description: Designs one training-plan diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 培训体系, 培训对象, courses, and assessment. Draws with SVG. Do not invent course hours or replace the implementation roadmap.
---

# 招投标培训体系图

一张图只表达一套培训安排。培训对象、课程、方式和考核以培训方案为准。课时和通过标准没有原文时标“待确认”。

对象放在左侧，课程按实施顺序横向排列，考核放在对应课程之后。不同对象的课程不相同，不合并成一张无法区分的总表；对象差异大时拆成多张图。

项目阶段交给 `bid-implementation-roadmap`。岗位体系交给 `bid-org-chart`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构证书、讲师和培训人数。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
