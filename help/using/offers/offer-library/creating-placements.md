---
title: 创建投放位置
description: 了解如何为选件创建版面
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: dfaf887e-d4b3-45b0-8297-bffdb0abff4d
source-git-commit: 51f93270c969875e94cc3e98919149d67d764ed1
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 11%

---

# 创建投放位置 {#create-placements}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement"
>title="版面"
>abstract="投放位置是用于展示优惠的容器。它有助于确保正确的优惠内容显示在消息中的正确位置。从“组件”菜单创建投放位置。"

版面有助于确保正确的选件内容显示在消息中的正确位置。 向选件添加内容时，将要求您选择可以显示该内容的版面。

➡️ [在此视频中了解如何创建版面](#video)

在以下示例中，有三个版面，对应于不同类型的内容(图像、文本、HTML)。

![](../assets/offers_placement_schema.png)

可在 **[!UICONTROL 组件]** 菜单。 过滤器可帮助您根据特定渠道或内容检索版面。

![](../assets/placements_filter.png)

要创建版面，请执行以下步骤：

1. 单击 **[!UICONTROL 创建版面]**.

   ![](../assets/offers_placement_creation.png)

1. 定义版面的属性：

   * **[!UICONTROL 名称]**:版面的名称。 确保定义一个有意义的名称，以便更轻松地检索该名称。
   * **[!UICONTROL 渠道类型]**:将用于放置的渠道。
   * **[!UICONTROL 内容类型]**:允许版面显示的内容类型：文本、HTML、图像链接或JSON。
   * **[!UICONTROL 描述]**:版面的描述（可选）。

   ![](../assets/offers_placement_creation_properties.png)


1. 的 **[!UICONTROL 请求设置]** 和 **[!UICONTROL 响应格式]** 部分提供了其他参数：

   * **[!UICONTROL 允许跨版面重复项]**:控制是否可以在不同版面中多次建议同一选件。 如果启用，系统将考虑同一选件用于多个版面。 默认情况下，参数设置为false。

      如果对于决策请求中的任何版面，将此选项设置为false，则请求中的所有版面都将继承“false”设置。

   * **[!UICONTROL 请求选件]**:默认情况下，每个用户档案会返回一个决策范围选件。 您可以使用此选项调整返回的选件数。 例如，如果您选择2，则将显示选定决策范围的2个最佳选件。

   * **[!UICONTROL 包含内容]** / **[!UICONTROL 包含元数据]**:指定是否应在API响应中返回选件的内容和元数据。 您只能包含所有元数据或特定字段。 默认情况下，Include元数据值设置为true。
   如果您使用 [决策API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/decisioning-api.html). 但是，在用户界面中配置这些参数可以帮助您节省时间，因为您无需在每个API请求中传递它们。 请注意，如果您在用户界面和API请求中都配置了参数，则API请求中的值将优先于界面中的值。

   >[!NOTE]
   >
   >如果您使用 [Edge Decisioning API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api.html?)，则无法在请求中设置这些参数。 您需要在此屏幕中定义它们。
   >
   >如果您使用 [批量决策API](../api-reference/offer-delivery-api/batch-decisioning-api.md)，您可以在此屏幕或API请求中设置这些参数。 如果屏幕和APi请求之间的参数值不匹配，则将使用请求值。

1. 单击 **[!UICONTROL 保存]** 确认。

1. 创建版面后，该版面会显示在版面列表中。 您可以选择它以显示其属性并进行编辑。

   ![](../assets/placement_created.png)

## 操作方法视频{#video}

了解如何在决策管理中创建版面。

>[!VIDEO](https://video.tv.adobe.com/v/329372?quality=12)

