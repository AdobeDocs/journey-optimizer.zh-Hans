---
solution: Journey Optimizer
product: journey optimizer
title: 建立區段
description: 瞭解如何建立區段
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 11%

---

# 构建区段 {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="创建规则"
>abstract="通过构建规则创建方法，您可以使用 Adobe Experience Platform Segmentation Service 创建新的区段定义。"

在此範例中，我們將建立一個區段，以鎖定亞特蘭大、舊金山或西雅圖居住且1980年後出生的所有客戶。 所有這些客戶應在過去7天內開啟Luma應用程式，然後在開啟應用程式後2小時內購買。

➡️ [在本影片中瞭解如何建立區段](#video-segment)

1. 存取 **[!UICONTROL 區段]** 功能表，然後按一下 **[!UICONTROL 建立區段]** 按鈕。

   ![](assets/create-segment.png)

   區段定義畫面可讓您設定定義區段所需的所有欄位。 瞭解如何在中設定區段 [Segment Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target="_blank"}.

   ![](assets/segment-builder.png)

1. 在 **[!UICONTROL 區段屬性]** 窗格中，提供區段的名稱和說明（選擇性）。

   ![](assets/segment-properties.png)

1. 將所需欄位從左窗格拖放至中央工作區，然後視需要加以設定。

   >[!NOTE]
   >
   >請注意，左窗格中可用的欄位會依以下方式而有所不同： **XDM個別設定檔** 和 **XDM ExperienceEvent** 已為貴組織設定結構描述。  進一步瞭解 [Experience Data Model (XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}.

   ![](assets/drag-fields.png)

   在此範例中，我們需要仰賴 **屬性** 和 **事件** 要建立區段的欄位：

   * **屬性**：1980年後出生且生活在亞特蘭大、舊金山或西雅圖的設定檔

      ![](assets/add-attributes.png)

   * **事件**：在過去7天內開啟Luma應用程式，然後在開啟應用程式後2小時內購買的使用者設定檔。

      ![](assets/add-events.png)

1. 當您在工作區中新增及設定新欄位時， **[!UICONTROL 區段屬性]** 窗格會自動更新屬於該區段的預估設定檔資訊。

   ![](assets/segment-estimate.png)

1. 區段準備就緒後，按一下 **[!UICONTROL 儲存]**. 它會顯示在Adobe Experience Platform區段清單中。 請注意，搜尋列可協助您搜尋清單中的特定區段。

該區段現在可用於您的歷程。 有关详细信息，请参阅[此部分](../segment/about-segments.md)。

## 操作方法视频{#video-segment}

瞭解如何建立區段。

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
