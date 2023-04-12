---
solution: Journey Optimizer
product: journey optimizer
title: 权限级别
description: 了解允许用户访问不同功能的高级和低级权限。
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: 权限，高级，低级别，配置文件，管理控制台
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 2%

---

# 权限级别 {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

每个产品配置文件都包含允许用户访问不同功能的权限。
分为两种类型：

* **高级权限**:表示可分配给的不同权限 **[!UICONTROL 产品配置文件]** 在 [!DNL Admin console]，例如 **[!DNL Publish journeys]** 和 **[!DNL Manage subdomains delegation]**. 高级权限包含低级权限。

* **低级别权限**:表示来自高级权限的不同权限。

例如， **[!DNL Journey administrator]** 已分配产品配置文件 **[!DNL Manage journeys]** 权限。 从此权限中，将产生低级权限，该权限将允许历程管理员写入、读取和删除历程。

## 历程功能 {#journey-capability}

### [!DNL Manage journeys] 权限 {#manage-journeys}

的 **[!DNL Manage journeys]** 高级权限允许用户创建新历程和编辑/删除现有访客，以及访问历程画布中用于构建历程流的对象。

它包括以下低级权限：

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

的 **[!DNL Publish journeys]** 用户通过高级权限发布历程。

它包括以下低级权限：

* Journey Optimizer特定：
   * journeys.publish
   * journeys.read

### [!DNL View journeys] 权限 {#view-journeys}

的 **[!DNL View journeys]** 高级权限允许用户浏览和查看历程。

它包括以下低级权限：

* Journey Optimizer特定：
   * journeys.read

* Adobe Experience Platform特定：
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] 权限 {#manage-journeys-events}

的 **[!DNL Manage journeys events, data sources and actions]** 高级权限允许用户配置事件和数据配置。

它包括以下低级权限：

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

的 **[!DNL View journeys events, data sources and actions]** 高级权限允许用户在历程流中使用事件和数据。

它包括以下低级权限：

* Journey Optimizer特定：
   * journeys_events.read
   * journeys_data_sources.read
   * journeys_actions.read

* Adobe Experience Platform特定：
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys report] 权限 {#view-journeys-report}

的 **[!DNL View journeys report]** 高级权限允许用户报告只读历程。

它包括以下低级权限：

* Journey Optimizer特定：
   * journeys_report.read
   * messages_report.read

* Adobe Experience Platform特定：
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## 决策管理能力 {#decisions-permissions}

### [!DNL Manage decisions] 权限 {#manage-decisioning}

的 **[!DNL Manage decisions]** 高级权限允许用户创建新页面，以及编辑/删除现有页面 **[!DNL Activity entities]**，以及管理这些活动中用于做出决策的对象。

它包括以下低级权限：

* 具体决策管理：
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

的 **[!DNL View decisions]** 高级权限允许用户使用现有活动和相关业务对象做出决策。

它包括以下低级权限：

* 具体决策管理：
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

的 **[!DNL Publish offers decisioning]** 高级权限允许用户访问批准/取消批准选件活动。

它包括以下低级权限：

* 具体决策管理：
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

的 **[!DNL Manage ranking strategies]** 高级权限允许用户读取、创建、编辑和删除排名策略。

它包括以下低级权限：

* 具体决策管理：
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## 管理能力 {#administration-permissions}

### [!DNL Manage subdomains delegation] 权限 {#manage-subdomain}

的 **[!DNL Manage subdomains delegation]** 高级权限允许用户创建、编辑和删除子域委派（包括IP池）。

它包括以下低级权限：

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### [!DNL Manage PTR records] 权限 {#manage-ptr}

的 **[!DNL Manage PTR records]** 高级权限允许用户读取和编辑已基于子域配置的PTR记录。

它包括以下低级权限：

* PTR_records.read
* PTR_records.write
* subdomains_delegation.read

### [!DNL View PTR records] 权限 {#view-ptr}

的 **[!DNL View PTR records]** 高级权限允许用户查看基于子域配置的PTR记录。

它包括以下低级权限：

* PTR_records.read
* subdomains_delegation.read

### [!DNL Manage IP pools] 权限 {#manage-ip-pools}

的 **[!DNL Manage IP pools]** 高级权限允许用户创建、编辑和删除亲和度定义。

它包括以下低级权限：

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

的 **[!DNL Manage channel surface]** 高级权限允许用户在沙盒级别跨渠道创建、编辑和删除渠道表面。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read(从Adobe Experience Platform Launch)

### [!DNL View channel surface] 权限 {#view-channel-surface}

的 **[!DNL View channel surface]** 高级权限允许用户查看通道曲面，以便知道要使用哪些通道曲面。

它包括以下低级权限：

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read(从Adobe Experience Platform数据收集)

### [!DNL Manage suppression] 权限 {#manage-suppression}

的 **[!DNL Manage suppression]** 高级权限允许用户在将电子邮件地址添加到禁止列表之前定义退回次数，以及向禁止列表添加和删除条目。

它包括以下低级权限：

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### [!DNL View suppression list] 权限 {#view-suppression-list}

的 **[!DNL View suppression list]** 高级权限允许用户查看禁止列表内容和设置。

它包括以下低级权限：

* Journey Optimizer特定：
   * suppression_list.view

* Adobe Experience Platform特定：
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] 权限 {#export-suppression-list}

的 **[!DNL Export suppression list]** 高级权限允许用户将禁止列表下载为CSV文件。

它包括以下低级权限：

* Journey Optimizer特定：
   * suppression_list.export

* Adobe Experience Platform特定：
   * profiles.read
   * datasets.read

### [!DNL Manage landing page settings] 权限 {#manage-landing-page-settings}

的 **[!DNL Manage landing page settings]** 高级权限允许用户读取、创建和编辑登陆页面子域和预设设置。

它包括以下低级权限：

* Journey Optimizer特定：
   * landing_page_subdomain.read
   * landing_page_subdomain.write
   * landing_page_subdomain.delete
   * landing_page_preset.read
   * landing_page_preset.write
   * landing_page_preset.delete

### [!DNL Manage frequency rules] 权限 {#manage-frequency-rules}

的 **[!DNL Manage frequency rules]** 高级权限允许用户读取、创建、编辑、删除和激活/停用频度规则。

它包括以下低级权限：

* Journey Optimizer特定：
   * frequency_rules.read
   * frequency_rules.write
   * frequency_rules.delete

### [!DNL View frequency rules] 权限 {#view-frequency-rules}

的 **[!DNL View frequency rules]** 高级权限允许用户查看频度规则。

它包括以下低级权限：

* Journey Optimizer特定：
   * frequency_rules.read
