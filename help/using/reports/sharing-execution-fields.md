---
solution: Journey Optimizer
product: journey optimizer
title: journeyStep 事件操作执行字段
description: journeyStep 事件操作执行字段
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 5%

---

# journeyStep 事件操作执行字段 {#sharing-execution-fields}

此字段组将由journeyStepEvent和journeyStepProfileEvent共享。

如果步骤包含要处理的操作，则这些字段将被添加到事件有效负载中。

## actionID {#actionid-field}

正在执行的操作的ID。

类型：字符串

## actionName {#actionname-field}

操作的名称。 如果未设置名称，则采用stepName。

类型：字符串

## actionType {#actionType-field}

操作的类型。

类型：字符串

## actionParameterized {#actionparameterized-field}

指示操作是否已参数化。

类型：布尔值

## actionExecutionTime {#actionexecutiontime-field}

执行当前操作所用的时间（以毫秒为单位）。

类型： long

## actionExecutionError {#actionexecutionerror-field}

调用操作时发生的错误类型。

类型：字符串

值：
* http
* 上限
* timeout
* 错误

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

操作执行错误的代码。 如果错误包含代码（如HTTP代码），则显示。

类型：字符串

## actionExecutionOriginError {#actionexecutionoriginerror-field}

在以下两种情况下，可能会出现超时：

* 在第一次尝试时，执行操作。 在这种情况下，执行未完成，因此不存在基础错误
* 重试：在这种情况下，actionExecOrigError/actionExecOrigErrorCode将描述在重试之前尝试时遇到的错误。

例如，会发送电子邮件，并在第一次尝试时返回HTTP 500错误。 将重试获取，但两次尝试的持续时间超过了超时。 然后，操作执行将标记为超时。 操作部分将如下所示：

```
    ...
    "actionId": "myActionId",
    "actionName": "My mail sending",
    "actionType": "acsRestAction",
    "actionParameterized": true,
    "actionExecError": "timedout",
    "actionExecOrigError": "http",
    "actionExecOrigErrorCode": "500"
```

类型：字符串

## actionExecutionOriginCode {#actionexecutionorigincode-field}

actionExecOrigError的错误代码。

类型：字符串

## actionBusinessType {#actionbusinesstype-field}

指示操作的类型。

值：

* 内置
* ACS电子邮件
* ACS短信
* ACS推送
* 客户
* Epsilon
* ...

类型：字符串

## deliveryJobId {#deliveryjobid-field}

此字段描述批处理历程的投放作业ID。

类型：字符串

## batchDeliveryID {#batchdeliveryid-field}

此字段描述批处理历程的投放ID。

类型：字符串

## fromSegmentTrigger {#fromsegmenttrigger-field}

此属性描述批处理历程是否从受众区段触发。

类型：布尔值

## actionSchedulerCount {#actionschedulercount-field}

在步骤处理期间发送到调度程序服务的调度程序通知请求的计数。

类型： long
