---
title: 配置业务事件
description: 了解如何创建业务事件
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '818'
ht-degree: 14%

---

# 配置业务事件{#configure-a-business-event}

![](../assets/do-not-localize/badge.png)

与统一事件不同，业务事件不与特定用户档案关联。 事件ID类型始终基于规则。 请阅读[本节](../event/about-events.md)中有关业务事件的更多信息。

基于读取细分的旅程可通过一次性、定期调度程序或业务事件在事件发生时触发。

业务事件可以是“产品现货”、“公司的股价达到一定值”等。

## 重要说明

* 事件模式必须包含主标识。
* 业务事件只能作为旅程的第一步丢弃。
* 当将业务事件作为旅程的第一步时，旅程的调度程序类型将是“业务事件”。
* 在业务活动之后，只能删除读取区段事件。 它将自动添加为下一步。
* 业务事件的触发频率不能超过一小时。
* 触发业务事件后，将延迟将区段从15分钟导出到1小时。
* 在测试业务事件时，您必须传递事件参数和将进入测试旅程的测试用户档案的标识符。 此外，在测试基于业务事件的旅程时，您只能触发单个用户档案入口。 请参阅[此小节](../building-journeys/testing-the-journey.md#test-business)。在测试模式下，没有可用的“代码视图”模式。
* 如果新的业务事件到来，当前处于旅程中的个人会怎样？ 它的行为方式与当新的循环发生时，个人仍处于循环旅程时相同。 他们的路结束了。 因此，如果营销人员预期业务事件频繁，则必须注意避免构建过长的旅程。

## 业务事件

以下是配置业务事件的第一步：

1. 在左侧菜单中，单击&#x200B;**[!UICONTROL Admin]**&#x200B;图标，然后单击&#x200B;**[!UICONTROL Events]**。 将显示事件列表。

   ![](../assets/jo-event1.png)

1. 单击&#x200B;**[!UICONTROL Add]**&#x200B;以创建新事件。事件配置窗格将在屏幕右侧打开。

   ![](../assets/jo-event2.png)

1. 输入事件的名称。 您还可以添加说明。

   ![](../assets/jo-event3-business.png)

   >[!NOTE]
   >
   >请勿使用空格或特殊字符。请勿使用超过 30 个字符。

1. 在&#x200B;**[!UICONTROL Type]**&#x200B;字段中，选择&#x200B;**业务**。

   ![](../assets/jo-event3bis-business.png)

1. 使用此事件的旅程数显示在&#x200B;**[!UICONTROL Used in]**&#x200B;字段中。您可以单击 **[!UICONTROL View journeys]**&#x200B;图标，以显示使用此事件的旅程列表。

1. 定义模式和有效负荷字段：在这里，您选择事件信息（通常称为有效负荷），预计将接收的旅程。 然后，您便能够在旅程中使用这些信息。请参阅[此小节](../event/about-creating-business.md#define-the-payload-fields)。

   ![](../assets/jo-event5-business.png)

   仅时间系列模式可用。 体验事件、决策事件和历程步骤事件模式不可用。 事件模式必须包含主标识。

   ![](../assets/test-profiles-4.png)

1. 在&#x200B;**[!UICONTROL Event ID condition]**字段内单击。 使用简单的表达式编辑器，定义系统将使用的条件，以识别将触发您旅程的事件。
   ![](../assets/jo-event6-business.png)

   在示例中，我们根据产品的id编写了一个条件。 这意味着，每当系统收到与此条件匹配的事件时，它都会将其传递给旅程。

1. 单击 **[!UICONTROL Save]**。

   ![](../assets/journey7-business.png)

   事件现已配置完毕，可随时投入旅程。还需要其他配置步骤以接收事件。请参阅[此页](../event/additional-steps-to-send-events-to-journey-orchestration.md)。

## 定义有效负荷字段{#define-the-payload-fields}

有效负荷定义允许您选择系统希望从旅程中的事件接收的信息，以及确定与事件关联的人员的键。 负载基于Experience CloudXDM字段定义。 有关XDM的详细信息，请参阅[此页](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans)。

1. 从列表中选择一个XDM模式，然后单击&#x200B;**[!UICONTROL Payload]**&#x200B;字段或&#x200B;**[!UICONTROL Edit]**&#x200B;图标。

   ![](../assets/journey8-business.png)

   将显示模式中定义的所有字段。 字段的列表因模式而异。 您可以搜索特定字段或使用过滤器显示所有节点和字段，或仅显示所选字段。 根据模式定义，某些字段可能是必填的并且是预选的。 您无法取消选择它们。 默认情况下，对于要由旅程正确接收事件，必须填写的所有字段都处于选中状态。

   ![](../assets/journey9-business.png)

1. 选择要从事件接收的字段。 这些是业务用户在旅程中将利用的字段。

   ![](../assets/journey10-business.png)

1. 选择完所需字段后，单击&#x200B;**[!UICONTROL Save]**&#x200B;或按&#x200B;**[!UICONTROL Enter]**。

   选定字段的数目将显示在&#x200B;**[!UICONTROL Payload]**&#x200B;字段中。

   ![](../assets/journey12-business.png)

## 预览有效负荷{#preview-the-payload}

有效负荷预览允许您验证有效负荷定义。

1. 单击&#x200B;**[!UICONTROL View Payload]**&#x200B;图标以预览系统预期的有效负荷。

   ![](../assets/journey13-business.png)

   您可以注意到显示了选定的字段。

   ![](../assets/journey14-business.png)

1. 检查预览以验证有效负荷定义。

1. 然后，您可以将有效负荷预览共享给负责事件发送的人员。 此负载可帮助他设计推送到[!DNL Journey Optimizer]的事件的设置。 请参阅[此页](../event/additional-steps-to-send-events-to-journey-orchestration.md)。
