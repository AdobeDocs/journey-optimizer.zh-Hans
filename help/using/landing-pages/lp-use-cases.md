---
title: 登陆页面用例
description: 了解Journey Optimizer中登陆页面的最常见用例
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 21%

---

# 登陆页面用例

以下是如何使用的示例 [!DNL Journey Optimizer] 登陆页面，让您的客户选择启用/禁用接收部分或全部通信。

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## 订购服务 {#subscription-to-a-service}

下面介绍了让收件人订阅服务的主要步骤。

![](../assets/lp_subscription-uc.png)

例如，假设您下月组织了一个事件，并且希望启动一个事件注册营销活动，以便有兴趣的客户随时更新该事件。

1. 创建事件注册的订阅列表。 了解详情 [订阅列表](subscription-list.md)

1. [创建登陆页面](create-lp.md)，以便收件人注册参加您的活动。

1. 配置和设计注册登陆页面，包括指向订阅列表的链接。 了解有关构建 [主登陆页面](create-lp.md#configure-primary-page)

1. 创建感谢页面，在收件人提交注册表单后，该页面将显示给收件人。 了解详情 [登陆子页面](create-lp.md#configure-subpages)

1. 创建电子邮件。 了解详情 [创建消息](../create-message.md)

1. [插入链接](../message-tracking.md#insert-links) 中。 选择 **[!UICONTROL Landing page]** 作为 **[!UICONTROL Link type]** 然后选择 [登陆页面](create-lp.md#configure-primary-page) 创建的注册目录。

   ![](../assets/lp_subscription-uc-link.png)

1. 保存您的内容并[发布您的消息](../publish-manage-message.md)。

1. 通过 [历程](../building-journeys/journey.md) 要宣布注册，现在将为您的活动打开并引导流量进入注册登陆页面。

   收到电子邮件后，如果您的收件人单击登陆页面的链接，他们将被定向到感谢页面，并被添加到订阅列表。

1. 您可以向为您的活动注册的收件人发送确认电子邮件。 为此，请使用 **[!UICONTROL Segment qualification]** 事件，然后选择您创建为区段的订阅列表。

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## 选择退出 {#opt-out}

要使收件人取消订阅您的通信，您可以在电子邮件中包含一个指向选择退出登陆页面的链接。

进一步了解管理收件人的同意，以及为什么在 [此部分](../consent.md).

### 选择退出管理 {#opt-out-management}

向收件人提供取消从品牌接收通信的功能是一项法律要求。详细了解 [Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}。

因此，您必须在发送给收件人的每封电子邮件中都加入&#x200B;**取消订阅链接**：

* 单击此链接后，收件人将被定向到一个包含确认取消订阅按钮的登陆页面。
* 单击选择退出按钮后，用户档案数据将更新此信息。

### 配置选择退出 {#configure-opt-out}

要让消息的收件人通过登陆页面取消订阅您的通信，请执行以下步骤。

1. 构建 [登陆页面](create-lp.md). 使用特定于登陆页面的 **[!UICONTROL Form]** 组件，定义 **[!UICONTROL Opt-out]** 复选框并选择更新 **[!UICONTROL Channel (email)]**:所有通信中将禁用您登陆页面上选择退出框的用户档案。 [了解详情](design-lp.md)

   <!--You can also build your own landing page and host it on the third-party system of your choice. To keep?-->

1. 在 [!DNL Journey Optimizer] 上[创建消息](../create-message.md)。

1. 选择内容中的文本，并 [插入链接](../message-tracking.md#insert-links) 使用上下文工具栏。 您还可以在按钮上使用链接。

   ![](../assets/lp_opt-out-insert-link.png)

1. 从 **[!UICONTROL Link type]** 下拉列表中选择 **[!UICONTROL Landing page]**。

1. 选择 [登陆页面](create-lp.md#configure-primary-page) 您为选择退出而创建的。

   ![](../assets/lp_opt-out-landing-page.png)

1. 单击 **[!UICONTROL Save]**。

1. 保存您的内容并[发布您的消息](../publish-manage-message.md)。

1. 通过 [历程](../building-journeys/journey.md).

1. 收到消息后，如果收件人单击取消订阅链接，将显示您的登陆页面。

   <!--![](../assets/lp_opt-out-lp-example.png)-->

1. 如果收件人单击登陆页面中的选择退出链接，则用户档案数据会更新，除非再次订阅，否则将不会从您的品牌接收通信。

   <!--The opted-out recipient is then redirected to a confirmation message screen indicating that opting out was successful.-->

   <!--![](../assets/lp_opt-out-confirmation-example.png)-->

要检查相应用户档案的选择是否已更新，请转到 Experience Platform，并通过选择身份命名空间和相应的身份值访问该用户档案。在 [Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}。

![](../assets/lp_opt-out-profile-choice.png)

在 **[!UICONTROL Attributes]** 选项卡中，您可以看到 **[!UICONTROL choice]** 的值已更改为 **[!UICONTROL no]**。

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../message-tracking.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../consent.md#unsubscribe-email)
-->