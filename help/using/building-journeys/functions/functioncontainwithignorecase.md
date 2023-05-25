---
product: journey optimizer
title: containIgnoreCase
description: 了解函数containIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: containIgnoreCase，函数，表达式，历程
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 21%

---

# containIgnoreCase {#containIgnoreCase}

检查第二个参数字符串是否包含在第一个参数字符串中，而不考虑大小写。

## 类别

字符串

## 函数语法

`containIgnoreCase(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 字符串 | 字符串 |
| 搜索字符串 | 字符串 |

## 签名和返回的类型

`containIgnoreCase(<string>,<string>)`

返回布尔值。

## 示例

`containIgnoreCase("rowing is great", "GREAT")`

返回真。
