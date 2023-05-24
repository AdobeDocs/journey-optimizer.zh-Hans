---
product: experience platform
solution: Experience Platform
title: 创建数据集以收集事件
description: 瞭解如何建立資料集以收集事件
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 10%

---

# 创建数据集以收集事件 {#create-dataset}

若要收集體驗事件，您首先需要建立將傳送這些事件的資料集。

首先，請建立要在資料集中使用的結構描述：

1. 從 **[!UICONTROL 資料管理]** 功能表，選取 **[!UICONTROL 結構描述]** 並前往 **[!UICONTROL 瀏覽]** 標籤。

1. 按一下 **[!UICONTROL 建立結構描述]** 並選擇 **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >瞭解更多關於XDM結構描述和欄位群組 [XDM系統概觀檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=en){target="_blank"}.

1. 從 **[!UICONTROL 欄位群組]** 部分，選取 **[!UICONTROL 新增]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. 在 **[!UICONTROL 搜尋]** 欄位，輸入「主張互動」。

1. 選取 **[!UICONTROL 體驗事件 — 主張互動]** 欄位群組並按一下 **[!UICONTROL 新增欄位群組]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >資料集中使用的結構描述必須具備 **[!UICONTROL 體驗事件 — 主張互動]** 與其相關聯的欄位群組。 否則，您將無法將其用於排名策略。

1. 輸入名稱並儲存結構。

>[!NOTE]
>
>進一步瞭解在中建立結構描述 [結構描述組合基本概念](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target="_blank"}.

您現在已準備好使用此結構描述建立資料集。 为此，请执行以下步骤：

1. 從 **[!UICONTROL 資料管理]** 功能表，選取 **[!UICONTROL 資料集]** 並前往 **[!UICONTROL 瀏覽]** 標籤。

1. 按一下 **[!UICONTROL 建立資料集]** 並選取 **[!UICONTROL 從結構描述建立資料集]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. 從清單中選取您剛建立的結構描述，然後按一下 **[!UICONTROL 下一個]**.

1. 為中的資料集提供唯一名稱 **[!UICONTROL 名稱]** 欄位並按一下 **[!UICONTROL 完成]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>現在可以選取此資料集，以便在下列情況下收集事件資料 [建立排名策略](#create-ranking-strategy).
