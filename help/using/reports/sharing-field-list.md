---
solution: Journey Optimizer
product: journey optimizer
title: 步骤事件字段列表
description: 步骤事件字段列表
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
TQID: https://experienceleague.adobe.com/7sYxw--oKKa6SnRgoXnwFxme5n-6L4pe9SR-AKZOmHA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 806
ht-degree: 8%

---

# 步骤事件字段列表 {#sharing-field-list}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;引用按类别组织的历程步骤事件字段，包括调试、历程、配置文件和服务事件字段，以及舍弃事件类型的疑难解答。

>[!ENDSHADEBOX]

步骤事件字段按类别组织。

* 调试信息字段
* 历程字段
* 配置文件字段
* 服务事件字段

对于identityMap属性，默认将主标识定义为“primary = true”。

## debugInfo {#debuginfo-field}

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| requestid | 字符串 | Journey Optimizer用于跟踪请求流的请求ID。 |

## 历程 {#journey-field}

此字段组在历程模式中使用（与journeyStepEvent相关）。 它包含以下字段：

| 字段名称 | 类型 | 说明 |
|---|---|------------|
| ID | 字符串 | 给定历程的标识符 |
| 版本ID | 字符串 | 历程版本的ID。 此id表示历程的身份 |
| name | 字符串 | 历程的名称 |
| 描述 | 字符串 | 历程描述 |
| version | 字符串 | 版本，表示为`major`.`minor` |

## 个人资料 {#profile-field}

此字段组特定于journeyStepEvent：此事件与历程相关，不具有identityMap，描述配置文件身份（如果有）。

对于journeyStepEvent，我们还需要添加与标识相关的字段：

| 字段名称 | 类型 | 说明 |
|---|---|------------|
| ID | 字符串 | 用户档案标识符标识历程中发送/使用的用户档案。 例如： foo@adobe.com。 |
| namespace | 字符串 | 此字段描述在历程中使用的配置文件引用的命名空间。 例如：电子邮件、ECID |

## serviceEvents {#servicevents-field}

此mixin包含与用户档案导出作业对应的所有字段。 这些事件是根据&#x200B;**读取受众**&#x200B;活动生成的，用于跟踪受众导出操作（已排队、已启动、已完成、错误）的生命周期。 与常规步骤事件不同，serviceEvents不绑定到单个配置文件，而是绑定到读取受众节点本身，这意味着它们可能没有关联的配置文件标识符。

| 字段名称 | 类型 | 说明 |
|---|---|------------|
| ID | 字符串 | 触发的受众导出作业的标识符 |
| 状态 | 字符串 | 受众导出作业的状态：已排队、已启动、已完成 |
| exportCountTotal | 整数 | 受众导出作业的最大可能值 |
| exportCountRealized | 整数 | 通过作业导出的实际受众数 |
| exportCountFailed | 整数 | 通过作业导出时失败的受众数 |
| exportSegmentId | 字符串 | 正在导出的受众的标识符 |
| 事件类型 | 字符串 | 指示它是错误事件还是信息事件的事件类型：信息、错误 |
| eventcode | 字符串 | 指示相应eventType原因的错误代码 |

在本节](#discarded-events)中了解有关eventTypes [的更多信息。

## stepEvents {#stepevents-field}

此类别包含原始步骤事件字段。 请参阅此[章节](../reports/sharing-legacy-fields.md)。


## 对历程步骤事件中丢弃的事件类型进行故障排除  {#discarded-events}

在查询包含`eventCode = 'discard'`的记录的历程步骤事件时，您可能会遇到多个eventTypes。

以下是最常丢弃`eventTypes`的定义、常见原因和故障排除步骤：

* **EXTERNAL_KEY_COMPUTATION_ERROR**：系统无法从事件数据计算客户的唯一标识符（外部键）。

  **常见原因**：事件有效负载中缺少客户标识符（例如电子邮件、客户ID）或标识符格式不正确。

  **故障排除**：检查所需标识符的事件配置，确保事件数据完整且格式正确。

* **NO_INTEREST_EVENT_FOR_SEGMENTMEMBERSHIP_EVENT**：已收到区段资格事件，但没有将任何旅程配置为响应此区段。

  **常见原因**：没有历程使用区段作为触发器，历程处于草稿/停止状态，或区段ID不匹配。

  **故障排除**：确保至少有一个历程处于活动状态并为该区段配置了历程，请验证区段ID。

* **历程_INSTANCE_ID_NOT_CREATED**：系统未能为客户创建历程实例。

  **常见原因**：重复的事件、高事件量、系统资源约束。

  **故障排除**：实施重复数据删除，避免流量尖峰，优化历程设计，[联系支持人员](../start/user-interface.md#support-ticket-guidelines)（如果持续）。

* **maxInstanceStackEventsReacted**：历程运行时已达到给定历程版本每个配置文件事件栈栈10个事件的内部限制。

  **常见原因**：配置文件的历程实例在长时间运行的步骤（例如，长时间等待、缓慢扩充或自定义操作重试）上被阻止，同一配置文件的事件也在该历程中使用，累积超过10个事件的限制。

  **故障排除**：减少可能频繁重新触发的路径上的长时间运行步骤、减少退回或消除重复上游事件，并将长时间方案拆分为多个历程。 这是安全护栏，限制不可配置；其他事件将被丢弃，直到栈栈排干。 有关更多指导，请参阅[由于历程实例被阻止而丢弃的事件](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached)。

* **EVENT_WITH_NO_Journey**：已收到一个历程，但没有将活动历程配置为响应它

  **常见原因**：事件名称/ID不匹配、历程未发布、沙盒/组织错误、测试模式/配置文件不匹配。

  **故障排除**：验证事件和历程配置，检查历程状态，使用调试工具。

* 对于暂停的历程中发生的丢弃：

   * **PAUSED_Journey_VERSION**：放弃在历程进入点发生的操作
   * **历程_IN_PAUSED_STATE**：放弃历程中用户档案时发生的操作

  在[暂停历程部分](../building-journeys/journey-pause.md#discards-troubleshoot)中了解有关这些事件的更多信息以及如何对其进行故障排除。

## 其他资源

* [数据集查询示例 — 历程步骤事件](../data/datasets-query-examples.md#journey-step-event)。
* [查询示例 — 基于事件的查询](query-examples.md#event-based-queries)。
* [查询示例 — 业务规则查询](query-examples.md#business-rules-queries)。
* [内置模式词典](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=zh-Hans)

