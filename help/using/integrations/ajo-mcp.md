---
solution: Journey Optimizer
product: journey optimizer
title: 使用MCP客户端
description: 了解如何使用MCP服务器将Adobe Journey Optimizer连接到MCP客户端
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta 版" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: 0a2c384faea70dcbc9b99596740e375d85b2bc64
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 1%

---

# 使用MCP客户端 {#ajo-mcp}

>[!AVAILABILITY]
>
>[!DNL Adobe Journey Optimizer] MCP服务器当前仅在&#x200B;**Claude Web**&#x200B;和&#x200B;**Claude Desktop**&#x200B;中可用。 未来版本中将增加对其他MCP兼容应用程序的支持。

通过[!DNL Adobe Journey Optimizer] MCP集成，您可以使用纯语言提示查询促销活动、历程和优惠，而无需编写API调用或导航产品屏幕。 此页面介绍集成的工作方式、您可以对其执行的操作以及如何入门。

## 什么是模型上下文协议？ {#mcp-overview}

营销和客户体验团队越来越依赖基于聊天的应用程序和开发人员工具（如Anthropic Claude、OpenAI ChatGPT、Cursor和Microsoft Copilot Studio）来简化日常工作。 这些应用程序支持&#x200B;**模型上下文协议(MCP)**，这是一个开放标准，允许应用程序以统一的方式向大型语言模型(LLM)公开后端工具。

[!DNL Adobe Journey Optimizer]现在提供了一个MCP服务器，该服务器直接在任何MCP兼容的应用程序中呈现营销活动、历程、忠诚度和沙盒操作。 通过[!DNL Adobe Journey Optimizer] MCP集成，不同的角色可以围绕相同的编排数据进行协作 — 无需针对[!DNL Adobe Journey Optimizer] REST API编写查询或导航多个UI屏幕。 客户可以通过对话方式描述其意图，并让LLM调用相应的MCP工具。

## 主要功能 {#mcp-capabilities}

[!DNL Adobe Journey Optimizer] MCP服务器允许您直接从AI助手检查、汇总旅程、营销活动和选件，并对其进行故障排除。 所有操作都是&#x200B;**只读** — MCP服务器表面将API作为纯语言答案进行检索，因此您可以：

* **了解历程逻辑** — 获取任何历程的分支、条件和操作的可读摘要。
* **检查营销活动准备情况** — 识别阻止发布营销活动的拦截器。
* **定位覆盖率差距** — 查看您的实时历程和营销活动覆盖了哪些渠道，以及存在差距的位置。
* **审核您的编排组合** — 查看营销活动和历程的完整状态，而无需解析JSON或跨产品屏幕跳转。

## 用例 {#mcp-use-cases}

以下示例显示如何使用自然语言与[!DNL Adobe Journey Optimizer] MCP服务器交互：

| 目标 | 示例提示 |
|---|---|
| **汇总促销活动详细信息** | “获取campaign cmp456并汇总受众、计划、状态和包。” |
| **清单和状态审核** | “我们拥有什么，处于什么状态？ 显示营销活动的实时计数、草稿计数以及已完成/已停止/已存档的计数。” |
| **检查发布准备情况** | “为什么营销活动cmp456还没有准备好发布？ 给我看看阻滞剂。” |
| **比较对象** | “比较促销活动abc123和xyz789 — 状态和计划有什么变化？” |
| **审核您的项目组合** | “在所有实时历程和营销活动中，涵盖哪些渠道以及存在哪些差距？” |
| **渠道覆盖范围和组合** | “显示历程、营销活动和优惠投放位置的渠道占用情况 — 仅限电子邮件与多渠道、推送/短信/应用程序内使用情况，以及历程渠道之间的不匹配情况。” |

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
