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
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
source-git-commit: d93b7ce225294257f49caee6ac08cfb575611a93
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 3%

---


# 执行API触发的营销活动 {#execute}

激活营销活动后，您需要检索生成的示例cURL请求，并将其用于API中以构建有效负载并触发营销活动。

## 必读 {#must-read}

* **促销活动开始/结束日期** — 如果您在创建促销活动时配置了特定的开始和/或结束日期，则不会在这些日期之外执行，并且API调用将失败。

* **调用超时** — 对交互式消息执行REST API的调用超时60秒。 但是，如果意外超时，则进行内部重试以确保投放。

## 触发活动 {#trigger}

1. 打开营销活动，然后从&#x200B;**[!UICONTROL cURL请求]**&#x200B;部分复制并粘贴有效负载请求。 此有效负载包含消息中使用的所有个性化（用户档案和上下文）变量。 活动开始后，即可使用该功能。

   ![](assets/api-triggered-curl.png)

   >[!IMPORTANT]
   >
   >cURL部分中的端点在标准和[高吞吐量营销活动](../campaigns/api-triggered-high-throughput.md)之间有所不同。

1. 将此cURL请求用到API中以构建有效负载并触发营销活动。 有关详细信息，请参阅[交互式消息执行API文档](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)，其中列出了标准和高吞吐量营销活动的所有端点。

   [此页面](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/)上也提供了API调用示例。
