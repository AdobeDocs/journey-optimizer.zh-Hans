---
title: 发行说明
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 4576fbc4f75951e0576787b7631e164a87fdb83d
workflow-type: ht
source-wordcount: '283'
ht-degree: 100%

---

# 发行说明 {#release-notes}

此页面列出了 [!DNL Journey Optimizer] 的所有新增功能和改进。您还可以查阅[最新文档更新](documentation-updates.md)页面以了解更多更改。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target=&quot;_blank&quot;} 中，进一步了解这些变更。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}邮件，每个季度就能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

## 2022 年 8 月版 {#aug-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>在 Journey Optimizer 中创建和管理营销活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用 Journey Optimizer 营销活动通过各种渠道向特定区段投放一次性内容。使用历程时，操作被设计为按顺序执行。 借助营销活动，可同时执行诸多操作：立即执行或根据指定计划执行。 </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>在<a href="../campaigns/get-started-with-campaigns.md">详细文档</a>和<a href="https://video.tv.adobe.com/v/346680">功能介绍视频</a>中了解如何创建营销活动。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>向用户发送短信（一般情况可用）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，通过与 <b>Sinch</b> 或 <b>Twilio</b> 集成，您可以在 Journey Optimizer 中创建、个性化和发送短信。</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>在此<a href="../messages/create-sms.md">详细文档</a>中了解如何创建和发送短信。</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->



### 改进

**报告**

* 历程全局报告中现在提供同意策略表和图表。利用这些小组件，可跟踪在自定义操作中从策略排除的用户档案。[了解详情](../reports/journey-global-report.md#journey-global)

   要访问最新的小组件，请注意，您必须重置不同的报告仪表板。有关仪表板自定义的更多信息，请参阅[详细文档](../reports/global-report.md)。

**管理**

* 现在，可以更新用于短信渠道的主电话号码。[了解详情](../configuration/primary-email-addresses.md)