---
solution: Journey Optimizer
product: journey optimizer
title: 将数据集导出到云存储位置
description: 瞭解如何使用Adobe Experience Platform雲端儲存空間目的地匯出資料集。
role: User
level: Beginner
badge: label="Beta" type="Informative"
keywords: 平台、数据湖、创建、湖、数据集、个人资料
exl-id: 66b5c691-ddc4-4e9b-9386-2ce6c307451c
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 8%

---

# 将数据集导出到云存储位置 {#export-datasets}

>[!AVAILABILITY]
>
>資料集匯出功能目前為測試版，可供所有Adobe Journey Optimizer使用者使用。 如果您尚未拥有访问权限，请与 Adobe 代表联系，获取目标的访问权限。

Journey Optimizer可讓您建立與雲端儲存位置的即時連線，以匯出資料集的內容。

藉由定期匯出資料，您可以確保擁有完整且最新的客戶互動記錄、將此資訊用於報告或分析目的，以及維持符合法律規定。

## 可用的雲端儲存空間目的地 {#destinations}

您可以將資料集匯出至6個雲端儲存空間目的地，您可從以下位置存取： **[!UICONTROL 目的地]** 功能表，在 **[!UICONTROL 目錄]** 標籤。

![](assets/dataset-export-setup.png)

>[!AVAILABILITY]
>
>這些目的地均提供測試版且隨時可能變更。

Adobe Experience Platform檔案中提供每個目的地的詳細資訊：

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html)
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html)
* [Azure Data Lake Gen 2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html)
* [数据登陆区](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html)
* [Google雲端儲存空間](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html)

## 先决条件 {#prerequisites}

開始匯出資料集之前，請先檢查下列必要條件：

* 若要匯出資料集，您需要 **管理目的地**， **檢視目的地**， **啟用目的地**、和 **管理和啟用資料集目的地** [存取控制許可權](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html#permissions). 閱讀 [存取控制總覽](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html) 或聯絡您的產品管理員以取得必要許可權。

* 此功能僅支援匯出第一代資料，亦即中定義的原始資料 [Real-time Customer Data Platform產品說明](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2c-edition-prime-and-ultimate-packages.html). 請確定您要匯出的資料集未包含第二代資料。

## 匯出資料集的主要步驟 {#main-steps}

將資料集匯出至雲端儲存位置的主要步驟如下：

![](assets/dataset-export-process.png)

Adobe Experience Platform檔案中提供每個步驟的詳細資訊： [將資料集匯出至雲端儲存空間目的地](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en).

1. **設定您的雲端儲存空間目的地**. 如果您尚未這樣做，請從目的地目錄連線至雲端儲存空間目的地。 [瞭解如何建立新的目的地連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=en#setup)

   <!--![](assets/dataset-export-setup.png)-->

1. **選取雲端儲存空間目的地** 匯出資料集的位置。 在目的地目錄中，按一下 **[!UICONTROL 匯出資料集]** 按鈕，並選取要使用的連線。

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >如果您使用Adobe Journey Optimizer以及即時客戶設定檔，目的地卡片會顯示「啟用」按鈕，讓您根據您啟用的許可權，匯出資料集並啟用此目的地的區段。

1. **選取資料集** 要匯出至所選目的地的檔案。

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **排程匯出** 資料集的URL名稱。 指定開始匯出的時間以及開始匯出的頻率。

   <!--![](assets/dataset-export-schedule.png)-->

1. **檢閱並確認匯出** 檢查設定結束時顯示的摘要。

   <!--![](assets/dataset-export-review.png)-->

匯出完成後，資料集的內容會根據您設定的排程儲存在雲端儲存位置。 [瞭解如何驗證資料集匯出是否成功](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html#verify)
