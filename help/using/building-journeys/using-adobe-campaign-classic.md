---
title: Adobe Campaign v7/v8 操作
description: 了解Adobe Campaign v7/v8操作
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 6%

---

# Adobe Campaign v7/v8 操作 {#using_campaign_classic}

An integration is available if you have Adobe Campaign v7 or v8. 它允许您使用Adobe Campaign事务型消息传送功能发送电子邮件、推送通知和短信。

Journey Optimizer实例和Campaign实例之间的连接是在预配时Adobe设置的。 联系Adobe。

要使此功能正常工作，您需要配置专用操作。 请参阅 [部分](../action/acc-action.md).

本节介绍了端到端用例 [部分](../building-journeys/campaign-classic-use-case.md).

1. Design your journey, starting with an event. See this [section](../building-journeys/journey.md).
1. In the **Action** section of the palette, select a Campaign action and add it to your journey.
1. 在 **操作参数**，则会显示消息有效负载中预期的所有字段。 您需要将每个字段与要使用的字段进行映射（来自事件或来自数据源）。 这类似于自定义操作。 请参阅 [部分](../building-journeys/using-custom-actions.md).

![](assets/accintegration2.png)
