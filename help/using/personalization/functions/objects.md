---
title: 物件函式庫
description: 物件函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# 物件函式 {#objects}

## 為null{#isNull}

此 `isNull` 函式決定物件參考是否不存在。

**语法**

```sql
{%= isNull(object) %}
```

**示例**

下列作業會檢查個人的住家地址是否不存在。

```sql
{%= isNull(person.homeAddress) %}
```

## 不是Null{#isNotNull}

此 `isNotNull` 函式決定物件參考是否存在。

**语法**

```sql
{%= isNotNull(object) %}
```

**示例**

下列作業會檢查人員的住家地址是否存在。

```sql
{%= isNotNull(person.homeAddress) %}
```
