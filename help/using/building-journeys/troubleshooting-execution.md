---
solution: Journey Optimizer
product: journey optimizer
title: 对实时历程执行进行故障诊断
description: 了解如何对实时历程执行中的错误进行故障排除
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 故障排除，故障排除，历程，检查，错误
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
version: Journey Orchestration
source-git-commit: 22c3c44106d51032cd9544b642ae209bfd62d69a
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 23%

---

# 对实时历程执行进行故障诊断 {#troubleshooting-execution}

在此部分中，了解如何对历程事件进行故障排除，检查用户档案是否进入您的历程，用户档案如何在历程中导航，以及是否发送了消息。

您还可以在测试或发布历程之前对错误进行故障排除。 在此页面[上了解](troubleshooting.md)的方式。

如果您使用入站操作，请在此页面[上了解如何对其进行故障排除](troubleshooting-inbound.md)。

## 检查事件是否正确发送 {#checking-that-events-are-properly-sent}

历程的起点永远是事件。您可以使用 Postman 等工具执行测试。

您可以检查通过这些工具发送的 API 调用是否正确发送。如果返回错误，则表示您的调用有问题。再次检查有效负载、标题（特别是组织 ID）以及目标 URL。您可以询问管理员要点击的正确 URL。

事件不会直接从源推送到历程。 事实上，历程依赖于Adobe Experience Platform的流摄取API。 因此，如果出现与事件相关的问题，您可以参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"}以了解流摄取API故障排除。

如果您的历程无法启用测试模式并出现错误`ERR_MODEL_RULES_16`，请确保使用的事件在使用渠道操作时包含[标识命名空间](../audience/get-started-identity.md)。

身份命名空间用于唯一标识测试配置文件。 例如，如果电子邮件用于识别测试用户档案，则应选择身份命名空间&#x200B;**Email**。 如果唯一标识符是电话号码，则应选择身份命名空间&#x200B;**电话**。

## 检查人员是否进入历程 {#checking-if-people-enter-the-journey}

历程报表实时衡量人员进入旅程。

如果您成功发送事件，但未看到有人进入历程，则意味着在事件发送和事件接收之间出现问题。

您可以通过以下问题开始进行故障诊断：

* 是否确定期待传入事件的历程处于测试模式或处于实时状态？
* 是否在从有效负载预览复制有效负载之前保存了您的事件？
* 您的事件有效负载是否包含事件 ID？
* 您是否点击了正确的 URL？
* 您是否使用“事件配置”窗格中的有效负载结构预览遵循了流摄取 API 的有效负载结构？请参阅[此页](../event/about-creating.md#preview-the-payload)。
* 您在事件标头中使用了正确的键值对吗？

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

## 检查人员在历程中的导航方式 {#checking-how-people-navigate-through-the-journey}

历程报表测量旅程中个人的进度。 很容易识别人员在何处被拦住以及为什么被拦住。

以下是一些要检查的内容：

* 是因为除人员外的情况吗？例如，条件为“性别=男性”，而该人员为女性。如果条件不太复杂，此检查可由商业用户执行。
* 是由于调用数据源时没有响应吗？当历程正在测试时，此信息可在测试模式日志中查看。当历程处于实时状态时，管理员可以测试对数据源的直接调用并检查收到的答案。管理员还可以重复历程并进行测试。

## 检查消息是否发送成功 {#checking-that-messages-are-sent-successfully}

如果人员在历程中以正确的方式流动，但没有收到他们应该收到的消息，您可以检查：

* [!DNL Journey Optimizer]已正确考虑发送邮件的请求。 商业用户可以访问应发送的消息，并检查最新执行的时间是否与历程的执行时间对应。 他们还可以检查收到的最新API调用/事件。
* [!DNL Journey Optimizer]已成功发送消息。 检查历程报告以确保没有错误。

对于通过自定义操作发送的消息，在历程测试中可以检查的唯一一点就是自定义操作系统的调用是否会导致错误。 如果与自定义操作关联的对外部系统的调用不会导致错误，但也不会导致消息发送，则应对外部系统进行一些调查。

## 了解历程步骤事件中的重复条目 {#duplicate-step-events}

### 为什么我会看到多个具有相同历程实例、配置文件、节点和请求ID的条目？

在查询历程步骤事件数据时，您可能会偶尔观察到同一旅程执行中显示的重复日志条目。 这些条目共享以下项的相同值：

* `profileID` — 配置文件标识
* `instanceID` — 历程实例标识符
* `nodeID` — 特定历程节点
* `requestID` — 请求标识符

但是，这些条目具有&#x200B;**不同的`_id`值**，这是将此方案与实际数据重复区分开的关键指示器。

### 导致此行为的原因是什么？

出现这种情况是由于Adobe Journey Optimizer微服务架构中的后端自动缩放操作（也称为“重新平衡”）。 在高负载或系统优化期间：

1. 旅程步骤事件开始处理并记录到历程步骤事件数据集
2. 自动缩放操作跨服务实例重新分配工作负载
3. 另一个服务实例可能会重新处理同一事件，从而创建具有不同`_id`的第二个日志条目

这是预期的系统行为，**按设计工作**。

### 是否对历程执行或消息投放有任何影响？

**否。**&#x200B;影响仅限于日志记录。 Adobe Journey Optimizer在消息执行层具有内置的重复数据删除机制，可确保：

* 只向每个用户档案发送一条消息（电子邮件、短信、推送通知等）
* 操作只执行一次
* 历程执行正确进行

您可以通过查询`ajo_message_feedback_event_dataset`或检查操作执行日志来验证这一点 — 您将看到实际只发送了一封邮件，尽管历程步骤事件条目重复。

### 如何在查询中识别这些案例？

分析历程步骤事件数据时：

1. **检查`_id`字段**： True系统级重复项具有相同的`_id`。 不同的`_id`值指示与上述重新平衡方案不同的日志条目。

2. **验证消息投放**：使用消息反馈数据进行交叉引用，以确认只发送了一封消息：

   ```sql
   SELECT
     timestamp,
     _experience.customerJourneyManagement.messageExecution.messageExecutionID,
     _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
   FROM ajo_message_feedback_event_dataset
   WHERE
     _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journeyVersionID>'
     AND TO_JSON(identityMap) like '%<profileID>%'
   ORDER BY timestamp DESC;
   ```

3. **按唯一标识符分组**：对执行进行计数时，请使用`_id`获取准确的计数：

   ```sql
   SELECT
     COUNT(DISTINCT _id) as unique_executions
   FROM journey_step_events
   WHERE
     _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
     AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID>'
   ```

### 如果我观察到这种情况，应该怎么办？

这是正常的系统行为，**无需执行任何操作**。 重复的日志记录并不指示您的历程配置或消息投放存在问题。

如果您基于历程步骤事件构建Reports/Analytics：

* 使用`_id`作为计算唯一事件的主键
* 分析消息投放时与消息反馈数据集交叉引用
* 请注意，定时分析可能会显示相互聚集的几秒内的条目

有关查询历程步骤事件的详细信息，请参阅[查询示例](../reports/query-examples.md)。
