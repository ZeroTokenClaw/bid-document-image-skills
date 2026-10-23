# 招投标文档图片设计技能

一套给 Cursor 使用的项目技能。根据招标文件、投标文件和技术方案，把架构图、流程图、拓扑图、部署图和其他标书配图逐张设计并生成。

许可：MIT。

## 使用

把本仓库的 `.cursor/skills/` 放到目标项目根目录，或直接在本仓库中放入招标文件、投标文件和技术方案。需要出图时说明图片用途，智能体会先读总流程，再按图种读取对应技能。

总流程：`.cursor/skills/bid-document-image-design/SKILL.md`

成图写入项目内的 `bid_images/`：

```text
bid_images/
├── 01_图片设计清单.xlsx
├── 02_图片索引.md
├── prompts/
├── generated/
└── review/
```

精确文字和结构使用 SVG、HTML 或 Mermaid，再导出 PNG。场景、产品、海报、网站素材和分镜使用 Cursor 内置图像工具，不需要单独配置 OpenAI API Key。外部模型只在明确要求时使用。

每张图单独设计、单独生成、单独校验。不合并多张图，不编造原文没有的模块、设备、接口和指标。

## 技能

| 类型 | 技能 |
| --- | --- |
| 架构图 | `bid-architecture-diagram` |
| 流程图 | `bid-flowchart` |
| 拓扑图 | `bid-topology-diagram` |
| 部署图 | `bid-deployment-diagram` |
| 数据关系图 | `bid-data-relationship-diagram` |
| 数据治理图 | `bid-data-governance-diagram` |
| 项目实施图、时间轴 | `bid-implementation-roadmap` |
| 场景、设备、概念配图 | `bid-scene-illustration` |
| 产品效果、机器人产品、白底图 | `bid-product-render` |
| 界面设计稿 | `bid-ui-mockup` |
| 信息图 | `bid-infographic` |
| 海报、封面 | `bid-poster` |
| 网站素材 | `bid-website-asset` |
| 数字孪生大屏 | `bid-dashboard-visual` |
| 线框图 | `bid-wireframe` |
| 标识 | `bid-logo` |
| 图标 | `bid-icon` |
| 组织架构 | `bid-org-chart` |
| 时序图 | `bid-sequence-diagram` |
| 安全架构 | `bid-security-architecture` |
| 机房与机柜布置 | `bid-room-layout` |
| 接口关系 | `bid-interface-diagram` |
| 现状与目标对照 | `bid-comparison-diagram` |
| 系统上下文 | `bid-context-diagram` |
| 业务架构 | `bid-business-architecture` |
| 功能结构 | `bid-function-tree` |
| 状态图 | `bid-state-diagram` |
| 用例图 | `bid-usecase-diagram` |
| 甘特图 | `bid-gantt` |
| 工作分解 | `bid-wbs` |
| 责任矩阵 | `bid-raci` |
| 运维体系 | `bid-ops-architecture` |
| 容灾备份 | `bid-dr-architecture` |
| 点位分布 | `bid-site-layout` |
| 迁移切换 | `bid-migration-plan` |
| 服务蓝图 | `bid-service-blueprint` |
| 信息架构、菜单 | `bid-ia-sitemap` |
| 应急响应 | `bid-emergency-plan` |
| 培训体系 | `bid-training-plan` |
| 用户旅程 | `bid-user-journey` |
| 质量管理 | `bid-quality-system` |
| 测试策略 | `bid-test-strategy` |
| 验收 | `bid-acceptance` |
| 风险矩阵 | `bid-risk-matrix` |
| 构建发布 | `bid-cicd` |
| 环境晋级 | `bid-environment-promotion` |
| 数据模型 | `bid-data-model` |
| 数据分级分类 | `bid-data-classification` |
| 权限模型 | `bid-permission-model` |
| 审计链路 | `bid-audit-chain` |
| 云资源 | `bid-cloud-resource` |
| 存储架构 | `bid-storage-architecture` |
| 集成架构 | `bid-integration-architecture` |
| 访问矩阵 | `bid-access-matrix` |
| 服务等级 | `bid-sla-service` |
| 人员进场 | `bid-staffing-plan` |
| 知识转移 | `bid-knowledge-transfer` |
| 供货到货 | `bid-supply-plan` |
| 场景分镜 | `bid-storyboard` |
| 已有图片的局部编辑 | `bid-image-edit` |
| 栅格图生成 | `imagegen` |
