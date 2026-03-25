---
solution: Journey Optimizer
product: journey optimizer
title: 数据源入门
description: 了解如何开始使用数据源
feature: Journeys, Data Sources
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: 数据，来源，历程，平台
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: a422cad5349de0ad87aa3a11ce923e04e862a63c
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 35%

---

# 数据源入门 {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="关于数据源"
>abstract="数据源配置操作必须始终由技术用户执行。数据源配置允许您定义与系统的连接，以检索将在您的历程中使用的其他信息，例如：条件定义、操作中的参数和个性化数据、自定义等待定义、时区定义。"

>[!TIP]
>初次使用Journey Optimizer中的数据管理？ 从[数据管理入门](../data/gs-data.md)概述开始，在配置数据源之前了解架构、数据集、标识以及数据如何流动。

数据源配置允许您定义与系统的连接，以检索将在您的历程中使用的其他信息，例如：

* [条件定义](../building-journeys/condition-activity.md)
* [操作](../action/action.md)中的参数和个性化数据
* [自定义等待定义](../building-journeys/wait-activity.md#custom)
* [时区定义](../building-journeys/timezone-management.md)

➡️ [通过观看视频了解此功能](#video)

如果您的历程只利用来自事件有效负载的本地数据，则不需要此配置。例如，如果您的历程由一个事件组成，后跟一个只使用事件数据的渠道操作活动，则无需配置数据源。

数据源有两种类型：

* 预配置的&#x200B;**Adobe Experience Platform数据源，它定义与实时客户资料服务的连接。**&#x200B;这是一种内置数据源。请参阅[此页](../datasource/adobe-experience-platform-data-source.md)。
* 允许您定义与外部系统连接的&#x200B;**外部**&#x200B;数据源。 这些是您可以创建的数据源。请参阅[此页](../datasource/external-data-sources.md)。

>[!NOTE]
>
>由于现在支持响应，因此您应该对外部数据源用例使用自定义操作而不是数据源。 有关回应的详细信息，请参阅此[部分](../action/action-response.md)

对于每个数据源，您定义要使用字段组检索的信息。字段组是可从数据源检索的字段集。请参阅[此页](../datasource/configure-data-sources.md#define-field-groups)。

>[!NOTE]
>
>数据源不支持架构关系。

## 选择您的数据访问策略 {#data-access-strategy}

在配置数据源之前，请考虑哪种方法最适合您的用例。 提供了三种选项，每种选项在持久性、配置文件扩充和可重用性方面都有不同的取舍。 有关这些选项的详细讨论，请参阅[Journey Optimizer中高级历程的最佳实践](https://experienceleague.adobe.com/zh-hans/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}。

**选项1 — 通过自定义操作（无数据湖）访问外部数据**

在旅程运行时直接连接到外部API，而无需将数据保留在Experience Platform数据湖中。 最适合以下情况：

* 数据仅在历程上下文中有用，而在其他位置则不需要它。
* 可通过返回所需属性的API端点访问外部系统。

了解有关[自定义操作](../action/action.md)和[自定义操作响应](../action/action-response.md)的更多信息。

**选项2 — 数据湖中的数据集，未为配置文件**&#x200B;启用

将数据摄取到数据集中，以根据上下文事件数据触发历程并对历程进行个性化，而不会影响实时客户个人资料。 最适合以下情况：

* 记录中包含一个标识字段，用于访问已存储在Experience Platform中的用户档案。
* 在Journey Optimizer之外创建受众或拼合身份时不需要数据。

**选项3 — 数据湖中启用了配置文件的数据集**

将数据摄取到启用了[配置文件的数据集](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"}中以创建受众、丰富身份图，并在多个历程和RT-CDP目标中利用数据。 最适合以下情况：

* 这些数据可用于Journey Optimizer以外的渠道中使用的受众定义。
* 数据包含多个身份，这些身份有助于创建更丰富的拼接配置文件片段。

| | 数据保留在数据湖中 | 为配置文件启用的数据集 |
| --- | --- | --- |
| **选项1** — 通过自定义操作获取外部数据 | 否 | 否 |
| **选项2** — 未为配置文件启用数据集 | 是 | 否 |
| **选项3** — 启用配置文件的数据集 | 是 | 是 |

有关如何配置 Adobe Experience Platform 数据源和外部数据源以及如何在历程中查找和使用数据的更多信息，请观看此[教程视频](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html?lang=zh-Hans){target="_blank"}。

## 操作方法视频 {#video}

了解什么是数据源以及如何配置 Experience Platform 和外部数据源。

>[!VIDEO](https://video.tv.adobe.com/v/3416632?captions=chi_hans&quality=12)

