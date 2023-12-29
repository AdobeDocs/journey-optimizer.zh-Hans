---
title: 创建投放位置
description: 了解如何为您的优惠创建投放位置
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: dfaf887e-d4b3-45b0-8297-bffdb0abff4d
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 12%

---

# 创建投放位置 {#create-placements}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement"
>title="版面"
>abstract="投放位置是用于展示优惠的容器。它有助于确保正确的优惠内容显示在消息中的正确位置。从“组件”菜单创建投放位置。"

版面有助于确保正确的选件内容显示在消息的正确位置。 向选件添加内容时，将要求您选择可以显示该内容的版面。

➡️ [在本视频中了解如何创建投放位置](#video)

在下面的示例中，有三个投放位置，对应于不同类型的内容(图像、文本、HTML)。

![](../assets/offers_placement_schema.png)

可在以下位置访问投放位置列表： **[!UICONTROL 组件]** 菜单。 您可以使用过滤器来帮助您根据特定渠道或内容检索投放位置。

![](../assets/placements_filter.png)

要创建投放位置，请执行以下步骤：

1. 单击 **[!UICONTROL 创建投放位置]**.

   ![](../assets/offers_placement_creation.png)

1. 定义投放位置的属性：

   * **[!UICONTROL 名称]**：投放位置的名称。 确保定义有意义的名称，以便更轻松地检索它。
   * **[!UICONTROL 渠道类型]**：使用投放位置的渠道。
   * **[!UICONTROL 内容类型]**：允许投放位置显示的内容类型：文本、HTML、图像链接或JSON。
   * **[!UICONTROL 描述]**：投放位置的描述（可选）。

   ![](../assets/offers_placement_creation_properties.png)


1. 此 **[!UICONTROL 请求设置]** 和 **[!UICONTROL 响应格式]** 部分提供了其他参数：

   * **[!UICONTROL 允许跨投放位置重复项]**：控制是否可以跨不同投放位置多次提议相同的选件。 如果启用，系统将考虑为多个投放位置使用相同的选件。 默认情况下，参数设置为false。

     如果此选项被设置为false，则决策请求中的任何投放位置都将继承“false”设置。

   * **[!UICONTROL 请求优惠]**：默认情况下，为每个用户档案返回一个决策范围选件。 您可以使用此选项调整返回的选件数。 例如，如果您选择2，则会为选定的决策范围显示最佳的2个优惠。

   * **[!UICONTROL 包含内容]** / **[!UICONTROL 包含元数据]**：指定是否应在API响应中返回选件的内容和元数据。 您可以仅包含所有元数据或特定字段。 默认情况下，“包含元数据”值设置为true。

   如果您正在使用，则这些参数也可以直接设置到API请求中 [Decisioning API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/decisioning-api.html). 但是，在用户界面中配置它们可以帮助您节省时间，因为您不必在每个API请求中传递它们。 请注意，如果您在用户界面和API请求中配置参数，则API请求中的值将优先于界面中的值。

   >[!NOTE]
   >
   >如果您使用 [Edge Decisioning API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api.html?)，则无法在请求中设置这些参数。 您需要在此屏幕中定义它们。
   >
   >如果您使用 [批量决策API](../api-reference/offer-delivery-api/batch-decisioning-api.md)中，您可以在此屏幕或API请求中设置这些参数。 如果屏幕和APi请求之间的参数值不匹配，将使用请求值。

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;确认。

1. 创建投放位置后，该投放位置将显示在投放位置列表中。 您可以选择它以显示其属性并对其进行编辑。

   ![](../assets/placement_created.png)

## 操作方法视频{#video}

了解如何在决策管理中创建投放位置。

>[!VIDEO](https://video.tv.adobe.com/v/329372?quality=12)

