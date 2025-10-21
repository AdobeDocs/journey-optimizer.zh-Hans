---
product: journey optimizer
title: intersect
description: 了解函数intersect
feature: Journeys
role: Engineer
level: Experienced
keywords: 相交，函数，表达式，旅程
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 11%

---

# intersect{#intersect}

返回两个输入列表中的公用值。 如果两个列表之一为null，则返回空列表。

## 类别

列表

## 函数语法

`intersect(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 列表1 | list |
| 列表2 | list |

## 签名和返回的类型

`intersect(listString,listString)`：列表字符串
`intersect(listDecimal,listDecimal)`： listDecimal
`intersect(listInteger,listInteger)`： listInteger
`intersect(listDateTime,listDateTime)`： listDateTime
`intersect(listDateTimeOnly,listDateTimeOnly)`： listDateTimeOnly
`intersect(listDateOnly,listDateOnly)`： listDateOnly
`intersect(listDuration,listDuration)`： listDuration
`intersect(listBoolean,listBoolean)`：列表布尔值

返回列表。

## 示例

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

返回[&quot;sports&quot;，&quot;news&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "documentary"]
)
```

返回配置文件属性和给定类别列表之间的通用项目。

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

返回用户档案属性和给定事件字段之间的公用项。
