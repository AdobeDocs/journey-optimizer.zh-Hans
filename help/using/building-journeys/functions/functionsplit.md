---
product: journey optimizer
title: 拆分
description: 了解函数拆分
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

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
