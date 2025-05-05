---
title: 创建个性化产品建议
description: 了解如何创建、配置和管理优惠
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 18%

---

# 创建个性化产品建议 {#create-personalized-offers}

在创建选件之前，请确保已创建：

* 将在其中显示优惠的&#x200B;**投放位置**。 查看[创建版面](../offer-library/creating-placements.md)
* 如果要添加资格条件： **决策规则**，该规则将定义优惠的呈现条件。 请参阅[创建决策规则](../offer-library/creating-decision-rules.md)。
* 要与优惠关联的一个或多个&#x200B;**收藏集限定符**（以前称为“标记”）。 请参阅[创建集合限定符](../offer-library/creating-tags.md)。

➡️ [在视频中了解此功能](#video)

可在&#x200B;**[!UICONTROL 优惠]**&#x200B;菜单中访问个性化优惠列表。

![](../assets/offers_list.png)

## 创建产品建议 {#create-offer}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_details"
>title="产品建议详细信息"
>abstract="填写产品建议的名称及其开始和结束日期。在这些日期之外，决策引擎将不会选择该产品建议。"

>[!CONTEXTUALHELP]
>id="od_offer_attributes"
>title="关于产品建议属性"
>abstract="借助产品建议属性，可将键值对与产品建议相关联，作报告和分析用途。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_attributes"
>title="产品建议属性"
>abstract="借助产品建议属性，可将键值对与产品建议相关联，作报告和分析用途。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_new_personalized"
>title="个性化产品建议"
>abstract="个性化产品建议是基于合格规则和约束的可定制消息。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_new_fallback"
>title="备用产品建议"
>abstract="后备产品建议是当最终用户没有资格获得任何个性化产品建议时显示的默认产品建议。"

要创建&#x200B;**选件**，请执行以下步骤：

1. 单击&#x200B;**[!UICONTROL 创建优惠]**，然后选择&#x200B;**[!UICONTROL 个性化优惠]**。

   ![](../assets/create_offer.png)

1. 指定选件的名称及其开始和结束日期和时间。 在这些日期之外，决策引擎将不会选择该产品建议。

   >[!NOTE]
   >
   >选择时间时，会考虑您当前的时区。

   ![](../assets/offer_details.png)

   >[!CAUTION]
   >
   >更新开始/结束日期可能会影响上限。 [了解详情](add-constraints.md#capping-change-date)

1. 您还可以将一个或多个现有的&#x200B;**[!UICONTROL 收藏集限定符]**&#x200B;关联到选件，使您能够更轻松地搜索和组织选件库。 [了解详情](creating-tags.md)。

1. **[!UICONTROL 选件属性]**&#x200B;部分允许您关联键值对和选件，以便进行报告和分析。

1. 要将自定义或核心数据使用标签分配给选件，请选择&#x200B;**[!UICONTROL 管理访问权限]**。 [了解有关对象级访问控制(OLAC)的更多信息](../../administration/object-based-access.md)

   ![](../assets/offer_manage-access.png)

1. 添加呈现以定义您的产品建议在消息中显示的位置。[了解详情](add-representations.md)

   ![](../assets/channel-placement.png)

   >[!CAUTION]
   >
   >选件（包括其所有呈现）的大小不能超过300KB。

1. 添加约束以设置要显示优惠的条件。 [了解详情](add-constraints.md)

   >[!NOTE]
   >
   >在选择受众或决策规则时，您可以看到有关预计的合格用户档案的信息。 单击&#x200B;**[!UICONTROL 刷新]**&#x200B;以更新数据。
   >
   >请注意，当规则参数包含不在配置文件中的数据（如上下文数据）时，配置文件估计不可用。 例如，资格规则要求当前天气为≥80度。

   ![](../assets/offer-constraints-example.png)

1. 查看并保存选件。 [了解详情](#review)

## 查看选件 {#review}

定义资格规则和限制后，将显示优惠属性的摘要。

1. 确保一切配置正确。

1. 您可以显示有关预计的合格用户档案的信息。 单击&#x200B;**[!UICONTROL 刷新]**&#x200B;以更新数据。

   ![](../assets/offer-summary-estimate.png)

1. 当您的选件已准备好呈现给用户时，请单击&#x200B;**[!UICONTROL 完成]**。

1. 选择&#x200B;**[!UICONTROL 保存并批准]**。

   ![](../assets/offer_review.png)

   您还可以将优惠另存为草稿，以便稍后进行编辑和批准。

该选件显示在状态为&#x200B;**[!UICONTROL 已批准]**&#x200B;或&#x200B;**[!UICONTROL 草稿]**&#x200B;的列表中，具体取决于您在上一步中是否批准了该选件。

现在已准备好交付给用户。

![](../assets/offer_created.png)

## 管理优惠 {#offer-list}

从选件列表中，您可以选择要显示其属性的选件。 您还可以编辑选件、更改其状态（**草稿**、**已批准**、**已存档**）、复制选件或删除选件。

![](../assets/offer_created.png)

选择&#x200B;**[!UICONTROL 编辑]**&#x200B;按钮以返回优惠版本模式，在该模式下，您可以修改优惠的[详细信息](#create-offer)、[呈现](#representations)，以及编辑[资格规则和约束](#eligibility)。

选择已批准的优惠并单击&#x200B;**[!UICONTROL 撤消批准]**&#x200B;以将优惠状态设置回&#x200B;**[!UICONTROL 草稿]**。

若要再次将状态设置为&#x200B;**[!UICONTROL 已批准]**，请选择现在显示的相应按钮。

![](../assets/offer_approve.png)

使用&#x200B;**[!UICONTROL 更多操作]**&#x200B;按钮可启用下述操作。

![](../assets/offer_more-actions.png)

* **[!UICONTROL 复制]**：创建具有相同属性、呈现、资格规则和约束的优惠。 默认情况下，新选件具有&#x200B;**[!UICONTROL 草稿]**&#x200B;状态。
* **[!UICONTROL 删除]**：从列表中删除选件。

  >[!CAUTION]
  >
  >将无法再访问选件及其内容。 此操作无法撤消。
  >
  >如果选件用在收藏集或决策中，则无法删除该选件。 必须先从任何对象中删除选件。

* **[!UICONTROL 存档]**：将选件状态设置为&#x200B;**[!UICONTROL 已存档]**。 该优惠仍然可以从列表中获得，但您不能将其状态设置回&#x200B;**[!UICONTROL 草稿]**&#x200B;或&#x200B;**[!UICONTROL 已批准]**。 您只能复制或删除它。

您还可以通过选择相应的复选框来同时删除或更改多个选件的状态。

![](../assets/offer_multiple-selection.png)

如果要更改具有不同状态的多个选件的状态，则只会更改相关状态。

![](../assets/offer_change-status.png)

创建选件后，您可以从列表中单击其名称。

![](../assets/offer_click-name.png)

这使您可以访问该选件的详细信息。 选择&#x200B;**[!UICONTROL 更改日志]**&#x200B;选项卡以[监视已对选件所做的所有更改](../get-started/user-interface.md#monitoring-changes)。

![](../assets/offer_information.png)

## 教程视频 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/341341?quality=12&captions=chi_hans)
