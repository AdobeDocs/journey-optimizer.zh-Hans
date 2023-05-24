---
solution: Journey Optimizer
product: journey optimizer
title: 历程入门
description: 历程入门
feature: Journeys
role: User
level: Beginner
keywords: 歷程，探索，開始
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 28%

---


# 历程入门{#jo-general-principle}

使用 [!DNL Journey Optimizer] 使用儲存在事件或資料來源中的情境資料，建立即時協調使用案例。

设计由以下功能提供支持的分步式高级方案：

* 实时发送由事件接收触发的&#x200B;**单一投放** ，或使用 Adobe Experience Platform 区段&#x200B;**批量**&#x200B;发送。

* 利用来自事件的&#x200B;**上下文数据**、来自 Adobe Experience Platform 的信息或来自第三方 API 服务的数据。

* 使用 **內建動作** 傳送設計的訊息： [!DNL Journey Optimizer] 或建立 **自訂動作** 如果您使用協力廠商系統來傳送訊息。

* 使用&#x200B;**历程设计器**，构建分步式用例：轻松地拖放进入事件或读取区段活动、添加条件和发送个性化消息。


>[!NOTE]
>
>中會詳細說明歷程護欄和限制 [此頁面](../start/guardrails.md)

## 建立歷程的步驟{#steps-journey}

使用Adobe Journey Optimizer從單一畫布設計和編排個人化歷程。 建立歷程的主要步驟如下：

![](assets/journey-creation-process.png)

Adobe Journey Optimizer包含全通路協調畫布，可讓行銷人員協調行銷外聯活動與一對一客戶參與。 使用者介面可讓您輕鬆將活動從浮動視窗拖放至畫布中，以建立您的歷程。

![](assets/interface-journeys.png)

瞭解如何開始並建立您的第一個歷程 [此頁面](journey-gs.md).

全通路歷程設計工具可協助您使用直覺式的拖放介面，透過目標受眾、根據即時客戶或業務互動的更新以及全通路訊息來建立多步驟歷程。

![](assets/journey38.png)

詳細內容： [本節](using-the-journey-designer.md).

身為資料工程師，設定歷程（包括資料來源、事件和動作）的步驟已詳載於 [本節](../configuration/about-data-sources-events-actions.md).


## 用例{#uc-journey}

瞭解如何在以下端對端使用案例中建立歷程。

商业用例:

* [发送多渠道消息](journeys-uc.md)
* [使用 Campaign v7/v8 发送消息](ajo-ac.md)
* [向订阅者发送消息](message-to-subscribers-uc.md)

技术用例:

* [使用自定义操作动态传递集合](collections.md)
* [增加投放数量](ramp-up-deliveries-uc.md)
* [使用外部数据源和自定义操作限制吞吐量](limit-throughput.md)

## 历程版本{#journey-versions}

在歷程清單中，所有歷程版本都會以版本號碼顯示。 请参阅[此页](../building-journeys/using-the-journey-designer.md)。

當您搜尋歷程時，最新版本會在應用程式首次開啟時出現在清單頂端。 然後，您可以定義所需的排序，應用程式會將其保留為使用者偏好設定。 歷程的版本也會顯示在歷程版本介面的頂端、畫布上方。

![](assets/journeyversions1.png)

>[!NOTE]
>
>通常，同一历程中无法同时存在多个用户档案。如果启用了重新进入，则用户档案可以重新进入历程，但只有在完全退出该历程的上一个实例后才能重新进入历程。[了解详情](end-journey.md)。

如果您需要修改為即時歷程，請建立歷程的新版本。

1. 開啟最新版本的即時歷程，按一下 **[!UICONTROL 建立新版本]** 並確認。

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >您只能從歷程的最新版本建立新版本。

1. 進行修改，按一下 **[!UICONTROL 發佈]** 並確認。

   ![](assets/journeyversions3.png)

從發佈歷程的那一刻起，個人將開始進入歷程的最新版本。 已進入先前版本的人會保留在裡面，直到完成歷程為止。 如果他們稍後重新進入相同的歷程，將進入最新版本。

歷程版本可個別停止。 所有版本的歷程都有相同的名稱。

當您發佈新版本的歷程時，先前版本會自動結束並切換到 **已關閉** 狀態。 無法進入歷程。 即使您停止最新版本，先前版本仍會保持關閉。
