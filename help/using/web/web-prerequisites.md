---
title: Web 渠道先决条件
description: 要在Journey Optimizer用户界面中访问和创作网页，请遵循此页面上的先决条件
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 6cb4f8ab-77ad-44a2-b2bf-a97f87b8f1db
source-git-commit: 65a33d6836c43564ef7c93660a8076677ea5cba8
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 13%

---

# 先决条件和护栏 {#web-prerequisites}

能够访问和创作中的网页 [!DNL Journey Optimizer] 用户界面，请遵循以下先决条件：

* 要向网站添加修改，您需要具有特定的实施。 [了解详情](#implementation-prerequisites)

* 要访问 [!DNL Journey Optimizer] Web Designer中，您必须安装特定的Google Chrome浏览器扩展。 [了解详情](#visual-authoring-prerequesites)

* 要正确交付Web体验，请确保您详细定义了Adobe Experience Platform设置 [此处](#delivery-prerequisites).

## 注意事项

这当前位于 [!DNL Journey Optimizer] 中，您只能使用&#x200B;**营销活动**&#x200B;创建 Web 体验。[了解详情](../campaigns/create-campaign.md#configure)


[!DNL Journey Optimizer] Web营销活动的目标是其他渠道中以前未参与过的新用户档案。 这将增加您的可参与用户档案总数，如果超出您购买的可参与用户档案的合同数量，则可能会带来成本影响。 每个包的许可证量度都列在 [Journey Optimizer产品描述](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html) 页面。

## 实施先决条件 {#implementation-prerequisites}

当前支持两种类型的实施，以便能够在Web资产上创作和交付Web渠道营销活动：

* 仅限客户端 — 要向网站添加修改，您需要实施 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"} 网站上的。

* 混合模式 — 您可以使用 [AEP Edge Network服务器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=zh-Hans){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>当前不支持仅服务器端实施。

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## 可视化创作先决条件 {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

要能够在中可靠地打开、创作和预览网页，请执行以下操作 [!DNL Journey Optimizer] Web设计器，您必须拥有 [Adobe Experience Cloud可视化编辑帮助程序](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 浏览器扩展已安装在您的Web浏览器上。

>[!CAUTION]
>
>Google Chrome和Microsoft Edge是目前唯一支持在中创作网页的浏览器 [!DNL Journey Optimizer].

### 安装可视化编辑帮助程序扩展 {#install-visual-editing-helper}

要下载并安装可视化编辑帮助程序浏览器扩展，请执行以下步骤。

1. 在浏览器(Google Chrome或Microsoft Edge)中打开新选项卡。

1. 转到 [Google Chrome网络商店](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. 如果您使用的是Microsoft Edge，请选择 **[!UICONTROL 允许来自其他商店的扩展]** 在顶部横幅上。 这将允许您从Chrome网络商店向Microsoft Edge添加扩展。

1. 搜索并导航到 [Adobe Experience Cloud可视化编辑帮助程序](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 浏览器扩展。

1. 点击&#x200B;**[!UICONTROL 添加至 Chrome]** > **[!UICONTROL 添加扩展。]**

   >[!NOTE]
   >
   >如果您使用的是Microsoft Edge，那么即使按钮带有标签，扩展也会添加到Edge **[!UICONTROL 添加到Chrome]**.

1. 确保在浏览器的工具栏中正确启用了可视化编辑帮助程序浏览器扩展。

   ![](assets/web-visual-editing-extension-edge.png)

<!--1. Launch [!DNL Journey Optimizer] in a new tab of your browser with the extension installed.

1. Create a web channel campaign in [!DNL Journey Optimizer]. [Learn how](author-web.md#create-web-campaign)

1. Open the [!DNL Journey Optimizer] web designer to start authoring your web experience. [Learn more](author-web.md)-->

现在，在中打开网站时，会自动启用Adobe Experience Cloud可视化编辑帮助程序。 [!DNL Journey Optimizer] Web设计器支持创作。

该扩展没有任何条件设置，并且会自动处理所有设置，包括SameSite Cookie设置。

>[!NOTE]
>
>某些网站可能无法在中可靠打开 [!DNL Journey Optimizer] Web Designer ，原因如下：
>
> * 网站具有严格的安全策略。
> * 网站位于 iframe 中。
> * 外部无法访问客户的 QA 或阶段站点（该站点为内部站点）。


### 网站未加载疑难解答 {#troubleshooting}

使用Adobe时 [!DNL Journey Optimizer] Web Designer如果尝试加载无法加载的网站，则会显示一条消息，建议您安装 [可视化编辑帮助程序浏览器扩展](#install-visual-editing-helper).

如果正确安装了可视化编辑帮助程序浏览器扩展，但网站仍然无法加载或行为异常，潜在的解决方法是，在尝试在中加载该网站之前，在浏览器中打开您的网站并接受Cookie [!DNL Journey Optimizer] Web设计器。

对于身份验证下的页面，如果登录页面加载失败，或者在尝试登录后，您仍未登录：

* 尝试首先在新浏览器选项卡中登录并导航到所需的页面，然后复制URL并尝试在 [!DNL Journey Optimizer] Web设计器。

* 如果您仍然无法在以下位置加载网站： [!DNL Journey Optimizer] Web Designer，请联系Adobe客户关怀部门报告问题，并确保指定失败的URL。

## 投放先决条件 {#delivery-prerequisites}

要正确交付Web体验，必须定义以下设置：

* 在 [Adobe Experience Platform数据收集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html){target="_blank"}，确保您有定义的数据流，例如 **[!UICONTROL Adobe Experience Platform]** 服务，您拥有 **[!UICONTROL 边缘分段]** 和 **[!UICONTROL Adobe Journey Optimizer]** 选项已启用。

   这可确保Adobe Experience Platform Edge正确处理Journey Optimizer入站事件。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=zh-Hans){target="_blank"}

   ![](assets/web-aep-datastream-ajo.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL Adobe Journey Optimizer]** 选项仅可在 **[!UICONTROL 边缘分段]** 选项已启用。

* In [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

   此合并策略的使用者 [!DNL Journey Optimizer] 入站渠道，用于在边缘上正确激活和发布入站营销活动。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hans){target="_blank"}

   ![](assets/web-aep-merge-policy.png)

## 资产品牌域 {#branded-domains-for-assets}

在创作Web体验时，如果您添加来自 [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) 库中，您必须设置用于发布此内容的子域。 [了解详情](web-delegated-subdomains.md)
