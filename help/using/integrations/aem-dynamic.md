---
solution: Journey Optimizer
product: journey optimizer
title: Dynamic media
description: 将Dynamic Media与Journey Optimizer结合使用
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: ccfc0870a8d59d16c7f5b6b02856785aa28dd307
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# 使用Dynamic Media {#aem-dynamic}

>[!AVAILABILITY]
>
>此集成仅适用于使用Dynamic Media Manager as a Cloud Service的客户。

资产选择器现在支持Dynamic Media，允许您在Journey Optimizer中无缝选择和使用批准的Dynamic Media演绎版。 对Adobe Experience Manager中的资源所做的更改会立即反映在您的Journey Optimizer内容中，从而确保始终使用最新版本，而无需手动更新。

要了解有关Adobe Experience Manager as a Cloud Service中Dynamic Media的更多信息，请参阅[Experience Manager文档](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media)。

## 添加和管理Dynamic Media

通过将Adobe Experience Manager as a Cloud Service中的Dynamic Media直接插入您的Journey Optimizer内容，可针对任何屏幕或浏览器增强和优化您的内容。  然后，您可以调整大小、裁切、增强并根据需要进行其他调整。

1. 将&#x200B;**[!UICONTROL HTML组件]**&#x200B;拖放到您的内容中。

1. 选择&#x200B;**[!UICONTROL 显示源代码]**。

   ![](assets/dynamic-media-1.png)

1. 在&#x200B;**[!UICONTROL 编辑HTML]**&#x200B;菜单中，导航到&#x200B;**[!UICONTROL Assets]**，然后单击&#x200B;**[!UICONTROL 打开资源选择器]**。

   或者，您可以复制并粘贴资产的URL。

   ![](assets/dynamic-media-2.png)

1. 浏览您的AEM资源，然后选择要添加到内容中的资源。

1. 根据需要调整图像参数（例如，高度、宽度），以匹配您的资源要求。

1. 单击&#x200B;**[!UICONTROL 保存]**。

您的内容现在包括Dynamic Media。 您在Experience Manager中所做的任何更新都将自动显示在Journey Optimizer中。

## Personalization使用带文本覆盖的图像

使用带有文本覆盖的图像轻松个性化内容。
可在AJO中更改文本而更改URL，如上所述

1. 将&#x200B;**[!UICONTROL HTML组件]**&#x200B;拖放到您的内容中。

1. 选择&#x200B;**[!UICONTROL 显示源代码]**。

1. 从&#x200B;**[!UICONTROL 编辑HTML]**&#x200B;菜单中，访问&#x200B;**[!UICONTROL Assets]**，然后&#x200B;**[!UICONTROL 打开资源选择器]**。

   您还只需复制并粘贴资产URL即可。

1. 浏览AEM资源并选择要添加到内容中的资源。

## 发送时间个性化

借助WYSIWYG创作实例参数化dm分层模板以个性化内容
使用AJO个性化编辑器映射配置文件/上下文属性

1. 将&#x200B;**[!UICONTROL HTML组件]**&#x200B;拖放到您的内容中。

1. 选择&#x200B;**[!UICONTROL 显示源代码]**。

1. 从&#x200B;**[!UICONTROL 编辑HTML]**&#x200B;菜单中，访问&#x200B;**[!UICONTROL Assets]**，然后&#x200B;**[!UICONTROL 打开资源选择器]**。

   您还只需复制并粘贴资产URL即可。

1. 浏览AEM资源并选择要添加到内容中的资源。