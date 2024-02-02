---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b87ebc097c0c1c52ab21a4d098fbc2e5e227c953
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 28%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

## 2024年1月早期发行说明 {#jan-2024}

**发行日期**：2024年1月30日至31日

### 新功能{#jan24-features}

此版本引入了下方列出的新功能。

<table>
<thead>
<tr>
<th><strong>可投放性更新</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在支持DMARC身份验证技术。</p>
<p>从2024年2月1日开始，Google和Yahoo！ 要求您拥有DMARC记录，以便您向任何域发送电子邮件。 确保为您已委派或正在委派给Journey Optimizer中的Adobe的所有子域设置了DMARC记录。</p>
<p>有关更多信息，请参阅<a href="../configuration/dmarc-record-update.md">详细文档</a>。</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>用例行动手册</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>利用Real-Time CDP和Journey Optimizer中特定于行业的用例行动手册目录，解决您可以使用Adobe Experience Platform和Adobe历程优化器执行的常见用例。</p><p>一旦您选择了最符合您需求的行动手册，您就可以启用该行动手册以生成支持您的用例所需的资产（如历程、消息、架构或区段），并根据您的架构对其进行自定义以更快地实现价值。</p>
<p>有关更多信息，请参阅<a href="../start/playbooks.md">详细文档</a>。</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### 改进 {#jan24-improvements}

此版本包含下方列出的改进。

**报告**

* **新的基于域的划分构件**  — 添加了新构件，用于增强您的促销活动和历程报表。 此 **按域列出的退回原因**， **按域发送和投放**， **按域划分的打开数和点击数** 和 **按域列出的退回和错误** 小组件在域级别提供了关键电子邮件投放和跟踪指标的详细细分。 [了解详情](../reports/channel-report.md)

**短信渠道**

* **双重选择加入**  — 短信的双重选择加入工作流程可确保用户在从其设备发起请求时，明确选择加入接收消息。 用户通过发送入站SMS消息启动同意流程。 确认同意后，将发送后续消息，请求进行最终验证。 如果用户配置文件不存在，则会在成功确认时创建该配置文件。 [了解详情](../sms/sms-configuration.md#create-api)

  请注意，此功能适用于Sinch和Infobip短信提供商。

**历程**

* **反应事件持续时间**  — 您可以在 **反应事件** 现在为29天，而不是30天。 [了解详情](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **读取受众**  - **读取受众** 活动现在依赖于批处理区段的配置文件快照数据集，该数据集仅在计划的每日批处理作业运行后一天生成一次，因此数据将刷新到上一次每日批处理作业。 [了解详情](../building-journeys/read-audience.md)

* **字段组**  — 此版本修复了在某些情况下阻止保存字段组的问题。

**频率规则**

* **每周和每日频率上限**  — 现在，您可以指定在一周或一天内（除月外），向客户配置文件发送的最大消息数。 频率上限基于所选日历周期并在相应时间范围的开始处重置。 [了解详情](../configuration/frequency-rules.md#create-new-rule)

**决策管理**

* **边缘的频率封顶**  — 频率上限计数器现已更新，不到3秒即可在Edge Decisioning API决策中提供。 [了解详情](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)