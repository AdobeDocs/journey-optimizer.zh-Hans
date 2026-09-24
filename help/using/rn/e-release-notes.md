---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
source-git-commit: 16ed1a917bdc0a32bba166dc7a71c2c1d2fdea95
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 37%
---

# 预发行说明 {#e-release-notes}

Adobe Journey Optimizer 不断地提供新功能、对现有功能的增强和错误修复。 所有更改会在每月末整合到[发行说明](release-notes.md)中。

## 2026年9月预发行说明 {#sep-26-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。 一旦更改发布到生产环境，链接、屏幕和更新的文档就会发布。 虽然大多数更改将在发布日期交付，但其中一些更改可能会稍后推出 — 有关详细信息，请参阅为每个条目列出的发布日期。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发行日期**： 2026年9月22日至23日


<!--
### Onboarding {#sep-26-onboarding}

The following capability is coming to onboarding in this release.

<table>
<thead>
<tr>
<th><strong>Guided capabilities for onboarding emails and journeys (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A <strong>dedicated workspace</strong> lets you reuse what you have instead of rebuilding from scratch.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>

-->

### 历程 {#sep-26-journeys}

在此版本中，历程中即将提供以下功能和改进。

* **减少等待和事件活动的步骤事件** — 不再为&#x200B;**等待**&#x200B;活动和&#x200B;**事件**&#x200B;活动生成步骤事件，因为在该活动中实际未处理配置文件。<!-- DRAFT: pending DOCAC sub-task under DOCAC-15691, see CJM-165835 -->
<!-- Documentation link: TBD -->

### 渠道 {#sep-26-channels}

此版本中的渠道即将推出以下改进。

* **直邮 — 自动拆分大文件** — 现在，当直邮文件大约超过20 GB时，可以自动将其拆分为多个部分，或者通过在文件路由配置中选择目标文件大小来手动拆分。

* **直邮 — 增加了受众限制** — 直邮渠道受众限制已从300万个配置文件增加到1亿个配置文件，使您可定位更多受众，而不会出现文件创建错误。

### 编排的营销活动 {#sep-26-oc}

在此版本中，编排的营销活动中即将提供以下功能和改进。


* **新的协调营销活动监控API** — 新&#x200B;**API规范**&#x200B;现在可用于协调营销活动，允许您以编程方式创建、管理和触发协调营销活动，从而与外部系统和自动化管道进行更深度的集成。


### 可用性改进 {#sep-26-usability}

* **内容模拟体验中的可用性改进** — 现在，通过新的内容模拟体验，您可以命名和组织变体以便轻松比较，直接从每个信息卡复制或删除变体详细信息，根据需要查看完整属性路径和每信息卡渠道配置，以及通过更突出的上传按钮上传您自己的CSV、JSON或JSONL配置文件。

* **促销活动、历程和编排的促销活动的统一日历** — 历程和促销活动的日历视图现在从单独的清单中移到一个统一的左边栏可访问菜单中，两者都显示在一个组合视图中。

