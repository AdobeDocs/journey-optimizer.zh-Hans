---
product: journey optimizer
title: endWith
description: 了解函数endWith
feature: Journeys
role: Developer
level: Experienced
keywords: endWith，函数，表达式，历程
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

---

# endWith {#endWith}

如果第二个参数是第一个参数的后缀，则返回true。

## 类别

字符串

## 函数语法

`endWith(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 字符串 | 字符串 |
| 后缀 | 字符串 |

## 签名和返回的类型

`endWith(<string>,<string>)`

返回布尔值。

## 示例

`endWith("Hello World", "World")`

返回真。

`endWith("Hello World", "Hello")`

返回假。
