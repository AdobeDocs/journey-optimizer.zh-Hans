---
title: 将呈现添加到产品建议
description: 了解如何向优惠添加呈现
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 9b66f4871d8b539bf0201b2974590672205a3243
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 7%

---

# 将呈现添加到产品建议 {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="呈现"
>abstract="添加呈现以定义您的产品建议在消息中显示的位置。产品建议的呈现越多，在不同的投放上下文中使用该产品建议的机会就越多。"

选件可以显示在消息中的不同位置：在带有图像的顶部横幅中、作为段落中的文本或者HTML块中，等等。 产品建议的呈现越多，在不同的投放上下文中使用该产品建议的机会就越多。

## 配置优惠的呈现 {#representations}

要向优惠添加一个或多个呈现并配置它们，请执行以下步骤。

1. 对于第一种呈现，首先选择将使用的&#x200B;**[!UICONTROL 渠道]**。

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >只有所选渠道的可用版面才会显示在&#x200B;**[!UICONTROL 版面]**&#x200B;下拉列表中。

1. 从列表中选择版面。

   您还可以使用&#x200B;**[!UICONTROL 版面]**&#x200B;下拉列表旁边的按钮来浏览所有版面。

   ![](../assets/browse-button-placements.png)

   在那里，您仍然可以根据投放位置的渠道和/或内容类型筛选投放位置。 选择版面，然后单击&#x200B;**[!UICONTROL 选择]**。

   ![](../assets/browse-placements.png)

1. 向演示文稿添加内容。 在[本节](#content)中了解详情。

1. 添加图像或URL等内容时，您可以指定&#x200B;**[!UICONTROL 目标链接]**：单击选件的用户将被定向到相应的页面。

   ![](../assets/offer-destination-link.png)

1. 最后，选择您选择的语言，以帮助识别和管理要向用户显示的内容。

1. 要添加其他呈现，请使用&#x200B;**[!UICONTROL 添加呈现]**&#x200B;按钮，并根据需要添加任意数量的呈现。

   ![](../assets/offer-add-representation.png)

1. 添加所有呈现后，请选择&#x200B;**[!UICONTROL 下一步]**。

## 定义呈现的内容 {#content}

您可以向表示法添加不同类型的内容。

>[!NOTE]
>
>只有与版面的内容类型对应的内容才可供使用。

### 添加图像 {#images}

如果所选版面为图像类型，则可以添加来自&#x200B;**Adobe Experience Cloud资源**&#x200B;库的内容，该库是由[!DNL Adobe Experience Manager Assets]提供的集中式资源存储库。

>[!NOTE]
>
> 若要使用[Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}，您需要为组织部署[!DNL Assets Essentials]，并确保用户是&#x200B;**Assets Essentials消费者用户**&#x200B;或/和&#x200B;**Assets Essentials用户**&#x200B;产品配置文件的一部分。 在[此页面](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html){target="_blank"}上了解详情。

1. 选择&#x200B;**[!UICONTROL 资源库]**&#x200B;选项。

1. 选择&#x200B;**[!UICONTROL 浏览]**。

   ![](../assets/offer-browse-asset-library.png)

1. 浏览资源以选择您选择的图像

1. 单击&#x200B;**[!UICONTROL 选择]**。

   ![](../assets/offer-select-asset.png)

### 添加HTML或JSON文件 {#html-json}

如果所选版面为HTML类型，您还可以添加来自[HTML资源库](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}的Adobe Experience Cloud或JSON内容。

例如，您在[Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target="_blank"}中创建了一个HTML电子邮件模板，并想要将该文件用于选件内容。 您只需将模板上传到&#x200B;**资源库**&#x200B;中，以便能够在优惠的呈现中重复使用它，而无需创建新文件。

要在呈现中重用您的内容，请按照[此部分](#images)中的说明浏览&#x200B;**资源库**，并选择您选择的HTML或JSON文件。

![](../assets/offer-browse-asset-library-json.png)

### 添加URL {#urls}

若要从外部公共位置添加内容，请选择&#x200B;**[!UICONTROL URL]**，然后输入要添加内容的URL地址。

您可以使用个性化编辑器个性化URL。 了解有关[个性化](../../personalization/personalize.md#use-expression-editor)的更多信息。

![](../assets/offer-content-url.png)

例如，您希望将显示为选件的图像个性化。 你想让喜欢城市度假的用户看到纽约的天际线，想让喜欢海滩度假的用户看到夏威夷的北岸。

使用个性化编辑器，使用合并模式检索存储在Adobe Experience Platform中的配置文件属性。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schemas-overview.html){target="_blank"}

![](../assets/offer-content-url-personalization.png)

如果您指定了&#x200B;**[!UICONTROL 目标链接]**，您还可以将单击选件的用户定向到的URL个性化。

### 添加自定义文本 {#custom-text}

您还可以在选择兼容的版面时插入文本类型内容。

1. 选择&#x200B;**[!UICONTROL 自定义]**&#x200B;选项，然后单击&#x200B;**[!UICONTROL 添加内容]**。

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >此选项不适用于图像类型的投放。

1. 键入将在选件中显示的文本。

   ![](../assets/offer-text-content.png)

   您可以使用个性化编辑器将内容个性化。 了解有关[个性化](../../personalization/personalize.md#use-expression-editor)的更多信息。

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >只有&#x200B;**[!UICONTROL 配置文件属性]**、**[!UICONTROL 受众]**&#x200B;和&#x200B;**[!UICONTROL 帮助程序函数]**&#x200B;源可用于决策管理。

## 根据上下文数据个性化呈现{#context-data}

在[Edge decisioning](../api-reference/offer-delivery-api/edge-decisioning-api.md)调用中传递上下文数据时，您可以利用这些数据动态地对呈现进行个性化。 例如，您可以根据实时因素（如决策时的当前天气条件）定制优惠的表示方式。

要在优惠呈现中使用上下文数据，请使用`profile.timeSeriesEvents.`命名空间将上下文数据变量直接合并到呈现内容中。

下面是一个语法示例，用于根据用户的操作系统对优惠的表示进行个性化：

```
 {%#if profile.timeSeriesEvents.device.model = "Apple"%}ios{%else%}android{%/if%} 
```

包含上下文数据的相应Edge决策请求如下：

```
{
    "body": {
        "xdm": {
            "identityMap": {
                "Email": [
                    {
                        "id": "xyz@abc.com"
                    }
                ]
            },
            "device": {
                "model": "Apple"
            }
        },
        "extra": {
            "query": {
                "decisionScopes": [
                    "eyJ4ZG06..."
                ]
            }
        }
    }
}
```
