---
title: 创建 Web 体验
description: 瞭解如何在Journey Optimizer中編寫網頁及編輯其內容
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 20%

---

# 创建 Web 体验 {#create-web}

[!DNL Journey Optimizer] 可讓您透過傳入的網頁行銷活動，個人化您提供給客戶的網頁體驗。

>[!CAUTION]
>
>这当前位于 [!DNL Journey Optimizer] 中，您只能使用&#x200B;**营销活动**&#x200B;创建 Web 体验。

[透過此影片瞭解如何建立網路行銷活動](#video)

## 创建 Web 营销活动 {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="定义 Web 表面"
>abstract="Web 表面可以匹配单个页面 URL 或多个页面，这让您可以在一个或多个网页上传递内容修改。"

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="构建页面匹配规则"
>abstract="一条页面匹配规则即可针对多个匹配同一规则的 URL - 例如，如果要将更改应用于跨越整个网站的主图横幅或添加在网站的所有产品页面上显示的置顶图像。"

若要透過行銷活動開始建立您的Web體驗，請遵循下列步驟。

>[!NOTE]
>
>如果您是首次创建 Web 体验，请确保遵循[此部分](web-prerequisites.md)中叙述的先决条件。

1. 创建营销活动. [了解详情](../campaigns/create-campaign.md)

1. 選取 **[!UICONTROL Web]** 動作。

1. 定义 Web 表面.

   >[!NOTE]
   >
   >Web介面是由要傳送內容的URL所識別的Web屬性。 它可以比對單一頁面URL或多個頁面，讓您在一或多個網頁之間傳送修改。

   您可以輸入 **[!UICONTROL 頁面URL]** 如果您只想將變更套用至單一頁面。

   ![](assets/web-campaign-surface.png)

1. 或者，您也可以建置 **[!UICONTROL 頁面比對規則]** 將多個符合相同規則的URL設為目標 — 例如，如果您想要將變更套用至整個網站的主圖橫幅，或新增顯示在網站所有產品頁面上的上層影像。

   若要這麼做，請選取 **[!UICONTROL 頁面比對規則]** 並按一下 **[!UICONTROL 建立規則]**.

   ![](assets/web-campaign-matching-rule.png)

1. 為以下專案定義條件： **[!UICONTROL 網域]** 和 **[!UICONTROL 頁面]** 欄位。

   例如，如果您想要編輯顯示在Luma網站所有女性產品頁面上的元素，請選取「 」 **[!UICONTROL 網域]** > **[!UICONTROL 開頭為]** > `luma` 和 **[!UICONTROL 頁面]** > **[!UICONTROL 包含]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. 保存更改。此規則會顯示在 **[!UICONTROL 建立行銷活動]** 畫面。

   ![](assets/web-pages-matching-rule-example.png)

1. 定義網頁表面後，選取 **[!UICONTROL 建立]**.

1. 完成步驟以建立網站行銷活動，例如行銷活動屬性、 [對象](../segment/about-segments.md)、和 [排程](../campaigns/create-campaign.md#schedule).

   ![](assets/web-campaign-steps.png)

有關如何設定行銷活動的詳細資訊，請參閱 [此頁面](../campaigns/get-started-with-campaigns.md).

## 啟動網站行銷活動 {#activate-web-campaign}

定義您的 [網站行銷活動設定](#configure-web-campaign) 而且您已視需要使用 [網頁設計工具](author-web.md)，即可檢閱及啟用您的網站行銷活動。 請遵循下列步驟。

>[!NOTE]
>
>您也可以在啟用網站行銷活動內容之前先預覽該內容。 [了解详情](author-web.md#test-web-campaign)

1. 從您的網路行銷活動中，選取 **[!UICONTROL 檢閱以啟動]**.

1. 視需要檢查並編輯內容、屬性、表面、對象和排程。

1. 選取 **[!UICONTROL 啟動]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >在您按一下 **[!UICONTROL 啟動]**，網站行銷活動變更最多可能需要15分鐘才能即時上線。

您的網路行銷活動會取得 **[!UICONTROL 即時]** 狀態，且現在對選取的對象可見。 行銷活動的每位收件者都能使用，檢視您新增至網站的修改 [!DNL Journey Optimizer] 網頁設計工具。

>[!NOTE]
>
>如果您為網頁行銷活動定義了排程，則它會 **[!UICONTROL 已排程]** 狀態直到達到開始日期和時間。
>
>如果您啟用的網路行銷活動會影響與另一個已上線的行銷活動相同的頁面，則所有變更將會套用至您的網頁。

進一步瞭解如何在中啟用行銷活動 [本節](../campaigns/review-activate-campaign.md).

## 停止網站行銷活動 {#stop-web-campaign}

當網站行銷活動上線時，您可以停止它以防止您的對象看到您的修改。 請遵循下列步驟。

1. 從清單中選取即時行銷活動。

1. 從頂端選單中選取 **[!UICONTROL 停止行銷活動]**.

   ![](assets/web-campaign-stop.png)

1. 您所定義的對象將無法再看見您新增的修改。

>[!NOTE]
>
>網站行銷活動停止後，您就無法再編輯或啟動它。 您只能複製並啟動複製的促銷活動。

## 操作方法视频{#video}

以下影片說明如何建立網站行銷活動、設定其屬性、檢閱並發佈。

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)