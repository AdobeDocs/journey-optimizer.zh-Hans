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
source-git-commit: 1cf62f949c1309b864ccd352059a444fd7bd07f0
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 9%

---

# journeysteps事件常用字段 {#sharing-common-fields}

此字段组将由journeyStepEvent和journeyStepProfileEvent共享。

这些是常见的XDM字段， [!DNL Journey Optimizer] 发送至Adobe Experience Platform。 将为历程中处理的每个步骤发送公共字段。 更具体的字段用于自定义操作和增强。

其中某些字段仅可用于特定的处理模式（操作执行、数据获取等） 以限制事件大小。

## 入口 {#entrance-field}

指示用户是否已进入历程。 如果不存在，则假定值为false。

类型：布尔值

值： true/false

## 重新进入 {#reentrance-field}

指示用户是否已使用同一实例重新进入历程。 如果不存在，则假定值为false。

类型：布尔值

值： true/false

## instanceEnd {#instance-ended-field}

指示实例是否已结束（成功或失败）。

类型：布尔值

## eventID {#eventid-field}

处理中的事件ID，用于步骤处理。 如果事件是外部事件，则该值为其eventId。 如果事件是内部事件，则该值为内部eventId（例如scheduledNotificationReceived、executedAction等）。

类型：字符串

## nodeID {#nodeid-field}

客户端节点ID（来自画布）。

类型：字符串

## 步骤ID {#stepdid-field}

当前正在处理的步骤的唯一ID。

类型：字符串

## stepName {#stepname-field}

当前正在处理的步骤的名称。

类型：字符串

## 步骤类型 {#steptype-field}

步骤的类型。

类型：字符串

可能的值：

* 条件
* 操作
* 调度程序
* 计时器

## stepStatus {#stepstatus-field}

步骤的状态，表示步骤的状态，表示步骤的处理何时完成（且步骤事件已触发）。

类型：字符串

状态可以是：

* 已结束：步骤没有过渡，其处理已成功结束。
* 错误：步骤处理引发错误。
* 过渡：步骤正在等待事件过渡到另一个步骤。
* capped：步骤因操作或扩充期间引发的上限错误而失败。
* 超时：步骤因超时错误而失败，该错误在操作或扩充期间引发。
* instanceTimedout：步骤已停止处理，因为实例已达到超时。

## journeyID {#journeyid-field}

历程的ID。

类型：字符串

## journeyVersionID {#journeyversionid-field}

历程版本的ID。 对于journeyStepEvent，此id表示对历程的身份引用。

类型：字符串

>[!NOTE]
>
>出于故障诊断目的，我们建议在查询历程时使用journeyVersionID，而不是journeyVersionName。

## journeyVersionName {#journeyversionname-field}

历程版本的名称。

类型：字符串

>[!NOTE]
>
>出于故障诊断目的，我们建议在查询历程时使用journeyVersionID，而不是journeyVersionName。

## journeyVersion {#journeyversion-field}

历程版本的版本。

类型：字符串

## instanceID {#instanceid-field}

历程实例的内部ID。

类型：字符串

## externalkey {#externalkey-field}

从事件中提取的外部键以对其进行处理。

类型：字符串

## parentStepID {#parenstepid-field}

实例中当前已处理步骤的父步骤ID。

类型：字符串

## parentStepName {#parentstepname-field}

当前步骤的父级步骤名称。

类型：字符串

## parentTransitionID {#parenttransitionid-field}

将实例带到已处理步骤的过渡ID。

类型：字符串

## parentTransitionName {#parenttransitionname-field}

将实例带到已处理步骤的过渡的名称。

类型：字符串

## inTest {#intest-field}

指示此历程是否处于测试模式。

类型：布尔值

## processingTime {#processingtime-field}

从实例步骤进入到处理结束的总时间（以毫秒为单位）。

类型： long

## instancetype {#instancetype-field}

指示实例类型（批次）或单一实例类型。

类型：字符串

值：批次/单一

## recurrenceIndex {#recurrenceindex-field}

如果历程是批次和周期性的（第一次运行具有recurrenceIndex = 1），则为周期性索引。

类型： long

## isBatchToUnitary {#isbatchtounitary-field}

指示此单一实例是否已从批处理实例触发。

类型：布尔值

## batchExternalKey {#batchexternalkey-field}

批次事件的外部键。

类型：字符串

## batchInstanceID {#batchinstanceid-field}

这是批次实例ID。

类型：字符串

## batchUnitaryBranchID {#batchunitarybranchid-field}

如果实例是从批处理实例触发的，则为统一分支ID。

类型：字符串
