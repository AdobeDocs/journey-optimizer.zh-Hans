---
product: journey optimizer
title: startWithIgnoreCase
description: 了解函数startWithIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWithIgnoreCase，函数，表达式，历程
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 22%

---

# startWithIgnoreCase {#startWithIgnoreCase}

如果第二个参数是第一个参数的前缀，而不考虑大小写，则返回true。

## 类别

字符串

## 函数语法

`startWithIgnoreCase(<parameters>)`

## 参数

| 参数 | 类型 |
|-------------|--------|
| 字符串 | 字符串 |
| 前缀 | 字符串 |

## 签名和返回的类型

`startWithIgnoreCase(<string>,<string>)`

返回布尔值。

## 示例

`startWithIgnoreCase("rowing is great", "RO")`

返回真。
