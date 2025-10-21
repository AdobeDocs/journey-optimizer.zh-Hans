---
solution: Journey Optimizer
product: journey optimizer
title: 数据源入门
description: 了解如何开始使用数据源
feature: Journeys, Data Sources
topic: Administration
role: Engineer, Admin
level: Intermediate, Experienced
keywords: 数据，来源，历程，平台
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 65%

---

# 数据源入门 {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="关于数据源"
>abstract="数据源配置操作必须始终由技术用户执行。数据源配置允许您定义与系统的连接，以检索将在您的历程中使用的其他信息，例如：条件定义、操作中的参数和个性化数据、自定义等待定义、时区定义。"

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

有关如何配置 Adobe Experience Platform 数据源和外部数据源以及如何在历程中查找和使用数据的更多信息，请观看此[教程视频](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html?lang=zh-Hans){target="_blank"}。

## 操作说明视频 {#video}

了解什么是数据源以及如何配置 Experience Platform 和外部数据源。

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

