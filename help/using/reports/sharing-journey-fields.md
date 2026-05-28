---
solution: Journey Optimizer
product: journey optimizer
title: 历程字段
description: 历程字段
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 177b4a97-c757-40ca-a190-fbd88169e5e2
TQID: https://experienceleague.adobe.com/dpQ6PEm-afX4PZuWSPrpAWDH7yBhUKZHZRF134VehAg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 6%

---

# 历程字段 {#sharing-journey-fields}

此字段组用于&#x200B;**journey**&#x200B;架构（与&#x200B;**journeyStepEvent**&#x200B;相关）。 它包含下面列出的字段。


>[!NOTE]
>
>在本节[&#128279;](../building-journeys/expression/journey-properties.md#journey-properties-fields)中了解有关历程属性的更多信息。


## journeyID {#journeyid-field}

主历程的ID。

类型：字符串

## journeyVersionID {#journeyversionid-field}

历程版本的ID。 此id表示历程的身份。

类型：字符串

## name {#name-field}

历程的名称。

类型：字符串

>[!NOTE]
>
>历程名称用于将历程执行数据与报表数据集关联。 如果重命名历程，请确保新名称与报告数据集中的名称匹配，以保持准确的报告。 不匹配可能会导致报表数据无法按预期显示。 了解有关[解决缺少报表数据问题](../building-journeys/report-journey.md#troubleshooting-missing-data)的详细信息。

## 描述 {#description-field}

历程的描述。

类型：字符串

## version {#version-field}

版本，表示为`major`.`minor`

类型：字符串
