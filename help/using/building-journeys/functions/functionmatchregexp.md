---
product: journey optimizer
title: matchRegExp
description: 了解函数matchRegExp
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: matchRegExp，函数，表达式，历程
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: 9e6b3fc5c91e360a9bd7e727949ac5445cd79654
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 19%

---

# matchRegExp {#matchRegExp}

如果第一个参数中的字符串与第二个参数中的正则表达式匹配，则返回true。 有关详细信息，请参阅[此页面](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html)。

## 类别

字符串

## 函数语法

`matchRegExp(<parameters>)`

## 参数

| 参数 | 类型 |
|--- |--- |
| 字符串 | 字符串 |
| regexp | 字符串 |

## 签名和返回的类型

`matchRegExp(<string>,<string>)`

返回布尔值。

## 示例

`matchRegExp("12345", "\\d+")`

返回真。
