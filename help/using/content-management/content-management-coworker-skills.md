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
source-git-commit: faea09992ef91725f52fed718a893f3a32198dd7
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 1%
---

# 内容管理的同事 {#content-management-coworker-skills}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解Adobe Journey Optimizer中可用的CX Coworker内容管理工具 — 浏览、创建、更新、克隆和发布内容模板、片段、登陆页以及历程/营销活动内联内容；跨渠道、区域设置、受众和变体规划营销活动策略并生成品牌内副本和图像；以及构建、审阅和分发可访问的电子邮件HTML — 提供详细指导、示例提示和最佳实践。

了解详情：

* [Journey Optimizer的同事技能](../start/ai-features.md#cx-coworker-skills) — 概述Journey Optimizer中跨历程、忠诚度和内容管理的同事技能。
* [同事文档](https://experienceleague.adobe.com/zh-hans/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"} — 同事的营销活动、聊天和项目功能概述。
* [同事聊天UI指南](https://experienceleague.adobe.com/zh-hans/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"} — 如何访问和导航同事聊天。

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

## 渠道内容 {#ce-channel-content}

>[!AVAILABILITY]
>
>渠道内容适用于有权访问CX Coworker的所有客户。 使用经过品牌培训的自定义模型生成图像时，需要具有对Firefly Services的生产访问权限。

渠道内容可简短地呈现历程、营销活动或提示信息，并将其转换为跨渠道、区域设置、受众和变体的有计划、品牌内复制和图像，包括最终的、可访问的组合电子邮件HTML。 内容可以探索和制定战略、编写、评估就绪性、修改并保存回活动解决方案（Adobe Journey Optimizer或其他支持的激活解决方案）。

### 可用技能

**渠道内容**&#x200B;插件下提供了以下技能：

* **编排内容创作** (`orchestrate-content-authoring`)

  在整个创作生命周期中，从简短、历程、营销活动或提示开始，构想、生成、查看和保存内容，包括文案、图像，以及跨受支持渠道的法规遵从性、可访问性和保真度检查。

* **浏览内容策略** (`explore-content-strategy`)

  在编写副本之前确定营销活动或消息的含义，在营销活动级别比较消息映射和接触点排序，在消息级别确定分区顺序、强调内容和CTA。

* **内容简介** (`content-brief`)

  将已批准的营销活动方向转换为具体的编写要求，包括语气、关键消息、优惠、必说要点、渠道、区域设置和变体，以及制作内容的计划。

* **生成内容** (`generate-content`)

  根据规定的受众、选件、音调、CTA和时长，为一个渠道起草单个全新营销消息或副本变体。 仅创建初稿。

* **检查内容准备情况** (`check-content-readiness`)

  评估现有内容（包括组装的电子邮件），以了解品牌声音、编辑质量、可访问性和合规性，然后显示可解释的阻止程序和后续步骤。

* **修改并重新生成内容** (`revise-regenerate-content`)

  对现有内容应用特定的、已确认的更改，例如修复审阅发现、调整色调、翻译或交换主题行或CTA，同时保留工件。

* **生成图像** (`generate-image`)

  生成并处理已批准投放位置的可视化图表，包括主页图像、裁切、叠加、变体或签名资产，并在应用计划之前确认计划。

* **评估内容设计** (`assess-content-design`)

  评估内容实际呈现的方式，包括层级、间距、图像、CTA投放位置和响应性，并建议更改副本或图像以弥补差距。

* **保存渠道内容** (`save-channel-content`)

  将批准的促销活动内容另存为草稿资源，或将其填充到Adobe Journey Optimizer或其他受支持的解决方案中的源模板中。

* **从Figma生成电子邮件** (`build-email-from-figma`)

  当副本、布局和图像应保持不变，而不涉及单独的布局计划时，直接从实时图像框架生成最终电子邮件HTML。

  +++如何使用此技能

  1. 登录到同事并转到&#x200B;**[!UICONTROL 设置]** > **[!UICONTROL 密钥]**。

     ![](assets/coworker-1.png)

  1. 在&#x200B;**[!UICONTROL 您的密钥]**&#x200B;下，单击&#x200B;**[!UICONTROL 添加]**。

  1. 在&#x200B;**[!UICONTROL Name]**&#x200B;中，输入`FIGMA_ACCESS_TOKEN`。

  1. 生成至少具有&#x200B;**文件内容的Figma Personal Access Token (PAT)：只读**&#x200B;范围。 [了解如何生成个人访问令牌](https://help.figma.com/hc/en-us/articles/8085703771159-Manage-personal-access-tokens#h_01JHJXYMB9CREBR8PB5VJ1Q5ME)。

  1. 将PAT粘贴到&#x200B;**[!UICONTROL 值]**&#x200B;中，然后单击&#x200B;**[!UICONTROL 保存]**。

  +++

* **品牌查找** (`brand-lookup`)

  在生成或评估品牌内内容的任何工作流之前，查找、解决并应用批准的品牌准则，包括语音、图像和法律。

### 提示最佳实践

1. **从简介开始**：预先提供营销活动目标、受众和渠道，以便内容计划反映您的预期范围。
1. **指定计划维度**：调出要在内容计划中表示的渠道、接触点、区域设置、受众和变体。
1. **包含品牌上下文**：引用您的品牌套件或语音准则，以便生成的文案和图像与品牌保持一致。
1. **状态字符限制**：显式提供通道字符限制，并在发布之前查看生成的副本以确认其适合。
1. **请求所有相关审核**：在将内容视为发送就绪之前，需要获得品牌、合规性、设计和辅助功能审核。
1. **保存前进行审核**：在请求同事将生成的内容保存回Adobe Journey Optimizer或其他支持的激活解决方案之前，先对其进行评估和编辑。

{{$include /help/_includes/do-not-localize/start/ai-augmented-content-management-coworker-skills.md}}
