---
solution: Journey Optimizer
product: journey optimizer
title: 创建实时活动消息
description: 了解如何在Journey Optimizer中创建实时活动
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 9864a136-e129-4279-bb09-081b72f584df
source-git-commit: 6b4e3a6c32d24861f1ea8df54fc2e4fbb19d0ce7
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 3%

---

# 创建实时活动 {#create-mobile-live}

配置移动配置并实施Adobe Experience Platform移动SDK后，您可以在Journey Optimizer中开始创建实时活动：

1. 访问&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建营销活动]**。

1. 选择&#x200B;**API触发**&#x200B;营销活动类型。

   * 对于基于受众的营销活动，请选择 **API 触发的营销**

   * 为各个营销活动选择&#x200B;**API触发的事务型**。

   >[!IMPORTANT]
   >
   > 请注意，对于&#x200B;**API触发的事务性**，不应启用&#x200B;**[!UICONTROL 高吞吐量]**&#x200B;选项。

   ![](assets/create-live-1.png)

1. 从&#x200B;**[!UICONTROL 属性]**&#x200B;部分，编辑营销活动的&#x200B;**[!UICONTROL 标题]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

1. 在&#x200B;**[!UICONTROL 操作]**&#x200B;部分中，选择&#x200B;**[!UICONTROL 实时活动]**，然后选择或创建新配置。

   在[此页面](mobile-live-configuration.md)上了解有关实时活动配置的更多信息。

   ![](assets/create-live-2.png)

1. 单击&#x200B;**[!UICONTROL 创建试验]**&#x200B;开始配置内容试验并创建处理以测量其性能并为目标受众确定最佳选项。 [了解详情](../content-management/content-experiment.md)

1. 从&#x200B;**[!UICONTROL 受众]**&#x200B;选项卡中，选择您的&#x200B;**[!UICONTROL 标识类型]**&#x200B;[了解更多](../audience/about-audiences.md)。

   >[!NOTE]
   >
   >对于&#x200B;**API触发的营销**&#x200B;营销活动，您可以在从API有效负载检查APNs channelID订阅之前，选择充当第一个分段的现有受众。

1. 营销活动旨在按特定日期或循环频率执行。 在&#x200B;**[!UICONTROL 本节]**&#x200B;中了解如何配置促销活动的[计划](../campaigns/create-campaign.md#schedule)。

1. 配置完毕后，单击&#x200B;**[!UICONTROL 查看以激活]**，然后单击&#x200B;**[!UICONTROL 激活]**。

1. 激活营销活动后，使用提供的&#x200B;**cURL请求**&#x200B;作为模板来触发实时活动开始、更新或结束事件。 在执行之前，使用特定数据更新示例有效负载。

   请确保您还复制要包含在有效负载中的&#x200B;**[!UICONTROL 促销活动ID]**&#x200B;标识符。

   ➡️请参阅[API触发的营销活动文档](https://developer.adobe.com/journey-optimizer-apis/references/messaging/)以了解身份验证要求，包括OAuth令牌和API密钥。

   ![](assets/create-live-3.png)

   +++ 单一用例的有效负载示例（API触发的事务型营销活动）

   此有效负载示例适用于使用&#x200B;**API触发的事务性**&#x200B;营销活动类型的单个营销活动。 请注意，以下有效负载示例中的大多数字段是必填字段，只有`requestId`、`dismissal-date`和`alert`是可选的。

   ```json
   {
       "requestId": "your-request-id",
       "campaignId": "your-campaign-id",
       "recipients": [
   {
       "type": "aep",
       "userId": "testemail@gmail.com",
       "namespace": "email",
       "context": {
        "requestPayload": {
       "aps": {
       "content-available": 1,
       "timestamp": 1756984054,              // current epoch time
       "dismissal-date": 1756984084,         // optional – auto remove when event="end"
       "event": "update",                    // start | update | end
   
       // Fields from FoodDeliveryLiveActivityAttributes
       "content-state": {
         "orderStatus": "Delivered"
       },
   
       "attributes-type": "FoodDeliveryLiveActivityAttributes",
       "attributes": {
         "restaurantName": "Pizza",
         "liveActivityData": {
           "liveActivityID": "orderId1"       // customer reference ID
         }
       },
   
       "alert": {
         "title": "Order Delivered!",
         "body": "Your pizza has arrived."
       }
     }
   }
   }
   }
   ]
   }
   ```

   +++

   +++ 广播用例的有效负载示例（API触发的营销活动）

   此有效负载示例适用于使用&#x200B;**API触发的营销**&#x200B;营销类型的基于受众的营销活动。

   ```json
   {
       "requestId": "123400000",
       "campaignId": "d32e6f6c-56df-4a98-a2c0-6db6008f8f32",
       "audience": {
           "id": "508f9416-52d0-4898-ba47-08baaa22e9c7"
       },
       "context": {
           "requestPayload": {
               "aps": {
                   "input-push-channel": "V+8UslywEfAAAOq9SbTrLg==",  //apns-channel-id
                   "content-available": 1,
                   "timestamp": 1770808339,
                   "event": "update",   // start | update | end
   
                   // Fields from GameScoreLiveActivityAttributes
                   "content-state": {
                       "homeTeamScore": 33,
                       "awayTeamScore": 49,
                       "statusText": "Wingdom keeps scoring!"
                   },
                   "attributes-type": "GameScoreLiveActivityAttributes",
                   "attributes": {
                       "liveActivityData": {
                           "channelID": "V+8UslywEfAAAOq9SbTrLg=="   //apns-channel-id, must match the "input-push-channel" value
                       }
                   },
                   "alert": {
                       "title": "This is the title for game",
                       "body": "This is the body for body"
                   }
               }
           }
       }
   }
   ```

   +++

设计实时活动后，您可以使用[内置报告](../reports/campaign-global-report-cja-activity.md)跟踪衡量实时活动的影响。

## 操作方法视频

了解如何使用Adobe Journey Optimizer配置iOS Live Activities，以便在iPhone锁屏界面和Dynamic Island上提供丰富的实时更新。

>[!VIDEO](https://video.tv.adobe.com/v/3479864)
