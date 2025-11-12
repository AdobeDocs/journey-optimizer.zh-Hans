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
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 1%

---

# 创建实时活动 {#create-mobile-live}

>[!BEGINSHADEBOX]

* [实时活动入门](get-started-mobile-live.md)
* [实时活动配置](mobile-live-configuration.md)
* [实时活动与Adobe Experience Platform Mobile SDK集成](mobile-live-configuration-sdk.md)
* **[创建实时活动](create-mobile-live.md)**
* [常见问题解答](mobile-live-faq.md)
* [实时活动营销活动报告](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

配置移动配置并实施Adobe Experience Platform移动SDK后，您可以在Journey Optimizer中开始创建实时活动：

1. 访问&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建营销活动]**。

1. 选择&#x200B;**API触发**&#x200B;营销活动类型。

   * 为基于受众的营销活动选择&#x200B;**API触发的营销**

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

1. 营销活动旨在按特定日期或循环频率执行。 在&#x200B;**[!UICONTROL 本节]**&#x200B;中了解如何配置促销活动的[计划](../campaigns/create-campaign.md#schedule)。

1. 配置完毕后，单击&#x200B;**[!UICONTROL 查看以激活]**，然后单击&#x200B;**[!UICONTROL 激活]**。

1. 激活营销活动后，使用提供的&#x200B;**cURL请求**&#x200B;作为模板来触发实时活动开始、更新或结束事件。 在执行之前，使用特定数据更新示例有效负载。

   请确保您还复制要包含在有效负载中的&#x200B;**[!UICONTROL 促销活动ID]**&#x200B;标识符。

   ➡️请参阅[API触发的营销活动文档](https://developer.adobe.com/journey-optimizer-apis/references/messaging/)以了解身份验证要求，包括OAuth令牌和API密钥。

   ![](assets/create-live-3.png)

   +++ 单个有效负载的示例

   请注意，以下有效负载示例中的大多数字段是必填字段，只有`requestId`、`dismissal-date`和`alert`是可选的。

       “&#39;json
”       &lbrace;
       &quot;requestId&quot;： &quot;your-request-id&quot;，
       &quot;campaignId&quot;： &quot;your-campaign-id&quot;，
       “收件人”： &lbrack;
       &lbrace;
       &quot;type&quot;： &quot;aep&quot;，
       &quot;userId&quot;： &quot;testemail@gmail.com&quot;，
       &quot;namespace&quot;： &quot;email&quot;，
       “上下文”： &lbrace;
       &quot;requestPayload&quot;： &lbrace;
       “aps”：&lbrace;
       “content-available”： 1，
       &quot;timestamp&quot;： 1756984054，              //当前纪元时间
       “驳回日期”： 1756984084，         //可选 — 当event=&quot;end&quot;
时自动删除       &quot;event&quot;： &quot;update&quot;，                    //开始 | 更新 | 结束
       
   FoodDeliveryLiveActivityAttributes中的    //字段
       &quot;content-state&quot;： &lbrace;
       &quot;orderStatus&quot;： &quot;Delivered&quot;
       &rbrace;，
       
       &quot;attributes-type&quot;： &quot;FoodDeliveryLiveActivityAttributes&quot;，
       “属性”： &lbrace;
       “restaurantName”：“Pizza”，
       “liveActivityData”： &lbrace;
       &quot;liveActivityID&quot;： &quot;orderId1&quot;       //客户参考ID
       &rbrace;
       &rbrace;，
       
       “警报”： &lbrace;
       &quot;title&quot;： &quot;Order Delivered！&quot;，
       “正文”：“您的披萨已送达。”
       &rbrace;
       &rbrace;
       &rbrace;
       &rbrace;
       &rbrace;
       &rbrack;
       &rbrace;
       “
+++”   

设计实时活动后，您可以使用[内置报告](../reports/campaign-global-report-cja-activity.md)跟踪衡量实时活动的影响。
