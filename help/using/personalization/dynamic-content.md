---
solution: Journey Optimizer
product: journey optimizer
title: 创建动态内容
description: 瞭解如何將動態新增至訊息。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 運算式，編輯器，動態，內容
exl-id: 639ad7df-0d0f-4c9b-95d1-f3101267aae2
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 9%

---

# 创建动态内容 {#dynamic-content}

Adobe Journey Optimizer可讓您善用程式庫中建立的條件式規則，將動態內容新增至訊息。

動態內容可建立至任何欄位，您可在其中使用運算式編輯器新增個人化。 這包括主旨列、連結、推播通知內容或文字型別優惠方案的表示方式。 [進一步瞭解個人化內容](personalization-contexts.md)

此外，您可以在電子郵件設計工具中使用條件式規則，以建立內容元件的多個變體。

## 將動態內容新增至運算式 {#perso-expressions}

在運算式中新增動態內容的步驟如下：

1. 導覽至您要新增動態內容的欄位，然後開啟運算式編輯器。

1. 選取 **[!UICONTROL 條件]** 功能表，以顯示可用的條件規則清單。 按一下規則旁的+按鈕，將其新增至目前的運算式。

   您也可以選取「 」，建立新規則 **[!UICONTROL 新建]**. [瞭解如何建立條件](create-conditions.md)

   ![](assets/conditions-expression.png)

1. 新增至 `{%if}` 和 `{%/if}` 標籤您要在符合條件規則時顯示的內容。 您可以視需要新增任意數量的規則，以建立運算式的多個變體。

   在以下範例中，根據收件者的偏好語言，已為SMS內容建立兩個變體。

   ![](assets/conditions-language-sample.png)

1. 內容準備就緒後，您就可以使用 **[!UICONTROL 模擬內容]** 按鈕。 [瞭解如何測試和預覽訊息](../email/preview.md)

   ![](assets/conditions-preview.png)

## 將動態內容新增至電子郵件 {#emails}

>[!CONTEXTUALHELP]
>id="ac_conditional_content"
>title="条件内容"
>abstract="使用条件规则创建内容组件的多个变体。如果在发送消息时不满足任何条件，则将显示默认变体中的内容。"

>[!CONTEXTUALHELP]
>id="ac_conditional_content_select"
>title="条件内容"
>abstract="使用保存在库中的条件规则或创建新规则。"

在電子郵件設計工具中建立內容元件變體的步驟如下：

1. 在電子郵件設計工具中，選取內容元件，然後按一下 **[!UICONTROL 啟用條件式內容]**.

   ![](assets/conditions-enable-conditional.png)

1. 此 **[!UICONTROL 條件式內容]** 窗格會顯示在左側。 在此窗格中，您可以使用條件來建立所選內容元件的多個變體。

   選取以下專案來設定您的第一個變體： **[!UICONTROL 套用條件]** 按鈕。

   ![](assets/conditions-apply.png)

1. 條件程式庫隨即顯示。 選取要與變體關聯的條件規則，然後按一下 **[!UICONTROL 選取]**. 在此範例中，我們想要根據收件者偏好的語言調整元件文字。

   ![](assets/conditions-select.png)

   您也可以按一下「 」，建立新規則 **[!UICONTROL 新建]**. [瞭解如何建立條件](create-conditions.md)

1. 條件式規則與變體相關聯。 為了提高可讀性，建議您按一下橢圓選單來重新命名變體。

   現在設定在傳送訊息時如果符合規則應如何顯示元件。 在此範例中，如果法文是收件者的慣用語言，我們想以法文顯示文字。

   ![](assets/conditions-design.png)

1. 視需要為內容元件新增任意數量的變體。 您可以隨時在不同的變體之間切換，以檢查內容元件如何根據條件規則顯示。

   >[!NOTE]
   >如果在傳送訊息時不符合變體中所定義的任何規則，則內容元件將顯示中定義的內容。 **[!UICONTROL 預設變體]**.
   >
   >條件式內容將會依照變體顯示的順序，根據關聯的規則進行評估。 如果未符合其他條件，則一律會顯示預設變體。
