---
solution: Journey Optimizer
product: journey optimizer
title: 权限级别
description: 瞭解允許使用者存取不同功能的高層級和低層級許可權。
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: 許可權，高階，低階，設定檔， admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 2%

---

# 权限级别 {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

每個產品設定檔都包含許可權，可讓使用者存取不同功能。
它們可以分為兩種型別：

* **高階許可權**：代表可指派給的不同許可權 **[!UICONTROL 產品設定檔]** 在 [!DNL Admin console]，例如 **[!DNL Publish journeys]** 和 **[!DNL Manage subdomains delegation]**. 高層級許可權包含低層級許可權。

* **低階許可權**：代表來自高階許可權的不同許可權。

例如， **[!DNL Journey administrator]** 產品設定檔已指派 **[!DNL Manage journeys]** 許可權。 此許可權會產生低階許可權，可讓Journey管理員寫入、讀取和刪除歷程。

## 歷程功能 {#journey-capability}

### [!DNL Manage journeys] 权限 {#manage-journeys}

此 **[!DNL Manage journeys]** 高階許可權可讓使用者建立新歷程及編輯/刪除現有歷程，以及存取歷程畫布中用來建立歷程流程的物件。

其中包含下列低階許可權：

* Journey Optimizer特定：

   * journeys.read
   * journeys.write
   * journeys.delete
   * messages.read

* Adobe Experience Platform特定：

   * segments.read
   * profiles.read
   * datasets.read
   * schemas.read

### [!DNL Publish journeys] 权限 {#publish-journeys}

此 **[!DNL Publish journeys]** 高階許可權可讓使用者發佈歷程。

其中包含下列低階許可權：

* Journey Optimizer特定：
   * journeys.publish
   * journeys.read

### [!DNL View journeys] 权限 {#view-journeys}

此 **[!DNL View journeys]** 高階許可權可讓使用者瀏覽和檢視歷程。

其中包含下列低階許可權：

* Journey Optimizer特定：
   * journeys.read

