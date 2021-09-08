---
title: 辅助程序
description: 辅助程序
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 5df4856c7be31a75116d906320ae50cd5dc6a2dc
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 4%

---

# 辅助程序 {#gs-helpers}

## 默认回退值{#default-value}

如果属性为空或null，则`Default Fallback Value`帮助程序用于返回默认的回退值。 此机制适用于用户档案属性和历程事件。

**语法**

```sql
Hello {%=profile.personalEmail.name.firstName ?: 'there' %}!
```

在此示例中，如果此配置文件的`firstName`属性为空或null，则显示值`there`。

## 条件{#if-function}

`if`帮助程序用于定义条件块。
如果表达式计算返回true，则会呈现块，否则会跳过该块。

**语法**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

在`if`帮助程序之后，如果相同的条件为false，则可以输入`else`语句以指定要执行的代码块。
`elseif`语句将指定一个新条件来测试第一个语句是否返回false。


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

1. **根据条件表达式呈现不同的存储链接**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **确定电子邮件地址扩展**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **添加条件链接**

   以下操作将添加一个链接，指向“www.adobe.com/academia&#39;”网站（仅适用于具有“.edu”电子邮件地址的用户档案）、“www.adobe.com/org&#39;网站（适用于具有“.org”电子邮件地址的用户档案），以及所有其他用户档案的默认URL“www.adobe.com/users&#39;”：

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **基于区段成员资格的条件内容**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

1. **确定用户档案是否已是成员**

   ```sql
   {%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
       You're a member!
   {%else%}
       You should be a member! Sign up now!
   {%/if%}
   ```

>[!NOTE]
>
>要了解有关分段和分段服务的更多信息，请参阅此[部分](../../segment/about-segments.md)。


## 除非{#unless}

`unless`帮助程序用于定义条件块。 与`if`帮助程序相反，如果表达式求值返回false，则会呈现块。

**语法**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**示例**

根据电子邮件地址扩展呈现某些内容：

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## 每个{#each}

`each`帮助程序用于在数组上迭代。
帮助程序的语法为```{{#each ArrayName}}``` YourContent {{/each}}
我们可以在块内使用关键字**this**&#x200B;来引用各个数组项目。 可使用{{@index}}呈现数组元素的索引。

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

呈现此用户购物车中的产品列表：

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## 使用{#with}

`with`帮助程序用于更改模板部分的评估令牌。

**语法**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

`with`帮助程序在定义快捷方式变量时也很有用。

**示例**

与一起使用，以将长变量名称取为短变量名称：

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## 让{#let}

`let`函数允许将表达式存储为变量，以便稍后在查询中使用。

**语法**

```sql
{% let variable = expression %} {{variable}}
```

**示例**

以下示例允许以美元表示的交易产品合计的所有合计金额，其合计金额大于100美元且小于1000美元。

```sql
{% let variable = expression %} {{variable}}
```
