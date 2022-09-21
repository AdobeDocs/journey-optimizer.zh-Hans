---
title: 全局报告
description: 了解如何使用全局报表中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: aecbf0f8bcfb8f6747ee072d891029a38f8f2ed1
workflow-type: tm+mt
source-wordcount: '1201'
ht-degree: 3%

---

# 全局报告入门 {#global-report}

>[!NOTE]
>
> 如果在使用查询服务时通过API进行自定义查询，则报表可能会出现延迟。

使用 **[!UICONTROL 全局报告]** 以测量选定时间段内历程和投放的影响。

* 如果要在历程上下文中定位历程或投放，请从 **[!UICONTROL 历程]** 菜单，访问您的历程并单击 **[!UICONTROL 查看报表]** 按钮。 然后，您可以找到历程、电子邮件、短信和推送全局报表。

   ![](assets/report_journey.png)

* 如果要定位营销活动，请从 **[!UICONTROL 促销活动]** 菜单，访问您的营销活动并单击 **[!UICONTROL 报表]** 按钮。

   ![](assets/report_campaign.png)

* 如果要从 **[!UICONTROL 实时报表]** 到 **[!UICONTROL 全局报告]** 对于投放，单击 **[!UICONTROL 所有时间]** 切换器。

   ![](assets/report_5.png)

