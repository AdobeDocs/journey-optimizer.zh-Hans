---
solution: Journey Optimizer
product: journey optimizer
title: 创建您的第一个历程
description: 使用 Adobe Journey Optimizer 构建您的首个历程的关键步骤
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 历程，第一，开始，快速入门，受众，事件，操作
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 523f38743a827db4f8a94430ef02eda78d4151d9
workflow-type: tm+mt
source-wordcount: '1710'
ht-degree: 25%

---

# 创建您的第一个历程{#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="创建历程"
>abstract="借助 **Adobe Journey Optimizer**，可以利用存储在事件或数据源中的上下文数据构建实时编排用例。"

## 先决条件{#start-prerequisites}

要通过历程发送消息，需要以下配置：

1. **配置事件**：如果您要在收到事件时统一触发历程，则需要配置事件。 您可以定义预期信息及其处理方式。 此步骤由&#x200B;**技术用户**&#x200B;执行。[了解更多信息](../event/about-events.md)。

   ![](assets/jo-event7bis.png)

1. **创建受众**：您的历程还可以侦听Adobe Experience Platform受众，以将消息批量发送到指定的一组用户档案。 为此，您需要创建受众。 [了解更多信息](../audience/about-audiences.md)。

   ![](assets/segment2.png)

1. **配置数据源**：您可以定义与系统的连接，以检索将在您的历程中使用的其他信息，例如在您的条件中。 在预配时还会配置内置 Adobe Experience Platform 数据源。如果您仅利用历程中事件的数据，则不需要执行此步骤。此步骤由&#x200B;**技术用户**&#x200B;执行。[了解详情](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **配置操作**：如果您使用第三方系统来发送消息，则可以创建自定义操作。 在本节中了解详情 [部分](../action/action.md). 此步骤由&#x200B;**技术用户**&#x200B;执行。如果您使用Journey Optimizer内置消息功能，则只需将渠道操作添加到历程并设计内容即可。

   ![](assets/custom2.png)

## 访问历程 {#journey-access}

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

