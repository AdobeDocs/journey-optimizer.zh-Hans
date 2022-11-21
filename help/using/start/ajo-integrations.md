---
solution: Journey Optimizer
product: journey optimizer
title: 与其他解决方案集成
description: 了解更多如何将Journey Optimizer与其他解决方案集成
topic: Content Management
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 90d7d4d39fe04198707be3d5b24888cfe5bed308
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 5%

---

# 与其他解决方案集成 {#integration}

借助Adobe Journey Optimizer，您可以轻松管理、保留此数据并将其导出到技术堆栈中所包含的平台或系统。 这些集成可帮助您解决特定用例问题并扩展Adobe Journey Optimizer功能范围。

>[!NOTE]
>
> Adobe Journey Optimizer构建于Adobe Experience Platform上，本地连接到 [Adobe实时客户资料](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target=&quot;_blank&quot;}。 此内置数据源已预配置，旨在从实时客户资料中检索和使用数据（例如，检查进入旅程的人员是否为客户）。 它允许您使用用户档案数据和体验事件数据。 [了解详情](../datasource/adobe-experience-platform-data-source.md)。

## Adobe Customer Journey Analytics{#integration-cja}

您可以使用Customer Journey Analytics对Journey Optimizer生成的数据执行高级分析。

Journey Optimizer在Adobe Experience Platform中存储数据，通过“Customer Journey Analytics”，可通过自动报表分发和数据的自定义可视化，全面了解您的所有历程、营销活动和选件。

在Journey Optimizer中创建您的旅程后，Customer Journey Analytics可以从平台中摄取数据以开始报告并了解客户与您的历程进行的每次交互的影响。

详细了解 [Journey Optimizer +Customer Journey Analytics](../reports/cja-ajo.md).

## Adobe Analytics{#integration-aa}

您可以利用已在捕获并流入Adobe Experience Platform的所有Adobe Analytics行为事件数据来触发实时历程并自动化客户体验。 此数据还可用于创建可使用Journey Optimizer参与的区段。

详细了解 [Journey Optimizer + Analytics](../event/about-analytics.md).

## Adobe智能服务{#integration-intelligent-service}

Adobe智能服务是Real Time Customer Data Platform的本机服务，让您能够在客户体验用例中利用人工智能和机器学习的强大功能。 这允许营销分析人员使用业务级别配置来设置特定于公司需求的预测，而无需具备数据科学专业知识。

Customer AI允许品牌创建基于流失率或转化机器学习的得分，这些得分将作为Adobe Experience Platform中的用户档案属性提供，并可用于个性化旅程。

[了解详情](../building-journeys/ai-services-overview.md)。


## Adobe Campaign{#integration-ac}

如果您具有Adobe Campaign v7或v8，则集成可用。 使用此集成，可使用Adobe Campaign事务型消息传送功能发送电子邮件、推送通知和短信。

详细了解 [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md).

您还可以设置与Adobe Campaign Standard的集成，以在您的历程中发送消息。

详细了解 [Journey Optimizer +Campaign Standard](../building-journeys/ajo-ac.md).

## 自定义渠道{#integration-custom}

如果您使用第三方系统发送消息，或者如果您希望历程将API调用发送到第三方系统，请使用自定义操作连接到您的历程。 例如，您可以通过自定义操作连接到以下系统：Epsilon，Slack, [Adobe Developer](https://developer.adobe.com){target=&quot;_blank&quot;}、Firebase等。

自定义操作是技术用户定义并可供营销人员使用的其他操作。 配置完毕后，它们会显示在 **[!UICONTROL 操作]** 类别。 请参阅[此页面](../building-journeys/about-journey-activities.md#action-activities)以了解详情。

详细了解 [自定义操作](../action/about-custom-action-configuration.md).

## 外部数据源{#integration-external-systems}

Journey Optimizer允许您通过自定义数据源和自定义操作配置与外部系统的连接。 例如，这允许您使用来自外部预订系统的数据扩充您的历程。

了解如何使用外部数据源定义与 [此部分](../datasource/external-data-sources.md).
