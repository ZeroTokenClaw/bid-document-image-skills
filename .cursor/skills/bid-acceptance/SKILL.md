---
name: bid-acceptance
description: Designs one acceptance diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 验收流程, 验收资料, acceptance parties, and pass or reject outcomes. Draws with SVG. Do not invent acceptance criteria or replace the test strategy.
---

# 招投标验收图

一张图只覆盖一次验收。参与方、资料、检查项和结论以招标验收要求或投标响应为准。

从验收申请到资料核验、现场检查、结论和整改复验排列。不通过只在原文规定整改时回到对应步骤。结论用语使用原文，不改成内部评审通过。

测试层次交给 `bid-test-strategy`。项目里程碑交给 `bid-implementation-roadmap`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构验收分数和签字人。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
