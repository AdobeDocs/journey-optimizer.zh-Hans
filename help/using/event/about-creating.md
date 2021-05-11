---
title: 配置统一事件
description: 了解如何配置统一事件
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '1637'
ht-degree: 14%

---

# 配置统一事件{#configure-an-event}

![](../assets/do-not-localize/badge.png)

统一事件与特定用户档案相链接。 它们可以是基于规则的，也可以是系统生成的。  阅读有关统一事件[本节](../event/about-events.md)的更多信息。

以下是配置新事件的第一步：

1. 在左侧菜单中，单击&#x200B;**[!UICONTROL Admin]**&#x200B;图标，然后单击&#x200B;**[!UICONTROL Events]**。 将显示事件列表。

   ![](../assets/jo-event1.png)

1. 单击&#x200B;**[!UICONTROL Add]**&#x200B;以创建新事件。事件配置窗格将在屏幕右侧打开。

   ![](../assets/jo-event2.png)

1. 输入事件的名称。 您还可以添加说明。

   ![](../assets/jo-event3.png)

   >[!NOTE]
   >
   >请勿使用空格或特殊字符。请勿使用超过 30 个字符。

1. 在&#x200B;**[!UICONTROL Type]**&#x200B;字段中，选择&#x200B;**幺正事件**。

   ![](../assets/jo-event3bis.png)

1. 在&#x200B;**[!UICONTROL Event ID type]**&#x200B;字段中，选择要使用的事件ID类型：**基于规则**&#x200B;或&#x200B;**系统生成的**。 请阅读[此部分](../event/about-events.md#event-id-type)中有关事件ID类型的更多信息。

   ![](../assets/jo-event4.png)

1. 使用此事件的旅程数显示在&#x200B;**[!UICONTROL Used in]**&#x200B;字段中。您可以单击 **[!UICONTROL View journeys]**&#x200B;图标，以显示使用此事件的旅程列表。

