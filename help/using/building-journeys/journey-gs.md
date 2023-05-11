---
solution: Journey Optimizer
product: journey optimizer
title: 创建您的第一个历程
description: 使用 Adobe Journey Optimizer 构建您的首个历程的关键步骤
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 历程，首次，开始，快速入门，区段，事件，操作
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '1512'
ht-degree: 25%

---

# 创建您的第一个历程{#jo-quick-start}

## 先决条件{#start-prerequisites}

要通过历程发送消息，需要以下配置：

1. **配置事件**:如果要在收到事件后一直触发历程，则需要配置事件。 您可以定义预期信息以及处理方式。 此步骤由&#x200B;**技术用户**&#x200B;执行。[了解更多信息](../event/about-events.md)。

   ![](assets/jo-event7bis.png)

1. **创建区段**:您的历程还可以监听Adobe Experience Platform区段，以便将消息批量发送到一组指定的用户档案。 为此，您需要创建区段。 [了解更多信息](../segment/about-segments.md)。

   ![](assets/segment2.png)

1. **配置数据源**:您可以定义与系统的连接，以检索将在您的历程中使用的其他信息，例如在您的条件中。 在预配时还会配置内置 Adobe Experience Platform 数据源。如果您仅利用历程中事件的数据，则不需要执行此步骤。此步骤由&#x200B;**技术用户**&#x200B;执行。[了解详情](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **配置操作**:如果您使用第三方系统发送消息，则可以创建自定义操作。 在中了解详情 [部分](../action/action.md). 此步骤由&#x200B;**技术用户**&#x200B;执行。如果您使用的是Journey Optimizer内置的消息功能，则只需在历程中添加渠道操作并设计内容即可。

   ![](assets/custom2.png)

## 访问历程 {#journey-access}

在“历程管理”菜单部分，单击 **[!UICONTROL 历程]**. 提供了两个选项卡：

**概述**:此选项卡显示包含与您的历程相关关键量度的功能板：

* **处理的用户档案**:过去24小时内处理的用户档案总数
* **实时历程**:过去24小时内具有流量的实时历程总数。 实时历程包括 **单一历程** （基于事件）和 **批量历程** （读取区段）。
* **错误率**:与过去24小时内输入的用户档案总数相比，所有出错用户档案的比率。
* **放弃率**:所有已描述用户档案的比率与过去24小时内输入的用户档案总数的比率。

>[!NOTE]
>
>此仪表板考虑了过去24小时内流量的历程。 仅显示您有权访问的历程。

![](assets/journeys-dashboard.png)

