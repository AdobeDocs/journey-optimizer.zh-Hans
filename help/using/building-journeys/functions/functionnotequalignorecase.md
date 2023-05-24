---
product: journey optimizer
title: notEqualIgnoreCase
description: 瞭解函式notEqualIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: notEqualIgnoreCase，函式，運算式，歷程
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '41'
ht-degree: 12%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

檢查第一個引數字串與第二個引數字串是否不同，忽略大小寫考量。

## 类别

字符串

## 函式語法

`notEqualIgnoreCase(<parameters>)`

## 参数

* 字符串

## 簽章和傳回的型別

`notEqualIgnoreCase(<string>,<string>)`

傳回布林值。

## 示例

`notEqualIgnoreCase(@{iOSPushPermissionAllowed.device.model}, "iPad")`
