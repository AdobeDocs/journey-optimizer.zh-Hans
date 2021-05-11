---
title: 技术设置
description: 了解管理和设置指南
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 7%

---

# 技术设置

![](assets/do-not-localize/badge.png)

## 设置品牌参数{#cjm-branding}

每个公司都具有属于自己的品牌视觉和技术准则。您可以定义一套规范，从徽标到技术方面(如电子邮件发送者、镜像页面URL的域或邮件跟踪设置)，向客户展示一致的品牌。
最终用户不能创建或修改品牌：此配置由Adobe管理。

要设置[!DNL Journey Optimizer]实例的品牌参数，您需要联系Adobe并共享以下详细信息：

* 公司名称

* 发件人（发件人）电子邮件地址

* 发件人（发件人）姓名

* 回复地址

配置品牌参数后，您将能够在创建消息时选择它们。

配置品牌参数后，您将能够在从&#x200B;**[!UICONTROL Presets]**&#x200B;列表创建消息时选择这些参数。 [了解有关内容创建的更多信息](create-message.md)。

## 配置推送通知渠道

了解如何在此[部分](configure-push.md)中配置推送渠道。

## 子域委派

对于要在[!DNL Journey Optimizer]中使用的任何新子域，第一步是委派它。 您需要联系Adobe技术联系人。

实施解决方案时，需要面向外部的组件：这包括设置要跟踪的链接和网页、显示镜像页面等。

虽然这些要求是通过由Adobe和客户托管的组件进行管理的，但它们包含URL，这些URL可以通过电子邮件的收件人查看。  为避免有指示基础技术解决方案或托管提供商的URL，可以设置子域以使此对电子邮件收件人透明。

在这些授权之后，Adobe建立的基础设施确保对每个授权的或基于CNAME的发送域执行以下服务：

* 创建postmaster@和ubuse@收件箱

* 为委托域设置反馈循环

* 基本DMARC记录配置

由Adobe建立的参数仅在完成委派后由Adobe验证时才有效，并且仍然有效。

[了解有关域委派的更多信息](https://helpx.adobe.com/cn/campaign/kb/domain-name-delegation.html)。


## 创建数据源、事件和操作

使用&#x200B;**[!UICONTROL Admin]**&#x200B;部分管理&#x200B;**[!UICONTROL Data Sources]**、**[!UICONTROL Events]**&#x200B;和&#x200B;**[!UICONTROL Actions]**。

![](assets/admin-menu.png)

### 数据源

数据源配置允许您定义与系统的连接，以检索将在您的旅程中使用的其他信息。

了解有关此[部分](../using/datasource/about-data-sources.md)中的数据源的更多信息

### 事件

事件允许您触发整个旅程，以实时向流入旅程的个人发送消息。

在事件配置中，您配置了旅程中预期的事件。 传入事件的数据将按照Adobe体验数据模型(XDM)进行标准化。 事件来自已验证和未验证事件（如 Adobe Mobile SDK 事件）的流摄取 API。

了解有关此[部分](../using/event/about-events.md)中事件的更多信息

### 操作

[!DNL Journey Optimizer] 消息功能内置：您只需设计内容并发布消息。如果您使用第三方系统发送消息，则可以创建自定义操作。

了解有关此[部分](../using/action/action.md)中操作的更多信息
