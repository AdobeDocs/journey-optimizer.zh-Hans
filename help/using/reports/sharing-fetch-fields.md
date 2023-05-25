---
solution: Journey Optimizer
product: journey optimizer
title: journeyStep 事件数据提取字段
description: journeyStep 事件数据提取字段
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 7%

---

# journeyStep 事件数据提取字段 {#sharing-fetch-fields}

此字段组将由journeyStepEvent和journeyStepProfileEvent共享。

在步骤处理期间，我们可以在字段组上获取N个数据。

## fetchTotalTime {#fetchtotaltime-field}

在步骤处理期间用于数据提取的总时间（以毫秒为单位）。

类型： long

## fetchTypeInError {#fetchtypeinerror-field}

定义错误获取是在Adobe Experience Platform上还是在自定义数据源上。

类型：字符串

值：
* aep
* 自定义

## fetchError {#fetcherror-field}

处理数据获取时发生的错误类型。

类型：字符串

值：
* http
* 上限
* 超时
* error

## fetchErrorCode {#fetcherrorcode-field}

提取错误的代码。 如果错误包含代码（例如HTTP代码），则会出现。 例如，如果actionExecError为http，则代码404表示HTTP 404错误。

类型：字符串

## fetchOriginError {#fetchoriginerror-field}

在以下两种情况下，可能会出现超时：

* 在第一次尝试时，执行操作。 在这种情况下，执行未完成，因此没有基础错误
* 重试：在这种情况下，actionExecOrigError/actionExecOrigErrorCode描述在重试之前尝试遇到的错误。

例如，正在从统一配置文件服务中获取数据，第一次尝试时返回HTTP 500错误。 将重试获取，但2次尝试的持续时间超过了超时。 然后，该操作执行将标记为超时。 操作部分将如下所示：

```
    ...
    "fetchTypeInError": "aep",
    "fieldgroupIdInError": "MyProfileFieldgroup",
    "fetchError": "timedout",
    "fetchOrigError": "http",
    "fetchOrigErrorCode": "500"
```

类型：字符串

## fetchOriginErrorCode {#fetchoriginerrorcode-field}

系统提供的错误代码 [!DNL Journey Optimizer] 正在查询。 例如，可以是404、500等。

类型：字符串

## fetchCount {#fetchcount-field}

获取数据的次数，不考虑源的类型。

类型： long

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

从Adobe Experience Platform获取数据所花费的总时间（以毫秒为单位）。 注释：此时间量从引擎将扩充事件发送到扩充服务并接收响应时开始计算。

类型： long

## fetchPlatformCount {#fetchplatformcount-field}

从Adobe Experience Platform获取数据的次数。

类型： long

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

获取自定义数据的时间（以毫秒为单位）。 注释：此时间量从引擎将扩充事件发送到扩充服务并接收响应时开始计算

类型： long

## fetchCustomCount {#fetchcustomcount-field}

从外部系统获取自定义数据的次数。

类型： long
