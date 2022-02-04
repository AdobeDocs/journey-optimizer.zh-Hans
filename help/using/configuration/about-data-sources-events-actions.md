---
title: 配置历程
description: 了解如何配置数据源、事件和操作。
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: dcdbf4a0cd6a93e56cbe97535515c1a6143db81b
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 56%

---

# 配置历程 {#configure-journeys}

要随历程发送消息，您需要配置 **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** 和 **[!UICONTROL Actions]**.

![](../assets/admin-menu.png)

## 数据源 {#data-sources}

数据源配置允许您定义与系统的连接，以检索将在您的历程中使用的其他信息。 [了解详情](../../using/datasource/about-data-sources.md)

## 活动 {#events}

事件允许您触发旅程，以便实时向流入旅程的个人发送消息。

在事件配置中，您可以配置历程中预期的事件。 传入事件的数据按照Adobe体验数据模型(XDM)进行标准化。 事件来自已验证和未验证事件（如 Adobe Mobile SDK 事件）的流摄取 API。[了解详情](../../using/event/about-events.md)

## 操作 {#actions}

Journey Optimizer消息功能是内置的：您只需设计内容并发布消息即可。 如果您使用第三方系统发送消息，则可以创建自定义操作。 [了解详情](../../using/action/action.md)

## 浏览 Adobe Experience Platform 字段 {#friendly-names-display}

在定义[事件有效负载](../event/about-creating.md#define-the-payload-fields)、[字段组有效负载](../datasource/configure-data-sources.md#define-field-groups)以及在[表达式编辑器](../building-journeys/expression/expressionadvanced.md)中选择字段时，除字段名称外，还会显示其显示名称。此信息可从体验数据模型中的架构定义中检索。

如果在设置架构时提供了诸如“xdm:alternateDisplayInfo”之类的描述符，则用户友好型名称将替换显示名称。在处理“eVars”和通用字段时，这个描述符特别有用。您可以通过 API 调用配置友好型名称描述符。有关更多信息，请参阅 [架构注册开发人员指南](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=zh-Hans){target=&quot;_blank&quot;}。

![](../assets/xdm-from-descriptors.png)

如果友好名称可用，则字段将显示为`<friendly-name>(<name>)`。如果没有可用的友好名称，将显示其显示名称，如`<display-name>(<name>)`。如果这两种名称均未定义，则仅显示字段的技术名称 `<name>`。

>[!NOTE]
>
>从架构组合中选择字段时，不会检索友好名称。
