---
solution: Journey Optimizer
product: journey optimizer
title: journeyStep 事件操作执行字段
description: journeyStep 事件操作执行字段
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: b93d2288156713ac7479eef491f6104df1955a18
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 2%

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

`actionExecutionTime`字段表示执行操作所花费的总时间（以毫秒为单位），包括请求在队列中等待所花费的时间（如果配置了限制并达到了速率限制）以及实际执行时间（包括到外部端点的网络延迟）。

`Timestamp`字段指示操作执行的结束时间。 要确定用户档案何时进入自定义操作节点，请从`actionExecutionTime`中减去`Timestamp`。

例如，如果`Timestamp`为“2025-02-04 09:39:03 UTC”，`actionExecutionTime`为1,813,227毫秒（~31分钟），则配置文件大约在“2025-02-04 09:08:32 UTC”进入节点。


## actionExecutionError {#actionexecutionerror-field}

调用操作时发生的错误类型。

类型：字符串

值：

* http
* 上限
* timeout
* error

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

## actionOriginEndpoint {#actionoriginendpoint}

操作中使用的自定义操作端点的URI。

类型：字符串

## actionOriginMethod {#actionoriginmethod}

这描述了HTTP请求(GET或POST)中使用的方法。

类型：字符串

## actionOriginIsMTLS {#actionoriginismtls}

此属性描述是否为端点启用MTLS。

类型：布尔值

## actionIsProxy {#actionisproxy}

此参数描述是否将具有定义的IP地址范围的HTTP代理用于调用。

类型：布尔值

## actionExecutionOriginStartTime {#actionexecutionoriginstarttime}

此属性描述启动HTTP请求的时间戳。 如果重试，这是启动最终重试尝试的时间戳。 时间戳使用UTC时区的ISO8601格式。

请注意，此时间戳通常在用户档案进入自定义操作节点后稍后，或者在遇到节流时显着进入节点。

类型：时间戳

## actionExecutionOriginTime {#actionexecutionorigintime}

这描述了HTTP调用的响应时间。 在重试的情况下，这是最后一次重试所花费的时间。 它测量从发起HTTP请求到从服务器返回完整响应的时间。 请注意，这排除了在限制情况下在队列中等待的任何时间。

类型： long

## actionIsThrottled {#actionisthrottled}

此属性描述是否为端点启用限制。

类型：布尔值

## actionWaitTime {#actionwaittime}

这描述了何时达到节流端点的配置速率限制，调用将按配置的速率排队和处理。 此字段报告呼叫在执行之前在队列中等待的时间。 仅在actionIsThrottled为true时指==。

类型： long

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
