---
solution: Journey Optimizer
product: journey optimizer
title: 使用 API 触发营销活动
description: 了解如何使用Journey Optimizer API触发营销活动
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 营销活动， API触发， REST，优化器，消息
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 2%

---

# 使用 API 触发营销活动 {#trigger-campaigns}

## 关于API触发的营销活动 {#about}

通过[!DNL Journey Optimizer]，您可以使用[交互式消息执行REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)创建营销活动，然后基于用户触发器从外部系统执行这些营销活动。 这允许您满足各种营销和事务性消息传递需求，如密码重置、OTP令牌等。

为此，您首先需要在Journey Optimizer中创建一个API触发的营销活动，然后通过API调用启动其执行。

![](../rn/assets/do-not-localize/api-triggered.gif)

API触发的营销活动的可用渠道包括电子邮件、短信和推送消息。

>[!NOTE]
>
>截至目前，推送通知API触发的营销活动不支持快速传递模式。

➡️ [在视频中了解此功能](#video)

## 创建API触发的营销活动 {#create}

### 配置和激活营销活动 {#create-activate}

要创建API触发的营销活动，请执行以下步骤。 有关如何创建营销活动的详细信息，请参阅[此部分](create-campaign.md)。

1. 使用&#x200B;**[!UICONTROL API触发的]**&#x200B;类型创建新营销活动。

1. 根据要发送的通信类型，选择&#x200B;**[!UICONTROL 营销]**&#x200B;或&#x200B;**[!UICONTROL 事务型]**&#x200B;类别。

1. 选择要用于发送消息的支持的渠道和相关渠道配置之一，然后单击“**[!UICONTROL 创建]**”。

   ![](assets/api-triggered-type.png)

1. 指定营销活动的标题和描述，然后单击&#x200B;**[!UICONTROL 编辑内容]**&#x200B;以配置要发送的消息。

   >[!NOTE]
   >
   >您可以将其他数据传递到API有效负荷，以利用这些数据将消息个性化。 [了解详情](#contextual)
   >
   >在内容中使用大量或繁重的上下文数据可能会影响性能。

1. 在&#x200B;**[!UICONTROL 受众]**&#x200B;部分中，指定要用于识别个人的命名空间。

   * 如果要创建&#x200B;**事务型**&#x200B;营销活动，则需要在API调用中定义定向的用户档案。 通过&#x200B;**[!UICONTROL 创建新配置文件]**&#x200B;选项，可自动创建数据库中不存在的配置文件。 [了解有关活动执行时创建用户档案的更多信息](#profile-creation)

     >[!NOTE]
     >
     >单个API调用最多支持20个唯一收件人。 每个收件人必须具有唯一的用户ID，不允许存在重复的用户ID。 请参阅[交互式消息执行API文档](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution/operation/postIMUnitaryMessageExecution){target="_blank"}以了解详情

   * 对于&#x200B;**营销**&#x200B;类型的营销活动，单击&#x200B;**[!UICONTROL 受众]**&#x200B;按钮以选择要定位的受众。

1. 配置营销活动的开始和结束日期。

   如果您为营销活动配置特定的开始和/或结束日期，则它不会在这些日期之外执行，并且如果营销活动由API触发，则API调用将失败。

1. 单击&#x200B;**[!UICONTROL 查看以激活]**&#x200B;以检查营销活动是否正确配置，然后激活它。

现在，您可以从API执行营销活动了。 [了解详情](#execute)

### 执行营销活动 {#execute}

激活营销活动后，您需要检索生成的示例cURL请求，并将其用于API中以构建有效负载并触发营销活动。

1. 打开营销活动，然后从&#x200B;**[!UICONTROL cURL请求]**&#x200B;部分复制并粘贴有效负载请求。 此有效负载包含消息中使用的所有个性化（用户档案和上下文）变量。 活动开始后，即可使用该功能。

   ![](assets/api-triggered-curl.png)

1. 将此cURL请求用到API中以构建有效负载并触发营销活动。 有关详细信息，请参阅[交互式消息执行API文档](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)。


   [此页面](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/)上也提供了API调用示例。

   >[!NOTE]
   >
   >如果您在创建营销活动时配置了特定的开始和/或结束日期，则它不会在这些日期之外执行，并且API调用将失败。

## 在API触发的营销活动中使用上下文属性 {#contextual}

借助API触发的营销活动，您可以在API有效载荷中传递其他数据，并在营销活动中使用这些数据来对消息进行个性化。

让我们举一个例子，客户希望重置密码，而您希望向他们发送一个在第三方工具中生成的密码重置URL。 借助API触发的营销活动，您可以将此生成的URL传递到API有效负荷中，并将其用于营销活动以将其添加到消息中。

>[!NOTE]
>
>与启用配置文件的事件不同，在REST API中传递的上下文数据用于一次性通信，而不是针对配置文件进行存储。 创建的配置文件最多包含命名空间详细信息（如果发现缺少该配置文件）。

要在营销活动中使用这些数据，您需要将这些数据传递到API有效负荷，并使用个性化编辑器将其添加到消息中。 为此，请使用`{{context.<contextualAttribute>}}`语法，其中`<contextualAttribute>`应与包含要传递的数据的API有效负载中的变量名称匹配。

`{{context.<contextualAttribute>}}`语法仅映射到String数据类型。

![](assets/api-triggered-context.png)


>[!IMPORTANT]
>
>传递到请求的上下文属性不能超过200kb，并且始终被视为字符串类型。
>
>`context.system`语法限制为仅供Adobe内部使用，不应用于传递上下文属性。

请注意，目前没有上下文属性可用于左边栏菜单。 属性必须直接在个性化表达式中键入，[!DNL Journey Optimizer]不执行任何检查。

## 活动执行时创建用户档案 {#profile-creation}

在某些情况下，您可能需要将事务型消息发送到系统中不存在的用户档案。 例如，如果未知用户尝试在您的网站上重置密码。

当数据库中不存在某个用户档案时，可使用Journey Optimizer在执行活动时自动创建该用户档案，以允许将消息发送到此用户档案。

>[!IMPORTANT]
>
>在事务型消息中，此功能用于在大容量事务型发送用例中创建&#x200B;**小容量用户档案**，其中大量的用户档案已存在于Platform中。

要在营销活动执行时激活用户档案创建，请在&#x200B;**[!UICONTROL 受众]**&#x200B;部分中将&#x200B;**[!UICONTROL 创建新用户档案]**&#x200B;选项切换为on。 如果禁用此选项，则任何发送都将拒绝未知配置文件，并且API调用将失败。

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>在&#x200B;**AJO交互式消息传递配置文件数据集**&#x200B;数据集中，为每个出站渠道（电子邮件、短信和推送）分别在三个默认命名空间（电子邮件、电话和ECID）中创建未知配置文件。 但是，如果您使用自定义命名空间，则会使用相同的自定义命名空间创建身份。

## 操作方法视频 {#video}

了解如何使用交互式消息执行REST API，根据用户交互从外部系统创建并触发活动。

>[!VIDEO](https://video.tv.adobe.com/v/3452735?quality=12&captions=chi_hans)
