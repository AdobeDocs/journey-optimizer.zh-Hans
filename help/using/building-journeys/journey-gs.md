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
source-git-commit: 18296fe54dcef6620d4f74374848199368f01475
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 24%

---

# 创建您的第一个历程{#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="创建历程"
>abstract="借助 **Adobe Journey Optimizer**，可以利用存储在事件或数据源中的上下文数据构建实时编排用例。"


## 先决条件{#start-prerequisites}

要通过历程发送消息，需要以下配置：

1. **配置事件**：如果要在收到事件时统一触发历程，则需要配置事件。 您可以定义预期信息及其处理方式。 此步骤由&#x200B;**技术用户**&#x200B;执行。 [了解更多信息](../event/about-events.md)。

   ![](assets/jo-event7bis.png)

1. **创建受众**：您的历程还可以侦听Adobe Experience Platform受众，以便向一组指定的用户档案批量发送消息。 为此，您需要创建受众。 [了解更多信息](../audience/about-audiences.md)。

   ![](assets/segment2.png)

1. **配置数据源**：您可以定义与系统的连接，以检索将在您的历程中使用的其他信息，例如在您的条件中。 在预配时还会配置内置 Adobe Experience Platform 数据源。如果您仅利用历程中事件的数据，则不需要执行此步骤。此步骤由&#x200B;**技术用户**&#x200B;执行。 [了解详情](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **配置操作**：如果您使用第三方系统发送消息，则可以创建自定义操作。 在此[部分](../action/action.md)中了解详情。 此步骤由&#x200B;**技术用户**&#x200B;执行。 如果您使用Journey Optimizer内置消息功能，则只需将渠道操作添加到历程并设计内容即可。

   ![](assets/custom2.png)

## 访问历程 {#journey-access}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="历程"
>abstract="设计客户历程以营造个性化的上下文体验。通过 Journey Optimizer，可用存储在事件或数据源中的上下文数据构建实时编排用例。**概述**&#x200B;选项卡显示一个仪表板，其中包含与您的历程相关的关键量度。**浏览**&#x200B;选项卡显示现有历程的列表。"

### 关键量度和历程列表 {#access-metrics}

在“历程管理”菜单部分中，单击&#x200B;**[!UICONTROL 历程]**。 提供了以下两个选项卡：

**概述**：此选项卡显示一个仪表板，其中包含与您的历程相关的关键量度：

* **已处理的配置文件**：过去24小时内处理的配置文件总数
* **实时历程**：过去24小时内具有流量的实时历程总数。 实时历程包括&#x200B;**单一历程** （基于事件）和&#x200B;**批次历程** （读取受众）。
* **错误率**：所有出错的配置文件与过去24小时内输入的配置文件总数之比。
* **放弃率**：已放弃的所有配置文件与过去24小时内输入的配置文件总数之比。 丢弃的个人资料表示无权进入历程的人，例如，由于命名空间不正确或重入规则所致。

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

从&#x200B;**[!UICONTROL 状态和版本筛选器]**&#x200B;中根据历程的状态、类型、版本和分配的标记筛选历程。

类型可以是： **[!UICONTROL 单一事件]**、**[!UICONTROL 受众资格]**、**[!UICONTROL 读取受众]**&#x200B;或&#x200B;**[!UICONTROL 商业事件]**。

状态可以是：

