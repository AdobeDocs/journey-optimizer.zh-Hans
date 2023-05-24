---
solution: Journey Optimizer
product: journey optimizer
title: 設定Journey Optimizer報表以進行實驗
description: 了解如何设置报表数据源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
keywords: 設定，實驗，報告，最佳化工具
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
badge: label="Beta" type="Informative"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 32%

---

# 設定用於實驗的報告 {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="设置报表数据集"
>abstract="报告配置让您可以检索将在营销活动报告的“目标”选项卡中使用的其他指标。该操作必须由技术用户执行。"

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="选择数据集"
>abstract="您只能选择一个事件类型的数据集，该数据集必须至少包含一个支持的字段组：应用程序详细信息、商务详细信息、Web 详细信息。"

>[!BEGINSHADEBOX]

本文档包括以下内容：

* [内容体验入门](get-started-experiment.md)
* [创建内容试验](content-experiment.md)
* [了解统计计算](experiment-calculations.md)
* **[配置实验报表](reporting-configuration.md)**
* [实验报表中的统计计算](experiment-report-calculations.md)

>[!ENDSHADEBOX]

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

報告資料來源設定可讓您擷取將用於以下專案的其他量度： **[!UICONTROL 目標]** 標籤內的任何專案。 [了解详情](content-experiment.md#objectives-global)

>[!NOTE]
>
>報告設定必須由技術使用者執行。 <!--Rights?-->

對於此設定，您需要新增一個或多個資料集，其中包含您要用於報告的其他元素。 若要這麼做，請遵循步驟 [以下](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## 先决条件


您必須先建立該資料集，才能將資料集新增至報表設定。 瞭解如何在 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=zh_Hans#create){target="_blank"}.

* 您只能新增事件型別資料集。

* 這些資料集必須至少包含下列其中一項 [欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh_Hans#field-group){target="_blank"}： **應用程式詳細資料**， **商務詳細資料**， **網頁詳細資訊**.

   >[!NOTE]
   >
   >目前僅支援這些欄位群組。

   例如，如果您想瞭解電子郵件行銷活動對商業資料（如購買或訂單）的影響，則需要使用建立體驗事件資料集 **商務詳細資料** 欄位群組。

   同樣地，如果您想要報告行動互動，則需要建立體驗事件資料集， **應用程式詳細資料** 欄位群組。

   會列出與每個欄位群組對應的量度 [此處](#objective-list).

* 您可以將這些欄位群組新增到一個或多個方案中，這些方案將用於一個或多個資料集。

>[!NOTE]
>
>瞭解更多關於XDM結構描述和欄位群組 [XDM系統概觀檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh_Hans){target="_blank"}.

## 對應至每個欄位群組的目標 {#objective-list}

下表顯示要將哪些量度新增至 **[!UICONTROL 目標]** 標籤中每個欄位群組的行銷活動報告。

| 字段组 | 目标 |
|--- |--- |
| 商務詳細資料 | 總價<br>付款金額<br>（不重複）結帳<br>（不重複）產品清單新增<br>（唯一）產品清單開啟<br>（獨特）產品清單移除<br>（不重複）產品清單檢視<br>（不重複）產品檢視<br>（不重複）購買<br>（不重複）儲存供日後使用<br>產品總價<br>產品數量 |
| 應用程式詳細資料 | （不重複）應用程式啟動次數<br>首次應用程式啟動<br>（不重複）應用程式安裝次數<br>（不重複）應用程式升級 |
| 網頁詳細資訊 | （不重複）頁面檢視 |

## 添加数据集 {#add-datasets}

1. 從 **[!UICONTROL 管理]** 功能表，選取 **[!UICONTROL 設定]**. 在  **[!UICONTROL 報告]** 區段，按一下 **[!UICONTROL 管理]**.

   ![](assets/reporting-config-menu.png)

   此时会显示已添加的数据集列表。

1. 從 **[!UICONTROL 資料集]** 標籤，按一下 **[!UICONTROL 新增資料集]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >如果您選取 **[!UICONTROL 系統資料集]** 索引標籤中，只會顯示由系統建立的資料集。 您将无法添加其他数据集。

1. 從 **[!UICONTROL 資料集]** 下拉式清單，選取您要用於報告的資料集。

   >[!CAUTION]
   >
   >您只能選取事件型別資料集，該資料集必須至少包含一個受支援的 [欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh_Hans#field-group){target="_blank"}： **應用程式詳細資料**， **商務詳細資料**， **網頁詳細資訊**. 如果选择的数据集与这些条件不匹配，您将无法保存所做的更改。

   ![](assets/reporting-config-datasets.png)

   進一步瞭解 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh_Hans){target="_blank"}.

1. 從 **[!UICONTROL 設定檔ID]** 從下拉式清單中，選取用於識別報告中每個設定檔的資料集欄位屬性。

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >只显示可用于报表的 ID。

1. 此 **[!UICONTROL 使用主要ID名稱空間]** 選項預設為啟用。 若已選取 **[!UICONTROL 設定檔ID]** 是 **[!UICONTROL 身分對應]**，您可以停用此選項，然後從顯示的下拉式清單中選擇另一個名稱空間。

   ![](assets/reporting-config-namespace.png)

   進一步瞭解 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=zh-Hans){target="_blank"}.

1. 保存您所做的更改，以将选定的数据集添加到报表配置列表。

   >[!CAUTION]
   >
   >如果您选择了非事件类型的数据集，则将无法继续。

建立行銷活動報表時，您現在可以看到與您新增的資料集中使用的欄位群組相對應的量度。 前往 **[!UICONTROL 目標]** 標籤並選取您選擇的量度，以更精細地調整報表。 [了解详情](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>如果添加多个数据集，则所有数据集中的所有数据都将可用于报表。

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
