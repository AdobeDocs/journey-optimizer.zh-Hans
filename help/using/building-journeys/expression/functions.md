---
solution: Journey Optimizer
product: journey optimizer
title: 功能
description: 了解历程表达式中的函数
feature: Journeys
role: Developer
level: Experienced
keywords: 函数，表达式，编辑器，历程，数据，操作
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1339
ht-degree: 6%

---

# 功能 {#functions}

函数是Adobe Journey Optimizer中动态旅程表达式的构建块。 它们使您能够实时转换、计算、验证和处理数据，以创建个性化的客户体验。 通过将60多种功能划分到直观的类别中，您可以在客户历程的每个步骤中构建复杂的条件、执行复杂的计算并做出数据驱动型决策。

## 了解函数

历程表达式中的函数遵循一致的语法模式：

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, ... ,`<expression as param N>`)

**关键特性：**

* **多个签名**：函数可以有不同的签名（不同的有序参数集）以适应不同的用例
* **特定于类型的返回**：每个函数都有一个特定的返回类型（字符串、整数、布尔值、日期、列表等）
* **Zero到N参数**：函数可以接受0-N表达式作为排序参数，这提供了使用它们的灵活性

## 为何使用函数？

函数使您能够：

* **创建动态条件** — 基于实时数据评估的分支旅程路径
* **大规模个性化** — 使用客户数据和行为分析定制内容和体验
* **自动执行决策** — 无需手动干预即可构建智能逻辑
* **转换数据** — 转换、格式化和处理数据类型以确保兼容性
* **执行计算** — 执行数学运算和统计分析
* **验证输入** — 在执行操作之前检查数据质量和完整性

## 按类别列出的函数

浏览按主要目的组织的功能，快速找到符合您需求的合适工具。

### Adobe Experience Platform {#aep-functions}

**受众分段和定位**

评估受众成员资格，以根据Adobe Experience Platform中定义的客户区段创建个性化的历程路径。

| 函数 | 描述 |
|----------|-------------|
| [inAudience](../functions/functioninaudience.md) | 检查个人是否属于特定受众 |

[查看Adobe Experience Platform函数详细信息→](../functions/functioninaudience.md)

### 聚合函数 {#aggregation-functions}

**统计计算和数据汇总**

对值集执行计算以得出平均值、计数、总和以及最小/最大值等见解。 对于数据驱动型决策至关重要。

