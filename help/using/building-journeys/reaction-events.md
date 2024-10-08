---
solution: Journey Optimizer
product: journey optimizer
title: 反应事件
description: 了解反应事件
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 历程，事件，反应，跟踪，平台
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: 343e7bbebf35711259d2f3392f1ce5658865599a
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 20%

---

# 反应事件 {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="反应事件"
>abstract="您可以通过此活动，对在同一历程中与所发送消息相关的跟踪数据做出反应。我们在与 Adobe Experience Platform 共享时实时捕获此信息。"

在面板中可用的不同事件活动中，您会找到内置的&#x200B;**[!UICONTROL 反应]**&#x200B;事件。 您可以通过此活动，对在同一历程中与所发送消息相关的跟踪数据做出反应。我们在与 Adobe Experience Platform 共享时实时捕获此信息。

您可以对单击或打开的消息做出反应。

也可以使用此机制在消息没有反应时执行操作。 为此，请创建与反应活动平行的第二个路径，并添加等待活动。 如果在等待活动中定义的时段内没有反应，则将选择第二条路径。 例如，您可以选择发送跟进消息。

请注意，仅当之前（电子邮件和推送）存在渠道操作活动时，才可以在画布中使用反应活动。

请参阅[关于操作活动](../building-journeys/about-journey-activities.md#action-activities)。

![](assets/journey45.png)

以下是配置反应事件的不同步骤：

1. 向反应添加&#x200B;**[!UICONTROL 标签]**。 此步骤是可选的。
1. 从下拉列表中，选择要做出反应的操作活动。 您可以选择位于路径前面步骤中的任何操作活动。
1. 根据您选择的操作，选择要做出反应的内容。
1. 您可以定义事件超时（40秒到90天之间）和超时路径。 这会为未在定义的持续时间内做出反应的个人创建第二个路径。 测试使用反应事件的历程时，测试模式&#x200B;**[!UICONTROL 等待时间]**&#x200B;的默认值和最小值为40秒。 请参阅[此小节](../building-journeys/testing-the-journey.md)。

>[!NOTE]
>
>
>反应事件无法跟踪在其他历程中发生的消息。
>
>反应事件跟踪“已跟踪”类型链接的点击次数。 未考虑退订和镜像页面链接。

>[!IMPORTANT]
>
>Gmail等电子邮件客户端允许阻止图像。 使用电子邮件中包含的0像素图像跟踪电子邮件打开次数。 如果图像被阻止，则不会考虑电子邮件打开次数。
