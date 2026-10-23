---
name: bid-room-layout
description: Designs one equipment-room or rack layout at a time from 招标文件, 投标文件, or 技术方案. Use for 机房平面, 机柜布置, 工位布局, and physical placement. Draws a plan view in SVG. Do not use for logical deployment, network topology, or product renders.
---

# 招投标机房与机柜布置图

一张图只画一个平面或一排机柜。房间、机柜、通道和设备位以原文为准，不按常规机房自行补齐。

## 表达边界

本图表达物理位置和尺寸关系。服务安装在哪类环境交给 `bid-deployment-diagram`。网络链路交给 `bid-topology-diagram`。单台设备外观交给 `bid-product-render`。

## 构图

平面图采用俯视。入口、通道和机柜排沿实际相对位置排列；原文给出尺寸时按同一比例标注，没有尺寸时只保留相对位置并标注“尺寸待确认”。

机柜图采用正面柜列。每个 U 位只填写原文点名的设备。空位保持空白，不填装饰设备。

## 绘制

用 SVG 绘制，再导出 PNG。名称和尺寸文字不小于 18px。不用图像模型生成平面或机柜图。

## 禁止

虚构机柜数量、U 位、空调、消防和桥架。使用 3D 机房效果代替布置图。把多房间画进不可读的一张总平面。

## 校验

每个设备和通道都能指回原文。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
