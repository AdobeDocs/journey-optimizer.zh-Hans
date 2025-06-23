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
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 31%

---

# Adobe Campaign v7/v8 操作 {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="自定义操作"
>abstract="如果您使用 Adobe Campaign v7 或 v8，则可以利用集成。通过它，可使用 Adobe Campaign 事务性消息传递功能发送电子邮件、推送通知和短信。"

如果您使用 Adobe Campaign v7 或 v8，则可以利用集成。利用此功能，可使用Adobe Campaign事务性消息传送功能发送电子邮件、推送通知和短信。

Journey Optimizer实例和Campaign实例之间的连接是在预配时由Adobe设置的。 联系Adobe。

要使此功能正常工作，您需要配置专用操作。 请参阅此[章节](../action/acc-action.md)。

此[部分](../building-journeys/ajo-ac.md)中介绍了端到端用例。

1. 设计您的历程，从事件开始。 请参阅此[部分](../building-journeys/journey.md)。
1. 在调色板的&#x200B;**操作**&#x200B;部分中，选择一个Campaign操作并将其添加到您的历程。
1. 在&#x200B;**操作参数**&#x200B;中，将显示消息有效负载中预期的所有字段。 您需要将每个字段映射到要使用的字段（从事件或从数据源）。 这与自定义操作类似。 请参阅此[章节](../building-journeys/using-custom-actions.md)。

![](assets/accintegration2.png)
