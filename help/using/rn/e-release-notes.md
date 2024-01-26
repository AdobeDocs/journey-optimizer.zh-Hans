---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 早期发行说明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 6683bfbb5569d197a2a746620cd7edc10f45b5d1
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 21%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月的最后一周整合到[发行说明](release-notes.md)中。

以下早期发行说明可能会在正式发行日期之前发生更改，恕不另行通知。链接、屏幕和更新文档，会在发行之日发布于[发行说明](release-notes.md)中。

## 2024年1月早期发行说明 {#oct-jan-2024}

**发行日期**：2024年1月20日至31日

### 新功能{#jan-2024-features}

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
<p>从2024年2月1日开始，Google和Yahoo！ 将要求您拥有用于向其发送电子邮件的任何域的DMARC记录。 确保为您已委派或正在委派给Journey Optimizer中的Adobe的所有子域设置了DMARC记录。</p>
<!--img src="assets/channel-reports.png"/-->
<p>有关更多信息，请参阅<a href="../configuration/dmarc-record-update.md">详细文档</a>。</p>
</tr>
</tbody>
</table>



### 改进 {#jan-2024-improvements}

此版本包含下方列出的改进。

**报告**

* **按域划分的渠道报表**  — 添加了新构件，用于增强您的促销活动和历程报表。 此 **按域列出的退回原因**， **按域发送和投放**， **按域划分的打开数和点击数** 和 **按域列出的退回和错误** 小组件在域级别提供了关键电子邮件投放和跟踪指标的详细细分。 [了解详情](../reports/channel-report.md)

**短信渠道**

* **双重选择加入**  — 短信的双重选择加入工作流程可确保用户在从其设备发起请求时，明确选择加入接收消息。 用户通过发送入站SMS消息启动同意流程。 确认同意后，将发送后续消息，请求进行最终验证。 如果用户配置文件不存在，则会在成功确认时创建该配置文件。

  请注意，这仅适用于Sinch和Infobip短信提供商。

**历程**

* **反应事件持续时间**  — 您可以在 **反应事件** 现在为29天，而不是30天。 [了解详情](../building-journeys/reaction-events.md)

* **日期过滤器**  — 除了现有的预定义日期过滤器之外，您现在可以使用自定义日期来筛选历程库存。 这允许您通过显示特定日期、特定月内、全年或指定时间范围内发布的旅程来优化列表。

* **读取受众**   — 现在，读取受众活动依赖于批处理区段的配置文件快照数据集，该数据集仅在计划的每日批处理作业运行一天后生成一次。

**频率规则**

* **每周和每日频率上限**  — 现在，您可以指定在一周或一天内（除月外），向客户配置文件发送的最大消息数。 频率上限基于所选日历周期并在相应时间范围的开始处重置。


**决策管理**

* **边缘上的频率字幕**  — 频率上限计数器现已更新，不到3秒即可在Edge Decisioning API决策中提供。