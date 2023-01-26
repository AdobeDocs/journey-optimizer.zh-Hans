---
solution: Journey Optimizer
product: journey optimizer
title: 使用 API 触发活动
description: 了解如何使用Journey Optimizer API触发营销活动
topic: Content Management
role: Developer, Admin
level: Intermediate, Experienced
keywords: 促销活动， API触发， REST，优化程序，消息
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 3%

---

# 使用 API 触发活动 {#trigger-campaigns}

## 关于API触发的营销活动 {#about}

使用 [!DNL Journey Optimizer]，您可以创建营销活动，然后使用根据用户触发器从外部系统调用它们 [交互式消息执行REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). 这允许您满足各种操作和事务性消息传递需求，如密码重置、OTP 令牌等。

为此，您首先需要在Journey Optimizer中创建由API触发的营销活动，然后通过API调用启动其执行。

API触发的营销活动的可用渠道有电子邮件、短信和推送消息。

## 创建API触发的营销活动 {#create}

### 配置和激活营销活动 {#create-activate}

创建API触发的营销活动的过程与计划的营销活动相同，但受众选择在API有效负载中执行的情况除外。 有关如何创建营销活动的详细信息，请参阅 [此部分](create-campaign.md).

要创建API触发的营销活动，请执行以下步骤：

1. 使用 **[!UICONTROL API触发]** 类型。

1. 选择要用于发送消息的渠道和渠道表面，然后单击 **[!UICONTROL 创建]**.

   ![](assets/api-triggered-type.png)

1. 为营销活动指定标题和描述，然后配置要发送的消息。

   ![](assets/api-triggered-properties.png)

   >[!NOTE]
   >
   >您可以将其他数据传递到API有效负载中，以便将其用于个性化您的消息。 [了解详情](#contextual)
   >
   >在内容中使用大量或大量上下文数据可能会影响性能。

1. 在 **[!UICONTROL 受众]** 部分，指定用于识别区段中个人的命名空间。

   的 **[!UICONTROL 创建新用户档案]** 选项，可自动创建数据库中不存在的配置文件。 [了解有关在营销活动执行时创建用户档案的更多信息](#profile-creation)

1. 配置营销活动的开始和结束日期。

   如果为营销活动配置特定的开始和/或结束日期，则不会在这些日期之外执行该日期，而且如果营销活动由API触发，则API调用将失败。

1. 单击 **[!UICONTROL 查看以激活]** 要检查营销活动配置是否正确，请将其激活。

现在，您可以从API执行营销活动。 [了解详情](#execute)

### 执行营销活动 {#execute}

激活营销活动后，您需要检索生成的示例cURL请求，并将其用到API中以构建有效负载并触发营销活动。

1. 打开营销活动，然后复制并粘贴 **[!UICONTROL cURL请求]** 中。

   ![](assets/api-triggered-curl.png)

1. 在API中使用此cURL请求来构建有效负载并触发营销活动。 有关更多信息，请参阅 [交互式消息执行API文档](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).

   >[!NOTE]
   >
   >如果您在创建营销活动时配置了特定的开始和/或结束日期，则不会在这些日期之外执行该日期，API调用将失败。

## 在API触发的营销活动中使用上下文属性 {#contextual}

借助API触发的营销活动，您可以在API有效负载中传递其他数据，并在营销活动中使用这些数据来个性化您的消息。

让我们举一个示例，其中客户希望重置其密码，而您希望向他们发送在第三方工具中生成的密码重置URL。 通过API触发的营销活动，您可以将此生成的URL传递到API有效负载中，并利用它进入营销活动，将其添加到消息中。

>[!NOTE]
>
>与启用用户档案的事件不同，在REST API中传递的上下文数据用于一次性通信，而不是存储在用户档案中。 如果发现缺少配置文件，则最大会创建包含命名空间详细信息的配置文件。

要在营销活动中使用这些数据，您需要将它们传递到API有效负载中，然后使用表达式编辑器将它们添加到消息中。 为此，请使用 `{{context.<contextualAttribute>}}` 语法，其中 `<contextualAttribute>` 应与API有效负载中包含要传递的数据的变量名称匹配。

的 `{{context.<contextualAttribute>}}` 语法仅映射到字符串数据类型。

![](assets/api-triggered-context.png)

>[!IMPORTANT]
>
>的 `context.system` 语法仅限于Adobe内部用法，不应用于传递上下文属性。

请注意，目前没有上下文属性可用于左边栏菜单。 必须在个性化表达式中直接键入属性，且不会执行任何检查 [!DNL Journey Optimizer].

## 在营销活动执行时创建用户档案 {#profile-creation}

在某些情况下，您可能需要向系统中不存在的用户档案发送事务型消息。 例如，未知用户尝试重置您网站上的密码。

当数据库中不存在用户档案时，利用Journey Optimizer，可在执行营销活动时自动创建该用户档案，以向此用户档案发送消息。

>[!IMPORTANT]
>
>此功能针对 **创建少量用户档案** 在大量事务性发送用例中，平台中已存在大量用户档案。

要在营销活动执行时激活用户档案创建，请将 **[!UICONTROL 创建新用户档案]** 的 **[!UICONTROL 受众]** 中。

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>未知的用户档案在 **AJO交互式消息传递配置文件数据集** 数据集，每个出站渠道（电子邮件、短信和推送）分别位于三个默认命名空间（电子邮件、电话和ECID）中。
