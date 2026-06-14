---
solution: Journey Optimizer
product: journey optimizer
title: journeyStep 事件数据提取字段
description: journeyStep 事件数据提取字段
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
TQID: https://experienceleague.adobe.com/obaiLWD6yq0dZ5ZhE69q-iLHzI99ll7XJnMNlOpJp1A
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 4%

---

# journeyStep 事件数据提取字段 {#sharing-fetch-fields}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;在步骤处理期间从Adobe Experience Platform或自定义源扩充数据时，引用添加到旅程步骤事件的数据提取字段。

>[!ENDSHADEBOX]

此字段组将由journeyStepEvent和journeyStepProfileEvent共享。

在步骤处理期间，我们可以在字段组上获取N个数据。

## fetchTotaltime {#fetchtotaltime-field}

在步骤处理期间进行数据提取所花费的总时间（以毫秒为单位）。

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

获取错误的代码。 如果错误包含代码（如HTTP代码），则显示。 例如，如果actionExecError为http，则代码404表示HTTP 404错误。

类型：字符串

## fetchOriginError {#fetchoriginerror-field}

在以下两种情况下，可能会出现超时：

* 在第一次尝试时，将执行该操作。 在这种情况下，执行未完成，因此不存在基础错误
* 重试：在这种情况下，actionExecOrigError/actionExecOrigErrorCode将描述在重试之前尝试时遇到的错误。

例如，正在从统一配置文件服务中获取数据，并且在第一次尝试时返回HTTP 500错误。 将重试获取，但两次尝试的持续时间超过了超时。 然后，操作执行将标记为超时。 操作部分将如下所示：

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

系统[!DNL Journey Optimizer]提供的错误代码正在查询。 例如，它可以是404、500等。

类型：字符串

## fetchCount {#fetchcount-field}

获取数据的次数，不考虑源的类型。

类型： long

## fetchPlatformTotaltime {#fetchplatformtotaltime-field}

从Adobe Experience Platform获取数据所需的总时间（以millis为单位）。 备注：此时间量从引擎将扩充事件发送到扩充服务并接收响应时开始计算。

类型： long

## Fetchplatformcount {#fetchplatformcount-field}

从Adobe Experience Platform获取数据的次数。

类型： long

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

获取自定义数据的时间（以毫秒为单位）。 备注：此时间量从引擎将扩充事件发送到扩充服务并接收响应时开始计算

类型： long

## Fetchcustomcount {#fetchcustomcount-field}

从外部系统获取自定义数据的次数。

类型： long
