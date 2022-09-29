---
title: 创建个性化优惠
description: 了解如何创建、配置和管理优惠
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: 11596bfbe5f98e362224384d51ba32d61275bc1d
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 3%

---

# 创建个性化优惠 {#create-personalized-offers}

在创建选件之前，请确保已创建：

* A **投放** 中显示选件。 请参阅 [创建版面](../offer-library/creating-placements.md)
* 如果要添加资格条件：a **决策规则** 定义显示选件的条件。 请参阅 [创建决策规则](../offer-library/creating-decision-rules.md).
* 一个或多个 **标记** 您可能希望与选件关联的选件。 请参阅 [创建标记](../offer-library/creating-tags.md).

➡️ [在视频中发现此功能](#video)

可在 **[!UICONTROL 选件]** 菜单。

![](../assets/offers_list.png)

## 创建选件 {#create-offer}

>[!CONTEXTUALHELP]
>id="od_offer_attributes"
>title="关于选件属性"
>abstract="使用选件属性，您可以将键值对与选件关联，以便进行报告和分析。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_attributes"
>title="选件属性"
>abstract="使用选件属性，您可以将键值对与选件关联，以便进行报告和分析。"

创建 **选件**，请执行以下步骤：

1. 单击 **[!UICONTROL 创建选件]**，然后选择 **[!UICONTROL 个性化优惠]**.

   ![](../assets/create_offer.png)

1. 指定选件的名称以及其开始和结束日期和时间。 在这些日期之外，决策引擎将不会选择选件。

   ![](../assets/offer_details.png)

   >[!CAUTION]
   >
   >更新开始/结束日期可能会对上限产生影响。 [了解详情](add-constraints.md#capping-change-date)

1. 您还可以关联一个或多个现有 **[!UICONTROL 标记]** 选件，以便您更轻松地搜索和组织选件库。 [了解详情](creating-tags.md)。

1. 的 **[!UICONTROL 选件属性]** 部分，可将键值对与选件关联以用于报告和分析。

1. 要为选件分配自定义或核心数据使用标签，请选择 **[!UICONTROL 管理访问权限]**. [了解有关对象级别访问控制(OLAC)的更多信息](../../administration/object-based-access.md)

   ![](../assets/offer_manage-access.png)

1. 添加表示法以定义选件在消息中的显示位置。 [了解详情](add-representations.md)

   ![](../assets/channel-placement.png)

1. 添加约束以设置要显示的选件的条件。 [了解详情](add-constraints.md)

   >[!NOTE]
   >
   >选择区段或决策规则时，可以查看有关估计的合格用户档案的信息。 单击 **[!UICONTROL 刷新]** 更新数据。
   >
   >请注意，如果规则参数包含的数据不在配置文件中，例如上下文数据，则配置文件估计将不可用。 例如，要求当前天气为≥80度的资格规则。

   ![](../assets/offer-constraints-example.png)

1. 查看并保存选件。 [了解详情](#review)

## 查看选件 {#review}

定义资格规则和约束后，将显示选件属性的摘要。

1. 确保已正确配置所有内容。

1. 您可以显示有关估计的合格用户档案的信息。 单击 **[!UICONTROL 刷新]** 更新数据。

   ![](../assets/offer-summary-estimate.png)

1. 当您的选件已准备好呈现给用户时，单击 **[!UICONTROL 完成]**.

1. 选择 **[!UICONTROL 保存和批准]**.

   ![](../assets/offer_review.png)

   您还可以将选件另存为草稿，以便稍后进行编辑和批准。

该选件将显示在列表中，其中 **[!UICONTROL 已批准]** 或 **[!UICONTROL 草稿]** 状态，具体取决于您在上一步中是否批准了它。

现在，它已准备好交付给用户。

![](../assets/offer_created.png)

## 管理选件 {#offer-list}

从选件列表中，您可以选择选件以显示其属性。 您还可以编辑、更改其状态(**草稿**, **已批准**, **已存档**)、复制选件或将其删除。

![](../assets/offer_created.png)

选择 **[!UICONTROL 编辑]** 按钮返回到选件编辑模式，在该模式中，您可以修改选件的 [详细信息](#create-offer), [表示](#representations)，以及编辑 [资格规则和限制](#eligibility).

选择已批准的选件并单击 **[!UICONTROL 撤消批准]** 将选件状态设置回 **[!UICONTROL 草稿]**.

再次将状态设置为 **[!UICONTROL 已批准]**，则选择当前显示的相应按钮。

![](../assets/offer_approve.png)

的 **[!UICONTROL 更多操作]** 按钮可启用下面描述的操作。

![](../assets/offer_more-actions.png)

* **[!UICONTROL 复制]**:创建具有相同属性、表示、资格规则和约束的选件。 默认情况下，新选件具有 **[!UICONTROL 草稿]** 状态。
* **[!UICONTROL 删除]**:从列表中删除选件。

   >[!CAUTION]
   >
   >该选件及其内容将无法再访问。 此操作无法撤消。
   >
   >如果选件在收藏集或决策中使用，则无法删除它。 必须先从任何对象中删除选件。

* **[!UICONTROL 存档]**:将选件状态设置为 **[!UICONTROL 已存档]**. 该选件仍可从列表中获取，但您无法将其状态重新设置为 **[!UICONTROL 草稿]** 或 **[!UICONTROL 已批准]**. 您只能复制或删除它。

您还可以通过选中相应的复选框来同时删除或更改多个选件的状态。

![](../assets/offer_multiple-selection.png)

如果要更改多个状态不同的选件的状态，则只会更改相关状态。

![](../assets/offer_change-status.png)

创建选件后，您可以从列表中单击其名称。

![](../assets/offer_click-name.png)

这样，您就可以访问该选件的详细信息。 选择 **[!UICONTROL 更改日志]** 选项卡 [监控所有更改](../get-started/user-interface.md#monitoring-changes) 已经提出了。

![](../assets/offer_information.png)

## 教程视频 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
