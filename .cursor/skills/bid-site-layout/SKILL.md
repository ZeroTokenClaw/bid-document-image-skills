---
name: bid-site-layout
description: Designs one site or point-layout diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 点位分布, 平面布点, 摄像机点位, and robot or terminal positions. Draws a schematic plan in SVG from confirmed points. Do not invent coordinates or replace room rack layouts.
---

# 招投标点位分布图

一张图只表示一个场地或一张楼层。点位名称、数量和相对位置以点位表、平面说明或技术方案为准。没有坐标时只保持原文描述的相对关系，并标注“坐标待确认”。

用俯视示意，不使用真实地图截图，除非项目提供了可发布的底图。不同点位类型用不同线框符号，并给出图例。通道和房间只作为定位参照。

机柜 U 位交给 `bid-room-layout`。设备外观交给 `bid-product-render`。

用 SVG 绘制并导出 PNG。不用图像模型补画点位。禁止虚构摄像机、机器人和网络点。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
