---
solution: Journey Optimizer
product: journey optimizer
title: 与 Adobe Campaign v7/v8 集成
description: 了解如何将Journey Optimizer与Adobe Campaign v7/v8集成
feature: Actions
topic: Administration
role: Admin,Developer
level: Intermediate
keywords: campaign， acc，集成
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: 417eea2a52d4fb38ae96cf74f90658f87694be5a
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 22%

---

# 与 Adobe Campaign v7/v8 集成 {#integrating-with-adobe-campaign-classic}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Adobe Campaign v7/v8 操作"
>abstract="此集成可用于 Adobe Campaign Classic v7 和 v8。它让您可以使用 Adobe Campaign 事务性消息传递功能发送电子邮件、推送通知和短信。Journey Optimizer 实例和 Campaign 实例之间的连接在配置时由 Adobe 设置。"

此集成适用于Adobe Campaign Classic v7（从7.1版本开始）和Adobe Campaign v8。 它让您可以使用 Adobe Campaign 事务性消息传递功能发送电子邮件、推送通知和短信。

Journey Optimizer 实例和 Campaign 实例之间的连接在配置时由 Adobe 设置。

本中介绍了端到端用例 [部分](../building-journeys/ajo-ac.md).

对于配置的每个操作，历程设计器面板中都提供了一个操作活动。 请参阅此[章节](../building-journeys/using-adobe-campaign-classic.md)。

## 重要说明 {#important-notes}

* 消息不受限制。 系统根据当前Campaign SLA，将每5分钟可发送的消息数量限制为4000条。 因此，Journey Optimizer应仅用于单一用例（单个事件，而不是受众）。

* 您需要在要使用的每个模板的画布上配置一个操作。 您需要在Journey Optimizer中为要从Adobe Campaign使用的每个模板配置一个操作。

* 我们建议您使用为此集成托管的专用消息中心实例，以避免影响您可能执行的任何其他Campaign操作。 营销服务器可以托管，也可以内部部署。 所需的版本是21.1版本候选版本或更高版本。

* 无法验证有效负载或Campaign消息是否正确。

* 您不能将Campaign操作与受众资格事件一起使用。

## 先决条件 {#prerequisites}

在Campaign中，您需要创建和发布事务型消息及其关联的事件。 请参阅 [Adobe Campaign文档](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target="_blank"}.

您可以按照以下模式构建与每条消息对应的JSON有效负载。 然后，在Journey Optimizer中配置操作时，您会粘贴此有效负载（请参阅下文）

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

* **渠道**：为Campaign事务模板定义的渠道
* **事件类型**：Campaign事件的内部名称
* **ctx**：变量基于您在消息中拥有的个性化设置。

## 配置操作 {#configure-action}

在Journey Optimizer中，您需要为每个事务型消息配置一个操作。 执行以下步骤：

1. 创建新操作。 请参阅此[章节](../action/action.md)。
1. 输入名称和说明。
1. 在 **操作类型** 字段，选择 **Adobe Campaign Classic**.
1. 单击 **有效负荷** 字段，并粘贴与Campaign消息对应的JSON有效负载示例。 联系Adobe以获取此有效负载。
1. 根据您想要在历程画布上映射这些字段，可将这些字段调整为静态或变量。 某些字段，例如电子邮件地址和个性化字段(ctx)的渠道参数，您可能需要定义为在历程上下文中映射的变量。
1. 单击&#x200B;**保存**。

![](assets/accintegration1.png)