---
product: journey optimizer
title: notEqualIgnoreCase
description: 了解函数notEqualIgnoreCase
feature: Journeys
role: Engineer
level: Experienced
keywords: notEqualIgnoreCase，函数，表达式，历程
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
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
