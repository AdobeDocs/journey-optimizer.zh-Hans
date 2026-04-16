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
hide: true
source-git-commit: 9450ff7b477ef3ef6825eb2c2feec77ffaec389f
workflow-type: tm+mt
source-wordcount: '1370'
ht-degree: 1%

---

# 使用MCP客户端(Beta) {#ajo-mcp}

>[!CAUTION]
>
>**Beta文档声明：**&#x200B;此文档涵盖了Beta的一项功能，并不构成最终文档。 此处描述的内容与Beta版本有关，在正式发布之前可能会发生更改。 Adobe不对本文档的完整性或准确性做出任何表示。
>
>© Adobe Inc.保留所有权利。 Adobe、Adobe徽标和Adobe Journey Optimizer是Adobe在美国和/或其他国家/地区的注册商标或商标。
>
>使用Adobe Journey Optimizer MCP Server (Beta) (“Beta”)，即表示您在此确认Beta按“原样”提供&#x200B;**，不提供任何形式的担保**。 Adobe没有义务维护、更正、更新、更改、修改或以其他方式支持Beta。 建议您谨慎使用，切勿依赖此类Beta和/或随附材料的正确功能或性能。 Beta被视为Adobe的机密信息。 您向Beta提供的任何“反馈”（有关Beta的信息，包括但不限于您在使用Adobe时遇到的问题或缺陷、建议、改进和推荐）均会分配给Adobe，其中包括针对该反馈的所有权利、标题和兴趣。

通过[!DNL Adobe Journey Optimizer] MCP集成，您可以使用纯语言提示查询促销活动、历程和优惠，而无需编写API调用或导航产品屏幕。 此页面介绍集成的工作方式、您可以对其执行的操作以及如何入门。

>[!AVAILABILITY]
>
>[!DNL Adobe Journey Optimizer] MCP服务器当前仅在&#x200B;**Claude Web**&#x200B;和&#x200B;**Claude Desktop**&#x200B;中可用。 未来版本中将增加对其他MCP兼容应用程序的支持。

## 什么是模型上下文协议？ {#mcp-overview}

营销和客户体验团队越来越依赖基于聊天的应用程序和开发人员工具（如Anthropic Claude、OpenAI ChatGPT、Cursor和Microsoft Copilot Studio）来简化日常工作。 这些应用程序支持&#x200B;**模型上下文协议(MCP)**，这是一个开放标准，允许应用程序以统一的方式向大型语言模型(LLM)公开后端工具。

[!DNL Adobe Journey Optimizer]现在提供了一个MCP服务器，该服务器直接在任何MCP兼容的应用程序中呈现营销活动、历程、忠诚度和沙盒操作。 通过[!DNL Adobe Journey Optimizer] MCP集成，不同的角色可以围绕相同的编排数据进行协作 — 无需针对[!DNL Adobe Journey Optimizer] REST API编写查询或导航多个UI屏幕。 客户可以通过对话方式描述其意图，并让LLM调用相应的MCP工具。

## 主要功能 {#mcp-capabilities}

[!DNL Adobe Journey Optimizer] MCP服务器允许您直接从AI助手检查、汇总旅程、营销活动和选件，并对其进行故障排除。 所有操作都是&#x200B;**只读** — MCP服务器表面将API作为纯语言答案进行检索，因此您可以：

<!--* **Understand journey logic** — Get a human-readable summary of any journey's branching, conditions, and actions.-->
* **即时查看营销活动** — 以纯语言询问营销活动状态、历程性能或渠道配置并即时获得答案，无需导航菜单或手动提取报告。
* **提早发现问题** — 即时发现停止的营销活动、孤立的草稿和渠道配置问题，以便您的团队可以快速采取行动。
* **围绕实时数据协作** — 营销人员、营销活动经理和利益相关者均可通过其AI助手查询相同的实时[!DNL Adobe Journey Optimizer]数据，从而更轻松地对齐、决定和移动数据。
* **审核您的编排组合** — 查看营销活动和历程的完整状态，而无需解析JSON或跨产品屏幕跳转。

## 可用工具 {#mcp-tools}

[!DNL Adobe Journey Optimizer] MCP服务器公开以下工具：

| 工具 | 描述 |
|---|---|
| **列出营销活动** | 浏览您的[!DNL Adobe Journey Optimizer]营销活动。 支持按状态（草稿、实时、已停止、已完成）过滤。 |
| **获取营销活动** | 按ID获取特定营销活动的完整详细信息和配置，包括受众定位、计划、渠道和内容设置。 |
| **列出历程** | 查看您的[!DNL Adobe Journey Optimizer]客户历程（自动化工作流），并可选地按状态筛选：草稿、实时、已关闭或已完成。 |
| **列出渠道配置** | 查看电子邮件、短信、推送或WhatsApp渠道的表面预设和品牌设置。 |