**浏览**：此选项卡显示现有历程的列表。 您可以搜索历程、使用过滤器并对每个元素执行基本操作。 例如，您可以删除项目或制作项目副本。有关更多信息，请参见[此章节](../start/user-interface.md#filter-lists)。

![](assets/journeys-browse.png)

在历程列表中，您可以根据历程的状态、类型和版本从&#x200B;**[!UICONTROL 状态和版本筛选器]**&#x200B;中筛选历程。类型可以是： **[!UICONTROL 单一事件]**， **[!UICONTROL 受众资格]**， **[!UICONTROL 读取受众]**， **[!UICONTROL 业务事件]** 或 **[!UICONTROL 突发]**.

您可以从&#x200B;**[!UICONTROL 活动过滤器]**&#x200B;和&#x200B;**[!UICONTROL 数据过滤器]**&#x200B;中选择仅显示使用特定事件、字段组或操作的历程。此外， **[!UICONTROL 发布过滤器]** 允许您选择发布日期或用户。 例如，您可以选择显示昨天发布的最新版实时历程。[了解详情](../building-journeys/using-the-journey-designer.md)。

![](assets/filter-journeys.png)

使用&#x200B;**[!UICONTROL 上次更新]**&#x200B;和&#x200B;**[!UICONTROL 上次更新者]**&#x200B;列检查历程的上次更新时间以及保存该更新的人员。

在“事件”、“数据源”和“操作”配置窗格中，**[!UICONTROL 使用位置]**&#x200B;字段显示使用该特定事件、字段组或操作的历程数。您可以单击&#x200B;**[!UICONTROL 查看历程]**&#x200B;按钮以显示相应历程的列表。

![](assets/journey3bis.png)

## 构建历程{#jo-build}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="构建历程"
>abstract="此屏幕显示现有历程的列表。打开某个历程或单击“创建历程”，然后组合不同的事件、编排和操作活动，以此来构建您的多步骤跨渠道场景。"

此步骤由 **商业用户**. 这是创建历程的位置。 结合不同的事件、编排和操作活动，构建多步跨渠道方案。

以下是通过历程发送消息的主要步骤：

1. 从 **浏览** 选项卡，单击 **[!UICONTROL 创建历程]** 以创建新旅程。

1. 编辑右侧显示的配置窗格中的历程属性。在本节中了解详情 [部分](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. 从拖放事件或 **读取受众** 活动从面板移入画布。 要了解有关历程设计的更多信息，请参阅 [本节](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. 拖放个人将执行的后续步骤。 例如，您可以添加一个条件，后跟一个渠道操作。 要了解有关活动的更多信息，请参阅 [本节](using-the-journey-designer.md).

1. 使用测试用户档案测试您的历程。 在本节中了解详情 [部分](testing-the-journey.md)

1. 发布您的历程以激活它。 在本节中了解详情 [部分](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. 使用专用的报告工具监控您的历程，以衡量历程的有效性。 在本节中了解详情 [部分](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## 定义您的历程属性 {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="历程属性"
>abstract="此部分显示历程属性。默认情况下，只读参数是隐藏的。可用设置取决于历程的状态、您的权限和产品配置。"

单击右上角的铅笔图标可访问历程的属性。

您可以更改历程的名称、添加描述、允许重新进入、选择开始和结束日期，以及作为管理员用户定义 **[!UICONTROL 超时和错误]** 持续时间。 您还可以将Adobe Experience Platform统一标记分配给旅程。 这样，您就可以轻松地对营销活动进行分类，并改进营销活动列表中的搜索。[了解如何使用标记](../start/search-filter-categorize.md#tags)

对于实时历程，此屏幕显示发布日期和发布历程的用户名称。

此 **复制技术详细信息** 允许您复制有关历程的技术信息，供支持团队用于进行故障排除。 复制了以下信息：JourneyVersion UID、OrgID、orgName、sandboxName、lastDeployedBy、lastDeployedAt。

![](assets/journey32.png)

### 进入和重新进入 {#entrance}

默认情况下，新历程允许重新进入。 您可以取消选中 **允许重新进入** “一次性”旅程选项，例如，如果您想在某人进入商店时提供一次性礼物。

当 **允许重新进入** 选项已激活， **重新进入等待期** 字段。 使用该字段，您可以定义允许用户档案再次进入单一历程（以事件或受众鉴别开始）之前等待的时间。这可防止同一事件多次错误触发历程。默认情况下，字段设置为 5 分钟。

在中了解有关用户档案进入和重入管理的更多信息 [本节](entry-management.md).

### 管理访问权限 {#access}

要将自定义或核心数据使用标签分配给历程，请单击 **[!UICONTROL 管理访问权限]** 按钮。 [了解有关对象级访问控制(OLA)的更多信息](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

### 时区和配置文件时区 {#timezone}

时区在历程级别定义。

您可以输入固定时区，或使用Adobe Experience Platform配置文件定义历程时区。

如果在Adobe Experience Platform配置文件中定义了时区，则可以在旅程中检索该时区。

有关时区管理的更多信息，请参阅 [此页面](../building-journeys/timezone-management.md).

### 开始和结束日期 {#dates}

您可以定义 **开始日期**. 如果您尚未指定名称，则将在发布时自动定义它。

您还可以添加 **结束日期**. 这允许用户档案在到期时自动退出。如果不指定结束日期，配置文件可以保留到默认历程超时（通常30天，Healthcare Shield附加产品为7天）为止。 唯一的例外是具有以下特征的定期读取受众历程 **在重复时强制重新进入** 激活，在下一次事件的开始日期结束。

### 历程活动中的超时和错误 {#timeout_and_error}

编辑操作或条件活动时，您可以定义替代路径以防出现错误或超时。 如果处理询问第三方系统的活动超出了历程属性中定义的超时持续时间(**[!UICONTROL 超时和错误]** 字段)，将选择第二条路径来执行潜在的回退操作。

授权值介于1和30秒之间。

我们建议您定义一个非常短的 **[!UICONTROL 超时和错误]** 值(如果您的旅程对时间敏感（例如：对人员的实时位置做出反应），因为您的操作不能延迟超过几秒钟。 如果您的旅程不太时效性，则可以使用较长的值，为调用的系统留出更多时间来发送有效响应。

历程还会使用全局超时。 请参阅 [下一节](#global_timeout).

### 全局历程超时 {#global_timeout}

除了 [timeout](#timeout_and_error) 在历程活动中使用，还有一个全局历程超时，该超时未显示在界面中并且无法更改。 此超时将在个人进入历程30天后停止个人进度。 这意味着个人的历程不能超过30天。 在30天超时之后，将删除个人的数据。 超时时间结束时仍在历程中流动的个人将被停止，并且不会在报表中考虑他们。 因此，您可能会看到进入历程的人员多于退出的人员。

>[!NOTE]
>
>历程不会直接对隐私选择退出、访问或删除请求做出反应。 但是，全局超时可确保个人在任何历程中的停留时间不超过30天。

由于30天历程超时，当历程不允许重新进入时，我们无法确保重新进入阻止将工作超过30天。 事实上，当我们删除有关进入旅程30天后进入旅程的人员的所有信息时，我们无法知道该人员是超过30天前进入的。

仅当个人在历程中剩余的时间足以在30天历程超时前完成等待持续时间时，他或她才能进入等待活动。 请参阅[此页](../building-journeys/wait-activity.md)。

## 复制历程 {#duplicate-a-journey}

您可以从以下位置复制现有历程 **浏览** 选项卡。 所有对象和设置都将复制到历程副本。

为此，请执行以下步骤：

1. 导航到要复制的历程，单击 **更多操作** 图标（历程名称旁边的三个点）。
1. 选择&#x200B;**复制**。

   ![复制历程](assets/duplicate-jo.png)

1. 输入历程的名称并进行确认。 您还可以在历程属性屏幕中更改名称。 默认情况下，名称设置如下： `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. 将创建新旅程，该旅程可在旅程列表中找到。
