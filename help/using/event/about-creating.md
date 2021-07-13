---
title: 配置统一事件
description: 了解如何配置单一事件
feature: 事件
topic: 管理
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '1674'
ht-degree: 13%

---

# 配置统一事件 {#configure-an-event}

单一事件与特定用户档案相关联。 它们可以是基于规则的，也可以是系统生成的。  有关单一事件[此部分](../event/about-events.md)的更多信息。

以下是配置新事件的首要步骤：

1. 在“管理”菜单部分，选择&#x200B;**[!UICONTROL Configurations]**。 在&#x200B;**[!UICONTROL Events]**&#x200B;部分中，单击&#x200B;**[!UICONTROL Manage]**。 将显示事件列表。

   ![](../assets/jo-event1.png)

1. 单击&#x200B;**[!UICONTROL Create Event]**&#x200B;以创建新事件。事件配置窗格将在屏幕右侧打开。

   ![](../assets/jo-event2.png)

1. 输入事件的名称。 您还可以添加描述。

   ![](../assets/jo-event3.png)

   >[!NOTE]
   >
   >请勿使用空格或特殊字符。请勿使用超过 30 个字符。

1. 在&#x200B;**[!UICONTROL Type]**&#x200B;字段中，选择&#x200B;**Uneminary**。

   ![](../assets/jo-event3bis.png)

1. 在&#x200B;**[!UICONTROL Event ID type]**&#x200B;字段中，选择要使用的事件ID类型：**基于规则的**&#x200B;或&#x200B;**系统生成的**。 有关[此部分](../event/about-events.md#event-id-type)中事件ID类型的更多信息。

   ![](../assets/jo-event4.png)

1. 使用此事件的旅程数显示在&#x200B;**[!UICONTROL Used in]**&#x200B;字段中。您可以单击 **[!UICONTROL View journeys]**&#x200B;图标，以显示使用此事件的旅程列表。

