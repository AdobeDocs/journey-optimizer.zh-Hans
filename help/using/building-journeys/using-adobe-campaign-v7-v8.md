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
TQID: https://experienceleague.adobe.com/Saqu6Kkm1Rdym10IuwLF88Fj-hT2crAwENajyKBeY5w
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 26%

---

# [!DNL Adobe Campaign] v7/v8 操作 {#using_campaign_v7-v8}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何使用Adobe Campaign v7和v8集成，通过Campaign事务性消息传递从您的历程发送电子邮件、推送通知和短信。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="自定义操作"
>abstract="如果使用的是 [!DNL Adobe Campaign] v7 或 v8，则可以使用集成功能。 该集成允许您使用 [!DNL Adobe Campaign] 的事务性消息功能发送电子邮件、推送通知和短信。"

如果使用的是 [!DNL Adobe Campaign] v7 或 v8，则可以使用集成功能。 该集成允许您使用 [!DNL Adobe Campaign] 的事务性消息功能发送电子邮件、推送通知和短信。

Journey Optimizer 实例和 Campaign 实例之间的连接在配置时由 Adobe 设置。 联系Adobe。

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
