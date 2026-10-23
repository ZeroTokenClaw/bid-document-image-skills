---
name: bid-usecase-diagram
description: Designs one use case diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 用例图, actors, and user goals. Draws with SVG or Mermaid. Do not use for function trees, flowcharts, or UI mockups.
---

# 招投标用例图

一张图只表达一组角色与他们直接完成的目标。角色和用例名称使用需求原文。包含、扩展和泛化只在原文写明关系时画出。

角色放在两侧，用例放在系统边界内。一个角色对应的用例过多时，按业务目标拆成多张图。不把步骤写进用例椭圆。

功能分解交给 `bid-function-tree`。页面布局交给 `bid-wireframe` 或 `bid-ui-mockup`。

用 SVG 或 Mermaid 绘制并导出 PNG。不用图像模型。禁止虚构角色和用例。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
