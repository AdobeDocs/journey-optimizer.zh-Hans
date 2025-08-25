---
solution: Journey Optimizer
product: journey optimizer
title: 与 Adobe Campaign v7/v8 集成
description: 了解如何将Journey Optimizer与Adobe Campaign v7/v8集成
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: campaign， acc，集成
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: 60cb5e1ba2b5c8cfd0a306a589c85761be1cf657
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 12%

---

# 与 Adobe Campaign v7/v8 集成 {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Adobe Campaign v7/v8 操作"
>abstract="此集成可用于 Adobe Campaign v7 和 v8。通过它，可使用 Adobe Campaign 事务性消息传递功能发送电子邮件、推送通知和短信。Journey Optimizer 实例和 Campaign 实例之间的连接在配置时由 Adobe 设置。"

如果您拥有Adobe Campaign Classic v7或Campaign v8，则可在您的历程中使用特定的自定义操作来集成Adobe Journey Optimizer和Adobe Campaign。 利用此集成，可使用Adobe Campaign事务性消息传送功能发送电子邮件、推送通知和短信。 在此[端到端用例](../building-journeys/ajo-ac.md)中了解详情。

对于所配置的每个操作，历程设计器面板中均提供[促销活动操作活动](../building-journeys/using-adobe-campaign-v7-v8.md)。

## 激活 {#access}

在请求时，Journey Optimizer和Adobe Campaign环境之间的连接是在配置时通过Adobe设置的。 如果您在配置时未请求连接，请联系Adobe Journey Optimizer支持以请求激活。 您必须提供以下详细信息：

>[!BEGINTABS]

>用于Adobe Journey Optimizer的[!TAB ]

* Organization ID (Adobe OrgID)
* 沙盒名称

>用于Adobe Campaign的[!TAB ]

* 营销活动服务器URL
* 实时服务器URL
* 您的Adobe Campaign版本

>[!ENDTABS]


## 护栏和限制 {#important-notes}

* 消息不受限制。 根据当前的Campaign SLA，系统会将每5分钟可发送的消息数限制为4,000条。 因此，Journey Optimizer只应在单一用例（单个事件，而不是受众）中使用。

* 您必须在每个模板上为每个要使用的画布配置一个操作。 您需要在Journey Optimizer中为要从Adobe Campaign使用的每个模板配置一个操作。

* 我们建议您对此集成使用托管的专用消息中心或Managed Services实例，以避免影响您可能正在执行的任何其他Campaign操作。 营销服务器可以是托管服务器，也可以是内部部署服务器。<!--The build required is 21.1 Release Candidate or greater. -->

* 无法验证有效负载或Campaign消息是否正确。

* Campaign操作不能与受众资格事件一起使用。

## 先决条件 {#prerequisites}

在Adobe Campaign中，必须创建并发布事务型消息及其关联的事件。 请参阅[Adobe Campaign文档](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/send/real-time/transactional){target="_blank"}。

您可以按照以下模式构建与每条消息对应的JSON有效负载。 然后，在Journey Optimizer中配置操作时，您会粘贴此有效负载（请参阅下文）。

+++ 示例

```json
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **渠道**：为营销活动事务模板定义的渠道
* **eventType**： Campaign事件的内部名称
* **ctx**：基于您在消息中拥有的个性化设置的可变数

+++

## 配置操作 {#configure-action}

在Journey Optimizer中，必须为每个事务型消息配置一个操作。

要创建Campaign操作，请执行以下步骤：

1. 创建新操作。 [了解如何创建自定义操作](../action/action.md)。
1. 输入名称和说明。
1. 在&#x200B;**操作类型**&#x200B;字段中，选择&#x200B;**Adobe Campaign Classic**。
   ![](assets/accintegration1.png)
1. 单击&#x200B;**有效负载**&#x200B;字段，并粘贴与营销活动消息对应的JSON有效负载示例。 联系Adobe以获取此有效负载。
1. 根据您希望字段在历程画布上映射，将每个字段设置为静态字段还是变量。 例如，电子邮件渠道参数和个性化字段(`ctx`)等字段通常应设置为变量，以便能够在历程中动态调整。
1. 单击&#x200B;**保存**。

