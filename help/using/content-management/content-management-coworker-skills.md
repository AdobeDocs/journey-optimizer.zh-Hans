---
solution: Journey Optimizer
product: journey optimizer
title: 内容管理的同事
description: 了解可用于发现、创建和管理CX Enterprise Coworker内容资源的Journey Optimizer内容管理工具，以及深入的指导和示例提示。
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 9f23a6f5-7221-4f87-95cd-047955ca33d5
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
    internal-label: Content management
subfeature_v2:
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
    internal-label: Templates
source-git-commit: 85784fbe98b5347f86899ce7811017cd368745ff
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 2%
---

# 内容管理的同事 {#content-management-coworker-skills}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解Adobe Journey Optimizer中可用的CX Enterprise Coworker内容管理工具 — 浏览、创建、更新、克隆和发布内容模板、片段、登陆页以及历程/营销活动内联内容 — 提供详细指导、示例提示和最佳实践。

了解详情：

* [Journey Optimizer的同事技能](../start/ai-features.md#cx-coworker-skills) — 概述Journey Optimizer中跨历程、忠诚度和内容管理的同事技能。
* [同事文档](https://experienceleague.adobe.com/zh-hans/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"} — 同事的营销活动、聊天和项目功能概述。
* [同事聊天UI指南](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"} — 如何访问和导航同事聊天。

>[!ENDSHADEBOX]

## 内容管理工具 {#content-management}

>[!AVAILABILITY]
>
>内容管理适用于所有有权访问同事的客户。

Journey Optimizer用户可以使用自然语言提示直接从同事中发现和管理内容资产，包括内容模板、片段、登陆页面和历程/营销活动内联消息内容。 它可让您从“告诉我我的内容”转到“构建、更新和发布内容”，而不离开对话。 此功能由适用于Journey Optimizer内容的15个可读写的MCP工具提供支持。

### 主要用例

1. **浏览并检查内容**

   * 列出可用的内容模板、片段或登陆页，并检索其结构、元数据和状态。
   * 检索在历程或营销活动操作节点上配置的内联消息内容。

   示例提示：
   * “列出我的电子邮件内容模板。”
   * “给我看看我的夏季促销活动可用的片段。”
   * “获取登陆页面123的详细信息。”
   * “为营销活动camp-789中的操作节点的电子邮件变体配置什么内容？”

1. **创建内容模板**

   * 为任何渠道创建新的内容模板。

   示例提示：
   * “使用此HTML内容创建一个名为‘夏季促销’的电子邮件模板。”
   * “创建一个名为‘Flash Alert’的新短信模板。”

1. **更新内容模板**

   * 完全替换现有模板的内容。

   示例提示：
   * “使用此新HTML正文更新模板abc-123。”

1. **创建、更新、克隆和发布片段**

   * 创建新的HTML或表达式片段。
   * 更新现有片段的内容或元数据。
   * 使用新名称克隆现有片段。
   * 提交草稿片段以供发布。

   示例提示：
   * “使用此标记创建名为‘促销横幅’的HTML片段。”
   * “更新片段frag-456以将其名称更改为‘促销横幅V2’。”
   * “克隆片段abc-123作为促销横幅 — 夏天（变体B）。”
   * “发布片段frag-456。”

1. **更新内联消息内容**

   * 替换营销活动或历程操作节点的内联消息中的一个渠道变体。
   * 列出在历程或营销活动操作节点上定义的渠道变体。

   示例提示：
   * “使用此新内容更新营销活动camp-789中操作节点的电子邮件变体。”
   * “此操作节点上定义了哪些渠道变体？”

### 范围

内容管理支持以下功能：

* **列出并获取内容模板**：浏览内容模板并检索其结构和元数据。
* **列出并获取片段**：浏览内容和表达式片段并检索其详细信息。
* **列出并获取登陆页面**：浏览登陆页面并检索其元数据和页面内容。
* **获取营销活动/历程内联内容**：检索在营销活动或历程操作节点上配置的内联消息内容，包括多语言变体。
* **创建内容模板**：为任何渠道创建新模板。
* **更新内容模板**：完全替换现有模板的内容。
* **创建、更新、克隆和发布片段**：创建新片段，更新现有片段，使用新名称克隆片段，并提交草稿片段以供发布。
* **更新内联消息内容**：替换促销活动/历程操作节点内联消息上的渠道变体（包括多语言变体），并列出操作节点上定义的渠道变体。

### 超出范围

目前不支持以下功能：

* **跨模板或片段的全文搜索**
* **模板或片段验证**（孤立的引用、断开的链接、已弃用的组件）
* **创建或发布登陆页面**
* **正在删除内容模板、片段或登陆页面**

### 提示最佳实践

1. **已知时引用ID**：在请求获取、更新、克隆或发布特定资产时，请提供模板、片段、登陆页面或营销活动/历程ID。
1. **明确了解渠道**：创建模板或片段时，请指定渠道或内容类型（电子邮件、HTML片段、表达式片段）。
1. **发布前确认**：在请求同事发布片段之前，请在创建或更新片段后查看片段的内容。
1. **提供完整的替换内容**：更新操作会完整替换内容，因此在提示中包含完整的HTML正文或变体内容。

{{$include /help/_includes/do-not-localize/start/ai-augmented-content-management-coworker-skills.md}}
