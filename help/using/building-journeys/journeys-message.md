---
solution: Journey Optimizer
product: journey optimizer
title: 在历程中添加消息
description: 了解如何在历程中添加消息
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# 电子邮件、短信、推送{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] 附带内置消息功能。 您只需在历程中添加推送、短信或电子邮件活动，并定义设置和内容即可。 然后，在历程的上下文中执行并发送该事件。

您还可以设置特定操作以发送消息：

* 如果您使用第三方系统发送消息，则可以创建自定义操作。 在中了解详情 [部分](../action/action.md).

* 如果您使用的是Campaign和Journey Optimizer，请参阅以下章节：

   * [[!DNL Journey Optimizer] 和Campaign Classic v7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] 和Campaign Standard](../action/acs-action.md)

要在历程中添加消息，请执行以下步骤：

1. 通过 [事件](general-events.md) 或 [读取区段](read-segment.md) 活动。

1. 从 **操作** ，拖放 **电子邮件**, **短信** 或 **推送** 活动。

1. 配置活动。 了解在以下页面中创建消息内容的详细步骤：

   <table style="table-layout:fixed">
   <tr style="border: 0;">
   <td>
   <a href="../email/create-email.md">
   <img alt="商机" src="../assets/do-not-localize/email.jpg">
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
   <a href="../sms/create-sms.md"><strong>创建短信消息</strong></a>
   </div>
   <p>
   </td>
   </tr>
   </table>

## 更新实时内容{#update-live-content}

您可以更新实时历程中消息的内容（电子邮件、短信、推送）。

为此，请打开您的实时历程，选择消息活动并单击 **编辑内容**.

![](assets/add-a-message2.png)

但是，您无法更改个性化中使用的属性，无论这些属性是用户档案属性还是上下文数据（来自事件或历程属性）。

## 发送时间优化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="关于发送时间优化"
>abstract="Adobe Journey Optimizer的“发送时间优化”功能由Adobe的AI服务提供支持，该功能可以根据历史打开率和点击率预测发送电子邮件或推送消息以最大化参与度的最佳时间。"

### 关于发送时间优化 {#about-send-time}

Adobe Journey Optimizer的“发送时间优化”功能由Adobe的AI服务提供支持，该功能可以根据历史打开率和点击率预测发送电子邮件或推送消息以最大化参与度的最佳时间。 使用我们的机器学习模型为每个用户安排个性化发送时间，以提高消息的打开率和点击率。

发送时间优化模型可摄取您的Adobe Journey Optimizer数据，并查看用户级别的打开（用于电子邮件和推送）和点击（用于电子邮件）率，以确定客户何时最可能参与您的消息传送。 发送时间优化需要至少一个月的消息跟踪数据才能做出明智的建议。 对于每个用户，系统将使用以下分数自动选择最佳时间：

* 一周中每天的最佳时刻，以最大限度地提高参与度
* 一周中最好的一天，以最大程度地提高参与度
* 一周中最佳时刻的最佳时刻，以最大限度地提高参与度

无论您是在说打分还是培训，模型都会有所不同。 培训最初每周进行，然后每季度进行。 评分最初是每周，然后是每月。

* 培训 — 用于打分的算法的开发
* 评分 — 根据训练好的模型将评分应用于个人用户档案

此信息与用户的配置文件一起存储，并在历程执行时被引用，以告知Adobe Journey Optimizer何时发送您的消息。

>[!CAUTION]
>
>此功能与拆分模式不兼容。

### 激活发送时间优化{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="激活发送时间优化"
>abstract="通过选择相应的单选按钮，选择是优化电子邮件打开次数还是电子邮件点进次数。 您还可以通过在下一个选项中为“发送”输入值，将系统使用的发送时间括起来。"

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="激活发送时间优化"
>abstract="推送消息默认为打开选项，因为点击不适用于推送消息。 您还可以通过在下一个选项中为“发送”输入值，将系统使用的发送时间括起来。"

通过选择 **发送时间优化** 从活动参数切换。

![](../building-journeys/assets/jo-message5.png)

对于电子邮件消息，选择是优化电子邮件打开次数，还是通过选择相应的单选按钮来优化电子邮件点进次数。 推送消息默认为打开选项，因为点击不适用于推送消息。

您还可以通过为 **在下一个** 选项。 如果选择“6小时”作为值， [!DNL Journey Optimizer] 将检查每个用户配置文件，并在历程执行时间后的六小时内选取最佳发送时间。
