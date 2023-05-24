---
product: journey optimizer
title: containIgnoreCase
description: 瞭解函式containIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: containIgnoreCase，函式，運算式，歷程
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 21%

---

# containIgnoreCase {#containIgnoreCase}

檢查第二個引數字串是否包含在第一個引數字串中，而不考慮大小寫。

## 类别

字符串

## 函式語法

`containIgnoreCase(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 字符串 | 字符串 |
| 字串已搜尋 | 字符串 |

## 簽章和傳回的型別

`containIgnoreCase(<string>,<string>)`

傳回布林值。

## 示例

`containIgnoreCase("rowing is great", "GREAT")`

傳回true。
