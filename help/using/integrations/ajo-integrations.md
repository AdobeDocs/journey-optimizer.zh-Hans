---
solution: Journey Optimizer
product: journey optimizer
title: 与其他解决方案集成
description: 详细了解如何将 Journey Optimizer 与其他解决方案集成
feature: Integrations
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: dbb1a4d649f29b763121c7856cecca16dcd2864f
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 68%

---

# 与其他解决方案集成 {#integration}

借助 Adobe Journey Optimizer，您可以轻松管理、保留此类数据，并将其导出到技术堆栈中所包含的平台或系统。这些集成可帮助您解决特定用例，并扩展 Adobe Journey Optimizer 的功能范围。

>[!NOTE]
>
> Adobe Journey Optimizer构建于Adobe Experience Platform之上，原生连接到[Adobe实时客户个人资料](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}。 此内置数据源已预配置，旨在检索和使用 Real-time Customer Profile 中的数据（例如，检查进入历程的人员是否为客户）。它允许您使用配置文件数据。 [了解详情](../datasource/adobe-experience-platform-data-source.md)。


## 了解 Adobe Customer Journey Analytics {#integration-cja}

您可以使用 Customer Journey Analytics 对 Journey Optimizer 生成的数据执行高级分析。

Journey Optimizer将数据存储在Adobe Experience Platform中，借助Customer Journey Analytics，可通过自动报告分发和自定义数据可视化，全面了解您的所有历程、营销活动和选件。

在 Journey Optimizer 中创建您的历程后，Customer Journey Analytics 可以从平台中摄取数据以生成报告，了解客户与您的历程每次交互的影响。

详细了解 [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md)。

## Adobe Analytics {#integration-aa}

您可以利用已在捕获并流入到 Adobe Experience Platform 中的所有 Adobe Analytics 行为事件数据，从而触发实时历程并将客户的体验自动化。此数据还可用于创建可使用 Journey Optimizer 接触的受众。

详细了解 [Journey Optimizer + Analytics](../event/about-analytics.md)。

## Adobe Experience Manager {#integration-aem}

作为Adobe Experience Manager用户，您可以将工作流与Adobe Journey Optimizer结合使用。 以下列出了可用的用例：


>[!BEGINTABS]

>[!TAB AEM Assets]

利用 **[!DNL Adobe Experience Manager Assets]** 整合营销和创意工作流。与&#x200B;**[!DNL Adobe Journey Optimizer]**&#x200B;本机集成，访问&#x200B;**[!DNL Assets Essentials]**&#x200B;或&#x200B;**[!DNL Assets as a Cloud Service]**&#x200B;以存储、管理、发现和分发数字资源。 提供了单一集中式资源存储库，您可以使用它来填充消息。

[![了解详情](../assets/do-not-localize/learn-more-button.svg)](../integrations/assets.md)

<!--
>[!TAB AEM Templates]

With Adobe Journey Optimizer, you can create custom-tailored messages through Adobe Experience Manager sites. Start by designing your templates using Adobe Experience Manager's content sources, then send them to Adobe Journey Optimizer. Once shared, these templates can be accessed in Adobe Journey Optimizer's Email Designer, simplifying the process of crafting and sending messages to your desired audience.

[![learn more](../assets/do-not-localize/learn-more-button.svg)](../integrations/aem-templates.md)

-->

>[!TAB AEM片段]

通过将Adobe Experience Manager与Adobe Journey Optimizer集成，您现在可以将AEM内容片段无缝地合并到Journey Optimizer电子邮件内容中。 这种简单的连接方式可简化访问和利用 AEM 内容的流程，从而能够创建个性化的动态营销活动和历程。

[![了解详情](../assets/do-not-localize/learn-more-button.svg)](../integrations/aem-fragments.md)

>[!TAB Dynamic Media]

使用Journey Optimizer Asset选择器可在Journey Optimizer中选择并使用已批准的Dynamic Media演绎版。 对Adobe Experience Manager中的资源所做的更改会立即反映在Journey Optimizer内容中，从而确保始终使用最新版本，而无需手动更新。

[![了解详情](../assets/do-not-localize/learn-more-button.svg)](../integrations/aem-dynamic.md)


>[!ENDTABS]



