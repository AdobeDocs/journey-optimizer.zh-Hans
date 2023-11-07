---
solution: Journey Optimizer
product: journey optimizer
title: 组件列表
description: 了解如何使用全局报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: c487bb38-49ce-4238-8e94-8364f994cedd
source-git-commit: 82b8c9032d6c377cb76acce4d5cc45afb0ddd6ba
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 9%

---

# 组件列表 {#list-of-components-global}

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
   <td> 到达历程的进入事件的个人总数。<br/> </td> 
</tr>
  <tr> 
   <td> 操作出错<br/> </td> 
   <td>操作发生的错误总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 退出的配置文件<br/> </td> 
   <td> 退出历程的个人总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 失败的个人历程<br/> </td> 
   <td> 未成功执行的单个历程的总数。<br/> </td> 
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
   <td> 退信数<br/> </td> 
   <td> 投放和自动返回处理期间累积的错误的总数与已发送邮件总数有关。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 退回的电子邮件与发送的电子邮件相比的百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 单击次数<br/> </td> 
   <td> 在电子邮件中点击内容的次数。<br/> </td> 
</tr> 
  <tr> 
   <td> 已送达 <br/> </td> 
   <td> 成功发送的消息数，与已发送消息的总数相关。<br/></td> 
</tr> 
  <tr> 
   <td> 投放率<br/> </td> 
   <td> 成功发送的消息百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 错误<br/> </td> 
   <td> 投放期间发生并阻止将其发送到用户档案的错误总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 错误率<br/> </td> 
   <td> 与已发送电子邮件相比，在投放期间发生并阻止发送该投放的错误百分比。<br/> </td> 
</tr>
</tr> 
  <tr> 
   <td> 错误原因<br/> </td> 
   <td> 导致该错误的特定原始原因的名称。 <a href="error-list.md">了解有关错误原因的更多信息</a>.<br/> </td> 
</tr>
  <tr> 
   <td> 已排除<br/> </td> 
   <td> Adobe Journey Optimizer已排除的用户档案数。<br/> </td> 
</tr>
  <tr> 
   <td> 硬退回<br/> </td> 
   <td> 永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，例如“未知用户”。<br/> </td>
</tr>
  <tr> 
   <td> 已忽略<br/> </td> 
   <td> 临时总数，例如“不在办公室”或技术错误，例如，如果发件人类型为“邮递员”。<br/> </td> 
</tr>
   <tr> 
   <td>优惠点击率<br/> </td> 
   <td>与选件交互的用户百分比。<br/> </td> 
</tr>
   <tr> 
   <td>优惠展示率<br/> </td> 
   <td>与已发送优惠数量相比的已打开优惠的百分比。<br/> </td> 
</tr>
   <tr> 
   <td>选件名称<br/> </td> 
   <td> 在投放中添加的优惠的名称。 有关版面的详细信息，请参阅此 <a href="../offers/offer-library/creating-personalized-offers.md">页面</a>.<br/> </td> 
</tr>
   <tr> 
   <td>已发送优惠<br/> </td> 
   <td>优惠的发送总数。<br/> </td> 
</tr> 
  <tr>
   <td>打开次数<br/> </td> 
   <td> 打开消息的次数。<br/> </td> 
</tr> 
  <tr> 
   <td> 打开率<br/> </td> 
   <td> 打开的电子邮件总数，与已投放的电子邮件数相比。<br/> </td> 
</tr>
  <tr> 
   <td>投放位置名称<br/> </td> 
   <td> 用于显示优惠的投放位置名称。 有关版面的详细信息，请参阅此 <a href="../offers/offer-library/creating-placements.md">页面</a>. </td> 
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
   <td> 已定位<br/> </td> 
   <td> 投放分析期间处理的消息的总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 唯一点击次数<br/> </td> 
   <td> 单击电子邮件中内容的收件人数量。<br> 请注意，在计算唯一点击量时，会考虑过去10天的点击量。 如果用户档案在10天内注册了多次点击，则都将计为唯一点击。 但是，如果某个用户档案相隔10天以上，有2次点击，则不会被视为唯一点击。<br/> </td> 
</tr> 
  <tr> 
   <td>独特点击率<br/> </td> 
   <td> 与投放交互的用户百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 唯一打开次数<br/> </td> 
   <td>打开投放的收件人数量。 <br> 请注意，计算唯一打开次数时，将考虑过去10天。 如果某用户档案在10天内注册了多次打开，则将被计为唯一打开。 但是，如果某个用户档案有2个打开次数，并且间隔超过10天，则这些打开次数不会被视为唯一打开次数。<br/> </td> 
</tr> 
  <tr> 
   <td> 退订次数<br/> </td> 
   <td> 取消订阅链接的点击次数。<br/> </td> 
</tr> 
 </tbody> 
</table>

<!--
## Experimentation metrics {#experimentation-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td>App installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>App launches<br/> </td> 
   <td><br/> </td> 
</tr>
 <tr> 
   <td>Average lift<br/> </td> 
   <td> Percentage improvement in conversion rate of a given treatment over the baseline.<a href="../campaigns/experiment-calculations.md#understand-lift">Learn more</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Confidence<br/> </td> 
   <td>Evidence that a given treatment is the same as the baseline treatment. <a href="../campaigns/experiment-calculations.md#understand-confidence">Learn more</a>.<br/> </td> 
</tr>
  <tr> 
   <td>Confidence interval<br/> </td> 
   <td>Percentage difference in performance between the baseline and the best performing treatment. <a href="../campaigns/experiment-calculations.md#understand-intervals">Learn more</a>.<br/> </td> 
</tr> 
  <tr> 
   <td>Count per profile<br/> </td> 
   <td>Total value of the Experiment objective metric divided by the number of profiles.<br/> </td> 
