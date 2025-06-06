---
solution: Journey Optimizer
product: journey optimizer
title: 编辑表达式
description: 了解如何编辑表达式。
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: bf0a905f-00af-4ed7-9e4f-bf8cb0af9ea9
source-git-commit: 04a21534d91e4fcfa550af50450ea241c9b1235c
workflow-type: tm+mt
source-wordcount: '2114'
ht-degree: 29%

---


# 编辑表达式 {#edit-expressions}

+++ 目录

| 欢迎使用编排的营销活动 | 启动您的第一个编排的营销活动 | 查询数据库  | 编排的营销活动活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](configuration-steps.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建协调的营销活动](create-orchestrated-campaign.md)<br/><br/>[协调的营销活动设置](orchestrated-campaign-settings.md)<br/><br/>[协调的活动](orchestrate-activities.md)<br/><br/>[发送包含协调的营销活动的消息](send-messages.md)<br/><br/>[开始并监视营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/><b>[编辑表达式](edit-expressions.md)</b> | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[And-join](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!NOTE]
>
>以下部分提供了有关如何使用表达式编辑器构建规则的信息。 请记住，用于构建规则的语法不同于用于添加个性化的语法。

## 使用表达式编辑器 {#edit}

编辑表达式需要手动输入条件以形成规则。 此模式允许您使用高级函数，这些函数允许您处理用于执行特定查询（如处理日期、字符串、数字字段和排序）的值。

在配置自定义条件时，表达式编辑器可从规则生成器&#x200B;**[!UICONTROL 编辑表达式]**&#x200B;按钮中使用，该按钮可用于&#x200B;**[!UICONTROL 属性]**&#x200B;和&#x200B;**[!UICONTROL 值]**&#x200B;字段。

| 从&#x200B;**属性**&#x200B;字段访问 | 从&#x200B;**值**&#x200B;字段访问 |
| --- | --- |
| 属性字段](assets/rule-builder-expression-access-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"}的![表达式编辑器 | 值字段](assets/rule-builder-expression-access-value.png){zoomable="yes"}{width="200" align="center" zoomable="yes"}的![表达式编辑器 |

表达式编辑器提供：

* 定义了表达式的&#x200B;**输入字段(1)**。
* 可用的&#x200B;**字段(2)**&#x200B;的列表，这些字段可在表达式中使用并对应于查询的定向维度。
* **辅助函数(3)**，按类别排序。

通过直接在输入字段中输入表达式来编辑表达式。 要添加字段或辅助函数，请将光标置于要添加该字段或辅助函数的表达式中，然后单击+按钮。

![表达式编辑器界面](assets/rule-builder-expression-editor.png){zoomable="yes"}

## 辅助功能

利用查询编辑工具，可使用高级功能根据所需结果和操作数据的类型执行复杂筛选。 可以使用以下函数：

### 总计

聚合函数对一组值执行计算。

<table>
<tbody>
<tr>
<td><strong>名称</strong></td>
<td><strong>描述</strong></td>
<td><strong>语法</strong></td>
</tr>
<tr>
<td><strong>平均</strong></td>
<td>返回数字类型列的平均值</td>
<td>Avg（&lt;值&gt;）</td>
</tr>
<tr>
<td><strong>计数</strong></td>
<td>计算列的非空值</td>
<td>Count（&lt;值&gt;）</td>
</tr>
<tr>
<td><strong>全部计数</strong></td>
<td>计算返回的值（所有字段）</td>
<td>CountAll()</td>
</tr>
<tr>
<td><strong>Countdistinct</strong></td>
<td>计算列的不同非空值</td>
<td>Countdistinct（&lt;值&gt;）</td>
</tr>
<tr>
<td><strong>最大值</strong></td>
<td>返回数字、字符串或日期类型列的最大值</td>
<td>Max（&lt;值&gt;）</td>
</tr>
<tr>
<td><strong>最小值</strong></td>
<td>返回数字、字符串或日期类型列的最小值</td>
<td>Min（&lt;值&gt;）</td>
</tr>
<tr>
<td><strong>标准开发</strong></td>
<td>返回数字、字符串或日期列的标准偏差</td>
<td>StdDev（&lt;值&gt;）</td>
</tr>
<tr>
<td><strong>字符串聚合</strong></td>
<td>返回字符串类型列的值的连接，在第二个参数中用字符分隔</td>
<td>StringAgg（&lt;值&gt;， &lt;字符串&gt;）</td>
</tr>
<tr>
<td><strong>Sum</strong></td>
<td>返回数字、字符串或日期类型列的值的总和</td>
<td>Sum（&lt;值&gt;）</td>
</tr>
</tbody>
</table>

### 日期

日期函数处理日期或时间值。

<table>
<tbody>
<tr>
<td><strong>名称</strong></td>
<td><strong>描述</strong></td>
<td><strong>语法</strong></td>
</tr>
<tr>
<td><strong>AddDays</strong></td>
<td>向日期添加天数</td>
<td>AddDays（&lt;日期&gt;， &lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>AddHours</strong></td>
<td>向日期添加小时数</td>
<td>AddHours（&lt;日期&gt;， &lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>AddMinutes</strong></td>
<td>向日期添加分钟数</td>
<td>AddMinutes（&lt;日期&gt;， &lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>AddMonths</strong></td>
<td>向日期添加月数</td>
<td>AddMonths（&lt;日期&gt;， &lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>AddSeconds</strong></td>
<td>向日期添加秒数</td>
<td>AddSeconds（&lt;日期&gt;， &lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>AddYears</strong></td>
<td>向日期添加年数</td>
<td>AddYears（&lt;日期&gt;， &lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>ConvertNTZ</strong></td>
<td>应用定义的会话TZ，将时间戳NTZ（不带时区的时间戳）转换为TZ（带时区的时间戳）</td>
<td>ConvertNTZ（&lt;日期+时间&gt;）</td>
</tr>
<tr>
<td><strong>DateCmp</strong></td>
<td>比较两个日期</td>
<td>DateCmp（&lt;日期&gt;， &lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>DateOnly</strong></td>
<td>仅返回日期（且时间为00:00）</td>
<td>DateOnly（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>日</strong></td>
<td>返回表示日期天数的数字</td>
<td>Day（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>DayOfYear</strong></td>
<td>返回日期年份中的天数</td>
<td>DayOfYear（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>天前</strong></td>
<td>返回对应于当前日期n天的日期</td>
<td>DaysAgo（&lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>DaysAgoInt</strong></td>
<td>返回对应于当前日期n天的日期（整数yyyymmdd）</td>
<td>DaysAgoInt（&lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>DaysDiff</strong></td>
<td>返回两个日期之间的天数</td>
<td>DaysDiff（&lt;结束日期&gt;， &lt;开始日期&gt;）</td>
</tr>
<tr>
<td><strong>Daysold</strong></td>
<td>返回日期的年龄（以天为单位）</td>
<td>DaysOld（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>GetDate</strong></td>
<td>返回服务器的当前系统日期</td>
<td>GetDate()</td>
</tr>
<tr>
<td><strong>小时</strong></td>
<td>返回日期的小时数</td>
<td>Hour（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>HoursDiff</strong></td>
<td>返回两个日期之间的小时数之差</td>
<td>HoursDiff（&lt;结束日期&gt;， &lt;开始日期&gt;）</td>
</tr>
<tr>
<td><strong>分钟</strong></td>
<td>返回日期的分钟数</td>
<td>Minute（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>MinutesDiff</strong></td>
<td>返回两个日期之间的分钟数之差</td>
<td>MinutesDiff（&lt;结束日期&gt;， &lt;开始日期&gt;）</td>
</tr>
<tr>
<td><strong>月</strong></td>
<td>返回表示日期月份的数字</td>
<td>Month（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>MonthsAgo</strong></td>
<td>返回对应于当前日期n个月的日期</td>
<td>MonthsAgo（&lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>MonthsDiff</strong></td>
<td>返回两个日期之间的月数</td>
<td>MonthsDiff（&lt;结束日期&gt;， &lt;开始日期&gt;）</td>
</tr>
<tr>
<td><strong>MonthsOld</strong></td>
<td>返回日期的年龄（月数）</td>
<td>MonthsOld（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>Oldest</strong></td>
<td>返回范围内最早的日期</td>
<td>Oldest（&lt;日期，日期&gt;）</td>
</tr>
<tr>
<td><strong>秒</strong></td>
<td>返回日期的秒数</td>
<td>Second（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>SecondsDiff</strong></td>
<td>返回两个日期之间的秒数</td>
<td>SecondsDiff（&lt;结束日期&gt;， &lt;开始日期&gt;）</td>
</tr>
<tr>
<td><strong>subdays</strong></td>
<td>从日期减去天数</td>
<td>SubDays（&lt;日期&gt;， &lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>subhours</strong></td>
<td>从日期减去小时数</td>
<td>SubHours（&lt;日期&gt;， &lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>subminutes</strong></td>
<td>从日期减去分钟数</td>
<td>SubMinutes（&lt;日期&gt;， &lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>submonths</strong></td>
<td>从日期减去月数</td>
<td>SubMonths（&lt;日期&gt;， &lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>SubSeconds</strong></td>
<td>从日期减去秒数</td>
<td>SubSeconds（&lt;日期&gt;， &lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>subyears</strong></td>
<td>从日期减去年数</td>
<td>SubYears（&lt;日期&gt;， &lt;数字&gt;）</td>
</tr>
<tr>
<td><strong>ToDate</strong></td>
<td>将日期+时间转换为日期</td>
<td>ToDate（&lt;日期+时间&gt;）</td>
</tr>
<tr>
<td><strong>ToDateTime</strong></td>
<td>将字符串转换为日期+时间</td>
<td>ToDateTime（&lt;字符串&gt;）</td>
</tr>
<tr>
<td><strong>ToTimestamp</strong></td>
<td>将字符串转换为时间戳</td>
<td>ToTimestamp（&lt;字符串&gt;）</td>
</tr>
<tr>
<td><strong>ToTimeZone</strong></td>
<td>将日期+时间转换为时区</td>
<td>TotimeZone（&lt;日期&gt;， &lt;时区&gt;&gt;）</td>
</tr>
<tr>
<td><strong>TruncDate</strong></td>
<td>将日期+时间舍入到最接近的秒数</td>
<td>TruncDate(@lastModified， &lt;秒数&gt;)</td>
</tr>
<tr>
<td><strong>TruncDateTZ</strong></td>
<td>将日期+时间舍入为以秒表示的精度</td>
<td>TruncDateTZ（&lt;日期&gt;， &lt;秒数&gt;， &lt;时区&gt;&gt;）</td>
</tr>
<tr>
<td><strong>TruncQuarter</strong></td>
<td>将日期舍入到季度</td>
<td>TruncQuarter（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>trunctime</strong></td>
<td>将时间部分舍入到最接近的秒</td>
<td>TruncTime（&lt;日期&gt;， &lt;秒数&gt;）</td>
</tr>
<tr>
<td><strong>TruncWeek</strong></td>
<td>将日期舍入到周</td>
<td>TruncWeek（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>TruncYear</strong></td>
<td>将日期+时间舍入到年度的1月1日</td>
<td>TruncYear（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>WeekDay</strong></td>
<td>返回表示日期一周中某天的数字（0=星期一，6=星期日）</td>
<td>WeekDay（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>年</strong></td>
<td>返回表示日期年份的数字</td>
<td>Year（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>YearAndMonth</strong></td>
<td>返回表示日期的年份和月份的数字</td>
<td>YearAndMonth（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>YearAgo</strong></td>
<td>返回给定日期与当前日期之间的年数之差</td>
<td>YearsAgo（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>YearsDiff</strong></td>
<td>返回两个日期之间的年数之差</td>
<td>YearsDiff（&lt;结束日期&gt;， &lt;开始日期&gt;）</td>
</tr>
<tr>
<td><strong>YearsOld</strong></td>
<td>返回日期的年龄（以年为单位）</td>
<td>YearsOld（&lt;日期&gt;）</td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>请注意，**DateOnly**&#x200B;函数考虑的是服务器的时区，而不是运算符的时区。


### 地理位置营销

利用地理位置营销函数来操作地理值。

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名称</strong><br /> </td> 
   <td> <strong>描述</strong><br /> </td> 
   <td> <strong>语法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Distance</strong><br /> </td> 
   <td> 返回由经度和纬度定义的两点之间的距离，以度表示。<br /> </td> 
   <td> Distance(&lt;经度 A&gt;, &lt;纬度 A&gt;, &lt;经度 B&gt;, &lt;纬度 B&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 数值

数值函数用于将文本转换为数字。

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名称</strong><br /> </td> 
   <td> <strong>描述</strong><br /> </td> 
   <td> <strong>语法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Abs</strong><br /> </td> 
   <td> 返回数字的绝对值<br /> </td> 
   <td> Abs(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> 返回大于或等于某个数字的最小整数<br /> </td> 
   <td> Ceil(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Floor</strong><br /> </td> 
   <td> 返回大于或等于数字<br />的最大整数 </td> 
   <td> Floor(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Greatest</strong><br /> </td> 
   <td> 返回两个数字中的较大者<br /> </td> 
   <td> Greatest(&lt;数字 1&gt;, &lt;数字 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Least</strong><br /> </td> 
   <td> 返回两个数字中的较小者<br /> </td> 
   <td> Least(&lt;数字 1&gt;, &lt;数字 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> 返回n1除以n2<br />的整数除余数 </td> 
   <td> Mod(&lt;数字 1&gt;, &lt;数字 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Percent</strong><br /> </td> 
   <td> 返回两个数字的比值，以百分比表示<br /> </td> 
   <td> Percent(&lt;数字 1&gt;, &lt;数字 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Random</strong><br /> </td> 
   <td> 返回随机值<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Round</strong><br /> </td> 
   <td> 将数字舍入为 n 位小数<br /> </td> 
   <td> Round(&lt;数字&gt;, &lt;小数&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Sign</strong><br /> </td> 
   <td> 返回数字的符号<br /> </td> 
   <td> Sign(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> 将整数转换为浮点<br /> </td> 
   <td> ToDouble(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> 将浮点转换为 64 位整数<br /> </td> 
   <td> ToInt64(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> 将浮点转换为整数<br /> </td> 
   <td> ToInteger(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> 将 n1 取整到 n2 位小数<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 其他 

此表包含剩余的可用函数。

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名称</strong><br /> </td> 
   <td> <strong>描述</strong><br /> </td> 
   <td> <strong>语法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AESEncrypt</strong><br /> </td> 
   <td> 加密参数<br />中提供的字符串 </td> 
   <td> AESEncrypt（&lt;值&gt;）<br /> </td> 
  </tr>
  <tr> 
   <td> <strong>Case</strong><br /> </td> 
   <td> 如果条件为true，则返回值1。 如果不存在，则返回值2.<br /> </td> 
   <td> Case(When(&lt;条件&gt;, &lt;值 1&gt;), Else(&lt;值 2&gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> 删除值中的标志<br /> </td> 
   <td> ClearBit(&lt;标识符&gt;, &lt;标识&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> 如果值 1 为 0 或 null，则返回值 2，否则返回值 1<br /> </td> 
   <td> Coalesce(&lt;值 1&gt;, &lt;值 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Decode</strong><br /> </td> 
   <td> 如果值1 =值2，则返回值3。 如果未返回值4.<br /> </td> 
   <td> Decode(&lt;值 1&gt;, &lt;值 2&gt;, &lt;值 3&gt;, &lt;值 4&gt;)<br /> </td>  
  </tr>

<tr> 
   <td> <strong>Else</strong><br /> </td> 
   <td> 返回值 1（只能用作 case 函数的参数）<br /> </td> 
   <td> Else（&lt;值1&gt;， &lt;值2&gt;）<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> 从电子邮件地址提取域名<br /> </td> 
   <td> GetEmailDomain(&lt;值&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> 检索镜像页面服务器的 URL<br /> </td> 
   <td> GetMirrorURL(&lt;值&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> 如果表达式为true，则返回值1。 如果不存在，则返回值2<br /> </td> 
   <td> Iif(&lt;条件&gt;, &lt;值 1&gt;, &lt;值 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> 指示标志是否在值中<br /> </td> 
   <td> IsBitSet(&lt;标识符&gt;, &lt;标识&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> 如果字符串1为空，则返回值2，否则返回值3<br /> </td> 
   <td> IsEmptyString（&lt;值1&gt;， &lt;值2&gt;， &lt;值3&gt;）<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NewUUID</strong><br /> </td> 
   <td> 返回唯一ID<br /> </td> 
   <td> NewUUID()<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> 如果参数为 NULL，则返回空字符串<br /> </td> 
   <td> NoNull(&lt;值&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> 返回行号<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> 强制将标志设在值中<br /> </td> 
   <td> SetBit(&lt;标识符&gt;, &lt;标识&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> 将数字转换为布尔值<br /> </td> 
   <td> ToBoolean(&lt;数字&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>When</strong><br /> </td> 
   <td> 如果表达式为true，则返回值1。 如果不是，则返回值2（只能用作case函数的参数）<br /> </td> 
   <td> When(&lt;条件&gt;, &lt;值 1&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 字符串

字符串函数用于操作一系列字符串。

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名称</strong><br /> </td> 
   <td> <strong>描述</strong><br /> </td> 
   <td> <strong>语法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> 指示所有参数是否为非 null 且不为空<br /> </td> 
   <td> AllNonNull2（&lt;字符串&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> 指示所有参数是否为非 null 且不为空<br /> </td> 
   <td> AllNonNull3（&lt;字符串&gt;， &lt;字符串&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ascii</strong><br /> </td> 
   <td> 返回字符串中第一个字符的ASCII值。<br /> </td> 
   <td> Ascii（&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> 返回与 ASCII 代码"n"对应的字符<br /> </td> 
   <td> Char（&lt;数字&gt;）<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> 返回字符串1中字符串2的位置。<br /> </td> 
   <td> Charindex（&lt;字符串&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>数据长度</strong><br /> </td> 
   <td> 返回字符串<br />的大小（以字节为单位） </td> 
   <td> dataLength（&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> 返回字符串的 n（从 1 到 n）行<br /> </td> 
   <td> GetLine（&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> 如果前两个参数相等，则返回第三个参数。 如果不是，则返回最后一个参数<br /> </td> 
   <td> IfEquals（&lt;字符串&gt;， &lt;字符串&gt;， &lt;字符串&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> 指示作为参数传递的 Memo 是否为 null<br /> </td> 
   <td> IsMemoNull(&lt;memo&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> 将作为参数传递的字符串连接起来。 如有必要，在字符串之间添加空格。<br /> </td> 
   <td> JuxtWords（&lt;字符串&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> 将作为参数传递的字符串连接起来。 如有必要，在字符串之间添加空格<br /> </td> 
   <td> JuxtWords3（&lt;字符串&gt;， &lt;字符串&gt;， &lt;字符串&gt;）<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Left</strong><br /> </td> 
   <td> 返回字符串的前 n 个字符<br /> </td> 
   <td> Left（&lt;字符串&gt;， &lt;数字&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Length</strong><br /> </td> 
   <td> 返回字符串<br />的长度 </td> 
   <td> Length（&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>行</strong><br /> </td> 
   <td> 从字符串<br />中提取行n </td> 
   <td> Line（&lt;字符串&gt;，&lt;数字&gt;）<br /></td> 
  </tr>
  <tr> 
   <td> <strong>Lower</strong><br /> </td> 
   <td> 以小写形式返回字符串<br /> </td> 
   <td> Lower（&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> 返回左侧的已完成字符串<br /> </td> 
   <td> LPad （&lt;字符串&gt;， &lt;数字&gt;， &lt;字符&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> 删除字符串左侧的空格<br /> </td> 
   <td> Ltrim（&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> 返回字符串以十六进制表示的 MD5 键值<br /> </td> 
   <td> Md5Digest（&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>MemoContains</strong><br /> </td> 
   <td> 指定 Memo 是否包含作为参数传递的字符串<br /> </td> 
   <td> MemoContains（&lt;memo&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>节点值</strong><br /> </td> 
   <td> 从其XPath和字段数据提取XML字段的值<br /> </td> 
   <td> NodeValue （&lt;字符串&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Replace</strong><br /> </td> 
   <td> 将指定字符串值的所有匹配项替换为其他字符串值。<br /> </td> 
   <td> Replace（&lt;字符串&gt;，&lt;字符串&gt;，&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Right</strong><br /> </td> 
   <td> 返回字符串的最后 n 个字符<br /> </td> 
   <td> Right(&lt;字符串&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> 返回右侧的已完成字符串<br /> </td> 
   <td> RPad（&lt;字符串&gt;， &lt;数字&gt;， &lt;字符&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> 删除字符串右侧的空格<br /> </td> 
   <td> Rtrim(&lt;字符串&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> 字符串的SHA256键的十六进制表示形式。<br /> </td> 
   <td> Sha256Digest （&lt;字符串&gt;）<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> 字符串的SHA512键的十六进制表示形式。<br /> </td> 
   <td> Sha512Digest （&lt;字符串&gt;）<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Smart</strong><br /> </td> 
   <td> 以大写方式返回带每个单词的第一个字母的字符串<br /> </td> 
   <td> Smart(&lt;字符串&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Substring</strong><br /> </td> 
   <td> 提取从字符串的字符n1开始的、长度为n2<br />的子字符串 </td> 
   <td> Substring(&lt;字符串&gt;, &lt;偏移&gt;, &lt;长度&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> 将数字转换为字符串<br /> </td> 
   <td> ToString（&lt;数字&gt;， &lt;数字&gt;）<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Upper</strong><br /> </td> 
   <td> 返回以大写表示的字符串<br /> </td> 
   <td> Upper(&lt;字符串&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> 如果其他两个参数相等，则返回作为参数传递的链接的外键<br /> </td> 
   <td> VirtualLink(&lt;数字&gt;, &lt;数字&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> 如果其他两个参数相等，则返回作为参数传递的链接的外键（文本）<br /> </td> 
   <td> VirtualLinkStr(&lt;字符串&gt;, &lt;数字&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 窗口

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名称</strong><br /> </td> 
   <td> <strong>描述</strong><br /> </td> 
   <td> <strong>语法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>_超过__</strong><br /> </td> 
   <td> 执行作为第1参数输入的SQL函数调用，通过Partition或Order By作为第2参数<br />输入的字段 </td> 
   <td> 超过_ （&lt;值&gt;， &lt;值&gt;）<br />(_Over_) </td>  
  </tr> 
  <tr> 
   <td> <strong>Desc</strong><br /> </td> 
   <td> 应用降序排序<br /> </td> 
   <td> Desc(&lt;值 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> 对分区中的结果进行排序<br /> </td> 
   <td> OrderBy(&lt;值 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> 对表格上的查询结果进行分区<br /> </td> 
   <td> PartitionBy(&lt;值 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>RowNum</strong><br /> </td> 
   <td> 根据表分区和排序顺序生成行号。<br /> </td> 
   <td> RowNum(PartitionBy(&lt;值 1&gt;), OrderBy(&lt;值 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>
