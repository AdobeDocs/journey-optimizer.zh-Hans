---
product: journey optimizer
title: getListItem
description: 瞭解函式gstListItem
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: getListItem，函式，運算式，歷程
exl-id: e995f479-bbaa-45f3-9531-e05680c5a723
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 20%

---

# getListItem {#gestListItem}

傳回指定索引處的清單專案。

## 类别

列表

## 函式語法

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

## 簽章和傳回型別

`getListItem(<listInteger>,<index>)`

傳回整數。

`getListItem(<listDecimal>,<index>)`

傳回小數。

`getListItem(<listString>,<index>)`

傳回字串。

`getListItem(<listDateTimeOnly>,<index>)`

傳回不考慮時區的日期時間。

`getListItem(<listDateTime>,<index>)`

傳回日期時間。

`getListItem(<listDateOnly>,<index>)`

傳回日期清單。

`getListItem(<listBoolean>,<index>)`

傳回布林值。

`getListItem(<listDuration>,<index>)`

傳回持續時間。

## 示例

`getListItem([10, 2, 3], 1)`

傳回「2」

`getListItem(["A", "B", "C"], 2)`
傳回「C」

具有事件欄位「event.appVersion」且值為「20.45.2.3434」的範例

`split(@{event.appVersion}, "\\.")`

返回结果 `["20", "45", "2", "3434"]`

`getListItem(split(@{event.appVersion}, "\\."), 0)`

傳回「20」
