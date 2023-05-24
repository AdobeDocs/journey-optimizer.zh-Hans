---
solution: Journey Optimizer
product: journey optimizer
title: 使用组合画布
description: 瞭解如何使用構成畫布
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 3eb9466e-9d88-4470-a22f-5e24a29923ae
badge: label="Beta" type="Informative"
source-git-commit: 66cf0332c62a9c3b034398c3a6046cbcec622d40
workflow-type: tm+mt
source-wordcount: '1353'
ht-degree: 28%

---

# 使用组合画布 {#composition-canvas}

>[!BEGINSHADEBOX]

本文档包括以下内容：

* [受众组合入门](get-started-audience-orchestration.md)
* [创建您的第一个组合工作流程](create-compositions.md)
* **[使用组合画布](composition-canvas.md)**
* [访问和管理受众](access-audiences.md)

>[!ENDSHADEBOX]

對象構成提供視覺畫布，可讓您建立對象並使用各種活動（分割、擴充等）。

在畫布中組成對象的步驟如下：

1. [定義您的開始對象](#starting-audience)
1. [新增一或多個活動](#action-activities)
1. [將結果儲存至新受眾](#save)

## 選取起始對象 {#starting-audience}

建立構成的第一步是選取一或多個現有對象作為構成的基礎。

1. 選取 **[!UICONTROL 對象]** 活動接著會提供活動的標籤。

1. 選擇要鎖定的對象：

   * 按一下 **[!UICONTROL 新增對象]** 按鈕以選取一或多個現有對象，
   * 按一下 **[!UICONTROL 建置規則]** 按鈕來建立新的區段定義，使用 [細分服務](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

   ![](assets/audiences-choose-audience.png)

1. 如果選取多個對象，請指定這些對象的設定檔合併方式：

* **[!UICONTROL 聯集]**：包含所選對象的所有設定檔，
* **[!UICONTROL 交集]**：包含所有選定對象通用的設定檔，
* **[!UICONTROL 排除重疊]**：僅包含屬於其中一個對象的設定檔。 屬於多個對象的設定檔將不會包括在內。

在此範例中，我們要鎖定屬於金級和銀級受眾的所有設定檔。

![](assets/audiences-starting-audience.png)

選取對象後，活動的底部會顯示預估的個人檔案數。

## 新增活動 {#action-activities}

在選取起始對象後新增活動，以精簡您的選取範圍。

若要這麼做，請按一下構成路徑上的+按鈕，然後選取所需活動。 右側窗格隨即開啟，可讓您設定新新增的活動。

![](assets/audiences-select-activity.png)

可用的活動包括：

* [對象](#audience)：包含屬於一個或多個現有受眾的其他設定檔，
* [排除](#exclude)：排除屬於現有對象的設定檔，或根據特定屬性排除設定檔，
* [擴充](#enrich)：使用來自Adobe Experience Platform資料集的其他屬性來豐富您的受眾，
* [排名](#rank)：根據特定屬性排名設定檔，指定要保留的設定檔數目，並將其納入您的構成中，
* [Split](#split)：根據隨機百分比或屬性，將構成分割為多個路徑。

您可以新增儘可能多的 **[!UICONTROL 對象]** 和 **[!UICONTROL 排除]** 構成中視需要呈現的活動。 不過，之後無法新增其他活動 **[!UICONTROL 排名]** 和 **[!UICONTROL Split]** 活動。

您可以隨時按一下右窗格中的刪除按鈕，從畫布中移除活動。  如果您要刪除的活動是構成中其他活動的父項，則會顯示一則訊息，讓您指定是隻刪除所選活動，還是刪除其所有子項活動。

### 受众活动 {#audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="受众活动"
>abstract="“受众活动”让您可以在组合中包括属于现有受众的配置文件。"

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="合并类型"
>abstract="指定应如何合并所选受众的配置文件。"

此 **[!UICONTROL 對象]** 活動可讓您在構成中包含屬於現有對象的其他設定檔。

此活動的設定與開頭相同 [對象活動](#starting-audience).

### 排除活动 {#exclude}

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="排除类型"
>abstract="使用“排除受众类型”排除属于现有受众的配置文件。“使用属性类型排除”让您可以根据特定属性来排除配置文件。"

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="排除活动"
>abstract="“排除活动”让您可以通过选择现有受众或使用规则，从组合中排除配置文件。"

此 **[!UICONTROL 排除]** 活動可讓您從構成中排除設定檔。 提供兩種排除型別：

* **[!UICONTROL 排除對象]**：排除屬於現有對象的設定檔。

   按一下 **[!UICONTROL 新增對象]** 按鈕，然後選取要排除的對象。

   ![](assets/audiences-exclude-audience.png)

* **[!UICONTROL 使用屬性排除]**：根據特定屬性排除設定檔。

   選取要查詢的屬性，然後指定要排除的值。 在此範例中，我們將從住址位於日本的構成設定檔中排除。

   ![](assets/audiences-exclude-attribute.png)

### 擴充 {#enrich}

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich"
>title="扩充活动"
>abstract="使用“扩充活动”排除属于现有受众的配置文件。“使用属性类型”排除让您可以根据特定属性来排除配置文件。"

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_dataset"
>title="扩充数据集"
>abstract="选择包含要与受众关联的数据的扩充数据集。"

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_criteria"
>title="扩充标准"
>abstract="选择要用作源数据集（即受众）与扩充数据集之间的合并关键项的字段。"

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_attributes"
>title="扩充属性"
>abstract="从扩充数据集中选择一个或多个属性以关联到受众。组合在发布之后，这些属性就会与受众相关联，并且可以在营销活动中用来提供个性化的投放。"

此 **[!UICONTROL 擴充]** 活動可讓您利用來自Adobe Experience Platform資料集的其他屬性來豐富受眾。 例如，您可以新增與所購買產品相關的資訊，例如其名稱、價格或製造商ID，並運用這些資訊來個人化傳送給對象的傳送。

>[!IMPORTANT]
>
>目前，資料集上的標籤（在資料集層級或欄位層級）不會傳播至新建立的對象。 這可能會影響所產生對象的存取控制及/或資料控管。 因此，在構成對象時，請僅使用測試資料。

若要設定活動，請遵循下列步驟：

1. 選取 **[!UICONTROL 擴充資料集]** 包含您要與對象建立關聯的資料。

1. 在 **[!UICONTROL 擴充條件]** 區段，選取在來源資料集（即對象）與擴充資料集之間當作調解金鑰使用的欄位。 在此範例中，我們使用購買產品的ID作為調解金鑰。

1. 按一下 **[!UICONTROL 新增屬性]** 按鈕後，從擴充資料集中選取一或多個屬性，以關聯至對象。

   ![](assets/audiences-enrich-activity.png)

組合發佈後，選取的屬性就會與對象建立關聯，並可在行銷活動中運用以個人化傳送。

### 排名活动 {#rank}

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="排名活动"
>abstract="“排名活动”允许您根据特定属性对配置文件进行排名并将它们包含在组合中。例如，包含忠诚度积分最高的 50 个配置文件。"

>[!CONTEXTUALHELP]
>id="ajo_ao_rank_profilelimit_text"
>title="添加配置文件限制"
>abstract="打开此选项以指定要包含在组合中的配置文件最大数量。"

此 **[!UICONTROL 排名]** 活動可讓您根據特定屬性來排名設定檔，並將其納入您的構成中。 例如，您可以包含忠誠度點數最高的50個設定檔。

1. 選取您要查閱的屬性，並指定排名順序（遞增或遞減）。

   >[!NOTE]
   >
   >您可以選取具有以下資料型別的屬性：整數、數字、短整數 <!--(other?)-->

1. 切換 **[!UICONTROL 新增設定檔限制]** 選項開啟，並指定要包含在構成中的設定檔數目上限。

   ![](assets/audiences-rank.png)

### 拆分活动 {#split}

<!-- [!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Control Group"
>abstract="Use control groups to isolate a portion of the profiles. This allows you to measure the impact of a marketing activity and make a comparison with the behavior of the rest of the population."-->

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="拆分活动"
>abstract="“拆分活动”让您可以将组合拆分成多个路径。在发布组合时，一个受众将在 Adobe Experience Platform 针对每个路径进行保存。"

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="拆分类型"
>abstract="使用“百分比拆分类型”可将配置文件随机拆分到多个路径中。“属性拆分类型”让您可以根据特定属性来拆分配置文件。"

>[!CONTEXTUALHELP]
>id="ajo_ao_split_otherprofiles_text"
>title="其他配置文件"
>abstract="打开此选项可以创建一个附加路径，其中包含与其他路径中指定的任意条件都不匹配的剩余配置文件。"

此 **[!UICONTROL Split]** 活動可讓您將撰寫分割為多個路徑。

此操作會自動新增 **[!UICONTROL 儲存]** 活動。 在发布组合时，一个受众将在 Adobe Experience Platform 针对每个路径进行保存。

有兩種分割作業可供使用：

* **[!UICONTROL 百分比分割]**：將設定檔隨機分割成兩個或多個路徑。 例如，您可以將設定檔分割為2個各自為50%的相異路徑。 <!--and add an additional path for control group.-->

   ![](assets/audiences-split-percentage.png)

* **[!UICONTROL 屬性分割]**：根據特定屬性分割設定檔。 在此範例中，我們根據它們的空間型別偏好來分割輪廓。

   ![](assets/audiences-split.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL 其他設定檔]** 選項可讓您使用不符合其他路徑中指定的任何條件的剩餘設定檔來建立其他路徑。

## 儲存您的對象 {#save}

設定將儲存至Adobe Experience Platform中的結果對象。

若要這麼做，請選取 **[!UICONTROL 儲存對象]** 每個路徑末尾的活動，然後指定要建立的新對象名稱。

![](assets/audiences-publish.png)

一旦您的構成準備就緒，您就可以發佈它。 [瞭解如何建立組合](create-compositions.md)
