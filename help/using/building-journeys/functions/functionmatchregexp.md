---
product: journey optimizer
title: matchRegExp
description: 了解函数matchRegExp
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 18%

---

# matchRegExp {#matchRegExp}

如果第一个参数中的字符串与第二个参数中的正则表达式匹配，则返回true。 有关更多信息，请参阅 [本页](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

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

`matchRegExp("username@adobe.com", "*adobe")`

返回true。
