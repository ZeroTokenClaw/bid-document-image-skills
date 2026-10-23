---
name: bid-raci
description: Designs one responsibility matrix at a time from 招标文件, 投标文件, or 技术方案. Use for RACI, 责任分配矩阵, and task-to-role assignments. Draws an editable table with HTML. Do not invent responsibilities or replace the organization chart.
---

# 招投标责任矩阵

一张矩阵只对应一组任务和一个角色范围。行是原文中的任务或交付物，列是原文中的角色。单元格只使用原文已经明确的负责、审核、配合或知情，不把空单元格填成负责。

角色来自组织方案，任务来自实施或服务方案。人员姓名未确定时使用岗位名。组织汇报线交给 `bid-org-chart`。

用 HTML 表格绘制，保证文字可复制，再导出 PNG。不用图像模型生成矩阵。禁止用颜色深浅代替缺失的责任说明。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
