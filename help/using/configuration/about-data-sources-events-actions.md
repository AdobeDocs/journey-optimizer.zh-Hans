---
solution: Journey Optimizer
product: journey optimizer
title: 配置历程
description: 了解如何配置数据源、事件和操作
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 配置，历程，功能板，数据源，事件，操作
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 65%

---

# 配置历程 {#configure-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_configuration_dashboard"
>title="关于历程配置"
>abstract="要随历程一起发送消息，您需要配置数据源、事件和操作。使用数据源，您可以定义与系统的连接，以检索将在您历程中使用的其他信息，例如在条件中。事件让您可以在收到事件时触发历程。利用自定义操作，您可以连接到第三方系统以发送消息。如果您使用 Journey Optimizer 内置消息功能，则无需配置操作。"

若要发送包含历程的消息，您需要配置&#x200B;**[!UICONTROL 数据源]**、**[!UICONTROL 事件]**&#x200B;和&#x200B;**[!UICONTROL 操作]**。

![](assets/admin-menu.png)

## 数据源 {#data-sources}

数据Source配置允许您定义与系统的连接，以检索将在您的旅程中使用的其他信息。 [了解详情](../../using/datasource/about-data-sources.md)

## 活动 {#events}

事件允许您统一触发历程，向流入历程的个人实时发送消息。

在事件配置中，您可以配置历程中的预期事件。传入事件的数据按照Adobe体验数据模型(XDM)进行标准化。 事件来自已验证和未验证事件（如 Adobe Mobile SDK 事件）的流摄取 API。[了解详情](../../using/event/about-events.md)

## 操作 {#actions}

Journey Optimizer消息功能内置：您只需将渠道操作活动添加到历程中。 如果您使用第三方系统来发送消息，则可以创建自定义操作。 [了解详情](../../using/action/action.md)

## 浏览Adobe Experience Platform字段 {#friendly-names-display}

在定义[事件有效负载](../event/about-creating.md#define-the-payload-fields)、[字段组有效负载](../datasource/configure-data-sources.md#define-field-groups)以及在[表达式编辑器](../building-journeys/expression/expressionadvanced.md)中选择字段时，除字段名称外，还会显示其显示名称。此信息可从体验数据模型中的架构定义中检索。

如果在设置架构时提供了诸如“xdm:alternateDisplayInfo”之类的描述符，则用户友好型名称将替换显示名称。在处理“eVars”和通用字段时，这个描述符特别有用。您可以通过 API 调用配置友好型名称描述符。有关详细信息，请参阅[架构注册开发人员指南](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=zh-Hans){target="_blank"}。

![](assets/xdm-from-descriptors.png)

如果友好名称可用，则字段将显示为`<friendly-name>(<name>)`。如果没有可用的友好名称，将显示其显示名称，如`<display-name>(<name>)`。如果这两种名称均未定义，则仅显示字段的技术名称 `<name>`。

>[!NOTE]
>
>从架构组合中选择字段时，不会检索友好名称。
