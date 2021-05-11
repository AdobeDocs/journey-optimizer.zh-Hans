---
title: 反应事件
description: 了解反应事件
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 2%

---

# 反应事件 {#section_dhx_gss_dgb}

![](../assets/do-not-localize/badge.png)

在调色板中提供的不同事件活动中，您会找到内置的&#x200B;**[!UICONTROL Reactions]**&#x200B;事件。 此活动允许您对与同一旅程中发送的消息相关的跟踪数据做出响应。 我们会在与Adobe Experience Platform共享时实时捕获此信息。 对于推送通知，您可以对单击、发送或失败的消息做出响应。 对于SMS消息，您可以对已发送或失败的消息做出响应。 对于电子邮件，您可以对单击、发送、打开或失败的消息做出响应。

您还可以使用此机制在消息没有反应时执行操作。 为此，请创建与反应活动平行的第二条路径并添加等待活动。 如果在等待活动中定义的期间内没有反应，则将选择第二条路径。 例如，您可以选择发送后续消息。

请注意，只有在前面有&#x200B;**Message**&#x200B;活动时，才能在画布中使用反应活动。

请参阅[关于操作活动](../building-journeys/about-journey-activities.md#action-activities)。

![](../assets/journey45.png)

以下是配置反应事件的不同步骤：

1. 将&#x200B;**[!UICONTROL Label]**&#x200B;添加到反应中。 此步骤是可选的。
1. 从下拉列表中，选择要对其做出响应的操作活动。 您可以选择位于路径的前几步中的任何操作活动。
1. 根据您选择的操作，选择要对其做出响应的内容。
1. 您可以定义事件超时（40秒到30天之间）和超时路径。 这将为未在定义持续时间内做出响应的个人创建第二条路径。 测试使用反应事件的旅程时，测试模式&#x200B;**[!UICONTROL Wait time]**&#x200B;的默认值和最小值为40秒。 请参阅[此小节](../building-journeys/testing-the-journey.md)。

>[!NOTE]
>
>
>反应事件无法跟踪在不同旅程中发生的消息。
>
>反应事件跟踪“跟踪”类型链接的点击。 退订和镜像页面链接未被考虑在内。

>[!IMPORTANT]
>
>电子邮件客户端（如Gmail）允许图像阻止。 打开的电子邮件使用电子邮件中包含的0像素图像进行跟踪。 如果图像被阻止，则打开的电子邮件将不会被考虑在内。
