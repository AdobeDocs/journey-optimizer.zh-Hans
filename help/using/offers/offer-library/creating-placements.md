---
title: 创建放置环境
description: 了解如何为您的优惠创建投放位置
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: dfaf887e-d4b3-45b0-8297-bffdb0abff4d
source-git-commit: 88e7140183700da0283fa00d89f6fff2c71c138f
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 31%

---

# 创建放置环境 {#create-placements}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement"
>title="投放"
>abstract="投放位置是用于展示产品建议的容器。它有助于确保正确的产品建议内容显示在消息中的正确位置。从“组件”菜单创建投放位置。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement_request"
>title="请求设置"
>abstract="启用&#x200B;**[!UICONTROL 允许在多个投放位置中出现重复内容]**&#x200B;选项，以便系统在多个投放位置中考虑相同的产品建议。使用&#x200B;**[!UICONTROL 请求产品建议]**&#x200B;字段来调整返回的产品建议数量。例如，如果您选择 2，则在所选决策范围内将显示最佳的 2 个产品建议。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement_response"
>title="响应格式"
>abstract="**[!UICONTROL 包含内容]**&#x200B;和&#x200B;**[!UICONTROL 包含元数据]**&#x200B;选项允许您指定是否应在 API 响应中返回产品建议的内容和元数据。您可以包含所有元数据或仅包含特定字段。默认情况下，“包含元数据”值设置为 true。"

版面有助于确保正确的选件内容显示在消息的正确位置。 向产品建议添加内容时，将要求您选择可以显示该内容的版面。

➡️ [在此视频中了解如何创建投放位置](#video)

在下面的示例中，有三个投放位置，对应于不同类型的内容(图像、文本、HTML)。

![](../assets/offers_placement_schema.png)

可在&#x200B;**[!UICONTROL 组件]**&#x200B;菜单中访问版面列表。 您可以使用过滤器来帮助您根据特定渠道或内容检索投放位置。

![](../assets/placements_filter.png)

要创建投放位置，请执行以下步骤：

1. 单击&#x200B;**[!UICONTROL 创建版面]**。

   ![](../assets/offers_placement_creation.png)

1. 定义投放位置的属性：

   * **[!UICONTROL 名称]**：投放位置的名称。 确保定义有意义的名称，以便更轻松地检索它。
   * **[!UICONTROL 渠道类型]**：将使用投放位置的渠道。
   * **[!UICONTROL 内容类型]**：允许投放位置显示的内容类型：文本、HTML、图像链接或JSON。
   * **[!UICONTROL 描述]**：投放位置的描述（可选）。

   ![](../assets/offers_placement_creation_properties.png)

1. **[!UICONTROL 请求设置]**&#x200B;和&#x200B;**[!UICONTROL 响应格式]**&#x200B;部分提供了其他参数：

   * **[!UICONTROL 允许跨版面存在重复项]**：控制是否可以在不同的版面中多次建议相同的选件。 如果启用，系统将考虑为多个投放位置使用相同的选件。 默认情况下，参数设置为false。

     如果此选项被设置为false，则决策请求中的任何投放位置都将继承“false”设置。

   * **[!UICONTROL 请求优惠]**：默认情况下，为每个配置文件返回一个决策范围优惠。 您可以使用此选项调整返回的选件数。 例如，如果您选择 2，则在所选决策范围内将显示最佳的 2 个产品建议。

   * **[!UICONTROL Include content]** / **[!UICONTROL Include metadata]**：指定API响应中是否应返回选件的内容和元数据。 您可以包含所有元数据或仅包含特定字段。默认情况下，“包含元数据”值设置为 true。

   如果您使用[Decisioning API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/decisioning-api.html?lang=zh-Hans)，也可以将这些参数直接设置为您的API请求。 但是，在用户界面中配置它们可以帮助您节省时间，因为您不必在每个API请求中传递它们。 请注意，如果您在用户界面和API请求中配置参数，则API请求中的值将优先于界面中的值。

   >[!NOTE]
   >
   >如果您使用的是[Edge Decisioning API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api.html?lang=zh-Hans&)，则无法在请求中设置这些参数。 您需要在此屏幕中定义它们。
   >
   >如果您使用的是[批量决策API](../api-reference/offer-delivery-api/batch-decisioning-api.md)，则可以在此屏幕或API请求中设置这些参数。 如果屏幕和APi请求之间的参数值不匹配，将使用请求值。

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;确认。

1. 创建投放位置后，该投放位置将显示在投放位置列表中。 您可以选择它以显示其属性并对其进行编辑。

   ![](../assets/placement_created.png)

## 操作说明视频{#video}

了解如何在决策管理中创建投放位置。

>[!VIDEO](https://video.tv.adobe.com/v/329372?quality=12)

