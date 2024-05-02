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
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '1605'
ht-degree: 12%

---

# 配置单一事件 {#configure-an-event}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_unitary"
>title="单一事件"
>abstract="事件配置让您可以定义 Journey Optimizer 将作为事件接收的信息。您可以使用多个事件（在历程的不同步骤中），而多个历程可以使用相同的事件。单一事件链接到特定配置文件。它们可以基于规则，也可以由系统生成。"

单一事件链接到特定配置文件。它们可以是基于规则的，也可以是系统生成的。  阅读有关单一事件的更多信息 [本节](../event/about-events.md).

以下是配置新事件的首要步骤：

1. 在“管理”菜单部分中，选择 **[!UICONTROL 配置]**. 在  **[!UICONTROL 活动]** 部分，单击 **[!UICONTROL 管理]**. 将显示事件列表。

   ![](assets/jo-event1.png)

1. 单击 **[!UICONTROL 创建事件]** 以创建新事件。 事件配置窗格将在屏幕右侧打开。

   ![](assets/jo-event2.png)

1. 输入事件的名称。 您还可以添加描述。

   ![](assets/jo-event3.png)

   >[!NOTE]
   >
   >只允许使用字母数字字符和下划线。 最大长度为30个字符。

1. 在 **[!UICONTROL 类型]** 字段，选择 **单一**.

   ![](assets/jo-event3bis.png)

