---
title: 辅助程序
description: 辅助程序
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 22752a30fef53808fa9deb80a2053d5bc22abc95
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 4%

---

# 辅助程序 {#gs-helpers}

## 預設遞補值{#default-value}

此 `Default Fallback Value` 如果屬性為空白或null，會使用helper傳回預裝置援值。 此機制適用於設定檔屬性和歷程事件。

**语法**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

在此範例中，值 `there` 顯示條件為 `firstName` 此設定檔的屬性為空白或null。

## 条件{#if-function}

此 `if` helper用於定義條件區塊。
如果運算式評估傳回true，則會轉譯區塊，否則會略過該區塊。

**语法**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

遵循 `if` helper，您可以輸入 `else` 陳述式，指定要在相同條件為false時執行的程式碼區塊。
此 `elseif` 陳述式會指定新條件，以測試第一個陳述式是否傳回false。


**格式**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

**示例**

1. **根據條件運算式演算不同的存放區連結**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **決定電子郵件地址副檔名**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **新增條件式連結**

   下列作業會將連結新增至僅含有「.edu」電子郵件地址之設定檔的「www.adobe.com/academia&#39;網站」、含有「.org」電子郵件地址之設定檔的「www.adobe.com/org&#39;網站」，以及所有其他設定檔的預設URL「www.adobe.com/users&#39;」：

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **以區段成員資格為基礎的條件式內容**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>若要進一步瞭解細分和細分服務，請參閱此 [區段](../../segment/about-segments.md).


## Unless{#unless}

此 `unless` helper用於定義條件區塊。 反對The `if`  協助程式，如果運算式評估傳回false，則會轉譯區塊。

**语法**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**示例**

根據電子郵件地址副檔名轉譯某些內容：

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## 每個{#each}

此 `each` helper是用來反複運算陣列。
協助程式的語法為 ```{{#each ArrayName}}``` 您的內容 {{/each}}
我們可以使用關鍵字來參照個別陣列專案 **此** 區塊內部。 可以使用呈現陣列元素的索引 {{@index}}.

**语法**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

**示例**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**示例**

呈現此使用者購物車中產品的清單：

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## 替換為{#with}

此 `with` helper用於變更範本部分的評估權杖。

**语法**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

此 `with` 協助程式也可用來定義捷徑變數。

**示例**

搭配使用可將長變數名稱等同為短變數名稱：

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

此 `let` 函式可將運算式儲存為變數，以便稍後在查詢中使用。

**语法**

```sql
{% let variable = expression %} {{variable}}
```

**示例**

下列範例會允許交易總和大於$100且小於$1000時以USD表示的所有產品總和。

```sql
{% let variable = expression %} {{variable}}
```
