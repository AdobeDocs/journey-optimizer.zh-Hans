---
title: 算術函式庫
description: 算術函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 7%

---

# 算术函数 {#maths}

算術函式用於對值執行基本計算。

## Add{#add}

此 `+` （加法）函式用於找出兩個引數運算式的總和。

**语法**

```sql
{%= double + double %}
```

**示例**

下列作業會加總兩種不同產品的價格。

```sql
{%= product1.price + product2.price %}
```

## 乘{#multiply}

此 `*` （乘法）函式用於尋找兩個引數運算式的乘積。

**语法**

```sql
{%= double * double %}
```

**示例**

下列作業會尋找存貨的產品與產品價格，以尋找產品的總值。

```sql
{%= product.inventory * product.price %}
```

## 減法{#substract}

此 `-` （減法）函式可用來找出兩個引數運算式的差異。

**语法**

```sql
{%= double - double %}
```

**示例**

下列作業會找出兩個不同產品之間的價格差異。

```sql
{%= product1.price - product2.price %}
```

## 除{#divide}

此 `/` (division)函式用於尋找兩個引數運算式的商。

**语法**

```sql
{%= double / double %}
```

**示例**

下列作業會找出已售出產品總數與已賺取金額總數之間的商數，以檢視每個專案的平均成本。

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## 餘數{#remainder}

此 `%` （模數/餘數）函式用來找出兩個引數運算式相除後的餘數。

**语法**

```sql
{%= double % double %}
```

**示例**

下列作業會檢查個人的年齡是否可被5整除。

```sql
{%= person.age % 5 = 0 %}
```
