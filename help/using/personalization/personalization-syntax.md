---
solution: Journey Optimizer
product: journey optimizer
title: 个性化语法
description: 了解如何使用个性化语法。
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: 表达式、编辑器、语法、个性化
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 3%

---

# 个性化语法 {#personalization-syntax}

[!DNL Journey Optimizer]中的Personalization基于名为Handlebars的模板语法。 有关Handlebars语法的完整说明，请参阅[HandlebarsJS文档](https://handlebarsjs.com/)。

它使用模板和输入对象来生成HTML或其他文本格式。 Handlebars模板看起来像包含嵌入Handlebars表达式的常规文本。

简单表达式示例：

`{{profile.person.name}}`

其中：

* `profile`是一个命名空间。
* `person.name`是由属性组成的令牌。 属性结构在Adobe Experience Platform XDM架构中定义。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}。

## 语法一般规则 {#general-rules}

* 标识符可以是除以下字符之外的任何unicode字符：

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* 语法区分大小写。

* 仅在路径表达式的第一部分中允许使用单词&#x200B;**true**、**false**、**null**&#x200B;和&#x200B;**undefined**。

* 在Handlebars中，{{expression}}返回的值是&#x200B;**HTML转义**。 如果表达式包含`&`，则返回的HTML转义输出将生成为`&amp;`。 如果不希望Handlebars转义值，请使用“三重存储”。

* 关于文字函数参数，模板化语言解析器不支持单个未转义的反斜杠(`\`)符号。 此字符必须使用其他反斜杠(`\`)符号进行转义。 示例：

  `{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## 可用命名空间 {#namespaces}

* **轮廓**

  此命名空间允许您引用[Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}中描述的配置文件架构中定义的所有属性。

  属性需要先在架构中定义，然后才能在[!DNL Journey Optimizer]个性化块中引用。

  有关如何利用条件中的配置文件属性的更多信息，请参阅[此部分](functions/helpers.md#if-function)。

  +++示例引用

   * `{{profile.person.name.fullName}}`
   * `{{profile.person.name.firstName}}`
   * `{{profile.person.gender}}`
   * `{{profile.personalEmail.address}}`
   * `{{profile.mobilePhone.number}}`
   * `{{profile.homeAddress.city}}`
   * `{{profile.faxPhone.number}}`

  +++

* **受众**

  要了解有关分段服务的更多信息，请参阅[本文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hans){target="_blank"}。

* **产品建议**

  此命名空间允许您引用现有优惠决策。

  要引用选件，您需要使用定义选件的不同信息声明路径。 此路径具有以下结构：

  `offers.Type.[Placement Id].[Activity Id].Attribute`

  其中：

   * `offers`标识属于优惠命名空间的路径表达式
   * `Type`确定优惠呈现的类型。 可能的值为： `image`、`html`和`text`
   * `Placement Id`和`Activity Id`是投放位置和活动标识符
   * `Attributes`是特定于优惠的属性，具体取决于优惠类型。 示例： `deliveryUrl`图像

  有关Decisions API和Offer呈现的详细信息，请参阅[此页面](../offers/api-reference/offer-delivery-api/decisioning-api.md)

  所有引用均通过[此页面](../personalization/personalization-build-expressions.md)中描述的验证机制针对优惠架构进行验证

  +++示例引用

   * 图像托管位置：

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

   * 单击图像时的目标URL：

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

   * 来自决策引擎的优惠的文本内容：

     `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

   * 来自决策引擎的优惠的HTML内容：

     `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

  +++

## 辅助程序{#helpers-all}

Handlebars帮助程序是一个简单标识符，后面可以跟参数。 每个参数都是一个Handlebars表达式。 可以从模板中的任何上下文访问这些帮助程序。

这些块帮助程序由帮助程序名称前的`#`标识，并需要相同名称的匹配闭合`/`。

块是具有块开始(`{{# }}`)和结束(`{{/}}`)的表达式。

有关辅助函数的更多信息，请参阅[此章节](functions/helpers.md)。

## 文本类型 {#literal-types}

[!DNL Adobe Journey Optimizer]支持以下文本类型：

| 文本 | 定义 |
| ------- | ---------- |
| 字符串 | 由双引号括起来的字符组成的数据类型。 <br>示例： `"prospect"`，`"jobs"`，`"articles"` |
| 布尔值 | true或false的数据类型。 |
| 整数 | 表示整数的数据类型。 它可以是正数、负数或零。 <br>示例： `-201`，`0`，`412` |
| 数组 | 由一组其他文字值组成的数据类型。 它使用方括号将不同的值分组，并使用逗号分隔不同的值。<br> **注意：**&#x200B;您不能直接访问数组中项的属性。 <br>示例： `[1, 4, 7]`，`["US", "FR"]` |

>[!CAUTION]
>
>**xEvent**&#x200B;变量的使用在个性化表达式中不可用。 对xEvent的任何引用都会导致验证失败。
