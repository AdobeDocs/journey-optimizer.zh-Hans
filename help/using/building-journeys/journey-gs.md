---
solution: Journey Optimizer
product: journey optimizer
title: 创建您的第一个历程
description: 使用 Adobe Journey Optimizer 构建您的首个历程的关键步骤
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: 历程，第一，开始，快速入门，受众，事件，操作
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: fec6b15db9f8e6b2a07b55bc9e8fc4d9cb0d73d7
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 22%

---

# 创建您的第一个历程{#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="创建历程"
>abstract="借助 **Adobe Journey Optimizer**，可以利用存储在事件或数据源中的上下文数据构建实时编排用例。"


## 先决条件{#start-prerequisites}

要通过历程发送消息，需要以下配置：

1. **配置事件**：如果您要在收到事件时统一触发历程，则需要配置事件。 您可以定义预期信息及其处理方式。 此步骤由 **技术用户**. [了解详情](../event/about-events.md)。

   ![](assets/jo-event7bis.png)

1. **创建受众**：您的历程还可以侦听Adobe Experience Platform受众，以将消息批量发送到指定的一组用户档案。 为此，您需要创建受众。 [了解详情](../audience/about-audiences.md)。

   ![](assets/segment2.png)

1. **配置数据源**：您可以定义与系统的连接，以检索将在您的历程中使用的其他信息，例如在您的条件中。 在预配时还会配置内置 Adobe Experience Platform 数据源。如果您仅利用历程中事件的数据，则不需要执行此步骤。此步骤由 **技术用户**. [了解详情](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **配置操作**：如果您使用第三方系统来发送消息，则可以创建自定义操作。 在本节中了解详情 [部分](../action/action.md). 此步骤由 **技术用户**. 如果您使用Journey Optimizer内置消息功能，则只需将渠道操作添加到历程并设计内容即可。

   ![](assets/custom2.png)

## 访问历程 {#journey-access}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="历程"
>abstract="设计客户历程以营造个性化的上下文体验。通过 Journey Optimizer，可用存储在事件或数据源中的上下文数据构建实时编排用例。**概述**&#x200B;选项卡显示一个仪表板，其中包含与您的历程相关的关键量度。**浏览**&#x200B;选项卡显示现有历程的列表。"

### 关键量度和历程列表 {#access-metrics}

在历程管理菜单部分，单击 **[!UICONTROL 历程]**. 提供了以下两个选项卡：

**概述**：此选项卡显示一个功能板，其中包含与您的历程相关的关键量度：

* **配置文件已处理**：过去24小时内处理的配置文件总数
* **实时历程**：过去24小时内具有流量的实时历程总数。 实时历程包括 **单一历程** （基于事件）和 **批量历程** （读取受众）。
* **错误率**：所有出错配置文件与过去24小时内输入的总配置文件数的比率。
* **丢弃率**：与过去24小时内输入的配置文件总数相比，已丢弃的所有配置文件的比率。 丢弃的个人资料表示无权进入历程的人，例如，由于命名空间不正确或重入规则所致。

>[!NOTE]
>
>此仪表板会考虑过去24小时内具有流量的历程。 只显示您有权访问的历程。 指标每30分钟刷新一次，并且仅在有新数据可用时刷新。

![](assets/journeys-dashboard.png)

**浏览**：此选项卡显示现有历程的列表。 您可以搜索历程、使用过滤器并对每个元素执行基本操作。 例如，您可以复制或删除项目。 有关更多信息，请参见[此章节](../start/user-interface.md#filter-lists)。

![](assets/journeys-browse.png)

### 筛选历程 {#filter}

在历程列表中，您可以利用各种过滤器来优化历程列表，以提高可读性。

![](assets/filter-journeys.png)

以下是您可以执行的各种筛选操作：

根据历程的状态、类型、版本和分配的标记，从筛选历程 **[!UICONTROL 状态和版本筛选器]**.

类型可以是： **[!UICONTROL 单一事件]**， **[!UICONTROL 受众资格]**， **[!UICONTROL 读取受众]** 或 **[!UICONTROL 业务事件]**.

状态可以是：

* **已关闭**：历程已使用 **对新进入关闭** 按钮。 历程停止让新个人进入历程。 已处于历程中的人员可以正常完成历程。
* **草稿**：历程处于第一个阶段。 它尚未发布。
* **草稿（测试）**：已使用激活测试模式 **测试模式** 按钮。
* **已完成**：历程在91天后自动切换到此状态 [全局超时](journey-properties.md#global_timeout). 历程中已有的用户档案通常会完成历程。 新配置文件无法再进入历程。
* **实时**：历程已使用发布 **Publish** 按钮。
* **已停止**：历程已使用 **停止** 按钮。 所有个人都会立即退出历程。

>[!NOTE]
>
>历程创作生命周期还包括一组不可过滤的中间状态：“发布”（在“草稿”和“实时”之间）、“激活测试模式”或“停用测试模式”(在“草稿”和“草稿（测试）”之间)以及“停止”（在“实时”和“已停止”之间）。 当历程处于中间状态时，只可读取它。

使用 **[!UICONTROL 创建过滤器]** 根据历程的创建日期或创建历程的用户对历程进行筛选。

显示使用来自的特定事件、字段组或操作的历程 **[!UICONTROL 活动过滤器]** 和 **[!UICONTROL 数据过滤器]**.

使用 **[!UICONTROL 发布过滤器]** 以选择发布日期或用户。 例如，您可以选择显示昨天发布的最新版实时历程。

要根据特定日期范围筛选历程，请选择 **[!UICONTROL 自定义]** 从 **[!UICONTROL 已发布]** 下拉列表。

此外，在“事件”、“数据源”和“操作”配置窗格中， **[!UICONTROL 使用位置]** 字段显示使用该特定事件、字段组或操作的历程数。 您可以单击&#x200B;**[!UICONTROL 查看历程]**&#x200B;按钮以显示相应历程的列表。

![](assets/journey3bis.png)

## 构建历程 {#jo-build}

设计历程以提供个性化的情境式体验。 [!DNL Journey Optimizer] 使您可以利用存储在事件或数据源中的上下文数据，生成实时编排用例。设计由以下功能提供支持的分步式高级方案：

* 使用 Adobe Experience Platform 受众在接收到事件时触发发送实时&#x200B;**单一投放**，或进行&#x200B;**批量**&#x200B;处理。

* 利用来自事件的&#x200B;**上下文数据**、来自 Adobe Experience Platform 的信息或来自第三方 API 服务的数据。

* 使用 **内置渠道操作** （电子邮件、短信、推送、InApp）发送在中设计的消息 [!DNL Journey Optimizer] 或创建 **自定义操作** 如果您使用第三方系统来发送消息。

* 使用&#x200B;**历程设计器**，构建分步式用例：轻松地拖放进入事件或读取受众活动、添加条件和发送个性化消息。

➡️ [在视频中了解此功能](journey.md#video)

以下列出了通过历程发送消息的步骤。

1. 从 **浏览** 选项卡，单击 **[!UICONTROL 创建历程]** 以创建新旅程。

1. 编辑右侧显示的配置窗格中的历程属性。了解如何在此设置您的历程属性 [此页面](journey-properties.md).

   ![](assets/jo-properties.png)

1. 从拖放事件或 **读取受众** 活动从面板移入画布。 要了解有关历程设计的更多信息，请参阅 [本节](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. 拖放个人将执行的后续步骤。 例如，您可以添加一个条件，后跟一个渠道操作。 要了解有关活动的更多信息，请参阅 [本节](using-the-journey-designer.md).

1. 使用测试用户档案测试您的历程。 在本节中了解详情 [部分](testing-the-journey.md)

1. 发布您的历程以激活它。 在本节中了解详情 [部分](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. 使用专用的报告工具监控您的历程，以衡量历程的有效性。 在本节中了解详情 [部分](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)


## 复制历程 {#duplicate-a-journey}

您可以从以下位置复制现有历程 **浏览** 选项卡。 所有对象和设置都将复制到历程副本。

为此，请执行以下步骤：

1. 导航到要复制的历程，单击 **更多操作** 图标（历程名称旁边的三个点）。
1. 选择&#x200B;**复制**。

   ![复制历程](assets/duplicate-jo.png)

1. 输入历程的名称并进行确认。 您还可以在历程属性屏幕中更改名称。 默认情况下，名称设置如下： `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. 将创建新旅程，该旅程可在旅程列表中找到。