* **已关闭**：历程已使用&#x200B;**关闭新入口**&#x200B;按钮关闭。 历程停止让新个人进入历程。 已处于历程中的人员可以正常完成历程。
* **草稿**：历程处于第一阶段。 它尚未发布。
* **草稿（测试）**：已使用&#x200B;**测试模式**&#x200B;按钮激活测试模式。
* **已完成**：历程在91天[全局超时](journey-properties.md#global_timeout)后自动切换到此状态。 历程中已有的用户档案通常会完成历程。 新配置文件无法再进入历程。
* **实时**：历程已使用&#x200B;**Publish**&#x200B;按钮发布。
* **已停止**：历程已使用&#x200B;**停止**&#x200B;按钮关闭。 所有个人都会立即退出历程。

>[!NOTE]
>
>历程创作生命周期还包括一组不可过滤的中间状态：“发布”（在“草稿”和“实时”之间）、“激活测试模式”或“停用测试模式”(在“草稿”和“草稿（测试）”之间)以及“停止”（在“实时”和“已停止”之间）。 当历程处于中间状态时，只可读取它。

使用&#x200B;**[!UICONTROL 创建过滤器]**&#x200B;根据历程的创建日期或创建历程的用户来筛选历程。

显示使用&#x200B;**[!UICONTROL 活动筛选器]**&#x200B;和&#x200B;**[!UICONTROL 数据筛选器]**&#x200B;中的特定事件、字段组或操作的历程。

使用&#x200B;**[!UICONTROL 发布筛选器]**&#x200B;选择发布日期或用户。 例如，您可以选择显示昨天发布的最新版实时历程。

要根据特定日期范围筛选历程，请从&#x200B;**[!UICONTROL 已发布]**&#x200B;下拉列表中选择&#x200B;**[!UICONTROL 自定义]**。

此外，在“事件”、“数据源”和“操作”配置窗格中，**[!UICONTROL 用于]**&#x200B;字段显示使用该特定事件、字段组或操作的历程数。 您可以单击&#x200B;**[!UICONTROL 查看历程]**&#x200B;按钮以显示相应历程的列表。

![](assets/journey3bis.png)

## 构建历程 {#jo-build}

设计历程以提供个性化的情境式体验。 [!DNL Journey Optimizer] 使您可以利用存储在事件或数据源中的上下文数据，生成实时编排用例。设计由以下功能提供支持的分步式高级方案：

* 使用 Adobe Experience Platform 受众在接收到事件时触发发送实时&#x200B;**单一投放**，或进行&#x200B;**批量**&#x200B;处理。

* 利用来自事件的&#x200B;**上下文数据**、来自 Adobe Experience Platform 的信息或来自第三方 API 服务的数据。

* 使用&#x200B;**内置渠道操作**（电子邮件、短信、推送和应用程序内消息）发送在 [!DNL Journey Optimizer] 中设计的消息；或者，如果您使用第三方系统，可以创建&#x200B;**自定义操作**&#x200B;来发送消息。

* 使用&#x200B;**历程设计器**，构建分步式用例：轻松地拖放进入事件或读取受众活动、添加条件和发送个性化消息。

➡️ [在视频中了解此功能](journey.md#video)

以下列出了通过历程发送消息的步骤：

1. 在&#x200B;**浏览**&#x200B;选项卡中，单击&#x200B;**[!UICONTROL 创建历程]**&#x200B;以创建新旅程。

1. 编辑右侧显示的配置窗格中的历程属性。在此[此页面](journey-properties.md)中了解如何设置历程的属性。

   ![](assets/jo-properties.png)

1. 首先，将事件或&#x200B;**读取受众**&#x200B;活动从调色板拖放到画布中。 要了解有关历程设计的更多信息，请参阅[此章节](using-the-journey-designer.md)。

   ![](assets/read-segment.png)

1. 拖放个人将执行的后续步骤。 例如，您可以添加一个条件，后跟一个渠道操作。 要了解有关活动的更多信息，请参阅[此章节](using-the-journey-designer.md)。

1. 使用测试用户档案测试您的历程。 在此[部分](testing-the-journey.md)中了解详情

1. Publish您的历程以激活它。 在此[部分](publishing-the-journey.md)中了解详情。

   ![](assets/jo-journeyuc2_32bis.png)

1. 使用专用的报告工具监控您的历程，以衡量历程的有效性。 在此[部分](../reports/live-report.md)中了解详情。

   ![](assets/jo-dynamic_report_journey_12.png)


## 复制历程 {#duplicate-a-journey}

您可以从&#x200B;**浏览**&#x200B;选项卡复制现有历程。 所有对象和设置都将复制到历程副本。

为此，请执行以下步骤：

1. 导航到要复制的历程，单击&#x200B;**更多操作**&#x200B;图标（历程名称旁边的三个圆点）。
1. 选择&#x200B;**复制**。

   ![复制历程](assets/duplicate-jo.png)

1. 输入历程的名称并进行确认。 您还可以在历程属性屏幕中更改名称。 默认情况下，名称设置如下： `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. 将创建新旅程，该旅程可在旅程列表中找到。
