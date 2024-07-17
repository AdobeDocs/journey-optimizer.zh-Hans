---
solution: Journey Optimizer
product: journey optimizer
title: 组件列表
description: 了解如何使用实时报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 12168cdf-f517-49b5-958b-ba689ade6982
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# 组件列表 {#list-of-components-live}

下表列出了报表中使用的量度及其定义，具体取决于投放类型。

## 历程指标 {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定义<br/> </th> 
</tr>
 </thead> 
 <tbody> 
  <tr> 
   <td>已成功执行操作<br/> </td> 
   <td> 为历程成功执行的操作总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 输入的配置文件<br/> </td> 
   <td> 到达历程进入事件的个人总数。<br/> </td> 
</tr>
  <tr> 
   <td> 操作<br/>出错 </td> 
   <td>操作发生的错误总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 退出的配置文件<br/> </td> 
   <td> 退出历程的个人总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 失败的单个历程<br/> </td> 
   <td> 未成功执行的个别历程总数。<br/> </td> 
</tr> 
 </tbody> 
</table>

## 电子邮件和短信维度和量度 {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定义<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td> 退回<br/> </td> 
   <td> 传递和自动返回处理期间累计的错误总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 与发送的电子邮件相比退回的电子邮件百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 点击次数<br/> </td> 
   <td> 在电子邮件中点击内容的次数。<br/> </td> 
</tr> 
  <tr> 
   <td> 已投放<br/> </td> 
   <td> 成功发送的消息数。<br/></td> 
</tr> 
  <tr> 
   <td> 投放率<br/> </td> 
   <td> 成功发送的邮件百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 错误<br/> </td> 
   <td> 传递期间发生的阻止将其发送到用户档案的错误总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 错误率<br/> </td> 
   <td> 与发送的电子邮件相比，在投放期间发生阻止发送该投放的错误百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 已排除<br/> </td> 
   <td> Adobe Journey Optimizer已排除的配置文件数。<br/> </td> 
</tr>
  <tr> 
   <td> 硬退回<br/> </td> 
   <td> 永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，如“未知用户”。<br/> </td>
</tr>
  <tr> 
   <td> 已忽略<br/> </td> 
   <td> 临时总数，例如“不在办公室”或技术错误，例如，如果发件人类型为postmaster。<br/> </td> 
</tr>
   <tr> 
   <td>优惠点击率<br/> </td> 
   <td>与优惠交互的用户百分比。<br/> </td> 
</tr>
   <tr> 
   <td>优惠展示率<br/> </td> 
   <td>与已发送优惠数量相比已打开优惠的百分比。<br/> </td> 
</tr>
   <tr> 
   <td>选件名称<br/> </td> 
   <td> 在投放中添加的优惠的名称。 有关版面的详细信息，请参阅此<a href="../offers/offer-library/creating-personalized-offers.md">页面</a>.<br/> </td> 
</tr>
   <tr> 
   <td>已发送优惠<br/> </td> 
   <td>优惠的发送总数。<br/> </td> 
</tr> 
  <tr>
   <td>打开<br/> </td> 
   <td> 消息的打开次数。<br/> </td> 
</tr> 
  <tr> 
   <td> 打开率<br/> </td> 
   <td> 已打开的电子邮件总数与已传递的电子邮件数之比。<br/> </td> 
</tr>
  <tr> 
   <td>投放位置名称<br/> </td> 
   <td> 用于显示优惠的投放位置名称。 有关版面的详细信息，请参阅此<a href="../offers/offer-library/creating-placements.md">页面</a>。 </td> 
</tr> 
  <tr> 
   <td> 重试<br/> </td> 
   <td> 重试队列中的电子邮件数。<br/> </td> 
</tr> 
  <tr> 
   <td> 已发送<br/> </td> 
   <td> 投放的发送总数。<br/> </td> 
</tr>
  <tr> 
   <td> 软退回<br/> </td> 
   <td> 临时错误总数，如收件箱已满。<br/> </td> 
