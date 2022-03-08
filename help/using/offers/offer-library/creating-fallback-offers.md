---
title: 创建后备优惠
description: 了解如何创建后备优惠以向不符合任何优惠条件的客户显示
topic: Integrations
role: User
level: Intermediate
exl-id: 9ba16ad9-a5e7-4ce7-8ed6-7707d37178c6
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 3%

---

# 创建后备优惠 {#create-fallback-offers}

如果客户不符合其他选件的资格，则会向客户发送备用选件。 创建备用选件的步骤包括创建一个或多个表示形式，例如创建选件时。

➡️ [在视频中发现此功能](#video)

后备优惠的列表可在 **[!UICONTROL Offers]** 菜单。

![](../../assets/offers_list.png)

要创建备用选件，请执行以下步骤：

>[!NOTE]
>
>请注意，与个性化选件不同，备用选件没有资格规则和约束参数，因为它们是作为最后一个度假村呈现给客户的，没有任何条件。

1. 单击 **[!UICONTROL Create offer]**，然后选择 **[!UICONTROL Fallback offer]**.

   ![](../../assets/create_fallback.png)

1. 指定备用选件的名称。 您还可以将一个或多个现有标记与其关联，从而更轻松地搜索和组织选件库。

   ![](../../assets/fallback_details.png)

1. 为备用选件创建一个或多个表示形式。 要实现此目的，请从左窗格拖放版面，例如在创建个性化选件时。 请参阅 [创建个性化优惠](../offer-library/creating-personalized-offers.md).

   ![](../../assets/fallback_content.png)

1. 添加备用选件的表示形式后，会显示一个摘要。 如果一切配置正确，并且您的备用选件已准备好呈现给客户，请单击 **[!UICONTROL Finish]**，然后选择 **[!UICONTROL Save and approve]**.

   您还可以将备用选件另存为草稿，以便稍后进行编辑和批准。

   ![](../../assets/fallback_review.png)

1. 后备选件会显示在列表中，其中 **[!UICONTROL Live]** 或 **[!UICONTROL Draft]** 状态，具体取决于您在上一步中是否批准了它。

   现在，它已准备好交付给客户。 您可以选择它以显示其属性并进行编辑。 <!-- no suppression? -->

   ![](../../assets/fallback_created.png)

## 教程视频 {#video}

>[!NOTE]
>
>此视频适用于基于Adobe Experience Platform构建的Offer decisioning应用程序服务。 但是，它为在Journey Optimizer上下文中使用选件提供了通用指南。

>[!VIDEO](https://video.tv.adobe.com/v/329383?quality=12)
