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
source-git-commit: 6961a07e2874f9beb76a9beaebb29997d114d8e7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 6%

---

# 历程字段 {#sharing-journey-fields}

此字段组用于&#x200B;**journey**&#x200B;架构（与&#x200B;**journeyStepEvent**&#x200B;相关）。 它包含下面列出的字段。


>[!NOTE]
>
>在本节[中了解有关历程属性](../building-journeys/expression/journey-properties.md#journey-properties-fields)的更多信息。


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
