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
source-git-commit: d4765f9084efac1fd241404dff365a66027ce5af
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 53%

---


# 使用 API 触发的营销活动 {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="API 触发的营销活动"
>abstract="**交易型 API 触发的营销活动**<br/>&#x200B;通过调用 API 触发实时消息&#x200B;<br/><br/>**营销消息**<br/>&#x200B;促销内容（需要选择加入，取决于业务规则）<br/><br/>**交易型消息**<br/>&#x200B;服务相关的内容（确认、提醒，无需获得营销同意）<br/><br/>**可用渠道**<br/>&#x200B;电子邮件、SMS、推送通知"

## 关于API触发的营销活动 {#about}

通过“API 触发的营销活动”，您可以在正确的时间将营销通信传达给受众，或者允许将事务性/运营消息发送给个人（如密码重置），其中需求可能涉及个性化，不仅会使用轮廓属性，还会用到触发器中的实时上下文数据（即 REST API 有效负载）。

为此，您首先需要在Journey Optimizer中创建API触发的营销活动，然后使用[交互式消息执行REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)通过API调用启动其执行。

API触发的营销活动的可用渠道包括电子邮件、短信和推送消息。

➡️ [通过观看视频了解此功能](#video)


>[!NOTE]
>
>支持的渠道包括：[电子邮件](../email/get-started-email.md)、[短信/彩信/RCS](../sms/get-started-sms.md)、[推送通知](../push/get-started-push.md)。
>
>可用渠道因您的许可模式和插件而异。

## API触发的营销活动创建的关键步骤 {#steps}

1. [定义营销活动属性](api-triggered-campaign-properties.md)
1. [配置营销活动操作](api-triggered-campaign-action.md)
1. [编辑营销活动内容](api-triggered-campaign-content.md)
1. [定义营销活动受众](api-triggered-campaign-audience.md)
1. [计划营销活动](api-triggered-campaign-schedule.md)
1. [查看和激活营销活动](review-activate-api-triggered-campaign.md)
1. [触发营销活动执行](trigger-campaigns.md)

>[!IMPORTANT]
>
>在创建营销活动之前，请确保已查看常规的[营销活动先决条件](../campaigns/get-started-with-campaigns.md#prerequisites)。

## 操作说明视频 {#video}

了解如何使用交互式消息执行REST API，根据用户交互从外部系统创建并触发活动。

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)
