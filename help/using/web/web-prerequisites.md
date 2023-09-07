---
title: Web 渠道先决条件
description: 要在Journey Optimizer用户界面中访问和创作网页，请遵循此页面上的先决条件
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 6cb4f8ab-77ad-44a2-b2bf-a97f87b8f1db
source-git-commit: cfa797146c4f6f87a55e72393f45c271480cf7f5
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 11%

---

# 先决条件和护栏 {#web-prerequisites}

要能够访问和创作中的网页，请执行以下操作： [!DNL Journey Optimizer] 用户界面中，请遵循以下先决条件：

* 要向网站添加修改，您需要具有特定的实施。 [了解详情](#implementation-prerequisites)

* 要访问 [!DNL Journey Optimizer] Web Designer中，您必须安装特定的Google Chrome浏览器扩展。 [了解详情](#visual-authoring-prerequesites)

* 为了正确交付Web体验，请确保您详细定义了Adobe Experience Platform设置 [此处](#delivery-prerequisites).

## 警告说明 {#caution-notes-web}

* 当前位置 [!DNL Journey Optimizer] 您只能在中创建Web体验 **营销活动**. [了解详情](../campaigns/create-campaign.md#configure)

* [!DNL Journey Optimizer] Web营销活动针对其他渠道中以前未参与过的新用户档案。 这将增加您的可参与用户档案总数，如果超出您购买的可参与用户档案的合同数量，则可能会带来成本影响。 每个包的许可证量度都列在 [Journey Optimizer产品描述](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html) 页面。


>[!AVAILABILITY]
>
>目前，Web渠道不适用于已购买AdobeHealthcare Shield附加产品的组织。
>

## 实施先决条件 {#implementation-prerequisites}

当前支持两种类型的实施，以便能够在Web资产上创作和交付Web渠道营销活动：

* 仅限客户端 — 要向网站添加修改，您需要实施 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"} 您的网站上的。

  >[!NOTE]
  >
  >确保您的AEP Web SDK版本为2.16或更高版本。

* 混合模式 — 您可以使用 [AEP Edge Network服务器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=zh-Hans){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>当前不支持仅服务器端实施。

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## 可视化创作先决条件 {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

要能够在中可靠地打开、创作和预览网页，请执行以下操作 [!DNL Journey Optimizer] Web设计器，您必须具有 [Adobe Experience Cloud可视化编辑帮助程序](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 浏览器扩展已安装在您的Web浏览器上。

>[!CAUTION]
>
>Google Chrome和Microsoft Edge是目前唯一支持在中创作网页的浏览器 [!DNL Journey Optimizer].

### 安装可视化编辑帮助程序扩展 {#install-visual-editing-helper}

要下载并安装可视化编辑帮助程序浏览器扩展，请执行以下步骤。

1. 在浏览器(Google Chrome或Microsoft Edge)中打开新选项卡。

1. 转到 [Google Chrome网络商店](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. 如果您使用的是Microsoft Edge，请选择 **[!UICONTROL 允许来自其他商店的扩展]** 在顶部的横幅上。 这将允许您从Chrome网络商店向Microsoft Edge添加扩展。

1. 搜索并导航到 [Adobe Experience Cloud可视化编辑帮助程序](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 浏览器扩展。

1. 点击&#x200B;**[!UICONTROL 添加至 Chrome]** > **[!UICONTROL 添加扩展。]**

   >[!NOTE]
   >
   >如果您使用的是Microsoft Edge，那么即使按钮带有标签，该操作也会将扩展添加到Edge **[!UICONTROL 添加到Chrome]**.

1. 确保在浏览器的工具栏中正确启用可视化编辑帮助程序浏览器扩展。

   ![](assets/web-visual-editing-extension-edge.png)

<!--1. Launch [!DNL Journey Optimizer] in a new tab of your browser with the extension installed.

1. Create a web channel campaign in [!DNL Journey Optimizer]. [Learn how](author-web.md#create-web-campaign)

1. Open the [!DNL Journey Optimizer] web designer to start authoring your web experience. [Learn more](author-web.md)-->

现在，在中打开网站时，会自动启用Adobe Experience Cloud可视化编辑帮助程序。 [!DNL Journey Optimizer] Web设计器支持创作。

该扩展没有任何条件设置，并且会自动处理所有设置，包括SameSite Cookie设置。

>[!NOTE]
>
>某些网站可能无法在中可靠地打开 [!DNL Journey Optimizer] Web设计人员出于以下原因之一：
>
> * 网站具有严格的安全策略。
> * 网站位于 iframe 中。
> * 外部无法访问客户的 QA 或阶段站点（该站点为内部站点）。

### 网站未加载疑难解答 {#troubleshooting}

使用Adobe时 [!DNL Journey Optimizer] web designer如果尝试加载无法加载的网站，则会显示一条消息，建议您安装 [可视化编辑帮助程序浏览器扩展](#install-visual-editing-helper).

1. 确保已正确安装可视化编辑帮助程序浏览器扩展。

1. 如果网站仍出现意外行为，请确保您的浏览器中允许第三方Cookie，否则网页无法在 [!DNL Journey Optimizer] Web设计器。

对于处于身份验证下的页面，如果登录页面加载失败，或者在尝试登录后您仍未登录：

1. 尝试先在新浏览器选项卡中登录并导航到所需的页面，然后复制URL并尝试在 [!DNL Journey Optimizer] Web设计器。

2. 如果您仍然无法在以下位置加载网站： [!DNL Journey Optimizer] Web设计人员联系Adobe客户关怀部门以报告此问题，并确保指定失败的URL。

## 投放先决条件 {#delivery-prerequisites}

要正确交付Web体验，必须定义以下设置：

* 在 [Adobe Experience Platform数据收集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hans){target="_blank"}，确保您有定义的数据流，例如 **[!UICONTROL Adobe Experience Platform]** 服务 **[!UICONTROL Adobe Journey Optimizer]** 选项已启用。

  这可确保Adobe Experience Platform Edge正确处理Journey Optimizer入站事件。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=zh-Hans){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* 在 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  此合并策略的使用者为 [!DNL Journey Optimizer] 入站渠道，用于在边缘上正确激活和发布入站营销活动。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hans){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

## 内容试验先决条件 {#experiment-prerequisites}

要为Web渠道启用内容实验，您需要确保 [数据集](../data/get-started-datasets.md) 在您的Web实施中使用 [数据流](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=zh-Hans){target="_blank"} 也包含在您的报表配置中。

换句话说，在配置试验报告时，如果添加的数据集不在Web数据流中，则Web数据将不会显示在内容试验报告中。

了解如何在中为内容实验报告添加数据集 [本节](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>数据集由 [!DNL Journey Optimizer] 并且不影响数据收集或数据摄取。

如果您是 **非** 使用以下预定义的 [字段组](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh_Hans#field-group){target="_blank"} for your dataset schema: `AEP Web SDK ExperienceEvent` and `Consumer Experience Event` (as defined in [this page](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"})，确保添加以下字段组： `Experience Event - Proposition Interactions`， `Application Details`， `Commerce Details`、和 `Web Details`. 这些是必需的 [!DNL Journey Optimizer] 内容试验报告，并跟踪每个用户档案参与哪些试验和处理。

>[!NOTE]
>
>添加这些字段组不会影响正常数据收集。 它仅适用于正在运行试验的页面，而所有其他跟踪保持不变。

## 资产的品牌域 {#branded-domains-for-assets}

在创作Web体验时，如果您添加来自 [Adobe Experience Manager Assets Essentials](../content-management/assets-essentials.md) 库中，您必须设置用于发布此内容的子域。 [了解详情](web-delegated-subdomains.md)
