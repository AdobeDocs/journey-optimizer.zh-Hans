---
solution: Journey Optimizer
product: journey optimizer
title: 使用 Customer Journey Analytics
description: Customer Journey Analytics入门
feature: Reporting, Integrations
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 6%

---

# 手动配置[!DNL Customer Journey Analytics] {#cja-ajo}

[!DNL Journey Optimizer]与[!DNL Customer Journey Analytics]的集成通过自动报告分发和自定义数据可视化提供了所有历程的整体视图。

以下部分概述了如何手动利用Journey Optimizer生成的数据在Customer Journey Analytics中进行深入分析。 请注意，此集成可自动设置。 [了解详情](report-gs-cja.md)

![](assets/cja.png)

在[!DNL Journey Optimizer]中创建您的历程后，您可以将客户数据导入到[!DNL Customer Journey Analytics]以启动报告并了解客户与您的历程每次交互的影响。

➡️[发现Customer Journey Analytics](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/integrations/ajo#manually-configure-a-data-view-to-be-used-with-journey-optimizer){target="_blank"}

>[!NOTE]
>
>除了此集成外，您还可以将Adobe Journey Optimizer数据集的内容导出到云存储位置，并将此信息用于报表或分析。 [了解如何将数据集导出到云存储位置](../data/export-datasets.md)
>
>请注意，数据集导出功能当前为测试版，可供所有Adobe Journey Optimizer用户使用。 如果您尚未拥有访问权限，请与 Adobe 代表联系，获取目标的访问权限。

在为您的历程使用[!DNL Customer Journey Analytics]之前，必须首先配置此集成：

1. [在[!DNL Customer Journey Analytics]中创建与要发送到Adobe Experience Platform的&#x200B;**[!UICONTROL 数据集]**&#x200B;的连接](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=zh-Hans)。

   可以配置以下[!DNL Journey Optimizer]：
   * [历程步骤事件](../data/datasets-query-examples.md#journey-step-event)：允许您查看谁进入您的旅程以及他们到达的距离。
   * [消息反馈/跟踪数据集](../data/datasets-query-examples.md#message-feedback-event-dataset)：允许您查看有关通过[!DNL Journey Optimizer]发送的消息的投放信息。
   * [实体和历程数据集](../data/datasets-query-examples.md#entity-dataset)：允许您搜索友好名称并在报表中使用它们。

1. [创建数据视图](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=zh-Hans)以配置要用于报告的维度和量度。

   您可以创建特定于Journey Optimizer的指标，以更好地反映历程的数据。 [了解详情](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html?lang=zh-Hans#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)

将[!DNL Journey Optimizer]与[!DNL Customer Journey Analytics]结合使用可能会导致报表数据存在某些差异，原因如下：

* **从Azure Data Lake Storage (ADLS)同步[!DNL Journey Optimizer]和[!DNL Customer Journey Analytics]数据以便报告。**

  不同产品处理传入数据的时间可能略有不同。 因此，显示从给定日期到当天的报表时，数据可能不匹配。 要减少差异，请使用除当天之外的日期范围。

* **在[!DNL Journey Optimizer]个报表中，发送的度量还包含重试度量。**

  **[!UICONTROL 重试]**&#x200B;将不包含在[!DNL Customer Journey Analytics]的&#x200B;**[!UICONTROL 已发送]**&#x200B;度量中。 这将导致[!DNL Customer Journey Analytics] **[!UICONTROL 已发送]**&#x200B;指标显示的值低于[!DNL Journey Optimizer]。 但是，重试数据已合并到&#x200B;**[!UICONTROL 成功发送的邮件]**&#x200B;或&#x200B;**[!UICONTROL 跳出次数]**&#x200B;度量中。
为了减少差异，请使用一周前甚至更晚的日期范围。

* **报告是从其他数据源提供的。**

  这可能会导致产品之间的数据差异在1%到2%之间。
