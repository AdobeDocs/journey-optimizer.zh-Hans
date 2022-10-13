---
title: 登陆页面用例
description: 了解Journey Optimizer中登陆页面的最常见用例
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
exl-id: 8c00d783-54a3-45d9-bd8f-4dc58804d922
source-git-commit: 32c69ef268c78ba834612d16b2ac1c721fb5df56
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 15%

---

# 登陆页面用例 {#lp-use-cases}

以下是一些说明如何使用的示例 [!DNL Journey Optimizer] 登陆页面，让您的客户选择启用/禁用接收部分或全部通信。

## 订购服务 {#subscription-to-a-service}

最常见的用例之一是邀请客户 [订购服务](subscription-list.md) （例如新闻稿或事件）。 下图介绍了主要步骤：

![](assets/lp_subscription-uc.png)

例如，假设您下月组织了一个事件，并且想要启动一个事件注册营销活动<!--to keep your customers that are interested updated on that event-->. 为此，您将发送一封电子邮件，其中包含指向登陆页面的链接，以便您的收件人注册参加此活动。 注册的用户将添加到您为此创建的订阅列表中。

### 设置登陆页面 {#set-up-lp}

1. 创建事件注册的订阅列表，该列表将存储注册的用户。 了解如何创建订阅列表 [此处](subscription-list.md#define-subscription-list).

   ![](assets/lp_subscription-uc-list.png)

1. [创建登陆页面](create-lp.md) ，以便收件人注册您的活动。

   ![](assets/lp_create-lp-details.png)

1. 配置注册 [主登陆页面](create-lp.md#configure-primary-page).

1. 设计 [登陆页面内容](design-lp.md)，选择您创建的订阅列表，以使用选中注册复选框的用户档案对其进行更新。

   ![](assets/lp_subscription-uc-lp-list.png)

1. 创建“感谢”页面，在收件人提交注册表单后，该页面将显示给收件人。 了解如何配置登陆子页面 [此处](create-lp.md#configure-subpages).

   ![](assets/lp_subscription-uc-thanks.png)

1. [发布](create-lp.md#publish) 登陆页面。

1. 在 [历程](../building-journeys/journey.md)，添加 **电子邮件** 活动，以引导流量进入注册登陆页面。

   ![](assets/lp_subscription-uc-journey.png)

1. [设计电子邮件](../messages/get-started-content.md) 以宣布注册现已对您的活动开放。

1. [插入链接](../design/message-tracking.md#insert-links) 到消息内容中。 选择 **[!UICONTROL 登陆页面]** 作为 **[!UICONTROL 链接类型]** 然后选择 [登陆页面](create-lp.md#configure-primary-page) 创建的注册目录。

   ![](assets/lp_subscription-uc-link.png)

   >[!NOTE]
   >
   >要发送消息，请确保您选择的登陆页面尚未过期。 了解如何更新到期日期 [在此部分中](create-lp.md#configure-primary-page).

   收到电子邮件后，如果您的收件人单击登陆页面的链接，他们将被定向到“谢谢”页面，并被添加到订阅列表。

### 发送确认电子邮件 {#send-confirmation-email}

此外，您还可以向为您的活动注册的收件人发送电子邮件确认。 为此，请执行以下步骤。

1. 创建其他 [历程](../building-journeys/journey.md). 您可以通过单击 **[!UICONTROL 创建历程]** 按钮。 了解更多 [此处](create-lp.md#configure-primary-page)

   ![](assets/lp_subscription-uc-create-journey.png)

1. 展开 **[!UICONTROL 事件]** 类别和拖放 **[!UICONTROL 区段鉴别]** 活动。 了解更多 [此处](../building-journeys/segment-qualification-events.md)

1. 单击 **[!UICONTROL 区段]** 字段，然后选择您创建的订阅列表。

   ![](assets/lp_subscription-uc-confirm-journey.png)

1. 添加您选择的确认电子邮件，并在历程中发送该电子邮件。

   ![](assets/lp_subscription-uc-confirm-email.png)

为您的活动注册的所有用户都将收到确认电子邮件。

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## 选择退出 {#opt-out}

要使收件人取消订阅您的通信，您可以在电子邮件中包含一个指向选择退出登陆页面的链接。

进一步了解管理收件人的同意，以及为什么在 [此部分](../privacy/opt-out.md).

### 选择退出管理 {#opt-out-management}

向收件人提供取消订阅以停止从品牌接收通信的功能是一项法律要求。在 [Experience Platform 文档](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=zh-Hans#regulations){target=&quot;_blank&quot;}中进一步了解适用的法规。

因此，您必须在发送给收件人的每封电子邮件中都加入&#x200B;**取消订阅链接**：

* 单击此链接后，收件人将被定向到一个包含确认取消订阅按钮的登陆页面。
* 单击选择退出按钮后，用户档案数据将更新此信息。

### 配置选择退出 {#configure-opt-out}

要使电子邮件的收件人能够通过登陆页面取消订阅您的通信，请执行以下步骤。

1. 创建登陆页面。 [了解详情](create-lp.md)

1. 定义主页面。 [了解详情](create-lp.md#configure-primary-page)

1. [设计](design-lp.md) 主页面内容：使用特定于登陆页面的 **[!UICONTROL 表单]** 组件，定义 **[!UICONTROL 选择退出]** 复选框并选择更新 **[!UICONTROL 渠道（电子邮件）]**:所有通信中将禁用您登陆页面上选择退出框的用户档案。

   ![](assets/lp_opt-out-primary-lp.png)

   <!--You can also build your own landing page and host it on the third-party system of your choice.-->

1. 添加确认 [子页面](create-lp.md#configure-subpages) 将向提交表单的用户显示。

   ![](assets/lp_opt-out-subpage.png)

   >[!NOTE]
   >
   >确保在主页面的 **[!UICONTROL 行动动员]** 部分 **[!UICONTROL 表单]** 组件。 [了解详情](design-lp.md)

1. 配置并定义页面内容后， [发布](create-lp.md#publish) 登陆页面。

   ![](assets/lp_opt-out-publish.png)

1. [创建电子邮件](../messages/get-started-content.md) 在旅程中。

1. 在内容中选择文本，然后使用上下文工具栏[插入链接](../design/message-tracking.md#insert-links)。您还可以在按钮上使用链接。

   ![](assets/lp_opt-out-insert-link.png)

1. 选择 **[!UICONTROL 登陆页面]** 从 **[!UICONTROL 链接类型]** 下拉列表中，然后选择 [登陆页面](create-lp.md#configure-primary-page) 您为选择退出而创建的。

   ![](assets/lp_opt-out-landing-page.png)

   >[!NOTE]
   >
   >要发送消息，请确保您选择的登陆页面尚未过期。 了解如何更新到期日期 [在此部分中](create-lp.md#configure-primary-page).

1. 发布并运行历程。 [了解详情](../building-journeys/journey.md)。

1. 收到消息后，如果收件人单击电子邮件中的取消订阅链接，则会显示您的登陆页面。

   ![](assets/lp_opt-out-submit-form.png)

   如果收件人选中框并提交表单：

   * 已选择退出的收件人将被重定向到确认消息屏幕。

   * 用户档案数据已更新，除非再次订阅，否则将不会从您的品牌接收通信。

要检查相应用户档案的选择是否已更新，请转到 Experience Platform，并通过选择身份命名空间和相应的身份值访问该用户档案。在 [Experience Platform 文档](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hans#getting-started){target=&quot;_blank&quot;}中了解更多信息。

![](assets/lp_opt-out-profile-choice.png)

在 **[!UICONTROL 属性]** 选项卡，您可以看到 **[!UICONTROL 选择]** 已更改为 **[!UICONTROL 否]**.

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../privacy/opt-out.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../privacy/opt-out.md#unsubscribe-header)

////////


## Leverage landing page submission event {#leverage-lp-event}

You can use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.

To do this, you need to create an event containing the landing page submission information and use it in a journey. Follow the steps below.

1. Go to **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**, and in the **[!UICONTROL Events]** section, select **[!UICONTROL Manage]**.

    ![](assets/lp_subscription-uc-configurations.png)

1. The list of events displays. Select **[!UICONTROL Create Event]**.

    ![](assets/lp_subscription-uc-create-event.png)

1. The event configuration pane opens on the right side of the screen. Configure a rule-based unitary event. [Learn more](../event/about-creating.md)

1. Define the schema: select **[!UICONTROL AJO Email Tracking Experience Event Schema v.1]** (available by default in [!DNL Journey Optimizer]).

    ![](assets/lp_subscription-uc-event-schema.png)

1. In the **[!UICONTROL Fields]** section, select the following elements:

    * **[!UICONTROL _experience]** > **[!UICONTROL customerJourneyManagement]** > **[!UICONTROL messageInteraction]** > **[!UICONTROL Interaction Type]**
    
    * **[!UICONTROL _experience]** > **[!UICONTROL customerJourneyManagement]** > **[!UICONTROL messageInteraction]** > **[!UICONTROL Landing Page Details]** > **[!UICONTROL Landing Page ID]**

    ![](assets/lp_subscription-uc-event-fields.png)

1. Click inside the **[!UICONTROL Event ID condition]** field. Using the simple expression editor, define the condition for the **[!UICONTROL Interaction Type]** and **[!UICONTROL Landing Page ID]** fields. This will be used by the system to identify the events that will trigger your journey.

    ![](assets/lp_subscription-uc-event-id-condition.png)

    >[!NOTE]
    >
    >To find the landing page ID, you can insert the landing page as a link into an email and select the source code from the contextual toolbar to display the landing page information.
    >
    >![](assets/lp_subscription-uc-lp-id.png)

1. Save your changes.

1. Create a [journey](../building-journeys/journey.md). You can do it directly from the landing page by clicking the **[!UICONTROL Create journey]** button. Learn more [here](create-lp.md#configure-primary-page)

    ![](assets/lp_subscription-uc-event-create-journey.png)

1. In the journey, unfold the **[!UICONTROL Events]** category and drop the event that you created into the canvas. Learn more [here](../building-journeys/segment-qualification-events.md)

    ![](assets/lp_subscription-uc-journey-event.png)

1. Unfold the **[!UICONTROL Actions]** category and drop an email action into the canvas.

    ![](assets/lp_subscription-uc-journey-email.png)

///How do you use the information from the event to send an email to the users? -->
