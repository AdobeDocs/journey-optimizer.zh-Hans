---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 38f85467256b22a6f05fee8137bc76b0d99c4e6e
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 95%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

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
<p>从2024年2月1日开始，Google和Yahoo！ 要求您拥有DMARC记录，以便您向任何域发送电子邮件。 确保您已在 Journey Optimizer 中为您已委派或正在委派给 Adobe 的所有子域设置了 DMARC 记录。</p>
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
<p>利用 Real-Time CDP 和 Journey Optimizer 中特定于行业的用例战术手册目录，解决您可以使用 Adobe Experience Platform 和 Adobe Journey Optimiser 执行的常见用例。</p><p>选择最符合您需求的战术手册后，就可以启用该战术手册以生成支持用例所需的资产（如历程、消息、架构或区段），并根据您的架构对其进行自定义以更快地实现价值。</p>
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

* **每周和每日频率上限** - 现在，除了可以指定一个月内向客户配置文件发送的最大消息数外，您还可以指定在一周或一天内发送的最大消息数。频率上限基于所选日历周期并在相应时间范围的起始点重置。[了解详情](../configuration/frequency-rules.md#create-new-rule)

**决策管理**

* **Edge 的频率上限** - 频率上限计数器现已更新，不到 3 秒即可在 Edge Decisioning API 决策中启用。[了解详情](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)