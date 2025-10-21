---
product: journey optimizer
title: getListItem
description: 了解函数gstListItem
feature: Journeys
role: Engineer
level: Experienced
keywords: getListItem，函数，表达式，历程
exl-id: e995f479-bbaa-45f3-9531-e05680c5a723
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 18%

---

# getListItem {#gestListItem}

返回给定索引处的列表项。

## 类别

列表

## 函数语法

`getListItem(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| index | 整数 |

## 签名和返回的类型

`getListItem(<listInteger>,<index>)`

返回整数。

`getListItem(<listDecimal>,<index>)`

返回小数。

`getListItem(<listString>,<index>)`

返回字符串。

`getListItem(<listDateTimeOnly>,<index>)`

返回不考虑时区的日期时间。

`getListItem(<listDateTime>,<index>)`

返回日期时间。

`getListItem(<listDateOnly>,<index>)`

返回日期列表。

`getListItem(<listBoolean>,<index>)`

返回布尔值。

`getListItem(<listDuration>,<index>)`

返回持续时间。

## 示例

`getListItem([10, 2, 3], 1)`

返回“2”

`getListItem(["A", "B", "C"], 2)`
返回“C”

具有事件字段&quot;event.appVersion&quot;且值为&quot;20.45.2.3434&quot;的示例

`split(@event{event.appVersion}, "\\.")`

返回`["20", "45", "2", "3434"]`

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

返回“20”
