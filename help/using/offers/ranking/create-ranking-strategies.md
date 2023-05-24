---
product: experience platform
solution: Experience Platform
title: 创建 AI 模型
description: 瞭解如何建立AI模型來對優惠進行排名
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 6%

---

# 创建 AI 模型 {#ai-rankings}

[!DNL Journey Optimizer] 可讓您建立 **AI模型** 以根據您的業務目標來排名優惠方案。

>[!CAUTION]
>
>若要建立、編輯或刪除AI模型，您必須擁有 **管理排名策略** 許可權。 [了解详情](../../administration/high-low-permissions.md#manage-ranking-strategies)

## 创建 AI 模型 {#create-ranking-strategy}

若要建立AI模型，請遵循下列步驟：

1. 建立將收集轉換事件的資料集。 [了解如何操作](../data-collection/create-dataset.md)

1. 在 **[!UICONTROL 元件]** 功能表，存取 **[!UICONTROL 排名]** 索引標籤，然後選取 **[!UICONTROL AI模型]**.

   ![](../assets/ai-ranking-list.png)

   列出目前為止建立的所有AI模型。

1. 按一下 **[!UICONTROL 建立AI模型]** 按鈕。

1. 指定AI模型的唯一名稱和說明，然後選取您要建立的AI模型型別：

   * **[!UICONTROL 自動最佳化]** 會根據過去的優惠方案效能來最佳化優惠方案。 [了解详情](auto-optimization-model.md)
   * **[!UICONTROL 個人化]** 根據區段和優惠方案效能最佳化並個人化優惠方案。 [了解详情](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL 最佳化量度]** 區段提供有關AI模型用來計算優惠排名之轉換事件的資訊。
   >
   >[!DNL Journey Optimizer] 根據以下專案排名優惠： **轉換率** （轉換率=轉換事件總數/曝光事件總數）。 轉換率是使用兩種量度型別來計算：
   >* **曝光事件** （已顯示的優惠方案）
   >* **轉換事件** （可透過電子郵件或網頁點按的選件）。

   >
   >系統會使用提供的Web SDK或Mobile SDK自動擷取這些事件。 進一步瞭解，請參閱 [Adobe Experience Platform Web SDK總覽](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=en).

1. 選取轉換和曝光事件收集所在的資料集。 瞭解如何在中建立這類資料集 [本節](../data-collection/create-dataset.md). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >只有從關聯的結構描述建立的資料集 **[!UICONTROL 體驗事件 — 主張互動]** 欄位群組（先前稱為mixin）會顯示在下拉式清單中。

1. 如果您要建立 **[!UICONTROL 個人化]** AI模型，選取要用來訓練AI模型的區段。

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >您最多可以選取5個區段。

1. 儲存並啟動AI模型。

   ![](../assets/ai-ranking-save-activate.png)

<!--At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.-->

現在，每次顯示和/或按一下優惠方案時，您都希望對應的事件能由 **[!UICONTROL 體驗事件 — 主張互動]** 使用下列專案的欄位群組： [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} 或Mobile SDK。

若要能夠在事件型別（顯示的優惠方案或按一下優惠方案）中傳送，您必須為傳送至Adobe Experience Platform的體驗事件中的每個事件型別設定正確的值。 [了解如何操作](../data-collection/schema-requirement.md)