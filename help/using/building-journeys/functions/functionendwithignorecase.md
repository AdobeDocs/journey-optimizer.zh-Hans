---
product: adobe campaign
title: endWithIgnoreCase
description: 了解函数endWithIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 278ef1a4-571c-4b5f-b4de-0cfc644ac7d7
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# endWithIgnoreCase {#endWithIgnoreCase}

检查第一个参数字符串是否以特定字符串（第二个参数字符串）结尾，而不考虑大小写。

## 类别

字符串

## 函数语法

`endWithIgnoreCase(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 字符串 | 字符串 |
| 后缀 | 字符串 |

## 签名和返回的类型

`endWithIgnoreCase(<string>,<string>)`

返回布尔值。

## 示例

`endWithIgnoreCase("rowing is great", "AT")`

返回true。
