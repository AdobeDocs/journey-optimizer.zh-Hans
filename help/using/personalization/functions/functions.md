---
title: 辅助函数入门
description: Journey Optimizer辅助函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: 9fa5330d766aa6fb1998e668a08d769d3fd1b2cc
workflow-type: tm+mt
source-wordcount: '2388'
ht-degree: 27%

---

# 辅助函数入门{#functions}

使用[!DNL Journey Optimizer]模板化语言对数据执行操作，如计算、数据格式或转换、条件，并在个性化上下文中处理这些操作。 在[此页面](../personalization-syntax.md)中了解个性化语法准则。



➡️[在此视频中了解如何使用辅助函数](#video)

在个性化编辑器的个性化下拉列表中提供的辅助函数中会利用模板语言，如下所示：

![](../assets/access-helper-functions.png)

>[!NOTE]
>
>个性化编辑器中的可用功能和功能与[历程高级表达式编辑器](../../building-journeys/expression/expressionadvanced.md)中的可用功能和功能不同。

在[!DNL Journey Optimizer]个性化编辑器中，辅助函数分为三类： [函数](#functions-helper)、[辅助函数](#helper-helper)和[运算符](#operators-helper)。

选择类别，以访问子类别和函数。

通过单击`>`图标访问子类别。 通过单击`+`图标选择一个函数：该函数会自动添加到个性化屏幕中。

单击`...`图标可查看函数的说明，并将其添加到收藏夹。 [了解详情](../personalize.md#fav)

## 功能{#functions-helper}

### 聚合和数组函数

<table>
    <tr>
        <td><a href="aggregation.md#average">平均</a></td><td>此函数返回数组中所有选定值的算术平均值。</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">计数</a></td><td>此函数返回给定数组中元素的数量。</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-only-null">Count Only Null</a></td><td>此函数对列表中的空值进行计数。</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-with-null">Count With Null</a></td><td>此函数对列表的所有元素（包括空值）进行计数</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinct</a></td><td>此函数从删除了重复值的数组或列表中获取值</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct-count-with-null">Distinct Count With Null</a></td><td>此函数对不同值（包括空值）进行计数</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">First item</a></td><td>此函数返回数组或列表中的第一项。</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">First n in array</a></td><td>当根据给定的数值表达式按升序排序时，此函数返回数组中的前“N”项</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">In</a></td><td>此函数用于确定一个项是否是一个数组或列表的成员</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Includes</a></td><td>此函数确定一个数组或列表是否包含给定项</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersects</a></td><td>此函数确定两个数组或列表是否至少有一个公共成员</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Last n in array</a></td><td>此函数返回数组中的最后“N”个项（当根据给定的数值表达式按升序排序时）</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Maximum</a></td><td>此函数返回数组中所有选定值中的最大值。</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimum</a></td><td>此函数返回数组中所有选定值中的最小值。</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Not in</a></td><td>此函数确定一个项是否不是一个数组或列表的成员</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Subset of</a></td><td>此函数确定特定数组（数组A）是否是另一个数组（数组B）的子集，即，如果数组A中的所有元素都是数组B的元素</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Sum</a></td><td>此函数返回数组中所有选定值的总和</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superset of</a></td><td>此函数确定特定数组（数组A）是否是另一个数组（数组B）的超集，即该数组A是否包含数组B中的所有元素</td>
    </tr>
</table>

### 日期时间函数{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#add-days">添加天数</a></td><td>此函数按指定的天数调整给定日期，使用正值递增，使用负值递减。</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-hours">添加小时数</a></td><td>此函数按指定的小时数调整给定日期，使用正值递增，使用负值递减。</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-minutes">添加分钟</a></td><td>此函数按指定的分钟数调整给定日期，使用正值递增，使用负值递减。</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-months">添加月份</a></td><td>此函数按指定的月数调整给定日期，使用正值递增，使用负值递减。</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-seconds">添加秒数</a></td><td>此函数按指定的秒数调整给定日期，使用正值递增，使用负值递减。</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-years">添加年份</a></td><td>此函数按指定的年数调整给定日期，使用正值递增，使用负值递减。</td>
    </tr>
    <tr>
        <td><a href="dates.md#age">Age</a></td><td>此函数从给定日期检索年龄。</td>
    </tr>
    <tr>
        <td><a href="dates.md#age-days">年龄（以天为单位）</a></td><td>此函数计算给定日期的年龄（以天为单位），即给定日期与当前日期之间经过的天数，对于未来日期为负值，对于过去日期为正值。</td>
    </tr>
    <tr>
        <td><a href="dates.md#age-months">年龄（以月为单位）</a></td><td>此函数计算给定日期的年龄（以月为单位），即给定日期与当前日期之间经过的月数（对于未来日期为负，对于过去日期为正）。</td>
    </tr>
    <tr>
        <td><a href="dates.md#compare-dates">比较日期</a></td><td>此函数将第一个输入日期与另一个输入日期进行比较。如果日期1 等于日期2，则返回 0；如果日期1 早于日期2，则返回 -1；如果日期1 晚于日期2，则返回 1。</td>
    </tr>
    <tr>
        <td><a href="dates.md#convert-zoned-date-time">转换分区日期时间</a></td><td>此函数将日期时间转换为给定时区。</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">Current time in milliseconds</a></td><td>此函数检索当前时间（以纪元毫秒为单位）。</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">Date difference</a></td><td>此函数检索两个日期之间的天数差。</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-month">每月的第几日</a></td><td>此函数返回代表月份的天数。</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">Day of week</a></td><td>此函数检索星期几。</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">Day of year</a></td><td>此函数检索年中日（该年的第几天）。</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-seconds">秒数差</a></td><td>此函数返回两个日期之间的秒数差。</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-hours">提取小时数</a></td><td>此函数从给定的时间戳中提取小时数组件。</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-minutes">提取分钟数</a></td><td>此函数从给定的时间戳中提取分钟数组件。</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-months">提取月数</a></td><td>此函数从给定的时间戳中提取月数组件。</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-seconds">提取秒数</a></td><td>此函数从给定的时间戳中提取秒数组件。</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">设置日期格式</a></td><td>此函数设置日期时间值的格式。</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date-locale">支持区域设置的日期格式</a></td><td>此函数将日期时间值格式化为其相应的语言敏感表示形式，即所需的区域设置中。</td>
    </tr>
    <tr>
        <td><a href="dates.md#get-current-zoned-date-time">获取 CurrentZonedDateTime</a></td><td>此函数返回当前日期和时间以及时区信息。</td>
    </tr>
    <tr>
        <td><a href="dates.md#hours-difference">小时数差</a></td><td>此函数以小时数返回两个日期之间的差值。</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-minutes">分钟数差</a></td><td>此函数返回两个日期之间的分钟数差。</td>
    </tr>
    <tr>
        <td><a href="dates.md#months-difference">月数差</a></td><td>此函数按月返回两个日期之间的差值。</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">Set Days</a></td><td>此函数为给定的日期时间设置月中日（该月中的第几天）。</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">Set Hours</a></td><td>此函数设置日期时间的小时。</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-date-time">To Date Time</a></td><td>此函数将字符串转换为日期。 对于无效的输入，它返回纪元日期作为输出。</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">To UTC</a></td><td>此函数将日期时间转换为 UTC。</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-day">截断到一天的开始</a></td><td>此函数修改给定的日期时间，将其设置为一天的开始时间（00:00）。</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-quarter">截断到一季度的开始</a></td><td>此函数在00:00将日期时间截断为其季度的第一天（例如，1月1日、4月1日、7月1日、10月1日）。
</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-week">截断到一周的开始</a></td><td>此函数修改给定的日期时间，将其设置为一周的开始时间（星期一 00:00）。</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-year">截断到一年的开始</a></td><td>此函数修改给定的日期时间，将其截断到一年的第一天（1 月 1 日），时间为 00:00。</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">Week of year</a></td><td>此函数返回年中周（该年中的第几周）</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-years">年数差异</a></td><td>此函数返回两个日期之间的年数差。</td>
    </tr>
</table>
</table>

### 映射函数 {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">Get</a></td><td>此函数用于检索给定键的映射值</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">键</a></td><td>此函数用于检索给定映射的所有键。</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">值</a></td><td>此函数检索给定映射的所有值。</td>
    </tr>
</table>

### 数学函数 {#math-functions}

<table>
    <tr>
        <td><a href="math.md#absolute">Absolute</a></td><td>此函数将任意数字格式化为其区分语言的表示形式。</td>
    </tr>
    <tr>
        <td><a href="math.md#format-number">设置数字格式</a></td><td>此函数将任意数字格式化为其区分语言的表示形式。</td>
    </tr>
    <tr>
        <td><a href="math.md#random">Random</a></td><td>此函数返回一个 0 到 1 之间的随机值</td>
    </tr>
    <tr>
        <td><a href="math.md#round-down">Round down</a></td><td>此函数对一个数字进行向下舍入。</td>
    </tr>
    <tr>
        <td><a href="math.md#round-up">Round up</a></td><td>此函数对一个数字进行向上舍入。</td>
    </tr>
    <tr>
    <td><a href="math.md#to-hex-string">到十六进制字符串</a></td><td>将任意数字转换为十六进制字符串。</td>
    </tr>
    <tr>
    <td><a href="math.md#to-int">ToInt</a></td><td>将任意这些类型（数字、双精度、整数、长整数、浮点数、短整数、字节、布尔值、字符串）转换为整数。</td>
    </tr>
    <tr>
        <td><a href="math.md#to-percentage">目标百分比</a></td><td>此函数将一个数字转换为百分比。</td>
    </tr>
    <tr>
        <td><a href="math.md#to-precision">到精度</a></td><td>此函数将一个数字转换为所需的精度。</td>
    </tr>
    <tr>
        <td><a href="math.md#to-string">目标字符串</a></td><td>此函数将任意数字转换为其字符串表示形式。 </td>
    </tr>
</table>

### 对象函数 {#object-functions}

<table>
    <tr>
        <td><a href="objects.md#isNotNull">不为空</a></td><td>此函数用于确定是否存在对象引用</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">为空</a></td><td>此函数用于确定对象引用是否不存在</td>
    </tr>
</table>

### 字符串函数 {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">驼峰式大小写</a></td><td>此函数用于将字符串中每个单词的第一个字母变为大写。</td>
    </tr>
    <tr>
        <td><a href="string.md#char-code-at">字符代码位于</a></td><td>此函数返回字符的ASCII值，与JavaScript中的charCodeAt函数类似</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concat</a></td><td>此函数用于将两个字符串组合为一个</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Contains</a></td><td>此函数用于确定一个字符串是否包含指定的子字符串。</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">不包含</a></td><td>此函数用于确定一个字符串是否不包含指定的子字符串。</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">Does not end with</a></td><td>此函数用于确定一个字符串是否不以指定的子字符串结尾。</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">Does not start with</a></td><td>此函数用于确定一个字符串是否不以指定的子字符串开头。</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">编码64</a></td><td>此函数用于对字符串进行编码。</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">结束于</a></td><td>此函数用于确定一个字符串是否以指定的子字符串结尾。</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">等于</a></td><td>此函数用于确定一个字符串是否不以指定的子字符串开头，且区分大小写</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Equals Ignore Case</a></td><td>此函数用于确定一个字符串是否不以指定的子字符串开头，不区分大小写</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">提取电子邮件域</a></td><td>此函数用于提取电子邮件地址的域</td>
    </tr>
    <tr>
        <td><a href="string.md#format-currency">设置货币格式</a></td><td>此函数根据在第二个参数中作为字符串传递的区域设置，将任何数字转换为相应的区分语言的货币表示形式</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-host">Get url host</a></td><td>此函数用于获取 URL 主机。</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-path">Get url path</a></td><td>此函数用于获取url路径。</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-protocol">Get url protocol</a></td><td>此函数用于获取url协议。</td>
    </tr>
    <tr>
        <td><a href="string.md#index-of">Index Of</a></td><td>此函数返回第二个参数在第一个参数中第一次出现的位置。如果没有匹配项，则返回–1</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>此函数用于检查字符串或表达式是否为空。</td>
    </tr>
    <tr>
        <td><a href="string.md#is-not-empty">Is Not Empty</a></td><td>如果参数中的字符串不为空，则此函数返回 true。</td>
    </tr>
    <tr>
        <td><a href="string.md#last-index-of">Last Index Of</a></td><td>此函数返回第二个参数在第一个参数中最后一次出现的位置。如果没有匹配项，则返回 -1。</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Left trim</a></td><td>此函数去除字符串开头的空格。</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Length</a></td><td>此函数用于获取字符串或表达式中的字符数。</td>
    </tr>
    <tr>
        <td><a href="string.md#like">喜欢</a></td><td>此函数用于确定一个字符串是否与指定的模式匹配</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">小写</a></td><td>此函数将字符串转换为小写字母。</td>
    </tr>
    <tr>
        <td><a href="string.md#mask">掩码</a></td><td>此函数用于将字符串的一部分替换为“X”字符。</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Matches</a></td><td>此函数用于确定一个字符串是否与特定的正则表达式匹配。</td>
    </tr>
    <tr>
        <td><a href="string.md#md5">MD5</a></td><td>此函数返回输入字符串的 md5 哈希值。</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">不等于</a></td><td>此函数用于确定一个字符串是否不等于指定的字符串。</td>
    </tr>
    <tr>
        <td><a href="string.md#not-equal-with-ignore-case">Not Equal With Ignore Case</a></td><td>此函数比较两个字符串（忽略大小写）。</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">正则表达式组</a></td><td>此函数用于根据提供的正则表达式提取特定信息</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">更换</a></td><td>此函数将字符串中的给定子字符串替换为另一个子字符串。</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">全部替换</a></td><td>此函数将匹配“target”的文本的所有子字符串替换为指定的文本“replacement”字符串</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Right trim</a></td><td>此函数去除字符串末尾的空格。 </td>
    </tr>
    <tr>
        <td><a href="string.md#split">拆分</a></td><td>此函数用于按给定字符拆分字符串。</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">开始于</a></td><td>此函数用于确定一个字符串是否以指定的子字符串开头。</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-date">String to date</a></td><td>此函数将一个字符串值转换为日期时间值。</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-integer">String to integer</a></td><td>此函数将一个字符串值转换为一个整数值。</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-number">String to number</a></td><td>此函数用于将字符串转换为数字。对于无效的输入，它返回相同字符串作为输出。</td>
    </tr>
    <tr>
        <td><a href="string.md#sub-string">Sub string</a></td><td>此函数返回字符串表达式在开始索引和结束索引之间的子字符串。</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">字首大写</a></td><td>此函数用于将字符串中每个单词的首字母大写。</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">To Bool</a></td><td>此函数根据类型将一个参数值转换为布尔值。</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">To Date Time</a></td><td>此函数用于将字符串转换为日期。对于无效的输入，它返回纪元日期作为输出。</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time-only">To Date Time only</a></td><td>此函数将一个参数值转换为仅日期时间值。 对于无效的输入，它返回纪元日期作为输出。</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">修剪</a></td><td>此函数去除字符串开头和结尾的空格。</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Upper case</a></td><td>此函数将一个字符串转换为大写字母。</td>
    </tr>
    <tr>
        <td><a href="string.md#url-decode">Url decode</a></td><td>此函数用于对 URL 编码的字符串进行解码。</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">Url encode</a></td><td>此函数用于对一个字符串进行 URL 编码。</td>
    </tr>
</table>


## 辅助程序{#helper-helper}

帮助程序在[此页面](helpers.md)中有详细介绍。


<table>
    <tr>
        <td><a href="helpers.md#default">默认回退值</a></td><td>此函数用于呈现默认变量</td>
    </tr>
    <tr>
        <td><a href="helpers.md#each">Each</a></td><td>此函数用于在数组上迭代</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">如果</a></td><td>此函数用于定义条件块 — 如果表达式求值返回true，则呈现块</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Let</a></td><td>此函数允许将表达式存储为变量，以便稍后在查询中使用</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">Unless</a></td><td>此函数用于定义一个条件块 — 如果表达式求值返回false，则会呈现块</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">With</a></td><td>此函数用于更改模板部分的求值令牌</td>
    </tr>
</table>

## 操作员{#operators-helper}

### 算术函数 {#arithmetic-helper}

算术函数用于对值进行基本计算。

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">加法</a></td><td>此运算符用于求两个参数表达式的总和</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">除</a></td><td>此运算符用于查找两个参数表达式的商</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">乘法</a></td><td>此运算符用于查找两个参数表达式的乘积</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">余数</a> </td><td>此运算符用于查找将两个参数表达式相除后的余数</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">减法</a> </td><td>此运算符计算两个表达式之间的差异</td>
    </tr>
</table>


### 布尔函数 {#boolean-functions}

布尔函数用于对不同元素执行布尔逻辑。

<table>
    <tr>
        <td><a href="operators.md#and">与</a></td><td>此运算符创建逻辑连接</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">或</a></td><td>此运算符创建逻辑分离</td>
    </tr>
</table>


### 比较函数 {#comparison-functions}

比较函数用于比较不同表达式和值之间的差异，从而相应地返回true或false。

<table>
    <tr>
        <td><a href="operators.md#equals">等于</a></td><td>此操作检查值是否相等</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">大于</a></td><td>此运算符检查第一个值是否大于第二个值</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">大于或等于</a></td><td>此运算符检查第一个值是否大于或等于第二个值</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">小于或等于</a> </td><td>此运算符检查第一个值是否小于或等于第二个值</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">不等于</a></td><td>此运算符检查给定的表达式是否不等于给定的值</td>
    </tr>
</table>

## 操作方法视频{#video}

了解如何使用个性化辅助函数转换个性化值以及辅助函数的不同用例。

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
