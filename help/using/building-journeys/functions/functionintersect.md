---
product: journey optimizer
title: intersect
description: 了解函数相交
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 12%

---

# intersect{#intersect}

返回两个输入列表中的公共值。 如果两个列表之一为空，则返回空列表。

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

`intersect(listString,listString)`:listString
`intersect(listDecimal,listDecimal)`:listDecimal
`intersect(listInteger,listInteger)`:listInteger
`intersect(listDateTime,listDateTime)`:listDateTime
`intersect(listDateTimeOnly,listDateTimeOnly)`:listDateTimeOnly
`intersect(listDateOnly,listDateOnly)`:listDateOnly
`intersect(listDuration,listDuration)`:listDuration
`intersect(listBoolean,listBoolean)`:listBoolean

返回列表。

## 示例

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

返回结果 [&quot;sports&quot;、&quot;news&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "news", "documentary"]
)
```

返回配置文件属性和给定类别列表之间的通用项目。

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @{myEvent.sport_interests}
)
```

返回用户档案属性和给定事件字段之间的常用项目。
