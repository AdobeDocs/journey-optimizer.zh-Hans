---
title: 个性化配方
description: Adobe Journey Optimizer的常见个性化模式和现实示例
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: id: cb09dcb7-3367-4b63-b02c-8a1356eb876eid: ac5d9310-7772-40fb-9d78-864562e1bfd6
source-git-commit: 18067b68e09b98e616126dd40b8ad729233c49fa
workflow-type: tm+mt
source-wordcount: 1530
ht-degree: 0%

---

# 个性化配方 {#personalization-recipes}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;查找可直接复制到Adobe Journey Optimizer内容中的日期、数组、字符串、条件逻辑和PQL边缘案例的现成个性化脚本。

>[!ENDSHADEBOX]

本页为Adobe Journey Optimizer中最常见的用例提供现成的个性化模式。 所有示例都使用个性化编辑器语法，并可直接复制到电子邮件、短信或推送内容中。

有关可用函数的完整引用，请参阅[帮助程序函数](functions/helpers.md)、[日期/时间函数](functions/dates.md)、[字符串函数](functions/string.md)和[数组函数](functions/arrays-list.md)。

>[!TIP]
>
>在复制示例之前，请查看[Personalization最佳实践](personalization-syntax.md#best-practices)以避免最常见的语法错误。

## 日期和时间指导方针 {#date-time-recipes}

### 方法1 — 以可读格式显示当前日期 {#recipe-current-date}

使用带`getCurrentZonedDateTime()`的`formatDate`以任意格式呈现今天的日期：

```sql
{%= formatDate(getCurrentZonedDateTime(), "MMMM dd, yyyy") %}
```

输出（示例）： `April 11, 2026`

**常见格式模式：**

| 模式 | 输出示例 |
|---------|---------------|
| `"dd/MM/yyyy"` | `11/04/2026` |
| `"MM/dd/yyyy"` | `04/11/2026` |
| `"EEEE, MMMM dd"` | `Saturday, April 11` |
| `"yyyy-MM-dd"` | `2026-04-11` |

>[!NOTE]
>
>使用小写`y`（日历年）而不是`Y`（基于周的年）以避免在年边界出现意外结果。 有关完整引用，请参阅[模式字符](functions/dates.md#pattern-characters)。

### 方法2 — 到期或事件日期的倒计时 {#recipe-countdown}

使用`dateDiff`计算配置文件日期属性剩余的天数，然后动态渲染它：

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
{%#if daysLeft > 0%}
Your reward points expire in {{daysLeft}} day{%#if daysLeft > 1%}s{%/if%}. Use them before they're gone!
{%else%}
Your reward points have expired.
{%/if%}
```

输出（示例）： `Your reward points expire in 7 days. Use them before they're gone!`

### 方法3 — 动态结束日期之前的X天 {#recipe-days-before}

要计算配置文件属性之前X天的日期（例如，在内容或主题行中引用），请使用具有负偏移量的`addDays`：

```sql
{%= formatDate(addDays(stringToDate(profile.subscription.endDate), -7), "MMMM dd, yyyy") %}
```

输出（示例）： `April 04, 2026` *（4月11日前7天）*

若要同时设置一天中的固定时间（例如，上午9点），请与`setHours`合并：

```sql
{%= formatDate(setHours(addDays(stringToDate(profile.subscription.endDate), -7), 9), "dd/MM/yyyy HH:mm") %}
```

### 方法4 — 将当前时间仅显示为HH:MM {#recipe-time-only}

使用`extractHours`和`extractMinutes`只显示时间部分，前导为0的保护时间为分钟：

```handlebars
{% let h = extractHours(getCurrentZonedDateTime()) %}
{% let m = extractMinutes(getCurrentZonedDateTime()) %}
Your appointment is at {{h}}:{%#if m < 10%}0{%/if%}{{m}}.
```

输出（示例）： `Your appointment is at 14:05.`

### 方法5 — 检测周末与工作日 {#recipe-weekend}

使用`dayOfWeek`根据日期调整内容。 此函数返回1（星期一）到7（星期日）。 使用单个`=`运算符（PQL语法，而不是`==`）：

```handlebars
{%#if dayOfWeek(getCurrentZonedDateTime()) = 6 or dayOfWeek(getCurrentZonedDateTime()) = 7%}
We're closed on weekends — our team will follow up on the next business day.
{%else%}
Our team will get back to you within 24 hours.
{%/if%}
```

>[!NOTE]
>
>`dayOfWeek()`用于根据日期调整&#x200B;**内容**。 对于在历程中基于星期以不同方式路由用户档案，请在历程条件活动中使用内置的&#x200B;**时间条件→星期几**&#x200B;选项。 [了解详情](../building-journeys/condition-activity.md#date_condition)

## 阵列和循环方法 {#array-recipes}

### 方法6 — 列出配置文件数组中的所有项目 {#recipe-list-items}

使用`{{#each}}`对配置文件数组进行迭代并渲染每个项。 这仅在个性化编辑器（电子邮件、短信、推送）中可用：

```handlebars
{{#each profile.purchases.recentItems}}
  - {{this.name}}: {{this.price}}&euro;
{{/each}}
```

输出（示例）：

```
- Running shoes: 89&euro;
- Water bottle: 15&euro;
- Gym bag: 45&euro;
```

>[!NOTE]
>
>历程条件活动不支持`{{#each}}`。 若要在条件中筛选数组，请使用[集合管理函数](../building-journeys/expression/collection-management-functions.md)。

### 方法7 — 按价格显示数组中的前N个项目 {#recipe-first-n}

使用`topN`按数值字段对前N个项进行排序和检索。 由于`topN`是PQL函数，请首先将其分配给包含`{% let %}`的变量，然后使用`{{#each}}`循环：

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

>[!NOTE]
>
>`topN(profile.orders, price, 3)`按`price`降序排序并返回前3项 — 它不会简单地返回原始数组顺序中的前3项。

或者使用`head`仅获取单个顶级项：

```sql
{%= head(profile.purchases.recentItems).name %}
```

### 方法8 — 有条件地按数组项呈现内容 {#recipe-conditional-loop}

在`{{#each}}`中使用`{%#if%}`仅呈现匹配项的输出。 使用`as |order|`定义循环别名，以便PQL计算器能够解析条件中的属性引用：

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending — we'll notify you when it ships.
  {%/if%}
{{/each}}
```

>[!NOTE]
>
>`this.status`在Handlebars表达式中工作，但未由`{%#if%}`内的PQL计算器解析。 使用命名循环别名（例如`order`）使该属性对Handlebars和PQL上下文均可用。

## 字符串和格式设置脚本 {#string-recipes}

### 方法9 — 使用replaceAll清理字符串并重复使用 {#recipe-replaceall-reuse}

`replaceAll`返回一个新值 — 它不会修改原始值。 使用`{% let %}`存储结果并多次引用它，而无需重复函数调用：

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}},
Your exclusive code is: WELCOME-{%= upperCase(cleanName) %}
```

输出（示例）：

```
Hi John,
Your exclusive code is: WELCOME-JOHN
```

### 方法10 — 在JSON输出中用双引号引出一个值 {#recipe-json-quotes}

要在字符串中包含字面双引号（例如，为自定义有效负载生成JSON），请使用反斜杠(`\"`)对其进行转义：

```handlebars
{ "greeting": "Hello \"{{profile.person.name.firstName}}\"" }
```

输出： `{ "greeting": "Hello \"John\"" }`

### 方法11 — 将日期组件设置为大写格式 {#recipe-uppercase-date}

将`formatDate`与`upperCase`结合使用，以大写形式呈现月份或日期名称：

```sql
{%= upperCase(formatDate(getCurrentZonedDateTime(), "MMMM")) %}
```

输出（示例）： `APRIL`

对于完整的大写日期字符串：

```sql
{%= upperCase(formatDate(profile.person.birthDateTime, "EEEE MMMM dd yyyy")) %}
```

输出（示例）： `WEDNESDAY JANUARY 01 2020`

## 条件逻辑脚本 {#conditional-recipes}

### 方法12 — 个性化内容中的IF/ELSEIF/ELSE {#recipe-if-elseif}

对多分支条件逻辑使用`{%#if%}`、`{%else if%}`和`{%else%}`。 此模式适用于电子邮件内容和片段：

```handlebars
{%#if profile.loyalty.tier = "gold"%}
As a Gold member, enjoy free shipping on all orders.
{%else if profile.loyalty.tier = "silver"%}
As a Silver member, enjoy free shipping on orders over &euro;50.
{%else%}
Join our loyalty program to unlock exclusive benefits.
{%/if%}
```

### 方法13 — 空安全属性显示 {#recipe-null-safe}

使用条件回退以避免在配置文件属性可能为null或缺失时呈现空值：

```handlebars
{%#if profile.person.name.firstName%}
Hi {{profile.person.name.firstName}},
{%else%}
Hi there,
{%/if%}
```

或使用`isEmpty`以三元样式模式内联：

```handlebars
Hi {%#if isEmpty(profile.person.name.firstName)%}valued customer{%else%}{{profile.person.name.firstName}}{%/if%},
```

## PQL边缘案例配方 {#pql-edge-cases}

### 方法14 — 引用连字符属性键 {#recipe-hyphenated-key}

如果XDM架构字段名称包含连字符（例如`order-total`， `event-type`），请在PQL表达式中以反撇号将其换行，以防止将连字符解释为减法运算符：

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>仅在PQL表达式(`{%= ... %}`)中支持反撇号。 在普通Handlebars插值(`{{...}}`)中不接受它们。 如果您需要直接渲染连字符字段值，请通过PQL表达式计算该值，或先使用`{% let %}`将其存储在变量中。

### 方法15 — 在上下文属性中引用数值事件ID {#recipe-numeric-event-id}

使用ID为数字字符串（例如`1697323153`）的历程上下文事件时，请用反撇号将ID换行，并将`{% let %}`与`toDateTime()`和`formatDate()`一起使用：

```handlebars
{% let appointmentDate = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy HH:mm") %}
Your appointment: {{appointmentDate}}
```

输出（示例）： `Your appointment: 18/03/2026 14:30`

### 方法16 — 类型强制：将字符串字段与数字进行比较 {#recipe-type-coercion}

PQL是强类型。 当个人资料字段存储为字符串但您需要对其进行数字比较时，请先将其与`stringToNumber()`进行转换：

```sql
{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}
```

对于存储为字符串的布尔字段：

```sql
{%= toBool(profile.consents.email.val) = true %}
```

## 快速参考 {#quick-reference}

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

>[!BEGINTABS]

>[!TAB 概述]

**TL；DR**

本页提供了16种现成的复制粘贴个性化脚本，其中涵盖日期、数组、字符串、条件逻辑和PQL边缘案例，分别用于Journey Optimizer电子邮件、短信和推送内容。

**意图**

* 复制现成的日期/时间模式（当前日期、倒计时、偏移日期、时间显示、周末检测）
* 复制数组和循环模式（列表项、前N个项、按项条件渲染）
* 复制字符串格式模式（清理并重用字符串、JSON引号、大写日期组件）
* 复制条件逻辑模式（多分支if/elseif/else、null-safe属性显示）
* 处理PQL边缘情况（连字符键、数字事件ID、类型强制）

>[!TAB 术语表]

* **Personalization方法**：使用个性化编辑器语法，为常见的个性化用例提供现成的复制 — 粘贴模式。 *（产品特定）*
* **`formatDate`**：使用指定的格式模式（如`"MMMM dd, yyyy"`）将日期转换为字符串的函数。
* **`dateDiff`**：计算两个日期之间数值差异的函数。
* **`getCurrentZonedDateTime()`**：以时区感知格式返回当前日期和时间的函数。
* **`topN`**：一个PQL函数，它按指定的数值字段以降序对数组进行排序，并返回前N项。 必须先通过`{% let %}`分配，然后才能在Handlebars循环中使用。
* **`{% let %}`**：用于存储计算值的Handlebars变量赋值语法；在后续Handlebars上下文中需要引用PQL函数结果时需要。
* **`replaceAll`**：一个字符串函数，它替换字符串中所有出现的模式；返回一个新的字符串而不修改原始字符串。

>[!TAB 术语]

* **规范名称：**&#x200B;个性化方法 — 变体：模式，模板，例如，复制粘贴模式
* **不要混淆：** `{%= ... %}` （PQL表达式语法 — 已计算，返回计算值）≠`{{...}}` （Handlebars插值 — 呈现变量或模板表达式）
* **请勿混淆：** `{%#if%}` / `{%/if%}` （Journey Optimizer条件语法，% — 大括号）≠ `{{#if}}` / `{{/if}}` （标准Handlebars条件语法）
* **不要混淆：** `topN(array, field, n)` （按字段降序排序，返回前N个）≠`head(array)` （仅返回数组中的第一项）
* **不要混淆：** `dayOfWeek()` （在消息内容中用于根据日期调整显示）≠历程时间条件“星期”选项（在历程条件活动中用于以不同方式路由用户档案）
* **请勿混淆：**&#x200B;日期格式模式`y` （日历年 — 正确）≠`Y` （基于周的年份 — 可能会在年边界产生意外结果）

>[!TAB 护栏和限制]

* 历程条件活动中不支持`{{#each}}`；请使用集合管理函数在历程条件中筛选数组。
* 仅在PQL表达式(`{%= ... %}`)中支持连字符属性键的反勾转义；在纯Handlebars插值(`{{...}}`)中不接受反勾选。
* `topN`是PQL函数，必须分配给`{% let %}`变量，才能用作`{{#each}}`循环目标。
* 在`{%#if%}`块中使用循环变量时，声明命名循环别名（如`as |order|`）；`{%#if%}`内的PQL计算器未解析`this.status`。
* 在日历年的`formatDate`模式中使用小写`y`；`Y`（基于周的年份）可能会在年终边界生成意外的值。

>[!TAB 常见问题解答]

**问：在个性化中，`{%= ... %}`与`{{...}}`之间有何区别？**

`{%= ... %}`是PQL表达式语法 — 对其进行计算并返回计算值（数字、字符串、布尔值）。 `{{...}}`是Handlebars插值 — 它呈现变量或模板表达式。 两者均显示在个性化内容中，但其用途不同。

**问：如何在Handlebars `{{#each}}`循环中使用PQL函数结果？**

使用`{% let variableName = pqlFunction(...) %}`将PQL函数结果分配给变量，然后使用`{{#each variableName}}`对其进行迭代。

**问：`{{#each}}`能否在历程条件活动中使用？**

没有。 `{{#each}}`仅在消息个性化内容（电子邮件、短信、推送）中可用。 要在历程条件中筛选数组，请使用集合管理函数。

**问：如何引用名称包含连字符的字段？**

在PQL表达式中，用反撇号将连字符键换行： ``{%= profile.events.`order-total` > 100 %}``。 纯Handlebars插值不支持反撇号 — 如果需要，请使用`{% let %}`变量作为中间步骤。

**问：为什么`topN`在`{{#each}}`循环之前需要`{% let %}`？**

`topN`是一个返回PQL列表的PQL函数。 将其分配给`{% let %}`变量可使结果在Handlebars上下文中可用，以便可将其与`{{#each}}`一起迭代。

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 20c7ee0f -->

