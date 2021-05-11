---
title: 旅程入门
description: 旅程入门
translation-type: tm+mt
source-git-commit: 0b48a0b0793d523021a2e19f86e101bdbab88305
workflow-type: tm+mt
source-wordcount: '1464'
ht-degree: 7%

---

# 开始使用journeys{#jo-quick-start}

![](../assets/do-not-localize/badge.png)

## 先决条件

要随旅程发送消息，需要以下配置：

1. **配置事件**:如果要在收到事件时一直触发旅程，则需要配置事件。您可以定义预期的信息以及如何处理它。 此步骤由&#x200B;**技术用户**&#x200B;执行。[了解更多信息](../event/about-events.md).

   ![](../assets/jo-event7.png)

1. **创建区段**:您的旅程还可以侦听Adobe Experience Platform区段，以便将消息批量发送到指定的一组用户档案。为此，您需要创建区段。 [了解更多信息](../segment/about-segments.md).

   ![](../assets/segment2.png)

1. **配置数据源**:您可以定义到系统的连接，以检索将在您的旅程中使用的其他信息，例如在您的条件中。在预配时还会配置内置 Adobe Experience Platform 数据源。如果您仅利用历程中事件的数据，则不需要执行此步骤。此步骤由&#x200B;**技术用户**&#x200B;执行。[了解更多信息](../datasource/about-data-sources.md)

   ![](../assets/jo-datasource.png)

1. **配置操作**:Journey Optimizer消息功能是内置的，您只需要设计内容并发布消息。请参阅[此小节](../get-started-content.md)。如果您使用第三方系统发送消息，则可以创建自定义操作。 请阅读此[部分](../action/action.md)了解更多信息。 此步骤由&#x200B;**技术用户**&#x200B;执行。

   ![](../assets/create-content-push.png)

## 构建您的旅程{#jo-build}

此步骤由&#x200B;**业务用户**&#x200B;执行。 这是您创造旅程的地方。 结合不同的事件、编排和操作活动，构建多步跨渠道方案。

以下是在旅程中发送消息的主要步骤：

1. 在左侧菜单中，单击&#x200B;**[!UICONTROL Journeys]**。 将显示旅程列表。

   ![](../assets/interface-journeys.png)

1. 单击&#x200B;**[!UICONTROL Create]**&#x200B;以创建新旅程。

