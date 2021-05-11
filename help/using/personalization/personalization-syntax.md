---
title: 个性化语法
description: 了解如何使用个性化语法
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 3%

---

# 个性化语法{#personalization-syntax}

![](../assets/do-not-localize/badge.png)

## 简介

Journey Optimizer中的个性化基于名为Handlebars的模板语法。
有关Handlebars语法的完整说明，请参阅[HandlebarsJS](https://handlebarsjs.com/)。

它使用模板和输入对象生成HTML或其他文本格式。 Handlebars模板与带有嵌入Handlebars表达式的常规文本类似。

简单表达式范例：

```
{{profile.person.name}}
```

其中：

* **概** 述是命名空间。
* **person.** name是由属性组成的标记。属性结构在Adobe Experience Platform XDM模式中定义。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans)。

## 语法一般规则

标识符可以是除以下字符之外的任何Unicode字符：

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

语法区分大小写。

仅在路径表达式的第一部分中才允许使用字词&#x200B;**true**、**false**、**null**&#x200B;和&#x200B;**undefined**。

在Handlebars中，{{表达式}}返回的值为&#x200B;**HTML-escaped**。 如果表达式包含&amp;，则返回的HTML转义输出将生成为&amp;。 如果你不想让Handlebars逃离某个值，就使用“三重藏”。

## 配置文件

此命名空间允许您引用在[Adobe Experience Platform用户档案模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html)中描述的模式中定义的所有属性。

在Journey Optimizer个性化块中引用属性之前，需要在模式中定义这些属性。

所有引用都针对用户档案模式进行验证，验证机制在[此处](personalization-validation.md)中有说明。

**示例引用：**

* ```{{profile.person.name.fullName}}```
* ```{{profile.person.name.firstName}}```
* ```{{profile.person.gender}}```
* ```{{profile.personalEmail.address}}```
* ```{{profile.mobilePhone.number}}```
* ```{{profile.homeAddress.city}}```
* ```{{profile.faxPhone.number}}```

**确定电子邮件地址扩展**:

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
{%else if contains(profile.personalEmail.address, ".org")%}
<a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
{%else%}
<a href="https://www.adobe.com/users">Checkout our page</a>
{%/if%}
```

## 区段

要了解有关分段和分段服务的更多信息，请参阅此[部分](../segment/about-segments.md)。

**根据区段成员关系呈现不同的内容**:

```
{%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
  Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
{%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
  Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
{%/if%}
```

**确定用户档案是否已是成员**:

```
{%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
    You're a member!
{%else%}
    You should be a member! Sign up now!
{%/if%}
```

## 选件

此命名空间允许您引用现有优惠决策。
要引用优惠，您需要使用定义优惠的不同信息声明路径。

此路径具有以下结构：
0 - &#39;优惠:标识属于优惠表达式的路径命名空间
1 — 类型：确定优惠呈现类型。 有效值为“image”、“html”和“text”
2 — 版面ID
3 -活动ID
4 -优惠特定属性。 可以使用取决于优惠类型支持的属性。 例如，图像`deliveryUrl`。

有关Decisions API的详细信息，请参阅此[页](https://experienceleague.corp.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#deliver-offers-using-the-decisions-api)

有关“优惠表示法”的详细信息，请参阅此[页](https://experienceleague.corp.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#accept-and-content-type-headers)。

所有引用都针对优惠模式进行验证，验证机制在[此处](personalization-validation.md)中有说明。

**示例引用：**

* 图像的托管位置：

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl```

* 目标URL:

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl```

* 来自决策引擎的优惠的文本内容：

```offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```

* 来自决策引擎的优惠的HTML内容：

```offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```


## Helpers

Handlebars帮助程序是一个简单的标识符，后面可能有参数。
每个参数都是Handlebars表达式。 这些帮助者可以从模板中的任何上下文访问。

这些块帮助程序由位于帮助程序名称前面的#标识，并需要同名的匹配结束/。
块是具有块打开({{# }})和关闭({{/})的表达式。

### 如果

使用&#x200B;**if**帮助程序定义条件块。
如果表达式评估返回true，则块将呈现，否则将跳过块。

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

在&#x200B;**if**&#x200B;帮助程序之后，如果相同的条件为false，则可以输入&#x200B;**else**语句以指定要执行的代码块。
**else if**&#x200B;语句将指定新条件以测试第一个语句是否返回false。

**根据条件表达式渲染不同的存储链接**:

```
{%#if profile.homeAddress.countryCode = "FR"%}
  <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
{%else%}
  <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
{%/if%}
```

### 除非

**#** unlesshelper用于定义条件块。对于&#x200B;**#if**&#x200B;帮助程序，如果表达式评估返回false，则呈现块。

**根据电子邮件地址扩展渲染某些内容**:

```
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

### 每个

**每个**帮助器用于在数组上迭代。
帮助程序的语法为```{{#each ArrayName}}``` YourContent {{/each}}
通过使用块内的关键字**this**，我们可以引用单个数组项。 可以使用{{@index}}呈现数组元素的索引。

示例：

```
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

```
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**呈现此用户在购物车中拥有的产品列表**:

```
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

### 使用

**#with**&#x200B;帮助程序用于更改template-part的评估令牌。

示例：

```
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

**#with**&#x200B;帮助程序对于定义快捷键变量也很有用。

**用于将长变量名称与短变量名称进行混淆**:

```
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```


## 限制

* 在个性化表达式中，不能使用&#x200B;**xEvent**&#x200B;变量。 对xEvent的任何引用都将导致验证失败。
