---
title: Journey Optimizer数据工程师入门
description: 作为数据工程师，了解如何使用Journey Optimizer
level: Intermediate
source-git-commit: a27a6d7ab96bd08e7a2601c2e86d1d9f0fc4be0a
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 8%

---

# 数据工程师入门 {#data-engineer}

![数据工程师](assets/do-not-localize/user-1.png)

作为 **Adobe Journey Optimizer数据工程师**、准备和维护客户用户档案数据，以支持由 [!DNL Journey Optimizer]，在架构中为客户和业务数据建模，并配置源连接器以摄取数据。 您可以开始使用 [!DNL Adobe Journey Optimizer] 一次 [系统管理员](administrator.md) 授予您访问权限并准备环境。


了解如何 **识别数据并创建架构和数据集** 以将您的数据导入本页中的Adobe Experience Platform。

>[!NOTE]
>
>详细了解 **数据摄取** in [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=zh-Hans){target=&quot;_blank&quot;}。

以下各节详细介绍了为用户档案和测试用户档案创建身份命名空间和启用数据集的步骤：

1. **创建身份命名空间**. Adobe [!DNL Journey Optimizer], **标识** 关联跨设备和渠道的用户，结果会生成一个身份图。 链接的身份图用于根据您所有业务接触点之间的交互对体验进行个性化。  进一步了解身份和身份命名空间 [本页](../get-started-identity.md).

1. **创建架构** 并为用户档案启用它。 架构是一组规则，用于表示和验证数据的结构和格式。 在高级别上，架构提供了真实世界对象（如人）的抽象定义，并概述了该对象的每个实例中应包含哪些数据（如名字、姓氏、生日等）。  进一步了解模式 [本页](../get-started-schemas.md).

1. **创建数据集** 并为用户档案启用它。 数据集是用于数据集合的存储和管理结构，通常是表格，其中包含架构（列）和字段（行）。数据集还包含描述其存储数据各个方面的元数据。 创建数据集后，您可以将其映射到现有架构并向其中添加数据。 了解有关数据集的更多信息 [本页](../get-started-datasets.md).

1. **配置源连接器**. Adobe历程优化器允许从外部源摄取数据，同时让您能够使用平台服务来构建、标记和增强传入数据。 您可以从各种源摄取数据，如Adobe应用程序、基于云的存储、数据库和许多其他源。 了解有关源连接器的更多信息 [本页](../get-started-sources.md).

1. **创建测试用户档案**. 使用 [测试模式](../building-journeys/testing-the-journey.md) 在旅程中，和 [预览和测试消息](../preview.md) 发送之前。 了解创建测试用户档案的步骤 [本页](../../using/building-journeys/creating-test-profiles.md).


此外，要在历程中发送消息，您必须配置 **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** 和 **[!UICONTROL Actions]**. 了解更多 [在此部分中](../../using/configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* 的 **数据源** 配置允许您定义与系统的连接，以检索将在您的历程中使用的其他信息。 了解有关数据源的更多信息 [在此部分中](../datasource/about-data-sources.md).

* **事件** 允许您一直触发旅程，以实时向流入旅程的个人发送消息。 在事件配置中，您可以配置历程中预期的事件。 传入事件的数据按照Adobe体验数据模型(XDM)进行标准化。 事件来自已验证和未验证事件（如 Adobe Mobile SDK 事件）的流摄取 API。进一步了解事件 [在此部分中](../event/about-events.md).

* [!DNL Journey Optimizer] 附带内置消息功能：您可以设计内容并发布消息。 如果您使用第三方系统来发送消息，例如Adobe Campaign，请创建 **自定义操作**. 了解有关此中操作的更多信息 [在此部分中](../action/action.md).
