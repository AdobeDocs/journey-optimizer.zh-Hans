---
title: Web 渠道先决条件
description: 要在Journey Optimizer用户界面中访问和创作网页，请遵循此页面上的先决条件
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 9509fd67-6d12-4440-aad8-59690936be97
source-git-commit: c5308cfdb237fcf563886db1dfca257d23bb4449
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 3%

---

# 先决条件和护栏 {#web-prerequisites}

要在[!DNL Journey Optimizer]用户界面中访问和创作网页，请遵循以下先决条件：

* 要向网站添加修改，您需要具有特定的实施。 [了解详情](#implementation-prerequisites)

* 要访问[!DNL Journey Optimizer] Web设计器，您必须安装特定的Google Chrome浏览器扩展。 [了解详情](#visual-authoring-prerequisites)

* 为了正确交付Web体验，请确保在[此处](#delivery-prerequisites)定义详细的Adobe Experience Platform设置。

>[!IMPORTANT]
>
>[!DNL Journey Optimizer] Web 营销活动针对的是以前在其他渠道上没有联系过的新用户档案。这会增加您的可参与用户档案总数，如果超出您购买的可参与用户档案的合同数量，则可能会带来成本影响。 [Journey Optimizer产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}页面上列出了每个包的许可证指标。 您可以在[许可证使用情况仪表板](../audience/license-usage.md)中检查可参与的配置文件数。
>

## 实施先决条件 {#implementation-prerequisites}

支持两种类型的实施，以便能够在Web资产上创作和交付Web渠道营销活动：

* 仅客户端 — 若要向网站添加修改，需要在网站上实施[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"}。

  >[!NOTE]
  >
  >确保您的[Adobe Experience Platform Web SDK版本](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/release-notes){target="_blank"}为2.16或更高版本。

* 混合模式 — 您可以使用[AEPEdge Network服务器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"}来请求在服务器端进行个性化；响应将提供给Adobe Experience Platform Web SDK以渲染客户端所做的修改。 请参阅Adobe Experience Platform [Edge Network服务器API文档](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html){target="_blank"}以了解详情。 您可以在[此博客文章](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}中找到有关混合模式的详细信息并查看一些实施示例。

>[!NOTE]
>
>Web渠道当前不支持仅服务器端实施。 如果您的网页只有服务器端实施，则可以改用[基于代码的体验渠道](../code-based/get-started-code-based.md)。

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## 可视化创作先决条件 {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

若要能够可靠地在[!DNL Journey Optimizer] Web设计器中打开、创作和预览网页，必须在Web浏览器上安装[Adobe Experience Cloud可视化编辑帮助程序](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"}浏览器扩展。

>[!CAUTION]
>
>Google Chrome和Microsoft Edge目前是唯一支持[!DNL Journey Optimizer]中创作网页的浏览器。

### 安装可视化编辑帮助程序扩展 {#install-visual-editing-helper}

要下载并安装可视化编辑帮助程序浏览器扩展，请执行以下步骤。

1. 在浏览器(Google Chrome或Microsoft Edge)中打开新选项卡。

1. 转到[Google Chrome网上商店](https://chrome.google.com/webstore/category/extensions){target="_blank"}。

1. 如果您使用的是Microsoft Edge，请在顶部横幅上选择&#x200B;**[!UICONTROL 允许来自其他商店的扩展]**。 这将允许您从Chrome网络商店向Microsoft Edge添加扩展。

1. 搜索并导航到[Adobe Experience Cloud可视化编辑帮助程序](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"}浏览器扩展。

1. 单击&#x200B;**[!UICONTROL 添加到Chrome]** > **[!UICONTROL 添加扩展]**。

   >[!NOTE]
   >
   >如果您使用的是Microsoft Edge，这将将该扩展添加到Edge，即使按钮标记为&#x200B;**[!UICONTROL 添加到Chrome]**。

1. 确保在浏览器的工具栏中正确启用可视化编辑帮助程序浏览器扩展。

   ![](assets/web-visual-editing-extension-edge.png)

现在，当在[!DNL Journey Optimizer] [Web设计器](edit-web-content.md#work-with-web-designer)中打开网站以进行创作时，会自动启用Adobe Experience Cloud可视化编辑帮助程序。

该扩展没有任何条件设置，并且会自动处理所有设置，包括SameSite Cookie设置。

>[!NOTE]
>
>由于以下原因之一，某些网站可能无法在[!DNL Journey Optimizer] Web设计器中可靠地打开：
>
> * 网站具有严格的安全策略。
> * 网站位于iframe中。
> * 外部无法访问客户的QA或暂存站点（该站点为内部站点）。

### 网站未加载疑难解答 {#troubleshooting}

在使用Adobe[!DNL Journey Optimizer] Web设计器时，如果尝试加载无法加载的网站，则会显示一条消息，建议您安装[可视化编辑帮助程序浏览器扩展](#install-visual-editing-helper)。

1. 确保已正确安装可视化编辑帮助程序浏览器扩展。

1. 如果网站仍出现意外行为，请确保浏览器中允许第三方Cookie，否则网页无法在[!DNL Journey Optimizer] Web设计器内加载。

对于处于身份验证下的页面，如果登录页面加载失败，或者在尝试登录后您仍未登录：

1. 尝试首先在新浏览器选项卡中登录并导航到所需的页面，然后复制URL并尝试在[!DNL Journey Optimizer] Web设计器中打开它。

2. 如果您仍然无法在[!DNL Journey Optimizer] Web设计器中加载您的网站，请联系Adobe客户关怀部门以报告此问题，并确保指定失败的URL。

## 投放先决条件 {#delivery-prerequisites}

要正确交付Web体验，必须定义以下设置：

* 在[Adobe Experience Platform数据收集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hans){target="_blank"}中，确保您具有定义的数据流，例如，在&#x200B;**[!UICONTROL Adobe Experience Platform]**&#x200B;服务下启用了&#x200B;**[!UICONTROL Adobe Journey Optimizer]**&#x200B;选项。

  这可确保Adobe Experience Platform Edge正确处理Journey Optimizer入站事件。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* 在[Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}中，确保您有一个启用了&#x200B;**[!UICONTROL Edge上的Active-On合并策略]**&#x200B;选项的合并策略。 为此，请在&#x200B;**[!UICONTROL 客户]** > **[!UICONTROL 配置文件]** > **[!UICONTROL 合并策略]**&#x200B;策略菜单下选择Experience Platform。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  [!DNL Journey Optimizer]入站渠道使用此合并策略在边缘上正确激活和发布入站营销活动。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hans){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

* 要对Journey Optimizer Web体验的交付进行故障诊断，您可以使用&#x200B;**Edge Delivery保证**&#x200B;中的&#x200B;**Adobe Experience Platform**&#x200B;视图。 利用此插件，您可以详细检查请求调用，验证预期的边缘调用是否按预期发生，并检查配置文件数据，包括身份映射、区段成员资格和同意设置。 此外，您还可以查看请求符合条件的活动，并识别未符合条件的活动。

  使用&#x200B;**Edge Delivery**&#x200B;插件可帮助您获得所需的见解，以便有效了解入站实施并排除其故障。

  [了解有关Edge Delivery视图的更多信息](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/assurance/view/edge-delivery)

## 报告先决条件 {#experiment-prerequisites}

要启用Web渠道报表，您需要确保您的Web实施[数据流](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"}中使用的[数据集](../data/get-started-datasets.md)也包含在您的报表配置中。

换言之，在配置报表时，如果添加的数据集在Web数据流中不存在，则Web数据将不会显示在报表中。

在[本节](../reports/reporting-configuration.md#add-datasets)中了解如何添加用于报告的数据集。

>[!NOTE]
>
>该数据集由[!DNL Journey Optimizer]报表系统以只读方式使用，不影响数据收集或数据摄取。

如果您&#x200B;**不是**，正在为数据集架构使用以下预定义的[字段组](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh_Hans#field-group){target="_blank"}： `AEP Web SDK ExperienceEvent`和`Consumer Experience Event`（如[此页面](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}中定义），请确保添加以下字段组： `Experience Event - Proposition Interactions`、`Application Details`、`Commerce Details`和`Web Details`。 [!DNL Journey Optimizer]内容试验报告需要这些项，因为它们正在跟踪每个配置文件参与哪些试验和处理。

[了解有关报告配置的更多信息](../reports/reporting-configuration.md)

>[!NOTE]
>
>添加这些字段组不会影响正常数据收集。 它仅适用于正在运行试验的页面，而所有其他跟踪保持不变。

## 资产的品牌域 {#branded-domains-for-assets}

在创作Web体验时，如果添加来自[Adobe Experience Manager Assets](../content-management/assets.md)库的内容，则必须设置将用于发布此内容的子域。 [了解详情](web-delegated-subdomains.md)
