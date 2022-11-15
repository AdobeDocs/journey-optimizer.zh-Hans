---
solution: Journey Optimizer
product: journey optimizer
title: 使用 Customer Journey Analytics
description: 开始使用Customer Journey Analytics
feature: Reporting
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 928ad6822efbe95c0ddf5456531d92be8b4bed75
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 8%

---

# 使用 [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] 集成 [!DNL Customer Journey Analytics] 通过自动报表分发和自定义的数据可视化，提供所有历程的整体视图。

![](assets/cja.png)

在中创建您的历程后 [!DNL Journey Optimizer]，您可以将客户数据导入 [!DNL Customer Journey Analytics] 以开始报告并了解客户与您的历程进行的每次交互的影响。

➡️ [发现Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html){target=&quot;_blank&quot;}

使用之前 [!DNL Customer Journey Analytics] 对于您的历程，必须首先配置此集成：

1. [创建连接](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=zh-Hans) in [!DNL Customer Journey Analytics] 和 **[!UICONTROL 数据集]** 你想发到Adobe Experience Platform。

   以下 [!DNL Journey Optimizer] 可以配置：
   * [历程步骤事件](../data/datasets-query-examples.md#journey-step-event):允许您查看进入您的历程的人员及其到达的距离。
   * [消息反馈/跟踪数据集](../data/datasets-query-examples.md#message-feedback-event-dataset):允许您查看通过 [!DNL Journey Optimizer].
   * [实体和历程数据集](../data/datasets-query-examples.md#entity-dataset):允许您搜索友好名称，并在报表中使用它们。

1. [创建数据视图](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) 配置要用于报表的维度和量度。

   您可以创建特定于Journey Optimizer的量度，以更好地反映您的历程数据。 [了解详情](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)


使用 [!DNL Journey Optimizer] with [!DNL Customer Journey Analytics] 可能会导致以下原因导致报表数据出现差异：

* **两者兼有 [!DNL Journey Optimizer] 和 [!DNL Customer Journey Analytics] 同步来自Azure数据湖存储(ADLS)的数据以进行报告。**

   不同产品对传入数据的处理时间可能略有不同。 因此，在显示从给定日期到当前日期的报表时，数据可能不匹配。 为了减少差异，请使用排除当天的日期范围。

* **在 [!DNL Journey Optimizer] 报表中，“已发送”量度还包含“重试”量度。**

   **[!UICONTROL 重试]** 将不包含在 **[!UICONTROL 已发送]** 量度 [!DNL Customer Journey Analytics]. 这将导致 [!DNL Customer Journey Analytics] **[!UICONTROL 已发送]** 显示的值低于 [!DNL Journey Optimizer]. 但是，重试数据会聚合到 **[!UICONTROL 消息已成功发送]** 或 **[!UICONTROL 跳出次数]** 量度。
要减少差异，请使用一周前甚至更晚的日期范围。

* **报表来自其他数据源。**

   这可能会导致产品之间出现1%到2%的数据差异。
