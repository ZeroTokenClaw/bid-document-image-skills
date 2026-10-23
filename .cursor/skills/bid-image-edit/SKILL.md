---
name: bid-image-edit
description: Edits one existing bid image at a time with Cursor's built-in GenerateImage tool. Use for 参考图编辑, 局部替换, 抠图, 换背景, 风格迁移, 合成, 草图转效果, 文字替换, and preserving a product or person identity. Requires a source image. Do not use to create architecture, flowchart, topology, or deployment diagrams.
---

# 招投标图片编辑

先确定原图路径和这一次只修改的一项，再按 `.cursor/skills/imagegen/SKILL.md` 执行。原图放入 `reference_image_paths`。新文件使用版本名，不覆盖原图。

每次只选一种编辑：

| 编辑 | 用例 | 必须保持 |
| --- | --- | --- |
| 只替换画面文字 | `text-localization` | 布局、间距和图像 |
| 保持同一设备或人物 | `identity-preserve` | 外形、比例、姿态和身份 |
| 替换指定物体 | `precise-object-edit` | 机位、光线和其余物体 |
| 只改光线或天气 | `lighting-weather` | 主体、几何和构图 |
| 去除背景 | `background-extraction` | 主体边缘和标签 |
| 借用参考风格 | `style-transfer` | 原图的对象和数量 |
| 把主体放入另一场景 | `compositing` | 场景透视，并匹配比例与光线 |
| 由草图生成效果 | `sketch-to-render` | 草图的布局、比例和视角 |

矢量原图中的文字、模块和连线应直接改 SVG、HTML 或 Mermaid，不把精确结构送进图像编辑。

提示词每轮重复“只修改 X，保持 Y 不变”。参考图要分别标明编辑对象、风格参考或被合成主体。不得在编辑中补入原文没有的设备、指标和品牌。

校验主体是否漂移、文字是否错、边缘是否有光晕。结果写入 `bid_images/generated/`，编辑说明写入 `bid_images/prompts/`。
