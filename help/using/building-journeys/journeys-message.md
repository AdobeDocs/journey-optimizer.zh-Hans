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
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 18%

---

# 电子邮件、短信、推送{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] 附带内置消息功能。 您只需在历程中添加推送、短信或电子邮件活动，以及 [定义设置和内容](../messages/messages-in-journeys.md). 然后，在历程的上下文中执行并发送该事件。

您还可以设置特定操作以发送消息：

* 如果您使用第三方系统发送消息，则可以创建自定义操作。 在中了解详情 [部分](../action/action.md).

* 如果您使用的是Campaign和Journey Optimizer，请参阅以下章节：

   * [[!DNL Journey Optimizer] 和Campaign Classicv7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] 和Campaign Standard](../action/acs-action.md)

要在历程中添加消息，请执行以下步骤：

1. 通过[事件](general-events.md)或[读取区段](read-segment.md)活动开始您的历程。

1. 从调板的&#x200B;**操作**&#x200B;部分，拖放&#x200B;**电子邮件**、**短信**&#x200B;或&#x200B;**推送**&#x200B;活动到画布中。

   ![](../messages/assets/add-a-message.png)


   有关配置消息和定义其内容的所有步骤，请参见 [此部分](../messages/get-started-content.md).

## 更新实时内容{#update-live-content}

您可以更新实时历程中消息的内容（电子邮件、短信、推送）。

为此，请打开您的实时历程，选择消息活动并单击 **编辑内容**.

![](assets/add-a-message2.png)

但是，您无法更改个性化中使用的属性，无论这些属性是用户档案属性还是上下文数据（来自事件或历程属性）。
