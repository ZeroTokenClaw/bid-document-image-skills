---
name: bid-comparison-diagram
description: Designs one current-versus-target comparison diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 现状与目标对照, 方案对比, and before-after figures. Draws with SVG or HTML. Do not invent the current state or merge unrelated diagrams.
---

# 招投标对照图

一张图只对照一个主题。左右或上下两栏分别使用原文中的两个对象，例如现状与目标、招标要求与投标响应。原文只有一侧时，不编造另一侧。

## 构图

两栏等宽对齐。同一行只放一组对应项，行间留白。差异用栏内文字说明，不使用奖杯、上升箭头或装饰性大红叉，除非原文要求标记满足与不满足。

满足情况以投标响应为准。指标没有响应值时标“待确认”。

## 绘制

用 SVG 或 HTML 绘制，再导出宽 2400px 的 PNG。行标题不小于 18px。不用图像模型生成对照表式图片。

## 禁止

把多类架构、流程和部署塞进同一张对照。虚构现状缺陷和响应指标。使用营销海报布局。

## 校验

每一行的两侧都能指回原文。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
