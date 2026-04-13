---
solution: Journey Optimizer
product: journey optimizer
title: 通过MCP与AI助理合作
description: 了解如何使用MCP服务器将Adobe Journey Optimizer连接到AI助理
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="限量发布版" type="Informative"
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 5eca5b3794731f030427fa426cb09e705d491b6f
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 1%

---

# 通过MCP与AI助理合作 {#ajo-mcp}

>[!AVAILABILITY]
>
>[!DNL Adobe Journey Optimizer] MCP服务器当前仅在&#x200B;**Claude Web**&#x200B;和&#x200B;**Claude Desktop**&#x200B;中可用。

## 什么是模型上下文协议？ {#mcp-overview}

营销和客户体验团队越来越依赖基于聊天的应用程序和开发人员工具（如Anthropic Claude、OpenAI ChatGPT、Cursor和Microsoft Copilot Studio）来简化日常工作。 这些应用程序支持&#x200B;**模型上下文协议(MCP)**，这是一个开放标准，允许应用程序以统一的方式向大型语言模型(LLM)公开后端工具。

[!DNL Adobe Journey Optimizer]现在提供了一个MCP服务器，该服务器直接在任何MCP兼容的应用程序中呈现营销活动、历程、忠诚度和沙盒操作。 通过[!DNL Adobe Journey Optimizer] MCP集成，不同的角色可以围绕相同的编排数据进行协作 — 无需针对[!DNL Adobe Journey Optimizer] REST API编写查询或导航多个UI屏幕。 客户可以通过对话方式描述其意图，并让LLM调用相应的MCP工具。

## 主要功能 {#mcp-capabilities}

[!DNL Adobe Journey Optimizer] MCP服务器允许您直接从AI助手检查、总结[!DNL Adobe Journey Optimizer]历程、营销活动和优惠，并对其进行故障排除。 [!DNL Adobe Journey Optimizer]的检索API被转换为纯语言答案，因此您可以：

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

在将[!DNL Adobe Journey Optimizer] MCP服务器连接到AI助手之前，请确保：

* 您有一个有效的[!DNL Adobe Journey Optimizer]许可证。
* 您可以访问支持的MCP兼容应用程序（当前为Claude Web或Claude Desktop）。
* 您在[!DNL Adobe Journey Optimizer]中拥有查看营销活动、历程和优惠的必要权限。

## 连接[!DNL Adobe Journey Optimizer] MCP服务器 {#mcp-connect}

>[!NOTE]
>
>集成正式可用后，将添加详细的设置步骤。 请联系您的Adobe代表以提前获取访问权限。

<!--
Step-by-step connection instructions to be added here, including:
- How to obtain MCP server credentials from [!DNL Adobe Journey Optimizer]
- How to configure the MCP server in Claude Desktop / Claude Web
- How to authenticate
-->

## 常见问题 {#mcp-faq}

+++支持哪些AI助理？

[!DNL Adobe Journey Optimizer] MCP服务器当前可用于&#x200B;**Claude Web**&#x200B;和&#x200B;**Claude Desktop**。 未来版本中可能会添加对其他MCP兼容应用程序的支持。
+++

+++我可以通过MCP访问哪些[!DNL Adobe Journey Optimizer]对象？

您可以访问营销活动、历程、优惠、忠诚度数据和沙盒信息。 操作是只读的（检索API）；当前版本不支持写入操作。
+++

+++是否需要开发人员访问权限才能使用[!DNL Adobe Journey Optimizer] MCP服务器？

否。 MCP服务器专为营销和技术人员而设计。 营销人员可以在Claude中使用自然语言提示与其交互，而开发人员也可以在支持MCP的开发人员工具中使用它。
+++

+++我的数据是否发送到AI助手提供商？

当您提交提示时，AI助手可能会将相关上下文（包括MCP服务器返回的[!DNL Adobe Journey Optimizer]数据）发送到其模型以供处理。 在连接到生产数据之前，请查看AI助手提供商的隐私和数据处理策略。
+++

