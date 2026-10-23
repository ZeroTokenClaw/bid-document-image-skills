---
name: bid-migration-plan
description: Designs one migration or cutover diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 迁移, 切换, 并行运行, and rollback. Draws with SVG. Do not invent a cutover window or replace the implementation roadmap.
---

# 招投标迁移切换图

一张图只描述一次迁移或切换。阶段顺序、冻结窗口、并行运行和回退条件以迁移方案为准。

从左到右排列准备、迁移、校验、切换和回退。回退从切换点走外侧返回，不穿过主路径。每个阶段只列该阶段的原文任务和判定标准。

总进度交给 `bid-implementation-roadmap` 或 `bid-gantt`。容灾站点关系交给 `bid-dr-architecture`。

用 SVG 绘制并导出宽 2400px 的 PNG。不用图像模型。禁止虚构停机时间和数据量。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
