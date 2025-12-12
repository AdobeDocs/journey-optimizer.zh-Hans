---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 数据工程师入门
description: 作为历程工程师，了解有关如何使用 Journey Optimizer 的更多信息
feature: Get Started
role: Developer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 52%

---

# 数据工程师入门 {#data-engineer}

作为&#x200B;**Adobe Journey Optimizer数据工程师**，您可以准备并维护客户配置文件数据以支持[!DNL Journey Optimizer]编排的体验，在架构中对客户和业务数据进行建模，并为摄取数据配置源连接器。 [系统管理员](administrator.md)向您授予访问权限并准备好环境后，您即可开始使用 [!DNL Adobe Journey Optimizer]。

>[!NOTE]
>
>要了解有关&#x200B;**数据摄取**&#x200B;的更多信息，请参阅 [Adobe Experience Platform 文档](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=zh-Hans){target="_blank"}。

## 基本数据配置步骤

请按照以下步骤为Journey Optimizer设置数据基础：

1. **创建身份命名空间**。 在 Adobe [!DNL Journey Optimizer] 中，跨设备和渠道的&#x200B;**身份标识**&#x200B;与用户相关联，从而会生成一个身份标识图。关联的身份图用于根据您所有业务接触点之间的交互对体验进行个性化。 要了解有关身份标识和身份标识命名空间的更多信息，请参阅[此页面](../../audience/get-started-identity.md)。

   此外，请配置&#x200B;**补充标识符**，使同一配置文件能够根据辅助标识符（如订单ID或预订ID）输入多个历程实例。 了解[补充标识符](../../building-journeys/supplemental-identifier.md)。

1. **创建架构**&#x200B;并为配置文件启用它们。 架构是一组规则，用于表示和验证数据的结构和格式。在高层面上，架构提供了真实世界对象（如人）的抽象定义，并概括了该对象的每个实例中应包含哪些数据（如名字、姓氏、生日等）。

   * 对于标准历程和营销活动：使用[XDM架构](../../data/get-started-schemas.md)
   * 对于编排的营销活动：创建[关系架构](../../orchestrated/gs-schemas.md)以启用多实体分段

1. **创建数据集**&#x200B;并为配置文件启用它们。 数据集是用于数据集合的存储和管理结构，通常是表格，其中包含架构（列）和字段（行）。数据集还包含描述其存储的数据的各方面特性的元数据。创建数据集后，您可以将其映射到现有架构并向其中添加数据。要了解有关数据集的更多信息，请参阅[此页面](../../data/get-started-datasets.md)。

   对于高级方案，请为运行时查找&#x200B;**准备**&#x200B;数据集，以使用记录数据集中的实时数据扩充历程执行。 了解[数据集查找](../../building-journeys/dataset-lookup.md)。

1. **配置源连接器**。 Adobe Journey Optimzer 允许从外部源摄取数据，同时让您能够使用 Platform 服务来构建、赋予标签和增强传入数据。您可以从各种源中摄取数据，如 Adobe 应用程序、基于云的存储、数据库和许多其他源。要了解有关源连接器的更多信息，请参阅[此页面](../get-started-sources.md)。

1. **创建测试轮廓**。当在历程中使用[测试模式](../../building-journeys/testing-the-journey.md)时，需要测试轮廓，并在发送之前[预览和测试消息](../../content-management/preview-test.md)。[本页面](../../audience/creating-test-profiles.md)中详细说明了创建测试轮廓的步骤。

1. **配置计算属性**（可选）。 从用户档案数据创建派生属性以简化分段和个性化。 计算属性会自动计算复杂量度，如“过去90天内的总购买量”或“平均订单值”。 了解[计算属性](../../audience/computed-attributes.md)。

此外，若要能够在历程中发送消息，您必须配置&#x200B;**[!UICONTROL 数据源]**、**[!UICONTROL 事件]**&#x200B;和&#x200B;**[!UICONTROL 操作]**。 [在此部分中](../../configuration/about-data-sources-events-actions.md)了解详情。

![](../assets/admin-menu.png)

* **数据源**&#x200B;配置允许您定义与系统的连接，以检索将在您的历程中使用的其他信息。要了解有关数据源的更多信息，请参阅[此部分](../../datasource/about-data-sources.md)。

* **事件**&#x200B;允许您统一触发历程，向流入历程的个人实时发送消息。在事件配置中，您可以配置历程中的预期事件。传入事件的数据按照 Adobe 体验数据模型 (XDM) 进行标准化。事件来自已验证和未验证事件（如 Adobe Mobile SDK 事件）的流摄取 API。要了解有关事件的更多信息，请参阅[此部分](../../event/about-events.md)。

* [!DNL Journey Optimizer] 附带内置消息功能：您可以在历程中创建消息并设计内容。如果您使用第三方系统来发送消息，例如 Adobe Campaign，请创建&#x200B;**自定义操作**。在本节[中了解有关操作](../../action/action.md)的更多信息。

## 监控和分析历程数据

运行历程后，您可以在数据湖中查询历程步骤事件以监测性能、排除问题并分析客户行为。 使用SQL查询进行分析：

* 配置文件进入和退出模式
* 错误率和放弃原因
* 读取受众导出作业性能
* 自定义操作性能指标
* 历程实例状态和瓶颈

探索历程分析[的现成](../../reports/query-examples.md)查询示例以开始数据分析和故障排除。

## 保持最新

跟上最新的Journey Optimizer功能和改进：

* **[发行说明](../../rn/release-notes.md)**：查看每月发布的新增功能、增强功能和修复
* **[文档更新](../../rn/documentation-updates.md)**：跟踪对文档的最近更改，包括新页面和更新的内容
* **产品通知**：在[Adobe Experience Cloud配置文件](https://experience.adobe.com/preferences){target="_blank"}中启用通知，以接收有关以下内容的提醒：
   * 新产品版本和功能
   * 维护窗口和系统更新
   * 重要公告和变更

  要启用通知，请单击Adobe Experience Cloud右上角的配置文件图标，转到&#x200B;**首选项>通知**，然后配置您的Journey Optimizer通知首选项。
