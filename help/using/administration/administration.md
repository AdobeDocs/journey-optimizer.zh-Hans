---
title: 技术设置
description: 了解管理和设置准则
hidefromtoc: true
hide: true
feature: 应用程序设置
topic: 管理
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 8%

---

# 技术设置

![](../assets/do-not-localize/badge.png)

## 设置品牌参数{#cjm-branding}

每个公司都具有属于自己的品牌视觉和技术准则。您可以定义一组规范，从徽标到技术方面（如电子邮件发件人、镜像页面URL的域或消息跟踪设置），向客户展示一致的品牌。
最终用户不能创建或修改品牌：此配置由Adobe管理。

要为[!DNL Journey Optimizer]实例设置品牌参数，您需要联系Adobe并共享以下详细信息：

* 公司名称

* 发件人（发件人）电子邮件地址

* 发件人（发件人）名称

* 回复地址

配置品牌策略参数后，您将能够在创建消息时选择这些参数。

配置了品牌策略参数后，在从&#x200B;**[!UICONTROL Presets]**&#x200B;列表创建消息时，将能够选择这些参数。 [了解有关内容创建的更多信息](../create-message.md)。

## 配置推送通知渠道

在此[部分](../create-push.md)中了解如何配置推送渠道。

## 子域委派

对于要在[!DNL Journey Optimizer]中使用的任何新子域，第一步是委派该子域。 您需要联系Adobe技术联系人。

实施解决方案时，需要面向外部的组件：这些功能包括设置要跟踪的链接和网页、显示镜像页面等。

虽然这些要求通过由Adobe和客户托管的组件进行管理，但它们包含可供电子邮件收件人查看的URL。  为避免拥有指示底层技术解决方案或托管提供商的URL，可以设置子域以使其对电子邮件的收件人透明。

在执行这些授权后，由Adobe建立的基础架构可确保为每个授权的或基于CNAME的发送域执行以下服务：

* 在收件箱中创建postmaster@和ubuse@

* 为委派的域设置反馈循环

* 基本DMARC记录配置

由Adobe建立的参数仅在委派完成后由Adobe验证并保持正常工作时有效。

[了解有关域委派的更多信息](https://helpx.adobe.com/cn/campaign/kb/domain-name-delegation.html)。


## 创建数据源、事件和操作

使用&#x200B;**[!UICONTROL Admin]**&#x200B;部分管理&#x200B;**[!UICONTROL Data Sources]**、**[!UICONTROL Events]**&#x200B;和&#x200B;**[!UICONTROL Actions]**。

![](../assets/admin-menu.png)

### 数据源

数据源配置允许您定义与系统的连接，以检索将在您的历程中使用的其他信息。

在此[部分](../datasource/about-data-sources.md)中了解有关数据源的更多信息

### 事件

事件允许您触发旅程，以便实时向流入旅程的个人发送消息。

在事件配置中，您可以配置历程中预期的事件。 传入事件的数据按照Adobe体验数据模型(XDM)进行标准化。 事件来自已验证和未验证事件（如 Adobe Mobile SDK 事件）的流摄取 API。

在此[部分](../event/about-events.md)中了解有关事件的更多信息

### 操作

[!DNL Journey Optimizer] 消息功能是内置的：您只需设计内容并发布消息即可。如果您使用第三方系统发送消息，则可以创建自定义操作。

了解有关此[部分](../action/action.md)中操作的更多信息
