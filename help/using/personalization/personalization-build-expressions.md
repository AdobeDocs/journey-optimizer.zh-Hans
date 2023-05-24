---
solution: Journey Optimizer
product: journey optimizer
title: 关于表达式编辑器
description: 瞭解如何使用運算式編輯器。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 運算式，編輯器，關於，開始
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 93e3ed9e1a9a437353b800aee58952b86eab9370
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 12%

---

# 開始使用運算式編輯器 {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="关于表达式编辑器"
>abstract="表达式编辑器让您可以选择、排列、自定义和验证所有数据，为自己的内容创建定制的个性化。"

運算式編輯器是中個人化的核心 [!DNL Journey Optimizer]. 它可用於您需要定義個人化的每個內容，例如電子郵件、推播和選件。

在運算式編輯器介面中，您將選取、排列、自訂及驗證所有資料，為您的內容建立自訂的個人化。

![](assets/perso_ee1.png)

## 可用的個人化來源 {#sources}

畫面左側會顯示網域選擇器，讓您選取個人化的來源。 可用的來源包括：

* **[!UICONTROL 設定檔屬性]** ：列出中所述與設定檔結構描述相關聯的所有參考 [Adobe Experience Platform資料模型(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}.
* **[!UICONTROL 區段會籍]** ：列出Adobe Experience Platform Segmentation服務中建立的所有區段。 有關區段的詳細資訊 [此處](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target="_blank"}.
* **[!UICONTROL 優惠決定]** ：列出與特定位置相關聯的所有優惠方案。 選取位置，然後將優惠方案插入內容中。 如需有關如何管理優惠方案的完整檔案，請參閱 [本節](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL 內容屬性]** ：當歷程中使用管道動作活動（電子郵件、推播、簡訊）時，可透過此選單使用內容歷程欄位。 有关详细信息，请参阅[此部分](personalization-use-case.md)。
* **[!UICONTROL 輔助函式]** ：列出所有可用於對資料執行操作（例如計算、資料格式或轉換、條件）的協助程式功能，並在個人化內容中操作它們。 有关详细信息，请参阅[此部分](functions/functions.md)。

## 新增個人化屬性 {#add}

按一下+按鈕，將屬性新增至個人化運算式。

「+」圖示旁的省略符號選單可讓您取得每個變數的詳細資訊，並將最常用的屬性新增至我的最愛。 [瞭解如何將屬性新增至我的最愛](personalization-favorites.md)

此外，您可以定義預設後援文字，在字串型別設定檔屬性為空白時顯示。 若要這麼做，請按一下屬性旁的省略符號按鈕，然後選取 **[!UICONTROL 插入後援文字]**. 撰寫設定檔的屬性值空白時預設應顯示的文字，然後按一下 **[!UICONTROL 新增]**.

![](assets/attribute-details.png)

在以下範例中，運算式編輯器可讓您選取今天生日的設定檔，然後插入與今天對應的特定選件來完成自訂。

![](assets/perso_ee2.png)

準備好個人化運算式後，您需要讓運算式編輯器驗證該運算式。 有关详细信息，请参阅[此部分](personalization-validation.md)。
