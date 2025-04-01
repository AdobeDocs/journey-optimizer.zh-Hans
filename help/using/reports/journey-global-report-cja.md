---
solution: Journey Optimizer
product: journey optimizer
title: 历程报告
description: 了解如何使用历程报告中的数据
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 30d4f967-e085-44f1-973d-11e79f693e6e
source-git-commit: 8feb2e74f4ca3321ba4c96204cbdd2343a4ba92b
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 1%

---

# 历程报告 {#journey-global-report}

**历程报表**&#x200B;可用作一个包含所有内容的仪表板，提供与您的旅程关联的基本量度分析。 其中包括已输入用户档案计数和失败的个人历程实例等详细信息，可全面了解历程的有效性和参与级别。

使用&#x200B;**[!UICONTROL 查看报告]**&#x200B;按钮，可以直接从您的旅程访问&#x200B;**历程报告**。

![](assets/gs-cja-report-3.png)

要了解有关Customer Journey Analytics Workspace以及如何过滤和分析数据的更多信息，请参阅[此页面](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/home)。

## 历程概述 {#journey-global}

**[!UICONTROL 历程]**&#x200B;报告让您清楚地了解历程的最重要跟踪数据。

### 历程KPI {#journey-perfomance}

![](assets/cja-journey-kpis.png)

**[!UICONTROL 历程]**&#x200B;关键绩效指标(KPI)用作一个包含所有内容的仪表板，提供与您的旅程关联的基本量度分析。 其中包括输入的配置文件计数和失败的个人历程实例等详细信息，可全面了解历程的有效性和参与级别。

+++ 了解有关历程KPI指标的更多信息

* **[!UICONTROL 历程参与度]**：接收通过历程发送的消息的独特个人的总数，代表到达历程中指定操作点的不同用户档案。

* **[!UICONTROL 历程进入]**：到达历程进入事件的个人总数。

* **[!UICONTROL 历程退出]**：退出历程的个人总数。

+++

### 历程统计信息 {#journey-stats}

![](assets/cja-journey-stats.png)

**[!UICONTROL 历程统计数据]**&#x200B;表提供了有关历程的关键数据的详细摘要。 其中包括关键量度，如失败次数和成功进入次数，为您的电子邮件和历程的性能和影响提供有价值的见解。

+++ 了解有关历程统计量度的更多信息

* **[!UICONTROL 历程排除]**：由于预定义的标准或禁止显示规则而从历程中排除的个人总数。

* **[!UICONTROL 历程参与度]**：接收通过历程发送的消息的独特个人的总数，代表到达历程中指定操作点的不同用户档案。

* **[!UICONTROL 历程进入]**：到达历程进入事件的个人总数。

* **[!UICONTROL 历程退出]**：退出历程的个人总数。

* **[!UICONTROL 历程失败]**：未成功执行的单个历程总数。

* **[!UICONTROL 独特的历程进入次数]**：到达历程进入事件的个人总数，不考虑一个用户档案的多个交互。

* **[!UICONTROL 独特历程退出]**：退出旅程的个人总数，未考虑一个用户档案的多个交互。

* **[!UICONTROL 独特历程失败]**：未成功执行的单个历程总数，未考虑一个配置文件的多个交互。

+++

## 历程排除 {#journey-exclusion}

**[!UICONTROL 历程排除项]**&#x200B;表提供了导致排除用户配置文件的各种因素的综合视图。

## 操作错误 {#action-error}

![](assets/cja-journey-action-error.png)

**[!UICONTROL 操作错误]**&#x200B;构件详细列出了历程操作所发生的不同错误。

## 历程画布 {#journey-canvas}

![](assets/cja-journey-canvas.png)

**[!UICONTROL 历程画布]**&#x200B;小组件允许您在定向用户档案浏览您的旅程时直观地跟踪其轨迹。 [请参阅Customer Journey Analytics文档以了解详情](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/journey-canvas/journey-canvas)

使用以下选项增强画布自定义：

* 从&#x200B;**[!UICONTROL 节点类型]**&#x200B;下拉菜单添加或删除所需的活动类型，如消息或条件。
* 调整&#x200B;**[!UICONTROL 百分比值]**&#x200B;以确定不同历程路径之间的流量分配。
* 自定义您的&#x200B;**[!UICONTROL 箭头设置]**&#x200B;以包含标签、条件或选择干净显示。
* 启用&#x200B;**[!UICONTROL 显示流失]**&#x200B;选项以在画布上直接可视化退出历程的用户档案。

使用&#x200B;**[!UICONTROL 节点类型]**&#x200B;筛选时应用以下规则：

* 在节点上创建区段时，它仍将包含历程早期阶段的节点，即使这些节点已通过&#x200B;**[!UICONTROL 节点类型]**&#x200B;过滤器排除。

* 如果历程早期阶段的节点已通过&#x200B;**[!UICONTROL 节点类型]**&#x200B;过滤器排除，则无法创建通过箭头形成的区段。 在这种情况下，将在这些箭头上禁用右键单击功能。

## 操作表现 {#action-performance}

### 随时间变化的性能 {#action-overtime}

![](assets/cja-journey-action-performance.png)

**[!UICONTROL 随时间变化的性能]**&#x200B;图表允许您识别和分析符合条件的配置文件数量，这些配置文件将被视为操作的目标配置文件。 此可视化图表提供了关于策略有效性的宝贵见解，并帮助您制定数据驱动型决策以优化性能。

### 操作概述 {#action-overview}

![](assets/cja-journey-action-overview.png)

**[!UICONTROL 操作概述]**&#x200B;表用作综合仪表板，提供与历程中操作相关的关键量度分析。 这包括关键详细信息，例如交互次数和点进率

+++ 了解有关操作概述量度的更多信息

* **[!UICONTROL 节点进入]**：进入历程中特定节点的个人总数。

* **[!UICONTROL 历程失败]**：未成功执行的单个历程总数。

* **[!UICONTROL 点进率]**：与操作交互的用户百分比。

* **[!UICONTROL 点击次数]**：在操作中点击内容的次数。

* **[!UICONTROL 已投放]**：成功发送的操作数与已发送操作的总数相关。

+++

## 事件性能 {#events-performance}

### 随时间变化的性能 {#event-overtime}

![](assets/cja-journey-performance-event.png)

通过&#x200B;**[!UICONTROL 随时间变化的性能]**&#x200B;图表，您可以识别和分析符合事件目标配置文件的资格配置文件数。 这个强大的工具可帮助您跟踪一段时间内的趋势和模式，提供有助于优化事件策略的宝贵见解。

### 事件概述 {#event-overview}

![](assets/cja-journey-events-overview.png)

**[!UICONTROL 事件概述]**&#x200B;表显示一段时间内符合您的事件条件的配置文件数。 此工具可帮助您识别资格鉴定率中的模式，以优化事件策略。

+++ 了解有关历程统计量度的更多信息

* **[!UICONTROL 人员]**：符合活动目标配置文件资格的用户配置文件数。

+++
