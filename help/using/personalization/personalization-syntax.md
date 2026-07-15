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
TQID: https://experienceleague.adobe.com/kZEw2lITdt8SMWMe-UT2vPzdoiAjB2vbItmK9zt-WJo
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: id: ac5d9310-7772-40fb-9d78-864562e1bfd6id: e51e8901-97d9-4f7d-a835-503025a90e32
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1979
ht-degree: 2%

---

# 个性化语法 {#personalization-syntax}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解Adobe Journey Optimizer中的Handlebars和PQL个性化语法，包括常规规则、保留关键词、类型强制、可用命名空间和最佳实践。

>[!ENDSHADEBOX]

[!DNL Journey Optimizer]中的Personalization使用两种互补语法，它们在同一表达式中协同工作：

* **Handlebars** (`{{...}}`) — 用于呈现配置文件属性、通过数组循环和调用块帮助程序。 有关完整参考，请参阅[HandlebarsJS文档](https://handlebarsjs.com/)。
* **Profile Query Language (PQL)** (`{%= ... %}`) — 用于调用内置函数（如`upperCase()`、`formatDate()`、`dateDiff()`）并计算条件表达式。

了解您所处的上下文是避免运行时错误的关键。 例如，置于`{{...}}`内的PQL函数调用将失败，因为Handlebars尝试将其解析为帮助程序，而不是将其计算为PQL表达式。

**示例：**

| 用例 | 句法 |
|----------|--------|
| 呈现配置文件属性 | `{{profile.person.name.firstName}}` |
| 调用PQL函数 | `{%= upperCase(profile.person.name.firstName) %}` |
| 条件块 | `{%#if profile.loyalty.tier = "gold"%}...{%/if%}` |
| 在阵列上循环 | `{{#each profile.orders}}...{{/each}}` |

属性结构在Adobe Experience Platform XDM架构中定义。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}。

>[!TIP]
>
>有关将这些语法应用于现实场景的现成表达式（日期格式、倒计时、条件回退等），请参阅&#x200B;**[Personalization方法](personalization-recipes.md)**&#x200B;页面。

## 语法一般规则 {#general-rules}

* 标识符可以是任何Unicode字符，但为Handlebars语法保留的以下特殊字符除外：

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* 语法区分大小写。

* 仅在路径表达式的第一部分中允许使用单词&#x200B;**true**、**false**、**null**&#x200B;和&#x200B;**undefined**。

* 在Handlebars中，{{expression}}返回的值是&#x200B;**HTML转义**。 如果表达式包含`&`，则返回的HTML转义输出将生成为`&amp;`。 如果不希望Handlebars转义值，请使用“三重存储”。

  假设字段`profile.person.name`的值为“Mark &amp; Mary”。 语法`{{profile.person.name}}`将显示`Mark &amp; Mary`，而`{{{profile.person.name}}}`将显示`Mark & Mary`。