>[!NOTE]
>
>所有工具均为只读。 当前Beta版本不支持写入操作（创建、更新或删除对象）。

## 用例 {#mcp-use-cases}

以下示例显示如何使用自然语言与[!DNL Adobe Journey Optimizer] MCP服务器交互：

| 目标 | 示例提示 |
|---|---|
| **促销活动概述** | “显示我的所有AJO营销活动”/“在AJO中设置了多少营销活动？” |
| **状态审核** | “哪些营销活动当前处于实时状态？” /“列出任何暂停或停止的营销活动。” |
| **促销活动详细信息** | “获取营销活动[ID]的完整详细信息”/“向我介绍在营销活动[ID]中设置的所有内容。” |
| **受众和定位** | “促销活动[ID]的目标受众是谁？” /“对营销活动[ID]设置了哪些资格规则？” |
| **计划和时间** | “何时计划运行营销活动[ID]？” /“促销活动[ID]是一次性发送还是定期发送？” |
| **疑难解答** | “为什么营销活动[ID]不会发送？” /“查看营销活动[ID]的设置以了解任何问题。” |
| **历程清单** | “列出所有实时历程”/“向我显示处于草稿状态的历程。” |
| **渠道配置** | “我的沙盒中有哪些渠道预设可用？” /“显示我的所有电子邮件渠道配置。” |
| **渠道审核** | “哪些渠道配置缺失或不完整？” / “我跨所有渠道有多少个渠道配置？” |

## 先决条件 {#mcp-prerequisites}

在将[!DNL Adobe Journey Optimizer] MCP服务器连接到MCP客户端之前，请确保：

* 您有一个有效的[!DNL Adobe Journey Optimizer]许可证。
* 您可以访问支持的MCP兼容应用程序（当前为Claude Web或Claude Desktop）。
* 您在[!DNL Adobe Journey Optimizer]中拥有查看营销活动、历程和优惠的必要权限。

## 连接[!DNL Adobe Journey Optimizer] MCP服务器 {#mcp-connect}

>[!NOTE]
>
>此集成位于Beta中。 详细的设置步骤将在发布后正式发布。 请联系您的Adobe代表以请求提前访问并接收配置说明。

在Beta阶段，您的Adobe代表将提供：

* 特定于您组织的MCP服务器端点URL。
* 用于将AI助手连接到[!DNL Adobe Journey Optimizer]的身份验证凭据。
* 有关在Claude Desktop或Claude Web中配置MCP服务器的指导。

<!--
Step-by-step connection instructions to be added here, including:
- How to obtain MCP server credentials from [!DNL Adobe Journey Optimizer]
- How to configure the MCP server in Claude Desktop / Claude Web
- How to authenticate
-->

## 已知限制(Beta) {#mcp-limitations}

以下限制适用于[!DNL Adobe Journey Optimizer] MCP服务器的当前Beta版本：

| 限制 | 描述 | 解决方法 |
|---|---|---|
| **没有参与或绩效指标** | MCP服务器不公开任何报表数据。 工具不会返回展示次数、点进率、转化率或投放统计信息。 | 将AJO报表UI、CJA MCP或Adobe Analytics MCP用于指标。 AEP查询服务可以使用营销活动执行ID查询原始事件数据。 |
| **营销活动列表分页限制** | `List Campaigns`始终返回结果的第一页（最多50个营销活动，按字母顺序排序）。 偏移和限制值未应用，这使得完整枚举对于大型沙盒不可行。 | 如果已知促销活动ID或名称，则直接使用`Get Campaign`。 使用AJO UI浏览和筛选完整列表。 |
| **没有按日期、渠道或计划进行服务器端筛选** | `List Campaigns`仅支持按状态筛选。 在服务器端，无法按发布日期、计划日期、渠道或营销活动类型进行筛选。 | 使用AJO UI促销活动列表，该列表支持原生日期和渠道筛选。 |
| **无法检索邮件内容** | 消息内容工具会为所有渠道类型（电子邮件、基于代码等）返回HTTP 502。 无法通过MCP检索消息HTML、主题行、个性化令牌和选件内容。 | 直接在AJO UI中的&#x200B;**促销活动> [促销活动] >内容**&#x200B;下查看消息内容和个性化令牌。 |

## 常见问题 {#mcp-faq}

+++支持哪些MCP客户端？

[!DNL Adobe Journey Optimizer] MCP服务器当前可用于&#x200B;**Claude Web**&#x200B;和&#x200B;**Claude Desktop**。 未来版本中可能会添加对其他MCP兼容应用程序的支持。
+++

+++我可以通过MCP访问哪些[!DNL Adobe Journey Optimizer]对象？

您可以访问营销活动、历程、优惠、忠诚度数据和沙盒信息。 操作是只读的（检索API）；当前版本不支持写入操作。
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

