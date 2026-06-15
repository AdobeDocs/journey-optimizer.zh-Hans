---
solution: Journey Optimizer
product: journey optimizer
title: 使用MCP客户端(Beta)
description: 了解如何使用MCP服务器将Adobe Journey Optimizer连接到MCP客户端
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta 版" type="Informative"
role: User, Developer
level: Beginner, Intermediate
subfeature_v2: []
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 7ced44f92f816d83d9a9ad667b4322dcb5930741
workflow-type: tm+mt
source-wordcount: 1369
ht-degree: 1%

---

# 使用MCP客户端 {#ajo-mcp}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;获取[!DNL Adobe Journey Optimizer] MCP服务器的分步概述 — 从模型上下文协议基础知识和支持的客户端，到可用的工具、示例提示、设置先决条件、连接步骤和常见问题的解答。

>[!ENDSHADEBOX]

通过[!DNL Adobe Journey Optimizer] MCP集成，您可以使用纯语言提示查询促销活动、历程和优惠，而无需编写API调用或导航产品屏幕。 此页面介绍集成的工作方式、您可以对其执行的操作以及如何入门。

>[!AVAILABILITY]
>
>[!DNL Adobe Journey Optimizer] MCP服务器当前在&#x200B;**Claude Web**、**Claude Desktop**&#x200B;和&#x200B;**Cursor**&#x200B;中可用。 未来版本中将增加对其他MCP兼容应用程序的支持。

## Beta、安全和法律声明 {#mcp-notices}

**Beta文档声明：**&#x200B;此文档涵盖了Beta的一项功能，并不构成最终文档。 此处描述的内容与Beta版本有关，在正式发布之前可能会发生更改。 Adobe不对本文档的完整性或准确性做出任何表示。

使用Adobe Journey Optimizer MCP Server (Beta) (“Beta”)，即表示您在此确认Beta按“原样”提供&#x200B;**，不提供任何形式的担保**。 Adobe没有义务维护、更正、更新、更改、修改或以其他方式支持Beta。 建议您谨慎使用，切勿依赖此类Beta和/或随附材料的正确功能或性能。 Beta被视为Adobe的机密信息。 您向Beta提供的任何“反馈”（有关Beta的信息，包括但不限于您在使用Adobe时遇到的问题或缺陷、建议、改进和推荐）均会分配给Adobe，其中包括针对该反馈的所有权利、标题和兴趣。

>[!WARNING]
>
>模型上下文协议(MCP)是一种新兴的开源标准，可能会带来安全性或可靠性风险。 Adobe MCP服务器集成和相关文档按“原样”提供，不提供任何类型的担保。
>
>将MCP客户端或服务器连接到Adobe产品是客户选择的配置。 客户负责评估任何MCP集成的安全性和适用性。 Adobe对于因错误配置、滥用MCP、第三方实施中的漏洞或通过支持MCP的工作流执行的意外操作而产生的问题，概不负责。
>
>为了降低风险，Adobe鼓励您在生产使用之前在沙盒环境中测试集成，并在确认或依赖集成之前，仔细审查和验证所有MCP启动的操作和响应。

## 什么是模型上下文协议？ {#mcp-overview}

营销和客户体验团队越来越依赖基于聊天的应用程序和开发人员工具（如Anthropic Claude、OpenAI ChatGPT、Cursor和Microsoft Copilot Studio）来简化日常工作。 这些应用程序支持&#x200B;**模型上下文协议(MCP)**，这是一个开放标准，允许应用程序以统一的方式向大型语言模型(LLM)公开后端工具。

[!DNL Adobe Journey Optimizer]现在提供了一个MCP服务器，该服务器直接在任何MCP兼容的应用程序中显示活动和沙盒操作。 通过[!DNL Adobe Journey Optimizer] MCP集成，不同的角色可以围绕相同的编排数据进行协作 — 无需针对[!DNL Adobe Journey Optimizer] REST API编写查询或导航多个UI屏幕。 客户可以通过对话方式描述其意图，并让LLM调用相应的MCP工具。

## 主要功能 {#mcp-capabilities}

[!DNL Adobe Journey Optimizer] MCP服务器允许您直接从AI助手检查、汇总营销活动、历程和选件并排除其故障。 所有操作都是&#x200B;**只读** — MCP服务器表面将API作为纯语言答案进行检索，因此您可以：

* **了解历程逻辑** — 获取任何历程的分支、条件和操作的可读摘要。
* **即时查看营销活动** — 以纯语言询问营销活动状态和渠道配置并即时获得答案，无需浏览菜单或手动提取报告。
* **提早发现问题** — 即时发现停止的营销活动、孤立的草稿和渠道配置问题，以便您的团队可以快速采取行动。
* **围绕实时数据协作** — 营销人员、营销活动经理和利益相关者均可通过其AI助手查询相同的实时[!DNL Adobe Journey Optimizer]数据，从而更轻松地对齐、决定和移动数据。
* **审核您的编排组合** — 查看营销活动的完整状态，而无需解析JSON或跨产品屏幕跳转。

## 可用工具 {#mcp-tools}

[!DNL Adobe Journey Optimizer] MCP服务器公开以下工具：

**促销活动工具**