1. 定义模式和有效负荷字段：在这里，您选择事件信息（通常称为有效负荷），预计将接收的旅程。 然后，您便能够在旅程中使用这些信息。请参阅[此小节](../event/about-creating.md#define-the-payload-fields)。

   ![](../assets/jo-event5.png)

   >[!NOTE]
   >
   >选择&#x200B;**[!UICONTROL System Generated]**&#x200B;类型时，只有具有eventID类型mixin的模式才可用。 选择&#x200B;**[!UICONTROL Rule Based]**&#x200B;类型时，所有体验事件模式都可用。

1. 对于基于规则的事件，请在&#x200B;**[!UICONTROL Event ID condition]**字段内单击。 使用简单的表达式编辑器，定义系统将使用的条件，以识别将触发您旅程的事件。
   ![](../assets/jo-event6.png)

   在我们的例子中，我们根据用户档案的城市写了一个条件。 这意味着，每当系统收到与此条件匹配的事件（**[!UICONTROL City]**&#x200B;字段和&#x200B;**[!UICONTROL Paris]**&#x200B;值）时，它都会将其传递给旅程。

1. 添加命名空间。此步骤是可选的，但还是建议您添加命名空间，以便您利用实时客户资料服务中存储的信息。它定义事件具有的键类型。请参阅[此小节](../event/about-creating.md#select-the-namespace)。
1. 定义键：从有效负载字段中选择一个字段或定义一个公式以标识与事件关联的个人。如果您选择命名空间，此键将自动设置（但仍可编辑）。实际上，“旅程”会选取应与命名空间对应的键(例如，如果您选择了电子邮件命名空间，则会选择该电子邮件键)。 请参阅[此小节](../event/about-creating.md#define-the-event-key)。

   ![](../assets/jo-event7.png)

1. 对于系统生成的事件，可以添加条件。 此步骤是可选的。这允许系统仅处理符合条件的事件。此条件只能基于事件中包含的信息。请参阅[此小节](../event/about-creating.md#add-a-condition)。
1. 单击 **[!UICONTROL Save]**。

   ![](../assets/journey7.png)

   事件现已配置完毕，可随时投入旅程。还需要其他配置步骤以接收事件。请参阅[此页](../event/additional-steps-to-send-events-to-journey-orchestration.md)。

## 定义有效负荷字段{#define-the-payload-fields}

有效负荷定义允许您选择系统希望从旅程中的事件接收的信息，以及确定与事件关联的人员的键。 负载基于Experience CloudXDM字段定义。 有关XDM的详细信息，请参阅[此页](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans)。

1. 从列表中选择一个XDM模式，然后单击&#x200B;**[!UICONTROL Payload]**&#x200B;字段或&#x200B;**[!UICONTROL Edit]**&#x200B;图标。

   ![](../assets/journey8.png)

   将显示模式中定义的所有字段。 字段的列表因模式而异。 您可以搜索特定字段或使用过滤器显示所有节点和字段，或仅显示所选字段。 根据模式定义，某些字段可能是必填的并且是预选的。 您无法取消选择它们。 默认情况下，对于要由旅程正确接收事件，必须填写的所有字段都处于选中状态。

   >[!NOTE]
   >
   >确保已将“业务流程”混音添加到XDM模式。 这将确保您的模式包含使用[!DNL Journey Optimizer]所需的所有信息。

   ![](../assets/journey9.png)

1. 选择要从事件接收的字段。 这些是业务用户在旅程中将利用的字段。 它们还必须包含用于标识与事件关联的人员的密钥（请参阅[本节](../event/about-creating.md#define-the-event-key)）。

   ![](../assets/journey10.png)

   >[!NOTE]
   >
   >对于系统生成的事件,**[!UICONTROL eventID]**&#x200B;字段会自动添加到所选字段的列表中，以便[!DNL Journey Optimizer]可以标识事件。 推送事件的系统不应生成ID，它应使用有效负荷预览中可用的ID。 请参阅[此小节](../event/about-creating.md#preview-the-payload)。

1. 选择完所需字段后，单击&#x200B;**[!UICONTROL Save]**&#x200B;或按&#x200B;**[!UICONTROL Enter]**。

   ![](../assets/journey11.png)

   选定字段的数目将显示在&#x200B;**[!UICONTROL Payload]**&#x200B;字段中。

   ![](../assets/journey12.png)

## 选择命名空间{#select-the-namespace}

命名空间允许您定义用于标识与事件关联的人员的键类型。 其配置是可选的。 如果要在旅程中检索来自[实时客户用户档案](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)的其他信息，则需要此信息。 如果您只使用来自第三方系统的数据通过自定义数据源，则不需要命名空间定义。

您可以使用其中一个预定义的命名空间，也可以使用Identity Player服务创建新的预定义标识。 请参阅此[页](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html)。

如果选择具有主标识的模式，则预填&#x200B;**[!UICONTROL Key]**&#x200B;和&#x200B;**[!UICONTROL Namespace]**&#x200B;字段。 如果未定义标识，则选择&#x200B;_identityMap > id_&#x200B;作为主键。 然后，您必须选择一个命名空间，然后使用&#x200B;_identityMap > id_&#x200B;预填（在&#x200B;**[!UICONTROL Namespace]**&#x200B;字段下）键。

选择字段时，主标识字段将被标记。

![](../assets/primary-identity.png)


从下拉命名空间中选择列表。

![](../assets/journey17.png)

每个旅程只允许一个命名空间。 如果您在同一旅程中使用多个事件，他们需要使用相同的命名空间。 请参阅[此页](../building-journeys/journey.md)。

## 定义事件键{#define-the-event-key}

关键是字段或字段组合是事件有效负荷数据的一部分，这将允许系统识别与事件关联的人。 密钥可以是Experience CloudID、CRM ID或电子邮件地址。

如果您计划利用存储在Real-time Customer 用户档案事件库中的数据，则必须选择在[Real-time Customer  Service](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)中定义为用户档案身份的信息作为用户档案密钥。

它将允许系统执行事件与个人用户档案之间的协调。 如果选择具有主标识的模式，则预填&#x200B;**[!UICONTROL Key]**&#x200B;和&#x200B;**[!UICONTROL Namespace]**&#x200B;字段。 如果未定义标识，则选择&#x200B;_identityMap > id_&#x200B;作为主键。 然后，您必须选择一个命名空间，然后使用&#x200B;_identityMap > id_&#x200B;预填（在&#x200B;**[!UICONTROL Namespace]**&#x200B;字段下）键。

选择字段时，主标识字段将被标记。

![](../assets/primary-identity.png)

如果您需要使用其他键（如CRM ID或电子邮件地址），则需要手动添加它：

1. 单击&#x200B;**[!UICONTROL Key]**&#x200B;字段或铅笔图标。

   ![](../assets/journey16.png)

1. 在有效负荷字段的列表中选择选作键的字段。 您还可以切换到高级表达式编辑器以创建更复杂的键(例如，事件的两个字段的串联)。 请参阅下面的部分。

   ![](../assets/journey20.png)

当收到事件时，键值将允许系统识别与事件关联的人。 与命名空间关联（请参阅[本节](../event/about-creating.md#select-the-namespace)），该键可用于在Adobe Experience Platform上执行查询。 请参阅[此页](../building-journeys/about-journey-activities.md#orchestration-activities)。钥匙还用于检查某人是否在旅程中。 事实上，一个人不可能在同一旅程中处于两个不同的位置。 因此，系统不允许同一密钥（例如密钥CRMID=3224）在同一旅程的不同位置。

如果要执行其他操作，您还可以访问高级表达式函数(**[!UICONTROL Advanced mode]**)。 通过这些函数，您可以操作用于执行特定查询的值，例如更改格式、执行字段连接，只考虑字段的一部分（例如10个前字符）。 请参阅[此页](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html)。

## 添加条件{#add-a-condition}

该条件仅适用于系统生成的事件。 您可以定义一个事件条件，该条件允许系统过滤事件的处理。 如果条件为true，则处理事件。 如果条件不为true，则忽略事件。

事件条件只能基于事件有效负荷中传递的数据。 营销人员不能在画布中更改在事件级别定义的条件。 其目的是在使用此事件时强化此条件。 例如，如果您不希望营销人员在购物车价值太小时使用购物车放弃事件，您可以在“购物车价值”事件字段中创建一个条件，并强加一个超过100美元的值。

您可以使用简单的表达式编辑器或高级表达式编辑器来设置事件上的条件。 请参阅[此页](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html)。

例如，您可以定义一个条件，以仅处理特定事件类型的事件并忽略其他类型。 或者，如果您的事件是购物车放弃率，且有效负荷包含购物车值字段，则您可以定义一个事件条件，以便仅在购物车值大于100美元时处理事件。

![](../assets/journey78.png)

## 预览有效负荷{#preview-the-payload}

有效负荷预览允许您验证有效负荷定义。

>[!NOTE]
>
>对于系统生成的事件，在创建事件时，在查看有效负荷预览之前，请保存事件并重新打开它。 需要此步骤才能在有效负荷中生成事件ID。

1. 单击&#x200B;**[!UICONTROL View Payload]**&#x200B;图标以预览系统预期的有效负荷。

   ![](../assets/journey13.png)

   您可以注意到显示了选定的字段。

   ![](../assets/journey14.png)

1. 检查预览以验证有效负荷定义。

1. 然后，您可以将有效负荷预览共享给负责事件发送的人员。 此负载可帮助他设计推送到[!DNL Journey Optimizer]的事件的设置。 请参阅[此页](../event/additional-steps-to-send-events-to-journey-orchestration.md)。
