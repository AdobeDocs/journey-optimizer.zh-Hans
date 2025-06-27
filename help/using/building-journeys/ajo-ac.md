---
solution: Journey Optimizer
product: journey optimizer
title: 使用 Campaign v7/v8 发送消息
description: 了解如何使用Campaign v7/v8发送消息
feature: Journeys, Integrations, Custom Actions, Use Cases
topic: Administration
role: Admin, Data Engineer, User
level: Intermediate, Experienced
keywords: 历程，消息，营销活动，集成
exl-id: b07feb98-b2ae-476c-8fcb-873b308176f0
source-git-commit: 824cbf12502f0a52e27636dddee38cb7dee94bf4
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 2%

---

# 使用Campaign v7/v8发送消息 {#campaign-v7-v8-use-case}

此用例说明了使用与Adobe Campaign v7和Adobe Campaign v8的集成发送电子邮件所需的所有步骤。

>[!NOTE]
>
>要使用此集成，您必须具有Campaign v7/v8内部版本9125或更高版本。

首先，在Campaign中创建事务性电子邮件模板。 然后，在Journey Optimizer中创建事件、操作并设计旅程。

要了解有关Campaign集成的更多信息，请参阅以下页面：

* [创建营销活动操作](../action/acc-action.md)
* [在历程中使用操作](../building-journeys/using-adobe-campaign-v7-v8.md)。

**Adobe Campaign**

必须为此集成配置您的Campaign实例。 必须配置事务性消息传递功能。

1. 登录到Campaign控制实例。

1. 在&#x200B;**管理** > **平台** > **枚举**&#x200B;下，选择&#x200B;**事件类型** (eventType)枚举。 创建新的事件类型（在我们的示例中为“journey-event”）。 在稍后写入JSON文件时使用事件类型的内部名称。

   ![](assets/accintegration-uc-1.png)

1. 断开并重新连接到实例，以使创建生效。

1. 在&#x200B;**消息中心** > **事务性消息模板**&#x200B;下，根据之前创建的事件类型创建新的电子邮件模板。

   ![](assets/accintegration-uc-2.png)

1. 设计您的模板。 在此示例中，个性化应用于用户档案的名字和订单号。 名字在Adobe Experience Platform数据源中，订单号是Journey Optimizer事件中的字段。 确保在Campaign中使用正确的字段名称。

   ![](assets/accintegration-uc-3.png)

1. 发布事务型模板。

   ![](assets/accintegration-uc-4.png)

1. 编写与模板对应的JSON有效负载。

```
{
     "channel": "email",
     "eventType": "journey-event",
     "email": "Email address",
     "ctx": {
          "firstName": "First name", "purchaseOrderNumber": "Purchase order number"
     }
}
```

* 对于渠道，您需要键入“email”。
* 对于eventType，使用之前创建的事件类型的内部名称。
* 电子邮件地址将是一个变量，因此您可以键入任何标签。
* 在ctx下，个性化字段也是变量。

**Journey Optimizer**

1. 创建一个事件。 包括“purchaseOrderNumber”字段。

   ![](assets/accintegration-uc-5.png)

1. 在Journey Optimizer中创建与活动模板对应的操作。 在&#x200B;**操作类型**&#x200B;下拉列表中，选择&#x200B;**Adobe Campaign Classic**。

   ![](assets/accintegration-uc-6.png)

1. 单击&#x200B;**有效负载字段**&#x200B;并粘贴之前创建的JSON。

   ![](assets/accintegration-uc-7.png)

1. 对于电子邮件地址和两个个性化字段，请将&#x200B;**常量**&#x200B;更改为&#x200B;**变量**。

   ![](assets/accintegration-uc-8.png)

1. 现在，创建一个新历程，并从之前创建的事件开始。

   ![](assets/accintegration-uc-9.png)

1. 添加操作并将每个字段映射到Journey Optimizer中的正确字段。

   ![](assets/accintegration-uc-10.png)

1. 测试您的历程。

   ![](assets/accintegration-uc-11.png)

1. 您现在可以发布历程。
