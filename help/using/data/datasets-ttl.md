---
solution: Journey Optimizer
product: journey optimizer
title: 关于数据集生存时间(TTL)护栏
description: ' [!DNL Adobe Journey Optimizer]中的数据集生存时间护栏'
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 平台, 数据湖, 创建, 湖, 数据集, 用户档案
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: b27ddcc88ca4b4209c9d29974a0b0d0dbe98cc94
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 17%

---

# 数据集生存时间 (TTL) 护栏 {#ttl-guardrail}

从 2025 年 2 月起，已在&#x200B;**新沙盒和新组织**&#x200B;中推出用于 Journey Optimizer 系统生成的数据集的生存时间 (TTL) 护栏，如下所示：

* 配置文件存储中的数据为 90 天，
* 数据湖中的数据为 13 个月。

此更改将在后续阶段转出到&#x200B;**现有客户沙盒**。

## 受影响的数据集 {#datasets}

下表列出了数据湖和个人资料存储中所有受影响的数据集及其各自的生存时间。

| 数据集 | 数据湖TTL | 配置文件存储TTL |
|------|-----|-----|
| AJO消息反馈事件数据集 | 13 个月 | 90 天 |
| AJO电子邮件跟踪体验事件数据集 | 13 个月 | 90 天 |
| AJO推送跟踪体验事件数据集 | 13 个月 | 90 天 |
| AJO实体数据集 | 13 个月 | 90 天 |
| AJO表面数据集 | 13 个月 | 不适用 |
| AJO入站活动事件数据集 | 13 个月 | 90 天 |
| AJO分类数据集 | 13 个月 | 不适用 |
| AJO电子邮件密件抄送反馈事件数据集 | 13 个月 | 不适用 |
| acpEntity事件数据集 | 13 个月 | 不适用 |
| 历程 | 13 个月 | 不适用 |
| 历程步骤事件 | 13 个月 | 不适用 |
| 决策对象存储库 — 个性化优惠 | 13 个月 | 不适用 |
| 决策对象存储库 — 后备优惠 | 13 个月 | 不适用 |
| 决策对象存储库 — 投放位置 | 13 个月 | 不适用 |
| 决策对象存储库 — 活动 | 13 个月 | 不适用 |
| ODE DecisionEvents - prod decisioning | 13 个月 | 不适用 |

## 常见问题 {#faq}

以下是有关数据集TLL的常见问题解答列表。

+++此更改是仅适用于生产沙盒，还是也适用于开发沙盒？

此更改将应用于所有沙盒类型。

+++

+++对于配置文件存储中的90天TTL，配置文件本身是否会受到影响？

在90天后丢弃配置文件中系统生成的数据集数据，而不是丢弃配置文件本身。

+++

+++如果将系统生成的数据集数据推送到[!DNL Customer Journey Analytics] (CJA)，CJA中的数据是否也会受TTL的影响？

[!DNL Customer Journey Analytics]中的数据与Experience Platform保持同步。 因此，因系统生成的数据集数据的TTL而删除数据也将影响[!DNL Customer Journey Analytics]中的数据。

+++

+++ 客户能否增加配置文件存储中[!DNL Journey Optimizer]系统数据集数据的TTL？

当前不支持TTL扩展。 但是，已计划优化TTL流程，以便在2025年下半年开始的某个时候允许这些扩展请求。

>[!NOTE]
>
>存储在用户档案中的数据受总数据量权利文件的约束。 因此，因TTL扩展而导致配置文件上任何数据存储增加都将计入总数据卷权利中。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/landing/license/total-data-volume.html?lang=zh-Hans){target=_blank}

+++

+++客户能否增加数据湖中[!DNL Journey Optimizer]系统数据集数据的TTL？

当前不支持TTL扩展。 客户可以通过目标导出数据，以更长时间地保留数据。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=zh-Hans){target=_blank}。 此外，拥有&#x200B;**[!DNL Data Distiller]**&#x200B;权利的客户可以创建派生的数据集以将数据存储在没有TTL的数据湖中。 [了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/query/data-distiller/derived-datasets/overview){target=_blank}

+++

+++TTL是否会影响以下功能？

* **查找存储**：否
* **历程上限**：否
* **优惠上限**：否
* **发送时间优化(STO)**：否
* **消息频率上限**（即业务规则）：否
* **报告**：否

  >[!NOTE]
  >
  >已在[!DNL Customer Journey Analytics] (CJA)连接上实施TTL，这将受影响的数据集数据的有效最大回顾周期减少到13个月。

* **Experience Platform数据源**：是 — 体验事件检索受90天TTL限制。
* **计算属性**：是 — 初始回填计算将限制为过去90天的数据；计算属性将根据后续更新的增量事件进行更新。 一旦后续更新到达回顾时段（最多6个月），TTL就基本上不再影响计算属性。 了解详情。
* **分段和重新定位**：是 — 分段依赖于个人资料存储中的数据；因此，对受影响的数据集数据的回溯限制为90天。
* **跟踪**：是 — 将受影响的数据集数据的有效最大回溯时段减少到90天。 来自受影响的数据集的数据在数据湖中保留13个月。

+++

+++什么时间戳用于TTL实施（例如，对于回填用例）？

将使用事件时间戳（即不是摄取日期）。

+++
