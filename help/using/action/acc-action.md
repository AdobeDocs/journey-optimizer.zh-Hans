---
title: 与 Adobe Campaign v7/v8 集成
description: 了解如何与Adobe Campaign v7/v8集成
feature: 操作
topic: 管理
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 5%

---

# 与 Adobe Campaign v7/v8 集成 {#integrating-with-adobe-campaign-classic}

此集成适用于从21.1版本开始的Adobe Campaign Classic v7和Adobe Campaign v8。 它允许您使用Adobe Campaign事务型消息传送功能发送电子邮件、推送通知和短信。

Journey Optimizer实例和Campaign实例之间的连接是在预配时Adobe设置的。

此[部分](../building-journeys/campaign-classic-use-case.md)中提供了端到端用例。

对于配置的每个操作，历程设计器面板中都提供了一个操作活动。 请参阅此[部分](../building-journeys/using-adobe-campaign-classic.md)。

## 重要说明

* 没有消息限制。 根据我们当前的促销活动SLA，我们将可发送的消息数量限制为50,000/小时。 因此，Journey Optimizer只应用于单一用例（单个事件，而不是区段）。

* 您需要在每个要使用的模板的画布上配置一个操作。 您需要在Journey Optimizer中为要从Adobe Campaign使用的每个模板配置一个操作。

* 我们建议您使用为此集成托管的专用消息中心实例，以避免影响您可能正在进行的任何其他Campaign操作。 营销服务器可以是托管的，也可以是内部部署的。 所需的内部版本为21.1发行候选版本或更高版本。

* 没有验证有效负载或Campaign消息是否正确。

* 您不能将促销活动操作与区段鉴别事件结合使用。

## 先决条件

在Campaign中，您需要创建并发布事务型消息及其关联事件。 请参阅[Adobe Campaign文档](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target=&quot;_blank&quot;}。

您可以按照以下模式构建与每个消息对应的JSON有效负载。 然后，在Journey Orchestration中配置操作时，您将粘贴此有效负载（请参阅下文）

示例如下：

```
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **渠道**:为营销活动事务型模板定义的渠道
* **eventType**:营销活动事件的内部名称
* **ctx**:变量。

## 配置操作

在Journey Optimizer中，您需要为每个事务型消息配置一个操作。 请执行以下步骤：

1. 创建新操作。 请参阅此[部分](../action/action.md)。
1. 输入名称和描述。
1. 在&#x200B;**Action type**&#x200B;字段中，选择&#x200B;**Adobe Campaign Classic**。
1. 单击&#x200B;**有效负荷**&#x200B;字段，并粘贴与Campaign消息对应的JSON有效负荷示例。 联系Adobe以获取此有效负载。
1. 根据要在历程画布上映射不同字段，将其调整为静态字段或变量字段。 某些字段(例如电子邮件地址和个性化字段(ctx)的渠道参数)，您可能希望定义为用于在历程上下文中映射的变量。
1. 单击&#x200B;**保存**。

![](../assets/accintegration1.png)


