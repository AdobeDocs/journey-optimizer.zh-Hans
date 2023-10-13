---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Campaign v7/v8 操作
description: 了解Adobe Campaign v7/v8操作
feature: Actions
topic: Administration
role: Admin
level: Intermediate
keywords: 历程，集成， campaign， v7， v8， classic
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
source-git-commit: 055b735308cc6f0f942c165541d87dfdb74f557c
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 39%

---

# Adobe Campaign v7/v8 操作 {#using_campaign_classic}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="自定义操作"
>abstract="如果您使用 Adobe Campaign v7 或 v8，则可以利用集成。它让您可以使用 Adobe Campaign 事务性消息传递功能发送电子邮件、推送通知和短信。"

如果您使用 Adobe Campaign v7 或 v8，则可以利用集成。利用此功能，可使用Adobe Campaign事务性消息传送功能发送电子邮件、推送通知和短信。

Journey Optimizer 实例和 Campaign 实例之间的连接在配置时由 Adobe 设置。联系Adobe。

要使此功能正常工作，您需要配置专用操作。 请参阅此[章节](../action/acc-action.md)。

本中介绍了端到端用例 [部分](../building-journeys/ajo-ac.md).

1. 设计您的历程，从事件开始。 请参阅此[部分](../building-journeys/journey.md)。
1. 在 **操作** 部分，选择一个Campaign操作并将其添加到您的历程。
1. 在 **操作参数**，则将显示消息有效负载中预期的所有字段。 您需要将每个字段映射到要使用的字段（从事件或从数据源）。 这与自定义操作类似。 请参阅此[章节](../building-journeys/using-custom-actions.md)。

![](assets/accintegration2.png)
