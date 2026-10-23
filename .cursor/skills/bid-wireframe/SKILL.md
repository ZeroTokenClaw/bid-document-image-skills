---
name: bid-wireframe
description: Designs one low-fidelity wireframe at a time from 招标文件, 投标文件, or 技术方案. Use for 线框图, 页面草图, 低保真界面, and grayscale layout. Draws with HTML or SVG. Do not use for finished UI mockups, dashboards, architecture, or flowcharts.
---

# 招投标线框图

一张图只画一个页面或一条不超过三个屏幕的连续低保真流程。区块名称以原文为准。

## 与界面稿的边界

线框图只表达区块、顺序和主操作，使用灰阶，不填真实数据和品牌色。需要精确菜单、字段和高保真外观时改用 `bid-ui-mockup`。

## 构图

按页面阅读顺序排列：导航、标题、主操作、内容区、辅助信息。桌面端横向，移动端纵向，同一张图只使用一种设备比例。

区块用细线矩形和短标签。图片位置用对角叉表示，不贴真实照片。三个屏幕的流程并排，屏幕之间只用顺序号连接，不画业务判断菱形。

## 绘制

用 HTML 或 SVG 绘制灰阶线框，再导出 PNG。宽 2400px，标签不小于 18px。不用图像模型生成带文字的线框。

## 禁止

虚构页面、价格方案和功能区块。使用彩色、真实照片、图标和装饰。把架构层画成页面区块。

## 校验

每个区块都能指回原文。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