</tr>
  <tr> 
   <td>Email Opens<br/> </td> 
   <td>Number of times the email was opened.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td>Number of clicks on the unsubscription link.<br/> </td> 
</tr>
  <tr> 
   <td>First app launches<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Outbound Clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Profiles<br/> </td> 
   <td>Number of profiles targeted for this treatment.<br/> </td> 
</tr>
  <tr> 
   <td>Unique email opens<br/> </td> 
   <td>Number of recipients who opened the email.<br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td>Number of recipients who clicked on the unsubscription link.<br/> </td>
</tr>
  <tr> 
   <td>Unique installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique launches<br/> </td> 
   <td><br/> </td> 
</tr> 
  <tr> 
   <td>Unique outbound clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique upgrades<br/> </td> 
   <td><br/> </td> 
</tr>
   <td>Upgrades<br/> </td> 
   <td><br/> </td> 
</tr> 
</tbody> 
</table>
-->

## 应用程序内量度 {#inapp-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定义<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>单击次数<br/> </td> 
   <td>与应用程序内消息中包含的按钮进行交互的收件人总数。<br/> </td> 
</tr>
  <tr> 
   <td>点击率<br/> </td> 
   <td>与应用程序内消息中包含的按钮进行交互的用户与看到该消息的用户相比的百分比。<br/> </td> 
</tr> 
  <tr> 
   <td>消除率<br/> </td> 
   <td> 收件人已解除的应用程序内消息的百分比。<br/> </td> 
</tr> 
  <tr> 
   <td>展示次数<br/> </td> 
   <td> 交付给所有用户的应用程序内消息总数。<br/> </td>
</tr>
  <tr> 
   <td>独特展示次数<br/> </td> 
   <td>向其传递应用程序内消息的独特用户数。<br/> </td>
</tr>
 </tbody> 
</table>

## 推送通知量度

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
   <td> 已投放推送通知上的操作总数，例如按钮点击或解除。<br/> </td> 
</tr>
  <tr> 
   <td>退信数<br/> </td> 
   <td> 投放和自动返回处理期间累积的错误的总数与已发送邮件总数有关。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 退回的推送通知与已发送的推送通知相比的百分比。<br/> </td>
</tr>
  <tr> 
   <td> 已送达<br/> </td> 
   <td> 成功发送的消息数，与已发送消息的总数相关。<br/> </td> 
</tr> 
  <tr> 
   <td> 投放率<br/> </td> 
   <td> 已成功发送的推送通知的百分比。<br/> </td> 
</tr>
  <tr> 
   <td>参与<br/> </td> 
   <td> 此推送通知的打开和操作总数，即用户档案是否已打开推送或者是否单击了按钮。<br/> </td> 
</tr> 
  <tr> 
   <td> 参与率<br/> </td> 
   <td> 此推送通知的打开次数和操作百分比，即用户档案是否已打开推送或是否单击了按钮。<br/> </td> 
</tr>
  <tr> 
   <td> 错误<br/> </td> 
   <td> 投放期间发生并阻止将其发送到用户档案的错误总数。<br/> </td> 
</tr>
  <tr> 
   <td> 错误率<br/> </td> 
   <td> 与发送的推送通知相比，在投放期间发生并阻止发送该投放的错误百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 错误原因<br/> </td> 
   <td> 导致该错误的特定原始原因的名称。 <a href="error-list.md">了解有关错误原因的更多信息</a>.<br/> </td> 
</tr>
  <tr> 
   <td> 已排除<br/> </td> 
   <td> Adobe Journey Optimizer已排除的用户档案数。<br/> </td> 
</tr>
  <tr> 
   <td> 打开次数<br/> </td> 
   <td> 发送到设备并由用户单击从而打开应用程序的推送通知总数。 这与推送点击类似，不同之处在于，如果取消通知，则不会触发推送打开。<br/> </td> 
</tr> 
  <tr> 
   <td> 打开率<br/> </td> 
   <td> 已打开推送通知的百分比。<br/> </td> 
</tr> 
  <tr> 
   <td> 已发送<br/> </td> 
   <td> 投放的发送总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 已定位<br/> </td> 
   <td> 投放分析期间处理的推送消息总数。<br/> </td> 
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
  <td>退信数<br/> </td> 
   <td>未与登陆页面交互且未完成订阅操作的人数。<br/> </td> 
</tr>
 <tr> 
   <td>跳出率<br/> </td> 
   <td>未与登陆页面交互且未完成订阅操作的人数，与访问总数相关。<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>单击次数<br/> </td> 
   <td>在登陆页面中点击内容的次数。<br/> </td> 
</tr>
 <tr> 
   <td>点击率<br/> </td> 
   <td>登陆页面中的点击百分比。<br/> </td>
</tr>
<tr>
<td>转化<br/> </td> 
   <td>与登陆页面交互（例如订阅了表单）的人数。<br/> </td> 
</tr>
<tr>
   <td>转化率<br/> </td> 
   <td>与登陆页面进行交互（例如订阅了表单）的人数，与访问总数相关。<br/> </td> 
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
   <td>访问总数<br/> </td> 
   <td> 来自历程和外部来源对登陆页面的访问总数，包括一个收件人的多次访问。<br/> </td> 
</tr>
 <tr> 
   <td>独特访客<br/> </td> 
   <td>访问您的登陆页面的人员数量，不考虑一位收件人的多次访问。<br/> </td> 
</tr>
 <tr> 
   <td>访问次数<br/> </td> 
   <td>对登陆页面的访问次数，包括一个收件人的多次访问。<br/> </td> 
</tr>
 </tbody> 
</table>
