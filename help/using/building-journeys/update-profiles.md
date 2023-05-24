---
solution: Journey Optimizer
product: journey optimizer
title: 更新設定檔
description: 瞭解如何在歷程中使用更新設定檔活動
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 設定檔，更新，歷程，活動
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 9%

---

# 更新設定檔 {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="更新配置文件活动"
>abstract="更新配置文件操作活动让您可以使用来自事件、数据源的信息或使用特定值，更新现有 Adobe Experience Platform 配置文件。"

使用 **[!UICONTROL 更新設定檔]** 動作活動，使用來自事件、資料來源的資訊或使用特定值更新現有的Adobe Experience Platform設定檔。

## Recommendations

* 此 **更新設定檔** 動作只能用於以具有名稱空間的事件開始的歷程。
* 該動作只會更新現有欄位，不會建立新的設定檔欄位。
* 您無法使用 **更新設定檔** 產生體驗事件的動作，例如購買。
* 就像任何其他動作一樣，您可以定義發生錯誤或逾時時的替代路徑，而且您無法同時放置兩個動作。
* 傳送至Adobe Experience Platform的更新要求即時/在一秒內。 這通常需要幾秒鐘的時間，但有時更長，無法保證。 因此，舉例來說，如果動作使用「欄位1」，而此欄位是由 **更新設定檔** 放在之前的動作，您不應該預期動作中會更新「欄位1」。
* 此 **更新設定檔** 活動不支援定義為列舉的XDM欄位。

## 使用設定檔更新

1. 從事件開始設計您的歷程。 请参阅此[部分](../building-journeys/journey.md)。

1. 在 **動作** 區段，拖放 **更新設定檔** 活動放入畫布。

   ![](assets/profileupdate0.png)

1. 從清單中選取結構描述。

1. 按一下 **欄位** 以選取您要更新的欄位。 只能選取一個欄位。

   ![](assets/profileupdate2.png)

1. 從清單中選取資料集。

   >[!NOTE]
   >
   >此 **更新設定檔** 動作會即時更新設定檔資料，但不會更新資料集。 需要選取資料集，因為設定檔是和資料集相關的記錄。

1. 按一下 **值** 欄位以定義您要使用的值：

   * 使用簡單運算式編輯器，您可以從資料來源或傳入事件中選取欄位。

      ![](assets/profileupdate4.png)

   * 如果要定義特定值或利用進階函式，請按一下 **進階模式**.

      ![](assets/profileupdate3.png)

此 **更新設定檔** 現已設定。

![](assets/profileupdate1.png)


## 使用測試模式 {#using-the-test-mode}

在測試模式中，將不會模擬設定檔更新。 更新將在測試設定檔上執行。

只有测试配置文件才能进入处于测试模式的历程。您可以建立新的測試設定檔，或將現有設定檔轉換為測試設定檔。 在Adobe Experience Platform中，您可以透過csv檔案匯入或API呼叫更新設定檔屬性。 更簡單的方法是使用 **更新設定檔** 動作活動，並將測試設定檔布林值欄位從false變更為true。

有關如何將現有設定檔轉換為測試設定檔的詳細資訊，請參閱此 [區段](../segment/creating-test-profiles.md#create-test-profiles-csv).
