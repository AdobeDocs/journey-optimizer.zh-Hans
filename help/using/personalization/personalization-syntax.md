---
title: 个性化语法
description: 了解如何使用个性化语法。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: 904fd645cba550fdb65821292293bf7d838c66f6
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 10%

---

# 个性化语法 {#personalization-syntax}

中的个性化 [!DNL Journey Optimizer] 基于名为Handlebars的模板语法。
有关Handlebars语法的完整说明，请参阅 [HandlebarsJS文档](https://handlebarsjs.com/).

它使用模板和输入对象来生成HTML或其他文本格式。 Handlebars模板看起来像带有嵌入Handlebars表达式的正则文本。

简单表达式示例：

`{{profile.person.name}}`

其中：

* `profile` 是命名空间。
* `person.name` 是由属性组成的令牌。 属性结构在Adobe Experience Platform XDM架构中定义。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target=&quot;_blank&quot;}.

## 语法常规规则 {#general-rules}

标识符可以是任何Unicode字符，但以下字符除外：

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

语法区分大小写。

词 **true**, **false**, **null** 和 **未定义** 仅在路径表达式的第一部分中允许。

在Handlebars中，由{{expression}}返回的值为 **HTML转义**. 如果表达式包含 `&`，则返回的HTML转义输出将生成为 `&amp;`. 如果你不希望Handlebars转义某个值，那就使用“三重藏货”。

## 配置文件

此命名空间允许您引用配置文件架构中定义的所有属性，详见 [Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}。

在 [!DNL Journey Optimizer] 个性化块。

>[!NOTE]
>
>了解如何在 [此部分](functions/helpers.md#if-function).

**示例引用：**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## 区段{#perso-segments}

了解如何在 [此部分](functions/helpers.md#if-function).

>[!NOTE]
>要了解有关分段和分段服务的更多信息，请参阅 [此部分](../segment/about-segments.md).

## 选件 {#offers-syntax}

此命名空间允许您引用现有选件决策。
要引用选件，您需要声明一个路径，其中包含定义选件的不同信息。

此路径具有以下结构：

`offers.Type.[Placement Id].[Activity Id].Attribute`

其中：

* `offers` 标识属于选件命名空间的路径表达式
* `Type`  确定选件表示的类型。 可能的值包括： `image`, `html` 和 `text`
* `Placement Id` 和 `Activity Id` 是放置和活动标识符
* `Attributes` 是选件特定的属性，取决于选件类型。 示例： `deliveryUrl` 对于图像

有关决策API和选件表示的更多信息，请参阅 [本页](../../using/offers/api-reference/decisions-api/deliver-offers.md)

所有引用都将通过选件架构通过 [本页](personalization-validation.md)

**示例引用：**

* 托管图像的位置：

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* 单击图像时的Target URL:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* 来自决策引擎的优惠的文本内容：

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* HTML来自决策引擎的优惠内容：

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## 辅助程序{#helpers-all}

Handlebars助手是一个简单的标识符，其后可能跟有参数。
每个参数都是Handlebars表达式。 这些帮助程序可以从模板中的任何上下文访问。

这些块帮助程序由帮助程序名称前的#标识，并且需要同名的匹配闭合/。
块是具有块开口({{# }})和关闭({{/}})。


>[!NOTE]
>
>有关帮助程序函数的详细信息，请参阅 [此部分](functions/helpers.md).

## 文字类型 {#literal-types}

[!DNL Adobe Journey Optimizer] 支持以下文字类型：

| 文字 | 定义 |
| ------- | ---------- |
| 字符串 | 数据类型，由被双引号括住的字符组成。 <br>示例: `"prospect"`, `"jobs"`, `"articles"` |
| 布尔型 | 数据类型为true或false。 |
| 整数 | 表示整数的数据类型。 可以是正数、负数或零。 <br>示例: `-201`, `0`, `412` |
| 数组 | 作为一组其他文字值组成的数据类型。 它使用方括号对不同值进行分组和逗号分隔。 <br> **注意：** 不能直接访问数组中项的属性。 <br> 示例: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>的使用 **xEvent** 变量在个性化表达式中不可用。 对xEvent的任何引用都将导致验证失败。

## URL个性化{#perso-urls}

个性化 URL 可将收件人引导至网站的特定页面，或引导至个性化的微型网站，具体取决于用户档案属性。在Adobe Journey Optimizer中，您可以向消息内容中的URL添加个性化。 URL 个性化可应用于文本和图像，并使用用户档案数据或上下文数据。

Journey Optimizer允许您通过向消息中的一个或多个个性化字段，来对其进行个性化。 要个性化URL，请执行以下步骤：

1. 在消息内容中创建链接。 [了解详情](../messages/message-tracking.md#insert-links)
1. 从个性化图标中，选择属性。 个性化图标仅适用于以下类型的链接： **外部链接**, **退订链接** 和 **选择退出**.

![](assets/perso-url.png)

>[!NOTE]
>
>在表达式编辑器中，当您编辑个性化的URL时，出于安全原因，帮助程序函数和区段成员资格会被禁用。

**个性化URL示例**

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!CAUTION]
>
>url中使用的个性化令牌不支持空格。