| 工具 | 描述 |
|---|---|
| **列出营销活动** | 浏览您的[!DNL Adobe Journey Optimizer]营销活动。 支持按状态（草稿、实时、已停止、已完成）过滤。 |
| **获取营销活动** | 按ID获取特定营销活动的完整详细信息和配置，包括受众定位、计划、渠道和内容设置。 |
| **列出渠道配置** | 查看电子邮件、短信、推送或WhatsApp渠道的表面预设和品牌设置。 |

**历程工具**

| 工具 | 描述 |
|---|---|
| **获取所有历程** | 浏览[!DNL Adobe Journey Optimizer]沙盒中的所有历程。 |
| **获取历程** | 按ID获取特定历程的完整详细信息，包括其分支、条件和操作。 |
| **可视化您的历程** | 使用交互式工具呈现您的历程，以便直观地探索其结构和流程。 |

>[!NOTE]
>
>所有工具均为只读。 当前Beta版本不支持写入操作（创建、更新或删除对象）。

## 用例 {#mcp-use-cases}

以下示例显示如何使用自然语言与[!DNL Adobe Journey Optimizer] MCP服务器交互：

| 目标 | 示例提示 |
|---|---|
| **营销活动和历程概述** | 显示我的所有Journey Optimizer营销活动/历程/在Journey Optimizer中设置了多少营销活动/历程？ |
| **状态审核** | 哪些营销活动/历程当前处于实时状态？ /列出任何暂停或停止的营销活动/历程。 |
| **营销活动和历程详细信息** | 获取营销活动[ID]的完整详细信息/向我介绍在营销活动[ID]中设置的所有内容。 /获取历程[ID]的完整详细信息/向我介绍历程[ID]中设置的所有内容。 |
| **受众和定位** | 营销活动/历程[ID]的目标受众是哪些？ /对营销活动/历程[ID]设置了哪些资格规则？ |
| **计划和时间** | 何时计划运行营销活动[ID]？ /营销活动[ID]是一次性发送还是定期发送？ |
| **故障排除** | 为什么营销活动[ID]可能未发送？ /查看营销活动[ID]的设置以了解任何问题。 |
| **渠道配置** | 我的沙盒中有哪些渠道预设可用？ /显示我的所有电子邮件渠道配置。 |
| **渠道审核** | 哪些渠道配置缺失或不完整？ /在所有渠道中我有多少渠道配置？ |

## 先决条件 {#mcp-prerequisites}

在将[!DNL Adobe Journey Optimizer] MCP服务器连接到MCP客户端之前，请确保：

* 您有一个有效的[!DNL Adobe Journey Optimizer]许可证。
* 您可以访问支持的MCP兼容应用程序（当前为Claude Web 、 Claude Desktop或Cursor ）。
* 您在[!DNL Adobe Journey Optimizer]中拥有查看营销活动、历程和优惠的必要权限。

## 连接[!DNL Adobe Journey Optimizer] MCP服务器 {#mcp-connect}

>[!NOTE]
>
>此集成位于Beta中。

您可以通过首选的MCP客户端连接[!DNL Adobe Journey Optimizer] MCP服务器，包括&#x200B;**Claude Web**、**Claude Desktop**&#x200B;和&#x200B;**Cursor**。

**通过MCP客户端连接**

在MCP客户端中设置MCP服务器时，请使用以下服务器端点URL：

`https://ajo-mcp.adobe.io/mcp`

**通过Claude Web或Claude Desktop连接**

要在Claude Web或Claude Desktop中设置MCP服务器，请转到&#x200B;**连接器**&#x200B;并选择&#x200B;**Adobe Journey Optimizer**。

## 常见问题 {#mcp-faq}

+++支持哪些MCP客户端？

[!DNL Adobe Journey Optimizer] MCP服务器当前可用于&#x200B;**Claude Web**、**Claude Desktop**&#x200B;和&#x200B;**Cursor**。 未来版本中可能会添加对其他MCP兼容应用程序的支持。
+++

+++我可以通过MCP访问哪些[!DNL Adobe Journey Optimizer]对象？

您可以访问营销活动、历程、选件和沙盒信息。 操作是只读的（检索API）；当前版本不支持写入操作。
+++

+++是否需要开发人员访问权限才能使用[!DNL Adobe Journey Optimizer] MCP服务器？

不是。 MCP服务器专为营销和技术人员而设计。 营销人员可以在任何支持的MCP客户端中使用自然语言提示与其交互，而开发人员也可以在支持MCP的开发人员工具中使用它。
+++

+++我的数据是否发送到MCP客户端提供商？

当您提交提示时，MCP客户端可能会将相关上下文（包括MCP服务器返回的[!DNL Adobe Journey Optimizer]数据）发送到其模型以供处理。 在连接到生产数据之前，请查看MCP客户端提供商的隐私和数据处理策略。
+++

+++我需要在[!DNL Adobe Journey Optimizer]中拥有哪些权限？

您需要对要查询的对象（营销活动、历程或选件）具有至少&#x200B;**查看**&#x200B;权限。 不需要写入权限，因为MCP服务器只执行读取操作。 如果您不确定当前的访问级别，请联系您的[!DNL Adobe Journey Optimizer]管理员。
+++

+++我可以在沙盒环境中使用MCP服务器吗？

可以。 MCP服务器遵循您的[!DNL Adobe Journey Optimizer]沙盒配置。 您可以查询特定于沙盒的数据，方法是在提示符下指定沙盒，或者使用限定于特定沙盒的凭据进行连接。
+++

