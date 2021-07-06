---
title: 管理和设置
description: 了解管理和设置准则
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: 应用程序设置
topic: 管理
role: Administrator
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 50%

---

# 配置历程

要随历程发送消息，您需要配置&#x200B;**[!UICONTROL Data Sources]**、**[!UICONTROL Events]**&#x200B;和&#x200B;**[!UICONTROL Actions]**。

![](../assets/admin-menu.png)

## 数据源

数据源配置允许您定义与系统的连接，以检索将在您的历程中使用的其他信息。 [了解详情](../../using/datasource/about-data-sources.md)

## 事件

事件允许您触发旅程，以便实时向流入旅程的个人发送消息。

在事件配置中，您可以配置历程中预期的事件。 传入事件的数据按照Adobe体验数据模型(XDM)进行标准化。 事件来自已验证和未验证事件（如 Adobe Mobile SDK 事件）的流摄取 API。[了解详情](../../using/event/about-events.md)

## 操作

Journey Optimizer消息功能是内置的：您只需设计内容并发布消息即可。 如果您使用第三方系统发送消息，则可以创建自定义操作。 [了解详情](../../using/action/action.md)

## 浏览 Adobe Experience Platform 字段 {#friendly-names-display}

定义[事件有效负载](../event/about-creating.md#define-the-payload-fields)、[字段组有效负载](../datasource/configure-data-sources.md#define-field-groups)并在[表达式编辑器](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html?lang=zh-Hans){target=&quot;_blank&quot;}中选择字段时，除字段名称外，还会显示显示名称。 此信息可从体验数据模型中的架构定义中检索。

如果在设置架构时提供了诸如“xdm:alternateDisplayInfo”之类的描述符，则用户友好型名称将替换显示名称。在处理“eVars”和通用字段时，这个描述符特别有用。您可以通过 API 调用配置友好型名称描述符。有关详细信息，请参阅[架构注册开发人员指南](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=zh-Hans){target=&quot;_blank&quot;}。

![](../assets/xdm-from-descriptors.png)

如果友好名称可用，则字段将显示为`<friendly-name>(<name>)`。如果没有可用的友好名称，将显示其显示名称，如`<display-name>(<name>)`。如果这两种名称均未定义，则仅显示字段的技术名称 `<name>`。

>[!NOTE]
>
>从架构组合中选择字段时，不会检索友好名称。