* 关于文字函数参数，模板化语言解析器不支持单个未转义的反斜杠(`\`)符号。 此字符必须使用额外的反斜杠(`\`)符号进行转义。 示例：

  `{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

* 要在字符串值中包含&#x200B;**文本双引号**（例如，在生成JSON输出时），请使用反斜杠(`\"`)对其进行转义：

  ```handlebars
  { "message": "Hello \"{{profile.person.name.firstName}}\"" }
  ```

  输出： `{ "message": "Hello \"John\"" }`

  或者，当值本身包含您不希望HTML编码的特殊字符时，使用三重存储`{{{ }}}`输出未转义的HTML。

## 保留关键词 {#reserved-keywords}

某些关键字在Profile Query Language (PQL)中是保留关键字，不能直接用作个性化表达式中的字段或变量名称。 如果XDM架构包含名称与保留关键词匹配的字段，则必须使用反撇号(`` ` ``)对其进行转义，以在表达式中引用它们。

**保留的关键字包括：**

* `next`
* `last`
* `this`

**示例：**

如果您的配置文件架构具有一个名为`next`的字段，则必须用反勾号将其换行：

```
{{profile.person.`next`.name}}
```

如果没有回退，个性化编辑器将验证失败并出现错误。

>[!NOTE]
>
>保留关键字的反勾转义适用于`{{...}}` Handlebars路径和`{%= ... %}` PQL表达式，因为这些关键字在路径解析级别保留。 这与连字符字段名称不同，在连字符字段中，仅在PQL表达式中支持反勾转义。 请参阅[连字符属性键](#hyphenated-keys)。

## 特殊属性键的PQL语法规则 {#pql-special-keys}

除了保留的关键字之外，还有两种情况需要在PQL表达式中进行反勾转义。

### 连字符属性键 {#hyphenated-keys}

如果XDM架构包含字段名称带有连字符（如`my-field`、`event-type`），或者名称以数字开头或包含数字，请在PQL表达式中以反撇号将键换行：

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>仅在PQL表达式(`{%= ... %}`)中支持反勾转义。 在Handlebars插值(`{{...}}`)中不支持它。 但是，可以在`{{...}}`块中直接引用连字符字段名称（例如`{{profile.my-custom-field}}`）；只有反勾语法在该块中失败。

在PQL表达式中没有反撇号的情况下，连字符会被解释为减法运算符，并导致PQL语法错误。

### 上下文属性中的数字事件ID {#numeric-event-ids}

在引用事件ID为数字（例如`1697323153`）的上下文事件属性时，请用反勾号将其换行。 这也适用于诸如`formatDate()`之类的函数：

```handlebars
{% let ts = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy") %}
{{ts}}
```

## 强制键入 {#type-coercion}

PQL是强类型。 比较或传递值时，两边的类型必须相同。 常见案例：

| 场景 | 解决方案 |
|----------|----------|
| 存储为字符串的数值 | 在算术或比较前使用`stringToNumber()`： `{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}` |
| 存储为字符串的整数 | 在计算前使用`string_to_integer()`或`stringToNumber()` |
| 布尔值存储为字符串 | 使用`toBool()`进行转换： `{%= toBool(profile.consents.email.val) = true %}` |

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

## 辅助程序 {#helpers-all}

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
| 数组 | 由一组其他文字值组成的数据类型。 它使用方括号将不同的值分组，并使用逗号分隔不同的值。<br> **注意：**&#x200B;您不能直接访问数组中项的属性。<br> 示例： `[1, 4, 7]`，`["US", "FR"]` |

>[!CAUTION]
>
>**xEvent**&#x200B;变量的使用在个性化表达式中不可用。 对xEvent的任何引用都会导致验证失败。

## 最佳实践 {#best-practices}

在构建个性化表达式之前，请查看这些语法规则。 大多数运行时错误来自混合Handlebars和PQL上下文。

**使用正确的条件块语法**

始终使用`{%#if%}` / `{%else if%}` / `{%else%}` / `{%/if%}`。 不支持`{% if %}` / `{% elseif %}` / `{% endif %}`语法。

```handlebars
{%#if profile.loyalty.tier = "gold"%}
Gold member content
{%else if profile.loyalty.tier = "silver"%}
Silver member content
{%else%}
Default content
{%/if%}
```

**请勿在`{{...}}` Handlebars块中调用PQL函数**

`{{...}}`仅解析Handlebars变量和帮助程序 — 它不计算PQL。 将PQL函数（如`upperCase()`）包装在`{{...}}`中会导致“无法找到帮助程序”错误。 请改用`{%= ... %}`：

| 不正确 | 正确 |
|-----------|---------|
| `{{upperCase(cleanName)}}` | `{%= upperCase(cleanName) %}` |

**将`{{#each}}`与`{%#if%}`**&#x200B;组合时使用命名循环别名

`this.field`由Handlebars渲染器解析，但不由`{%#if%}`条件内的PQL计算器解析。 使用`as |item|`定义命名别名，以便两个上下文都可以解析该字段：

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending.
  {%/if%}
{{/each}}
```

**在循环前将PQL函数结果分配给变量**

不能直接在`{{#each}}`中调用PQL UDF（如`topN`）。 首先使用`{% let %}`对其进行评估，然后对结果进行迭代：

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

**使用`{% let %}`避免重复函数调用**

当计算值需要多次时，将其存储在变量中。 这样可提高可读性并防止冗余评估：

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}}, your code is: WELCOME-{%= upperCase(cleanName) %}
```

**对`dateDiff`**&#x200B;使用正确的参数顺序

`dateDiff(start, end)`首先采用较早的日期。 要计算未来日期前的剩余天数，请将当前日期作为第一个参数传递：

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
```

**在PQL中使用`=`进行等式比较，而不是`==`**

PQL使用单个`=`运算符实现相等。 使用`==`会导致语法错误。

**对连字符字段名称使用反撇号 — 仅在PQL表达式中**

如果XDM架构字段名称包含连字符（例如`order-total`），请用反撇号将其换行，以防止将连字符解析为减法运算符。 这仅在`{%= ... %}`个PQL表达式中受支持，在`{{...}}`个Handlebars块中不受支持：

```sql
{%= profile.events.`order-total` > 100 %}
```

对于可以直接复制到内容中的现成表达式，请参阅[Personalization脚本](personalization-recipes.md)。

## 快速参考 {#quick-reference}

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

>[!BEGINTABS]

>[!TAB 概述]

**TL；DR**

本页介绍Journey Optimizer中的Handlebars和PQL个性化语法 — 它们的一般规则、保留关键词、命名空间结构、类型系统和避免常见运行时错误的最佳实践。

**意图**

* 了解何时使用Handlebars (`{{...}}`)与PQL (`{%= ... %}`)语法
* 应用常规语法规则：保留字符、区分大小写、HTML转义、反斜杠处理
* 正确转义保留的关键字和特殊属性键（连字符名称、数字事件ID）
* 在比较或传递不匹配类型的值时应用类型强制
* 从可用命名空间引用个性化：个人资料、受众、选件
* 遵循最佳实践以避免最常见的运行时和验证错误

>[!TAB 术语表]

* **Handlebars**：用于呈现属性、循环数组以及调用块帮助程序的`{{...}}`模板语法；默认情况下，HTML-escapes输出。 *（产品特定）*
* **Profile Query Language (PQL)**：用于调用内置函数（如`upperCase()`、`formatDate()`）和计算条件表达式的`{%= ... %}`表达式语法。 *（产品特定）*
* **三重存储(`{{{ }}}`)**：一个Handlebars语法变量，它输出不带HTML转义的值，当值本身包含不应编码的HTML字符时很有用。
* **保留关键字**：不能直接用作字段或变量名称的PQL标识符(`next`、`last`、`this`)；当架构字段使用这些名称之一时，必须用反撇号括起来。
* **类型强制**：使用`stringToNumber()`或`toBool()`等函数将值从一种数据类型显式转换为另一种数据类型（例如字符串→数字），在PQL中比较或算术之前需要这些函数。
* **命名空间**：个性化数据的顶级分组 — 个人资料、受众、选件 — 每个分组都有自己的路径结构和访问规则。
* **块帮助程序**：在帮助程序名称和匹配的结束`/`之前由`#`标识的Handlebars帮助程序，用于块构造，如`{{#each}}`。

>[!TAB 术语]

* **规范名称：** Handlebars — 用于`{{...}}`语法； PQL — 用于`{%= ... %}`语法
* **请勿混淆：** `{{...}}` （Handlebars — 呈现变量和帮助程序，HTML转义）≠ `{%= ... %}` （PQL — 计算函数和表达式）≠ `{%#if%}` / `{%/if%}` （条件块语法，百分比大括号）
* **请勿混淆：** `{{profile.person.name}}` （单存储 — HTML转义输出）≠`{{{profile.person.name}}}` （三存储 — 未转义输出）
* **请勿混淆：**&#x200B;保留关键字反勾转义（适用于`{{...}}`和`{%= ... %}`）≠连字符键反勾转义（仅在`{%= ... %}`个PQL表达式中受支持，在`{{...}}`中不受支持）
* **请勿混淆：** `=` （PQL等式运算符 — 正确）≠`==` （无效的PQL — 导致语法错误）

>[!TAB 护栏和限制]

* `xEvent`变量在个性化表达式中不可用；对`xEvent`的任何引用都会导致验证失败。
* `{{...}}` Handlebars块中的PQL函数调用将失败；请改用`{%= ... %}`。
* 不支持`{% if %}` / `{% elseif %}` / `{% endif %}`条件语法；请使用`{%#if%}` / `{%else if%}` / `{%/if%}`。
* 仅在PQL表达式(`{%= ... %}`)中支持连字符字段名称的回勾转义。 在`{{...}}` Handlebars插值中，反勾语法失败，但连字符的字段名称仍可以直接引用（例如`{{profile.my-custom-field}}`）。
* 用作架构字段名称时，保留的关键字(`next`， `last`， `this`)必须用反撇号括起来；同时适用于`{{...}}`和`{%= ... %}`。
* 不支持将单反斜杠`\`作为文本函数参数；请使用双反斜杠`\\`。
* PQL是强类型；比较或算术中不匹配的类型需要使用`stringToNumber()`、`toBool()`或类似的强制函数进行显式转换。

>[!TAB 常见问题解答]

**问：何时应使用`{{...}}`，何时应使用`{%= ... %}`？**

使用`{{...}}` (Handlebars)呈现属性值、循环数组以及调用块帮助程序。 使用`{%= ... %}` (PQL)调用`upperCase()`和`formatDate()`等内置函数，并计算条件表达式。

**问：如何在不使用HTML编码的情况下输出值？**

使用三存储`{{{ }}}`而不是`{{...}}`。 单大括号Handlebars HTML-escapes输出（例如，`&`变为`&amp;`）；三存储绕过了转义。

**问：在PQL中，正确的相等运算符是什么？**

在PQL中使用单个`=`进行等式比较。 使用`==`是一个语法错误。

**问：如何引用名称为保留关键字（如`next`、`last`、`this`）的架构字段？**

以反撇号将其换行： `{{profile.person.\`next\`.name}}。 这适用于Handlebars路径和PQL表达式。

**问：能否在`{{...}}` Handlebars块中调用PQL函数？**

没有。 `{{...}}`仅解析Handlebars变量和帮助程序。 `{{...}}`中的PQL函数导致“无法找到帮助程序”错误。 请改用`{%= functionName(...) %}`。

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 7fa07aa5 -->
