---
title: 步骤事件字段列表
description: 步骤事件字段列表
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 16%

---

# 步骤事件字段列表 {#sharing-field-list}

Step event fields are organized by category.

* Debug information fields
* 历程字段
* 用户档案字段
* Service event fields

## debugInfo {#debuginfo-field}

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| requestId | 字符串 | The request Id used by Journey Orchestration to track the flow of a request. |

## journey {#journey-field}

This field group is used in the journey schema (in relation with journeyStepEvent). It contains the following fields:

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| ID | 字符串 | Identifier for the given Journey |
| 版本ID | 字符串 | 历程版本的ID。 This id represents the identity of a journey |
| name | 字符串 | 历程的名称 |
| description | 字符串 | Description of the journey |
| 版本 | 字符串 | version, represented as `major`.`minor` |

## profile {#profile-field}

This field group is specific to journeyStepEvent: this event is in relation with journey, and doesn’t have the identityMap, describing the profile identity, if any.

For journeyStepEvent, we need also to add fields related to the identity:

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| ID | 字符串 | Profile identifier identifies the profile sent/used in a journey. 例如：foo@adobe.com。 |
| namespace | 字符串 | 此字段描述在历程中使用的配置文件引用的命名空间。 E.g: Email, ECID |

## serviceEvents {#servicevents-field}

此混合包含与用户档案导出作业对应的所有字段。

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| ID | 字符串 | The identifier of the segment export job triggered |
| 状态 | 字符串 | 区段导出作业的状态：已排队，已启动，已完成 |
| exportCountTotal | 整数 | 区段导出作业的最大可能值 |
| exportCountReatived | 整数 | The actual number of segments exported through the job |
| exportCountFailed | 整数 | 通过作业导出时，区段数失败 |
| exportSegmentID | 字符串 | 要导出的区段的标识符 |
| eventType | 字符串 | 事件类型，用于指示它是否为信息事件的错误事件：信息，错误 |
| eventCode | 字符串 | 指示相应eventType原因的错误代码 |

## stepEvents {#stepevents-field}

This category contains the original step event fields. 请参阅 [部分](../reports/sharing-legacy-fields.md).
