---
title: 映射函数库
description: 映射函数库
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
TQID: https://experienceleague.adobe.com/KeitEe0NQxxc-snCyWSGlov-OyUgiva6ddzrCTxEKSs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 6%

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
