---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Campaign v7/v8 操作
description: 了解Adobe Campaign v7/v8操作
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: 历程，集成， campaign， v7， v8
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
version: Journey Orchestration
source-git-commit: 339285cbc82d5b30b221feb235ed8425a66f8802
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 6%

---

# [!DNL Adobe Campaign] v7/v8操作 {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="自定义操作"
>abstract="如果您有[!DNL Adobe Campaign] v7或v8，则集成可用。 它允许您使用[!DNL Adobe Campaign]事务性消息传递功能发送电子邮件、推送通知和短信。"

如果您有[!DNL Adobe Campaign] v7或v8，则集成可用。 它允许您使用[!DNL Adobe Campaign]事务性消息传递功能发送电子邮件、推送通知和短信。

Journey Optimizer实例和Campaign实例之间的连接是在预配时由Adobe设置的。 联系Adobe。

**何时使用**：当您的消息传送依赖活动事务模板、特定于活动的数据模型或现有活动投放工作流时，请使用Campaign v7/v8操作。

**先决条件**

* 您的[!DNL Adobe Campaign] v7/v8实例已通过Adobe配置并连接到Journey Optimizer。
* 您有权访问Campaign事务型消息传递，并拥有所需的权限。

要使此功能正常工作，您需要配置专用操作。 请参阅此[章节](../action/acc-action.md)。

此[部分](../building-journeys/ajo-ac.md)中介绍了端到端用例。

1. 设计您的历程，从事件开始。 请参阅此[部分](../building-journeys/journey.md)。
1. 在调色板的&#x200B;**操作**&#x200B;部分中，选择一个Campaign操作并将其添加到您的历程。
1. 在&#x200B;**操作参数**&#x200B;中，将显示消息有效负载中预期的所有字段。 您需要将每个字段映射到要使用的字段（从事件或从数据源）。 这与自定义操作类似。 请参阅此[章节](../building-journeys/using-custom-actions.md)。

>[!NOTE]
>
>* Campaign v7/v8操作可与同一历程中的本机渠道操作一起使用。 这不适用于Campaign Standard操作。 查看[促销活动护栏](../start/guardrails.md#ac-g)。
>* Campaign v7/v8操作不能用于“读取受众”或“受众资格”活动。 请参阅护栏页面中的读取受众和受众资格护栏。

![[!DNL Adobe Campaign] v7/v8操作配置和集成设置](assets/accintegration2.png)
