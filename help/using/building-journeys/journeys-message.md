---
solution: Journey Optimizer
product: journey optimizer
title: 将内置渠道操作添加到历程
description: 了解如何将内置渠道操作添加到历程
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: 历程，消息，推送，短信，电子邮件，应用程序内， Web，内容卡，基于代码的体验
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: db3c87d10469550eb30224c932344ff1e3ae1767
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 18%

---

# 使用内置渠道操作 {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="内置渠道操作"
>abstract="Journey Optimizer 附带内置操作功能。您只需在历程中添加一条消息（电子邮件、短信（SMS/MMS）、推送）或入站体验（应用程序内、网页、基于代码的体验、信息卡）活动，并定义设置和内容。然后将在历程的上下文中执行和发送它。"

[!DNL Journey Optimizer]具有内置渠道操作功能，用于发送消息：当用户档案进入此活动时，会向其发送消息。

要在历程中添加内置渠道操作，请拖放渠道活动，并定义其设置和内容。 然后将在历程的上下文中执行和发送它。

>[!NOTE]
>
>您还可以设置自定义操作，以在[!DNL Journey Optimizer]中发送消息。 [了解详情](#recommendation)

## 在历程中添加消息  {#add-msg-in-journey}

通过内置渠道操作，可配置出站或入站消息。 支持的入站渠道包括电子邮件、短信(SMS/MMS)和推送通知。 支持的出站渠道包括应用程序内、Web、基于代码的体验和内容卡片。

要将内置渠道操作添加到历程，请执行以下步骤。

1. 通过[事件](general-events.md)或[读取受众](read-audience.md)活动开始您的历程。

1. 从调色板的&#x200B;**操作**&#x200B;部分，将渠道活动拖放到画布中。

   ![](assets/journey-web-activity.png)


1. 配置您的活动。 详细配置指南可在以下链接中找到。

   * 了解创建叫客操作的详细步骤，如下所示：

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../email/create-email.md">
      <img alt="潜在客户" src="../assets/do-not-localize/email.jpg">
      </a>
      <div><a href="../email/create-email.md"><strong>创建电子邮件</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../push/create-push.md">
      <img alt="不频繁" src="../assets/do-not-localize/push.jpg">
      </a>
      <div>
      <a href="../push/create-push.md"><strong>创建推送通知<strong></a>
      </div>
      <p>
      </td>
      <td>
      <a href="../sms/create-sms.md">
      <img alt="验证" src="../assets/do-not-localize/sms.jpg">
      </a>
      <div>
      <a href="../sms/create-sms.md"><strong>创建短信(SMS/MMS)</strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

   * 了解创建集客操作的详细步骤，如下所示：

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../in-app/create-in-app.md">
      <img alt="潜在客户" src="../assets/do-not-localize/in-app.jpg">
      </a>
      <div><a href="../in-app/create-in-app.md"><strong>创建应用程序内消息</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../web/create-web.md">
      <img alt="潜在客户" src="../assets/do-not-localize/web-create.jpg">
      </a>
      <div><a href="../web/create-web.md"><strong>创建Web体验</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../content-card/create-content-card.md">
      <img alt="潜在客户" src="../assets/do-not-localize/sms-config.jpg">
      </a>
      <div><a href="../content-card/create-content-card.md"><strong>创建内容卡</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../code-based/create-code-based.md">
      <img alt="不频繁" src="../assets/do-not-localize/web-design.jpg">
      </a>
      <div>
      <a href="../code-based/create-code-based.md"><strong>创建基于代码的体验<strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

>[!NOTE]
>
>* 每个入站体验活动都附带3天&#x200B;**等待**&#x200B;活动。 [了解详情](wait-activity.md#auto-wait-node)
>
>* 对于电子邮件和推送通知，您可以启用发送时间优化。 [了解详情](send-time-optimization.md)



## 更新实时内容 {#update-live-content}

您可以在实时历程中更新内置渠道操作的内容。

为此，请打开您的实时历程，选择渠道活动，然后单击&#x200B;**编辑内容**。

![](assets/add-a-message2.png)

但是，您无法更改个性化中使用的属性，无论这些属性是配置文件属性还是上下文数据（来自事件或历程属性）。

如果您修改了上下文数据，则会显示以下错误消息： `ERR_AUTHORING_JOURNEYVERSION_201`

如果您修改了配置文件属性，将显示以下错误消息： `ERR_AUTHORING_JOURNEYVERSION_202`

请注意，对于应用程序内活动，可以在历程实时期间对内容进行任何更改，但无法修改应用程序内触发器。

## 通过自定义操作发送 {#recommendation}

您可以使用自定义操作配置第三方系统的连接，以发送消息或API调用，而不是使用内置的消息功能。

* 如果您使用第三方系统来发送消息，则可以创建自定义操作。 [了解详情](../action/action.md)

* 如果您在使用Adobe Campaign，请参阅以下章节：

   * [[!DNL Journey Optimizer]和Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer]和Campaign Standard](../action/acs-action.md)