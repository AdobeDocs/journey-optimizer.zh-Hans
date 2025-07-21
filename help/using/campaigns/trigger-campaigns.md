---
solution: Journey Optimizer
product: journey optimizer
title: 查看和激活营销活动
description: 了解如何在Journey Optimizer中查看和激活营销活动
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: 营销活动，审阅，验证，激活，激活，优化器
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 执行API触发的营销活动 {#execute}

激活营销活动后，您需要检索生成的示例cURL请求，并将其用于API中以构建有效负载并触发营销活动。

1. 打开营销活动，然后从&#x200B;**[!UICONTROL cURL请求]**&#x200B;部分复制并粘贴有效负载请求。 此有效负载包含消息中使用的所有个性化（用户档案和上下文）变量。 活动开始后，即可使用该功能。

   ![](assets/api-triggered-curl.png)

1. 将此cURL请求用到API中以构建有效负载并触发营销活动。 有关详细信息，请参阅[交互式消息执行API文档](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)。


   [此页面](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/)上也提供了API调用示例。

   >[!NOTE]
   >
   >如果您在创建营销活动时配置了特定的开始和/或结束日期，则它不会在这些日期之外执行，并且API调用将失败。
