---
solution: Journey Optimizer
product: journey optimizer
title: 反应事件
description: 了解反应事件
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 历程，事件，反应，跟踪，平台
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 21%

---

# 反应事件 {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="反应事件"
>abstract="您可以通过此活动，对在同一历程中与所发送消息相关的跟踪数据做出反应。我们在与 Adobe Experience Platform 共享时实时捕获此信息。"

在面板中可用的不同事件活动中，您会找到 **[!UICONTROL 反应]** 事件。 您可以通过此活动，对在同一历程中与所发送消息相关的跟踪数据做出反应。我们在与 Adobe Experience Platform 共享时实时捕获此信息。

您可以对点击或打开的消息做出响应。

您还可以使用此机制在消息未受到任何反应时执行操作。 为此，请创建与反应活动平行的第二个路径，并添加等待活动。 如果在等待活动中定义的时间段内没有反应，则将选择第二个路径。 例如，您可以选择发送跟进消息。

请注意，仅当画布中之前存在渠道操作活动（电子邮件和推送）时，才能使用反应活动。

请参阅 [关于操作活动](../building-journeys/about-journey-activities.md#action-activities).

![](assets/journey45.png)

以下是配置反应事件的不同步骤：

1. 添加 **[!UICONTROL 标签]** 反应。 此步骤是可选的。
1. 从下拉列表中，选择要对其做出响应的操作活动。 您可以选择位于路径前面步骤中的任何操作活动。
1. 根据您选择的操作，选择要对哪些内容做出响应。
1. 您可以定义事件超时（在40秒到30天之间）和超时路径。 这将为未在定义的持续时间内做出反应的个人创建第二个路径。 测试使用反应事件的历程时，测试模式 **[!UICONTROL 等待时间]** 默认值和最小值为40秒。 请参阅[此小节](../building-journeys/testing-the-journey.md)。

>[!NOTE]
>
>
>反应事件无法跟踪在其他历程中发生的消息。
>
>反应事件跟踪“跟踪”类型链接的点击量。 未考虑退订和镜像页面链接。

>[!IMPORTANT]
>
>电子邮件客户端（如Gmail）允许图像阻止。 使用电子邮件中包含的0像素图像跟踪打开的电子邮件。 如果图像被阻止，则不会考虑打开的电子邮件。
