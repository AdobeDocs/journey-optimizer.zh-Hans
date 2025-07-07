---
solution: Journey Optimizer
product: journey optimizer
title: 在测试或发布历程之前排除错误
description: 了解如何在测试或发布历程之前对错误进行故障排除
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 故障排除，故障排除，历程，检查，错误
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: 61498b61f7f05e0553fe575c980fd1bee08500a3
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 40%

---

# 在测试历程之前排除错误 {#troubleshooting}

在此部分中，了解如何在测试或发布之前对历程进行故障排除。 当历程处于测试模式或历程处于实时状态时，可以执行以下列出的所有检查。建议在测试模式下进行以下所有检查，然后继续发布。在[此页面](../building-journeys/testing-the-journey.md)上了解有关测试模式的更多信息。

了解如何排查历程事件、检查用户档案是否进入您的历程、用户档案如何浏览历程以及是否在此页面[上发送](troubleshooting-execution.md)消息。

如果您使用入站操作，请在此页面[上了解如何对其进行故障排除](troubleshooting-inbound.md)。

## 活动中的错误 {#activity-errors}

测试和发布历程之前，请验证所有活动均已正确配置。如果系统仍检测到错误，则无法执行测试或发布。

出现错误时，画布上的活动本身会显示警告符号。将光标放在感叹号上以显示错误消息。如果选择活动，您应该会看到带警告的错误行。 例如：

* 如果必填字段为空，则会显示错误

  ![](assets/journey63.png)

* 在画布中，当两个活动断开连接时，会显示警告

  ![](assets/canvas-disconnected.png)

## 历程中的错误 {#canvas-errors}

画布上方的&#x200B;**[!UICONTROL 警报]**&#x200B;按钮上也显示错误。 此按钮让您看到系统检测到的错误，这些错误会阻止测试模式激活或历程发布。

系统检测到两种问题：**错误**&#x200B;和&#x200B;**警告**。 错误阻止发布和测试激活。警告指示未阻止测试激活或发布的潜在问题。您将看到问题的描述和 ERR_XXX_XXX 类型的问题日志 ID。这有助于确定问题。

![](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

历程全局的错误和警告首先在列表中显示。之后，与特定活动相关的错误和警告按活动顺序或在历程中的出现顺序从左到右列出。在警报列表的底部，**[!UICONTROL 复制详细信息]**&#x200B;按钮允许您复制有关历程的技术信息，这些信息对解决问题很有用。

## 添加替代路径 {#canvas-add-path}

您可以为以下历程活动定义一个发生错误时的回退操作： **[!UICONTROL 条件]**&#x200B;和&#x200B;**[!UICONTROL 操作]**。

当操作或条件中发生错误时，个人历程将停止。使其得以继续的唯一方法是解决问题。 为避免中断历程，您还可以选中选项&#x200B;**[!UICONTROL 在活动属性中出现超时或错误时添加替代路径]**。 有关详细信息，请参阅[此部分](../building-journeys/using-the-journey-designer.md#paths)。
