---
product: journey optimizer
title: startWithIgnoreCase
description: 了解函数startWithIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 25%

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

返回true。
