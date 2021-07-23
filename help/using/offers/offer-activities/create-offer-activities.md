---
title: 创建决策
description: 了解如何创建决策
feature: 优惠
topic: 集成
role: User
level: Intermediate
source-git-commit: 80451fcd012257c8648e751076ed668aa05c44c7
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 3%

---

# 创建决策 {#create-offer-activities}

决策（以前称为选件活动）是选件的容器，将利用选件决策引擎来根据投放的目标选择要交付的最佳选件。

➡️ [在视频中发现此功能](#video)

可在&#x200B;**[!UICONTROL Offers]**&#x200B;菜单/ **[!UICONTROL Decisions]**&#x200B;选项卡中访问决策列表。 过滤器可帮助您根据其状态或开始和结束日期来检索决策。

![](../../assets/activities-list.png)

在创建决策之前，请确保已在选件库中创建以下组件：

* [版面](../offer-library/creating-placements.md)
* [收藏集](../offer-library/creating-collections.md)
* [个性化优惠](../offer-library/creating-personalized-offers.md)
* [后备优惠](../offer-library/creating-fallback-offers.md)

## 创建决策 {#create-activity}

1. 访问决策列表，然后单击&#x200B;**[!UICONTROL Create decision]**。

1. 指定决策的名称及其开始和结束日期和时间，然后单击&#x200B;**[!UICONTROL Next]**。

   ![](../../assets/activities-name.png)

## 添加决策作用域 {#add-decision-scopes}

1. 从列表中拖放版面以将其添加到决策中，然后单击&#x200B;**[!UICONTROL Add collection]**。

   ![](../../assets/activities-placement.png)

   >[!NOTE]
   >
   >在决策中可多次选择同一版面。

1. 选择包含要考虑的选件的集合，然后单击&#x200B;**[!UICONTROL Add]**。

   ![](../../assets/activities-collection.png)

1. 所选选件将添加到版面中。 在此示例中，我们选择了两个将显示在JSON类型版面中的选件，该版面旨在将选件呈现到呼叫中心解决方案中。

   ![](../../assets/offers-added.png)

1. 默认情况下，如果多个选件符合此版面的条件，则具有最高优先级分数的选件将会交付给客户。

   如果要使用特定公式选择要交付的合格选件，请从&#x200B;**[!UICONTROL Rank offers by]**&#x200B;下拉列表中选择一个排名公式。 如需详细信息，请参阅[此部分](../offer-activities/configure-offer-selection.md)。

1. **[!UICONTROL Constraint]**&#x200B;字段可限制为此版面选择的选件。 可使用决策规则或一个或多个Adobe Experience Platform区段来应用此约束。

   要将选件的选择限制为Adobe Experience Platform区段的成员，请选择&#x200B;**[!UICONTROL Segments]**，然后单击&#x200B;**[!UICONTROL Add segments]**。

   ![](../../assets/activity_constraint_segment.png)

   从左窗格中添加一个或多个区段，使用&#x200B;**[!UICONTROL And]** / **[!UICONTROL Or]**&#x200B;逻辑运算符组合它们，然后单击&#x200B;**[!UICONTROL Select]**&#x200B;进行确认。

   有关如何使用区段的更多信息，请参阅[此页面](../../segment/about-segments.md)。

   ![](../../assets/activity_constraint_segment2.png)

   如果要使用决策规则为此版面添加选择约束，请选择&#x200B;**[!UICONTROL Decision rule]**&#x200B;选项，然后将所需规则从左侧窗格拖到&#x200B;**[!UICONTROL Decision rule]**&#x200B;区域。 有关如何创建决策规则的更多信息，请参阅[此部分](../offer-library/creating-decision-rules.md)。

   ![](../../assets/activity_constraint_rule.png)

## 添加后备优惠 {#add-fallback}

选择将作为最后手段向不符合选件资格规则和限制的客户显示的备用选件，然后单击&#x200B;**[!UICONTROL Next]**。

![](../../assets/add-fallback-offer.png)

## 查看并保存决策 {#review}

如果一切配置正确，则会显示决策属性的摘要。

1. 确保已做好准备，可用于向客户展示选件。
1. 单击 **[!UICONTROL Finish]**。
1. 然后选择&#x200B;**[!UICONTROL Save and activate]**。

   ![](../../assets/save-activities.png)

   您还可以将决定另存为草稿，以便在以后编辑和激活它。

此决策将以&#x200B;**[!UICONTROL Live]**&#x200B;或&#x200B;**[!UICONTROL Draft]**&#x200B;状态显示在列表中，具体取决于您是否在上一步中激活了该决策。

现在，它已准备好用于向客户交付选件。

## 决策列表 {#decision-list}

从决策列表中，您可以选择显示其属性的决策。 在此处，您还可以编辑它、更改其状态（**草稿**、**实时**、**完成**、**已存档**）、复制决定或删除它。

![](../../assets/decision_created.png)

选择&#x200B;**[!UICONTROL Edit]**&#x200B;按钮以返回到决策版模式，在该模式中，您可以修改决策的[details](#create-activity)、[决策范围](#add-decision-scopes)和[后备选件](#add-fallback)。

选择实时决策，然后单击&#x200B;**[!UICONTROL Deactivate]**&#x200B;将决策状态重新设置为&#x200B;**[!UICONTROL Draft]**。

要再次将状态设置为&#x200B;**[!UICONTROL Live]**，请选择现在显示的&#x200B;**[!UICONTROL Activate]**&#x200B;按钮。

![](../../assets/decision_activate.png)

**[!UICONTROL More actions]**&#x200B;按钮可启用下述操作。

![](../../assets/decision_more-actions.png)

* **[!UICONTROL Complete]**:将决策的状态设置 **[!UICONTROL Complete]**&#x200B;为，这意味着不能再调用决策。此操作仅适用于已激活的决策。 该决策仍可从列表中获取，但您无法将其状态重新设置为&#x200B;**[!UICONTROL Draft]**&#x200B;或&#x200B;**[!UICONTROL Approved]**。 您只能复制、删除或存档它。

* **[!UICONTROL Duplicate]**:创建具有相同属性、决策范围和备用选件的决策。默认情况下，新决策的状态为&#x200B;**[!UICONTROL Draft]**。

* **[!UICONTROL Delete]**:从列表中删除决策。

   >[!CAUTION]
   >
   >该决策及其内容将无法再访问。 此操作无法撤消。
   >
   >如果决策在其他对象中使用，则无法删除该决策。

* **[!UICONTROL Archive]**:将决策状态设置为 **[!UICONTROL Archived]**。该决策仍可从列表中获取，但您无法将其状态重新设置为&#x200B;**[!UICONTROL Draft]**&#x200B;或&#x200B;**[!UICONTROL Approved]**。 您只能复制或删除它。

您还可以通过选中相应的复选框，同时删除或更改多个决策的状态。

![](../../assets/decision_multiple-selection.png)

如果要更改具有不同状态的多个决策的状态，则只会更改相关状态。

![](../../assets/decision_change-status.png)

创建决策后，您可以在列表中单击其名称。

![](../../assets/decision_click-name.png)

这样，您就可以访问该决策的详细信息。 选择&#x200B;**[!UICONTROL Change log]**&#x200B;选项卡以[监视对决策所做的所有更改](../get-started/user-interface.md#changes-log)。

![](../../assets/decision_information.png)

## 教程视频 {#video}

>[!NOTE]
>
>此视频适用于基于Adobe Experience Platform构建的Offer decisioning应用程序服务。 但是，它为在Journey Optimizer上下文中使用选件提供了通用指导。

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
