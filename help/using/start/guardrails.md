---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 护栏和限制
description: 详细了解 Journey Optimizer 护栏
feature: Guardrails
role: User
level: Intermediate
mini-toc-levels: 2
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
TQID: https://experienceleague.adobe.com/k4DqGogrTZ9QrnqyFGwdgDeUI9ivpOd1iSI0c5comuU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
subfeature_v2:
  - id: a6c67b0d-bd3e-4d5d-95a8-882e3709d632
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 4655cf2a206b613b0b668a74a8ebffed66616d91
workflow-type: tm+mt
source-wordcount: 4590
ht-degree: 69%

---


# 护栏和限制 {#limitations}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;查看Adobe Journey Optimizer的系统、历程、受众、渠道和内容限制，以便您可以规划可伸缩的部署而不会遇到失败。

>[!ENDSHADEBOX]

您可以在下方了解使用 [!DNL Adobe Journey Optimizer] 时的护栏和限制。

[Adobe Journey Optimizer 产品说明页面](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}列出了授权、产品限制和性能护栏。

>[!CAUTION]
>
>* [实时客户轮廓数据和分段的护栏](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/guardrails){target="_blank"}也适用于 Adobe Journey Optimizer。
>
>* 另请参阅[实时客户轮廓中的数据摄取护栏](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ingestion/guardrails){target="_blank"}


## 系统和平台 {#system-platform}

### 支持的浏览器 {#browsers}

Adobe [!DNL Journey Optimizer] 界面设计为可在最新版 Google Chrome 中发挥最佳表现。 在旧版本或其他浏览器上使用某些功能时可能会遇到问题。

### 数据集护栏 {#datasets-guardrails}

从 2025 年 2 月起，已在&#x200B;**新沙盒和新组织**&#x200B;中推出用于 Journey Optimizer 系统生成的数据集的生存时间 (TTL) 护栏，如下所示：

* 个人资料存储中的数据为&#x200B;**90天**
* 数据湖中的数据为&#x200B;**13个月**

此更改将在后续阶段推广到&#x200B;**现有的客户沙盒**。 [了解有关数据集生存时间 (TTL) 护栏的更多信息](../data/datasets-ttl.md)

## 历程 {#journeys-guardrails}

本部分涵盖历程的护栏和限制，包括常规历程限制、历程组件（操作、事件、数据源）、历程活动以及自定义操作和表达式编辑器等特定功能。

### 一般历程护栏 {#journeys-guardrails-journeys}

* 历程中的活动数限制为&#x200B;**50**。 活动数显示在历程画布的左上角部分。

  由于历程接近此限制，编辑和发布性能可能会降低，并且可能会发生保存或验证失败。 如果发生这种情况，请使用[跳转活动](../building-journeys/jump.md)将您的历程拆分为较小的子历程，或者在新版本中重新创建。 无法增加活动限制。

* 可一次性处于活动状态的实时、已关闭、已暂停和练习历程的数量在生产沙盒中限制为&#x200B;**200**，在开发沙盒中限制为&#x200B;**100**。 此限制在您发布历程时强制执行。 当前历程数显示在历程画布上方。

  当您发布历程时，我们会自动进行缩放和调整，确保最大吞吐量和稳定性。 只有在转出此护栏后创建已关闭的历程时，才会计算这些历程。

>[!NOTE]
>
>对于发布时护栏，在引入护栏时已超出限制的组织会收到异常。 现有历程不受影响。

* 在历程中使用受众资格时，该受众资格活动最多可能需要&#x200B;**10分钟**&#x200B;才能激活，并侦听进入或退出受众的用户档案。

* 配置文件的历程实例的最大大小为&#x200B;**1 MB**。 在历程执行过程中收集的所有数据都存储在该历程实例中。 因此，来自传入事件的数据、从 Adobe Experience Platform 检索的用户档案信息、自定义操作响应等都会存储在该历程实例中，并影响历程的大小。 当历程以事件开始时，建议限制该事件有效负载的最大大小（例如，小于&#x200B;**800 KB**）以避免在历程执行中的一些活动后达到该限制。 当达到该限制时，轮廓会处于错误状态并被从历程中排除。

