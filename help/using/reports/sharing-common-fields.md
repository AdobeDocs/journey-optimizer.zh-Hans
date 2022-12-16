---
solution: Journey Optimizer
product: journey optimizer
title: journeysteps事件常用字段
description: journeysteps事件常用字段
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 9%

---

# journeysteps事件常用字段 {#sharing-common-fields}

此字段组将由journeyStepEvent和journeyStepProfileEvent共享。

这些是常见的XDM字段， [!DNL Journey Optimizer] 发送到Adobe Experience Platform。 对于历程中处理的每个步骤，都将发送通用字段。 自定义操作和扩充使用更多特定字段。

其中某些字段仅在特定处理模式（操作执行、数据获取等）中可用 以限制事件的大小。

## 入口 {#entrance-field}

指示用户是否已进入历程。 如果不存在，则我们假定该值为false。

类型：布尔值

值：true/false

## 重入 {#reentrance-field}

指示用户是否使用同一实例重新进入历程。 如果不存在，则我们假定该值为false。

类型：布尔值

值：true/false

## instanceEnded {#instance-ended-field}

指示实例是否已结束（成功或未成功）。

类型：布尔值

## eventID {#eventid-field}

处理中的事件ID，用于步骤处理。 如果事件是外部事件，则值为其eventId。 如果事件是内部事件，则值为内部eventId（例如scheduledNotificationReceived、exceutedAction等）。

类型：字符串

## nodeID {#nodeid-field}

客户端节点id（从画布中）。

类型：字符串

## stepID {#stepdid-field}

当前正在处理的步骤的唯一ID。

类型：字符串

## stepName {#stepname-field}

当前正在处理的步骤的名称。

类型：字符串

## stepType {#steptype-field}

步骤的类型。

类型：字符串

可能值：

* 条件
* 操作
* 调度程序
* 计时器

## stepStatus {#stepstatus-field}

完成处理（触发步骤事件）后，步骤的状态，表示步骤的状态。

类型：字符串

状态可以是：

* 结束：该步骤没有过渡，且其处理已成功结束。
* 错误：步骤处理引发错误。
* 过渡：该步骤正在等待事件转换到另一个步骤。
* 上限：在操作或扩充期间引发的上限错误导致步骤失败。
* timedout:在操作或扩充过程中引发的超时错误导致步骤失败。
* instanceTimedout:该步骤已停止处理，因为实例已达到其超时。

## journeyID {#journeyid-field}

历程的ID。

类型：字符串

## journeyVersionID {#journeyversionid-field}

历程版本的ID。 此ID表示对历程的身份引用，对于journeyStepEvent。

类型：字符串

## journeyVersionName {#journeyversionname-field}

历程版本的名称。

类型：字符串

## journeyVersion {#journeyversion-field}

历程版本的版本。

类型：字符串

## instanceID {#instanceid-field}

历程实例的内部ID。

类型：字符串

## externalKey {#externalkey-field}

从事件提取的外部键值以处理它。

类型：字符串

## parentStepID {#parenstepid-field}

实例中当前已处理步骤的父级的步骤ID。

类型：字符串

## parentStepName {#parentstepname-field}

当前步骤的父项的步骤名称。

类型：字符串

## parentTransitionID {#parenttransitionid-field}

将实例引入已处理步骤的过渡的ID。

类型：字符串

## parentTransitionName {#parenttransitionname-field}

将实例引入已处理步骤的过渡的名称。

类型：字符串

## inTest {#intest-field}

指示此历程是否处于测试模式。

类型：布尔值

## processingTime {#processingtime-field}

从实例步骤进入到处理结束的总时间（以毫秒为单位）。

类型：long

## instanceType {#instancetype-field}

指示实例类型（如果是批类型或单一类型）。

类型：字符串

值：批次/单一

## recurrenceIndex {#recurrenceindex-field}

当历程是批处理并且是定期的时，循环的索引（首次运行的recurrenceIndex = 1）。

类型：long

## isBatchToUnimation {#isbatchtounitary-field}

指示此单一实例是否已从批处理实例触发。

类型：布尔值

## batchExternalKey {#batchexternalkey-field}

批处理事件的外部键。

类型：字符串

## batchInstanceID {#batchinstanceid-field}

这是批量实例ID。

类型：字符串

## batchUneminaryBranchID {#batchunitarybranchid-field}

如果实例是从批处理实例触发的，则表示唯一的分支ID。

类型：字符串
