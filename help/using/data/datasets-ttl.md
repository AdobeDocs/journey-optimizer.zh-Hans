---
solution: Journey Optimizer
product: journey optimizer
title: 关于生存时间(TTL)和流式分段更改
description: Adobe Journey Optimizer中的生存时间和流分段更改
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 平台、数据湖、创建、湖、数据集、个人资料
source-git-commit: 1be920fb8b3ea825e38084f459523ccde0ad979b
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 5%

---


# 生存时间和流分段更改 {#ttl-guardrail}

## 存留时间(TTL)护栏 {#ttl}

从2024年11月1日开始，将在&#x200B;**新沙盒和新组织**&#x200B;中向Journey Optimizer系统生成的数据集推出生存时间(TTL)护栏，如下所示：

* 配置文件存储中的数据为 90 天
* 数据湖中的数据为 13 个月

此更改将在以后的阶段中随后转出到&#x200B;**现有客户沙盒**。

**常见问题解答**

+++ 此更改将仅适用于生产沙盒，还是也适用于开发沙盒？

此更改将应用于所有沙盒类型。

+++


+++ 对于配置文件存储中的90天TTL，配置文件本身是否会受到影响？

在90天后丢弃配置文件中系统生成的数据集数据，而不是丢弃配置文件本身。

+++

+++ 如果系统生成的数据集数据被推送到Customer Journey Analytics(CJA)，CJA中的数据是否也会受到TTL的影响？

CJA中的数据与Experience Platform保持同步。 因此，由于TTL而删除系统生成的数据集数据也会影响CJA中的数据。

+++

## 流式分段更新 {#segmentation-update}

此外，从11月1日起，流式分段将不再支持使用跟踪和反馈数据集中的发送和反馈事件。  有关过去不建议采用这种做法的原因的信息，请参阅[此处](../audience/about-audiences.md#streaming-segmentation-events-guardrails)。


**常见问题解答**

+++ 这些更改是否会影响点击或其他跟踪事件的使用？

此更改仅影响发送和打开事件的使用；点击和其他跟踪事件仍可在流区段中使用。

+++

+++ 此更改是否会影响批量分段？

此更改仅影响流式客户细分；发送和打开事件仍可在批处理客户细分中使用。 如果在流区段中使用它们，则将批量评估它们。

+++

+++ 此更改是否会影响跟踪数据的收集？

此更改不会影响跟踪数据的收集。 将继续收集发送和未结事件。

+++


+++ 反应事件是否受此更改的影响？

历程中的反应事件不受此更改的影响。

+++


+++ 此更改将仅适用于生产沙盒，还是也适用于开发沙盒？

此更改将应用于所有沙盒类型。

+++