---
solution: Journey Optimizer
product: journey optimizer
description: 了解历程活动
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 22%

---

# 关于历程活动 {#about-journey-activities}

结合不同的事件、编排和操作活动，构建多步跨渠道方案。

## 事件活动 {#event-activities}

技术用户配置的事件(请参阅 [本页](../event/about-events.md))都显示在屏幕左侧面板的第一个类别中。 可以使用以下事件活动：

* [一般事件](../building-journeys/general-events.md)
* [反应](../building-journeys/reaction-events.md)
* [区段鉴别](../building-journeys/segment-qualification-events.md)

![](assets/journey43.png)

通过拖放事件活动以开始您的历程。 您还可以双击该页面。

![](assets/journey44.png)

## 编排活动 {#orchestration-activities}

从屏幕左侧的面板中，可以使用以下编排活动：

* [条件](../building-journeys/condition-activity.md)
* [等待](../building-journeys/wait-activity.md)
* [读取区段](../building-journeys/read-segment.md)

![](assets/journey49.png)

## 操作活动 {#action-activities}

从屏幕左侧的面板，下方 **[!UICONTROL 事件]** 和 **[!UICONTROL 编排]**，您将找到 **[!UICONTROL 操作]** 类别。 可使用以下操作活动：

* [电子邮件、短信、推送](../building-journeys/journeys-message.md)
* [自定义操作](../building-journeys/using-custom-actions.md)
* [跳转](../building-journeys/jump.md)

![](assets/journey58.png)

这些活动代表各种的可用通信渠道。您可以将它们组合在一起，以创建跨渠道方案。

如果您配置了自定义操作，则它们将显示在此处(请参阅 [本页](../building-journeys/using-custom-actions.md))。

## 最佳实践 {#best-practices}

大多数活动都允许您定义 **[!UICONTROL 标签]**. 这会为将在画布中活动下方显示的名称添加后缀。 如果您在历程中多次使用同一活动并希望更轻松地识别它们，则此功能非常有用。 它还可以在出错时更轻松地进行调试，并且还可以更轻松地阅读报表。 您还可以添加一个可选 **[!UICONTROL 描述]**.

![](assets/journey59bis.png)

当操作或条件中发生错误时，个人历程将停止。使其继续的唯一方法是选中方框 **[!UICONTROL 在出现超时或错误时添加替代路径]**. 请参阅[此小节](../building-journeys/using-the-journey-designer.md#paths)。

![](assets/journey42.png)
