---
product: adobe campaign
title: notEqualIgnoreCase
description: 了解函数notEqualIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 13%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

检查具有第二个参数字符串的第一个参数字符串是否不同，忽略大小写注意事项。

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

`notEqualIgnoreCase(@{iOSPushPermissionAllowed.device.model}, "iPad")`
