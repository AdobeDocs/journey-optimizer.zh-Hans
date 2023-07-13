---
solution: Journey Optimizer
product: journey optimizer
title: 步骤事件字段列表
description: 步骤事件字段列表
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 18%

---

# 步骤事件字段列表 {#sharing-field-list}

步骤事件字段按类别组织。

* 调试信息字段
* 历程字段
* 配置文件字段
* 服务事件字段

## debugInfo {#debuginfo-field}

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| requestid | 字符串 | Journey Optimizer用于跟踪请求流的请求ID。 |

## 历程 {#journey-field}

此字段组在历程模式中使用（与journeyStepEvent相关）。 它包含以下字段：

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| ID | 字符串 | 给定历程的标识符 |
| 版本ID | 字符串 | 历程版本的ID。 此ID表示历程的身份 |
| name | 字符串 | 历程的名称 |
| 描述 | 字符串 | 历程描述 |
| version | 字符串 | 版本，表示为 `major`.`minor` |

## 个人资料 {#profile-field}

此字段组特定于journeyStepEvent：此事件与历程相关，不具有描述配置文件身份（如果有）的identityMap。

对于journeyStepEvent，我们还需要添加与标识相关的字段：

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| ID | 字符串 | 配置文件标识符标识历程中发送/使用的配置文件。 例如： foo@adobe.com。 |
| namespace | 字符串 | 此字段描述历程中使用的配置文件引用的命名空间。 例如：电子邮件、ECID |

## serviceEvents {#servicevents-field}

此mixin包含与配置文件导出作业对应的所有字段。

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| ID | 字符串 | 触发的受众导出作业的标识符 |
| 状态 | 字符串 | 受众导出作业的状态：已排队、已启动、已完成 |
| exportCountTotal | 整数 | 受众导出作业的最大可能值 |
| exportCountRealized | 整数 | 通过作业导出的实际受众数量 |
| exportCountFailed | 整数 | 通过作业导出时失败的受众数量 |
| exportSegmentID | 字符串 | 正在导出的受众的标识符 |
| 事件类型 | 字符串 | 指示它是否为信息事件的错误事件的事件类型：信息、错误 |
| eventcode | 字符串 | 指示相应eventType原因的错误代码 |

## stepEvents {#stepevents-field}

此类别包含原始步骤事件字段。 请参阅此[章节](../reports/sharing-legacy-fields.md)。
