---
name: bid-access-matrix
description: Designs one network or zone access matrix at a time from 招标文件, 投标文件, or 技术方案. Use for 访问矩阵, zone access, allowed paths, and denied paths. Draws an editable table with HTML. Do not invent allow rules or replace topology diagrams.
---

# 招投标访问矩阵

一张矩阵只覆盖一组源区域和目标区域。允许、限制和禁止以网络安全方案为准。空单元格标“待确认”，不默认成允许或禁止。

行是源，列是目标。单元格写原文中的端口、协议或访问结论；没有端口时只写结论。设备图标和链路走向不画进矩阵。

网络节点交给 `bid-topology-diagram`。安全控制点交给 `bid-security-architecture`。

用 HTML 表格绘制再导出 PNG。不用图像模型。禁止虚构任意端口放行。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
