---
solution: Journey Optimizer
product: journey optimizer
title: 从受众资格历程中迁移批量受众
description: 了解如何在2026年8月3日实施日期之前迁移在“受众资格”节点中使用批次受众的历程。
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: 受众资格，批量受众，弃用，迁移，读取受众，流受众
exl-id: f3c2a7d1-b58e-4a92-c3d5-0e871f2a9b4c
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
source-git-commit: 6560a168d3ea7c6c27b47829ac4158b6a69b5d88
workflow-type: tm+mt
source-wordcount: 874
ht-degree: 0%

---


# 从受众资格历程中迁移批量受众 {#aq-batch-migration}

从2026年8月3日开始，Journey Optimizer将阻止发布在“受众资格”节点中使用批量受众的历程。 请在下方确定您的用例，然后遵循建议的迁移路径。

>[!CAUTION]
>
>**强制实施日期：2026年8月3日。** 在此日期之后，无法发布在“受众资格”节点中使用批量受众的新历程、草稿历程和重复历程。 自2026年6月版本发布以来，历程画布中已显示验证警告。

## 为什么会出现此更改 {#why}

**[受众资格](audience-qualification-events.md)**&#x200B;节点旨在随着单个用户档案进入或退出受众而近乎实时地做出反应 — 资格事件逐个连续到达。 它适用于&#x200B;**[流式受众](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)**。

当将批量受众与“受众资格”节点一起使用时，所有资格事件都在摄取窗口期间同时到达。 这会同时触发数万或数百万个历程条目，导致严重的系统压力和下游系统中的不可预测行为。 这不是“受众资格”节点的预期设计。

**[读取受众](read-audience.md)**&#x200B;活动是基于批次的用例的正确工具：构建该活动是为了以受控和可预测的方式处理计划的批量处理。

## 您的历程会受到什么影响 {#impact}

在Audience Qualification节点中使用批量受众的实时历程在2026年8月3日之后继续运行。 但是，如果您停止、复制或重新发布历程，则会在更新配置之前阻止该历程。


| 历程状态 | 2026年8月3日之后的影响 |
| --- | --- |
| **实时历程** | 未受影响。 现有的实时历程将继续运行。 不自动停止。 |
| **新历程** | 在替换批次受众之前，阻止发布。 |
| **草稿历程** | 在替换批次受众之前，阻止发布。 |
| **重复的历程** | 在替换批次受众之前，阻止发布。 |


## 迁移指南 {#migration-paths}

如果您在“受众资格”节点中使用批量受众，请在下面确定您的用例，然后遵循建议的迁移路径。

### 用例1 — 基于AJO消息跟踪事件构建的受众 {#use-case-1}

**如下所示：**&#x200B;您的受众资格受众使用基于Journey Optimizer内部跟踪数据集的电子邮件发送、打开或单击的条件 — 例如，*“配置文件收到电子邮件”*&#x200B;或&#x200B;*“配置文件打开了电子邮件”*。

>[!NOTE]
>
>自2024年11月起，流式分段不再支持来自Journey Optimizer跟踪数据集的发送和打开事件。 现在将在批处理模式下评估基于这些事件的受众。 [了解有关受众评估方法的更多信息](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)

**推荐的替代项：**

* **响应同一历程中的打开或点击** — 使用&#x200B;**[反应事件](reaction-events.md)**&#x200B;节点。 它专门构建用于响应在同一历程中发送的消息中的打开次数和点击次数，而无需单独的受众。 [查看使用反应事件的端到端示例](journeys-uc.md#send-multi-channel-messages)

* **跨历程点击定位** — 从点击事件构建[流式受众](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)，然后将“受众资格”节点用于该流式受众。

* **基于退回的禁止显示** — 使用Journey Optimizer的原生[禁止显示列表](../configuration/manage-suppression-list.md)，而不是将退回行为建模为受众条件。

* **任何剩余的发送/打开逻辑** — 在计划的运行中切换到&#x200B;**[读取受众](read-audience.md)**&#x200B;历程以安全地处理批次受众。


### 用例2 —历程等待新的批量分段数据 {#use-case-2}

**如下所示：**&#x200B;您计划了在每日分段作业后运行的历程，并使用“受众资格”节点以确保仅在最新的受众数据可用时触发历程。

**推荐的替代项：**

在启用批量受众评估后使用&#x200B;**[!UICONTROL 触发器的**[&#x200B;读取受众&#x200B;](read-audience.md)**历程]**&#x200B;选项。 此内置功能可保留历程执行，直到分段作业完成，然后在有新数据可用时立即开始，而无需受众资格节点。 [了解如何配置此选项](read-audience.md#schedule)


### 用例3 — 大规模定期批量受众激活 {#use-case-3}

**外观：**&#x200B;您定期激活或刷新大量受众（可能包含数百万个配置文件），并且会同时为所有新限定的配置文件触发受众资格历程。

**推荐的替代项：**

使用&#x200B;**[读取受众](read-audience.md)**&#x200B;历程。 它专门构建用于批量处理大量受众、受控批量处理用户档案以及大规模提供更可预测、更可靠的历程执行。 [查看端到端示例](message-to-subscribers-uc.md)

## 如果任何替代方案都不适合您的用例，该怎么办？ {#exceptions}

如果使用上述任何迁移路径都无法解决您的用例，请联系您的Adobe代表。 对于无法使用现有替代品解决的案例，将单独进行审查。

## 相关资源 {#related}

* [受众资格事件](audience-qualification-events.md) — 完整配置指南和护栏
* [读取受众活动](read-audience.md) — 如何配置计划的批量受众条目
* [反应事件](reaction-events.md) — 如何对同一历程中的打开数和点击数做出反应
* [受众评估方法](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer) — 说明批处理、流式处理和边缘分段
* [关于受众](../audience/about-audiences.md) — 受众类型以及如何在Journey Optimizer中构建受众
* [管理禁止列表](../configuration/manage-suppression-list.md) — 如何访问和配置退回禁止显示
* [历程护栏和限制](limitations.md)
* [历程进入和退出条件](entry-exit-criteria-guide.md) — 通过实际示例了解实时与批次进入模式
* [发送多渠道消息](journeys-uc.md#send-multi-channel-messages) — 结合读取受众、反应事件、电子邮件和推送的端到端用例
* [向订阅者发送消息](message-to-subscribers-uc.md) — 使用“读取受众”批量激活受众的端到端用例