</tr>
  <tr> 
   <td> 垃圾邮件投诉次数<br/> </td> 
   <td> 将邮件声明为垃圾邮件或垃圾邮件的次数。<br/> </td> 
</tr>
  <tr> 
   <td> 目标<br/> </td> 
   <td> 传递分析期间处理的邮件总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 独特点击<br/> </td> 
   <td> 点击电子邮件中内容的收件人数量。<br/> </td> 
</tr> 
  <tr> 
   <td>独特点击率<br/> </td> 
   <td> 与投放交互的用户百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 唯一打开次数<br/> </td> 
   <td>打开投放的收件人数量。<br/> </td> 
</tr> 
  <tr> 
   <td> 取消订阅<br/> </td> 
   <td> 取消订阅链接的点击次数。<br/> </td> 
</tr> 
 </tbody> 
</table>

## 登陆页面量度 {#landing-page-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定义<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
  <td>退回<br/> </td> 
   <td>未与登陆页面交互且未完成订阅操作的人数。<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>点击次数<br/> </td> 
   <td>在登陆页面中点击内容的次数。<br/> </td> 
</tr>
<tr>
<td>转换<br/> </td> 
   <td>与登陆页面交互（例如订阅了表单）的人数。<br/> </td> 
</tr>
 <tr> 
   <td>历程<br/> </td> 
   <td>来自历程的登陆页面访问次数。<br/> </td> 
</tr>
 <tr> 
   <td>其他源<br/> </td> 
   <td>来自外部源而非历程对登陆页面的访问次数。<br/> </td> 
</tr>
 <tr> 
   <td>总访问次数<br/> </td> 
   <td> 来自历程和外部来源对登陆页面的访问总数，包括一个收件人的多次访问。<br/> </td> 
</tr>
 <tr> 
   <td>独特访客<br/> </td> 
   <td>访问您的登陆页面的人员数量，不考虑一位收件人的多次访问。<br/> </td> 
</tr>
 <tr> 
   <td>访问<br/> </td> 
   <td>对登陆页面的访问次数，包括一个收件人的多次访问。<br/> </td> 
</tr>
 </tbody> 
</table>

## 推送通知量度 {#push-notification-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定义<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>操作<br/> </td> 
   <td> 对已传递的推送通知执行的总操作数，例如按钮点击或解除。<br/> </td> 
</tr>
  <tr> 
   <td>退回<br/> </td> 
   <td> 传递和自动返回处理期间累计的错误总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 已投放<br/> </td> 
   <td> 成功发送的邮件数。<br/> </td> 
</tr> 
  <tr> 
   <td>预订<br/> </td> 
   <td> 此推送通知的打开和操作总数，即如果用户档案打开了推送或单击了按钮。<br/> </td> 
</tr> 
  <tr> 
   <td> 错误<br/> </td> 
   <td> 传递期间发生的阻止将其发送到用户档案的错误总数。<br/> </td> 
</tr>
  <tr> 
   <td> 已排除<br/> </td> 
   <td> Adobe Journey Optimizer已排除的配置文件数。<br/> </td> 
</tr>
  <tr> 
   <td> 打开<br/> </td> 
   <td> 发送到设备并由用户单击从而打开应用程序的推送通知总数。 这与推送点击类似，不同之处在于，如果取消通知，则不会触发推送打开。<br/> </td> 
</tr> 
  <tr> 
   <td> 已发送<br/> </td> 
   <td> 投放的发送总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 目标<br/> </td> 
   <td> 投放分析期间处理的推送消息总数。<br/> </td> 
</tr>  
 </tbody> 
</table>

<!--
## In-app metrics {#inapp-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Clicks<br/> </td> 
   <td>Total number of recipients who interacted with the buttons included in the In-app message.<br/> </td> 
</tr>
  <tr> 
   <td>Impressions<br/> </td> 
   <td> Total number of In-app messages delivered to all users.<br/> </td>
</tr>
  <tr> 
   <td>Unique impressions<br/> </td> 
   <td>Number of unique users to whom the In-app message was delivered.<br/> </td>
</tr>
 </tbody> 
</table>
-->