1. 定义架构和有效负载字段：在这里，您可以选择历程预期接收的事件信息（通常称为有效负载）。 然后，您便能够在旅程中使用这些信息。请参阅[此小节](../event/about-creating.md#define-the-payload-fields)。

   ![](../assets/jo-event5.png)

   >[!NOTE]
   >
   >选择&#x200B;**[!UICONTROL System Generated]**&#x200B;类型时，只有具有eventID类型字段的架构才可用。 选择&#x200B;**[!UICONTROL Rule Based]**&#x200B;类型时，所有体验事件架构均可用。

1. 对于基于规则的事件，在&#x200B;**[!UICONTROL Event ID condition]**字段内单击。 使用简单表达式编辑器，定义系统将使用的条件以识别将触发历程的事件。
   ![](../assets/jo-event6.png)

   在我们的示例中，我们根据用户档案所在的城市写了一个条件。 这意味着，每当系统收到与此条件（**[!UICONTROL City]**&#x200B;字段和&#x200B;**[!UICONTROL Paris]**&#x200B;值）匹配的事件时，它都会将其传递到历程。

   >[!NOTE]
   >
   >定义&#x200B;**[!UICONTROL Event ID condition]**&#x200B;时，高级表达式编辑器不可用。

1. 添加命名空间。此步骤是可选的，但还是建议您添加命名空间，以便您利用实时客户资料服务中存储的信息。它定义事件具有的键类型。请参阅[此小节](../event/about-creating.md#select-the-namespace)。
1. 定义用户档案标识符：从有效负载字段中选择一个字段或定义一个公式以标识与事件关联的人员。 如果您选择命名空间，此键将自动设置（但仍可编辑）。事实上，历程会选取应与命名空间对应的键（例如，如果您选择了电子邮件命名空间，则会选择电子邮件键）。 请参阅[此小节](../event/about-creating.md#define-the-event-key)。

   ![](../assets/jo-event7.png)

1. 对于系统生成的事件，您可以添加条件。 此步骤是可选的。这允许系统仅处理符合条件的事件。此条件只能基于事件中包含的信息。请参阅[此小节](../event/about-creating.md#add-a-condition)。
1. 单击 **[!UICONTROL Save]**。

   事件现已配置完毕，可随时投入旅程。还需要其他配置步骤以接收事件。请参阅[此页](../event/additional-steps-to-send-events-to-journey-orchestration.md)。

## 定义有效负载字段 {#define-the-payload-fields}

有效负载定义允许您选择系统希望从历程中的事件接收的信息，以及用于标识与事件关联的人员的键。 负载基于Experience CloudXDM字段定义。 有关XDM的更多信息，请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target=&quot;_blank&quot;}。

1. 从列表中选择XDM架构，然后单击&#x200B;**[!UICONTROL Fields]**&#x200B;字段或&#x200B;**[!UICONTROL Edit]**&#x200B;图标。

   ![](../assets/journey8.png)

   将显示架构中定义的所有字段。 字段列表因架构而异。 您可以搜索特定字段，或使用过滤器显示所有节点和字段，或仅显示选定的字段。 根据架构定义，某些字段可能是必填的，并且是预选的。 您无法取消选择它们。 默认情况下，将选择所有对于历程要正确接收事件而言必须填写的字段。

   >[!NOTE]
   >
   >对于系统生成的事件，请确保已将“编排”字段组添加到XDM架构。 这将确保您的架构包含使用[!DNL Journey Optimizer]所需的所有信息。

   ![](../assets/journey9.png)

1. 选择要从事件接收的字段。 业务用户将在历程中利用这些字段。 这些参数还必须包含用于标识与事件关联的人员的键（请参阅[此部分](../event/about-creating.md#define-the-event-key)）。

   >[!NOTE]
   >
   >对于系统生成的事件，将在所选字段列表中自动添加&#x200B;**[!UICONTROL eventID]**&#x200B;字段，以便[!DNL Journey Optimizer]能够识别事件。 推送事件的系统不应生成ID，它应使用有效负荷预览中提供的ID。 请参阅[此小节](../event/about-creating.md#preview-the-payload)。

1. 选择完所需字段后，单击&#x200B;**[!UICONTROL Ok]**&#x200B;或按&#x200B;**[!UICONTROL Enter]**。

   选定字段的数量显示在&#x200B;**[!UICONTROL Fields]**&#x200B;字段中。

   ![](../assets/journey12.png)

## 选择命名空间 {#select-the-namespace}

命名空间允许您定义用于标识与事件关联的人员的键类型。 其配置是可选的。 如果要在您的历程中检索来自[实时客户资料](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}的其他信息，则需要此信息。 如果您仅使用来自第三方系统的数据通过自定义数据源，则不需要命名空间定义。

您可以使用其中一个预定义命名空间，或使用身份命名空间服务创建新的一个预定义命名空间。 请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html){target=&quot;_blank&quot;}。

如果选择具有主标识的架构，则会预填充&#x200B;**[!UICONTROL Profiler identifier]**&#x200B;和&#x200B;**[!UICONTROL Namespace]**&#x200B;字段。 如果未定义标识，我们将选择&#x200B;_identityMap > id_&#x200B;作为主键。 然后，您必须选择命名空间，并使用&#x200B;_identityMap > id_&#x200B;预填充键（在&#x200B;**[!UICONTROL Namespace]**&#x200B;字段下）。

选择字段时，主标识字段会进行标记。

![](../assets/primary-identity.png)


从下拉列表中选择一个命名空间。

![](../assets/journey17.png)

每个历程只允许一个命名空间。 如果您在同一历程中使用多个事件，则它们需要使用相同的命名空间。 请参阅[此页](../building-journeys/journey.md)。

## 定义用户档案标识符 {#define-the-event-key}

键值是字段或字段组合是事件有效负载数据的一部分，它将允许系统识别与事件关联的人员。 键可以是Experience CloudID、CRM ID或电子邮件地址。

如果您计划利用存储在实时客户资料数据库中的数据，则必须选择在[实时客户资料服务](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}中定义为资料身份的信息作为事件键。

它将允许系统执行事件与个人用户档案之间的协调。 如果选择具有主标识的架构，则会预填充&#x200B;**[!UICONTROL Profile identifier]**&#x200B;和&#x200B;**[!UICONTROL Namespace]**&#x200B;字段。 如果未定义标识，我们将选择&#x200B;_identityMap > id_&#x200B;作为主键。 然后，您必须选择命名空间，并使用&#x200B;_identityMap > id_&#x200B;预填充键（在&#x200B;**[!UICONTROL Namespace]**&#x200B;字段下）。

选择字段时，主标识字段会进行标记。

![](../assets/primary-identity.png)

如果您需要使用其他键（如CRM ID或电子邮件地址），则需要手动添加它：

1. 单击&#x200B;**[!UICONTROL Profile identifier]**&#x200B;字段内或铅笔图标上的。

   ![](../assets/journey16.png)

1. 在有效负载字段列表中选择作为键的字段。 您还可以切换到高级表达式编辑器以创建更复杂的键（例如，事件的两个字段的串联）。 请参阅下面的此部分。

   ![](../assets/journey20.png)

收到事件后，键值将允许系统识别与事件关联的人员。 与命名空间关联（请参阅[此部分](../event/about-creating.md#select-the-namespace)），可使用键对Adobe Experience Platform执行查询。 请参阅[此页](../building-journeys/about-journey-activities.md#orchestration-activities)。键还用于检查人员是否处于历程中。 事实上，一个人不可能在同一旅程中处于两个不同的位置。 因此，系统不允许同一密钥（例如CRMID=3224）位于同一历程中的不同位置。

如果要执行其他操作，则还可以访问高级表达式函数(**[!UICONTROL Advanced mode]**)。 利用这些函数，可处理用于执行特定查询（如更改格式、执行字段连接）的值，只考虑字段的一部分（例如10个前字符）。 请参阅[Journey Orchestration文档](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html?lang=zh-Hans){target=&quot;_blank&quot;}。

## 添加条件 {#add-a-condition}

条件仅适用于系统生成的事件。 您可以定义一个事件条件，以便系统过滤事件的处理。 如果条件为true，则会处理该事件。 如果条件不为true，则忽略该事件。

事件条件只能基于事件有效负载中传递的数据。 营销人员不能在画布中更改在事件级别定义的条件。 其目的是在使用此事件时强化此条件。 例如，如果您从不希望营销人员在购物车值太小时使用购物车放弃事件，则可以在“购物车值”事件字段中创建条件，并强加值超过100美元。

您可以使用简单表达式编辑器或高级表达式编辑器来设置事件条件。 请参阅[Journey Orchestration文档](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html){target=&quot;_blank&quot;}。

例如，您可以定义一个条件，以便仅处理特定事件类型的事件并忽略其他类型。 或者，如果您的事件是购物车放弃，并且有效负荷包含购物车值字段，则您可以定义一个事件条件以仅在购物车值大于100美元时处理事件。

![](../assets/journey78.png)

## 预览有效负载 {#preview-the-payload}

有效负载预览允许您验证有效负载定义。

>[!NOTE]
>
>对于系统生成的事件，在创建事件时，在查看有效负载预览之前，请保存事件并重新将其打开。 需要此步骤才能在有效负载中生成事件ID。

1. 单击&#x200B;**[!UICONTROL View Payload]**&#x200B;图标以预览系统预期的有效负载。

   ![](../assets/journey13.png)

   您可以注意到已显示选定的字段。

   ![](../assets/journey14.png)

1. 检查预览以验证有效负载定义。

1. 然后，您可以将有效负载预览共享给负责事件发送的人员。 此负载可帮助他设计推送到[!DNL Journey Optimizer]的事件的设置。 请参阅[此页](../event/additional-steps-to-send-events-to-journey-orchestration.md)。
