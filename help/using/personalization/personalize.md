---
solution: Journey Optimizer
product: journey optimizer
title: 在 Journey Optimizer 中个性化内容
description: 个性化入门。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
keywords: 運算式，編輯器，開始，個人化
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 28%

---

# 个性化入门{#add-personalization}

探索 [!DNL Adobe Journey Optimizer] 個人化功能，可運用您擁有的訊息相關資料和資訊，根據每位特定收件者調整訊息。 可以是他們的名字、興趣、居住地、購買內容等。

➡️ [瞭解如何在這些影片中個人化訊息](#video-perso)
➡️ [探索運用個人化的使用案例](personalization-use-case.md)

## 使用專用語法建置個人化運算式 {#syntax}

[!DNL Journey Optimizer] 使用 **內嵌** 以Handlebars為基礎的簡單個人化語法，可讓您建立包含雙大括弧之內容的運算式 **{{}}**. 您可以在同一内容或字段中添加多个表达式，而不受限制。進一步瞭解 [個人化語法](personalization-syntax.md).

**示例：**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

處理訊息（電子郵件和推播）時，Journey Optimizer會以Experience Platform資料庫中包含的資料取代運算式：  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` 會變成「Hello John Doe」。

## 運用設定檔資料個人化您的訊息 {#data}

个性化基于 Adobe Experience Platform 中定义的 **XDM Individual Profile** 架构管理的用户档案数据。進一步瞭解 [Adobe Experience Platform資料模型(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}.

>[!CAUTION]
>此 **XDM個別設定檔** 結構描述是您唯一可用來個人化內容的結構描述 [!DNL Journey Optimizer].

## 在不同內容中新增個人化 {#contexts}

[!DNL Journey Optimizer] 可讓您以數種不同的方式個人化內容及顯示訊息。 進一步瞭解您可以在中執行個人化的內容 [本節](personalization-contexts.md).

## 使用運算式編輯器 {#editor}

[!DNL Journey Optimizer] 提供運算式編輯器，您可在其中選取、排列、自訂及驗證所有資料，以建立內容的自訂個人化。

有數種工具可協助您建置個人化內容（協助程式函式、預先定義的運算式程式庫、受歡迎的屬性……）

進一步瞭解 [!DNL Journey Optimizer] 中的運算式編輯器 [本節](personalization-build-expressions.md)

## 操作说明视频{#video-perso}

了解如何使用历程中的情境式事件信息来对消息进行个性化。

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

了解如何在消息中添加基于个人资料的个性化设置，以及如何将区段会员资格用作个性化块的先决条件。

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
