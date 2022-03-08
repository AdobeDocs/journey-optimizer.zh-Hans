---
title: 关于数据源
description: 了解如何配置数据源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 72%

---

# 关于数据源 {#about-data-sources}

>[!CONTEXTUALHELP]
>id="jo_datasources"
>title="关于数据源"
>abstract="数据源配置操作必须始终由技术用户执行。数据源配置允许您定义与系统的连接，以检索将在您的历程中使用的其他信息，例如：条件定义、操作中的参数和个性化数据、自定义等待定义、时区定义。"

数据源配置允许您定义与系统的连接，以检索将在您的历程中使用的其他信息，例如：

* [条件定义](../building-journeys/condition-activity.md)
* [操作](../action/action.md)中的参数和个性化数据
* [自定义等待定义](../building-journeys/wait-activity.md#custom)
* [时区定义](../building-journeys/timezone-management.md)

如果您的历程只利用来自事件有效负载的本地数据，则不需要此配置。例如，如果您的历程由事件组成，后跟一个仅使用事件数据的消息活动，则无需配置数据源。

数据源有两种类型：

* 预配置的 Adobe Experience Platform 数据源，它定义与实时客户资料服务的连接。这是一种内置数据源。请参阅[此页](../datasource/adobe-experience-platform-data-source.md)。
* 外部数据源，它允许您定义与外部系统的连接。这些是您可以创建的数据源。请参阅[此页](../datasource/external-data-sources.md)。

对于每个数据源，您定义要使用字段组检索的信息。字段组是可从数据源检索的字段集。请参阅[此页](../datasource/configure-data-sources.md#define-field-groups)。

>[!NOTE]
>
>数据源现在支持架构关系。

有关如何配置Adobe Experience Platform数据源和外部数据源以及如何在历程中查找和使用数据的更多信息，请观看此视频 [教程视频](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/configure-data-sources.html){target=&quot;_blank&quot;}。