* 对于每个配置文件和历程版本，历程运行时在处理一个事件时保持内部队列最多&#x200B;**10个待处理事件**。 如果达到此限制，则会以`maxInstanceStackEventsReached`原因丢弃其他事件，直到堆栈耗尽为止。 查看[由于受阻的历程实例而丢弃的事件](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached)。

* 除了历程活动中使用的超时之外，还有未显示在界面中且无法更改的全局历程超时。 此全局超时在个人进入历程&#x200B;**91天**&#x200B;后停止个人进度。 [了解更多信息](../building-journeys/journey-properties.md#global_timeout)

>[!TIP]
>
>**这对您意味着什么：** **50个活动限制**&#x200B;和&#x200B;**活动历程限制**&#x200B;是大多数团队在缩放时首先遇到的两个护栏。 提前规划历程拆分，并将读取受众开始时间至少相隔5-10分钟以避免沙盒吞吐量竞争。

#### 历程有效负载大小验证 {#journey-payload-size}

保存或发布历程时，Journey Optimizer 会验证历程有效负载的总大小，以保持稳定性和性能。

| 场景 | 阈值 | 行为 |
|---|---|---|
| 有效负载小于限制的90% | 低于警告 | 历程保存并发布成功。 未显示警告或错误。 |
| 有效负荷为限制的90-99% | 警告（软） | 历程保存和发布时出现警告： **警告**：历程有效负载大小接近限制。 最大节点：&#39;[NodeName]&#39; (type: &#39;[NodeType]&#39;, size: [N] bytes)。 |
| 有效负载≥限制的100% | **错误（硬）** | 保存或发布被阻止。 返回&#x200B;**HTTP 413请求实体太大**。 错误：历程的有效负载大小超出限制。 最大节点：&#39;[NodeName]&#39; (type: &#39;[NodeType]&#39;, size: [N] bytes)。 |

**默认配置**

* **默认最大请求大小**： **2 MB** （2,000,000字节）。 某些组织可能受制于 Adobe 配置的自定义限制。
* **警告阈值**：最大限制的 90%。
* **错误阈值**：最大限制的 100%。

**故障排除和建议**

* 查看警告或错误中突出显示的最大节点。
* 简化条件，减少数据映射，并移除不必要的步骤或参数。
* 如果需要，请考虑将历程拆分为较小的历程。
* 如果您认为贵组织需要更高的限制，请联系您的 Adobe 代表。

要在发布之前监测历程的当前负载大小，请使用历程属性面板中的&#x200B;**[!UICONTROL 当前历程负载大小]**&#x200B;指示器。 [了解如何检查历程负载的大小](../building-journeys/journey-properties.md#journey-payload-size)

### 许可证包比较 {#select-package-limitations}

>[!NOTE]
>
>以下“选择包”限制不适用于读取受众或业务事件历程。 若您需要具有多个操作、条件或等待活动的更复杂历程逻辑，请考虑升级您的许可套餐或在适用的情况下使用读取受众历程。

对于使用&#x200B;**Select**&#x200B;许可证包的客户，以下附加限制尤其适用于单一历程（以事件或受众资格开始的历程）：

| 限制 | 错误代码 | 描述 |
|---|---|---|
| 只允许一个操作 | `ERR_PKG_SELECT_8` | 单一历程只能包含&#x200B;**one**&#x200B;操作活动。 不允许在同一历程中使用多个电子邮件、推送、短信或其他操作活动。 |
| 不允许条件 | `ERR_PKG_SELECT_7` | 条件活动不能在单一历程中使用。 历程必须遵循单一线性路径，不得包含分支逻辑。 |
| 无等待活动 | `ERR_PKG_SELECT_6` | 无法将等待活动添加到单一历程。 操作必须立即执行，不得延迟。 |
| 超时/错误过渡必须转至结束节点 | `ERR_PKG_SELECT_2` | 如果为操作（例如电子邮件操作）配置超时或错误过渡，这些路径必须直接指向结束节点。 它们无法连接到历程中的其他活动或操作。 |

>[!TIP]
>
>**这对您意味着什么：**&#x200B;如果您位于Select程序包中，并且需要分支逻辑、等待活动或多个操作，则必须改用“读取受众”历程，或联系您的Adobe代表以升级程序包。

### 历程版本 {#journey-versions-g}

以下护栏适用于[历程版本](../start/user-interface.md)：

