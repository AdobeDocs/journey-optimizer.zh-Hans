---
product: adobe campaign
title: split
description: 了解函数拆分
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 19%

---

# 拆分 {#split}

将第一个参数字符串与分隔符字符串（第二个参数字符串，可以是正则表达式）拆分，以生成字符串列表（令牌）。

## 类别

字符串

## 函数语法

`split(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 输入字符串 | 字符串 |
| 分隔符 | 字符串 |

## 签名和返回类型

`split(<input string>, <separator string>)`

返回listString。

## 示例

`split(["A_B_C"], "_")`

返回结果 `["A","B","C"]`

事件字段为“event.appVersion”且值为的示例：&quot;20.45.2.3434&quot;

`split(@{event.appVersion}, "\\.")`

返回结果 `["20", "45", "2", "3434"]`
