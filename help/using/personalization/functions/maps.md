---
title: 映射函数库
description: 映射函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 8%

---

# 映射函数{#maps}

在个性化中使用地图功能，更轻松地与地图交互。

## Get{#get}

`get`函数用于检索给定键的映射值。

**语法**

```sql
{%= get(map, string) %}
```

**示例**

以下操作获取键`example@example.com`的标识映射值。

```sql
{%= get(identityMap,"example@example.com") %}
```

## 键{#keys}

`keys`函数用于检索给定映射的所有键。

**语法**

```sql
{%= keys(map) %}
```

**示例**

以下操作获取映射`identityMap`的所有键。

```sql
{%= keys(identityMap) %}
```

## 值{#values}

`values`函数用于检索给定映射的所有值。

**语法**

```sql
{%= values(map) %}
```

**示例**

以下操作获取映射`identityMap`的所有值。

```sql
{%= values(identityMap) %}
```