## Adobe Stock {#integration-stock}

[!DNL Adobe Stock] 和 [!DNL Adobe Journey Optimizer] 电子邮件设计器集成增效工具可帮助客户在创作消息时轻松进行导航、许可并保存图像。

了解 [Journey Optimizer + Stock](../integrations/stock.md) 的更多信息。

## Adobe Express {#express}

借助 Adobe Journey Optimizer 中的 Adobe Express 集成，您可以在创建内容时轻松访问 Adobe Express 的功能强大的编辑工具。通过这种集成，您可以调整图像大小、移除背景、裁剪视觉元素并将资源转换为 JPEG 或 PNG，而无需在解决方案之间切换。

了解有关[Journey Optimizer + Adobe Express](../integrations/express.md)的更多信息。

## GenStudio for Performance Marketing

Adobe GenStudio for Performance Marketing是一个创作、人工智能优先的应用程序，它允许营销团队创建自己的广告和电子邮件，以推动有效且个性化的营销活动，从而遵守您的品牌标准并遵守您的企业策略。 通过利用Adobe AI技术，它提供了一套全面的工具，可简化内容创建和管理过程，以便创意人员可以专注于创新。

了解有关[Journey Optimizer + GenStudio for Performance Marketing](../integrations/genstudio.md)的更多信息。


## Adobe 智能服务 {#integration-intelligent-service}

Adobe 智能服务是 Real Time Customer Data Platform 的原生服务，让您能够在客户体验用例中利用人工智能和机器学习的强大功能。借助此功能，营销分析人员可使用商业级别配置来设置特定于公司需求的预测，而无需具备数据科学专业知识。

借助客户人工智能，品牌商可利用流失率或转化率机器学习功能来建立分数，这些分数将作为 Adobe Experience Platform 中的轮廓属性，并可用于个性化历程。

了解有关[Journey Optimizer + Adobe Intelligent Services](../building-journeys/ai-services-overview.md)的更多信息。


## Adobe Campaign {#integration-ac}

如果您使用 Adobe Campaign v7 或 v8，则可以利用集成。借助此集成，可使用 Adobe Campaign 事务性消息传送功能发送电子邮件、推送通知和短信。

详细了解 [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md)。

您还可以设置与 Adobe Campaign Standard 的集成，以在历程中发送消息。

详细了解 [Journey Optimizer + Campaign Standard](../building-journeys/using-adobe-campaign-standard.md)。


## Adobe Workfront {#integration-workfront}

使用 Adobe Workfront 中的 Adobe Journey Optimizer 模块创建、读取、更新或删除记录，或执行对 Adobe Journey Optimizer API 的自定义 API 调用。

此博客文章[中提供了此集成的关键步骤的概述](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/accelerating-go-to-market-how-workfront-workfront-fusion-aep-and/ba-p/653685){target="_blank"}。

在Journey Optimizer文档[&#128279;](https://experienceleague.adobe.com/docs/workfront/using/adobe-workfront-fusion/fusion-apps-and-modules/adobe-journey-optimizer-modules.html?lang=zh-Hans){target="_blank"}中了解有关Adobe Workfront + Adobe Workfront 的更多信息。

## 自定义渠道 {#integration-custom}

如果您使用第三方系统发送消息，或者如果您希望历程将 API 调用发送到第三方系统，请使用自定义操作连接到您的历程。例如，您可以通过自定义操作连接到以下系统：Epsilon、Slack、[Adobe Developer](https://developer.adobe.com){target="_blank"}、Firebase等。

自定义操作是由技术用户定义并提供给营销人员的附加操作。配置完毕后，它们会显示在历程的左侧面板的&#x200B;**[!UICONTROL 操作]**&#x200B;类别中。请参阅[此页面](../building-journeys/about-journey-activities.md#action-activities)以了解详情。

详细了解[自定义操作](../action/about-custom-action-configuration.md)。

## 外部数据源 {#integration-external-systems}

借助 Journey Optimizer，您可以通过自定义数据源和自定义操作配置与外部系统的连接。例如，您可以使用来自外部预订系统的数据扩充您的历程。

有关如何使用外部数据源来定义与第三方系统的连接，请参阅[此部分](../datasource/external-data-sources.md)。