* v1 中以事件活动开始的历程，在后续版本中无法以事件之外的其他内容开始。 无法从&#x200B;**受众资格筛选**&#x200B;事件开始历程。
* v1 中从&#x200B;**受众资格筛选**&#x200B;活动开始的历程在后续版本中必须始终从&#x200B;**受众资格筛选**&#x200B;开始。
* 无法在新版本中更改在&#x200B;**受众资格筛选** （第一个节点）中选择的受众和命名空间。
* 在所有历程版本中，重新进入规则必须相同。
* 从&#x200B;**读取受众**&#x200B;开始的历程，在后续版本中无法从其他事件开始。
* 您无法创建具有增量读取的读取受众历程的新版本。 您必须复制历程。

### 历程和轮廓创建 {#journeys-limitation-profile-creation}

在 Adobe Experience Platform 中，创建/更新基于 API 的轮廓存在延迟。 延迟方面的服务水平目标(SLT)从摄取到统一配置文件的第95百分位请求的时间小于1分钟，每秒请求量为&#x200B;**20K (RPS)**。

如果在创建轮廓的同时触发了历程，并立即检查/检索轮廓服务中的信息，则该历程可能无法正常工作。

您可以从以下两种解决方案中选择一种：

* 在第一个事件后添加等待活动，以便给 Adobe Experience Platform 提供向轮廓服务执行摄取所需的时间。

* 设置不会立即利用轮廓的历程。 例如，如果历程旨在确认帐户创建，则体验事件可能包含发送第一条确认消息（名字、姓氏、电子邮件地址等）所需的信息。

### 活动 {#events-g}

以下护栏适用于历程中的[事件](../event/about-events.md)：

* Journey Optimizer支持所有沙盒的峰值容量为每秒&#x200B;**5,000个入站旅程事件**。 要了解有关此限制的更多信息，请参阅[此页面](../event/about-events.md#event-thoughput)。
* 事件触发的历程可能最多需要&#x200B;**5分钟**&#x200B;来处理历程中的第一个操作。
* 对于系统生成的事件，必须先在 Journey Optimizer 中配置用于启动客户历程的流数据，才能获取唯一的编排 ID。 此编排 ID 必须附加到传入 Adobe Experience Platform 的流有效负载中。 此限制不适用于基于规则的事件。
* 业务事件无法与单一事件或受众资格筛选活动结合使用。
* 在任何时候，一个事件最多可以引用&#x200B;**25**&#x200B;个历程。 达到此限制后，将阻止发布使用该事件的任何其他历程。
* 单个XDM架构一次可以由所有实时历程和已关闭历程中的最多&#x200B;**100**&#x200B;个事件引用。 达到此限制后，将阻止发布任何包含引用该架构的事件节点的历程。
* 单一历程（以事件或受众资格筛选开始）包含护栏，可防止同一事件多次错误触发历程。 默认情况下，重新进入用户档案会被暂时阻止&#x200B;**5分钟**。 例如，如果某个事件在 12:01 触发某个特定轮廓的历程，而另一个事件在 12:03 到达（无论是同一事件还是其他事件触发同一历程），则对于此轮廓，该历程将不会重新开始。
* Journey Optimizer 要求将事件流式传输到数据收集核心服务 (DCCS) 才能触发历程。 批量摄取的事件、通过&#x200B;**查询服务**&#x200B;插入的事件，或来自 Journey Optimizer 内部数据集（如消息反馈、电子邮件跟踪等）的事件 无法用于触发历程。 对于无法获取流式处理事件的用例，您必须根据这些事件构建一个受众，然后使用&#x200B;**读取受众**&#x200B;活动。 从技术上讲，可以使用受众资格筛选，但不建议这么做，因为这可能会导致下游挑战，具体取决于所使用的操作。

### 数据源 {#data-sources-g}

以下护栏适用于历程中的[数据源](../datasource/about-data-sources.md)：

* 可在客户历程中利用外部数据源，以实时查找外部数据。 这些源必须可通过 REST API 使用，支持 JSON，并能够处理大量请求。
* URL 和 API 不支持 Adobe 内部地址 (`.adobe.*`)。

>[!NOTE]
>
>由于现在支持响应，因此您应该对外部数据源用例使用自定义操作而不是数据源。

