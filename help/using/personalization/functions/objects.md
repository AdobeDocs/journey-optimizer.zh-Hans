---
title: 对象函数库
description: 对象函数库
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
TQID: https://experienceleague.adobe.com/EdvzBXdtv1Mm4yIZ8ehu4tx6uQBxnpcXTMVQIc1oQkI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 57
ht-degree: 7%

---

# 对象函数 {#objects}

## Is null{#isNull}

`isNull`函数确定对象引用是否不存在。

**语法**

```sql
{%= isNull(object) %}
```

**示例**

以下操作检查人员的家庭地址是否不存在。

```sql
{%= isNull(person.homeAddress) %}
```

## 不为null{#isNotNull}

`isNotNull`函数确定是否存在对象引用。

**语法**

```sql
{%= isNotNull(object) %}
```

**示例**

以下操作检查人员的家庭地址是否存在。

```sql
{%= isNotNull(person.homeAddress) %}
```
