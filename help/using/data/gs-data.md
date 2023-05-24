---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用Journey Optimizer中的資料
description: 瞭解如何在Journey Optimizer中使用資料
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 資料，管理，平台
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: ef34cb0207d3011eca6d76ad6568f3edc00e13a3
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 1%

---

# 開始使用中的資料管理 [!DNL Journey Optimizer] {#about-data}

終端客戶資料的豐富度和涵蓋範圍決定著客戶體驗解決方案的優勢和成功；這些資料是神聖的，也是任何特定客戶的最高價值。 技術選擇現在內建於資料管理能力嚴格的評估中。

替換為 [!DNL Adobe Journey Optimizer]，您可輕鬆管理、保留這些資料，並將其匯出至屬於您技術棧疊一部分的平台或系統。

**我的資料，我的規則** - [!DNL Adobe Journey Optimizer] 不斷（且即時）建立豐富的客戶設定檔資料集，以及所有歷程資料和其操作固有的選件資料。 從您的資料庫擷取的Strawman版本使用者資料，可以豐富並轉換為涵蓋範圍及深度的高價值資料。 您既希望這些資料安全無虞，又希望這些資料無處不在，好讓您可以在整體IT生態系統中運用這些資料。

整體而言，您想要從資料中獲得的彈性是：


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="目的地" src="assets/do-not-localize/dest.png" /> 
    <br>可在其他目的地使用 — 時間 [!DNL Adobe Journey Optimizer] 針對超個人化的客戶體驗整合併協同使用資料，您希望這些資料出現在整體技術環境中的其他系統中，同時尋找其他方法運用這些資料。
    <div>
     <a href="../start/ajo-integrations.md">了解详情</a></div>
    </div>
    <br>
  </td>
</tr>
</table>

<!--td>
    <div><img alt="retention" src="assets/do-not-localize/retention.png" />  
    <br>Retained for a stipulated duration – Industry or regional regulations (such as GDPR or CCPA) or internal data governance policies stipulate how long or how short a duration, data needs to be maintained or archived in Adobe Experience Platform Data Lake. <a href="../privacy/get-started-privacy.md">Learn more</a></div>
  </td>
</tr>
<tr style="border: 0;"-->
<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="原則" src="assets/do-not-localize/policy.png" /> 
    <br>刪除依據是同意的時間表或您的原則 — 資料刪除是資料保護的重要方面，也是所有資料控管流程的關鍵步驟。 [!DNL Adobe Journey Optimizer] 可能會產生超過所需的資料。 此外，無論資料集是否因公用程式或法規而持續，您都希望最大程度地注意資料集所需持續期間之後的情形。 您需要的控制是刪除任何指定時間點的資料。 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">了解详情</a></div>
    </div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform]，在哪個 [!DNL Adobe Journey Optimizer] 內建，在參與期間以及參與結束時為您提供最高級別的資料控制。 範圍 [!DNL Journey Optimizer]，即可完全控制由以下專案產生的資料： [!DNL Journey Optimizer])、該資料上覆蓋的控管以及該資料傳送到的目的地。

所有資料都被視為客戶的屬性，只能應您的請求進行維護、加密、散佈或銷毀。 Adobe會充當您的受託人，對您的資料絕對沒有權利。

您可以使用 [!DNL Journey Optimizer]的資料彈性，可滿足與資料保留、封存或刪除相關的特定需求：

* **資料擷取/匯出**：您可以隨時透過資料存取API起始來源資料的擷取，不受任何懲罰或時間延遲。 此 [資料存取API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target="_blank"} 為使用者提供RESTful介面，著重於內擷取資料集的可發現性和可存取性 [!DNL Adobe Experience Platform]. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   請注意，無法透過上述的API或目的地方法擷取歷程或行銷活動中使用的內容。

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer’s default setting of retaining this data for up to 30 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization’s data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **清除與封存機制**：資料清除和封存可自由定義，並可在以下位置自動化： [!DNL Adobe Journey Optimizer] 自動化資料保留政策。 您可以為不同的資料實體定義不同的老化策略。 也可定義匯出機制，以在清除或封存老化資料之前自動匯出該資料。

   資料衛生工作區可讓您建立及監控各種資料衛生工作，包括刪除消費者身分和排程資料集有效期。 此工作區隨Security &amp; Privacy Shield和Healthcare Shield提供。 请参阅[此页面](../privacy/data-hygiene.md)以了解详情。

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **參與終止/結束時的資料擷取**：合約終止時，您的資料會從Adobe的儲存空間完全移除。 此外，您也可以在終止協定之前提取完整的設定檔擷取。 此功能不需額外付費。 這可以隨時完成，而且不僅僅是在終止時。

上述方法皆由合約定義，並在資料處理協定(DPA)中詳細說明，而Adobe在合約開始時會與您相互同意。 Adobe應用程式，包括 [!DNL Journey Optimizer]，是根據每個使用者端的資料都被視為該使用者端專有資料資產的原則所設計。
