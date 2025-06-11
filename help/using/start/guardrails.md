---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 护栏和限制
description: 详细了解 Journey Optimizer 护栏
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 284c4896b923eac1d360b61d97cbe560d747ea4f
workflow-type: tm+mt
source-wordcount: '2513'
ht-degree: 98%

---

# 护栏和限制 {#limitations}

下文中介绍了使用 [!DNL Adobe Journey Optimizer] 时的额外护栏和限制。

[Adobe Journey Optimizer 产品说明页面](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}列出了授权、产品限制和性能护栏。


>[!CAUTION]
>
>* 实时客户配置文件数据和分段的[护栏](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/guardrails){target="_blank"}也适用于Adobe Journey Optimizer。
>
>* 另请参阅[实时客户资料中的数据摄取护栏](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ingestion/guardrails){target="_blank"}


## 支持的浏览器 {#browsers}

Adobe [!DNL Journey Optimizer] 界面设计为可在最新版 Google Chrome 中发挥最佳表现。在旧版本或其他浏览器上使用某些功能时可能会遇到问题。

## 数据集护栏 {#datasets-guardrails}

从 2025 年 2 月起，已在&#x200B;**新沙盒和新组织**&#x200B;中推出用于 Journey Optimizer 系统生成的数据集的生存时间 (TTL) 护栏，如下所示：

* 配置文件存储中的数据为 90 天，
* 数据湖中的数据为 13 个月。

此更改将在后续阶段推广到&#x200B;**现有的客户沙盒**。[了解有关数据集生存时间 (TTL) 护栏的更多信息](../data/datasets-ttl.md)

## 渠道护栏 {#channel-guardrails}

