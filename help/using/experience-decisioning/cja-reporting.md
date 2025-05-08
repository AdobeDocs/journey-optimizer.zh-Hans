---
title: 决策报告
description: 了解如何报告决策。
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
source-git-commit: 4839c3c70dcc524da5f3cc394d5573ce5755ea64
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 4%

---


# 决策报告 {#decisioning-report}

## 基于代码的营销活动报表 {#campaigns}

一旦基于代码的体验上线，您就可以访问专用报告来监控决策关键绩效指标(KPI)。

<!--Once code-based experiences are live, you can access dedicated reports to monitor Key Performance Indicators (KPIs) as an all-encompassing dashboard, delivering an analysis of essential metrics associated with your campaign.

This encompasses details related to the decision items performances and how users interacted with them. [Learn how to work with Code-based experience reports](../reports/campaign-global-report-cja-code.md)-->

![](../reports/assets/cja-decisioning-kpis.png)

您还可以访问与决策项目绩效以及用户如何与其交互相关的详细信息，从而提供与您的活动关联的基本量度分析。

![](../reports/assets/cja-decisioning-item-performance.png)

在[本节](../reports/campaign-global-report-cja-code.md#decisioning-reporting)中了解如何使用有关Decisioning的基于代码的体验报告。

## 客户历程分析中的报告 {#cja}

如果您正在使用Customer Journey Analytics，则可以利用Decisioning为您的基于代码的营销活动创建自定义报告仪表板。

下面列出了主要步骤。 有关如何使用Customer Journey Analytics的详细信息，请参阅[Customer Journey Analytics文档](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/cja-landing){target="_blank"}。

1. 在Customer Journey Analytics中创建并配置&#x200B;**连接**。 这允许您连接到需要报表的数据集。 [了解如何创建连接](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. 创建&#x200B;**数据视图**&#x200B;并将其关联到之前创建的连接。 在&#x200B;**[!UICONTROL 组件]**&#x200B;选项卡中，选择要显示在报告中的相关架构字段。 对于Decisioning，请确保包含&#x200B;**propositioninteract**&#x200B;和&#x200B;**propositiondisplay**&#x200B;字段。 [了解如何创建和配置数据视图](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. 在&#x200B;**工作区项目**&#x200B;中组合数据组件、表和可视化图表，为基于代码的营销活动创建和共享报告。 [了解如何创建工作区项目](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
