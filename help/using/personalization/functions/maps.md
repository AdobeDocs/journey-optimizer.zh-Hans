---
title: 函数库
description: 函数库
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 5%

---

# 映射函数{#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL)优惠函数，使与地图的交互更简单。

## 获取

`get`函数用于检索给定键的映射值。

**格式**

```sql
get({MAP},{STRING})
```

**示例**

以下PQL查询获取键`example@example.com`的标识映射值。

```sql
get(identityMap,"example@example.com")
```

## 按键

`keys`函数用于检索给定映射的所有键。

**格式**

```sql
keys({MAP})
```

**示例**

以下PQL查询将获取映射`identityMap`的所有键。

```sql
keys(identityMap)
```

## 值

`values`函数用于检索给定映射的所有值。

**格式**

```sql
values({MAP})
```

**示例**

以下PQL查询将获取映射`identityMap`的所有值。

```sql
values(identityMap)
```
