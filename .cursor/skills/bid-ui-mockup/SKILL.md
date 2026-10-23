---
name: bid-ui-mockup
description: Designs one bid-document UI mockup at a time from 招标文件, 投标文件, or 技术方案. Use for 界面设计稿, 系统界面, Web 端, and 移动端页面. Exact labels use HTML; atmosphere mockups use the imagegen skill. Do not use for architecture, flowchart, topology, deployment, or dashboard scenes.
---

# 招投标界面设计稿

一张图只设计一个页面或一种状态。页面名称、菜单、字段和按钮以招标文件、投标文件或技术方案为准，不补充未写明的功能。

## 绘制方式

- 菜单、字段、状态和数据需要准确阅读：用 HTML 按页面绘制，再导出宽 2400px 的 PNG。这是默认方式。
- 只需要低保真氛围、且画面几乎没有文字：按 `.cursor/skills/imagegen/SKILL.md` 生成，用例 `ui-mockup`，`aspect_ratio` 用 `16:9`。

同一页面不得既用精确 HTML 又用图像模型各做一张来充数。原文要求多个页面时，每个页面单独出图。

## 构图

页面按真实阅读顺序排列：导航、标题、主操作、内容区、辅助信息。内容区只放该页原文中的模块。桌面端用横向浏览器画布，移动端用纵向单列，二者不混在一张图里。

色彩使用主色 `#1F3A4D` 和背景 `#F7F8F6`。组件对齐，间距一致。不画设备样机外壳，除非原文要求展示终端外观。

## 禁止

虚构图表数据、告警数量和用户姓名。用图像模型生成整屏中文后台冒充正式界面。把系统架构层画进页面。添加与该页无关的装饰插画。

## 校验

逐项核对导航和字段是否来自原文，文字是否被裁切或重叠。提示词或 HTML 说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
