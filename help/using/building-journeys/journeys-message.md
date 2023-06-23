---
solution: Journey Optimizer
product: journey optimizer
title: 在历程中添加消息
description: 了解如何在历程中添加消息
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 历程，消息，推送，短信，电子邮件，应用程序内
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 1cf62f949c1309b864ccd352059a444fd7bd07f0
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 23%

---

# 电子邮件、应用程序内消息、推送、短信{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] 附带内置消息功能。 您只需在历程中添加推送、短信、应用程序内或电子邮件消息活动，并定义设置和内容即可。 然后，将在历程的上下文中执行并发送它。

您还可以设置发送消息的特定操作：

* 如果您使用第三方系统来发送消息，则可以创建自定义操作。 在本节中了解详情 [部分](../action/action.md).

* 如果您使用的是Campaign和Journey Optimizer，请参阅以下章节：

   * [[!DNL Journey Optimizer] 和Campaign Classicv7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] 和Campaign Standard](../action/acs-action.md)

要在历程中添加消息，请执行以下步骤：

1. 通过[事件](general-events.md)或[读取区段](read-segment.md)活动开始您的历程。

1. 从 **操作** 部分，拖放 **电子邮件**，和 **应用程序内**，和 **短信** 或 **推送** 活动移入画布。

1. 配置活动。 在以下页面中了解创建消息内容的详细步骤：

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
   <a href="../in-app/create-in-app.md">
   <img alt="潜在客户" src="../assets/do-not-localize/in-app.jpg">
   </a>
   <div><a href="../in-app/create-in-app.md"><strong>创建应用程序内消息</strong>
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
   <a href="../sms/create-sms.md"><strong>创建短信消息</strong></a>
   </div>
   <p>
   </td>
   </tr>
   </table>

## 更新实时内容{#update-live-content}

您可以在实时历程中更新消息的内容（电子邮件、应用程序内、推送、短信）。

为此，请打开您的实时历程，选择消息活动并单击 **编辑内容**.

![](assets/add-a-message2.png)

但是，您无法更改个性化中使用的属性，无论这些属性是配置文件属性还是上下文数据（来自事件或历程属性）。

如果修改了上下文数据，将显示以下错误消息：ERR_AUTHORING_JOURNEYVERSION_201

如果修改了配置文件属性，将显示以下错误消息：ERR_AUTHORING_JOURNEYVERSION_202

请注意，对于应用程序内活动，可以在历程处于实时状态时对内容进行任何更改，但无法修改应用程序内触发器。

## 发送时间优化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="关于发送时间优化"
>abstract="Adobe Journey Optimizer 的发送时间优化功能由 Adobe 的 AI 服务提供支持，可以预测发送电子邮件或推送消息的最佳时间，从而根据历史打开率和点击率最大限度地提高参与度。"

### 关于发送时间优化 {#about-send-time}

Adobe Journey Optimizer 的发送时间优化功能由 Adobe 的 AI 服务提供支持，可以预测发送电子邮件或推送消息的最佳时间，从而根据历史打开率和点击率最大限度地提高参与度。使用我们的机器学习模型安排每个用户的个性化发送时间，以提高消息的打开率和点击率。

发送时间优化模型会摄取您的Adobe Journey Optimizer数据，并查看用户级别的打开（针对电子邮件和推送）和点击（针对电子邮件）率，以确定客户何时最有可能参与您的消息传送。 发送时间优化需要至少一个月的消息跟踪数据才能提出有根据的建议。 对于每个用户，系统将使用以下得分自动选择最佳时间：

* 一周中每天的最佳时刻以最大限度地提高参与度
* 一周中最佳的一天，可最大限度地提高参与度
* 一周中最佳一天中最佳的一小时，最大化参与度

无论您是在说得分还是训练，模型都有所不同。 培训最初每周进行，然后每季度进行。 评分最初为每周，然后是每月。

* 训练 — 用于生成得分的算法的开发
* 评分 — 根据经过训练的模型，将评分应用于个人资料

此信息存储在用户的配置文件中，并在历程执行中引用，以告知Adobe Journey Optimizer何时发送消息。

### 激活发送时间优化{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="激活发送时间优化"
>abstract="通过选择相应的单选按钮，选择是针对电子邮件打开操作还是针对电子邮件点进操作进行优化。您还可以为“发送于下一个”选项输入一个值，选择限定系统使用的发送时间。"

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="激活发送时间优化"
>abstract="推送消息默认为打开选项，因为点击不适用于推送消息。 您还可以为“发送于下一个”选项输入一个值，选择限定系统使用的发送时间。"

通过选择电子邮件或推送消息的 **发送时间优化** 切换活动参数。

![](../building-journeys/assets/jo-message5.png)

对于电子邮件，通过选择相应的单选按钮来选择是优化电子邮件打开次数，还是优化电子邮件点进次数。 推送消息默认为打开选项，因为点击不适用于推送消息。 

您还可以通过为输入一个值，选择将系统使用的发送时间包括在内。 **发送于下一个** 选项。 如果你选择“六小时”作为值， [!DNL Journey Optimizer] 将检查每个用户配置文件，并在旅程执行时间后的6小时内选择最佳发送时间。

**如果最佳时间在窗口之外，会发生什么情况？**

让我们以以下设置为例：

* 优化点击次数
* 操作定于上午10点开始
* 窗口为3小时

用户档案可以有一个最佳打开时间，该时间位于窗口之外。 例如，John的最佳点击打开时间是下午5点。

在用户档案级别，每周的每个小时都有分数。 在此示例中，电子邮件将始终在窗口中发送。 在运行时，系统会检查该时段（从上午10点开始的3小时时段）内的分数列表。 然后，系统比较10、11和中午的分数，并选择最高分。 此时会发送电子邮件。
