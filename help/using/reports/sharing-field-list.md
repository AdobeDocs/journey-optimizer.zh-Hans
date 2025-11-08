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
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 9%

---

# 步骤事件字段列表 {#sharing-field-list}

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

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| ID | 字符串 | 给定历程的标识符 |
| 版本ID | 字符串 | 历程版本的ID。 此id表示历程的身份 |
| name | 字符串 | 历程的名称 |
| 描述 | 字符串 | 历程描述 |
| 版本 | 字符串 | 版本，表示为`major`.`minor` |

## 个人资料 {#profile-field}

此字段组特定于journeyStepEvent：此事件与历程相关，不具有identityMap，描述配置文件身份（如果有）。

对于journeyStepEvent，我们还需要添加与标识相关的字段：

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| ID | 字符串 | 用户档案标识符标识历程中发送/使用的用户档案。 例如： foo@adobe.com。 |
| 命名空间 | 字符串 | 此字段描述在历程中使用的配置文件引用的命名空间。 例如：电子邮件、ECID |

## serviceEvents {#servicevents-field}

此mixin包含与用户档案导出作业对应的所有字段。 这些事件是根据&#x200B;**读取受众**&#x200B;活动生成的，用于跟踪受众导出操作（已排队、已启动、已完成、错误）的生命周期。 与常规步骤事件不同，serviceEvents不绑定到单个配置文件，而是绑定到读取受众节点本身，这意味着它们可能没有关联的配置文件标识符。

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| ID | 字符串 | 触发的受众导出作业的标识符 |
| 状态 | 字符串 | 受众导出作业的状态：已排队、已启动、已完成 |
| exportCountTotal | 整数 | 受众导出作业的最大可能值 |
| exportCountRealized | 整数 | 通过作业导出的实际受众数 |
| exportCountFailed | 整数 | 通过作业导出时失败的受众数 |
| exportSegmentId | 字符串 | 正在导出的受众的标识符 |
| 事件类型 | 字符串 | 指示它是错误事件还是信息事件的事件类型：信息、错误 |
| eventcode | 字符串 | 指示相应eventType原因的错误代码 |

在本节[中了解有关eventTypes &#x200B;](#discarded-events)的更多信息。

## stepEvents {#stepevents-field}

此类别包含原始步骤事件字段。 请参阅此[章节](../reports/sharing-legacy-fields.md)。


## 对历程步骤事件中丢弃的事件类型进行故障排除  {#discarded-events}

在查询包含`eventCode = 'discard'`的记录的历程步骤事件时，您可能会遇到多个eventTypes。

以下是最常丢弃`eventTypes`的定义、常见原因和故障排除步骤：

* **EXTERNAL_KEY_COMPUTATION_ERROR**：系统无法从事件数据计算客户的唯一标识符（外部键）。

  **常见原因**：事件有效负载中缺少客户标识符（例如电子邮件、客户ID）或标识符格式不正确。

  **故障排除**：检查所需标识符的事件配置，确保事件数据完整且格式正确。

* 历程 **NO_INTEREST_EVENT_FOR_SEGMENTMEMBERSHIP_EVENT**：已收到区段资格事件，但没有将任何旅程配置为响应此区段。

  **常见原因**：没有历程使用区段作为触发器，历程处于草稿/停止状态，或区段ID不匹配。

  **故障排除**：确保至少有一个历程处于活动状态并为该区段配置了历程，请验证区段ID。

* **历程_INSTANCE_ID_NOT_CREATE**：系统无法为客户创建历程实例。

  **常见原因**：重复的事件、高事件量、系统资源约束。

  **故障排除**：实施重复数据删除，避免流量尖峰，优化历程设计，如果持续存在，请联系支持人员。

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
* [内置架构词典](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=zh-Hans)

