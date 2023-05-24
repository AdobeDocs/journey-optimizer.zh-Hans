---
solution: Journey Optimizer
product: journey optimizer
title: 歷程疑難排解
description: 瞭解如何疑難排解歷程中的錯誤
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 疑難排解，疑難排解，歷程，檢查，錯誤
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 74%

---

# 对历程进行故障排除{#troubleshooting}

在本部分中，您将了解如何在测试或发布之前对历程进行故障排除。当历程处于测试模式或历程处于实时状态时，可以执行以下列出的所有检查。建议在测试模式下进行以下所有检查，然后继续发布。请参阅[此页](../building-journeys/testing-the-journey.md)。

## 測試前先檢查錯誤{#checking-for-errors-before-testing}

测试和发布历程之前，请验证所有活动均已正确配置。如果系统仍检测到错误，则无法执行测试或发布。

出现错误时，画布上的活动本身会显示警告符号。将光标放在感叹号上以显示错误消息。如果单击活动，您将看到带警告的错误行。例如，如果必填字段为空，则会显示错误。

![](assets/journey63.png)

例如，在画布中，当两个活动断开连接时，系统将显示一条警告消息。

![](assets/canvas-disconnected.png)

旁邊 **[!UICONTROL 測試]** 切換及 **[!UICONTROL 發佈]** 按鈕時，會顯示警告符號。 此警告标记显示系统检测到的错误，并阻止测试模式激活或历程发布。大多数时间，系统检测到的错误都与活动上可见的错误相关，但有时它们也与其他问题相关。在这种情况下，您可以显示它们，尝试使用错误描述来识别问题。如果您无法识别问题，可以复制详细信息并发送给管理员或支持团队。请注意，阻止测试的错误和阻止发布的错误是相似的。

系统检测到两种问题：错误和警告。错误阻止发布和测试激活。警告指示未阻止测试激活或发布的潜在问题。您将看到问题的描述和 ERR_XXX_XXX 类型的问题日志 ID。这将帮助技术支持人员确定问题。

兩個不同的顏色可以顯示在旁邊的符號上 **[!UICONTROL 測試]** 切換及 **[!UICONTROL 發佈]** 按鈕。 出现错误时，该符号以红色显示。出现警告时，以橙色显示。

![](assets/journey75.png)

历程全局的错误和警告首先在列表中显示。之后，与特定活动相关的错误和警告按活动顺序或在历程中的出现顺序从左到右列出。此 **[!UICONTROL 複製詳細資料]** 按鈕會複製支援團隊可用於疑難排解的歷程相關技術資訊。

当操作或条件中发生错误时，个人历程将停止。唯一能讓它繼續的方法就是勾選方塊 **[!UICONTROL 在逾時或錯誤的情況下新增替代路徑]**. 请参阅[此小节](../building-journeys/using-the-journey-designer.md#paths)。

## 檢查是否已正確傳送事件{#checking-that-events-are-properly-sent}

历程的起点永远是事件。您可以使用 Postman 等工具执行测试。

您可以检查通过这些工具发送的 API 调用是否正确发送。如果返回错误，则表示您的调用有问题。再次检查有效负载、标题（特别是组织 ID）以及目标 URL。您可以询问管理员要点击的正确 URL。

事件不會直接從來源推送到歷程。 事實上，歷程仰賴Adobe Experience Platform的串流獲取API。 因此，若發生事件相關問題，您可以參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"} 適用於串流獲取API的疑難排解。

## 檢查是否有人進入歷程{#checking-if-people-enter-the-journey}

歷程報告會即時測量歷程中的人員入口。

如果您成功发送事件，但未看到有人进入历程，则意味着在事件发送和事件接收之间出现问题。

以下是管理员应检查的一些事项：

* 是否确定期待传入事件的历程处于测试模式或处于实时状态？
* 是否在从有效负载预览复制有效负载之前保存了您的事件？
* 您的事件有效负载是否包含事件 ID？
* 您是否点击了正确的 URL？
* 您是否使用“事件配置”窗格中的有效负载结构预览遵循了流摄取 API 的有效负载结构？请参阅[此页](../event/about-creating.md#preview-the-payload)。
* 您在事件標頭中使用正確的機碼值組嗎？

   ```
   X-gw-ims-org-id - your organization's ID
   Content-type - application/json
   ```

## 檢查人們如何導覽歷程{#checking-how-people-navigate-through-the-journey}

歷程報告會衡量歷程中個人的進度。 很容易识别人员在何处被拦住以及为什么被拦住。

以下是一些要检查的内容：

* 是因为除人员外的情况吗？例如，条件为“性别=男性”，而该人员为女性。如果条件不太复杂，此检查可由商业用户执行。
* 是由于调用数据源时没有响应吗？当历程正在测试时，此信息可在测试模式日志中查看。当历程处于实时状态时，管理员可以测试对数据源的直接调用并检查收到的答案。管理员还可以重复历程并进行测试。

## 檢查訊息是否成功傳送{#checking-that-messages-are-sent-successfully}

如果人员在历程中以正确的方式流动，但没有收到他们应该收到的消息，您可以检查：

* [!DNL Journey Optimizer] 已正確考量傳送訊息的要求。 商業使用者可以存取應傳送的訊息，並檢查最新執行的時間是否與歷程的執行時間對應。 他們也可以檢查收到的最新API呼叫/事件。
* [!DNL Journey Optimizer] 已成功傳送訊息。 檢查歷程報告以確定沒有錯誤。

对于通过自定义操作发送的消息，在历程测试中可以检查的唯一一点就是自定义操作系统的调用是否会导致错误。如果与自定义操作关联的对外部系统的调用不会导致错误，但也不会导致消息发送，则应对外部系统进行一些调查。
