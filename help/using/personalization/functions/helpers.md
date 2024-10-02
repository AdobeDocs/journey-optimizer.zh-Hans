---
title: 辅助程序
description: 辅助程序
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 110c4895ac7f0b683a695e9705a8f8ac54d09637
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 5%

---

# 辅助程序 {#gs-helpers}

## 默认回退值{#default-value}

如果属性为空或null，则使用`Default Fallback Value`帮助程序返回默认回退值。 此机制适用于配置文件属性和历程事件。

**语法**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

在此示例中，如果此配置文件的`firstName`属性为空或null，则显示值`there`。

## 条件{#if-function}

`if`帮助程序用于定义条件块。
如果表达式求值返回true，则会呈现块，否则将跳过该块。

**语法**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

在`if`帮助程序之后，您可以输入`else`语句以指定要执行的代码块（如果相同条件为false）。
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

1. **确定电子邮件地址扩展名**

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

   以下操作将添加一个链接，指向仅包含“.edu”电子邮件地址的用户档案的“www.adobe.com/academia&#39;网站”、包含“.org”电子邮件地址的用户档案的“www.adobe.com/org&#39;网站”，以及所有其他用户档案的默认URL“www.adobe.com/users&#39;”：

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **基于受众成员资格的条件内容**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>要了解有关受众和分段服务的更多信息，请参阅此[部分](../../audience/about-audiences.md)。


## Unless{#unless}

`unless`帮助程序用于定义条件块。 通过与`if`帮助程序相对，如果表达式求值返回false，则呈现块。

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

## Each{#each}

`each`辅助函数用于遍历数组。
辅助函数的语法为```{{#each ArrayName}}``` YourContent {{/each}}
我们可以在块中使用关键字**this**&#x200B;引用单个数组项。 可以使用{{@index}}呈现数组元素的索引。

**语法**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**示例**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**示例**

呈现此用户在其购物车中拥有的产品列表：

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

## With{#with}

`with`帮助程序用于更改模板部分的评估令牌。

**语法**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

`with`辅助函数也可用于定义快捷键变量。

**示例**

与一起使用，将长变量名称别名更改为短变量名称：

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

`let`函数允许将表达式存储为变量，以便稍后在查询中使用。

**语法**

```sql
{% let variable = expression %} {{variable}}
```

**示例**

以下示例允许您计算购物车中价格在100和1000之间的产品的总价。

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```
