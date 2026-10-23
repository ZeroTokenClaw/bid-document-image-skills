---
name: bid-icon
description: Designs one bid-document icon at a time for a named function, device, or status in 招标文件, 投标文件, or 技术方案. Use for 图标, 功能图标, and status symbols. Draws matching icons as SVG on one grid. Do not use for logos, product photos, or technical diagrams.
---

# 招投标图标

每个图标单独设计、单独保存。一组图标必须共用 24 的倍数网格、同一线宽和同一圆角，但每个图形只表示一个原文中的对象。

## 构图

图标使用正面、填实或统一线框中的一种，全组不混用。图形占网格内侧约四分之三，不放背景场景。需要文字时，文字放在图标下方的标签中，不写进图形内部。

标签使用原文中的功能、设备或状态名称。原文没有的状态不画。

## 绘制

用 SVG 绘制，再导出 PNG。不用图像模型批量生成一组需要相互匹配的图标。单个无文字的氛围符号只有在用户明确要求栅格探索时，才按 `.cursor/skills/imagegen/SKILL.md` 生成，用例 `stylized-concept`，选定后重画为 SVG。

## 禁止

使用品牌形状、emoji 和写实设备照片。一张图塞入整套图标当作唯一交付。用图标墙代替架构图或功能列表。

## 校验

核对每个图标是否对应一个已确认名称，风格是否同组一致。文件写入 `bid_images/generated/`，说明写入 `bid_images/prompts/`。
