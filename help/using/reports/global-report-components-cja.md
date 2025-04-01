---
solution: Journey Optimizer
product: journey optimizer
title: 组件列表
description: 了解如何使用报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: aa060d8e-23e2-4bab-b709-636077eb5d20
source-git-commit: 8feb2e74f4ca3321ba4c96204cbdd2343a4ba92b
workflow-type: tm+mt
source-wordcount: '1362'
ht-degree: 1%

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
<td>历程参与</td> 
<td>接收通过历程发送的消息的独特个人的总数，表示到达历程中指定操作点的不同用户档案。</td> 
</tr> 
<tr> 
<td>历程进入</td> 
<td>到达历程的进入事件的个人总数。</td> 
</tr>
<tr> 
<td>历程退出</td> 
<td>退出历程的个人总数。</td> 
</tr>
<tr> 
<td>历程失败</td> 
<td>未成功执行的单个历程的总数。</td> 
</tr>
<tr> 
<td>独特的历程进入</td> 
<td>到达历程的进入事件的个人总数，同一用户档案的多次交互不考虑在内。</td> 
</tr>
<tr> 
<td>独特历程退出</td> 
<td>已退出旅程的个人总数，其中未考虑同一用户档案的多次交互。</td> 
</tr>
<tr> 
<td>独特历程失败次数</td> 
<td>未成功执行、未考虑同一用户档案的多个交互的单个历程总数。</td> 
</tr>
 </tbody> 
</table>

## 电子邮件量度 {#email-metrics}

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
   <td> 发送进程和自动返回处理期间累计的错误总数与已发送消息的总数之比。<br/> </td> 
  </tr> 
  <tr> 
   <td> 点进打开率(CTOR)<br/> </td> 
   <td> 电子邮件的打开次数。<br/> </td> 
  </tr>
  <tr> 
   <td> 点进率(CTR)<br/> </td> 
   <td> 与电子邮件交互的用户百分比。<br/> </td> 
  </tr>
  <tr> 
   <td> 点击次数<br/> </td> 
   <td> 在电子邮件中点击内容的次数。<br/> </td> 
  </tr> 
  <tr> 
   <td> 已投放<br/> </td> 
   <td> 成功发送的消息数，与已发送消息的总数相关。<br/></td> 
  </tr> 
  <tr> 
   <td> 投放率<br/> </td> 
   <td> 成功发送的邮件百分比。<br/> </td> 
  </tr>
  <tr> 
   <td> 错误原因<br/> </td> 
   <td> 导致该错误的特定原始原因的名称。 <a href="exclusion-list.md">了解有关错误原因的更多信息</a>。<br/> </td> 
  </tr>
  <tr> 
   <td> 优惠点击率<br/> </td> 
   <td> 与优惠交互的用户百分比。<br/> </td> 
  </tr>
  <tr> 
   <td> 优惠展示率<br/> </td> 
   <td> 与已发送优惠数量相比已打开优惠的百分比。<br/> </td> 
  </tr>
  <tr> 
   <td> 选件名称<br/> </td> 
   <td> 在投放中添加的优惠的名称。 有关版面的详细信息，请参阅此<a href="../offers/offer-library/creating-personalized-offers.md">页面</a>.<br/> </td> 
  </tr>
  <tr> 
   <td> 已发送优惠<br/> </td> 
   <td> 优惠的发送总数。<br/> </td> 
  </tr> 
  <tr> 
   <td> 打开<br/> </td> 
   <td> 消息的打开次数。<br/> </td> 
  </tr> 
  <tr> 
   <td> 出站错误<br/> </td> 
   <td> 发送过程中发生的错误总数，导致无法将其发送到配置文件。<br/> </td> 
  </tr> 
  <tr> 
   <td> 出站排除项<br/> </td> 
   <td> Adobe Journey Optimizer已排除的配置文件数。<br/> </td> 
  </tr>
  <tr> 
   <td> 投放位置名称<br/> </td> 
   <td> 用于显示优惠的投放位置名称。 有关版面的详细信息，请参阅此<a href="../offers/offer-library/creating-placements.md">页面</a>。 </td> 
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
   <td> 单击电子邮件中内容的用户档案数。<br>请注意，在计算唯一点击时，将考虑过去10天。 如果用户档案在10天内注册了多次点击，则都将计为唯一点击。 但是，如果某个用户档案相隔10天以上，有2次点击，则不会被视为唯一点击。<br/> </td> 
  </tr>
  <tr> 
   <td> 独特电子邮件取消订阅<br/> </td> 
   <td> 取消订阅您电子邮件的用户档案数。<br/> </td> 
  </tr>
  <tr> 
   <td> 唯一打开次数<br/> </td> 
   <td> 打开投放的用户档案数。 <br>请注意，在计算唯一打开次数时，将考虑过去10天。 如果某用户档案在10天内注册了多次打开，则将被计为唯一打开。 但是，如果某个用户档案有2个打开且间隔超过10天，则这些打开将不会被视为唯一打开。<br/> </td> 
  </tr> 
  <tr> 
   <td> 取消订阅<br/> </td> 
   <td> 取消订阅链接的点击次数。<br/> </td> 
  </tr> 
 </tbody> 
