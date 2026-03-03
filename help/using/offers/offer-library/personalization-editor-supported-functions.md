---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 个性化编辑器中支持的功能
description: 了解在决策管理(Offer Decisioning)中个性化优惠内容时支持哪些个性化编辑器功能。
badge: label="旧版" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
exl-id: c4df41a2-d740-437c-acc3-957508c4a1c0
source-git-commit: c15bae97ea52243d65aa59fdd4e924dc4e1852d8
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 15%

---

# 个性化编辑器中支持的功能 {#personalization-editor-supported-functions}

在决策管理中，当您&#x200B;**添加呈现**&#x200B;并个性化[优惠内容](add-representations.md)（优惠中的图像、文本、链接）时，请使用&#x200B;**个性化编辑器**。

在个性化该内容时，Offer Decisioning后端仅支持个性化编辑器中可用函数的&#x200B;**子集**。 此页面列出了可在选件内容编辑器中安全使用的每个功能。 展开每个部分以查看支持的运算符、帮助程序和函数。

>[!NOTE]
>
>此函数列表仅将&#x200B;**应用于个性化优惠内容**（呈现）。 决策规则和排名公式使用不同的编辑器，并且不限于此子集。

## 支持的函数列表 {#supported-functions-list}

+++ 操作员

* 算术：`+` `-` `*` `/` `%`
* 逻辑： `and` `or` `!`
* 比较： `=` `!=` `>` `>=` `<` `<=`

+++

+++ 辅助程序

* 每个
* 替换为
* 如果
* Unless
* Let
* 默认回退值
* 片段
* datasetLookup
* externalDataLookup (Alpha)
* 内嵌
* Url
* 执行元数据
* valueAt路径

+++

+++ 字符串函数

| 显示名称 | 内部名称 |
|--------------|---------------|
| 小写 | lowerCase |
| 大写 | 大写 |
| 驼峰式拼写 | camelCase |
| 字首大写 | titleCase |
| 修剪 | trim |
| Left Trim | leftTrim |
| Right Trim | rightTrim |
| 为空 | isEmpty |
| Equals Ignore Case | equalsIgnoreCase |
| 不等于，忽略大小写 | notEqualWithIgnoreCase |
| 替换 | replace |
| 全部替换 | replaceAll |
| Concat | concat |
| 拆分 | split |
| Encode64 | encode64 |
| 长度 | 长度 |
| MD5 | md5 |
| SHA256 | sha256 |
| 类似 | like |
| 开头为 | startsWith |
| 开头不是 | doesNotStartWith |
| 结束于 | endsWith |
| 结尾不是 | doesNotEndWith |
| 包含 | 包含 |
| 不包含 | doesNotContain |
| 等于 | 等于 |
| 不等于 | notEqualto |
| 匹配 | matches |
| 正则表达式组 | 正则表达式组 |
| 字符串到数字 | stringToNumber |
| String to date | stringToDate |
| To Date Time | toDateTime |
| To Date Time Only | toDateTimeOnly |
| 提取电子邮件域 | extractEmailDomain |
| 提取电子邮件用户名 | extractEmailUsername |
| 不为空 | isNotEmpty |
| 索引： | indexOf |
| 最后索引： | lastIndexOf |
| 子字符串 | substr |
| To Bool | toBool |
| String to integer | string_to_integer |
| 蒙版 | 蒙版 |
| 获取格式货币 | formatCurrency |
| 获取字符的unicode值 | charCodeAt |
| 获取任何文本的二维码 | 二维码 |

+++

+++ 数组、列表和集合函数

| 显示名称 | 内部名称 |
|--------------|---------------|
| Distinct | distinct |
| 在 | in |
| 不在 | notIn |
| 相交 | 相交 |
| 子集 | subsetOf |
| 超集 | 超集 |
| 包括 | 包含 |
| 排序并获取数组中的前N个 | topN |
| 排序并获取数组中的最后N个 | bottomN |
| 第一个项目 | head |
| Count | count |
| Sum | sum |
| 平均 | 平均 |
| 最小值 | min |
| 最大值 | max |

+++

+++ 映射函数

| 显示名称 | 内部名称 |
|--------------|---------------|
| Get | get |
| 键 | 键 |
| 值 | 值 |

+++

+++ 目标函数

| 显示名称 | 内部名称 |
|--------------|---------------|
| Is null | isNull |
| 不为null | isNotNull |

+++

+++ 数学函数

| 显示名称 | 内部名称 |
|--------------|---------------|
| 目标百分比 | toPercentage |
| Round Up | 汇总 |
| Round down | roundDown |
| 到Precision | toPrecision |
| 绝对 | 绝对 |
| Random | random |
| 到十六进制 | toHexString |
| 获取区域设置的编号 | 格式数字 |
| 目标字符串 | toString |
| 到Int | toInt |
| 到长 | toLong |

+++

+++ 日期时间函数

| 显示名称 | 内部名称 |
|--------------|---------------|
| 现在 | now |
| 获取CurrentZoneDateTime | getCurrentZonedDateTime |
| 结束日期 | toDate |
| 结束时间 | toTime |
| To Date Time | toDateTime |
| To Date Time Only | toDateTimeOnly |
| 仅截止日期 | toDateOnly |
| 仅至时间 | toTimeOnly |
| 到时区 | toTimeZone |
| 设置日期格式 | formatdate |
| 设置日期时间格式 | formatDateTime |
| 设置时间格式 | formatTime |
| 解析日期 | parseDate |
| 分析日期时间 | parseDateTime |
| 解析时间 | parseTime |
| 添加天数 | addDays |
| 添加月份 | addMonths |
| 添加年份 | addYears |
| 添加小时 | addHours |
| 添加分钟 | addMinutes |
| 添加秒数 | addSeconds |
| 减去天数 | subtractDays |
| 减去月份 | subtractMonths |
| 减去年数 | subtractyears |
| 减去小时 | subtracthours |
| 减去分钟 | subtractminutes |
| 减去秒 | subtractSeconds |
| 天数差异 | diffDays |
| 月份差异 | diffmonths |
| 年差异 | diffyears |
| 小时差异 | diffhours |
| 差异（分钟） | diffMinutes |
| 以秒为单位的差异 | diffSeconds |
| 一天开始 | startOfDay |
| 一天结束时 | endOfDay |
| 早于 | isBefore |
| 晚于 | isAfter |

+++

+++ URL函数

| 显示名称 | 内部名称 |
|--------------|---------------|
| 编码URL | encodeUrl |
| 解码URL | decodeUrl |
| 获取URL查询参数 | getUrlQueryParam |
| 获取URL协议 | getUrlProtocol |
| 获取URL主机 | getUrlHost |

+++

>[!NOTE]
>
>在对选件内容进行个性化时，如果您使用的函数不在上述列表中，则表达式可能会在运行时失败或产生意外结果。 有关[!DNL Journey Optimizer]个性化中可用的整套功能，请参阅[帮助程序功能列表](../../personalization/functions/functions.md)。 Offer Decisioning中个性化内容仅支持此页面上记录的子集。
