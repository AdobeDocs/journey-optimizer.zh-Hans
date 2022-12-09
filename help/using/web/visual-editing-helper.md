---
title: Visual Editing Helper扩展
description: 了解可视化编辑助手Chrome扩展，该扩展允许您在Journey Optimizer中创作和预览网页
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: f4a0ec45-d624-4f80-b888-42e5987cdc4f
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Visual Editing Helper扩展 {#visual-editing-helper}

为了快速创作和预览您的Web体验，借助适用于Google Chrome的Adobe Experience Cloud可视化编辑助手浏览器扩展，您可以在Adobe内可靠地加载网站 [!DNL Journey Optimizer] web设计器。

>[!NOTE]
>
>Web渠道功能目前仅作为测试版提供给选定的用户。

## 安装Visual Editing Helper扩展 {#install-visual-editing-helper}

要获取并安装Visual Editing Helper浏览器扩展，请执行以下步骤。

1. 从Google Chrome Web Store中，导航到 [Adobe Experience Cloud可视化编辑助手](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=&quot;_blank&quot;}浏览器扩展。

1. 单击 **[!UICONTROL Add to Chrome]** > **[!UICONTROL Add Extension]**.

1. 在中创建Web渠道营销活动 [!DNL Journey Optimizer]. [了解如何](author-web.md#create-web-campaign)

1. 打开 [!DNL Journey Optimizer] web设计器来开始创作Web体验。 [了解更多](author-web.md)

1. 通过单击相应的图标，确保在Chrome浏览器的工具栏中启用了可视化编辑助手浏览器扩展。

   ![](assets/web-visual-editing-extension.png)

现在，当在 [!DNL Journey Optimizer] web设计器来实现创作。

该扩展没有任何条件设置，并会自动处理所有设置，包括SameSite Cookie设置。

>[!NOTE]
>
>某些网站可能无法在 [!DNL Journey Optimizer] web designer的原因如下：
>
> * 网站具有严格的安全策略。
> * 网站位于iframe中。
> * 客户的QA或阶段网站不适用于外部环境（网站是内部网站）。


## 疑难解答

使用Adobe时 [!DNL Journey Optimizer] web设计器中，如果尝试加载无法加载的网站，则会显示一条消息，建议您安装 [Visual Editing Helper浏览器扩展](#install-visual-editing-helper).

如果尚未在网站上实施Adobe Experience Platform Web SDK，则Web设计器中会显示一条消息，建议您安装可视化编辑助手浏览器扩展并实施 [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target=&quot;_blank&quot;}。

如果网站加载失败或行为意外失败，则可能存在的修复是：在尝试在Adobe中加载网站之前，接受浏览器中您网站上的Cookie [!DNL Journey Optimizer].

对于受身份验证的页面，如果登录页面加载失败，或者如果尝试登录后您仍未登录，请尝试先在浏览器的其他选项卡中登录，然后在Adobe中加载网站 [!DNL Journey Optimizer] web设计器。
