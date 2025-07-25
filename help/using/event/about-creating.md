---
solution: Journey Optimizer
product: journey optimizer
title: 配置单一事件
description: 了解如何配置单一事件
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: 事件，单一，创建，历程
exl-id: e22e2bc7-0c15-457a-8980-97bea5da7784
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '1693'
ht-degree: 13%

---

# 配置单一事件 {#configure-an-event}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_unitary"
>title="单一事件"
>abstract="事件配置让您可以定义 Journey Optimizer 将作为事件接收的信息。您可以使用多个事件（在历程的不同步骤中），而多个历程可以使用相同的事件。单一事件链接到特定轮廓。它们可以基于规则，也可以由系统生成。"

>[!CONTEXTUALHELP]
>id="ajo_journey_event_parameters"
>title="参数"
>abstract="定义事件的参数，例如架构和负载字段。对于基于规则的事件，使用&#x200B;**[!UICONTROL 事件 ID 条件]**&#x200B;字段来定义系统将用来识别触发您的历程的事件的条件。添加用于事件的身份标识类型和轮廓标识符。"

单一事件链接到特定轮廓。它们可以是基于规则的，也可以是系统生成的。  阅读有关单一事件[本节](../event/about-events.md)的更多信息。

以下是配置新事件的首要步骤：

1. 在“管理”菜单部分中浏览到&#x200B;**[!UICONTROL 配置]**，在&#x200B;**[!UICONTROL 事件]**&#x200B;部分中单击&#x200B;**[!UICONTROL 管理]**。 将显示事件列表。

   ![](assets/jo-event1.png)

1. 单击&#x200B;**[!UICONTROL 创建事件]**&#x200B;以创建新事件。 事件配置窗格将在屏幕右侧打开。

   ![](assets/jo-event2.png)

1. 输入事件的名称。 您还可以添加描述。

   ![](assets/jo-event3.png)

   >[!NOTE]
   >
   >只允许使用字母数字字符和下划线。 最大长度为30个字符。

1. 在&#x200B;**[!UICONTROL 类型]**&#x200B;字段中，选择&#x200B;**单一**。

   ![](assets/jo-event3bis.png)

1. 在&#x200B;**[!UICONTROL 事件ID类型]**&#x200B;字段中，选择要使用的事件ID类型： **基于规则**&#x200B;或&#x200B;**系统生成**。 有关[此部分](../event/about-events.md#event-id-type)中事件ID类型的更多信息。

   ![](assets/jo-event4.png)

1. 使用此事件的历程数显示在&#x200B;**[!UICONTROL 在]**&#x200B;中使用字段中。 您可以单击&#x200B;**[!UICONTROL 查看历程]**&#x200B;图标以显示使用此事件的历程列表。

