---
title: 地圖函式庫
description: 地圖函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 5%

---

# 地圖函式{#maps}

在個人化中使用地圖功能，以便更輕鬆地與地圖互動。

## 取得{#get}

此 `get` 函式用於擷取給定索引鍵的對映值。

**语法**

```sql
{%= get(map, string) %}
```

**示例**

下列作業取得索引鍵的身分對應值 `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## 金鑰{#keys}

此 `keys` 函式來擷取給定對應的所有索引鍵。

**语法**

```sql
{%= keys(map) %}
```

**示例**

下列作業取得對應的所有索引鍵 `identityMap`.

```sql
{%= keys(identityMap) %}
```

## 值{#values}

此 `values` 函式來擷取給定對應的所有值。

**语法**

```sql
{%= values(map) %}
```

**示例**

下列作業取得對應的所有值 `identityMap`.

```sql
{%= values(identityMap) %}
```
