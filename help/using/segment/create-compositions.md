---
solution: Journey Optimizer
product: journey optimizer
title: 创建您的第一个组合工作流程
description: 瞭解如何建立構成工作流程，以組合和排列現有對象。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
badge: label="Beta" type="Informative"
source-git-commit: 818c3ff2d159ec3a668c55224996b4736f950e5d
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 14%

---

# 创建您的第一个组合工作流程 {#create-compositions}

>[!BEGINSHADEBOX]

本文档包括以下内容：

* [受众组合入门](get-started-audience-orchestration.md)
* **[创建您的第一个组合工作流程](create-compositions.md)**
* [使用组合画布](composition-canvas.md)
* [访问和管理受众](access-audiences.md)

>[!ENDSHADEBOX]

## 建立構成工作流程 {#create}

若要建立構成工作流程，請遵循下列步驟：

1. 存取 **[!UICONTROL 區段]** 功能表並選取 **[!UICONTROL 建立對象]**.

1. 選取 **[!UICONTROL 組成對象]**.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL 建置規則]** 建立方法可讓您使用建立新的區段定義。 [細分服務](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

1. 構成畫布會顯示兩個預設活動：

   * **[!UICONTROL 對象]**：構成起點。 此活動可讓您選取一或多個對象作為工作流程的基礎。

   * **[!UICONTROL 儲存]**：構成的最後一步。 此活動可讓您將工作流程的結果儲存至新受眾。
   如需如何在構成工作流程畫布中設定活動的詳細資訊，請參閱 [使用構成畫布](composition-canvas.md).

1. 開啟構成屬性以指定標題和說明。

   如果屬性中未定義標題，構成標籤會設為「構成」，接著是建立日期和時間。

   ![](assets/audiences-properties.png)

1. 視需要在「 」之間新增任意數量的活動，以設定您的構成 **[!UICONTROL 對象]** 和 **[!UICONTROL 儲存]** 活動。 [瞭解如何使用構成畫布](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. 在構成準備就緒後，按一下 **[!UICONTROL 發佈]** 按鈕來發佈構成並將產生的對象儲存到Adobe Experience Platform中。

   >[!IMPORTANT]
   >
   >您可以在指定的沙箱中發佈最多75個組合。 如果您已達到此臨界值，則需要刪除構成以釋放空間並發佈新構成。

   如果在發佈期間發生任何錯誤，將顯示警報，其中包含如何解決問題的資訊。

   ![](assets/audiences-alerts.png)

1. 組合已發佈。 產生的對象會儲存至Adobe Experience Platform，並準備好在Journey Optimizer行銷活動中鎖定目標。 [了解如何使用营销活动](../campaigns/get-started-with-campaigns.md)

## 存取組合 {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="发布受众"
>abstract="发布您的组合以将生成的受众保存到 Adobe Experience Platform 中。"

所有已建立的構成都可從以下網址存取： **[!UICONTROL 組合]** 標籤。 它們可以有多個狀態：

* **[!UICONTROL 草稿]**：構成正在進行中，尚未發佈。
* **[!UICONTROL 已發佈]**：構成已發佈，產生的對象已儲存並可供使用。
* **[!UICONTROL 已封存]**：構成已封存。

![](assets/audiences-compositions.png)

>[!NOTE]
>
>您可以使用清單中的省略符號按鈕，隨時複製或刪除現有構成。
