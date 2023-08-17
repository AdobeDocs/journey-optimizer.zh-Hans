---
solution: Journey Optimizer
product: journey optimizer
title: 使用 Customer Journey Analytics
description: Customer Journey Analytics入门
feature: Reporting
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 0e45d6e4995f4f21dc5122203b715ae999e2b760
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 11%

---

# 使用 [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] 与集成 [!DNL Customer Journey Analytics] 通过自动报告分发和自定义数据可视化图表，全面了解您的所有历程。

![](assets/cja.png)

在中创建您的旅程后 [!DNL Journey Optimizer]，您可以将客户数据导入 [!DNL Customer Journey Analytics] 启动报告并了解客户与您的历程每次交互的影响。

➡️ [发现Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html){target="_blank"}

>[!NOTE]
>
>除了此集成外，您还可以将Adobe Journey Optimizer数据集的内容导出到云存储位置，并将此信息用于报表或分析。 [了解如何将数据集导出到云存储位置](../data/export-datasets.md)
>
>请注意，数据集导出功能当前为测试版，可供所有Adobe Journey Optimizer用户使用。 如果您尚未拥有访问权限，请与 Adobe 代表联系，获取目标的访问权限。

使用前 [!DNL Customer Journey Analytics] 对于您的历程，必须首先配置此集成：

1. [创建连接](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=zh-Hans) 在 [!DNL Customer Journey Analytics] 使用 **[!UICONTROL 数据集]** 您希望发送到Adobe Experience Platform。

   以下各项 [!DNL Journey Optimizer] 可以配置：
   * [历程步骤事件](../data/datasets-query-examples.md#journey-step-event)：用于查看谁进入您的旅程以及他们到达的距离。
   * [消息反馈/跟踪数据集](../data/datasets-query-examples.md#message-feedback-event-dataset)：用于查看有关您发送的消息的投放信息 [!DNL Journey Optimizer].
   * [实体和历程数据集](../data/datasets-query-examples.md#entity-dataset)：允许您搜索友好名称并在报表中使用它们。

1. [创建数据视图](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) 以配置要用于报表的维度和量度。

   您可以创建特定于Journey Optimizer的指标，以更好地反映历程的数据。 [了解详情](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)

使用 [!DNL Journey Optimizer] 替换为 [!DNL Customer Journey Analytics] 可能会导致报表数据中存在一些差异，原因如下：

* **两者 [!DNL Journey Optimizer] 和 [!DNL Customer Journey Analytics] 从Azure Data Lake Storage (ADLS)同步数据以进行报告。**

  不同产品处理传入数据的时间可能略有不同。 因此，显示从给定日期到当天的报表时，数据可能不匹配。 要减少差异，请使用除当天之外的日期范围。

* **在 [!DNL Journey Optimizer] 报表，“已发送”量度还包含“重试”量度。**

  **[!UICONTROL 重试]** 将不会包含在 **[!UICONTROL 已发送]** 中的量度 [!DNL Customer Journey Analytics]. 这将导致 [!DNL Customer Journey Analytics] **[!UICONTROL 已发送]** 用于显示小于以下值的量度 [!DNL Journey Optimizer]. 但是，重试数据会收敛到 **[!UICONTROL 成功发送的邮件数]** 或 **[!UICONTROL 跳出次数]** 量度。
为了减少差异，请使用一周前甚至更晚的日期范围。

* **报告是从其他数据源提供的。**

  这可能会导致产品之间的数据差异在1%到2%之间。