>[!NOTE]
>
>在极少数情况下，特定区域的临时故障可能会导致从历程中排除有效的用户档案，或导致邮件被错误标记为退回。恢复服务后，重新检查历程日志，验证同意用户档案字段，并根据需要重新发布历程。如果 ISP 中断，请参阅[本部分](../configuration/manage-suppression-list.md#remove-from-suppression-list)，了解如何从禁止列表中移除用户档案。
>

### 电子邮件护栏 {#message-guardrails}

以下护栏适用于[电子邮件渠道](../email/get-started-email.md)：

* 无法使用 [!DNL Journey Optimizer] 向电子邮件添加附件。
* 无法使用相同的发送域从 [!DNL Adobe Journey Optimizer] 和其他产品（例如 [!DNL Adobe Campaign] 或 [!DNL Adobe Marketo Engage]）发送消息。

### 短信护栏 {#sms-guardrails}

以下护栏适用于[短信渠道](../sms/get-started-sms.md)：

* 可以通过支持的 URL 加入 MMS 的媒体文件。请确保单独上传媒体文件。
* 消息反馈同步当前不适用于 MMS。
* 同意管理在 MMS 的短信渠道级别运行。

### Web 渠道护栏 {#web-guardrails}

[!DNL Journey Optimizer] [Web 营销活动](../web/get-started-web.md)针对的是以前在其他渠道上没有联系过的新用户档案。这将增加符合资格的轮廓总数，如果超出您购买的符合资格的轮廓的合同数量，则可能会对成本产生影响。

[Journey Optimizer 产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}页面上列出了每个包的许可证指标。

### 基于代码的渠道护栏 {#code-based-guardrails}

要在 [!DNL Journey Optimizer] 中使用基于代码的体验操作，并交付应用程序可以使用的代码内容负载，请遵守[此页面](../code-based/code-based-prerequisites.md)中详述的先决条件。

## 登陆页面护栏 {#lp-guardrails}

以下护栏适用于[登录页面](../landing-pages/get-started-lp.md)：

* 在单个主页面中只能使用一个&#x200B;**表单**&#x200B;组件。
* 无法在子页面中使用&#x200B;**表单**&#x200B;组件。
* 无法向登陆页添加预编译标头。
* 设计主登录页面时，无法选择&#x200B;**自己编写代码**&#x200B;选项。

## 子域护栏 {#subdomain-guardrails}

默认情况下，[!DNL Journey Optimizer] 允许您总共委派最多 10 个子域（包括电子邮件和 Web 渠道）。

但是，根据您的许可合同，您最多可以委派 100 个子域。请联系您的 Adobe 联系人，以进一步了解您有权使用的子域数量。

要了解有关域委派的更多信息，请参阅[此页面](../configuration/delegate-subdomain.md)。

## 片段护栏 {#fragments-guardrails}

以下护栏适用于[片段](../content-management/fragments.md)：

* 可视化片段仅适用于电子邮件渠道。
* 表达式片段不适用于应用程序内渠道。

## 受众护栏 {#audience}

您最多可以在给定沙盒中发布 10 个受众构成。如果您已达到此阈值，则需要删除组合以释放空间，然后才能发布新组合。

要了解有关受众构成的更多信息，请参阅[此页面](../audience/get-started-audience-orchestration.md)。

## Decisioning 和决策管理护栏 {#decisioning-guardrails}

有关使用 Decisioning 或决策管理时要牢记的护栏和限制，请参阅以下 Decisioning 和决策管理部分：

* [决策护栏和限制](../experience-decisioning/decisioning-guardrails.md)
* [决策管理护栏和限制](../offers/decision-management-guardrails.md)


## 历程护栏 {#journeys-guardrails}

### 一般历程护栏 {#journeys-guardrails-journeys}

* 历程中的活动数量限制为 50 个。活动数显示在历程画布的左上角部分。这有益于可读性、进行 QA 检查和故障排除。
* 当您发布历程时，我们会自动进行缩放和调整，确保最大吞吐量和稳定性。当您接近达成 100 个实时历程的里程碑时，将在 UI 中收到有关此成就的通知。如果您看到此通知，并且需要将每次的历程扩展到多于 100 个实时历程，请创建客户关怀支持工单，我们将帮助您实现目标。
  <!-- DOCAC-10977 * As you publish journeys, we automatically scale and adjust to ensure maximum throughput and stability. As you near the milestone of 500 live journeys at one time, you will see a notification appear in the UI on this achievement. If you see this notification and have a need to extend your journeys beyond 500 live journeys at a time, please create a ticket for customer care and we will help you reach your goals.-->
* 在历程中使用受众资格筛选时，该受众资格活动可能最多需要 10 分钟才能生效，并侦听进入或退出受众的轮廓。
* 轮廓的历程实例的最大大小为 1MB。在历程执行过程中收集的所有数据都存储在该历程实例中。因此，来自传入事件的数据、从 Adobe Experience Platform 检索的轮廓信息、自定义操作响应等都会存储在历程实例中并影响历程大小。当历程以事件开始时，建议限制该事件负载的最大大小（例如：小于 800 KB），以避免在历程执行过程中完成少数几个活动后就达到该限制。当达到该限制时，轮廓会处于错误状态并被从历程中排除。
* 除了历程活动中使用的超时之外，还有未显示在界面中且无法更改的全局历程超时。此全局超时会在个人进入历程 91 天后停止个人进度。[了解详情](../building-journeys/journey-properties.md#global_timeout)

### 常规操作 {#general-actions-g}

以下护栏适用于历程中的[操作](../building-journeys/about-journey-activities.md)：

* 如果出现错误，系统将执行三次重试。无法根据收到的错误消息调整重试次数。对 HTTP 401、403 和 404 以外的所有 HTTP 错误执行重试。
* 使用内置的&#x200B;**反应**&#x200B;事件，可对开箱即用的操作做出反应。请参阅[此页面](../building-journeys/reaction-events.md)以了解详情。如果要对通过自定义操作发送的消息做出反应，则必须配置专用事件。
* 无法同时设置两个操作，必须先添加一个，然后再添加另一个操作。
* 对于所有有效的[历程版本](../building-journeys/publishing-the-journey.md#create-a-new-version-of-a-journey-journey-create-new-version)，一个轮廓不能在同一历程中同时多次出现。如果启用了重新进入，则用户档案可以重新进入历程，但只有在完全退出该历程的上一个实例后才能重新进入历程。[了解详情](../building-journeys/end-journey.md)

### 历程版本 {#journey-versions-g}

以下护栏适用于[历程版本](../start/user-interface.md)：

* v1 中以事件活动开始的历程，在后续版本中无法以事件之外的其他内容开始。无法从&#x200B;**受众资格筛选**&#x200B;事件开始历程。
* v1 中从&#x200B;**受众资格筛选**&#x200B;活动开始的历程在后续版本中必须始终从&#x200B;**受众资格筛选**&#x200B;开始。
* 无法在新版本中更改在&#x200B;**受众资格筛选** （第一个节点）中选择的受众和命名空间。
* 在所有历程版本中，重新进入规则必须相同。
* 从&#x200B;**读取受众**&#x200B;开始的历程，在后续版本中无法从其他事件开始。
* 您无法创建具有增量读取的读取受众历程的新版本。您必须复制历程。

### 自定义操作 {#custom-actions-g}

以下护栏适用于历程中的[自定义操作](../action/action.md)：

* 为所有自定义操作、每个主机和每个沙盒定义了 1 分钟内 300,000 次调用的上限。请参见[此页面](../action/about-custom-action-configuration.md)。此限制是根据客户使用情况设置的，用于保护自定义操作所针对的外部端点。您必须在基于受众的历程中考虑这一点，相应地定义适当的读取率（使用自定义操作时为 5,000 个用户档案/秒）。如果需要，您可以通过我们的“上限/限制 API”定义较大的上限或限制来覆盖此设置。请参阅[此页](../configuration/external-systems.md)。
* 自定义操作 URL 不支持动态参数。
* 支持 POST、PUT 和 GET 调用方法
* 查询参数或标头的名称不得以“.”或“$”开始
* 不允许使用 IP 地址
* URL 和 API 不支持 Adobe 内部地址 (`.adobe.*`)。
* 无法移除内置的自定义操作。
* 仅当使用请求或响应负载时，自定义操作才支持 JSON 格式。请参阅[此页](../action/about-custom-action-configuration.md#custom-actions-limitations)。
* 在使用自定义操作选择要锁定的端点时，请确保：

   * 可以使用 [API 限制](../configuration/throttling.md) 或 [API 上限](../configuration/capping.md)的配置对此端点进行限制，从而支持历程的吞吐量。请注意，限制配置不能低于 200 TPS。任何目标端点都必须支持至少 200 TPS。
   * 此端点的响应时间需要尽可能短。根据预期吞吐量，高响应时间可能会影响实际吞吐量。

### 活动 {#events-g}

以下护栏适用于历程中的[事件](../event/about-events.md)：

* Journey Optimizer 支持的的峰值流量可达每秒 5,000 个入站历程。
* 事件触发的历程可能最多需要 5 分钟才能处理历程中的第一个操作。
* 对于系统生成的事件，必须先在 Journey Optimizer 中配置用于启动客户历程的流数据，才能获取唯一的编排 ID。此编排 ID 必须附加到传入 Adobe Experience Platform 的流有效负载中。此限制不适用于基于规则的事件。
* 业务事件无法与单一事件或受众资格筛选活动结合使用。
* 单一历程（以事件或受众资格筛选开始）包含护栏，可防止同一事件多次错误触发历程。默认情况下，会在 5 分钟内暂时阻止用户档案重新进入。例如，如果某个事件在 12:01 触发某个特定用户档案的历程，而另一个事件在 12:03 到达（无论是同一事件还是其他事件触发同一历程），则对于此用户档案，该历程将不会重新开始。
* Journey Optimizer 要求将事件流式传输到数据收集核心服务 (DCCS) 才能触发历程。无法使用批量摄取的事件或来自内部 Journey Optimizer 数据集（消息反馈、电子邮件跟踪等）的事件来触发历程。对于无法获取流式处理事件的用例，您必须根据这些事件构建一个受众，然后使用&#x200B;**读取受众**&#x200B;活动。从技术上讲，可以使用受众资格筛选，但不建议这么做，因为这可能会导致下游挑战，具体取决于所使用的操作。

### 数据源 {#data-sources-g}

以下护栏适用于历程中的[数据源](../datasource/about-data-sources.md)：

* 可在客户历程中利用外部数据源，以实时查找外部数据。这些源必须可通过 REST API 使用，支持 JSON，并能够处理大量请求。
* URL 和 API 不支持 Adobe 内部地址 (`.adobe.*`)。

>[!NOTE]
>
>由于现在支持响应，因此您应该对外部数据源用例使用自定义操作而不是数据源。

### 历程和轮廓创建 {#journeys-limitation-profile-creation}

在 Adobe Experience Platform 中，创建/更新基于 API 的轮廓存在延迟。延迟方面的服务水平目标 (SLT) 是在每秒请求量 (RPS) 为 20K 的情况下，从摄取到统一轮廓的第 95% 的请求的延迟小于 1 分钟。

如果在创建轮廓的同时触发了历程，并立即检查/检索轮廓服务中的信息，则该历程可能无法正常工作。

您可以从以下两种解决方案中选择一种：

* 在第一个事件后添加等待活动，以便给 Adobe Experience Platform 提供向轮廓服务执行摄取所需的时间。

* 设置不会立即利用轮廓的历程。例如，如果历程旨在确认帐户创建，则体验事件可能包含发送第一条确认消息（名字、姓氏、电子邮件地址等）所需的信息。

### 更新轮廓 {#update-profile-g}

特定护栏适用于&#x200B;**[!UICONTROL 更新轮廓]**&#x200B;活动。请参见[此页面](../building-journeys/update-profiles.md)中所列。

### 读取受众 {#read-segment-g}

以下护栏适用于[读取受众](../building-journeys/read-audience.md)历程活动：

* 流式处理受众始终会保持更新，但在检索时间中不会考虑批量区段。它们每天仅在每日批量评估时间中进行评估。
* 对于使用&#x200B;**读取受众**&#x200B;活动的历程，可以同时启动的历程数具有上限。系统将重试，但请不要同时启动超过 5 个历程（**读取受众**、计划或“尽快”开始），可以将其分散到不同的时间，例如间隔 5 到 10 分钟。
* **读取受众**&#x200B;活动不能与 Adobe Campaign 活动一起使用。
* **读取受众**&#x200B;活动只能用作历程中的第一个活动，即业务事件活动后的第一个活动。
* 历程只能有一个&#x200B;**读取受众**&#x200B;活动。
* 另请参阅[此页面](../building-journeys/read-audience.md)中有关如何使用&#x200B;**读取受众**&#x200B;活动的建议。
* 在检索导出作业时，重试操作会被默认应用于受众触发的历程（从&#x200B;**读取受众**&#x200B;或&#x200B;**业务事件**&#x200B;开始）。如果在创建导出作业期间发生错误，则每 10 分钟重试一次，最多 1 小时。之后，我们将它视为失败。因此，这些类型的历程可以在预定时间之后 1 小时内执行。

### 受众资格筛选 {#audience-qualif-g}

以下护栏适用于[受众资格筛选](../building-journeys/audience-qualification-events.md)历程活动：

* “受众资格筛选”活动不能与 Adobe Campaign 活动一起使用。

### 表达式编辑器 {#expression-editor}

以下护栏适用于[历程表达式编辑器](../building-journeys/expression/expressionadvanced.md)：

* 以读取受众、受众资格筛选或业务事件活动开始的历程中，无法使用体验事件字段组。您必须创建一个新受众，并在历程中使用`inaudience`条件。
* 不能在表达式编辑器中使用 `timeSeriesEvents` 属性。要在轮廓级别访问体验事件，请基于 `XDM ExperienceEvent` 架构创建新的字段组。


### 应用程序内活动 {#in-app-activity-limitations}

以下护栏适用于&#x200B;**[!UICONTROL 应用程序内消息]**&#x200B;操作。要了解应用程序内消息的更多信息，请参阅[此页面](../in-app/create-in-app.md)。

* 此功能目前不适用于医疗保健客户。

* 个性化只能包含轮廓属性。

* 应用程序内活动不能与 Adobe Campaign 活动一起使用。

* 应用程序内显示与历程生命周期绑定，这意味着当具有相应轮廓的受众的历程结束时，该历程中的所有应用程序内消息将不再会显示给该受众。因此，无法直接从历程活动停止应用程序内消息。相反，您必须结束整个历程以停止向具有相关轮廓的受众显示应用程序内消息。

* 在测试模式下，应用程序内显示取决于历程的有效期。要防止历程在测试期间过早结束，请调整&#x200B;**[!UICONTROL 等待]**&#x200B;活动的&#x200B;**[!UICONTROL 等待时间]**&#x200B;值。

* **[!UICONTROL 反应]**&#x200B;活动无法用于对应用程序内打开或点击作出反应。

* 从用户轮廓到达画布中应用程序内活动到开始看到应用程序内消息之间，可能会发生激活延迟。

* 应用程序内消息内容的大小限制为 2Mb。包含大图像可能会妨碍发布流程。

### 跳转活动 {#jump-g}

特定护栏适用于&#x200B;**[!UICONTROL 跳转]**&#x200B;活动。请参见[此页面](../building-journeys/jump.md#jump-limitations)中所列。

### Campaign 活动 {#ac-g}

以下护栏适用于 **[!UICONTROL Campaign v7/v8]** 和 **[!UICONTROL Campaign Standard]** 活动：

* Adobe Campaign 活动不能与“读取受众”或“受众资格筛选”活动一起使用。
* 营销活动不能与其他渠道活动一起使用：卡片、基于代码的体验、电子邮件、推送、短信、应用程序内消息、Web。
