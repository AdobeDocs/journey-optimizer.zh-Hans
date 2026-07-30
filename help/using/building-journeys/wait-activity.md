---
solution: Journey Optimizer
product: journey optimizer
title: 等待活动
description: 了解如何配置等待活动
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 等待，活动，历程，下一个，画布
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/qWxnLiuHh-sJQyUOuRB6CgRIpZ6ud6eO-WNoWcv9JeU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c3f67a94-f1ff-4f5e-bf6f-bc22405930a3id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1589
ht-degree: 8%

---

# 等待活动 {#wait-activity}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何将Wait活动配置为在相对持续时间或自定义计算日期之前暂停路径，直到下一次活动运行。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="等待活动"
>abstract="“等待”活动允许您在执行路径中的下一个活动之前暂停一段时间。 这让您可以定义执行下一个活动的时刻。 有两个选项可用：持续时间和自定义。"

您可以使用&#x200B;**[!UICONTROL 等待]**&#x200B;活动定义持续时间，然后再执行下一个活动。  最长等待时间为&#x200B;**90天**。

您可以设置两种类型的&#x200B;**等待**&#x200B;活动：

* 基于相对持续时间的等待。 [了解详情](#duration)
* 自定义日期，使用函数进行计算。 [了解详情](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## 推荐 {#wait-recommendations}

使用这些建议可保持等待的可预测性和安全性。

### 多个等待活动 {#multiple-wait-activities}

在历程中使用多个&#x200B;**等待**&#x200B;活动时，请注意，历程的[全局超时](journey-properties.md#global_timeout)为91天，这意味着用户档案始终在进入历程后91天内退出该历程。 请参阅[此页面](journey-properties.md#global_timeout)以了解详情。

仅当个人在历程中剩余的时间足以在91天历程超时之前完成等待持续时间时，个人才能进入&#x200B;**等待**&#x200B;活动。

### 等待并重新进入 {#wait-reentrance}

不使用&#x200B;**等待**&#x200B;活动阻止重新进入的最佳实践。 请改用历程属性级别的&#x200B;**允许重入**&#x200B;选项。 请参阅[此页面](../building-journeys/journey-properties.md#entrance)以了解详情。

### 等待和测试模式 {#wait-test-mode}

在测试模式下，**[!UICONTROL 测试中的等待时间]**&#x200B;参数允许您定义每个&#x200B;**等待**&#x200B;活动的持续时间。 默认时间为 10 秒。 这将确保您快速获得测试结果。 请参阅[此页面](../building-journeys/testing-the-journey.md)以了解详情。

### 等待和移动渠道 {#wait-mobile-channels}

如果要在发送[推送通知](../../rp_landing_pages/push-landing-page.md)后不久显示[应用程序内消息](../in-app/create-in-app.md)，请使用&#x200B;**等待**&#x200B;活动以允许传播应用程序内消息有效负荷时间。 通常建议等待5-15分钟，但具体时间会因有效负载复杂性和个性化需求而异。

## 配置 {#wait-configuration}

在此处配置等待时长和计时。

### 持续时间等待 {#duration}

选择&#x200B;**持续时间**&#x200B;类型以设置下一个活动执行前等待的相对持续时间。 最长持续时间为&#x200B;**90天**。

![定义等待持续时间](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![Wait activity configuration panel with duration and fixed date options](assets/journey56.png)
-->

### 自定义等待 {#custom}

选择&#x200B;**自定义**&#x200B;类型以使用基于来自事件或自定义操作响应的字段的高级表达式来定义自定义日期。 您不能直接定义相对持续时间，例如7天，但您可以根据需要使用函数计算相对持续时间（例如：购买后2天）。

![使用表达式定义自定义等待](assets/journey57.png)

编辑器中的表达式应提供`dateTimeOnly`格式。 请参见[此页面](expression/expressionadvanced.md)。 有关dateTimeOnly格式的详细信息，请参阅[此页面](expression/data-types.md)。

最佳实践是使用特定于您用户档案的自定义日期，并避免对所有用户使用相同的日期。 例如，不要定义`toDateTimeOnly('2024-01-01T01:11:00Z')`，而是要定义特定于每个配置文件的`toDateTimeOnly(@event{Event.productDeliveryDate})`。 请注意，使用固定日期可能会导致历程执行出现问题。 在[本节](entry-management.md#wait-activities-impact)中进一步了解等待活动对历程处理率的影响。


>[!CAUTION]
>
>使用`dateTimeOnly`表达式时，请牢记以下几点：
>
>* 您可以直接使用`dateTimeOnly`表达式，或使用函数转换为该表达式 — 例如： `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`，其中字段值采用`2023-08-12T09:46:06Z`格式。
>* 在历程属性中定义&#x200B;**时区**。 因此，从UI无法指向混合了时间和时区偏移的完整ISO-8601时间戳，例如`2023-08-12T09:46:06.982-05`。 [了解详情](../building-journeys/timezone-management.md)
>* 使用`toDateTimeOnly()`生成自定义等待表达式时，**不**&#x200B;附加`Z`或时区偏移（例如，`-05:00`）。 表达式必须引用历程配置的时区，且不能使用明确的时区指示器，否则配置文件可能会卡在等待活动中。
>
>| | 示例 |
>| --- | --- |
>| **正确** | `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00"))` |
>| **不正确** | `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00Z"))` ❌ （包含`Z`） |

要验证等待活动是否按预期运行，您可以使用步骤事件。 [了解详情](../reports/query-examples.md#common-queries)。

## 等待后配置文件刷新 {#profile-refresh}

当配置文件驻留在以&#x200B;**读取受众**&#x200B;活动开始的历程中的&#x200B;**等待**&#x200B;活动时，该历程会自动从统一配置文件服务(UPS)中刷新配置文件的属性，以获取最新可用数据。

* **在历程条目**：配置文件使用历程启动时计算的受众快照中的属性值。
* **在等待节点之后**：历程执行查找以从UPS检索最新的配置文件数据，而不是旧的快照数据。 这意味着自历程开始以来，配置文件属性可能已更改。

此行为可确保下游活动在等待时段后使用当前配置文件信息。 但是，如果您希望历程在整个执行过程中仅使用原始快照数据，则可能会产生意外结果。

示例：如果配置文件在历程开始时符合“银级客户”受众的条件，但在3天等待期间升级到“金级客户”，则等待后的活动将看到更新的“金级客户”状态。

## 自动等待节点  {#auto-wait-node}

>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node"
>title="关于自动等待节点"
>abstract="系统会在此入站操作后自动插入一个&#x200B;**等待**&#x200B;节点。 默认设置为 3 天，以确保轮廓在历程中停留足够长的时间来查看消息或体验。 如果业务场景需要，可以修改等待时长或删除该节点。"

每个入站体验活动（应用程序内消息、基于代码的体验或卡片）都包含3天&#x200B;**等待**&#x200B;活动。 当用户档案到达历程终点时，入站消息会自动结束，因此我们假定您希望用户至少在3天内看到该消息。 您可以删除此&#x200B;**等待**&#x200B;活动，或者根据需要更改其配置。

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;本页说明如何配置旅程中的“等待”活动，以暂停相对持续时间的配置文件进度，或直到自定义计算日期为止，然后再执行下一步。

**意图：**

* 添加等待活动以暂停固定相对持续时间（最多90天）的历程
* 使用高级表达式配置自定义等待，以延迟到配置文件特定的计算日期
* 了解等待活动如何与历程全局超时（91天）交互
* 使用Wait time in test参数可加快测试模式验证的速度
* 了解如何在读取受众历程中的等待节点后刷新配置文件属性

**术语表：**

* **等待活动**：在下一个活动执行&#x200B;*（产品特定）*&#x200B;之前，在指定的持续时间或计算日期之前暂停配置文件进展的历程编排活动
* **持续时间wait**：一种等待类型，设置相对暂停时间段，最长90天&#x200B;*（产品特定）*
* **自定义等待**：一种等待类型，它使用从配置文件或事件数据派生的`dateTimeOnly`表达式来定义恢复的特定未来日期/时间&#x200B;*（产品特定）*
* **自动等待节点**：在入站体验活动（应用程序内、基于代码、卡片）之后自动插入3天等待活动，以将配置文件在历程中保留足够长的时间以查看内容&#x200B;*（产品特定）*
* **测试中的等待时间**：历程测试模式参数，该参数覆盖实际等待持续时间（默认为10秒），因此测试结果会快速返回&#x200B;*（产品特定）*

**护栏：**

* 最长等待时间为90天。
* 配置文件会在91天（全局超时）后从历程中删除，这与挂起的等待活动无关。
* 仅当历程中剩余足够的时间在91天超时前完成等待时，用户档案才能进入等待活动。
* 请勿使用等待活动阻止重新进入；请改用历程属性中的允许重新进入选项。
* 自定义等待表达式必须使用`dateTimeOnly`格式，并且不得包含`Z`后缀或显式时区偏移。
* 在自定义等待中使用固定静态日期（例如`toDateTimeOnly('2024-01-01T01:11:00Z')`）可能会导致问题；请改用特定于用户档案的动态日期。
* 在读取受众历程中的等待节点后，配置文件属性会从统一配置文件服务中刷新，如果预期快照一致性，这可能会导致意外结果。

**术语：**

* 规范名称：等待活动 — 缩写：无 — 变体：等待节点，等待步骤
* 同义词： &quot;Duration wait&quot; = &quot;relative wait&quot;； &quot;Custom wait&quot; = &quot;expression-based wait&quot;
* 请勿混淆：“持续时间等待”（相对，例如，从现在起的3天）≠“自定义等待”（来自配置文件数据的绝对计算日期）

**常见问题解答：**

* **问：等待活动的最长持续时间是多少？**  — 最长等待时间为90天；配置文件也受91天的全局历程超时的约束。
* **问：测试模式如何处理等待活动？**  — 在测试模式下，“测试中的等待时间”参数会覆盖实际的等待持续时间；默认值为10秒，因此测试会快速完成。
* **问：为何要避免将Z附加到自定义等待表达式？**  — 将Z或时区偏移添加到`toDateTimeOnly()`表达式可能会导致配置文件卡在等待活动中；表达式必须依赖历程配置的时区。
* **问：在等待节点之后是否更新了配置文件属性？**  — 是，在以读取受众开始的历程中，历程会在等待后刷新统一配置文件服务的配置文件属性，因此下游活动可能会看到更新的值，而不是原始受众快照数据。
* **问：什么是自动等待节点？**  — 在入站体验活动（应用程序内、基于代码、卡片）之后自动插入3天等待活动，以确保用户档案在历程中停留足够长的时间以查看消息；可以根据需要删除或重新配置该活动。

+++
