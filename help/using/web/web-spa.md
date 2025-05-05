---
title: 创作单页应用程序
description: 了解如何在Journey Optimizer中创作SPA并将修改应用于不同的视图
feature: Web Channel
topic: Content Management
role: User
level: Intermediate
exl-id: b33e4bca-d2e9-4610-9f04-008d47f686d0
source-git-commit: 4b822eb45857556359ba9444e9bf7379608f1dff
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 16%

---

# 创作单页应用程序 {#web-author-spas}

## 关于视图 {#about-views}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications_views"
>title="将更改应用于所选视图"
>abstract="更改将仅应用于所选视图。可使用&#x200B;**浏览**&#x200B;模式发现视图并导航到这些视图。找不到您要找的视图？"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans" text="了解详情"

现在可以在Web设计器可视编辑器中创作&#x200B;**单页应用程序** (SPA)。 这允许您选择要将网页修改应用于的特定&#x200B;**视图**。

[在此视频中了解如何创作单页面应用程序](#video)

视图可定义为整个网站或网站上的一组可视化元素，例如主页、整个产品网站或所有结账页面上的投放首选项框架。

在Adobe Experience Platform Web SDK实施中定义视图需要一次性开发人员设置。 这使您能够在SPA上创建并运行Adobe Journey Optimizer Web营销活动。

## 在Web SDK实施中定义视图 {#define-views}

可以在Adobe[!DNL Journey Optimizer]中利用XDM视图，使营销人员能够通过Web可视化编辑器在SPA上运行Web个性化和实验营销活动。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html?lang=zh-Hans){target="_blank"}

若要能够在[!DNL Journey Optimizer]用户界面中访问和创作视图，请确保按照[本节](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html?lang=zh-Hans#implement-xdm-views){target="_blank"}中列出的步骤操作。

## 在Web设计器中发现视图 {#discover-views}

在Adobe Experience Platform Web SDK实施中完成SPA设置后，您需要浏览要应用修改的网站的所有视图。 请按照以下步骤操作。

1. [创建Web历程或营销活动](create-web.md)并访问[Web设计器](web-visual-editor.md)。

   您当前所在的视图将显示在左上方。

   ![](assets/web-designer-view-home.png)

1. 切换到&#x200B;**[!UICONTROL 浏览]**&#x200B;模式。 [了解详情](web-visual-editor.md#browse-mode)

   ![](assets/web-designer-view-browse.png)

1. 在网站的不同页面之间导航以发现所有页面。 当您浏览其他页面时，顶部显示的视图名称会发生更改。

   ![](assets/web-designer-other-view.png)

## 将修改应用于其他视图 {#apply-modifications-views}

在特定视图中添加修改后，可将其应用于其他选定视图。 请按照以下步骤操作。

>[!CAUTION]
>
>如果您尚未使用&#x200B;**[!UICONTROL 浏览]**&#x200B;模式发现视图，则无法选择它们以应用您的修改。 [了解详情](#discover-views)

1. 选择&#x200B;**[!UICONTROL 修改]**&#x200B;图标以在左侧显示相应的窗格。

   ![](assets/web-designer-view-modifications-pane.png)

1. 选择任何修改并单击其旁边的&#x200B;**[!UICONTROL 更多操作]**&#x200B;按钮。 选择&#x200B;**[!UICONTROL 应用到更多视图]**。

   ![](assets/web-designer-modifications-more-actions.png)

1. 选择要将更改应用到其中的视图。

   ![](assets/web-designer-modifications-apply-to.png)

1. 单击&#x200B;**[!UICONTROL 应用]**。

1. 切换到&#x200B;**[!UICONTROL 浏览]**&#x200B;模式以检查修改是否应用于所需页面。

   ![](assets/web-designer-modifications-applied-view.png)

## 操作方法视频{#video}

以下视频介绍了如何：

* 使用&#x200B;**[!UICONTROL 浏览]**&#x200B;模式发现SPA视图
* 在当前视图上进行创作
* 将网站修改应用于发现的多个视图或所有视图
* 对修改执行批量操作

>[!VIDEO](https://video.tv.adobe.com/v/3446895/?quality=12&learn=on&captions=chi_hans)