</table>

## 短信量度

<table> 
  <thead> 
    <tr> 
      <th> 短信量度 </th> 
      <th> 定义 </th> 
    </tr>
  </thead> 
  <tbody> 
    <tr> 
      <td>已送达</td> 
      <td>成功发送的短信消息数，与短信消息总数相关。</td> 
    </tr>
    <tr> 
      <td>点击次数</td> 
      <td>短信消息中链接的点击次数。</td> 
    </tr>
    <tr> 
      <td>出站SMS消息的退回</td> 
      <td>在发送过程和自动返回处理过程中累积的错误总数，与已发送短信消息的总数相关。</td> 
    </tr>
    <tr> 
      <td>出站短信错误</td> 
      <td>发生的错误总数，阻止将短信消息发送给收件人。</td> 
    </tr>
    <tr> 
      <td>出站短信排除</td> 
      <td>Adobe Journey Optimizer不接收短信消息的用户档案数。</td> 
    </tr>
    <tr> 
      <td>独特点击</td> 
      <td>点击短信消息中链接的独特收件人数量。</td> 
    </tr>
    <tr> 
      <td>显示数</td> 
      <td>短信消息显示或打开的次数。</td> 
    </tr>
    <tr> 
      <td>独特显示区</td> 
      <td>打开短信消息的独特收件人数量，不包括来自同一用户的多个交互。</td> 
    </tr>
    <tr> 
      <td>人员</td> 
      <td>接收短信消息或与短信消息交互的独特用户配置文件数。</td> 
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
   <td>Number of profiles who opened the email.<br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td>Number of profiles who clicked on the unsubscription link.<br/> </td>
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

## 应用程序内指标 {#inapp-metrics}
<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定义<br/> </th> 
  </tr>
 </thead> 
 <tbody>
  <tr> 
   <td>点击次数<br/> </td> 
   <td>与应用程序内消息中包含的按钮交互的配置文件总数。<br/> </td> 
  </tr>
  <tr> 
   <td>点击率<br/> </td> 
   <td>与应用程序内消息中包含的按钮进行交互的用户与看到该消息的用户相比的百分比。<br/> </td> 
  </tr>
  <tr> 
   <td>解除率<br/> </td> 
   <td>配置文件已解除的应用程序内消息的百分比。<br/> </td> 
  </tr>
  <tr> 
   <td>展示次数<br/> </td> 
   <td>传递给所有用户的应用程序内消息总数。<br/> </td>
  </tr>
  <tr> 
   <td>独特展示次数<br/> </td> 
   <td>向其传递应用程序内消息的独特用户数。<br/> </td>
  </tr>
  <tr> 
   <td>显示<br/> </td>
   <td>应用程序内消息的打开次数。<br/> </td>
  </tr>
  <tr> 
   <td>独特显示<br/> </td>
   <td>应用程序内消息的打开次数，不包括来自同一配置文件的多个交互。<br/> </td>
  </tr>
  <tr> 
   <td>独特点击<br/> </td>
   <td>点击应用程序内消息中内容的配置文件数。<br/> </td>
  </tr>
  <tr> 
   <td>点击次数<br/> </td>
   <td>在您的应用程序内消息中点击内容的次数。<br/> </td>
  </tr>
  <tr> 
   <td>点进率(CTR)<br/> </td>
   <td>与应用程序内消息交互的用户百分比。<br/> </td>
  </tr>
  <tr> 
   <td>点进打开率(CTOR)<br/> </td>
   <td>应用程序内消息的打开次数。<br/> </td>
  </tr>
  <tr> 
   <td>发送<br/> </td>
   <td>已发送的应用内消息总数。<br/> </td>
  </tr>
  <tr> 
   <td>入站已触发<br/> </td>
   <td>用户交互或预定义事件触发应用程序内消息的次数。<br/> </td>
  </tr>
  <tr> 
   <td>入站消除<br/> </td>
   <td>用户在不与应用程序内消息交互的情况下解除该消息的次数。<br/> </td>
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
   <td> 对已传递的推送通知执行的总操作数，例如按钮点击或解除。<br/> </td> 
