---
title: 辅助程序
description: 辅助程序
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 221368c7766e942143639fcd554b32f9de5ab0c9
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 5%

---

# 辅助程序 {#gs-helpers}

## 默认回退值{#default-value}

如果属性为空或null，则使用`Default Fallback Value`帮助程序返回默认回退值。 此机制适用于配置文件属性和历程事件。

**语法**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

在此示例中，如果此配置文件的`there`属性为空或null，则显示值`firstName`。

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
   {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>要了解有关受众和分段服务的更多信息，请参阅[此章节](../../audience/about-audiences.md)。


## Unless{#unless}

`unless`帮助程序用于定义条件块。 通过对`if`帮助程序的反对，如果表达式求值返回false，则呈现块。

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
Some edu specific content
{%/unless%}
```

## 每个{#each}

`each`辅助函数用于遍历数组。
辅助函数的语法为```{{#each ArrayName}}``` YourContent `{{/each}}`
我们可以在块中使用关键字&#x200B;**this**&#x200B;引用单个数组项。 可以使用`{{@index}}`呈现数组元素的索引。

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

>[!NOTE]
>
>您还可以使用`each`帮助程序对从自定义操作响应返回的数组进行迭代。 有关从自定义操作响应迭代嵌套数组的示例，请参阅[在本机渠道中使用自定义操作响应](../../action/action-response.md#response-in-channels)。

## 替换为{#with}

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

## 执行元数据 {#execution-metadata}

>[!AVAILABILITY]
>
>此功能为限量发布版。请联系 Adobe 代表以获取访问权限。

`executionMetadata`帮助程序允许动态捕获自定义键值对并将其存储到消息执行上下文中。

**语法**

```
{{executionMetadata key="your_key" value="your_value"}}
```

在此语法中，`key`引用元数据名称，`value`是要保留的元数据。

**用例**

利用此功能，您可以将上下文信息附加到营销活动或历程中的任何本机操作。 这使您能够将实时投放上下文数据导出到外部系统，用于各种目的，例如跟踪、分析、个性化和下游处理。

>[!NOTE]
>
>[自定义操作](../../action/action.md)不支持执行元数据函数。

例如，您可以使用执行元数据帮助程序将特定ID附加到发送到每个用户档案的每个投放中。 此信息在运行时生成，随后可导出扩充的执行元数据以用于与外部报告平台的下游协调。

**工作原理**

从营销活动或历程中的渠道内容中选择任何元素，并使用个性化编辑器将`executionMetadata`帮助程序添加到此元素。

>[!NOTE]
>
>显示内容本身时，执行元数据函数不可见。


在运行时，元数据值被添加到现有&#x200B;**[!UICONTROL 消息反馈事件数据集]**&#x200B;中，并添加了以下架构：

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!NOTE]
>
>在[本节](../../data/get-started-datasets.md)中了解关于数据集的更多信息。

**限制**

每个操作的键值对的上限为2kb。

如果超过2Kb限制，则仍会投放消息，但可以截断任何键值对。

**示例**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

在此示例中，假设`profile.person.name.firstName` = &quot;Alex&quot;，则生成的实体为：

```
{
  "key": "firstName",
  "value": "Alex"
}
```