* Adobe Experience Platform特定：
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] 权限 {#manage-journeys-events}

此 **[!DNL Manage journeys events, data sources and actions]** 高階許可權可讓使用者設定事件和資料設定。

其中包含下列低階許可權：

* Journey Optimizer特定：
   * journeys_events.read
   * journeys_events.write
   * journeys_events.delete
   * journeys_data_sources.read
   * journeys_data_sources.write
   * journeys_data_sources.delete
   * journeys_actions.read
   * journeys_actions.write
   * journeys_actions.delete

* Adobe Experience Platform特定：
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys events, data sources and actions] 权限 {#view-journeys-event}

此 **[!DNL View journeys events, data sources and actions]** 高階許可權可讓使用者在歷程流程中使用事件和資料。

其中包含下列低階許可權：

* Journey Optimizer特定：
   * journeys_events.read
   * journeys_data_sources.read
   * journeys_actions.read

* Adobe Experience Platform特定：
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys report] 权限 {#view-journeys-report}

此 **[!DNL View journeys report]** 高階許可權可讓使用者以唯讀方式存取歷程報告。

其中包含下列低階許可權：

* Journey Optimizer特定：
   * journeys_report.read
   * message_report.read

* Adobe Experience Platform特定：
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## 決策管理功能 {#decisions-permissions}

### [!DNL Manage decisions] 权限 {#manage-decisioning}

此 **[!DNL Manage decisions]** 高階許可權可讓使用者建立新專案和編輯/刪除現有專案 **[!DNL Activity entities]**，以及管理用於這些活動中以做出決策的物件。

其中包含下列低階許可權：

* 特定決策管理：
   * activities.read
   * activities.write
   * activities.delete
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Adobe Experience Platform特定：
   * datasets.read
   * datasets.write
   * datasets.delete
   * schemas.read
   * profile.read
   * segments.read

### [!DNL View decisions] 权限 {#view-decisions}

此 **[!DNL View decisions]** 高階許可權可讓使用者使用現有活動和相關商業物件來做出決定。

其中包含下列低階許可權：

* 特定決策管理：
   * activities.read
   * offers.read
   * placements.read
   * ranking_strategy.read

* Adobe Experience Platform特定：
   * schemas.read
   * segment.read
   * datasets.read
   * datasets.write
   * datasets.delete

### [!DNL Publish offers decisioning] 权限 {#publish-decisions}

此 **[!DNL Publish offers decisioning]** 高階許可權可讓使用者存取以核准/取消核准優惠方案活動。

其中包含下列低階許可權：

* 特定決策管理：
   * offers_activity.read
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Adobe Experience Platform特定：
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### [!DNL Manage ranking strategies] 权限 {#manage-ranking-strategies}

此 **[!DNL Manage ranking strategies]** 高階許可權可讓使用者讀取、建立、編輯和刪除排名策略。

其中包含下列低階許可權：

* 特定決策管理：
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## 管理功能 {#administration-permissions}

### [!DNL Manage subdomains delegation] 权限 {#manage-subdomain}

此 **[!DNL Manage subdomains delegation]** 高階許可權可讓使用者建立、編輯和刪除子網域委派（包括IP集區）。

其中包含下列低階許可權：

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### [!DNL Manage PTR records] 权限 {#manage-ptr}

此 **[!DNL Manage PTR records]** 高階許可權可讓使用者讀取和編輯已根據子網域設定的PTR記錄。

其中包含下列低階許可權：

* PTR_records.read
* PTR_records.write
* subdomains_delegation.read

### [!DNL View PTR records] 权限 {#view-ptr}

此 **[!DNL View PTR records]** 高階許可權可讓使用者檢視已根據子網域設定的PTR記錄。

其中包含下列低階許可權：

* PTR_records.read
* subdomains_delegation.read

### [!DNL Manage IP pools] 权限 {#manage-ip-pools}

此 **[!DNL Manage IP pools]** 高階許可權可讓使用者建立、編輯和刪除相似性定義。

其中包含下列低階許可權：

* IP_pools.read
* IP_pools.write
* IP_pools.delete

<!--
### [!DNL Manage messages general settings] permission {#manage-message-settings}

The **[!DNL Manage messages general settings]** high-level permission allows users to create, edit and delete global settings at the sandbox level.

It includes the following low-level permissions: 

* Journey Optimizer specific: 
  * messages_general_settings.read
  * messages_general_settings.write
  * messages_general_settings.delete
* Adobe Experience Platform specific:
  * schemas.read

### [!DNL View messages general settings] permission {#view-message-settings}

The **[!DNL View messages general settings]** high-level permission allows users to view messages general settings such as the execution address.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  * messages_general_settings.read
* Adobe Experience Platform specific: 
  * schemas.read
-->

### [!DNL Manage channel surface] 权限 {#manage-channel-surface}

此 **[!DNL Manage channel surface]** 高階許可權可讓使用者在沙箱層級建立、編輯和刪除跨頻道的頻道介面。

其中包含下列低階許可權：

* Journey Optimizer特定：
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (來自Adobe Experience Platform Launch)

### [!DNL View channel surface] 权限 {#view-channel-surface}

此 **[!DNL View channel surface]** 高階許可權可讓使用者檢視管道表面，以瞭解要使用哪些管道表面。

其中包含下列低階許可權：

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (來自Adobe Experience Platform Data Collection)

### [!DNL Manage suppression] 权限 {#manage-suppression}

此 **[!DNL Manage suppression]** 高階許可權可讓使用者定義將電子郵件地址新增至隱藏清單前的跳出次數，以及在隱藏清單中新增和刪除專案。

其中包含下列低階許可權：

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### [!DNL View suppression list] 权限 {#view-suppression-list}

此 **[!DNL View suppression list]** 高階許可權可讓使用者檢視隱藏清單內容和設定。

其中包含下列低階許可權：

* Journey Optimizer特定：
   * suppression_list.view

* Adobe Experience Platform特定：
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] 权限 {#export-suppression-list}

此 **[!DNL Export suppression list]** 高階許可權可讓使用者將隱藏清單下載為CSV檔案。

其中包含下列低階許可權：

* Journey Optimizer特定：
   * suppression_list.export

* Adobe Experience Platform特定：
   * profiles.read
   * datasets.read

### [!DNL Manage landing page settings] 权限 {#manage-landing-page-settings}

此 **[!DNL Manage landing page settings]** 高階許可權可讓使用者讀取、建立及編輯登陸頁面子網域和預設集設定。

其中包含下列低階許可權：

* Journey Optimizer特定：
   * landing_page_subdomain.read
   * landing_page_subdomain.write
   * landing_page_subdomain.delete
   * landing_page_preset.read
   * landing_page_preset.write
   * landing_page_preset.delete

### [!DNL Manage frequency rules] 权限 {#manage-frequency-rules}

此 **[!DNL Manage frequency rules]** 高階許可權可讓使用者讀取、建立、編輯、刪除和啟用/停用頻率規則。

其中包含下列低階許可權：

* Journey Optimizer特定：
   * frequency_rules.read
   * frequency_rules.write
   * frequency_rules.delete

### [!DNL View frequency rules] 权限 {#view-frequency-rules}

此 **[!DNL View frequency rules]** 高階許可權可讓使用者檢影片率規則。

其中包含下列低階許可權：

* Journey Optimizer特定：
   * frequency_rules.read
