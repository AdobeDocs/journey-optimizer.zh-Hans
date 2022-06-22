---
title: 向选件添加表示法
description: 了解如何向选件添加表示法
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 3513f5415ebbac1be889ba390877611ad5a71030
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 1%

---

# 向选件添加表示法 {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="表示"
>abstract="添加表示法以定义选件在消息中的显示位置。 选件表示的越多，在不同版面环境中使用该选件的机会就越多。"

选件可以显示在消息中的不同位置：在顶部横幅中显示图像、段落中的文本、HTML块等。 选件表示的越多，在不同版面环境中使用该选件的机会就越多。

## 配置选件的表示形式 {#representations}

要向选件添加一个或多个表示形式并对其进行配置，请执行以下步骤。

1. 对于第一个表示，首先选择 **[!UICONTROL Channel]** 将使用的URL。

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >只有所选渠道的可用版面会显示在 **[!UICONTROL Placement]** 下拉列表。

1. 从列表中选择版面。

   您还可以使用 **[!UICONTROL Placement]** 下拉列表以浏览所有版面。

   ![](../assets/browse-button-placements.png)

   您仍然可以根据其渠道和/或内容类型筛选版面。 选择版面并单击 **[!UICONTROL Select]**.

   ![](../assets/browse-placements.png)

1. 向您的演示文稿中添加内容。 了解 [此部分](#content).

1. 添加图像或URL等内容时，您可以指定 **[!UICONTROL Destination link]**:单击选件的用户将被定向到相应的页面。

   ![](../assets/offer-destination-link.png)

1. 最后，选择您选择的语言，以帮助识别和管理要向用户显示的内容。

1. 要添加其他表示形式，请使用 **[!UICONTROL Add representation]** 按钮，并根据需要添加任意数量的表示形式。

   ![](../assets/offer-add-representation.png)

1. 添加所有表示形式后，选择 **[!UICONTROL Next]**.

## 定义表示的内容 {#content}

您可以向表示中添加不同类型的内容。

>[!NOTE]
>
>只有与版面内容类型对应的内容才可供使用。

### 添加图像 {#images}

如果所选版面是图像类型，则可以添加来自 **Adobe Experience Cloud Asset** 库，由提供的集中资产存储库 [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> 使用 [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target=&quot;_blank&quot;}，您需要部署 [!DNL Assets Essentials] ，并确保用户是 **Assets Essentials消费者用户** 或/和 **Assets Essentials用户** 产品配置文件。 了解详情 [本页](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html){target=&quot;_blank&quot;}。

1. 选择 **[!UICONTROL Asset library]** 选项。

1. 选择 **[!UICONTROL Browse]**。

   ![](../assets/offer-browse-asset-library.png)

1. 浏览资产以选择您选择的图像

1. 单击 **[!UICONTROL Select]**。

   ![](../assets/offer-select-asset.png)

### 添加HTML或JSON文件 {#html-json}

如果所选版面是HTML类型，则还可以添加来自的HTML或JSON内容 [Adobe Experience Cloud资产库](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target=&quot;_blank&quot;})。

例如，您在 [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target=&quot;_blank&quot;}，并且您希望将该文件用于选件内容。 您只需将模板上传到 **资产库** 以便能够在选件的表示法中重复使用。

要在演示文稿中重复使用您的内容，请浏览 **资产库** 如 [此部分](#images) 并选择您选择的HTML或JSON文件。

![](../assets/offer-browse-asset-library-json.png)

### 添加URL {#urls}

要从外部公共位置添加内容，请选择 **[!UICONTROL URL]**，然后输入要添加内容的URL地址。

![](../assets/offer-content-url.png)

### 添加自定义文本 {#custom-text}

您还可以在选择兼容的版面时插入文本类型内容。

1. 选择 **[!UICONTROL Custom]** 选项并单击 **[!UICONTROL Add content]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >此选项不适用于图像类型放置。

1. 键入将在选件中显示的文本。

   ![](../assets/offer-text-content.png)

   您可以使用表达式编辑器将内容个性化。 了解详情 [个性化](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >仅 **[!UICONTROL Profile attributes]**, **[!UICONTROL Segment memberships]** 和 **[!UICONTROL Helper functions]** 源可用于决策管理。

