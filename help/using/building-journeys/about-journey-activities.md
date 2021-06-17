---
title: 关于历程活动
description: 了解历程活动
feature: 历程
topic: 内容管理
role: User
level: Intermediate
source-git-commit: 9e152f50c2360010d83ffccbe536380879ffb5da
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 30%

---

# 关于历程活动 {#about-journey-activities}

结合不同的事件、编排和操作活动，构建多步跨渠道方案。

## 事件活动 {#event-activities}

技术用户配置的事件（请参阅[此页面](../event/about-events.md)）全部显示在屏幕左侧面板的第一个类别中。 可以使用以下事件活动：

* [一般事件](../building-journeys/general-events.md)
* [反应](../building-journeys/reaction-events.md)
* [区段鉴别](../building-journeys/segment-qualification-events.md)

![](../assets/journey43.png)

通过拖放事件活动以开始您的历程。 您还可以双击该页面。

![](../assets/journey44.png)

## 编排活动 {#orchestration-activities}

从屏幕左侧的面板中，可以使用以下编排活动：

* [条件](../building-journeys/condition-activity.md)
* [终止 ](../building-journeys/end-activity.md)
* [等待](../building-journeys/wait-activity.md)
* [读取区段](../building-journeys/read-segment.md)

![](../assets/journey49.png)

## 操作活动 {#action-activities}

从屏幕左侧的面板中，在&#x200B;**[!UICONTROL Events]**&#x200B;和&#x200B;**[!UICONTROL Orchestration]**&#x200B;下方，您将找到&#x200B;**[!UICONTROL Actions]**&#x200B;类别。 可使用以下操作活动：

* [消息](../building-journeys/journeys-message.md)
* [自定义操作](../building-journeys/using-custom-actions.md)
* [跳转](../building-journeys/jump.md)

![](../assets/journey58.png)

这些活动代表各种的可用通信渠道。您可以将它们组合在一起，以创建跨渠道方案。

如果已配置自定义操作，则它们将显示在此处（请参阅[此页面](../building-journeys/using-custom-actions.md)）。

## 最佳实践 {#best-practices}

大多数活动都允许您定义&#x200B;**[!UICONTROL Label]**。 这会为将在画布中活动下方显示的名称添加后缀。 如果您在历程中多次使用同一活动并希望更轻松地识别它们，则此功能非常有用。 它还可以在出错时更轻松地进行调试，并且还可以更轻松地阅读报表。 您还可以添加一个可选的&#x200B;**[!UICONTROL Description]**。

![](../assets/journey59bis.png)

当操作或条件中发生错误时，个人历程将停止。使其继续的唯一方法是选中 **[!UICONTROL Add an alternative path in case of a timeout or an error]** 框。请参阅[此章节](../building-journeys/using-the-journey-designer.md#paths)。

![](../assets/journey42.png)
