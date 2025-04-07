---
solution: Journey Optimizer
product: journey optimizer
title: 历程疑难解答
description: 了解如何对历程中的错误进行故障排除
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 故障排除，故障排除，历程，检查，错误
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '989'
ht-degree: 51%

---

# 对历程进行故障排除 {#troubleshooting}

在此部分中，了解如何在测试或发布之前对历程进行故障排除。 当历程处于测试模式或历程处于实时状态时，可以执行以下列出的所有检查。建议在测试模式下进行以下所有检查，然后继续发布。在[此页面](../building-journeys/testing-the-journey.md)上了解有关测试模式的更多信息。

作为管理员，您还可以通过直接从用户界面进行实际API调用来测试自定义操作配置。 在[此页面](../action/troubleshoot-custom-action.md)上了解详情。

## 测试之前检查错误 {#checking-for-errors-before-testing}

测试和发布历程之前，请验证所有活动均已正确配置。如果系统仍检测到错误，则无法执行测试或发布。


### 活动中的错误 {#activity-errors}

出现错误时，画布上的活动本身会显示警告符号。将光标放在感叹号上以显示错误消息。如果单击活动，您将看到带警告的错误行。例如：

* 如果必填字段为空，则会显示错误

  ![](assets/journey63.png)

* 在画布中，当两个活动断开连接时，会显示警告

  ![](assets/canvas-disconnected.png)

### 历程中的错误 {#canvas-errors}

画布上方的&#x200B;**[!UICONTROL 警报]**&#x200B;按钮上也显示错误。 此按钮让您看到系统检测到的错误，这些错误会阻止测试模式激活或历程发布。

系统检测到两种问题：**错误**&#x200B;和&#x200B;**警告**。 错误阻止发布和测试激活。警告指示未阻止测试激活或发布的潜在问题。您将看到问题的描述和 ERR_XXX_XXX 类型的问题日志 ID。这有助于确定问题。

![](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

历程全局的错误和警告首先在列表中显示。之后，与特定活动相关的错误和警告按活动顺序或在历程中的出现顺序从左到右列出。在警报列表的底部，**[!UICONTROL 复制详细信息]**&#x200B;按钮允许您复制有关历程的技术信息，这些信息对解决问题很有用。

### 添加替代路径 {#canvas-add-path}

您可以为以下历程活动定义一个发生错误时的回退操作： **[!UICONTROL 条件]**&#x200B;和&#x200B;**[!UICONTROL 操作]**。

当操作或条件中发生错误时，个人历程将停止。使其得以继续的唯一方法是解决问题。 为避免中断历程，您还可以选中选项&#x200B;**[!UICONTROL 在活动属性中出现超时或错误时添加替代路径]**。 有关详细信息，请参阅[此部分](../building-journeys/using-the-journey-designer.md#paths)。


## 检查事件是否正确发送 {#checking-that-events-are-properly-sent}

历程的起点永远是事件。您可以使用 Postman 等工具执行测试。

您可以检查通过这些工具发送的 API 调用是否正确发送。如果返回错误，则表示您的调用有问题。再次检查有效负载、标题（特别是组织 ID）以及目标 URL。您可以询问管理员要点击的正确 URL。

事件不会直接从源推送到历程。 事实上，历程依赖于Adobe Experience Platform的流摄取API。 因此，如果出现与事件相关的问题，您可以参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"}以了解流摄取API故障排除。

## 检查人员是否进入历程 {#checking-if-people-enter-the-journey}

历程报表实时衡量人员进入旅程。

如果您成功发送事件，但未看到有人进入历程，则意味着在事件发送和事件接收之间出现问题。

您可以通过以下问题开始进行故障诊断：

* 是否确定期待传入事件的历程处于测试模式或处于实时状态？
* 是否在从有效负载预览复制有效负载之前保存了您的事件？
* 您的事件有效负载是否包含事件 ID？
* 您是否点击了正确的 URL？
* 您是否使用“事件配置”窗格中的有效负载结构预览遵循了流摄取 API 的有效负载结构？请参阅[此页](../event/about-creating.md#preview-the-payload)。
* 您在事件标头中使用了正确的键值对吗？

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

## 检查人员在历程中的导航方式 {#checking-how-people-navigate-through-the-journey}

历程报表测量旅程中个人的进度。 很容易识别人员在何处被拦住以及为什么被拦住。

以下是一些要检查的内容：

* 是因为除人员外的情况吗？例如，条件为“性别=男性”，而该人员为女性。如果条件不太复杂，此检查可由商业用户执行。
* 是由于调用数据源时没有响应吗？当历程正在测试时，此信息可在测试模式日志中查看。当历程处于实时状态时，管理员可以测试对数据源的直接调用并检查收到的答案。管理员还可以重复历程并进行测试。

## 检查消息是否发送成功 {#checking-that-messages-are-sent-successfully}

如果人员在历程中以正确的方式流动，但没有收到他们应该收到的消息，您可以检查：

* [!DNL Journey Optimizer]已正确考虑发送邮件的请求。 商业用户可以访问应发送的消息，并检查最新执行的时间是否与历程的执行时间对应。 他们还可以检查收到的最新API调用/事件。
* [!DNL Journey Optimizer]已成功发送消息。 检查历程报告以确保没有错误。

对于通过自定义操作发送的消息，在历程测试中可以检查的唯一一点就是自定义操作系统的调用是否会导致错误。 如果与自定义操作关联的对外部系统的调用不会导致错误，但也不会导致消息发送，则应对外部系统进行一些调查。
