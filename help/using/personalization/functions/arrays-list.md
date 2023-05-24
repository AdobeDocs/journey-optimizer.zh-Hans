---
title: 陣列函式庫
description: 陣列函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 6%

---

# 数组和列表函数 {#arrays}

使用這些函式可讓與陣列、清單和字串的互動更容易。

## 僅計算null {#count-only-null}

此 `countOnlyNull` 函式用於計算清單中null值的數量。

**语法**

```sql
{%= countOnlyNull(array) %}
```

**示例**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

傳回3。

## Null計數 {#count-with-null}

此 `countWithNull` 函式用於計算包含null值之清單中的所有元素。

**语法**

```sql
{%= countWithNull(array) %}
```

**示例**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

傳回6。

## 相異{#distinct}

此 `distinct` 函式用於從移除重複值的陣列或清單中取得值。

**语法**

```sql
{%= distinct(array) %}
```

**示例**

下列作業會指定在多個商店下訂單的人。

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Null的相異計數 {#distinct-count-with-null}

此 `distinctCountWithNull` 函式用於計算清單中包括null值的不同值數目。

**语法**

```sql
{%= distinctCountWithNull(array) %}
```

**示例**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

傳回3。

## 第一個專案{#head}

此 `head` 函式用於傳回陣列或清單中的第一個專案。

**语法**

```sql
{%= head(array) %}
```

**示例**

下列作業會傳回價格最高的前五個訂單中的第一個。 更多關於「 」的資訊 `topN` 函式位於 [第一個 `n` 在陣列中](#first-n) 區段。

```sql
{%= head(topN(orders,price, 5)) %}
```

## 第一個 `n` 在陣列中 {#first-n}

此 `topN` 函式用於傳回第一個 `N` 陣列中的專案（當根據給定的數值運算式依遞增順序排序時）。

**语法**

```sql
{%= topN(array, value, amount) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{ARRAY}` | 要排序的陣列或清單。 |
| `{VALUE}` | 排序陣列或清單的屬性。 |
| `{AMOUNT}` | 要傳回的專案數。 |

**示例**

下列作業會傳回價格最低的前五個訂單。

```sql
{%= topN(orders,price, 5) %}
```

## 在{#in}

此 `in` 函式用來判斷專案是否為陣列或清單的成員。

**语法**

```sql
{%= in(value, array) %}
```

**示例**

下列作業會定義3月、6月或9月有生日的人。

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## 包含{#includes}

此 `includes` 函式用於確定陣列或清單是否包含給定專案。

**语法**

```sql
{%= includes(array,item) %}
```

**示例**

下列作業會定義其最喜愛顏色包含紅色的人員。

```sql
{%= includes(person.favoriteColors,"red") %}
```

## 相交{#intersects}

此 `intersects` 函式用來判斷兩個陣列或清單是否至少有一個通用成員。

**语法**

```sql
{%= intersects(array1, array2) %}
```

**示例**

下列作業會定義其最喜愛顏色至少包含紅色、藍色或綠色其中一種的人員。

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## 上次 `n` 在陣列中{#last-n}

此 `bottomN` 函式用於傳回最後 `N` 陣列中的專案（當根據給定的數值運算式依遞增順序排序時）。

**语法**

```sql
{%= bottomN(array, value, amount) %}
```

| 参数 | 描述 |
| --------- | ----------- | 
| `{ARRAY}` | 要排序的陣列或清單。 |
| `{VALUE}` | 排序陣列或清單的屬性。 |
| `{AMOUNT}` | 要傳回的專案數。 |

**示例**

下列作業會傳回價格最高的最後五筆訂單。

```sql
{%= bottomN(orders,price, 5) %}
```

## 不在……之內{#notin}

此 `notIn` 函式用來判斷專案是否不是陣列或清單的成員。

>[!NOTE]
>
>此 `notIn` 函式 *另外* 確保這兩個值都不等於null。 因此，結果並非完全否定 `in` 函式。

**语法**

```sql
{%= notIn(value, array) %}
```

**示例**

下列作業會定義不在三月、六月或九月過生日的使用者。

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## 子集：{#subset}

此 `subsetOf` 函式來判斷特定陣列（陣列A）是否為另一個陣列（陣列B）的子集。 換句話說，陣列A中的所有元素都是陣列B的元素。

**语法**

```sql
{%= subsetOf(array1, array2) %}
```

**示例**

下列作業會定義造訪過其所有最喜愛城市的人。

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## 超集{#superset}

此 `supersetOf` 函式來判斷特定陣列（陣列A）是否為另一個陣列（陣列B）的超集。 換句話說，陣列A包含陣列B中的所有元素。

**语法**

```sql
{%= supersetOf(array1, array2) %}
```

**示例**

下列作業會定義至少吃過一次壽司和比薩的人。

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
