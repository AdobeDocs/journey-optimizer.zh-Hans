---
title: 優惠資料庫使用者介面
description: 深入瞭解優惠資料庫使用者介面
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 722f9c3b-b505-48c0-b126-31a7a841c245
source-git-commit: b5fa17bfc888236994e73474c35b1aaafcda3ebe
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 35%

---

# 優惠資料庫使用者介面 {#user-interface}

此 **[!UICONTROL 決定管理]** 左側邊欄中的區段提供兩個選單，可讓您存取決策管理功能：

使用 **[!UICONTROL 選件]** 管理及傳遞優惠方案的功能表：


![](../assets/offers_menu.png)

* **[!UICONTROL 概觀]**：新至 [!DNL decision management]？ 依照熒幕上的步驟開始設定位置、優惠和集合。 熟悉時 [!DNL decision management]，取得您最近優惠、集合和決定的概觀。 [了解详情](#overview)
* **[!UICONTROL 選件]**：建立並存取您的個人化和遞補優惠。 瞭解如何建立 [優惠方案](../offer-library/creating-personalized-offers.md) 和 [遞補優惠](../offer-library/creating-fallback-offers.md)
* **[!UICONTROL 集合]**：將優惠方案組織成靜態和動態集合。 [了解详情](../offer-library/creating-collections.md)
* **[!UICONTROL 決定]**：建立和管理決定以傳遞您的優惠。 [了解详情](../offer-activities/create-offer-activities.md)
* **[!UICONTROL 批次決策]**：將優惠決定傳送至指定Adobe Experience Platform區段中的所有設定檔。 [了解详情](../batch-delivery.md)
* **[!UICONTROL 模擬]**：模擬會將哪些優惠傳遞至指定位置的測試設定檔，以驗證決策邏輯。 [了解详情](../offer-activities/simulation.md)

使用 **[!UICONTROL 元件]** 建立和管理元件以建立優惠和決定的功能表：

![](../assets/offer_activities.png)

* **[!UICONTROL 版位]**：建立並管理您的優惠將顯示的位置。 [了解详情](../offer-library/creating-placements.md)
* **[!UICONTROL 集合限定詞]**：建立和管理集合限定詞（先前稱為「標籤」）以組織及篩選您的優惠。 [了解详情](../offer-library/creating-tags.md)
* **[!UICONTROL 規則]**：管理提供您優惠的條件。 [了解详情](../offer-library/creating-decision-rules.md)
* **[!UICONTROL 排名]**：建立和管理排名公式，以決定應先針對指定位置顯示哪個優惠。 [了解详情](../ranking/create-ranking-formulas.md)

>[!NOTE]
>
>如果您在存取決策管理或其部分功能時遇到問題，請向管理員使用者確認您已獲得所需許可權。 另請參閱 [授與決策管理的存取權](starting-offer-decisioning.md#granting-acess-to-decision-management).

## 概述 {#overview}

當您初次使用 [!DNL decision management]，則 **[!UICONTROL 概觀]** 索引標籤會引導您完成開始建立第一個優惠決定所需的主要步驟。 依照熒幕上的步驟開始建立版位、優惠和集合。 完成這些第一個步驟後，系統會提示您建立優惠決定。

>[!NOTE]
>
>建立優惠並在決定中使用優惠的主要步驟在中介紹 [本節](../offer-library/key-steps.md).

當您更熟悉 [!DNL decision management] 而且您已建立至少一個優惠決定， **[!UICONTROL 概觀]** 標籤會顯示您最近的優惠、集合和決定。

按一下優惠或決定，直接存取所選專案的詳細資料。

按一下 **[!UICONTROL 檢視全部]** 按鈕來存取優惠方案、集合或決定清單。

![](../assets/overview_view-all.png)

## 搜索和筛选信息 {#search-and-filter-information}

使用&#x200B;**搜索栏**&#x200B;查找特定项目。

单击列表左上角的过滤器图标即可访问&#x200B;**过滤器**。 它们允许您根据不同的条件筛选显示的元素。例如，您可以筛选为电子邮件通信渠道和图像类型内容创建的投放位置。

![](../assets/filters.png)

## 自定义显示的信息 {#customize-displayed-information}

针对决策管理菜单的列表，可以通过列表右上角的配置按钮对其进行个性化设置。

这允许您根据需要选择要显示的信息。

请注意，将为每个用户保存列自定义。

![](../assets/columns.png)

## 信息窗格 {#information-pane}

在不同的列表中，选择一个元素以显示一个信息窗格，该窗格允许您检索信息并对元素执行基本操作。

![](../assets/information-pane.png)

通过优惠和优惠活动列表也可对多个元素执行批量操作。为此，请选择所需的优惠或决策，然后从信息窗格中选择要执行的操作。

請注意，您也可以複製現有優惠或決定，以便使用建立副本 **[!UICONTROL 草稿]** 狀態。 可以在信息窗格或在优惠或决策的详细视图中执行此操作。

## 优惠和决策更改日志 {#changes-logs}

優惠資料庫可讓您以視覺效果呈現對優惠或決定進行的所有變更。 若要這麼做，請按一下清單中優惠或決定的名稱，然後選取 **[!UICONTROL 變更記錄]** 標籤。

此屏幕中显示所有已完成的更改，还显示执行更改的用户姓名。

![](../assets/change-logs.png)
