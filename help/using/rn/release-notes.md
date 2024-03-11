---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: dd47299b780dfe388632b0bad5d587606ece0b23
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 71%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

## 2024 年 2 月发行说明 {#feb-2024}

**发行日期**：2024 年 2 月 21-22 日

### 新功能{#feb-features}

此版本引入了下方列出的新功能。


<table>
<thead>
<tr>
<th><strong>Web 应用程序内消息传送</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用新的 Web 应用程序内消息传送功能，通过模式叠加消息直接在网站上显示个性化内容。此功能使您能够有效地与 Web 访客互动，提升用户交互水平、保留率和转化率。<br/><br/></p>
<p>有关更多信息，请参阅<a href="../in-app/create-in-app-web.md">详细文档</a>。<br></br></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>多渠道内容模板</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了电子邮件之外，内容模板现在还可用于以下渠道：推送、应用程序内、短信和直邮，每个渠道都具有专用的模板类型。 对于电子邮件，您现在可以选择内容类型，这允许您保存主题行作为电子邮件模板的一部分。 <br/><br/></p>
<p>有关更多信息，请参阅<a href="../content-management/content-templates.md">详细文档</a>。<br></br></p>
<img src="assets/do-not-localize/multi-chan-templates.gif">
</tr>
</tbody>
</table>


### 改进 {#feb-improvements}

此版本包含下方列出的改进。

**受众**

* **种子列表** - 现在使用&#x200B;**种子列表**&#x200B;时支持变体。种子地址接收同一消息的所有变体的副本（例如对内容实验的不同处理）。 [了解详情](../configuration/seed-lists.md)

以前作为 Beta 版提供，现在所有用户都可以使用以下改进功能：

* 您现在可以定位&#x200B;**通过受众组合创建的受众**，并利用历程中的扩充属性。[了解详情](../building-journeys/read-audience.md)

* 您现在可以将&#x200B;**从 CSV 文件上传的受众**&#x200B;定位到历程和营销活动中。[了解详情](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* 当前，无法将受众组合和自定义上传（CSV 文件）中的受众和属性用于 Healthcare Shield 或 Privacy and Security Shield。
  >* 此 **从CSV文件上传受众** 在首次发布后的几天内正在逐步推出改进。 虽然某些用户可以立即访问，但其他用户在环境中使用它之前可能会遇到延迟。

**历程**