| 函数 | 描述 |
|----------|-------------|
| [avg](../functions/aggregation-functions.md#avg) | 计算平均值 |
| [count](../functions/aggregation-functions.md#count) | 对非null元素计数 |
| [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) | 仅对null值进行计数 |
| [countWithNull](../functions/aggregation-functions.md#countWithNull) | 计算所有元素（包括null） |
| [distinctCount](../functions/aggregation-functions.md#distinctCount) | 计算唯一的非空值 |
| [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) | 计算包括null的唯一值 |
| [max](../functions/aggregation-functions.md#max) | 查找最大值 |
| [min](../functions/aggregation-functions.md#min) | 查找最小值 |
| [sum](../functions/aggregation-functions.md#sum) | 计算总和 |

[查看所有聚合函数→](../functions/aggregation-functions.md)

### 转换函数 {#conversion-functions}

**数据类型转换**

在不同类型（字符串、整数、小数、布尔值、日期、持续时间）之间转换数据，以确保操作和数据源之间的兼容性。

| 函数 | 描述 |
|----------|-------------|
| [toBool](../functions/conversion-functions.md#toBool) | 转换为布尔值 |
| [toDateOnly](../functions/conversion-functions.md#toDateOnly) | 仅转换为日期（无时间） |
| [toDateTime](../functions/conversion-functions.md#toDateTime) | 转换为日期（含时间） |
| [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) | 转换为不带时区的日期时间 |
| [toDecimal](../functions/conversion-functions.md#toDecimal) | 转换为十进制数 |
| [toDuration](../functions/conversion-functions.md#toDuration) | 转换为持续时间 |
| [toInteger](../functions/conversion-functions.md#toInteger) | 转换为整数 |
| [toString](../functions/conversion-functions.md#toString) | 转换为字符串 |

[查看所有转换函数→](../functions/conversion-functions.md)

### 日期函数 {#date-functions}

**日期和时间操作**

使用日期、时间和时区创建基于时间的条件、计划操作和执行临时计算。

| 函数 | 描述 |
|----------|-------------|
| [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) | 获取当前时间（以毫秒为单位） |
| [inLastDays](../functions/date-functions.md#inLastDays) | 检查日期是否在过去的N天内 |
| [inLastHours](../functions/date-functions.md#inLastHours) | 检查日期是否在过去的N小时内 |
| [inLastMonths](../functions/date-functions.md#inLastMonths) | 检查日期是否在过去的N个月内 |
| [inLastYears](../functions/date-functions.md#inLastYears) | 检查日期是否在过去的N年内 |
| [inNextDays](../functions/date-functions.md#inNextDays) | 检查日期是否在未来N天内 |
| [inNextHours](../functions/date-functions.md#inNextHours) | 检查日期是否在接下来的N小时内 |
| [inNextMonths](../functions/date-functions.md#inNextMonths) | 检查日期是否在未来N个月内 |
| [inNextYears](../functions/date-functions.md#inNextYears) | 检查日期是否在未来N年内 |
| [now](../functions/date-functions.md#now) | 获取当前日期时间 |
| [nowWithDelta](../functions/date-functions.md#nowWithDelta) | 使用偏移量获取当前时间 |
| [setHours](../functions/date-functions.md#setHours) | 在日期时间中设置特定小时数 |
| [setDays](../functions/date-functions.md#setDays) | 在日期时间中设置特定日期 |
| [updateTimeZone](../functions/date-functions.md#updateTimeZone) | 更新日期时间的时区 |

[查看所有日期函数→](../functions/date-functions.md)

### 列表函数 {#list-functions}

**集合操作和分析**

筛选、排序、转换和分析数组和列表，以处理复杂的数据结构并执行集合操作。

| 函数 | 描述 |
|----------|-------------|
| [distinct](../functions/list-functions.md#distinct) | 获取唯一值（不包括null） |
| [distinctWithNull](../functions/list-functions.md#distinctWithNull) | 获取唯一值（包括null） |
| [筛选器](../functions/list-functions.md#filter) | 根据条件筛选列表 |
| [getListItem](../functions/list-functions.md#getListItem) | 获取特定索引处的项目 |
| [in](../functions/list-functions.md#in) | 检查值是否存在于列表中 |
| [相交](../functions/list-functions.md#intersect) | 查找列表之间的通用元素 |
| [限制](../functions/list-functions.md#limit) | 限制返回的项目数 |
| [listSize](../functions/list-functions.md#listSize) | 获取列表大小 |
| [serializeList](../functions/list-functions.md#serializeList) | 将列表转换为字符串 |
| [sort](../functions/list-functions.md#sort) | 对列表元素排序 |

[查看所有列表函数→](../functions/list-functions.md)

### 数学函数 {#math-functions}

**数学运算**

执行数值计算和转换，以实现数据处理和业务逻辑。

| 函数 | 描述 |
|----------|-------------|
| [random](../functions/math-functions.md#random) | 生成随机数(0-1) |
| [round](../functions/math-functions.md#round) | 四舍五入到最近的整数 |

[查看所有数学函数→](../functions/math-functions.md)

### 字符串函数 {#string-functions}

**文本操作和验证**

处理、转换、搜索和验证文本数据，用于动态内容创建和条件逻辑。

| 函数 | 描述 |
|----------|-------------|
| [concat](../functions/string-functions.md#concat) | 连接字符串 |
| [contain](../functions/string-functions.md#contain) | 检查字符串是否包含子字符串 |
| [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) | 检查包含（不区分大小写） |
| [endWith](../functions/string-functions.md#endWith) | 检查字符串是否以后缀结尾 |
| [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) | 检查结束于（不区分大小写） |
| [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) | 比较字符串（不区分大小写） |
| [indexOf](../functions/string-functions.md#indexOf) | 查找第一个发生位置 |
| [isEmpty](../functions/string-functions.md#isEmpty) | 检查字符串是否为空 |
| [isNotEmpty](../functions/string-functions.md#isNotEmpty) | 检查字符串是否不为空 |
| [lastIndexOf](../functions/string-functions.md#lastIndexOf) | 查找最后一个发生位置 |
| [length](../functions/string-functions.md#length) | 获取字符串长度 |
| [lower](../functions/string-functions.md#lower) | 转换为小写 |
| [matchRegExp](../functions/string-functions.md#matchRegExp) | 匹配正则表达式 |
| [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) | 检查不等于（区分大小写） |
| [replace](../functions/string-functions.md#replace) | 替换第一个匹配项 |
| [replaceAll](../functions/string-functions.md#replaceAll) | 替换所有匹配项 |
| [split](../functions/string-functions.md#split) | 将字符串拆分为数组 |
| [startWith](../functions/string-functions.md#startWith) | 检查字符串是否以前缀开头 |
| [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) | 检查开头为（不区分大小写） |
| [substr](../functions/string-functions.md#substr) | 提取子字符串 |
| [trim](../functions/string-functions.md#trim) | 删除前导/尾随空格 |
| [upper](../functions/string-functions.md#upper) | 转换为大写 |
| [uuid](../functions/string-functions.md#uuid) | 生成UUID |

[查看所有字符串函数→](../functions/string-functions.md)

## 后续步骤

现在您已了解可用的功能，接下来请探索：

* **[高级表达式编辑器](expressionadvanced.md)** — 了解如何使用高级编辑器构建复杂表达式
* **[表达式语法](generalities.md)** — 掌握用于编写历程表达式的语法规则
* **[运算符](operators.md)** — 发现可用于生成逻辑的函数的运算符
* **[字段引用](field-references.md)** — 了解如何在表达式中引用数据字段

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;此页面是历程高级表达式编辑器中所有可用的60多个内置函数的分类引用，这些函数包括聚合、转换、日期/时间、列表、数学、字符串和Adobe Experience Platform受众函数。

**意图：**

* 通过浏览分类函数表确定任务的正确函数
* 使用转换函数在字符串、整数、小数、布尔值、日期和持续时间之间转换数据类型
* 使用诸如`inLastDays`、`inNextHours`和`nowWithDelta`之类的函数执行基于日期的筛选
* 使用诸如`contain`、`replace`、`split`和`trim`之类的函数操纵和验证字符串值
* 使用聚合函数（如`count`、`avg`、`sum`和`distinctCount`）对集合执行统计计算
* 使用`inAudience`函数检查历程条件中的受众成员资格

**术语表：**

* **聚合函数**：从值集合&#x200B;*（产品特定）*&#x200B;计算单个值（计数、总和、平均值、最小值、最大值）的函数
* **转换函数**：将值从一个数据类型转换为另一个数据类型的函数（例如`toString`、`toDateTime`、`toDuration`）*（产品特定）*
* **日期函数**：用于处理历程表达式&#x200B;*（产品特定）*&#x200B;中的日期、时间和时区值的函数
* **列表函数**：用于筛选、排序和分析数组/集合数据的函数&#x200B;*（产品特定）*
* **inAudience**：检查配置文件是否属于指定的Adobe Experience Platform受众区段&#x200B;*（产品特定）*&#x200B;的函数

**护栏：**

* 函数遵循一致的语法： `functionName(param1, param2, ...)`
* 函数可以有多个特征码（不同的参数集）来处理不同的用例
* 每个函数都有一个固定的返回类型 — 确保返回类型与表达式上下文所需的类型匹配
* 历程表达式编辑器中的可用函数与个性化编辑器中的可用函数不同

**术语：**

* 规范名称：函数 — 首字母缩略词：none — 变体：内置函数，表达式函数
* 同义词：&quot;aggregation functions&quot; = &quot;statistical functions&quot;；&quot;conversion functions&quot; = &quot;type casting functions&quot;
* 请勿混淆：历程表达式函数≠个性化编辑器函数（不同的集）

**常见问题解答：**

* **问：历程表达式编辑器中有多少函数可用？**  — 超过60个函数按不同类别进行整理，其中包括聚合、转化、日期、列表、数学、字符串和Adobe Experience Platform。
* **问：如何检查配置文件是否属于历程条件中的受众？**  — 将`inAudience`函数与受众标识符一起使用。
* **问：我应该使用哪个函数来获取当前日期和时间偏移天数？**  — 使用`nowWithDelta(N, "days")`获取当前时间的dateTime偏移。
* **问：函数能否根据调用方式返回不同的类型？**  — 函数在每个签名中都有一个特定的返回类型，但单个函数名可以有多个具有不同参数集和返回类型的签名。
* **问：`count`与`countWithNull`之间有何区别？** — `count`只计算非null元素；`countWithNull`计算包括null的所有元素。

+++
