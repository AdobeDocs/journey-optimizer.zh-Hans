---
solution: Journey Optimizer
product: journey optimizer
title: 使用历程步骤事件
description: 了解如何在Adobe Journey Optimizer中使用journey step事件 — 了解它们是什么、它们为什么重要以及如何使用它们进行分析和优化
feature: Journeys, Reporting
role: Developer, Admin, User
level: Intermediate, Experienced
keywords: 历程，步骤事件，分析，报告，监控， XDM
exl-id: 2e7c5ea5-d8c5-416d-ab88-d2bc02043558
source-git-commit: 97fa287d94efb7fb95817fc15268e736517cb629
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 2%

---

# 使用历程步骤事件 {#work-with-journey-step-events}

历程步骤事件是自动生成的事件，用于捕获[配置文件](../audience/get-started-profiles.md)在Adobe Journey Optimizer中执行[历程](../building-journeys/journey.md)时执行的每个步骤的详细信息。 这些事件提供对[历程性能](../building-journeys/report-journey.md)的全面可见性，并启用强大的分析功能。

## 什么是历程步骤事件 {#what-are-step-events}

历程步骤事件是系统生成的[XDM (Experience Data Model)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}事件，每当配置文件在旅程中从一个节点移动到另一个节点时，Adobe Journey Optimizer会自动创建这些事件并将其发送到[Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=zh-Hans){target="_blank"}。 每个事件对应于客户历程体验中的特定[历程活动](../building-journeys/about-journey-activities.md)或过渡。

历程步骤事件有两种主要类型：

- **journeyStepEvent**：与通过历程步骤的各个配置文件进程相关的事件
- **journeyStepProfileEvent**：包含其他配置文件上下文信息的事件

### 什么会触发历程步骤事件？ {#event-triggers}

系统会自动为各种旅程活动生成历程步骤事件：

- **进入事件**：个人资料[进入历程](../building-journeys/entry-management.md)时
- **操作执行**：发送[消息时](../building-journeys/journey-action.md)或执行[自定义操作](../building-journeys/using-custom-actions.md)
- **条件评估**：当配置文件通过[条件](../building-journeys/condition-activity.md)和决策点时
- **等待活动**：配置文件进入并退出时[等待节点](../building-journeys/wait-activity.md)
- **退出事件**：当配置文件完成或[退出历程](../building-journeys/end-journey.md)
- **错误处理**：在历程执行期间发生错误时

>[!NOTE]
>
>默认情况下，将在所有实例上激活历程步骤事件。 您无法修改或更新在配置步骤事件期间创建的[架构和数据集](sharing-overview.md)。 这些架构和数据集处于只读模式。

了解有关[历程步骤事件架构](sharing-field-list.md)的更多信息。

## 历程步骤事件为何重要 {#why-step-events-matter}

历程步骤事件为使用Adobe Journey Optimizer的组织提供了关键值：

### 实时分析和监控 {#real-time-analytics}

- **历程性能跟踪**：使用[实时报告](live-report.md)实时监视用户档案如何在您的历程中流动
- **转化分析**：通过[历程分析](journey-global-report-cja.md)了解流失点和成功的转化路径
- **错误检测**：通过[监视和警报](alerts.md)发现并解决出现的问题

### 数据集成和见解 {#data-integration}

- **跨平台分析**：将历程数据与其他[Adobe Experience Platform数据源](../datasource/adobe-experience-platform-data-source.md)相结合
- **客户360视图**：创建包含历程交互的完整[客户配置文件](../audience/get-started-profiles.md)
- **归因建模**：使用[Customer Journey Analytics](cja-ajo.md)将历程接触点连接到下游业务结果

### 优化机会 {#optimization}

- **A/B测试见解**：使用[试验](campaign-global-report-cja-experimentation.md)分析不同历程路径的性能
- **Personalization增强功能**：使用历程行为数据来改进[动态内容](../personalization/dynamic-content.md)的未来体验
- **运营效率**：识别瓶颈并优化[历程设计](../building-journeys/using-the-journey-designer.md)

## 如何使用历程步骤事件 {#how-to-use-step-events}

### 访问历程步骤事件数据 {#accessing-data}

历程步骤事件数据自动存储在Adobe Experience Platform中，可通过以下方式访问：

1. **Data Lake查询**：使用SQL查询`journey_step_events`查询服务[的](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=zh-Hans){target="_blank"}数据集
2. **Customer Journey Analytics**：通过[高级分析工具](cja-ajo.md)分析历程数据
3. **实时报表**：通过Journey Optimizer的[内置报表功能访问数据](gs-reports.md)
4. **API**：以编程方式访问自定义应用程序的事件数据

