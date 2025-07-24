---
solution: Journey Optimizer
product: journey optimizer
title: 使用API触发的营销活动
description: 了解如何使用Journey Optimizer API触发营销活动。
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 营销活动， API触发， REST，优化器，消息
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 15f5fdfde0e9f7c93739a624918838dbd6787833
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 4%

---


# 使用API触发的营销活动 {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="API触发的营销活动"
>abstract="**事务性API触发的营销活动**<br/>&#x200B;通过API调用触发实时消息&#x200B;<br/><br/>**营销消息**<br/>&#x200B;促销内容（需要选择加入，但须遵守业务规则）<br/><br/>**事务性消息**<br/>&#x200B;与服务相关的内容（确认、提醒、不须遵守营销同意）<br/><br/>**可用渠道**<br/>&#x200B;电子邮件、短信、推送通知"

## 关于API触发的营销活动 {#about}

API触发的营销活动允许营销通信在适当的时间联系受众，或允许向个人发送交易/运营消息，如密码重置，其中需求可能涉及个性化，不仅使用用户档案属性，还涉及触发器中的实时上下文数据，即REST API有效负载。

为此，您首先需要在Journey Optimizer中创建API触发的营销活动，然后使用[交互式消息执行REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)通过API调用启动其执行。

API触发的营销活动的可用渠道包括电子邮件、短信和推送消息。

➡️ [通过观看视频了解此功能](#video)

## API触发的营销活动创建的关键步骤 {#steps}

1. [定义营销活动属性](api-triggered-campaign-properties.md)
1. [配置活动操作](api-triggered-campaign-action.md)
1. [编辑营销活动内容](api-triggered-campaign-content.md)
1. [定义活动受众](api-triggered-campaign-audience.md)
1. [计划营销活动](api-triggered-campaign-schedule.md)
1. [查看并激活营销活动](review-activate-api-triggered-campaign.md)
1. [触发活动执行](trigger-campaigns.md)

## 操作说明视频 {#video}

了解如何使用交互式消息执行REST API，根据用户交互从外部系统创建并触发活动。

>[!VIDEO](https://video.tv.adobe.com/v/3452735?quality=12&captions=chi_hans)