**浏览**:此选项卡显示现有历程的列表。 您可以搜索历程、使用过滤器并对每个元素执行基本操作。 例如，您可以删除项目或制作项目副本。有关更多信息，请参见[此章节](../start/user-interface.md#filter-lists)。

![](assets/journeys-browse.png)

在历程列表中，您可以根据历程的状态、类型和版本从&#x200B;**[!UICONTROL 状态和版本筛选器]**&#x200B;中筛选历程。类型可以是：**[!UICONTROL 单一事件]**、**[!UICONTROL 区段鉴别]**、**[!UICONTROL 读取区段]**、**[!UICONTROL 业务事件]**&#x200B;或&#x200B;**[!UICONTROL 突发]**。

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

此步骤由 **商业用户**. 您可以在此处创建历程。 结合不同的事件、编排和操作活动，构建多步跨渠道方案。

以下是通过历程发送消息的主要步骤：

1. 从 **浏览** ，单击 **[!UICONTROL 创建历程]** 以创建新历程。

1. 编辑右侧显示的配置窗格中的历程属性。在中了解详情 [部分](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. 首先，拖放事件或 **读取区段** 活动。 要了解有关历程设计的更多信息，请参阅 [此部分](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. 拖放个人将遵循的后续步骤。 例如，您可以添加一个条件，后跟一个渠道操作。 要进一步了解活动，请参阅 [此部分](using-the-journey-designer.md).

1. 使用测试用户档案测试您的历程。 在中了解详情 [部分](testing-the-journey.md)

1. 发布历程以激活它。 在中了解详情 [部分](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. 使用专用的报告工具监控您的历程以衡量历程的有效性。 在中了解详情 [部分](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## 定义历程属性 {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="历程属性"
>abstract="此部分显示历程属性。默认情况下，只读参数是隐藏的。可用设置取决于历程的状态、您的权限和产品配置。"

单击右上方的铅笔图标以访问历程的属性。

您可以更改历程名称、添加描述、允许重新进入、选择开始和结束日期，并作为管理员用户定义 **[!UICONTROL 超时和错误]** 持续时间。 您还可以将Adobe Experience Platform统一标记分配给历程。 这样，您就可以轻松地对促销活动进行分类，并改进促销活动列表中的搜索。 [了解如何使用标记](../start/search-filter-categorize.md#tags)

对于实时历程，此屏幕显示发布日期和发布历程的用户名称。

的 **复制技术详细信息** 允许您复制有关历程的技术信息，供支持团队用于进行故障排除。 将复制以下信息：JourneyVersion UID、OrgID、orgName、sandboxName、lastDeployedBy、lastDeployedAt。

![](assets/journey32.png)

### 入口{#entrance}

默认情况下，新历程允许重新进入。 您可以取消选中 **允许重新进入** “一次性”历程的选项，例如，当某人进入商店时，您想提供一次性礼物。

当 **允许重新进入** 选项时， **重新进入等待期** 字段。 使用该字段，您可以定义允许用户档案再次进入单一历程（以事件或区段鉴别开始）之前等待的时间。这可防止同一事件多次错误触发历程。默认情况下，字段设置为 5 分钟。

在 [此部分](entry-management.md).

### 管理访问权限 {#access}

要为历程分配自定义或核心数据使用标签，请单击 **[!UICONTROL 管理访问权限]** 按钮。 [了解有关对象级别访问控制(OLA)的更多信息](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

### 时区和配置文件时区 {#timezone}

在历程级别定义时区。

您可以输入固定时区或使用Adobe Experience Platform配置文件定义历程时区。

如果在Adobe Experience Platform配置文件中定义了时区，则可以在历程中进行检索。

有关时区管理的更多信息，请参阅 [本页](../building-journeys/timezone-management.md).

### 开始和结束日期 {#dates}

您可以定义 **开始日期**. 如果您未指定，则将在发布时自动定义它。

您还可以添加 **结束日期**. 这允许用户档案在到期时自动退出。如果您没有指定结束日期，则配置文件可以一直保留到默认历程超时（通常为30天，使用Healthcare Shield附加组件服务时为7天）。 唯一的例外是重复读取区段历程， **重复时的强制重入** 激活，在下次发生的开始日期结束。

### 历程活动中的超时和错误 {#timeout_and_error}

在编辑操作或条件活动时，您可以定义出现错误或超时的替代路径。 如果查询第三方系统的活动的处理超过了历程属性中定义的超时持续时间(**[!UICONTROL 超时和错误]** 字段)，则将选择第二个路径来执行潜在的回退操作。

授权值介于1到30秒之间。

我们建议您定义一个非常短的 **[!UICONTROL 超时和错误]** 值(例如：响应人员的实时位置)，因为您不能将操作延迟超过几秒钟。 如果您的历程不太时间敏感，您可以使用较长的值为调用的系统提供更多时间以发送有效响应。

历程还使用全局超时。 请参阅 [下一部分](#global_timeout).

### 全局历程超时 {#global_timeout}

除 [超时](#timeout_and_error) 在历程活动中，还存在全局历程超时，该超时未显示在界面中，且无法更改。 此超时将在个人进入后30天停止历程中的进度。 这意味着个人的历程不能持续超过30天。 在30天超时期后，将删除个人数据。 在超时时段结束时仍在历程中流动的个人将被停止，并将其作为报表中的错误考虑在内。

>[!NOTE]
>
>历程不会直接对隐私选择退出、访问或删除请求做出反应。 但是，全局超时可确保个人在任何历程中停留的时间不得超过30天。

由于历程超时30天，因此当不允许历程重新进入时，我们无法确保重新进入阻止的工作时间超过30天。 事实上，由于我们删除了有关在进入历程30天后进入历程的人员的所有信息，因此我们无法知道之前进入的人员，即30天前。

