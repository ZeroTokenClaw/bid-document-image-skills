---
name: bid-staffing-plan
description: Designs one staffing plan diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 人员进场, staffing curve, roles by phase, and on-site plans. Draws with SVG from confirmed roles. Do not invent headcount or replace organization charts.
---

# 招投标人员进场图

一张图只表达各阶段投入的岗位。岗位和阶段以人员计划为准。人数只有在原文给出时才标注，否则只标岗位是否进场。

横轴是阶段，纵轴是岗位。每个交点表示该阶段是否承担工作。不画个人姓名和照片。

汇报关系交给 `bid-org-chart`。任务责任交给 `bid-raci`。日历工期交给 `bid-gantt`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构人月峰值和证书数量。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
