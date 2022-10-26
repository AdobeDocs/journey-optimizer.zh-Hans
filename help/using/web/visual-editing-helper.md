---
title: 可视化编辑帮助程序扩展
description: 了解可视化编辑助手Chrome扩展，该扩展允许您在Journey Optimizer中创作和预览网页
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 14%

---

# 可视化编辑帮助程序扩展 {#visual-editing-helper}

为了快速创作和预览您的Web体验，适用于Google Chrome的Adobe Experience Cloud可视化编辑助手浏览器扩展允许您在Adobe内可靠地加载网站 [!DNL Journey Optimizer] web设计器。

>[!NOTE]
>
>Web渠道功能目前仅作为测试版提供给选定的用户。

## 安装Visual Editing Helper扩展 {#install-visual-editing-helper}

要获取并安装Visual Editing Helper浏览器扩展，请执行以下步骤。

1. 从Google Chrome Web Store中，导航到 [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=&quot;_blank&quot;}浏览器扩展。

1. 点击&#x200B;**[!UICONTROL 添加至 Chrome]** > **[!UICONTROL 添加扩展。]**

1. 在中创建Web渠道营销活动 [!DNL Journey Optimizer]. [了解如何](author-web.md#create-web-campaign)

1. 打开 [!DNL Journey Optimizer] web设计器来开始创作Web体验。 [了解详情](author-web.md)

1. 通过单击相应的图标，确保在Chrome浏览器的工具栏中启用了可视化编辑助手浏览器扩展。

   ![](assets/web-visual-editing-extension.png)

现在，当在 [!DNL Journey Optimizer] web设计器来实现创作。

该扩展没有任何条件设置，并会自动处理所有设置，包括SameSite Cookie设置。

>[!NOTE]
>
>某些网站可能无法在 [!DNL Journey Optimizer] web designer的原因如下：
>
> * 网站具有严格的安全策略。
> * 网站位于 iframe 中。
> * 外部无法访问客户的 QA 或阶段站点（该站点为内部站点）。


## 故障排除

使用Adobe时 [!DNL Journey Optimizer] web设计器中，如果尝试加载无法加载的网站，则会显示一条消息，建议您安装 [Visual Editing Helper浏览器扩展](#install-visual-editing-helper).

如果尚未在网站上实施Adobe Experience Platform Web SDK，则Web设计器中会显示一条消息，建议您安装可视化编辑助手浏览器扩展并实施 [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target=&quot;_blank&quot;}。

如果网站加载失败或行为异常，可能的修复是：在尝试以Adobe方式加载网站之前，接受浏览器中您网站上的Cookie [!DNL Journey Optimizer].

对于处于身份验证下的页面，如果登录页面加载失败，或者如果尝试登录后您仍未登录，请尝试先在浏览器的其他选项卡中登录，然后在Adobe中加载网站 [!DNL Journey Optimizer] web设计器。
