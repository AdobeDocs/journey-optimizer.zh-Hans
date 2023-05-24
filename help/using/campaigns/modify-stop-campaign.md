---
solution: Journey Optimizer
product: journey optimizer
title: 修改或停止营销活动
description: 瞭解如何修改、停止或複製Journey Optimizer中的即時行銷活動
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 管理行銷活動、狀態、排程、存取、最佳化工具
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 2%

---

# 管理活动 {#modify-stop-campaign}

行銷活動啟動後，您可以隨時修改或停止它。 這些操作僅適用於具有重複執行的行銷活動。

此外，您可以複製即時行銷活動（執行一次或循環執行）以建立新行銷活動，並封存已完成或停止的行銷活動。

## 访问活动 {#access}

行銷活動可從存取 **[!UICONTROL 行銷活動]** 功能表。

依預設，清單會顯示所有促銷活動包含 **[!UICONTROL 草稿]**， **[!UICONTROL 已排程]**、和 **[!UICONTROL 即時]** 狀態。 若要顯示已停止、已完成和已封存的行銷活動，您必須清除篩選器。

![](assets/create-campaign-list.png)

此外，您可以根據行銷活動型別和頻道，或是在建立行銷活動時指派給行銷活動的標籤來篩選清單。 [瞭解如何將標籤指派至行銷活動](create-campaign.md#create)

## 行銷活動狀態 {#statuses}

行銷活動可以有多個狀態：

* **[!UICONTROL 草稿]**：行銷活動正在編輯中，尚未啟用。
* **[!UICONTROL 啟用]**：正在啟動行銷活動。
* **[!UICONTROL 即時]**：行銷活動已啟用。
* **[!UICONTROL 已排程]**：行銷活動已設定為在特定的開始日期啟動。
* **[!UICONTROL 已停止]**：行銷活動已手動停止。 您無法再啟用或重複使用它。 [瞭解如何停止行銷活動](modify-stop-campaign.md#stop)
* **[!UICONTROL 已完成]**：行銷活動完成。 此狀態會在行銷活動啟動3天後自動指派，如果行銷活動有週期性執行，則會在行銷活動的結束日期指派。
* **[!UICONTROL 已封存]**：行銷活動已封存。 [瞭解如何封存行銷活動](modify-stop-campaign.md#archive)

>[!NOTE]
>
>旁的「開啟草稿版本」圖示 **[!UICONTROL 即時]** 或 **[!UICONTROL 已排程]** status表示已建立新版本的行銷活動，但尚未啟用。 [了解详情](modify-stop-campaign.md#modify)。

## 修改週期性行銷活動 {#modify}

若要修改和建立循環行銷活動的新版本，請遵循下列步驟：

1. 開啟行銷活動，然後按一下 **[!UICONTROL 修改行銷活動]** 按鈕。

1. 會建立新版本的行銷活動。 您可以按一下「 」以檢查即時版本 **[!UICONTROL 開啟即時版本]**.

   ![](assets/create-campaign-draft.png)

   在行銷活動清單中，正在進行草稿版本的已啟動行銷活動會在中顯示特定圖示 **[!UICONTROL 狀態]** 欄。 按一下此圖示以開啟行銷活動的草稿版本。

   ![](assets/create-campaign-edit-list.png)

1. 準備好變更後，您就可以啟動新版本的行銷活動(請參閱 [檢閱及啟用行銷活動](create-campaign.md#review-activate))。

   >[!IMPORTANT]
   >
   >啟用草稿將會取代行銷活動的即時版本。

## 停止週期性行銷活動 {#stop}

若要停止週期性行銷活動，請開啟該行銷活動，然後按一下 **[!UICONTROL 停止行銷活動]** 按鈕。

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>停止行銷活動不會停止進行中的傳送，但會停止排程的傳送，如果傳送已在進行中，則會停止下一次發生。

<!-- inbound campaign (inapp): can stop and resume -->

## 複製行銷活動 {#duplicate}

您可以複製即時行銷活動以建立新行銷活動。 若要這麼做，請開啟行銷活動，然後按一下 **[!UICONTROL 複製]**.

![](assets/create-campaign-duplicate.png)

## 封存行銷活動 {#archive}

隨著時間推移，行銷活動清單不斷成長，最終導致瀏覽已完成和已停止的行銷活動變得更加困難。

為避免此問題，您可以封存您不再需要的已完成和已停止的行銷活動。 若要這麼做，請按一下省略符號按鈕，然後選取 **[!UICONTROL 封存]**.

![](assets/create-campaign-archive.png)

然後可以使用清單中的專用篩選器來擷取已封存的行銷活動。 [瞭解如何存取行銷活動](get-started-with-campaigns.md#access)
