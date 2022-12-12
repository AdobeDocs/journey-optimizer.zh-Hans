---
solution: Journey Optimizer
product: journey optimizer
title: 配置统一事件
description: 了解如何配置单一事件
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: e22e2bc7-0c15-457a-8980-97bea5da7784
source-git-commit: ef838945e0c3595de8ad920203b278bb51671d16
workflow-type: tm+mt
source-wordcount: '1479'
ht-degree: 0%

---

# 配置统一事件 {#configure-an-event}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_unitary"
>title="单一事件"
>abstract="事件配置允许您定义Journey Optimizer将作为事件接收的信息。 您可以使用多个事件（在历程的不同步骤中），而多个历程可以使用相同的事件。 单一事件与特定用户档案相关联。 它们可以是基于规则的，也可以是系统生成的。"

单一事件与特定用户档案相关联。 它们可以是基于规则的，也可以是系统生成的。  阅读有关单一事件的更多信息 [此部分](../event/about-events.md).

以下是配置新事件的首要步骤：

1. 在“管理”菜单部分，选择 **[!UICONTROL Configurations]**. 在  **[!UICONTROL Events]** ，单击 **[!UICONTROL Manage]**. 将显示事件列表。

   ![](assets/jo-event1.png)

1. 单击 **[!UICONTROL Create Event]** 创建新事件。 事件配置窗格将在屏幕右侧打开。

   ![](assets/jo-event2.png)

1. 输入事件的名称。 您还可以添加描述。

   ![](assets/jo-event3.png)

   >[!NOTE]
   >
   >请勿使用空格或特殊字符。 请勿使用超过30个字符。

1. 在 **[!UICONTROL Type]** 字段，选择 **单一**.

   ![](assets/jo-event3bis.png)

