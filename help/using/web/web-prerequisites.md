---
title: Web渠道先决条件
description: 要在Journey Optimizer用户界面中访问和创作网页，请遵循本页的先决条件
feature: Web Channel
topic: Content Management
role: User
level: Beginner
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 11%

---

# Web渠道先决条件 {#web-prerequisites}

在 [!DNL Journey Optimizer] 用户界面中，请遵循以下先决条件：

* 要向网站添加修改，您需要具有特定实施。 [了解详情](#implementation-prerequisites)

* 访问 [!DNL Journey Optimizer] web designer中，您必须安装特定的Google Chrome浏览器扩展。 [了解详情](#visual-authoring-prerequesites)

* 为了正确提供Web体验，请确保详细定义Adobe Experience Platform设置 [此处](#delivery-prerequisites).

## 实施先决条件 {#implementation-prerequisites}

目前支持两种类型的实施，以便能够在您的Web属性上创作和交付Web渠道营销活动：

* 仅限客户端 — 要向网站添加修改，您需要实施 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"} 在您的网站上。

* 混合模式 — 您可以使用 [AEP Edge Network Server API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=zh-Hans){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>当前不支持仅服务器端实施。

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## 可视化创作先决条件 {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

要能够可靠地在 [!DNL Journey Optimizer] Web设计器，您必须 [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 浏览器扩展。

>[!CAUTION]
>
>Google Chrome和Microsoft Edge当前是唯一支持在中创作网页的浏览器 [!DNL Journey Optimizer].

### 安装Visual Editing Helper扩展 {#install-visual-editing-helper}

要下载并安装Visual Editing Helper浏览器扩展，请执行以下步骤。

1. 在浏览器中打开一个新选项卡(Google Chrome或Microsoft Edge)。

1. 转到 [Google Chrome网上商店](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. 如果您使用的是Microsoft Edge，请选择 **[!UICONTROL 允许来自其他商店的扩展]** 在顶部横幅上。 这将允许您将扩展从Chrome Web Store添加到Microsoft Edge。

1. 搜索并导航到 [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 浏览器扩展。

1. 点击&#x200B;**[!UICONTROL 添加至 Chrome]** > **[!UICONTROL 添加扩展。]**

   >[!NOTE]
   >
   >如果您使用的是Microsoft Edge，则即使按钮已标记，也会将扩展添加到Edge **[!UICONTROL 添加到Chrome]**.

1. 确保在浏览器的工具栏中正确启用可视化编辑助手浏览器扩展。

   ![](assets/web-visual-editing-extension-edge.png)

<!--1. Launch [!DNL Journey Optimizer] in a new tab of your browser with the extension installed.

1. Create a web channel campaign in [!DNL Journey Optimizer]. [Learn how](author-web.md#create-web-campaign)

1. Open the [!DNL Journey Optimizer] web designer to start authoring your web experience. [Learn more](author-web.md)-->

现在，当在 [!DNL Journey Optimizer] web设计器来实现创作。

该扩展没有任何条件设置，并会自动处理所有设置，包括SameSite Cookie设置。

>[!NOTE]
>
>某些网站可能无法在 [!DNL Journey Optimizer] web designer的原因如下：
>
> * 网站具有严格的安全策略。
> * 网站位于 iframe 中。
> * 外部无法访问客户的 QA 或阶段站点（该站点为内部站点）。


### 网站加载故障诊断 {#troubleshooting}

使用Adobe时 [!DNL Journey Optimizer] web设计器中，如果尝试加载无法加载的网站，则会显示一条消息，建议您安装 [Visual Editing Helper浏览器扩展](#install-visual-editing-helper).

如果Visual Editing Helper浏览器扩展安装正确，但网站仍无法加载或行为异常，则可能的解决方法是在浏览器中打开您的网站，并接受Cookie，然后再尝试在中加载它 [!DNL Journey Optimizer] web设计器。

对于处于身份验证下的页面，如果登录页面加载失败，或者如果尝试登录后仍未登录：

* 尝试先在新的浏览器选项卡中登录，然后导航到所需的页面，然后复制URL，然后尝试在 [!DNL Journey Optimizer] web设计器。

* 如果仍然无法在 [!DNL Journey Optimizer] Web设计人员，请联系Adobe客户关怀团队以报告问题，并确保指定失败的URL。

## 投放先决条件 {#delivery-prerequisites}

要正确交付Web体验，必须定义以下设置：

* 在 [Adobe Experience Platform数据收集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html){target="_blank"}，请确保在 **[!UICONTROL Adobe Experience Platform]** 你们都有 **[!UICONTROL 边缘分割]** 和 **[!UICONTROL Adobe Journey Optimizer]** 选项。

   这可确保Journey Optimizer集客事件由Adobe Experience Platform Edge正确处理。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=zh-Hans){target="_blank"}

   ![](assets/web-aep-datastream-ajo.png)

   >[!NOTE]
   >
   >的 **[!UICONTROL Adobe Journey Optimizer]** 选项仅在 **[!UICONTROL 边缘分割]** 选项。

* 在 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

   此合并策略由 [!DNL Journey Optimizer] 入站渠道，以在边缘上正确激活和发布入站营销活动。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html){target="_blank"}

   ![](assets/web-aep-merge-policy.png)

<!--
Branded domains for assets

When authoring web experiences, if you add content coming from the [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) library, you  must set up the subdomain that will be used to publish this content. [Learn more](web-delegated-subdomains.md)-->