</tr>
  <tr> 
   <td>退回<br/> </td> 
   <td> 传递和自动返回处理期间累计的错误总数与已发送消息的总数之比。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 退回的推送通知与已发送的推送通知相比的百分比。<br/> </td>
</tr>
  <tr> 
   <td> 已投放<br/> </td> 
   <td> 成功发送的邮件数，与已发送的邮件总数相关。<br/> </td> 
</tr> 
  <tr> 
   <td> 投放率<br/> </td> 
   <td> 已成功发送推送通知的百分比。<br/> </td> 
</tr>
  <tr> 
   <td>预订<br/> </td> 
   <td> 此推送通知的打开和操作总数，即如果用户档案打开了推送或单击了按钮。<br/> </td> 
</tr> 
  <tr> 
   <td> 参与率<br/> </td> 
   <td> 此推送通知的打开和操作百分比，即如果用户档案打开了推送或单击了按钮。<br/> </td> 
</tr>
  <tr> 
   <td> 错误<br/> </td> 
   <td> 传递期间发生的阻止将其发送到用户档案的错误总数。<br/> </td> 
</tr>
  <tr> 
   <td> 错误率<br/> </td> 
   <td> 与发送的推送通知相比，在投放期间发生阻止发送该投放的错误百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 错误原因<br/> </td> 
   <td> 导致该错误的特定原始原因的名称。 <a href="exclusion-list.md">了解有关错误原因的更多信息</a>。<br/> </td> 
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
   <td> 打开率<br/> </td> 
   <td> 已打开推送通知的百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 推送自定义操作<br/> </td> 
   <td>用户档案为响应推送通知而采取的自定义操作数。<br/> </td> 
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
   <td>跳出率<br/> </td> 
   <td>未与登陆页面交互且未完成订阅操作的人员数量，与访问总数相关。<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>点击次数<br/> </td> 
   <td>在登陆页面中点击内容的次数。<br/> </td> 
</tr>
 <tr> 
   <td>点击率<br/> </td> 
   <td>登陆页面中的点击百分比。<br/> </td>
</tr>
<tr>
<td>转换<br/> </td> 
   <td>与登陆页面交互（例如订阅了表单）的人数。<br/> </td> 
</tr>
<tr>
   <td>转化率<br/> </td> 
   <td>与登陆页面交互（例如订阅了表单）的人员数，与访问总数相关。<br/> </td> 
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
   <td> 来自历程和外部源的登陆页面访问总数，包括一个用户档案的多次访问。<br/> </td> 
</tr>
 <tr> 
   <td>独特访客<br/> </td> 
   <td>访问您的登陆页面的人员数量，一个配置文件的多次访问未被考虑在内。<br/> </td> 
</tr>
 <tr> 
   <td>访问<br/> </td> 
   <td>对登陆页面的访问次数，包括一个配置文件的多次访问。<br/> </td> 
</tr>
 </tbody> 
</table>
