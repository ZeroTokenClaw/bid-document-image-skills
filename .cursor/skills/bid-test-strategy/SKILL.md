---
name: bid-test-strategy
description: Designs one test-strategy diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 测试策略, 测试层次, test scope, and entry or exit criteria. Draws with SVG. Do not use for business flowcharts or acceptance ceremonies.
---

# 招投标测试策略图

一张图只说明一个测试范围。测试层次、对象、环境和通过标准以测试方案为准。原文没有单元、集成、性能或安全测试时不自行补层。

层次自上而下或自左向右排列。每层只列该层的对象和出入口条件。用例步骤不展开成业务流程。

质量门禁交给 `bid-quality-system`。验收组织交给 `bid-acceptance`。环境晋级交给 `bid-environment-promotion`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构覆盖率、并发数和缺陷数。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
