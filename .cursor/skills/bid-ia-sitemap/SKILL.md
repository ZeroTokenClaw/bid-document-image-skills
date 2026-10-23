---
name: bid-ia-sitemap
description: Designs one information architecture or menu map at a time from 招标文件, 投标文件, or 技术方案. Use for 信息架构, 站点地图, 菜单结构, and navigation hierarchy. Draws with SVG. Do not use for wireframes, UI mockups, or function trees that are not navigation.
---

# 招投标信息架构图

一张图只表达一套导航或菜单。节点名称与层级使用界面清单或需求中的信息结构。页面里的字段和视觉样式不在本图展开。

首页或入口在上方，下级页面按层级展开。外部链接和权限差异只在原文写明时标注。菜单过深时按一级栏目拆成多张图。

低保真页面交给 `bid-wireframe`。高保真界面交给 `bid-ui-mockup`。软件功能分解交给 `bid-function-tree`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构栏目和按钮。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