1. 在 **[!UICONTROL 事件ID类型]** 字段中，选择要使用的事件ID类型： **基于规则** 或 **系统生成**. 有关事件ID类型的更多信息，请参阅 [本节](../event/about-events.md#event-id-type).

   ![](assets/jo-event4.png)

1. 使用此事件的旅程数显示在 **[!UICONTROL 使用位置]** 字段。 您可以单击 **[!UICONTROL 查看历程]** 图标，以显示使用此事件的旅程列表。

1. 定义架构和有效负载字段：在这里，您可以选择历程预期接收的事件信息（通常称为有效负载）。 然后，您便能够在旅程中使用这些信息。请参阅[此小节](../event/about-creating.md#define-the-payload-fields)。

   ![](assets/jo-event5.png)

   >[!NOTE]
   >
   >当您选择 **[!UICONTROL 系统生成]** 类型，则只有具有eventID类型字段的架构可用。 当您选择 **[!UICONTROL 基于规则]** 类型，则所有体验事件架构都可用。

1. 对于基于规则的事件，请单击 **[!UICONTROL 事件ID条件]** 字段。 使用简单表达式编辑器，定义系统将使用的条件，以识别将触发历程的事件。
   ![](assets/jo-event6.png)

   在我们的示例中，我们根据用户档案所在的城市编写了条件。 这意味着每当系统收到与此条件(**[!UICONTROL 城市]** 字段和 **[!UICONTROL 巴黎]** 值)，它会将其传递到历程。

   >[!NOTE]
   >
   >定义时，高级表达式编辑器不可用 **[!UICONTROL 事件ID条件]**. 在简单表达式编辑器中，并非所有运算符都可用，它们取决于数据类型。 例如，对于字符串类型的字段，可以使用“包含”或“等于”。
   >
   >如果在创建事件后使用新的枚举值修改架构，则需要按照以下步骤将更改应用于现有事件：从事件字段中取消选择枚举字段，确认选择，然后再次选择枚举字段。 此时将显示新的枚举值。

1. 添加命名空间。此步骤是可选的，但还是建议您添加命名空间，以便您利用实时客户资料服务中存储的信息。它定义事件具有的键类型。请参阅[此小节](../event/about-creating.md#select-the-namespace)。

1. 定义用户档案标识符：从有效负荷字段中选择一个字段，或定义一个公式以标识与事件关联的个人。 如果您选择命名空间，此键将自动设置（但仍可编辑）。事实上，历程会选取应与命名空间对应的键（例如，如果您选择了电子邮件命名空间，则会自动选择电子邮件键）。 请参阅[此小节](../event/about-creating.md#define-the-event-key)。

   ![](assets/jo-event7.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。

   事件现已配置完毕，可随时投入旅程。还需要其他配置步骤以接收事件。请参阅[此页](../event/additional-steps-to-send-events-to-journey.md)。

## 定义有效负载字段 {#define-the-payload-fields}

有效负载定义允许您选择系统预计从历程中的事件接收的信息，以及用于识别哪个人员与事件关联的键。 有效负载基于Experience CloudXDM字段定义。 有关XDM的详细信息，请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target="_blank"}.

1. 从列表中选择一个XDM架构，然后单击 **[!UICONTROL 字段]** 字段或在 **[!UICONTROL 编辑]** 图标。

   ![](assets/journey8.png)

   将显示架构中定义的所有字段。 字段列表因架构而异。 您可以搜索特定字段，或使用过滤器显示所有节点和字段或仅显示选定的字段。 根据架构定义，某些字段可能是必填字段，并且已预先选择。 不能取消选择它们。 默认情况下，选择历程正确接收事件所必需的所有字段。

   >[!NOTE]
   >
   >对于系统生成的事件，请确保已将“编排”字段组添加到XDM架构。 这将确保您的架构包含与配合使用所需的所有信息 [!DNL Journey Optimizer].

   ![](assets/journey9.png)

1. 选择您希望从事件接收的字段。 这些是业务用户在历程中将利用的字段。 还必须包含用于识别与事件关联的人员的键(请参阅 [本节](../event/about-creating.md#define-the-event-key))。

   >[!NOTE]
   >
   >对于系统生成的事件， **[!UICONTROL eventID]** 字段会自动添加到所选字段的列表中，以便 [!DNL Journey Optimizer] 可以识别事件。 推送事件的系统不应生成ID，它应使用有效负载预览中可用的ID。 请参阅[此小节](../event/about-creating.md#preview-the-payload)。

1. 选择完所需的字段后，单击 **[!UICONTROL 确定]** 或按 **[!UICONTROL 输入]**.

   所选字段的数目显示在 **[!UICONTROL 字段]** 字段。

   ![](assets/journey12.png)

## 选择命名空间 {#select-the-namespace}

>[!CONTEXTUALHELP]
>id="ajo_journey_namespace"
>title="身份命名空间"
>abstract="选择用于标识与事件关联的客户配置文件的键。"

命名空间允许您定义用于识别与事件关联的人员的键类型。 其配置是可选的。 如果您想在历程中检索来自 [Real-time Customer Profile](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}. 如果您仅使用来自第三方系统的数据（通过自定义数据源），则不需要命名空间定义。

您可以使用其中一个预定义命名空间，也可以使用Identity Namespace Service创建新命名空间。 请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=zh-Hans){target="_blank"}.

如果选择具有主标识的架构，则 **[!UICONTROL Profiler标识符]** 和 **[!UICONTROL 命名空间]** 字段是预填充的。 如果未定义标识，我们将选择 _identityMap > id_ 作为主键。 然后，您必须选择一个命名空间，并且密钥将会预填充(位于 **[!UICONTROL 命名空间]** 字段)，使用 _identityMap > id_.

选择字段时，将标记主要标识字段。

![](assets/primary-identity.png)

从下拉列表中选择一个命名空间。

![](assets/journey17.png)

每个历程只允许一个命名空间。 如果您在同一历程中使用多个事件，则需要使用相同的命名空间。 请参阅[此页](../building-journeys/journey.md)。

>[!NOTE]
>
>您只能选择基于人员的身份命名空间。 如果您为查找表定义了命名空间（例如：产品查找的ProductID命名空间），则它将在 **命名空间** 下拉列表。

## 定义用户档案标识符 {#define-the-event-key}

键是字段或字段组合，它是事件有效负载数据的一部分，允许系统识别与事件关联的人员。 例如，键可以是Experience CloudID、CRM ID或电子邮件地址。

要使用存储在Adobe实时客户资料数据库中的数据，事件键必须是您在以下位置定义为用户档案标识的信息： [Real-time Customer Profile Service](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}.

用户档案标识符允许系统在事件和个人用户档案之间执行协调。 如果选择具有主标识的架构，则 **[!UICONTROL 配置文件标识符]** 和 **[!UICONTROL 命名空间]** 字段是预填充的。 如果未定义标识，则 _identityMap > id_ 是主键。 然后，您必须选择一个命名空间，并且密钥会使用自动预填充 _identityMap > id_.

选择字段时，将标记主要标识字段。

![](assets/primary-identity.png)

如果您需要使用其他密钥，如CRM ID或电子邮件地址，则需要手动添加该密钥，如下所述：

1. 在 **[!UICONTROL 配置文件标识符]** 字段或铅笔图标上。

   ![](assets/journey16.png)

1. 在有效负载字段列表中选择已选作键的字段。 您还可以切换到高级表达式编辑器以创建更复杂的键（例如，两个事件字段的串联）。

   ![](assets/journey20.png)

当接收到事件时，该键的值允许系统识别与该事件相关联的人员。 与命名空间关联(请参阅 [本节](../event/about-creating.md#select-the-namespace))，密钥可用于对Adobe Experience Platform执行查询。 请参阅 [此页面](../building-journeys/about-journey-activities.md#orchestration-activities).
密钥还用于检查人员是否正在旅程中。 事实上，一个人在同一历程中不能位于两个不同的位置。 因此，系统不允许相同的键（例如键CRMID=3224）位于同一历程的不同位置。

您还可以访问高级表达式函数(**[!UICONTROL 高级模式]**)。 利用这些函数，可处理用于执行特定查询的值，例如更改格式、执行字段连接，同时仅考虑字段的一部分（例如，前10个字符）。 请参阅此[页面](../building-journeys/expression/expressionadvanced.md)。

## 预览有效负载 {#preview-the-payload}

有效负载预览允许您验证有效负载定义。

>[!NOTE]
>
>对于系统生成的事件，在创建事件时，在查看有效负载预览之前，请保存事件并重新打开它。 在有效负载中生成事件ID时需要此步骤。

1. 单击 **[!UICONTROL 查看有效负荷]** 图标以预览系统所需的有效负载。

   ![](assets/journey13.png)

   您可以注意到已选择的字段已显示。

   ![](assets/journey14.png)

1. 检查预览以验证有效负载定义。

1. 然后，您可以将有效负载预览与共享给负责事件发送的人员。 此有效负载可以帮助他们设计推送到以下位置的事件设置： [!DNL Journey Optimizer]. 请参阅[此页](../event/additional-steps-to-send-events-to-journey.md)。
