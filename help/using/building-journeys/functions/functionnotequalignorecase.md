---
product: journey optimizer
title: notEqualIgnoreCase
description: 了解函数notEqualIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: notEqualIgnoreCase，函数，表达式，历程
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '41'
ht-degree: 12%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

检查第一个参数字符串与第二个参数字符串是否不同，忽略大小写注意事项。

## 类别

字符串

## 函数语法

`notEqualIgnoreCase(<parameters>)`

## 参数

* 字符串

## 签名和返回的类型

`notEqualIgnoreCase(<string>,<string>)`

返回布尔值。

## 示例

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`