有关Adobe Journey Optimizer中可用的每个量度的详细列表，请参阅 [本页](#list-of-components-global)

## 自定义功能板 {#modify-dashboard}

可以通过更改时间段以及调整大小或删除小组件来修改每个报表功能板。 更改小组件仅会影响当前用户的功能板。 其他用户将看到他们自己的功能板或默认设置的功能板。

1. 从全局报表中，选择开始和结束时间以定位特定数据。

   ![](assets/report_modify_1.png)

1. 选择是否要使用切换栏从报表中排除测试事件。 有关测试事件的更多信息，请参阅 [本页](../building-journeys/testing-the-journey.md).

   请注意， **[!UICONTROL 排除测试事件]** 选项仅可用于历程报表。

   ![](assets/report_modify_2.png)

1. 单击 **[!UICONTROL 修改]** 开始自定义功能板。

   ![](assets/report_modify_3.png)

1. 通过拖动小组件的右下角来调整其大小。

   ![](assets/report_modify_4.png)

1. 单击 **[!UICONTROL 删除]** 删除您不需要的任何小组件。

   ![](assets/report_modify_5.png)

1. 当您对小组件的显示顺序和大小感到满意后，单击 **[!UICONTROL 保存]**.

功能板现已保存。 您的不同更改将重新应用，以便日后使用您的实时报表。 如果需要，请使用 **[!UICONTROL 重置]** 用于恢复默认小组件和小组件顺序的选项。

## 组件列表 {#list-of-components-global}

下表提供了报表中使用的量度列表及其定义，具体取决于投放类型。

### 历程量度 {#journey-metrics}

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
   <td> 输入的用户档案<br/> </td> 
   <td> 到达历程的登入事件的个人总数。<br/> </td> 
</tr>
  <tr> 
   <td> 操作错误<br/> </td> 
   <td>操作发生的错误总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 退出用户档案<br/> </td> 
   <td> 退出历程的个人总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 失败的单个历程<br/> </td> 
   <td> 未成功执行的各个历程的总数。<br/> </td> 
</tr> 
 </tbody> 
</table>

### 电子邮件和短信量度 {#email-and-sms-metrics}

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
   <td> 在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 退回的电子邮件与发送的电子邮件的百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 单击次数<br/> </td> 
   <td> 电子邮件中内容的点击次数。<br/> </td> 
</tr> 
  <tr> 
   <td> 已送达 <br/> </td> 
   <td> 已成功发送的消息数，与已发送消息的总数有关。<br/></td> 
</tr> 
  <tr> 
   <td> 投放率<br/> </td> 
   <td> 成功发送的消息的百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 错误<br/> </td> 
   <td> 投放期间发生的阻止将其发送到用户档案的错误总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 错误率<br/> </td> 
   <td> 与发送的电子邮件相比，在阻止发送投放的投放期间发生的错误百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 排除<br/> </td> 
   <td> 已被Adobe Journey Optimizer排除的用户档案数。<br/> </td> 
</tr>
  <tr> 
   <td> 硬退回<br/> </td> 
   <td> 永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，如未知用户。<br/> </td>
</tr>
  <tr> 
   <td> 已忽略<br/> </td> 
   <td> 临时（如“不在办公室”）或技术错误（例如，如果发件人类型为邮递员）的总数。<br/> </td> 
</tr>
   <tr> 
   <td>选件点击率<br/> </td> 
   <td>与选件进行交互的用户百分比。<br/> </td> 
</tr>
   <tr> 
   <td>优惠展示率<br/> </td> 
   <td>已打开选件与已发送选件数的百分比。<br/> </td> 
</tr>
   <tr> 
   <td>选件名称<br/> </td> 
   <td> 在投放中添加的选件的名称。 有关版面的更多信息，请参阅 <a href="../offers/offer-library/creating-personalized-offers.md">页面</a>.<br/> </td> 
</tr>
   <tr> 
   <td>已发送选件<br/> </td> 
   <td>选件的发送总数。<br/> </td> 
</tr> 
  <tr>
   <td>打开<br/> </td> 
   <td> 消息的打开次数。<br/> </td> 
</tr> 
  <tr> 
   <td> 打开率<br/> </td> 
   <td> 已打开的电子邮件总数与已投放电子邮件的数量相比较。<br/> </td> 
</tr>
  <tr> 
   <td>版面名称<br/> </td> 
   <td> 用于显示选件的版面名称。 有关版面的更多信息，请参阅 <a href="../offers/offer-library/creating-placements.md">页面</a>. </td> 
</tr> 
  <tr> 
   <td> 重试<br/> </td> 
   <td> 队列中要重试的电子邮件数量。<br/> </td> 
</tr> 
  <tr> 
   <td> 已发送<br/> </td> 
   <td> 投放的发送总数。<br/> </td> 
</tr>
  <tr> 
   <td> 软退回<br/> </td> 
   <td> 临时错误（如完整收件箱）的总数。<br/> </td> 
</tr>
  <tr> 
   <td> 垃圾邮件投诉<br/> </td> 
   <td> 将消息声明为垃圾邮件或垃圾邮件的次数。<br/> </td> 
</tr>
  <tr> 
   <td> 目标<br/> </td> 
   <td> 在投放分析期间处理的消息总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 唯一点击次数<br/> </td> 
   <td> 单击电子邮件中内容的收件人数量。<br/> </td> 
</tr> 
  <tr> 
   <td>独特点击率<br/> </td> 
   <td> 与投放进行交互的用户百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 唯一打开次数<br/> </td> 
   <td>打开投放的收件人数。<br/> </td> 
</tr> 
  <tr> 
   <td> 取消订阅<br/> </td> 
   <td> 退订链接的点击次数。<br/> </td> 
</tr> 
 </tbody> 
</table>

<!--
### Experimentation metrics {#experimentation-metrics}
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
   <td>.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td><br/> </td> 
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
   <td><br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td><br/> </td>
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

### 推送通知量度 {#push-notification-metrics}

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
   <td> 已送达推送通知的操作总数，例如按钮单击或解除。<br/> </td> 
</tr>
  <tr> 
   <td>退信数<br/> </td> 
   <td> 在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 与发送的推送通知相比，已退回的推送通知的百分比。<br/> </td>
</tr>
  <tr> 
   <td> 已送达<br/> </td> 
   <td> 已成功发送的消息数，与已发送消息的总数有关。<br/> </td> 
</tr> 
  <tr> 
   <td> 投放率<br/> </td> 
   <td> 成功发送推送通知的百分比。<br/> </td> 
</tr>
  <tr> 
   <td>参与<br/> </td> 
   <td> 此推送通知的打开和操作总数，例如用户档案打开推送或单击按钮时。<br/> </td> 
</tr> 
  <tr> 
   <td> 参与率<br/> </td> 
   <td> 此推送通知的打开次数和操作的百分比，例如用户档案打开了推送或单击了按钮。<br/> </td> 
</tr>
  <tr> 
   <td> 错误<br/> </td> 
   <td> 投放期间发生的阻止将其发送到用户档案的错误总数。<br/> </td> 
</tr>
  <tr> 
   <td> 错误率<br/> </td> 
   <td> 与发送的推送通知相比，在阻止发送投放的投放期间发生的错误百分比。<br/> </td> 
</tr> 
  <tr> 
   <td> 排除<br/> </td> 
   <td> 已被Adobe Journey Optimizer排除的用户档案数。<br/> </td> 
</tr>
  <tr> 
   <td> 打开<br/> </td> 
   <td> 用户交付到设备并点击的推送通知总数，从而打开应用程序。 这类似于推送点击，除非取消通知后不会触发推送打开。<br/> </td> 
</tr> 
  <tr> 
   <td> 打开率<br/> </td> 
   <td> 打开的推送通知的百分比。<br/> </td> 
</tr> 
  <tr> 
   <td> 已发送<br/> </td> 
   <td> 投放的发送总数。<br/> </td> 
</tr> 
  <tr> 
   <td> 目标<br/> </td> 
   <td> 在投放分析期间处理的推送消息总数。<br/> </td> 
</tr>  
 </tbody> 
</table>

### 登陆页面量度 {#landing-page-metrics}

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
   <td>未与登陆页面进行交互且未完成订阅操作的人员数。<br/> </td> 
</tr>
 <tr> 
   <td>跳出率<br/> </td> 
   <td>与访问总数相比，未与登陆页面进行交互且未完成订阅操作的人员数。<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>单击次数<br/> </td> 
   <td>内容在登陆页面中的点击次数。<br/> </td> 
</tr>
 <tr> 
   <td>点击率<br/> </td> 
   <td>登陆页面中的点击次数百分比。<br/> </td>
</tr>
<tr>
<td>转化<br/> </td> 
   <td>与登陆页面进行交互（例如订阅了表单）的人数。<br/> </td> 
</tr>
<tr>
   <td>转化率<br/> </td> 
   <td>与登陆页面进行交互（例如，订阅表单）的人数与访问总数相关。<br/> </td> 
</tr>
 <tr> 
   <td>历程<br/> </td> 
   <td>历程对登陆页面的访问次数。<br/> </td> 
</tr>
 <tr> 
   <td>其他来源<br/> </td> 
   <td>来自外部源而非历程的登陆页面访问次数。<br/> </td> 
</tr>
 <tr> 
   <td>总访问量<br/> </td> 
   <td> 来自历程和外部源对您登陆页面的访问总数，包括一个收件人的多次访问。<br/> </td> 
</tr>
 <tr> 
   <td>独特访客<br/> </td> 
   <td>访问您的登陆页面的人数，则不会考虑一个收件人的多次访问。<br/> </td> 
</tr>
 <tr> 
   <td>访问次数<br/> </td> 
   <td>登陆页面的访问次数，包括一个收件人的多次访问。<br/> </td> 
</tr>
 </tbody> 
</table>

