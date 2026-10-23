---
name: bid-permission-model
description: Designs one permission model at a time from 招标文件, 投标文件, or 技术方案. Use for 权限模型, RBAC, roles, and resource grants. Draws with SVG or HTML. Do not invent grants or replace organization charts and RACI matrices.
---

# 招投标权限模型图

一张图只表达角色、资源和授权关系。角色名、资源名和允许的操作以权限设计为准。未写明的操作不标成允许。

角色放在左侧，资源放在右侧，中间用短标签表示操作。角色继承只在原文定义时画出。人员姓名不替代角色。

岗位汇报交给 `bid-org-chart`。项目任务责任交给 `bid-raci`。菜单层级交给 `bid-ia-sitemap`。

用 SVG 或 HTML 绘制并导出 PNG。不用图像模型。禁止虚构管理员超级权限。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
