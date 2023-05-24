---
product: journey optimizer
title: endWith
description: 瞭解函式endWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWith，函式，運算式，歷程
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

---

# endWith {#endWith}

如果第二個引數是第一個引數的尾碼，則傳回true。

## 类别

字符串

## 函式語法

`endWith(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 字符串 | 字符串 |
| 字尾 | 字符串 |

## 簽章和傳回的型別

`endWith(<string>,<string>)`

傳回布林值。

## 示例

`endWith("Hello World", "World")`

傳回true。

`endWith("Hello World", "Hello")`

傳回false。
