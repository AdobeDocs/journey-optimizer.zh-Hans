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
source-git-commit: bf4044bc23b0e7c0ef74e5b612d93cb45ec20242
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 13%

---

# 与 Adobe Campaign v7/v8 集成 {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Adobe Campaign v7/v8 操作"
>abstract="此集成可用于 Adobe Campaign v7 和 v8。通过它，可使用 Adobe Campaign 交易型消息传递功能发送电子邮件、推送通知和短信。Journey Optimizer 实例和 Campaign 实例之间的连接在配置时由 Adobe 设置。"

如果您拥有Adobe Campaign Classic v7或Campaign v8，则可在您的历程中使用特定的自定义操作来集成Adobe Journey Optimizer和Adobe Campaign。 利用此集成，可使用Adobe Campaign事务性消息传送功能发送电子邮件、推送通知和短信。 在此[端到端用例](../building-journeys/ajo-ac.md)中了解详情。

对于所配置的每个操作，历程设计器面板中均提供[促销活动操作活动](../building-journeys/using-adobe-campaign-v7-v8.md)。

## 激活 {#access}

在请求时，Journey Optimizer和Adobe Campaign环境之间的连接是在配置时通过Adobe设置的。 如果您在配置时未请求连接，请联系Adobe Journey Optimizer支持以请求激活。 您必须提供以下详细信息：

>[!BEGINTABS]
>[!TAB 用于Adobe Journey Optimizer的] 

* Organization ID (Adobe OrgID)

* 沙盒名称

>[!TAB 用于Adobe Campaign的] 

* 营销活动服务器URL

* 实时服务器URL

* Campaign 版本

>[!ENDTABS]


## 重要说明 {#important-notes}

* 消息不受限制。 根据当前的Campaign SLA，系统会将每5分钟可发送超过4000条消息的数量限制在4000条以上。 因此，Journey Optimizer只应在单一用例（单个事件，而不是受众）中使用。

* 您需要在要使用的每个模板的画布上配置一个操作。 您需要在Journey Optimizer中为要从Adobe Campaign使用的每个模板配置一个操作。

* 我们建议您使用为此集成托管的专用消息中心实例，以避免影响您可能正在执行的任何其他Campaign操作。 营销服务器可以托管，也可以内部部署。 所需的版本是21.1版本候选版本或更高版本。

* 无法验证有效负载或Campaign消息是否正确。

* Campaign操作不能与受众资格事件一起使用。

## 先决条件 {#prerequisites}

在Adobe Campaign中，必须创建并发布事务型消息及其关联的事件。 请参阅[Adobe Campaign文档](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/send/real-time/transactional){target="_blank"}。

您可以按照以下模式构建与每条消息对应的JSON有效负载。 然后，在Journey Optimizer中配置操作时，您会粘贴此有效负载（请参阅下文）。

示例如下：

```JSON
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

## 配置操作 {#configure-action}

在Journey Optimizer中，必须为每个事务型消息配置一个操作。 执行以下步骤：

1. 创建新操作。 [了解有关自定义操作的更多信息](../action/action.md)。
1. 输入名称和说明。
1. 在&#x200B;**操作类型**&#x200B;字段中，选择&#x200B;**Adobe Campaign Classic**。
1. 单击&#x200B;**有效负载**&#x200B;字段，并粘贴与营销活动消息对应的JSON有效负载示例。 联系Adobe以获取此有效负载。
1. 根据您想要在历程画布上映射这些字段，可以将这些字段调整为静态或变量。 某些字段，例如电子邮件地址和个性化字段(ctx)的渠道参数，您可能希望定义为要在历程上下文中映射的变量。
1. 单击&#x200B;**保存**。

![](assets/accintegration1.png)