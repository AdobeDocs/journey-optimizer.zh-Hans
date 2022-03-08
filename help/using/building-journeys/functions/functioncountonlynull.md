---
product: adobe campaign
title: countOnlyNull
description: 了解函数countOnlyNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 33%

---

# countOnlyNull {#countOnlyNull}

计算列表中空值的数量。

## 类别

聚合

## 函数语法

`countOnlyNull(<listAny>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 列表 | listString |
| 列表 | listBoolean |
| 列表 | listInteger |
| 列表 | listDecimal |
| 列表 | listDuration |
| 列表 | listDateTime |
| 列表 | listDateTimeOnly |
| 列表 | listDateOnly |

## 签名和返回的类型

`countOnlyNull(<listAny>)`

返回整数。

## 示例

`countOnlyNull([10,2,10,null])`

返回1。
