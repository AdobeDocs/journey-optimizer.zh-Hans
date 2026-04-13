---
solution: Journey Optimizer
product: journey optimizer
title: 使用 API 触发的营销活动
description: 了解如何使用Journey Optimizer API触发营销活动。
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 营销活动， API触发， REST，优化器，消息
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: d1fd0b60ae60c2642108a1eb308564c9d04f5f9e
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 40%

---


# 使用 API 触发的营销活动 {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="API 触发的营销活动"
>abstract="**交易型 API 触发的营销活动**<br/>&#x200B;通过调用 API 触发实时消息&#x200B;<br/><br/>**营销消息**<br/>&#x200B;促销内容（需要选择加入，取决于业务规则）<br/><br/>**交易型消息**<br/>&#x200B;服务相关的内容（确认、提醒，无需获得营销同意）<br/><br/>**可用渠道**<br/>&#x200B;电子邮件、SMS、推送通知"

## 关于API触发的营销活动 {#about}

API触发的营销活动允许营销通信在适当的时间联系受众，或允许向个人发送交易/运营消息，如密码重置，其中需求可能涉及在触发器中不仅使用用户档案属性而且使用实时上下文数据（即REST API有效负载）的个性化。

为此，您首先需要在Journey Optimizer中创建API触发的营销活动，然后使用[交互式消息执行REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)通过API调用启动其执行。

➡️ [通过观看视频了解此功能](#video)

>[!NOTE]
>
>有关支持的渠道的更多信息，请参阅本节中的表：[历程和营销活动中的渠道](../channels/gs-channels.md#channels)。
>
>可用渠道因您的许可模式和附加组件而异。

## API触发的营销活动创建的关键步骤 {#steps}

在开始营销活动之前，请检查此部分[中列出的以下先决条件](get-started-with-campaigns.md#prerequisites)。 在满足以下先决条件后，您就可以开始创建营销活动：

1. [定义营销活动属性](api-triggered-campaign-properties.md)
1. [配置营销活动操作](api-triggered-campaign-action.md)
1. [编辑营销活动内容](api-triggered-campaign-content.md)
1. [定义营销活动受众](api-triggered-campaign-audience.md)
1. [计划营销活动](api-triggered-campaign-schedule.md)
1. [查看和激活营销活动](review-activate-api-triggered-campaign.md)
1. [触发营销活动执行](trigger-campaigns.md)

详细了解[完整营销活动创建工作流以及特定于类型的指南→](get-started-with-campaigns.md#workflow)

## 操作说明视频 {#video}

了解如何使用交互式消息执行REST API，根据用户交互从外部系统创建并触发活动。

>[!VIDEO](https://video.tv.adobe.com/v/3452735?captions=chi_hans&quality=12)
