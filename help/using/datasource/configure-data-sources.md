---
solution: Journey Optimizer
product: journey optimizer
title: 配置数据源
description: 了解如何配置数据源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
keywords: 資料，來源，設定，欄位
exl-id: 9b0dcffb-f543-4066-850c-67ec33f74a31
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 15%

---

# 配置数据源 {#configure-data-source}


>[!NOTE]
>
>数据源配置操作必须始终由&#x200B;**技术用户**&#x200B;执行。

若要設定資料來源，請遵循下列步驟：

1. 在「管理」選單區段中，選取 **[!UICONTROL 設定]**. 在  **[!UICONTROL 資料來源]** 區段，按一下 **[!UICONTROL 管理]**. 将显示数据源列表。有关该界面的更多信息，请参阅[此页面](../start/user-interface.md)。

   ![](assets/journey18.png)

1. 然后，您可以将字段组添加到内置数据源（请参阅[此页面](../datasource/adobe-experience-platform-data-source.md)）或创建新的外部数据源（请参阅[此页面](../datasource/external-data-sources.md)）和关联的字段组（请参阅](../datasource/configure-data-sources.md#define-field-groups)此页面[）。

   ![](assets/journey23.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。

   数据源现已配置完毕，可随时用于您的历程。

## 定義欄位群組 {#define-field-groups}

欄位群組是一組欄位，您可以從資料來源擷取並在歷程中使用。

對於每個資料來源，您可以定義數個欄位群組。

例如，您可以建立包含電話號碼、電子郵件、名字和個人資料地址的欄位群組。 然後，您就可以在歷程中使用此資料來建立條件。 例如，您可以決定只有在客戶已安裝行動應用程式時才會傳送推播通知。 如果它是空的，您可以傳送電子郵件。

即使自動新增預設名稱，我們仍建議您為欄位群組提供名稱。 事實上，欄位群組名稱對中的其他使用者可見 [!DNL Journey Optimizer]. 為欄位群組指定相關名稱是最佳做法。

當歷程中使用資料來源欄位時，系統會擷取為該欄位群組定義的所有欄位。 因此，最佳實務就是僅選取歷程所需的欄位。 這將減少歷程中的請求延遲，從而提高效能。 請注意，您稍後可以輕鬆地在欄位群組中新增更多欄位。

使用欄位群組的歷程次數會顯示在 **[!UICONTROL 使用位置]** 欄位。 您可以按一下 **[!UICONTROL 檢視歷程]** 按鈕以顯示使用此欄位群組的歷程清單。

>[!NOTE]
>
>請注意，如果欄位群組沒有欄位，則運算式編輯器中不會顯示該欄位。

![](assets/journey3bis.png)

## 欄位群組生命週期 {#field-group-lifecycle}

您可以從未用於任何草稿或即時歷程的欄位群組中新增或移除欄位。

您可以新增欄位，但無法從一個或多個草稿或即時歷程中使用的欄位群組中移除欄位。 這可避免中斷歷程。

若要從用於一或多個歷程的欄位群組中刪除欄位，請按照以下步驟操作。 讓我們以名為「欄位群組A」的欄位群組為例。

1. 在欄位群組清單中，將游標放在「欄位群組A」上，然後按一下 **[!UICONTROL 複製]** 圖示加以檢視。 例如，將複製的欄位群組命名為「欄位群組B」。
1. 在「欄位群組B」中，移除您不再想要的欄位。
1. 在「欄位群組A」中，檢查此欄位群組的使用位置。 此資訊會顯示在 **[!UICONTROL 使用位置]** 欄位。
1. 開啟所有使用「欄位群組A」的歷程。
1. 建立每個歷程的新版本。 使用「欄位群組A」編輯所有活動並選取「欄位群組B」。
1. 停止使用「欄位群組A」的舊版歷程。 然後，您應該沒有使用「欄位群組A」的歷程。
1. 移除「欄位群組A」，因為它已不再使用。
