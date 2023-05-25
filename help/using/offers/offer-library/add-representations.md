---
title: 向优惠添加呈现
description: 了解如何向优惠添加呈现
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 9%

---

# 向优惠添加呈现 {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="呈现"
>abstract="添加呈现以定义您的优惠在消息中显示的位置。优惠的呈现越多，在不同的投放上下文中使用该优惠的机会就越多。"

选件可以显示在消息中的不同位置：在带有图像的顶部横幅中、作为段落中的文本、作为HTML块等。 优惠的呈现越多，在不同的投放上下文中使用该优惠的机会就越多。

## 配置优惠的呈现 {#representations}

要向优惠添加一个或多个呈现并配置它们，请执行以下步骤。

1. 对于第一种表示形式，首先选择 **[!UICONTROL 渠道]** 将被使用。

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >中仅显示选定渠道的可用投放位置 **[!UICONTROL 投放]** 下拉列表。

1. 从列表中选择一个版面。

   您还可以使用 **[!UICONTROL 投放]** 下拉列表来浏览所有投放位置。

   ![](../assets/browse-button-placements.png)

   在那里，您仍然可以根据投放位置的渠道和/或内容类型筛选投放位置。 选择投放位置并单击 **[!UICONTROL 选择]**.

   ![](../assets/browse-placements.png)

1. 向演示文稿中添加内容。 了解如何在 [本节](#content).

1. 添加图像或URL等内容时，可以指定 **[!UICONTROL 目标链接]**：单击选件的用户将被定向到相应的页面。

   ![](../assets/offer-destination-link.png)

1. 最后，选择您选择的语言，以帮助识别和管理要向用户显示的内容。

1. 要添加其它表示法，请使用 **[!UICONTROL 添加呈现]** 按钮并添加所需数量的呈现。

   ![](../assets/offer-add-representation.png)

1. 添加所有表示法后，选择 **[!UICONTROL 下一个]**.

## 定义呈现的内容 {#content}

您可以将不同类型的内容添加到表示法中。

>[!NOTE]
>
>只能使用与版面的内容类型对应的内容。

### 添加图像 {#images}

如果所选版面为图像类型，则可以添加来自 **Adobe Experience Cloud资产** 库，由提供的资产集中存储库 [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> 使用 [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}, you need to deploy [!DNL Assets Essentials] for your organization and make sure that users are a part of the **Assets Essentials Consumer Users** or/and **Assets Essentials Users** Product profiles. Learn more on [this page](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html){target="_blank"}.

1. 选择 **[!UICONTROL 资产库]** 选项。

1. 选择 **[!UICONTROL 浏览]**.

   ![](../assets/offer-browse-asset-library.png)

1. 浏览资源以选择您选择的图像

1. 单击&#x200B;**[!UICONTROL 选择]**。

   ![](../assets/offer-select-asset.png)

### 添加HTML或JSON文件 {#html-json}

如果所选版面为HTML类型，您还可以添加来自的HTML或JSON内容 [Adobe Experience Cloud资源库](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"})。

例如，您在中创建了一个HTML电子邮件模板 [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target="_blank"} 并希望将该文件用于选件内容。 您只需将模板上传到，而无需创建新文件 **资产库** 以便在优惠的表示法中重复使用。

要在演示文稿中重用内容，请浏览 **资产库** 如中所述 [本节](#images) 并选择您选择的HTML或JSON文件。

![](../assets/offer-browse-asset-library-json.png)

### 添加URL {#urls}

要从外部公共位置添加内容，请选择 **[!UICONTROL URL]**，然后输入要添加的内容的URL地址。

您可以使用表达式编辑器个性化URL。 详细了解 [个性化](../../personalization/personalize.md#use-expression-editor).

![](../assets/offer-content-url.png)

例如，您希望对显示为选件的图像进行个性化。 你想让喜欢城市度假的用户看到纽约的天际线，想让喜欢海滩度假的用户看到夏威夷的北岸。

使用表达式编辑器可使用合并架构检索存储在Adobe Experience Platform中的配置文件属性。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schemas-overview.html){target="_blank"}

![](../assets/offer-content-url-personalization.png)

如果您指定 **[!UICONTROL 目标链接]**，您还可以对单击选件的用户所定向的URL进行个性化设置。

### 添加自定义文本 {#custom-text}

您还可以在选择兼容的版面时插入文本类型内容。

1. 选择 **[!UICONTROL 自定义]** 选项并单击 **[!UICONTROL 添加内容]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >此选项不适用于图像类型的投放。

1. 键入将在选件中显示的文本。

   ![](../assets/offer-text-content.png)

   您可以使用表达式编辑器对内容进行个性化设置。 详细了解 [个性化](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >仅 **[!UICONTROL 配置文件属性]**， **[!UICONTROL 区段成员资格]** 和 **[!UICONTROL 辅助函数]** 源可用于Decision Management。