1. 编辑右侧显示的配置窗格中的历程属性。请阅读此[部分](journey-gs.md#change-properties)了解更多信息。

   ![](../assets/jo-properties.png)

1. 开始，方法是将事件或&#x200B;**从调色板中读取段**&#x200B;活动拖放到画布中。 要了解有关旅程设计的更多信息，请参阅[此部分](using-the-journey-designer.md)。

   ![](../assets/read-segment.png)

1. 拖放个人将遵循的后续步骤。 例如，可添加一个条件，后跟一条消息。 要了解有关活动的更多信息，请参阅[本节](using-the-journey-designer.md)。

1. 使用测试用户档案测试您的旅程。 在此[部分](testing-the-journey.md)中了解更多信息

1. 发布您的旅程以激活它。 请阅读此[部分](publishing-the-journey.md)了解更多信息。

   ![](../assets/jo-journeyuc2_32bis.png)

1. 使用专用的报告工具监控您的旅程，以衡量您的旅程的有效性。 请阅读此[部分](../reports/live-report.md)了解更多信息。

   ![](../assets/jo-dynamic_report_journey_12.png)

## 更改属性 {#change-properties}

单击右上角的铅笔图标以访问旅程的属性。

您可以更改旅程名称、添加描述、允许重新进入、选择开始和结束日期，并定义&#x200B;**[!UICONTROL Timeout and error]**&#x200B;持续时间（如果您是管理员）。

**复制技术详细信息**&#x200B;允许您复制支持团队可用来进行故障诊断的旅程的技术信息。 将复制以下信息：JourneyVersion UID、OrgID、orgName、sandboxName。

![](../assets/journey32.png)

### 入口{#entrance}

默认情况下，新旅程允许重新进入。 您可以取消选中“一次性”旅程选项，例如，当某人进入商店时，您要优惠一次性馈赠。 在这种情况下，您不希望客户能够重新进入旅程并再次接收优惠。

当旅程“结束”时，其状态为&#x200B;**[!UICONTROL Closed (no entrance)]**。 这一旅程将不再让新人进入旅程。 已经在旅程中的人将正常完成旅程。

在默认全局超时30天后，旅程将切换到&#x200B;**已完成**&#x200B;状态。 请参阅此[部分](../building-journeys/journey-gs.md#global_timeout)。

### 旅程活动{#timeout_and_error}中的超时和错误

在编辑操作或条件活动时，您可以在出现错误或超时时定义替代路径。 如果询问第三方系统的活动的处理超过了在旅程的属性（**[!UICONTROL Timeout and  error]**&#x200B;字段）中定义的超时持续时间，则将选择第二路径以执行潜在的回退操作。

授权值介于1到30秒之间。

如果您的旅程是时间敏感型的(例如：对人的实时位置做出响应)，因为您不能将您的动作延迟超过几秒钟。 **[!UICONTROL Timeout and error]**&#x200B;如果您的旅程对时间不太敏感，则可以使用一个较长的值为调用的系统提供更多时间以发送有效响应。

历程还使用全局超时。 请参见[下一节](#global_timeout)。

### 全局旅程超时{#global_timeout}

除了在旅程活动中使用的[timeout](#timeout_and_error)之外，还存在全局旅程超时，该超时不会显示在接口中，并且无法更改。 此超时将在个人进入后30天内停止其在旅程中的进度。 这意味着个人的旅程不能持续超过30天。 在30天超时期后，将删除个人的数据。 在超时期结束时仍在旅程中流动的个人将被停止，并将其作为报告中的错误予以考虑。

>[!NOTE]
>
>历程不会对隐私选择退出、访问或删除请求做出直接反应。 但是，全局超时可确保个人在任何旅程中停留30天以上。

由于30天的旅程超时，当不允许重新进入旅程时，我们无法确保重新进入的阻塞超过30天。 事实上，由于我们删除了有关在进入旅程30天后进入旅程的人员的所有信息，因此我们无法知道之前输入的人员，超过30天前。

### 时区和用户档案时区{#timezone}

时区在旅程级别定义。

您可以输入固定时区或使用Adobe Experience Platform用户档案定义旅程时区。

有关时区管理的详细信息，请参阅[此页](../building-journeys/timezone-management.md)。

## 结束旅程

一个旅程可能会因个人而结束，原因有二：

* 那人到达了路的最后活动。 最后一个活动可以是结束活动或其他活动。 没有义务用结束活动结束路径。 请参阅[此页](../building-journeys/end-activity.md)。
* 该人到达条件活动(或具有条件的等待活动)，并且不符合任何条件。

如果允许重新进入，则人员随后可以重新进入旅程。 请参阅[此页](../building-journeys/journey-gs.md#change-properties)

由于以下原因，旅程可能会结束：

* 通过&#x200B;**[!UICONTROL Close to new entrances]**&#x200B;按钮手动关闭旅程。
* 已完成执行的基于一次性片段的旅程。
* 上次出现基于区段的定期旅程后。

当旅程关闭时（出于上述任何原因），其状态将为&#x200B;**[!UICONTROL Closed (no entrance)]**。 这一旅程将不再让新人进入旅程。 已经在旅程中的人将正常完成旅程。 在默认全局超时30天后，旅程将切换到&#x200B;**已完成**&#x200B;状态。 请参阅此[部分](../building-journeys/journey-gs.md#global_timeout)。

如果您需要阻止旅程中所有个人的进步，您可以阻止它。 停止旅程将超时旅程中的所有个人。

下面是您如何手动关闭或停止旅程：

使用&#x200B;**[!UICONTROL Stop]**&#x200B;和&#x200B;**[!UICONTROL Close to new entrances]**&#x200B;选项可以终止&#x200B;**实时**&#x200B;旅程。 结束旅程需要&#x200B;**阻止新客户进入旅程**，并且已进入旅程的客户能够体验到旅程结束。 这是结束旅程的最推荐方式，因为它优惠了最佳客户体验。 阻止旅程意味着已经进入旅程的人都被阻止。 旅程基本上被关闭。

>[!NOTE]
>
>请注意，您无法恢复已关闭或已停止的旅程。

### 结束旅程

您可以手动结束旅程，以确保已进入旅程的客户能够完成其旅程，但新用户无法进入旅程。

结束后，旅程将具有&#x200B;**[!UICONTROL Closed (no entrance)]**&#x200B;状态。 在默认全局超时30天后，旅程将切换到&#x200B;**已完成**&#x200B;状态。 请参阅此[部分](../building-journeys/journey-gs.md#global_timeout)。

无法重新启动或删除已关闭的旅程版本。 您可以创建新版本或将其重复。 只能删除已完成的旅程。

在旅程列表中悬停某个旅程时，单击&#x200B;**[!UICONTROL Close to new entrances]**&#x200B;即可关闭该旅程。

![](../assets/do-not-localize/journey-finish-quick-action.png)

您还可以：

1. 在&#x200B;**[!UICONTROL Journeys]**&#x200B;列表中，单击要关闭的旅程。
1. 在右上角，单击向下箭头。

   ![](../assets/finish_drop_down_list.png)

1. 单击 **[!UICONTROL Close to new entrances]**。将显示一个对话框。
1. 单击&#x200B;**[!UICONTROL Close to new entrances]**&#x200B;进行确认。

### 停止旅程

当出现紧急情况且所有处理需要在旅程中立即结束时，您可以停止旅程。

无法重新启动已停止的旅程版本。

停止时，旅程将具有&#x200B;**[!UICONTROL Stopped]**&#x200B;状态。

在旅程列表中悬停一段旅程时，单击&#x200B;**[!UICONTROL Stop]**，即可停止一段旅程(例如，当营销人员意识到旅程目标错误的受众或应用于传送消息的自定义操作无法正确运行时)。

![](../assets/do-not-localize/journey-stop-quick-action.png)

您还可以：

1. 在&#x200B;**[!UICONTROL Journeys]**&#x200B;列表中，单击要停止的旅程。
1. 在右上角，单击向下箭头。

![](../assets/finish_drop_down_list.png)

1. 单击 **[!UICONTROL Stop]**。将显示一个对话框。
1. 单击&#x200B;**[!UICONTROL Stop]**&#x200B;进行确认。