1. 在 **[!UICONTROL Event ID type]** 字段中，选择要使用的事件ID类型： **基于规则** 或 **系统生成**. 有关事件ID类型的更多信息，请参阅 [此部分](../event/about-events.md#event-id-type).

   ![](assets/jo-event4.png)

1. 使用此事件的旅程数显示在 **[!UICONTROL Used in]** 字段。 您可以单击 **[!UICONTROL View journeys]** 图标以显示使用此事件的历程列表。

1. 定义架构和有效负载字段：在这里，您可以选择历程预期接收的事件信息（通常称为有效负载）。 然后，您便能够在历程中使用此信息。 请参阅 [此部分](../event/about-creating.md#define-the-payload-fields).

   ![](assets/jo-event5.png)

   >[!NOTE]
   >
   >当您选择 **[!UICONTROL System Generated]** 类型，只有具有eventID类型字段的架构才可用。 当您选择 **[!UICONTROL Rule Based]** 类型时，所有体验事件架构都可用。

1. 对于基于规则的事件，请在 **[!UICONTROL Event ID condition]** 字段。 使用简单表达式编辑器，定义系统将使用的条件以识别将触发历程的事件。
   ![](assets/jo-event6.png)

   在我们的示例中，我们根据用户档案所在的城市写了一个条件。 这意味着每当系统收到与此条件匹配的事件时(**[!UICONTROL City]** 字段和 **[!UICONTROL Paris]** 值)，它会将其传递到历程。

   >[!NOTE]
   >
   >在定义 **[!UICONTROL Event ID condition]**. 在简单的表达式编辑器中，并非所有运算符都可用，它们取决于数据类型。 例如，对于字段的字符串类型，可以使用“包含”或“等于”。

1. 添加命名空间。 此步骤是可选的，但是建议您执行，因为添加命名空间允许您利用实时客户资料服务中存储的信息。 它定义事件具有的键类型。 请参阅 [此部分](../event/about-creating.md#select-the-namespace).
1. 定义用户档案标识符：从有效负载字段中选择一个字段或定义一个公式以标识与事件关联的人员。 如果您选择命名空间，此键将自动设置（但仍可编辑）。 事实上，历程会选取应与命名空间对应的键（例如，如果您选择了电子邮件命名空间，则会选择电子邮件键）。 请参阅 [此部分](../event/about-creating.md#define-the-event-key).

   ![](assets/jo-event7.png)

1. 单击 **[!UICONTROL Save]**.

   事件现已配置完毕，可随时放入历程中。 接收事件需要其他配置步骤。 请参阅 [本页](../event/additional-steps-to-send-events-to-journey.md).

## 定义有效负载字段 {#define-the-payload-fields}

有效负载定义允许您选择系统希望从历程中的事件接收的信息，以及用于标识与事件关联的人员的键。 有效负载基于Experience Cloud XDM字段定义。 有关XDM的更多信息，请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}。

1. 从列表中选择XDM架构，然后单击 **[!UICONTROL Fields]** 字段或 **[!UICONTROL Edit]** 图标。

   ![](assets/journey8.png)

   将显示架构中定义的所有字段。 字段列表因架构而异。 您可以搜索特定字段，或使用过滤器显示所有节点和字段，或仅显示选定的字段。 根据架构定义，某些字段可能是必填的，并且是预选的。 您无法取消选择它们。 默认情况下，将选择所有对于历程要正确接收事件而言必须填写的字段。

   >[!NOTE]
   >
   >对于系统生成的事件，请确保已将“编排”字段组添加到XDM架构。 这将确保您的架构包含所有使用所需的信息 [!DNL Journey Optimizer].

   ![](assets/journey9.png)

1. 选择要从事件接收的字段。 业务用户将在历程中利用这些字段。 它们还必须包含用于标识与事件关联的人员的键(请参阅 [此部分](../event/about-creating.md#define-the-event-key))。

   >[!NOTE]
   >
   >对于系统生成的事件， **[!UICONTROL eventID]** 字段会自动添加到选定的字段列表中，以便 [!DNL Journey Optimizer] 可以识别事件。 推送事件的系统不应生成ID，它应使用有效负荷预览中提供的ID。 请参阅 [此部分](../event/about-creating.md#preview-the-payload).

1. 选择完所需字段后，单击 **[!UICONTROL Ok]** 或按 **[!UICONTROL Enter]**.

   选定字段的数量显示在 **[!UICONTROL Fields]** 字段。

   ![](assets/journey12.png)

## 选择命名空间 {#select-the-namespace}

>[!CONTEXTUALHELP]
>id="ajo_journey_namespace"
>title="身份命名空间"
>abstract="选择键以标识与事件关联的客户用户档案。"

命名空间允许您定义用于标识与事件关联的人员的键类型。 其配置是可选的。 如果要在您的历程中检索来自 [实时客户资料](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}。 如果您仅使用来自第三方系统的数据通过自定义数据源，则不需要命名空间定义。

您可以使用其中一个预定义命名空间，或使用身份命名空间服务创建新的一个预定义命名空间。 请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html){target=&quot;_blank&quot;}。

如果您选择的架构具有主标识，则 **[!UICONTROL Profiler identifier]** 和 **[!UICONTROL Namespace]** 字段已预填充。 如果未定义身份，我们将选择 _identityMap > id_ 作为主键。 然后，您必须选择命名空间，并且该键值将被预填充(位于 **[!UICONTROL Namespace]** 字段)使用 _identityMap > id_.

选择字段时，主标识字段会进行标记。

![](assets/primary-identity.png)


从下拉列表中选择一个命名空间。

![](assets/journey17.png)

每个历程只允许一个命名空间。 如果您在同一历程中使用多个事件，则它们需要使用相同的命名空间。 请参阅 [本页](../building-journeys/journey.md).

## 定义用户档案标识符 {#define-the-event-key}

键值是字段或字段组合，字段是事件有效负载数据的一部分，并允许系统标识与事件关联的人员。 键可以是Experience Cloud ID、CRM ID或电子邮件地址。

要使用存储在Adobe实时客户资料数据库中的数据，事件键必须是您在 [实时客户资料服务](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}。

用户档案标识符允许系统执行事件与个人用户档案之间的协调。 如果您选择的架构具有主标识，则 **[!UICONTROL Profile identifier]** 和 **[!UICONTROL Namespace]** 字段已预填充。 如果未定义身份，则 _identityMap > id_ 是主键。 然后，您必须选择命名空间，并且该键值会使用 _identityMap > id_.

选择字段时，主标识字段会进行标记。

![](assets/primary-identity.png)

如果您需要使用其他密钥（如CRM ID或电子邮件地址），则需要手动添加该密钥，如下所述：

1. 在 **[!UICONTROL Profile identifier]** 字段，或在铅笔图标上。

   ![](assets/journey16.png)

1. 在有效负载字段列表中选择作为键的字段。 您还可以切换到高级表达式编辑器以创建更复杂的键（例如，事件的两个字段的级联）。

   ![](assets/journey20.png)

当收到事件时，键值允许系统识别与该事件关联的人员。 与命名空间关联(请参阅 [此部分](../event/about-creating.md#select-the-namespace))，则可以使用键对Adobe Experience Platform执行查询。 请参阅 [本页](../building-journeys/about-journey-activities.md#orchestration-activities).
键还用于检查人员是否处于历程中。 事实上，一个人不可能在同一旅程中处于两个不同的位置。 因此，系统不允许同一密钥（例如CRMID=3224）位于同一历程中的不同位置。

您还可以访问高级表达式函数(**[!UICONTROL Advanced mode]**)。 利用这些函数，可处理用于执行特定查询（如更改格式、执行字段连接）的值，只考虑字段的一部分（例如10个前字符）。 请参阅 [页面](../building-journeys/expression/expressionadvanced.md).

## 预览有效负载 {#preview-the-payload}

有效负载预览允许您验证有效负载定义。

>[!NOTE]
>
>对于系统生成的事件，在创建事件时，在查看有效负载预览之前，请保存事件并重新将其打开。 需要此步骤才能在有效负载中生成事件ID。

1. 单击 **[!UICONTROL View Payload]** 图标以预览系统预期的有效负荷。

   ![](assets/journey13.png)

   您可以注意到已显示选定的字段。

   ![](assets/journey14.png)

1. 检查预览以验证有效负载定义。

1. 然后，您可以将有效负载预览共享给负责事件发送的人员。 此有效负载可帮助他们设计推送到的事件的设置 [!DNL Journey Optimizer]. 请参阅 [本页](../event/additional-steps-to-send-events-to-journey.md).
