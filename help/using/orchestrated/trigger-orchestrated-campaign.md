---
solution: Journey Optimizer
product: journey optimizer
title: 使用信号触发编排的营销活动
description: 了解如何使用REST API或其他营销活动结束活动的信号触发编排的营销活动，以及如何将参数传递到营销活动中。
feature: Campaigns
topic: Content Management
role: Developer
level: Intermediate
version: Campaign Orchestration
exl-id: d1fd072d-b143-4752-822f-23f98684ba80
feature_v2:
  - id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 1429
ht-degree: 0%

---

# 使用信号触发编排的营销活动 {#trigger-signal}

您可以使用信号而不是固定计划来启动编排的营销活动。 当营销活动收到信号时，它将运行，您可以在有效载荷中传递参数。 它们可用作定位、条件或表达式的变量。

信号可能来自以下任一来源：

* REST API — 您的应用程序或集成调用触发器终结点（请参阅[发布并触发营销活动](#publish)和[API引用](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"}）。
* 另一个编排的营销活动 — 上游营销活动的&#x200B;**[!UICONTROL End]**&#x200B;活动在分支完成时发送相同类型的信号。 [了解如何配置结束活动](#signal-end)。

本页介绍如何设置接收信号（计划、参数、测试、发布）的营销活动，以及如何从API或&#x200B;**[!UICONTROL 结束]**&#x200B;活动触发它。 变量可用后，有关如何在规则和&#x200B;**[!UICONTROL 测试]**&#x200B;条件中使用变量的详细信息，请参阅[在编排的活动中使用变量](variables-orchestrated-campaigns.md)。

有关触发器端点的完整REST规范（路径、标头、正文、响应和错误），请参阅Adobe Journey Optimizer API文档中的[触发器编排的营销活动API](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"}。

使用信号触发编排营销活动的端到端流程：

1. [计划由信号触发的营销活动](#configure-signal)
1. [添加信号有效负载的参数](#parameters)（可选）
1. [构建和测试活动](#build-and-test)
1. [发布并触发营销活动](#publish)

>[!NOTE]
>
>要使用信号触发编排的营销活动，您需要&#x200B;**[!DNL Publish orchestrated campaigns]**&#x200B;权限(`orchestrated-campaign.publish`)。 查看[内置权限](../administration/ootb-permissions.md)。

## 计划由信号触发的营销活动 {#configure-signal}

要将编排的营销活动设置为在信号而不是计划上启动，请执行以下步骤：

1. 使用信号打开要触发的已编排营销活动。

1. 打开计划配置。 [了解如何计划编排的营销活动](create-orchestrated-campaign.md#schedule)。

1. 选择&#x200B;**[!UICONTROL 由信号]**&#x200B;触发，以便营销活动等待信号而不是按计划运行。

   ![计划菜单，已选择信号选项触发](assets/triggered-oc-scheduler.png){zoomable="yes"}

## 添加信号有效负载的参数（可选） {#parameters}

您可以在触发信号中传递参数，并在执行上下文中的促销活动中使用这些参数 — 例如，在定位、条件或表达式中。 首先在计划设置中定义每个参数，然后在调用触发器API或从上游营销活动的&#x200B;**[!UICONTROL 结束]**&#x200B;活动映射参数时传递其值（[请参阅以下](#signal-end)）。

1. 打开活动计划程序并选择&#x200B;**[!UICONTROL 添加参数]**。

1. 定义要在信号有效负载中发送的每个参数的名称和数据类型。 您还可以提供在测试模式下触发营销活动时将使用的&#x200B;**测试值**。 [了解如何测试触发的营销活动](#build-and-test)。

   ![添加参数以定义信号的有效负荷参数](assets/triggered-oc-parameter.png){zoomable="yes"}

>[!NOTE]
>
>对于由REST API触发的编排活动，如果您在API调用中传递了未在调度程序中定义的参数，则API调用仍会成功，并且会传播该参数，您可以在表达式中使用它。 但是，编排的活动界面不会帮助您使用它，例如，测试活动不会列出或显示未在调度程序中定义的参数。

## 测试活动 {#build-and-test}

在画布上构建营销活动，然后在&#x200B;**[!UICONTROL 草稿]**&#x200B;中测试它，然后通过REST API发送信号以进行发布。

* **由REST API触发的编排营销活动** — 使用以下步骤在草稿中运行营销活动，并在发布之前验证定位、参数和投放逻辑。

* **由结束活动触发的编排营销活动** — 无法在草稿中运行完整的端到端链：发布上游营销活动后，其&#x200B;**[!UICONTROL 结束]**&#x200B;活动将只启动已发布的下游营销活动。 要在发布两个营销活动之前测试下游端，请将该营销活动保留在&#x200B;**[!UICONTROL 草稿]**&#x200B;中，在调度程序中为信号参数设置&#x200B;**[!UICONTROL 测试值]**（[添加信号有效负载的参数](#parameters)），然后执行以下API步骤。 触发器API调用在运行时使用与&#x200B;**[!UICONTROL End]**&#x200B;活动相同的负载，因此您可以在发布下游营销活动并配置上游&#x200B;**[!UICONTROL End]**&#x200B;活动（[从另一个营销活动的End活动](#signal-end)触发事件）之前验证参数路由和画布逻辑。

1. 在画布上添加并连接活动（受众、定位、投放）。 [了解如何精心策划营销活动](orchestrate-activities.md)

1. 如果您在信号中定义了参数，则可以将它们引入画布逻辑（例如，在条件或定位中）。 在此示例中，“channel”参数用作&#x200B;**[!UICONTROL 测试]**&#x200B;活动中的条件。

   ![在测试活动中用作条件的渠道参数](assets/triggered-oc-use-parameters.png)

   要在表达式编辑器中使用信号参数（例如，在&#x200B;**[!UICONTROL 构建受众]**&#x200B;活动中构建查询），请在表达式字段中键入`$(vars/@<parameterName>)`。 将`<parameterName>`替换为调度程序中定义的参数名称，例如`$(vars/@channel)`。 [了解如何使用表达式编辑器](edit-expressions.md)。

1. 打开活动计划程序，选择&#x200B;**[!UICONTROL 复制API请求]**，然后选择格式（cURL或HTTP请求）。

   复制的信息包括编排的营销活动ID、沙盒名称、组织ID以及参数的测试值（如果您已添加某些值）。

   在计划配置中![复制API请求选项](assets/triggered-oc-copy.png)

   +++带参数和测试值的示例cURL请求

   ```bash
   POST https://platform.adobe.io/ajo/campaign-orchestration/orchestratedCampaigns/1c7529c7-7a8c-491a-a2c6-3d8131d2e17d/trigger
   
   Headers:
   Authorization: Bearer ## Access token ##
   Content-Type: application/json
   x-api-key: ## Provide API Key here ##
   x-api-version: 1
   x-gw-ims-org-id: 123456ABCDEFG@LumaOrg
   x-sandbox-name: prod
   
   Body:
   {
   "variables": {
      "channel": "sms"
   }
   }
   ```

   +++

1. 单击&#x200B;**[!UICONTROL 开始]**&#x200B;以开始营销活动。

1. 使用您从调度程序复制的示例请求发送触发器API调用。 有关请求和响应详细信息，请参阅[触发编排的营销活动API](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"}。

如果对测试结果满意，[发布营销活动](#publish)。

## 发布并触发营销活动 {#publish}

在您[测试营销活动](#build-and-test)后，请发布该营销活动，以便它能够从您的应用程序或其他营销活动的&#x200B;**[!UICONTROL 结束]**&#x200B;活动接收信号。 [了解有关启动和监视营销活动的更多信息](start-monitor-campaigns.md#publish)。

然后，您可以从REST API或其他营销活动的&#x200B;**[!UICONTROL End]**&#x200B;活动触发它。 请参阅以下部分。

### 使用REST API发送信号 {#publish-api}

发布后，每次从自己的应用程序触发活动时，请按照以下步骤操作：

1. 打开活动计划程序，选择&#x200B;**[!UICONTROL 复制API请求]**，然后选择格式（cURL或HTTP请求）。

   复制的信息包括编排的营销活动ID、沙盒名称、组织ID和参数（如果您已添加某些内容）。

   ![在计划配置中复制API请求](assets/triggered-oc-copy.png)

1. 从系统中调用触发器API。 请参阅[触发编排的营销活动API](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"}，了解实时终结点规范。

   >[!IMPORTANT]
   >
   >对于实时编排的营销活动，节流护栏强制在两个API触发器执行之间至少间隔一小时。 如果您在该间隔时间耗尽之前再次调用API，则API返回HTTP 429（请求过多）。 触发草稿版本进行测试时，不应用此护栏。

   如果您向信号有效负载添加了参数，则在营销活动运行时，您在API调用中传递的值将显示为营销活动事件变量。 要检查这些活动，请从活动画布工具栏中打开活动日志。 在&#x200B;**[!UICONTROL 任务]**&#x200B;选项卡中，识别与信号对应的任务，然后单击铅笔图标以访问相关事件变量。 [了解如何访问日志和任务](start-monitor-campaigns.md#logs-tasks)。

   ![活动事件变量可用的日志和任务屏幕](assets/trigger-events-variables.png){zoomable="yes"}

### 发送来自其他营销活动结束活动的信号 {#signal-end}

使用此路径链接编排的营销活动：当上游营销活动完成分支时，**[!UICONTROL End]**&#x200B;活动会向已设置为&#x200B;**[!UICONTROL 并由信号]**&#x200B;触发的下游营销活动发送信号。 这样，您可以重复使用较小的营销活动，并从每个调用方传递不同的有效负载。

>[!NOTE]
>
>* 您可以在同一画布上使用多个&#x200B;**[!UICONTROL End]**&#x200B;活动，并配置每个活动以触发不同的下游营销活动。
>* 多个营销活动可以触发相同的下游营销活动。 每个调用均可发送不同的有效负载。

在应首先运行的营销活动上执行以下步骤：

1. 打开应发送信号的已编排营销活动，并在分支末尾选择&#x200B;**[!UICONTROL End]**&#x200B;活动，该活动必须在下游营销活动开始之前完成。
1. 在&#x200B;**[!UICONTROL 外部信号]**&#x200B;部分中，选择要触发的下游营销活动。

1. （可选）添加参数：使用与下游市场活动计划相同的名称，并设置每个值。

   ![](assets/end-signal.png)

1. 要在发布之前在草稿模式下测试下游营销活动，请按照[测试营销活动](#build-and-test)部分中的步骤操作，以使用REST API在草稿中触发它。

必须先发布下游营销活动，然后上游营销活动运行到足以触发它的&#x200B;**[!UICONTROL 结束]**&#x200B;活动。 如果未发布目标营销活动时发送信号，则执行将失败。 发布下游营销活动，然后根据需要继续或重新启动。
