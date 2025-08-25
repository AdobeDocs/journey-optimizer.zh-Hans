---
solution: Journey Optimizer
product: journey optimizer
title: 配置业务事件
description: 了解如何创建商业活动
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: 事件、历程、业务、配置
exl-id: 39eb40e1-d7f5-4a8e-9b64-c620940d5ff2
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 12%

---

# 配置业务事件 {#configure-a-business-event}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_business"
>title="业务事件"
>abstract="事件配置让您可以定义 Journey Optimizer 将作为事件接收的信息。您可以使用多个事件（在历程的不同步骤中），而多个历程可以使用相同的事件。与单一事件不同，业务事件不链接到特定的轮廓。事件 ID 类型始终基于规则。"

与单一事件不同，业务事件不链接到特定的轮廓。事件ID类型始终基于规则。 在[此部分](../event/about-events.md)中阅读有关业务事件的更多信息。

基于受众的读取历程可以在事件发生时由调度程序定期或业务事件一次性触发。

业务事件可以是“产品重新上架”、“公司股价达到一定价值”等。

>[!NOTE]
>
>您还可以观看业务事件用例[教程](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-business-event.html)。 请注意，不需要为配置文件启用架构。

## 重要说明 {#important-notes}

* 只有时间序列架构可用。 体验事件、决策事件和历程步骤事件架构不可用。
* 事件架构必须包含不基于人员的主标识。 定义事件时必须选择以下字段： `_id`和`timestamp`
* 业务事件只能作为历程的第一步放置。
* 将业务事件作为历程的第一步删除时，历程的调度程序类型将为“业务事件”。
* 在业务事件后，只能删除读取受众活动。 它会自动添加为下一步。
* 要允许多个业务事件执行，请在历程属性的&#x200B;**[!UICONTROL 执行]**&#x200B;部分中激活相应的选项。
* 触发业务事件后，将延迟一段时间以将受众导出15分钟到1小时。
* 测试业务事件时，必须传递事件参数和将进入测试历程的测试用户档案的标识符。 此外，在测试基于业务事件的历程时，您只能触发单个用户档案进入。 请参阅[此部分](../building-journeys/testing-the-journey.md#test-business)。 在测试模式下，没有“代码视图”模式可用。
* 如果新的业务事件到达，当前正在历程中的个人会发生什么情况？ 它的行为与当新循环发生时个人仍处于循环历程中的情况相同。 他们的道路已经结束。 因此，营销人员必须注意避免在预计业务事件频繁时构建过长的历程。
* 业务事件无法与单一事件或受众资格筛选活动结合使用。

## 多个业务事件 {#multiple-business-events}

下面是一些重要说明，适用于连续接收多个业务事件时。

**当历程正在进行时，接收业务事件时的行为是什么？**

业务事件遵循的重新进入规则与单一事件的方式相同。 如果历程允许重新进入，则将处理下一个业务事件。

**避免过度加载具体化受众的护栏是什么？**

对于拍摄业务事件，对于给定历程，第一个事件作业推送的数据会在1小时时间范围内重用一次。 对于计划的历程，没有护栏。 在[Adobe Experience Platform Segmentation Service文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hans)中了解有关受众的更多信息。

## 商业活动入门 {#gs-business-events}

以下是配置业务事件的首要步骤：

1. 在“管理”菜单部分中，选择&#x200B;**[!UICONTROL 配置]**。 在&#x200B;**[!UICONTROL 事件]**&#x200B;部分中，单击&#x200B;**[!UICONTROL 管理]**。 将显示事件列表。

   ![](assets/jo-event1.png)

1. 单击&#x200B;**[!UICONTROL 创建事件]**&#x200B;以创建新事件。 事件配置窗格将在屏幕右侧打开。

   ![](assets/jo-event2.png)

1. 输入事件的名称。 您还可以添加描述。

   ![](assets/jo-event3-business.png)

   >[!NOTE]
   >
   >只允许使用字母数字字符和下划线。 最大长度为30个字符。

1. 在&#x200B;**[!UICONTROL 类型]**&#x200B;字段中，选择&#x200B;**业务**。

   ![](assets/jo-event3bis-business.png)

1. 使用此事件的历程数显示在&#x200B;**[!UICONTROL 在]**&#x200B;中使用字段中。 您可以单击&#x200B;**[!UICONTROL 查看历程]**&#x200B;图标以显示使用此事件的历程列表。

1. 定义架构和有效负载字段：在这里，您可以选择历程预期接收的事件信息（或有效负载）。 您稍后将在历程中使用这些信息。 请参阅[此小节](../event/about-creating-business.md#define-the-payload-fields)。

   ![](assets/jo-event5-business.png)

   只有时间序列架构可用。 `Experience Events`、`Decision Events`和`Journey Step Events`架构不可用。 事件架构必须包含不基于人员的主标识。 定义事件时必须选择以下字段： `_id`和`timestamp`

   ![](assets/test-profiles-4.png)

1. 在&#x200B;**[!UICONTROL 事件ID条件]**&#x200B;字段中单击。 使用简单表达式编辑器定义条件，系统使用它来识别触发历程的事件。

   ![](assets/jo-event6-business.png)

   在我们的示例中，我们根据产品ID编写了条件。 这意味着每当系统收到与此条件匹配的事件时，它都会将其传递给历程。

   >[!NOTE]
   >
   >在简单表达式编辑器中，并非所有运算符都可用，它们取决于数据类型。 例如，对于字符串类型的字段，可以使用“包含”或“等于”。

1. 单击&#x200B;**[!UICONTROL 保存]**。

   ![](assets/journey7-business.png)

   事件现已配置完毕，可随时投入旅程。还需要其他配置步骤以接收事件。请参阅[此页面](../event/additional-steps-to-send-events-to-journey.md)以了解详情。

## 定义有效负载字段 {#define-the-payload-fields}

有效负载定义允许您选择系统预计从历程中的事件接收的信息，以及用于识别哪个人员与事件关联的键。 有效负载基于Experience Cloud XDM字段定义。 有关XDM的详细信息，请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target="_blank"}。

1. 从列表中选择XDM架构，然后单击&#x200B;**[!UICONTROL 字段]**&#x200B;字段或&#x200B;**[!UICONTROL 编辑]**&#x200B;图标。

   ![](assets/journey8-business.png)

   将显示架构中定义的所有字段。 字段列表因架构而异。 您可以搜索特定字段，或使用过滤器显示所有节点和字段或仅显示选定的字段。 根据架构定义，某些字段可能是必填字段，并且已预先选择。 不能取消选择它们。 默认情况下，选择历程正确接收事件所必需的所有字段。

   ![](assets/journey9-business.png)

   >[!NOTE]
   >
   > 确保选择以下字段： `_id`和`timestamp`

1. 选择您希望从事件接收的字段。 这些是业务用户在历程中将利用的字段。

1. 选择完所需的字段后，单击&#x200B;**[!UICONTROL 保存]**&#x200B;或按&#x200B;**[!UICONTROL Enter]**。

   所选字段的数目显示在&#x200B;**[!UICONTROL 字段]**&#x200B;中。

   ![](assets/journey12-business.png)

## 预览有效负载 {#preview-the-payload}

使用有效负载预览以验证有效负载定义。

1. 单击&#x200B;**[!UICONTROL 查看有效负载]**&#x200B;图标可预览系统所需的有效负载。

   ![](assets/journey13-business.png)

   您可以注意到已选择的字段已显示。

   ![](assets/journey14-business.png)

1. 检查预览以验证有效负载定义。

1. 然后，您可以将有效负载预览与共享给负责事件发送的人员。 此有效负载可以帮助他们设计推送到[!DNL Journey Optimizer]的事件的设置。 请参阅[此页](../event/additional-steps-to-send-events-to-journey.md)。
