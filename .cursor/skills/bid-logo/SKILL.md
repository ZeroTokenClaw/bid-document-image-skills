---
name: bid-logo
description: Designs one project logo or wordmark at a time when a bid document requires an original identity. Use for 项目标识, Logo, 文字标志, and monogram exploration. Final marks are SVG. Do not redraw the purchaser's existing logo or replace architecture diagrams.
---

# 招投标标识

只在投标方案需要项目标识，且原文没有规定必须沿用现有标志时新建设计。采购人、产品和合作方已有标志直接使用原文件，不重新生成。

## 构图

一张图只放一个标志，居中，四周留白充足。按原文选择一种：

- 图形标：单一可识别轮廓，一两色，无渐变。
- 字母标：只使用已确认的缩写。
- 文字标：项目名称逐字一致，字距均匀。

色彩从 `#1F3A4D` 与 `#F7F8F6` 中取色。多个探索方向分成多张图，不排在同一张展示板上充当成稿。

## 绘制

成稿用 SVG 绘制并导出 PNG。图像模型只可用于无文字的图形方向探索，用例 `logo-brand`，执行 `.cursor/skills/imagegen/SKILL.md`。选定方向后必须重画为 SVG，不把栅格图当作最终标识。

## 禁止

模仿已知商标。添加口号、立体字、样机和未确认的项目名称。用标识图代替技术图。

## 校验

核对名称拼写、留白和单色缩小后是否仍可识别。源文件与 PNG 写入 `bid_images/generated/`，说明写入 `bid_images/prompts/`。