* **筛选您的历程** - 您现在可以使用&#x200B;**自定义日期筛选历程**&#x200B;库存，以及现有的预定义日期筛选器。这允许您细化列表，显示在特定日期、特定月份、整个年份或指定时间范围内创建或发布的历程。 [了解详情](../building-journeys/journey-gs.md#filter)
* **自定义操作**  — 您现在可以更新 **content-type** 标题。 此新 **content-type** 应引用JSON内容。 [了解详情](../action/about-custom-action-configuration.md#url-configuration)
* **配置** - stepEvents 中的 identityMap 属性现在会预填充。主标识被定义为“primary = true”。 [了解详情](../reports/sharing-field-list.md)
* **用户界面** - 历程屏幕中的顶部栏已重新组织，以改善体验。在不同的更新中，请注意允许您访问历程属性的“铅笔”图标现在显示在顶部栏的左侧，位于历程名称的旁边。 [了解详情](../building-journeys/journey-gs.md#change-properties)

**短信渠道**

* **选择启用/选择禁用关键词** - 配置短信渠道时，您现在可以根据自己的喜好，自定义&#x200B;**选择启用和选择禁用关键词**。Journey Optimizer会根据这些指定的关键词触发响应。 [了解详情](../sms/sms-configuration.md#create-api)

**营销活动**

* **API 触发的营销活动** - 对激活 API 触发的营销活动后生成的 cURL 代码进行了增强。它现在包含消息中使用的所有个性化（用户档案和上下文）变量。 [了解详情](../campaigns/api-triggered-campaigns.md#execute)

**频率规则**

* 除了电子邮件和推送之外，您现在还可以为短信和直邮渠道创建频率规则。 当达到频率上限时，频率规则会自动从消息和操作中排除过度请求的用户档案。 [了解详情](../configuration/frequency-rules.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->

<!--
**Content templates**

* **Thumbnails** - A **Grid view** is now available for content templates for improved visual access.

   >[!AVAILABILITY]
   >
   >This capability is released in Limited Availability (LA) for a small set of customers.
-->


## 2024 年 1 月发行说明 {#jan-2024}

**发行日期**：2024 年 1 月 30-31 日

### 新功能{#jan24-features}

此版本引入了下方列出的新功能。

<table>
<thead>
<tr>
<th><strong>可传递性更新</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 现在支持 DMARC 身份验证技术。</p>
<p>从 2024 年 2 月 1 日开始，Google 和 Yahoo!都会要求您为用于向它们发送电子邮件的任何域设置 DMARC 记录。确保您已在 Journey Optimizer 中为您已委派或正在委派给 Adobe 的所有子域设置了 DMARC 记录。</p>
<p>有关更多信息，请参阅<a href="../configuration/dmarc-record-update.md">详细文档</a>。</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>用例战术手册</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>利用Real-Time CDP和Journey Optimizer中特定于行业的用例行动手册目录，解决您可以使用Adobe Experience Platform和Adobe Journey Optimizer执行的常见用例。</p><p>选择最符合您需求的战术手册后，就可以启用该战术手册以生成支持用例所需的资产（如历程、消息、架构或区段），并根据您的架构对其进行自定义以更快地实现价值。</p>
<p>有关更多信息，请参阅<a href="../start/playbooks.md">详细文档</a>。</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### 改进 {#jan24-improvements}

此版本包含下方列出的改进。

**报告**

* **新的基于域的细分构件** - 添加了新构件，用于增强营销活动和历程报告。**按域列出的退回原因**、**按域列出的已发送和已投放数**、**按域列出的打开数和点击数**&#x200B;以及&#x200B;**按域列出的退回和错误**&#x200B;构件可在域级别提供关键电子邮件投放和跟踪指标的详细细分。[了解详情](../reports/channel-report.md)

**短信渠道**

* **双重选择加入** - 短信的双重选择加入工作流程可确保用户在从其设备发起请求时，明确选择加入以接收消息。用户通过发送入站短信消息启动同意流程。确认同意后，将发送后续消息，请求进行最终验证。如果用户配置文件不存在，则会在确认成功时创建该配置文件。[了解详情](../sms/sms-configuration.md#create-api)

  请注意，此功能适用于 Sinch 和 Infobip 短信提供商。

**历程**

* **反应事件持续时间** - 现在，您可以定义的最长&#x200B;**反应事件**&#x200B;持续时间为 29 天，而不是 30 天。[了解详情](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **读取受众** - 现在，**读取受众**&#x200B;活动依赖于批量区段的配置文件快照数据集，该数据集仅在计划的每日批量作业运行后每天生成一次，因此数据将刷新到上一次每日批量作业。[了解详情](../building-journeys/read-audience.md)

* **字段组** - 此版本修复了在某些情况下阻止保存字段组的问题。

* 在多个函数中修改了对 `<listObject>` 的支持。

**频率规则**

* **每周频率上限**  — 您现在可以指定每周以及每月发送到客户配置文件的最大消息数。 频率上限基于所选日历周期并在相应时间范围的起始点重置。[了解详情](../configuration/frequency-rules.md#create-new-rule)

  >[!NOTE]
  >
  >每日频率上限也可根据需要提供。 请联系您的Adobe代表。

**决策管理**

* **Edge 的频率上限** - 频率上限计数器现已更新，不到 3 秒即可在 Edge Decisioning API 决策中启用。[了解详情](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
