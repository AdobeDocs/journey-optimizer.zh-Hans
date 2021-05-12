---
title: 创建决策
description: 了解如何制定决策
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 3%

---

# 创建决策{#create-offer-activities}

决策(以前称为优惠活动)是优惠的容器，将利用优惠决策引擎，以根据投放的目标来选择要交付的最佳优惠。

![](../../assets/do-not-localize/how-to-video.png) [在视频中发现此功能](#video)

可在&#x200B;**[!UICONTROL Offers]**&#x200B;菜单/ **[!UICONTROL Decisions]**&#x200B;选项卡中访问决策列表。 过滤器可帮助您根据决策的状态或开始和结束日期来检索决策。

![](../../assets/activities-list.png)

在创建决策之前，请确保在优惠库中创建了以下组件：

* [版面](../offer-library/creating-placements.md),
* [收藏集](../offer-library/creating-collections.md),
* [个性化优惠](../offer-library/creating-personalized-offers.md),
* [后备优惠](../offer-library/creating-fallback-offers.md).

## 创建决定{#create-activity}

1. 访问决策列表，然后单击&#x200B;**[!UICONTROL Create activity]**。

1. 指定决策的名称及其开始和结束日期和时间，然后单击&#x200B;**[!UICONTROL Next]**。

   ![](../../assets/activities-name.png)

## 添加决定{#add-decisions}

1. 从列表中拖放放置以将其添加到决策中，然后单击&#x200B;**[!UICONTROL Add collection]**。

   ![](../../assets/activities-placement.png)

1. 选择包含要考虑的优惠的集合，然后单击&#x200B;**[!UICONTROL Add]**。

   ![](../../assets/activities-collection.png)

1. 选定的优惠将添加到版面。 在此示例中，我们选择了两个优惠，它们将显示在JSON类型的位置中，旨在将优惠呈现到呼叫中心解决方案中。

   ![](../../assets/offers-added.png)

1. 默认情况下，如果多个优惠有资格参加此次安排，则优先级分数最高的优惠将交付给客户。

   如果要使用特定公式来选择要传送的合格优惠，请从&#x200B;**[!UICONTROL Rank offers by]**&#x200B;下拉列表中选择排名公式。 如需详细信息，请参阅[此部分](../offer-activities/configure-offer-selection.md)。

1. **[!UICONTROL Constraint]**&#x200B;字段限制此位置的优惠选择。 此约束可通过使用决策规则或一个或多个Adobe Experience Platform段来应用。

   要将优惠的选择限制为Adobe Experience Platform区段的成员，请选择&#x200B;**[!UICONTROL Segments]**，然后单击&#x200B;**[!UICONTROL Add segments]**。

   ![](../../assets/activity_constraint_segment.png)

   从左侧窗格添加一个或多个区段，使用&#x200B;**[!UICONTROL And]** / **[!UICONTROL Or]**&#x200B;逻辑运算符组合这些区段，然后单击&#x200B;**[!UICONTROL Select]**&#x200B;进行确认。

   有关如何使用区段的详细信息，请参阅[分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)。

   ![](../../assets/activity_constraint_segment2.png)

   如果要使用决策规则为此位置添加选择约束，请选择&#x200B;**[!UICONTROL Decision rule]**&#x200B;选项，然后将所需规则从左窗格拖至&#x200B;**[!UICONTROL Decision rule]**&#x200B;区域。 有关如何创建决策规则的详细信息，请参阅[本节](../offer-library/creating-decision-rules.md)。

   ![](../../assets/activity_constraint_rule.png)

## 添加回退优惠{#add-fallback}

选择将作为最后手段呈现给与优惠合格规则和约束不匹配的客户的回退优惠，然后单击&#x200B;**[!UICONTROL Next]**。

![](../../assets/add-fallback-offer.png)

## 审查并保存决定{#review}

如果所有内容配置正确，且您的决定已准备好向客户展示优惠，请单击&#x200B;**[!UICONTROL Finish]**，然后选择&#x200B;**[!UICONTROL Save and activate]**。

您还可以将决定保存为草稿，以便在以后编辑和激活该决定。

![](../../assets/save-activities.png)

此决定显示在列表中，状态为&#x200B;**[!UICONTROL Live]**&#x200B;或&#x200B;**[!UICONTROL Draft]**，具体取决于您在上一步中是否激活了它。

现在，它已准备好用于向客户提供优惠。 您可以选择它以显示其属性并编辑或隐藏它。

有关提供优惠的详细信息，请参阅以下部分：

* [在消息中添加个性化优惠](../../deliver-personalized-offers.md)
* [使用API交付优惠](../api-reference/decisions-api/deliver-offers.md)

![](../../assets/activities-created.png)

>[!NOTE]
>
>创建决策后，您可以单击列表中其名称以访问详细信息，并使用&#x200B;**[!UICONTROL Change log]**&#x200B;选项卡查看对其所做的所有更改(请参阅[优惠和决策更改日志](../get-started/user-interface.md#changes-log))。

## 教程视频{#video}

>[!NOTE]
>
>此视频适用于在Adobe Experience Platform上构建的Offer Decisioning应用程序服务。 但是，它提供了在Journey Optimizer环境中使用优惠的通用指导。

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
