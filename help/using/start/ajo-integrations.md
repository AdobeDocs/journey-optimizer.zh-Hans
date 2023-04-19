---
solution: Journey Optimizer
product: journey optimizer
title: 与其他解决方案集成
description: 详细了解如何将 Journey Optimizer 与其他解决方案集成
topic: Content Management
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 14b081fbc1d824664c82e6af262a0a7e50764c0c
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 100%

---

# 与其他解决方案集成 {#integration}

借助 Adobe Journey Optimizer，您可以轻松管理、保留此类数据，并将其导出到技术堆栈中所包含的平台或系统。这些集成可帮助您解决特定用例，并扩展 Adobe Journey Optimizer 的功能范围。

>[!NOTE]
>
> Adobe Journey Optimizer 构建于 Adobe Experience Platform 之上，以原生方式连接到 [Adobe Real-time Customer Profile](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}。此内置数据源已预配置，旨在检索和使用 Real-time Customer Profile 中的数据（例如，检查进入历程的人员是否为客户）。该数据源允许您使用用户档案数据和体验事件数据。[了解详情](../datasource/adobe-experience-platform-data-source.md)。

## 了解 Adobe Customer Journey Analytics{#integration-cja}

您可以使用 Customer Journey Analytics 对 Journey Optimizer 生成的数据执行高级分析。

Journey Optimizer 将数据存储在 Adobe Experience Platform 中，借助 Customer Journey Analytics，可通过自动报告分发和自定义数据可视化，全面了解您的所有历程、活动和优惠。

在 Journey Optimizer 中创建您的历程后，Customer Journey Analytics 可以从平台中摄取数据以生成报告，了解客户与您的历程每次交互的影响。

详细了解 [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md)。

## Adobe Analytics{#integration-aa}

您可以利用已在捕获并流入到 Adobe Experience Platform 中的所有 Adobe Analytics 行为事件数据，从而触发实时历程并将客户的体验自动化。此数据还可用于创建可使用 Journey Optimizer 接触的区段。

详细了解 [Journey Optimizer + Analytics](../event/about-analytics.md)。


## Adobe Experience Manager Assets Essentials{#integration-assets}

利用 [!DNL Adobe Experience Manager Assets Essentials] 整合营销和创意工作流。与 [!DNL Adobe Journey Optimizer] 原生集成，可访问 [!DNL Assets Essentials] 来存储、管理、发现和分配数字资源。提供了单一集中式资源存储库，您可以使用它来填充消息。

通过左侧菜单&#x200B;**[!UICONTROL 资源]**&#x200B;部分的 [!DNL Adobe Journey Optimizer]，可直接访问 [!DNL Adobe Experience Manager Assets Essentials]。

了解 [Journey Optimizer + Assets Essentials](../email/assets-essentials.md) 的更多信息。


## Adobe Stock{#integration-stock}

[!DNL Adobe Stock] 和 [!DNL Adobe Journey Optimizer] 电子邮件设计器集成增效工具可帮助客户在创作消息时轻松进行导航、许可并保存图像。

通过 [!DNL Adobe Journey Optimizer]，您可以将图像直接从 [!DNL Adobe Stock] 上传到电子邮件，并使用&#x200B;**[!UICONTROL 查找 Adobe Stock 照片]**&#x200B;选项将其添加到&#x200B;**[!UICONTROL 资源]**&#x200B;文件夹中。此外，**[!UICONTROL 查找类似 Stock 照片]**&#x200B;选项可帮助您查找与投放中所用资源的内容、颜色和合成相匹配的图像。

了解 [Journey Optimizer + Stock](../email/stock.md) 的更多信息。


## Adobe 智能服务{#integration-intelligent-service}

Adobe 智能服务是 Real Time Customer Data Platform 的原生服务，让您能够在客户体验用例中利用人工智能和机器学习的强大功能。借助此功能，营销分析人员可使用商业级别配置来设置特定于公司需求的预测，而无需具备数据科学专业知识。

借助客户人工智能，品牌商可利用流失率或转化率机器学习功能来建立分数，这些分数将作为 Adobe Experience Platform 中的用户档案属性，并可用于个性化历程。

[了解详情](../building-journeys/ai-services-overview.md)。


## Adobe Campaign{#integration-ac}

如果您使用 Adobe Campaign v7 或 v8，则可以利用集成。借助此集成，可使用 Adobe Campaign 事务性消息传送功能发送电子邮件、推送通知和短信。

详细了解 [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md)。

您还可以设置与 Adobe Campaign Standard 的集成，以在历程中发送消息。

详细了解 [Journey Optimizer + Campaign Standard](../building-journeys/ajo-ac.md)。

## 自定义渠道{#integration-custom}

如果您使用第三方系统发送消息，或者如果您希望历程将 API 调用发送到第三方系统，请使用自定义操作连接到您的历程。例如，您可以通过自定义操作连接到以下系统：Epsilon、Slack、[Adobe Developer](https://developer.adobe.com){target="_blank"}、Firebase 等。

自定义操作是由技术用户定义并提供给营销人员的附加操作。配置完毕后，它们会显示在历程的左侧面板的&#x200B;**[!UICONTROL 操作]**&#x200B;类别中。请参阅[此页面](../building-journeys/about-journey-activities.md#action-activities)以了解详情。

详细了解[自定义操作](../action/about-custom-action-configuration.md)。

## 外部数据源{#integration-external-systems}

借助 Journey Optimizer，您可以通过自定义数据源和自定义操作配置与外部系统的连接。例如，您可以使用来自外部预订系统的数据扩充您的历程。

有关如何使用外部数据源来定义与第三方系统的连接，请参阅[此部分](../datasource/external-data-sources.md)。
