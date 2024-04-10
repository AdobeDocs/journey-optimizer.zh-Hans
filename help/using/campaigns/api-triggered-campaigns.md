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
source-git-commit: 352ffebda7eda2ceb54b0f5c3f6d3b577522191f
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 2%

---

# 使用 API 触发营销活动 {#trigger-campaigns}

## 关于API触发的营销活动 {#about}

替换为 [!DNL Journey Optimizer]，您可以创建营销策划，然后使用根据用户触发器从外部系统调用它们。 [交互式消息执行REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). 这允许您满足各种营销和事务性消息传递需求，如密码重置、OTP令牌等。

为此，您首先需要在Journey Optimizer中创建一个API触发的营销活动，然后通过API调用启动其执行。

![](../rn/assets/do-not-localize/api-triggered.gif)

API触发的营销活动的可用渠道包括电子邮件、短信和推送消息。

>[!NOTE]
>
>截至目前，推送通知API触发的营销活动不支持快速传递模式。

➡️ [在视频中了解此功能](#video)

## 创建API触发的营销活动 {#create}

### 配置和激活营销活动 {#create-activate}

要创建API触发的营销活动，请执行以下步骤。 有关如何创建营销活动的详细信息，请参阅 [本节](create-campaign.md).

1. 使用创建新营销活动 **[!UICONTROL API触发]** 类型。

1. 选择 **[!UICONTROL 营销]** 或 **[!UICONTROL 事务性]** 类别，具体取决于您要发送的通信类型。

1. 选择一个受支持的渠道和关联的渠道表面来用于发送消息，然后单击 **[!UICONTROL 创建]**.

   ![](assets/api-triggered-type.png)

1. 指定营销活动的标题和描述，然后单击 **[!UICONTROL 编辑内容]** 以配置要发送的消息。

   >[!NOTE]
   >
   >您可以将其他数据传递到API有效负荷，以利用这些数据将消息个性化。 [了解详情](#contextual)
   >
   >在内容中使用大量或繁重的上下文数据可能会影响性能。

1. 在 **[!UICONTROL 受众]** 部分，指定用于识别个人的命名空间。

   * 如果您要创建 **事务性**-type营销活动，则需要在API调用中定义目标用户档案。 此 **[!UICONTROL 创建新配置文件]** 选项允许您自动创建数据库中不存在的配置文件。 [了解有关活动执行时用户档案创建的更多信息](#profile-creation)

   * 对象 **营销**-type campaigns，单击 **[!UICONTROL 受众]** 按钮以选择要定位的受众。

1. 配置营销活动的开始和结束日期。

   如果您为营销活动配置特定的开始和/或结束日期，则它不会在这些日期之外执行，并且如果营销活动由API触发，则API调用将失败。

1. 单击 **[!UICONTROL 审查以激活]** 检查营销活动是否正确配置，然后激活它。

现在，您可以从API执行营销活动了。 [了解详情](#execute)

### 执行营销活动 {#execute}

激活营销活动后，您需要检索生成的示例cURL请求，并将其用于API中以构建有效负载并触发营销活动。

1. 打开营销活动，然后从复制并粘贴有效负载请求 **[!UICONTROL cURL请求]** 部分。 此有效负载包含消息中使用的所有个性化（用户档案和上下文）变量。 活动开始后，即可使用该功能。

   ![](assets/api-triggered-curl.png)

1. 将此cURL请求用到API中以构建有效负载并触发营销活动。 欲了解更多信息，请参见 [交互式消息执行API文档](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).


   中还提供了API调用示例 [此页面](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).

   >[!NOTE]
   >
   >如果您在创建营销活动时配置了特定的开始和/或结束日期，则它不会在这些日期之外执行，并且API调用将失败。

## 在API触发的营销活动中使用上下文属性 {#contextual}

借助API触发的营销活动，您可以在API有效载荷中传递其他数据，并在营销活动中使用这些数据来对消息进行个性化。

让我们举一个例子，客户希望重置密码，而您希望向他们发送一个在第三方工具中生成的密码重置URL。 借助API触发的营销活动，您可以将此生成的URL传递到API有效负荷中，并将其用于营销活动以将其添加到消息中。

>[!NOTE]
>
>与启用配置文件的事件不同，在REST API中传递的上下文数据用于一次性通信，而不是针对配置文件进行存储。 创建的配置文件最多包含命名空间详细信息（如果发现缺少该配置文件）。

要在营销策划中使用这些数据，您需要将这些数据传递到API有效负荷中，并使用表达式编辑器将其添加到消息中。 要执行此操作，请使用 `{{context.<contextualAttribute>}}` 语法，其中 `<contextualAttribute>` 应与包含要传递的数据的API有效负载中的变量名称匹配。

此 `{{context.<contextualAttribute>}}` 语法仅映射到String数据类型。

![](assets/api-triggered-context.png)


>[!IMPORTANT]
>
>传递到请求的上下文属性不能超过50kb，并且始终被视为字符串类型。
>
>此 `context.system` 语法限制为仅供Adobe内部使用，并且不得用于传递上下文属性。

请注意，目前没有上下文属性可用于左边栏菜单。 必须在个性化表达式中直接键入属性，并且不执行任何检查 [!DNL Journey Optimizer].

## 活动执行时创建用户档案 {#profile-creation}

在某些情况下，您可能需要将事务型消息发送到系统中不存在的用户档案。 例如，如果未知用户尝试在您的网站上重置密码。

当数据库中不存在某个用户档案时，可使用Journey Optimizer在执行活动时自动创建该用户档案，以允许将消息发送到此用户档案。

>[!IMPORTANT]
>
>在事务型消息中，此功能是为提供的 **创建非常小的卷配置文件** 在大量事务性发送用例中，大量用户档案已存在于platform中。

要在活动执行时激活用户档案创建，请切换 **[!UICONTROL 创建新配置文件]** 中的选项 **[!UICONTROL 受众]** 部分。 如果禁用此选项，则任何发送都将拒绝未知配置文件，并且API调用将失败。

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>在中创建未知配置文件 **AJO交互式消息传递配置文件数据集** 数据集，分别位于每个出站渠道（电子邮件、短信和推送）的三个默认命名空间（电子邮件、电话和ECID）中。 但是，如果您使用自定义命名空间，则会使用相同的自定义命名空间创建身份。

## 操作方法视频 {#video}

了解如何使用交互式消息执行REST API，根据用户交互从外部系统创建并触发活动。

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)