### 常规操作 {#general-actions-g}

以下护栏适用于历程中的[操作](../building-journeys/about-journey-activities.md)：

* 如果出现错误，系统将执行三次重试。 无法根据收到的错误消息调整重试次数。 对 HTTP 401、403 和 404 以外的所有 HTTP 错误执行重试。
* 使用内置的&#x200B;**反应**&#x200B;事件，可对开箱即用的操作做出反应。 请参阅[此页面](../building-journeys/reaction-events.md)以了解详情。 如果要对通过自定义操作发送的消息做出反应，则必须配置专用事件。
* 无法同时设置两个操作，必须先添加一个，然后再添加另一个操作。
* 对于所有有效的[历程版本](../building-journeys/publish-journey.md#journey-create-new-version)，一个轮廓不能在同一历程中同时多次出现。 如果启用了重新进入，则用户档案可以重新进入历程，但只有在完全退出该历程的上一个实例后才能重新进入历程。 [了解详情](../building-journeys/end-journey.md)

### 自定义操作 {#custom-actions-g}

以下护栏适用于历程中的[自定义操作](../action/action.md)：

* 为所有自定义操作、每个主机和每个沙盒定义了&#x200B;**300,000次1分钟以上调用的上限**。 对于响应时间短于 0.75 秒的端点，此上限强制作为每个沙盒和每个端点的滑动窗口。 对于响应时间大于0.75秒的端点，将应用每30秒&#x200B;**150,000次调用的单独限制**（也是滑动窗口）。
* 自定义操作 URL 不支持动态参数。
* 支持POST、PUT和GET调用方法。
* 查询参数或标头的名称不得以“.” 或“$”。
* URL中不允许使用IP地址。 请改用主机名。
* URL 和 API 不支持 Adobe 内部地址 (`.adobe.*`)。
* 无法移除内置的自定义操作。
* 仅当使用请求或响应负载时，自定义操作才支持 JSON 格式。 请参阅[此页](../action/about-custom-action-configuration.md#custom-actions-limitations)。
* 自定义操作所针对的任何终结点都必须至少支持&#x200B;**200 TPS**。 请注意，限制配置不能低于 200 TPS。 根据您的预期吞吐量，高响应时间可能会影响实际吞吐量。

>[!TIP]
>
>**这对您意味着什么：**&#x200B;默认的300,000次调用/分钟上限可保护您的外部端点不被历程吞吐量淹没。 如果您的端点可以处理更多负载，则可以使用[上限API](../configuration/capping.md)或[限制API](../configuration/throttling.md)提高此限制。 有关Journey Optimizer如何连接到外部系统的更广泛概述，请参阅[此页面](../configuration/external-systems.md)。 如果您需要更高的组织限制，请联系您的Adobe代表。

### 补充标识符 {#supplemental}

在历程中使用补充标识符需遵循特定护栏的限制。 请参见[此页面](../building-journeys/supplemental-identifier.md#guardrails)中所列。

### 表达式编辑器 {#expression-editor}

以下护栏适用于[历程表达式编辑器](../building-journeys/expression/expressionadvanced.md)：

* 以读取受众、受众资格筛选或业务事件活动开始的历程中，无法使用体验事件字段组。 您必须创建新受众并在历程中使用 `inaudience` 条件。
* 不能在表达式编辑器中使用 `timeSeriesEvents` 属性。 要在轮廓级别访问体验事件，请基于 `XDM ExperienceEvent` 架构创建新的字段组。

### 历程活动 {#activities}

#### 受众资格筛选活动 {#audience-qualif-g}

以下护栏适用于[受众资格](../building-journeys/audience-qualification-events.md)历程活动：

* “受众资格筛选”活动不能与 Adobe Campaign 活动一起使用。
* 受众资格筛选历程不支持补充标识符。
* 沙盒在所有实时历程和已关闭历程中最多可包含&#x200B;**300**&#x200B;个受众资格节点。 达到此限制后，将阻止发布具有其他受众资格节点的历程。

要进一步了解历程处理速率和吞吐量限制，请参阅[此部分](../building-journeys/entry-management.md#journey-processing-rate)。

[此页面](../building-journeys/audience-qualification-events.md#audience-qualification-guardrails)上列出了其他护栏，包括有关流式受众与批次受众的推荐以及合成受众限制。

#### Campaign 活动 {#ac-g}

以下护栏适用于 **[!UICONTROL Campaign v7/v8]** 和 **[!UICONTROL Campaign Standard]** 活动：

* Adobe Campaign 活动不能与“读取受众”或“受众资格筛选”活动一起使用。
* **[!UICONTROL Campaign Standard]** 活动不能与其他渠道活动一起使用：卡片、基于代码的体验、电子邮件、推送、短信、应用程序内消息、Web。
* **[!UICONTROL Campaign v7/v8]** 活动可与同一历程中的原生渠道活动一起使用。

#### 反应事件 {#reaction-events-g}

特定护栏适用于&#x200B;**[!UICONTROL 反应]**&#x200B;事件，包括要求将活动立即置于渠道操作之后，以及无法跟踪在其他历程中发送的消息。 请参见[此页面](../building-journeys/reaction-events.md#guardrails-limitations)中所列。

#### 应用程序内活动 {#in-app-activity-limitations}

以下护栏适用于&#x200B;**[!UICONTROL 应用程序内消息]**&#x200B;操作。 要了解应用程序内消息的更多信息，请参阅[此页面](../in-app/create-in-app.md)。

* 此功能目前不适用于医疗保健客户。

* 个性化只能包含轮廓属性。

* 应用程序内活动不能与 **[!UICONTROL Campaign Standard]** 活动一起使用。

* 应用程序内显示与历程生命周期绑定，这意味着当具有相应轮廓的受众的历程结束时，该历程中的所有应用程序内消息将不再会显示给该受众。 因此，无法直接从历程活动停止应用程序内消息。 相反，您必须结束整个历程以停止向具有相关轮廓的受众显示应用程序内消息。

* 在测试模式下，应用程序内显示取决于历程的有效期。 要防止历程在测试期间过早结束，请调整&#x200B;**[!UICONTROL 等待]**&#x200B;活动的&#x200B;**[!UICONTROL 等待时间]**&#x200B;值。

* **[!UICONTROL 反应]**&#x200B;活动无法用于对应用程序内打开或点击作出反应。

* 从用户轮廓到达画布中应用程序内活动到开始看到应用程序内消息之间，可能会发生激活延迟。

* 应用程序内消息内容大小限制为&#x200B;**2 MB**。 包含大图像可能会妨碍发布流程。

#### 内容决策活动 {#content-decision-g}

特定护栏适用于&#x200B;**[!UICONTROL 内容决策]**&#x200B;活动，包括更新的同意策略在决策策略中生效之前的48小时延迟。 请参见[此页面](../building-journeys/content-decision.md#guardrails)中所列。

#### 跳转活动 {#jump-g}

特定护栏适用于&#x200B;**[!UICONTROL 跳转]**&#x200B;活动。 请参见[此页面](../building-journeys/jump.md#jump-limitations)中所列。

#### 读取受众活动 {#read-segment-g}

以下护栏适用于[读取受众](../building-journeys/read-audience.md)历程活动：

* 流式处理受众始终会保持更新，但在检索时间中不会考虑批量区段。 它们每天仅在每日批量评估时间中进行评估。
* 在历程入口处，档案使用的是批量受众快照中的属性值。 然而，当档案到达&#x200B;**等待**&#x200B;活动时，历程会自动从统一档案服务 (UPS) 获取最新数据来刷新档案属性。 这意味着在历程执行期间，档案属性可能会发生更改。
* **读取受众**&#x200B;活动不能与 Adobe Campaign 活动一起使用。
* **读取受众**&#x200B;活动只能用作历程中的第一个活动，即业务事件活动后的第一个活动。
* 历程只能有一个&#x200B;**读取受众**&#x200B;活动。
* **读取受众**&#x200B;活动只能针对每个历程的一个受众。 如果需要多个受众，请先将其合并到单个受众中。 [了解如何使用组合工作流合并受众](../audience/get-started-audience-orchestration.md)。
* 每个组织在所有沙盒和历程中最多可并发运行&#x200B;**5个** **读取受众**&#x200B;实例（已计划或已触发业务事件）。 避免同时启动超过 5 个包含&#x200B;**读取受众**&#x200B;的历程；将其相隔 5 到 10 分钟。 要进一步了解历程处理速率，请参阅[此部分](../building-journeys/entry-management.md#journey-processing-rate)。
* 沙盒吞吐量：系统管理每个沙盒的处理，最多每秒&#x200B;**20,000个配置文件**，这些配置文件在所有&#x200B;**读取受众**&#x200B;活动中共享。 单个活动可以配置为每秒有&#x200B;**500到20,000个配置文件**。 如果达到沙盒限制，作业可能会排入队列。
* 作业处理超时： **无法在** 12小时&#x200B;**内处理的读取受众**&#x200B;作业将被自动清理并且不会执行。
* 默认情况下，在检索导出作业时对受众触发的历程应用重试。 如果在创建导出作业期间发生错误，将每10分钟重试一次，最长为&#x200B;**1小时**。 之后，该历程会被视为失败，因此最多可以在计划时间后1小时内执行。
* 对于使用补充ID的历程，每个历程实例的&#x200B;**读取受众**&#x200B;活动的读取率限制为每秒&#x200B;**500个用户档案**。

>[!TIP]
>
>**这对您意味着什么：** 5并发实例限制是整个组织的硬性上限。 如果您有多个团队在计划读取受众历程，请仔细协调开始时间。 错过12小时处理窗口的作业会被静默丢弃 — 始终在历程日志中确认成功执行。

另请参阅有关“读取受众”活动的[建议和配置](../building-journeys/read-audience.md#must-read)。

#### 更新轮廓活动 {#update-profile-g}

特定护栏适用于&#x200B;**[!UICONTROL 更新轮廓]**&#x200B;活动。 请参见[此页面](../building-journeys/update-profiles.md)中所列。

#### 历程暂停 {#pause-g}

特定护栏适用于&#x200B;**暂停历程**，包括组织中所有暂停历程的最长暂停持续时间&#x200B;**14天**&#x200B;和&#x200B;**1000万个配置文件上限**。 请参见[此页面](../building-journeys/journey-pause.md#journey-pause-guardrails)中所列。

#### 历程试运行 {#dry-run-g}

特定护栏适用于&#x200B;**历程练习**，包括计入可参与的用户档案和实时历程配额。 请参见[此页面](../building-journeys/journey-dry-run.md#journey-dry-run-limitations)中所列。

#### 历程片段 {#fragments-journey-g}

特定护栏适用于&#x200B;**历程片段**，包括每个片段&#x200B;**最多** 20个节点，以及每个沙盒&#x200B;**最多** 200个活动片段。 请参见[此页面](../building-journeys/journey-fragments.md#guardrails)中所列。

#### 按波次发送 {#waves-g}

特定护栏适用于旅程中的&#x200B;**波次发送**，包括2-10波次范围以及波次之间的&#x200B;**30分钟最小间隔**。 请参见[此页面](../building-journeys/send-using-waves.md#limitations-guardrails)中所列。

#### 历程模拟 {#simulation-g}

特定护栏适用于&#x200B;**历程模拟**。 请参见[此页面](../building-journeys/simulate-journey.md#limitations)中所列。

## 受众和配置文件 {#audiences-profiles}

本部分内容涵盖受众管理护栏、轮廓处理以及可互动轮廓的考虑事项。

### 受众和配置文件护栏 {#audience}

* 您最多可以在给定的沙盒中发布&#x200B;**10个受众合成**。 如果您已达到此阈值，则需要删除组合以释放空间，然后才能发布新组合。

  要了解有关受众构成的更多信息，请参阅[此页面](../audience/get-started-audience-orchestration.md)。

* 摄取数据时，电子邮件区分大小写。 这意味着在 [!DNL Journey Optimizer] 历程和营销活动中选择相应的目标收件人时可能创建和使用重复的轮廓（例如，一个轮廓对应 John.Greene@luma.com，另一个轮廓对应 john.greene@luma.com）。

* 当使用入站渠道将匿名配置文件（未经身份验证的访客）选择为目标时，请考虑设置生存时间 (TTL) 以自动删除配置文件，从而管理可参与配置文件的数量和相关成本。 [了解详情](#profile-management-inbound)

## 渠道和消息 {#channel-guardrails}

本部分涵盖所有通信渠道的使用规范，包括电子邮件、短信、入站渠道（web、应用程序内、基于代码推送、内容卡片）以及交易型消息。

>[!NOTE]
>
>在极少数情况下，特定区域的临时故障可能会导致从历程中排除有效的用户档案，或导致邮件被错误标记为退回。 恢复服务后，重新检查历程日志，验证同意用户档案字段，并根据需要重新发布历程。 如果 ISP 中断，请参阅[本部分](../configuration/manage-suppression-list.md#remove-from-suppression-list)，了解如何从禁止列表中移除用户档案。

### 电子邮件护栏 {#message-guardrails}

以下护栏适用于[电子邮件渠道](../email/get-started-email.md)：

* 无法使用相同的发送域从 [!DNL Adobe Journey Optimizer] 和其他产品（例如 [!DNL Adobe Campaign] 或 [!DNL Adobe Marketo Engage]）发送电子邮件消息。

在设计电子邮件时，系统会检查关键设置并显示警告（建议和最佳实践）和错误（阻止测试或激活的阻止问题）警报。 要进一步了解电子邮件警报和验证要求，请参阅[此部分](../email/create-email.md#check-email-alerts)。

#### 历程发布的消息内容大小 {#message-content-size}

发布包含电子邮件的历程时，后端处理后的邮件内容总大小不得超过&#x200B;**2 MB**。 在发布过程中，系统会通过修补链接、图像和应用转换来自动处理消息内容，这会增加负载大小，使其超过创作的内容大小。

>[!CAUTION]
>
>如果最终处理的消息内容超过&#x200B;**2 MB**，则历程发布将失败。 将您的已创作消息内容保持在2 MB以下（最好在&#x200B;**1 MB**&#x200B;以下），以便允许300-400 KB的缓冲区用于后端处理开销。

**防止发布失败的最佳实践：**

* 将编写的电子邮件内容保留在&#x200B;**1 MB**&#x200B;以下
* 最大程度减少内容变体的数量
* 在将图像添加到消息之前，先对其进行优化和压缩
* 删除未使用的资产和不必要的 HTML 元素
* 在将历程发布到生产环境之前测试消息大小

如果因内容大小而导致历程发布失败，请精简消息内容并重新发布历程。

### 短信护栏 {#sms-guardrails}

以下护栏适用于[短信渠道](../mobile/get-started-mobile.md)：

* 可以通过支持的 URL 加入 MMS 的媒体文件。 请确保单独上传媒体文件。
* 消息反馈同步当前不适用于 MMS。
* 同意管理在 MMS 的短信渠道级别运行。

### 入站渠道护栏 {#inbound-guardrails}

* 要在 [!DNL Journey Optimizer] 中使用[基于代码的体验](../code-based/get-started-code-based.md)操作，并传递应用程序可以使用的代码内容负载，请遵守[此页面](../code-based/code-based-prerequisites.md)中详述的先决条件。

* 要访问和创作 [!DNL Journey Optimizer] 用户界面中的[网页](../web/get-started-web.md)，请遵循[此页面](../web/web-prerequisites.md)中列出的先决条件。

* 要在包含 [!DNL Journey Optimizer] 的历程和营销活动中发送应用程序内消息，请遵循[此页面](../in-app/inapp-configuration.md)中列出的投放先决条件。

* 要让 Adobe Journey Optimizer 正确显示内容卡片，您必须配置[此页面](../content-card/content-card-configuration-prereq.md)中列出的 Adobe Experience Platform 设置。

* Journey Optimizer支持每秒&#x200B;**5,000个入站请求的峰值**。 此护栏适用于所有入站请求，这些请求可能是来自 Journey Optimizer 支持的入站渠道（[Web](../web/get-started-web.md)、[应用程序内](../in-app/get-started-in-app.md)、[基于代码的体验](../code-based/get-started-code-based.md)、[内容卡](../../rp_landing_pages/content-card-landing-page.md)）。

* Journey Optimizer在任何时刻最多支持&#x200B;**500个活动的入站操作**。 如果这些入站操作是实时营销活动的一部分，或者是实时历程中使用的节点，则会被计算在内。 达到此数量后，您需要停用使用入站操作的旧营销活动或历程，然后才能启动新营销活动或历程。

#### 使用入站渠道管理配置文件 {#profile-management-inbound}

[!DNL Journey Optimizer] 入站渠道可以将匿名配置文件（即未经身份验证或未知的配置文件）选择为目标，因为这些配置文件以前未在其他渠道上参与。 例如，当基于 ECID 等临时 ID 将所有访客或受众选择为目标时。

这将增加可参与配置文件的总数，如果超出您购买的可参与配置文件的合同数量，则可能会产生成本影响。 [Journey Optimizer 产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}页面上列出了每个包的许可证指标。 您可以在[许可证使用情况仪表板](../audience/license-usage.md)中查看可参与配置文件的数量。

要将可互动轮廓的数量保持在合理范围内，Adobe 建议设置生存时间 (TTL)，以便在特定时间范围内未看到匿名轮廓或这些轮廓未参与互动时，自动从实时客户轮廓中删除它们。 Adobe建议将TTL值设置为&#x200B;**14天**&#x200B;以匹配当前的Edge配置文件TTL。

>[!NOTE]
>
>请参阅 [Experience Platform 文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}，了解如何为匿名配置文件配置数据过期时间。

### 事务性消息护栏 {#transactional-message-guardrails}

Journey Optimizer在营销活动中支持每秒&#x200B;**500条事务性消息的高峰**。

## 内容和资产 {#content-assets}

本部分涵盖内容创建和管理的护栏，包括登陆页面、子域和片段。

### AI助手护栏 {#ai-assistant-g}

**AI助手内容生成**&#x200B;的护栏和限制(包括支持的渠道（电子邮件、推送、Web、短信）和个性化编辑器限制)在[此页面](../content-management/gs-generative.md#generative-guardrails)中列出。

### 登陆页面护栏 {#lp-guardrails}

以下护栏适用于[登录页面](../landing-pages/get-started-lp.md)：

* 在单个主页面中只能使用一个&#x200B;**表单**&#x200B;组件。
* 无法在子页面中使用&#x200B;**表单**&#x200B;组件。
* 无法向登陆页添加预编译标头。
* 设计主登录页面时，无法选择&#x200B;**自己编写代码**&#x200B;选项。

### 子域护栏 {#subdomain-guardrails}

[此页面](../configuration/delegate-subdomain.md#guardrails)详细介绍了 Journey Optimizer 中适用于子域委派的护栏和限制。

### 片段护栏 {#fragments-guardrails}

以下护栏适用于[片段](../content-management/fragments.md)：

* 要创建、编辑、存档和发布片段，您需要拥有 **[!DNL Content Library Manager]** 产品配置文件中包含的 **[!DNL Manage library items]** 和&#x200B;**[发布片段]**&#x200B;的权限。 [了解详情](../administration/ootb-product-profiles.md#content-library-manager)
* 可视化片段仅适用于电子邮件渠道。
* 表达式片段不适用于应用程序内渠道。
* 可视片段不能超过&#x200B;**100 KB**。 表达式片段不能超过&#x200B;**200 KB**。
* 要在历程或营销活动中使用某个片段，该片段必须处于&#x200B;**实时**&#x200B;状态。
* 不支持在片段中使用[上下文属性](../personalization/personalization-build-expressions.md)。
* 在“使用主题”和“手动样式设置”模式之间，可视化片段不交叉兼容。 为了能够在需要应用主题的内容中使用片段，必须在“使用主题”模式下创建此片段。 [了解有关主题的更多信息](../email/apply-email-themes.md)
* 在历程或营销活动中启用跟踪时，如果您向某个片段添加链接，并且在消息中使用了该片段，则会跟踪这些链接，例如消息中包含的所有其他链接。 [了解有关链接和跟踪的更多信息](../email/message-tracking.md)

## 决策管理 {#decision-management}

### 决策和决策管理护栏 {#decisioning-guardrails}

有关使用 Decisioning 或决策管理时要牢记的护栏和限制，请参阅以下 Decisioning 和决策管理部分：

* [决策护栏和限制](../experience-decisioning/decisioning-guardrails.md)
* [决策管理护栏和限制](../offers/decision-management-guardrails.md)

## 营销活动编排 {#campaign-orchestration}

### 营销活动编排护栏 {#orchestration-guardrails}

有关使用营销活动编排功能时要牢记的护栏和限制，在此部分中进行了详细介绍：[护栏和限制](../orchestrated/guardrails.md)。