1. 定义架构和有效负载字段：在这里，您可以选择历程预期接收的事件信息（通常称为有效负载）。 然后，您便能够在旅程中使用这些信息。请参阅[此小节](../event/about-creating.md#define-the-payload-fields)。

   ![](assets/jo-event5.png)

   >[!NOTE]
   >
   >选择&#x200B;**[!UICONTROL 系统生成的]**&#x200B;类型时，只有具有eventID类型字段的架构可用。 当您选择&#x200B;**[!UICONTROL 基于规则的]**&#x200B;类型时，所有体验事件架构都可用。

1. 对于基于规则的事件，请单击&#x200B;**[!UICONTROL 事件ID条件]**&#x200B;字段中的。 使用简单或高级表达式编辑器，定义系统将使用的条件，以识别将触发历程的事件。

   ![](assets/jo-event6.png)

   在我们的示例中，我们根据用户档案所在的城市编写了条件。 这意味着每当系统收到与此条件（**[!UICONTROL 城市]**&#x200B;字段和&#x200B;**[!UICONTROL 巴黎]**&#x200B;值）匹配的事件，它就会将其传递到历程。

   >[!NOTE]
   >
   >在简单表达式编辑器中，并非所有运算符都可用，它们取决于数据类型。 例如，对于字符串类型的字段，可以使用“包含”或“等于”。
   >
   >如果在创建事件后使用新的枚举值修改架构，则需要按照以下步骤将更改应用于现有事件：从事件字段中取消选择枚举字段，确认选择，然后再次选择枚举字段。 此时将显示新的枚举值。

1. 添加标识类型。 此步骤是可选的，但还是建议您添加标识类型，以便您利用实时客户资料服务中存储的信息。 它定义事件具有的键类型。有关详细信息，请参阅[此部分](../event/about-creating.md#select-the-namespace)。

1. 定义用户档案标识符：从有效负荷字段中选择一个字段，或定义一个公式以标识与事件关联的个人。 如果您选择身份类型，此键将自动设置（但仍可编辑）。 事实上，历程会选取应与身份类型对应的键（例如，如果您选择了电子邮件身份类型，则会选择电子邮件键）。 有关详细信息，请参阅[此部分](../event/about-creating.md#define-the-event-key)。

   ![](assets/jo-event7.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。

   事件现已配置完毕，可随时投入旅程。还需要其他配置步骤以接收事件。请参阅[此页](../event/additional-steps-to-send-events-to-journey.md)。

## 定义有效负载字段 {#define-the-payload-fields}

有效负载定义允许您选择系统预计从历程中的事件接收的信息，以及用于识别哪个人员与事件关联的键。 有效负载基于Experience Cloud XDM字段定义。 有关XDM的详细信息，请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}。

1. 从列表中选择XDM架构，然后单击&#x200B;**[!UICONTROL 字段]**&#x200B;字段或&#x200B;**[!UICONTROL 编辑]**&#x200B;图标。

   ![](assets/journey8.png)

   将显示架构中定义的所有字段。 字段列表因架构而异。 您可以搜索特定字段，或使用过滤器显示所有节点和字段或仅显示选定的字段。 根据架构定义，某些字段可能是必填字段，并且已预先选择。 不能取消选择它们。 默认情况下，选择历程正确接收事件所必需的所有字段。

   >[!NOTE]
   >
   >对于系统生成的事件，请确保已将“编排”字段组添加到XDM架构。 这将确保您的架构包含使用[!DNL Journey Optimizer]所需的所有信息。

   ![](assets/journey9.png)

1. 选择您希望从事件接收的字段。 这些是业务用户在历程中将利用的字段。 它们还必须包含用于识别与事件关联的人员的键（请参阅[此部分](../event/about-creating.md#define-the-event-key)）。

   >[!NOTE]
   >
   >对于系统生成的事件，**[!UICONTROL eventID]**&#x200B;字段会自动添加到所选字段列表中，以便[!DNL Journey Optimizer]可以识别该事件。 推送事件的系统不应生成ID，它应使用有效负载预览中可用的ID。 请参阅[此小节](../event/about-creating.md#preview-the-payload)。

1. 选择完所需的字段后，单击&#x200B;**[!UICONTROL 确定]**&#x200B;或按&#x200B;**[!UICONTROL Enter]**。

   所选字段的数目显示在&#x200B;**[!UICONTROL 字段]**&#x200B;字段中。

   ![](assets/journey12.png)

## 选择身份标识类型 {#select-the-namespace}

>[!CONTEXTUALHELP]
>id="ajo_journey_namespace"
>title="身份标识类型"
>abstract="选择用于标识与事件关联的客户轮廓的键。"

身份类型（以前称为“namespace”）允许您定义用于识别与事件关联的人员的键类型。 其配置是可选的。 如果您想在历程中检索来自[实时客户个人资料](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}的其他信息，则需要此项。 如果您仅使用来自第三方系统的数据（通过自定义数据源），则不需要标识类型定义。

您可以使用现有的身份类型或使用Adobe Experience Platform Identity服务创建新身份类型。 请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=zh-Hans){target="_blank"}以了解详情。

如果选择具有主标识的架构，则将预填充&#x200B;**[!UICONTROL Profiler标识符]**&#x200B;和&#x200B;**[!UICONTROL 标识类型]**&#x200B;字段。 如果未定义标识，我们选择&#x200B;_identityMap > id_&#x200B;作为主键。 然后，您必须选择身份类型，并使用&#x200B;_identityMap > id_&#x200B;预填充键（在&#x200B;**[!UICONTROL 身份类型]**&#x200B;字段下）。

选择字段时，将标记主要标识字段。

![](assets/primary-identity.png)

从下拉列表中选择标识类型。

![](assets/journey17.png)

每个历程只允许一个标识类型。 如果您在同一历程中使用多个事件，则需要使用相同的标识类型。 请参阅[此页](../building-journeys/journey.md)。

>[!NOTE]
>
>您只能选择基于人员的身份类型。 如果您为查找表定义了标识类型（例如：产品查找的ProductID标识类型），则该标识类型在&#x200B;**标识类型**&#x200B;下拉列表中不可用。

## 定义用户档案标识符 {#define-the-event-key}

键是字段或字段组合，它是事件有效负载数据的一部分，允许系统识别与事件关联的人员。 例如，键可以是Experience Cloud ID、CRM ID或电子邮件地址。

要使用存储在Adobe实时客户个人资料数据库中的数据，事件键必须是您在[实时客户个人资料服务](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}中定义为个人资料身份的信息。

用户档案标识符允许系统在事件和个人用户档案之间执行协调。 如果选择具有主标识的架构，则将预填充&#x200B;**[!UICONTROL 配置文件标识符]**&#x200B;和&#x200B;**[!UICONTROL 标识类型]**&#x200B;字段。 如果未定义标识，则&#x200B;_identityMap > id_&#x200B;是主键。 然后，您必须选择一个标识类型，并使用&#x200B;_identityMap > id_&#x200B;自动预填该键。

选择字段时，将标记主要标识字段。

![](assets/primary-identity.png)

如果您需要使用其他密钥，如CRM ID或电子邮件地址，则需要手动添加该密钥，如下所述：

1. 单击&#x200B;**[!UICONTROL 用户档案标识符]**&#x200B;字段内或铅笔图标。

   ![](assets/journey16.png)

1. 在有效负载字段列表中选择已选作键的字段。

当接收到事件时，该键的值允许系统识别与该事件相关联的人员。 与[标识类型](../event/about-creating.md#select-the-namespace)关联的键，可用于对Adobe Experience Platform执行查询。 查看[此页面](../building-journeys/about-journey-activities.md#orchestration-activities)。
密钥还用于检查人员是否正在旅程中。 事实上，一个人在同一历程中不能位于两个不同的位置。 因此，系统不允许相同的键（例如键CRMID=3224）位于同一历程的不同位置。

## 高级表达式编辑器 {#adv-exp-editor}

在定义事件ID条件或用户档案标识符时，您可以切换到高级表达式编辑器以创建更复杂的键（例如，两个事件字段的串联）。

![](assets/journey20.png)

如果要执行其他操作，可以从&#x200B;**[!UICONTROL 高级模式]**&#x200B;按钮访问高级表达式函数。 利用这些函数，可处理用于执行特定查询的值，例如更改格式、执行字段连接，同时仅考虑字段的一部分（例如，前10个字符）。 请参阅此[页面](../building-journeys/expression/expressionadvanced.md)。


## 预览有效负载 {#preview-the-payload}

有效负载预览允许您验证有效负载定义。

>[!NOTE]
>
>对于系统生成的事件，在创建事件时，在查看有效负载预览之前，请保存事件并重新打开它。 在有效负载中生成事件ID时需要此步骤。

1. 单击&#x200B;**[!UICONTROL 查看有效负载]**&#x200B;图标可预览系统所需的有效负载。

   ![](assets/journey13.png)

   您可以注意到已选择的字段已显示。

   ![](assets/journey14.png)

1. 检查预览以验证有效负载定义。

1. 然后，您可以将有效负载预览与共享给负责事件发送的人员。 此有效负载可以帮助他们设计推送到[!DNL Journey Optimizer]的事件的设置。 请参阅[此页](../event/additional-steps-to-send-events-to-journey.md)。
