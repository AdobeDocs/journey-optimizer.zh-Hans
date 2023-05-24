---
solution: Journey Optimizer
product: journey optimizer
title: 关于数据源
description: 了解如何配置数据源
feature: Data Sources
topic: Administration
role: Admin, Developer
level: Intermediate
keywords: 資料，來源，歷程，平台
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 73%

---

# 关于数据源 {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="关于数据源"
>abstract="数据源配置操作必须始终由技术用户执行。数据源配置允许您定义与系统的连接，以检索将在您的历程中使用的其他信息，例如：条件定义、操作中的参数和个性化数据、自定义等待定义、时区定义。"

数据源配置允许您定义与系统的连接，以检索将在您的历程中使用的其他信息，例如：

* [条件定义](../building-journeys/condition-activity.md)
* [操作](../action/action.md)中的参数和个性化数据
* [自定义等待定义](../building-journeys/wait-activity.md#custom)
* [时区定义](../building-journeys/timezone-management.md)

➡️ [在视频中发现此功能](#video)

如果您的历程只利用来自事件有效负载的本地数据，则不需要此配置。例如，如果您的歷程由事件組成，接著是隻使用事件資料的管道動作活動，則不需要設定資料來源。

数据源有两种类型：

* 预配置的 Adobe Experience Platform 数据源，它定义与实时客户资料服务的连接。这是一种内置数据源。请参阅[此页](../datasource/adobe-experience-platform-data-source.md)。
* 外部数据源，它允许您定义与外部系统的连接。这些是您可以创建的数据源。请参阅[此页](../datasource/external-data-sources.md)。

对于每个数据源，您定义要使用字段组检索的信息。字段组是可从数据源检索的字段集。请参阅[此页](../datasource/configure-data-sources.md#define-field-groups)。

>[!NOTE]
>
>資料來源不支援結構描述關係。

如需如何設定Adobe Experience Platform資料來源和外部資料來源，以及如何在歷程中尋找和使用資料的詳細資訊，請觀看此影片 [教學課程影片](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target="_blank"}.

## 操作方法视频 {#video}

了解什么是数据源以及如何配置 Experience Platform 和外部数据源。

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