了解有关[访问数据集](../data/datasets-query-examples.md)的详细信息。

### 可用的关键数据点 {#key-data-points}

历程步骤事件捕获全面的信息，包括：

- **历程标识**：[历程ID、版本和名称](sharing-journey-fields.md)
- **配置文件信息**：[配置文件ID和关联的身份](sharing-identity-fields.md)
- **步骤详细信息**：[节点名称、步骤类型和执行状态](sharing-common-fields.md)
- **时间戳**：每个历程步骤的精确计时
- **操作结果**： [成功/失败状态和执行详细信息](sharing-execution-fields.md)
- **错误信息**：发生问题时显示详细的[错误代码和描述](sharing-field-list.md#discarded-events)

浏览所有[可用的字段定义](sharing-field-list.md)。

### 常见使用案例 {#common-use-cases}

**性能监控**

```sql
-- Example: Count profiles entering a journey in the last 24 hours
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-id>'
AND _experience.journeyOrchestration.stepEvents.nodeType='start'
AND DATE(timestamp) > (now() - interval '24' hour);
```

**错误分析**

```sql
-- Example: Identify errors by journey node
SELECT _experience.journeyOrchestration.stepEvents.nodeName,
       count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName;
```

**历程funnel分析**

- 跟踪每个历程步骤的转化率
- 确定用户档案最常退出历程的位置
- 测量不同历程阶段逗留的时间

了解有关funnel analysis[的更多](query-examples.md#common-queries)查询技术。

## 示例和资源 {#samples-resources}

### 查询示例和模板 {#query-examples}

浏览全面的查询示例以了解常见的历程步骤事件分析：

- **[历程步骤事件查询示例](query-examples.md)**：适用于常见分析方案的现成的SQL查询
- **[数据集查询示例](../data/datasets-query-examples.md#journey-step-event)**：查询历程步骤事件数据集的示例
- **[基于个人资料的查询](query-examples.md#profile-based-queries)**：跟踪个人资料历程和交互

### 字段文档 {#field-documentation}

了解历程步骤事件的完整数据结构：

- **[历程步骤事件字段列表](sharing-field-list.md)**：所有可用字段的综合引用
- **[常用字段](sharing-common-fields.md)**：跨journeyStepEvent和journeyStepProfileEvent的共享字段
- **[操作执行字段](sharing-execution-fields.md)**：特定于操作执行跟踪的字段
- **[历程字段](sharing-journey-fields.md)**：特定于历程的元数据和标识符

### 最佳实践和故障排除 {#best-practices}

**性能优化**

- 使用`journeyVersionID`而不是`journeyVersionName`以获得更好的查询性能（[了解有关历程属性的更多信息](../building-journeys/expression/journey-properties.md)）
- 按日期范围过滤，提高大型数据集的查询速度
- 利用与您的[历程命名空间配置](../building-journeys/entry-management.md)匹配的配置文件身份

**数据质量**

- 定期监视[丢弃的事件](sharing-field-list.md#discarded-events)以识别数据问题
- 验证事件架构是否符合您的分析要求
- 在自定义查询中实施正确的错误处理

**分析策略**

- 将历程步骤事件与[消息反馈数据](../data/datasets-query-examples.md#message-feedback-event-dataset)相结合，以实现完整归因
- 使用基于时间的分析来了解历程速度和瓶颈

### 高级分析功能 {#advanced-analytics}

**Customer Journey Analytics集成**
可以使用[Customer Journey Analytics](cja-ajo.md)分析历程步骤事件：

- 高级归因建模
- 跨渠道历程可视化
- 历程结果的预测分析

了解如何[为Journey Optimizer数据](report-gs-cja.md)配置Customer Journey Analytics。

## 其他资源 {#additional-resources}

### 文档链接 {#documentation-links}

- **[历程步骤共享概述](sharing-overview.md)**：了解历程数据如何流向Adobe Experience Platform
- **[内置架构词典](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=zh-Hans){target="_blank"}**：完整XDM架构引用
- **[Journey Optimizer报表](report-gs-cja.md)**： Journey Optimizer报表功能概述

### 集成指南 {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)**：分析CJA中的Journey Optimizer数据
- **[数据管理](../data/export-datasets.md)**：导出和管理历程数据
- **[隐私和治理](../privacy/audit-logs.md)**：历程事件的数据管理注意事项


**后续步骤：**

- 从[创建您的第一个历程报告开始](sharing-overview.md)
- 浏览[查询示例](query-examples.md)以了解特定用例
- 了解[历程管理最佳实践](../building-journeys/journey.md)
