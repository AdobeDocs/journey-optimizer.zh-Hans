---
solution: Journey Optimizer
product: journey optimizer
title: 历程活动入门
description: 历程活动入门
feature: Journeys, Activities, Overview
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 历程，活动，入门，事件，操作
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 503bedc30c35305537c62f9452f4a2dc07424523
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 12%

---

# 历程活动入门 {#about-journey-activities}

结合不同的事件、编排和操作活动，构建多步骤跨渠道方案。

## 事件活动 {#event-activities}

个性化历程由事件触发，例如在线购买。 用户档案进入历程后，将作为一个个人进行移动，并且没有两个个人以相同的速度或沿着相同的路径移动。 通过事件开始历程时，会在收到事件时触发历程。 然后，历程中的每个人分别遵循历程中定义的后续步骤。

技术用户配置的事件（请参阅[此页面](../event/about-events.md)）均显示在屏幕左侧的面板的第一个类别中。 可以使用以下事件活动：

* [一般事件](../building-journeys/general-events.md)
* [反应](../building-journeys/reaction-events.md)
* [受众资格](../building-journeys/audience-qualification-events.md)

![](assets/journey43.png)

通过拖放事件活动开始您的历程。 您还可以双击该图标。

![](assets/journey44.png)

## 编排活动 {#orchestration-activities}

编排活动是不同的条件，可帮助确定历程的下一步骤。 可以是，此人是否拥有未结支持案例，当前位置的天气预报，是否完成购买或达到10,000个忠诚度点数。

在屏幕左侧的面板中，提供了以下编排活动：

* [条件](../building-journeys/condition-activity.md)
* [等待](../building-journeys/wait-activity.md)
* [读取受众](../building-journeys/read-audience.md)

![](assets/journey49.png)

## 操作活动 {#action-activities}

操作是指您希望由于某种类型的触发而发生的操作，例如发送消息。 这是客户体验的历程。

从屏幕左侧的调色板，在&#x200B;**[!UICONTROL 事件]**&#x200B;和&#x200B;**[!UICONTROL 编排]**&#x200B;下方，可以找到&#x200B;**[!UICONTROL 操作]**&#x200B;类别。 可以使用以下操作活动：

* [内置渠道操作](../building-journeys/journeys-message.md)
* [自定义操作](../building-journeys/using-custom-actions.md)
* [跳转](../building-journeys/jump.md)

![](assets/journey58.png)

这些活动代表各种的可用通信渠道。您可以将它们组合在一起，创建跨渠道方案。

<!--If you have configured custom actions, they also appear here. [Learn more](../building-journeys/using-custom-actions.md)-->

您还可以设置向您发送消息的特定操作：

* 如果您使用第三方系统来发送消息，则可以创建特定的自定义操作。 [了解详情](../action/action.md)

* 如果您使用的是Campaign和Journey Optimizer，请参阅以下部分：

   * [[!DNL Journey Optimizer]和Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer]和Campaign Standard](../action/acs-action.md)

## 最佳实践 {#best-practices}

### 添加标签

大多数活动允许您定义&#x200B;**[!UICONTROL 标签]**。 这会在名称中添加一个后缀，该后缀将显示在画布的活动下方。 如果您在历程中多次使用同一活动，并且希望更轻松地识别它们，则此功能非常有用。 这样还可以使错误时的调试更容易，并使报告更易于阅读。 您还可以添加可选的&#x200B;**[!UICONTROL 描述]**。

![](assets/journey-action-label.png)

>[!NOTE]
>
>对于某些活动，其ID也会显示在窗格中。 在报表中，此ID可用作比标签更稳定的键，标签会发生变化。

### 管理高级参数 {#advanced-parameters}

大多数活动会显示许多您无法修改的高级和/或技术参数。

![](assets/journey-advanced-parameters.png)

为了提高可读性，您可以使用&#x200B;**[!UICONTROL 隐藏只读字段]**&#x200B;按钮来隐藏这些参数。

![](assets/journey-hide-read-only-fields.png)

在某些特定上下文中，您可以覆盖这些参数的值以供特定使用。 要强制使用某个值，请单击字段右侧的&#x200B;**[!UICONTROL 启用参数覆盖]**&#x200B;图标。[了解详情](../configuration/primary-email-addresses.md#journey-parameters)

![](assets/journey-enable-parameter-override.png)

### 添加替代路径

当操作或条件中发生错误时，个人历程将停止。使其继续的唯一方法是选中框&#x200B;**[!UICONTROL 在超时或错误的情况下添加替代路径]**。 请参阅[此小节](../building-journeys/using-the-journey-designer.md#paths)。

![](assets/journey42.png)
