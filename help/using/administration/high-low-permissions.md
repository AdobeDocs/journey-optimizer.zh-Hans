---
title: 权限级别
description: 了解高级和低级权限
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Control Groups
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: bbeecbacb4838dfb0794d5625eb2774cf4b983ef
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# 权限级别 {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

每个产品配置文件都包含允许用户访问不同功能的权限。
分为两种类型：

* **高级权限**:表示可分配给的不同权限 **[!UICONTROL Product profile]** 在 [!DNL Admin console]，例如 **[!DNL Publish journeys]** 和 **[!DNL Manage subdomains delegation]**. 高级权限包含低级权限。

* **低级别权限**:表示来自高级权限的不同权限。

例如， **[!DNL Journey administrator]** 已分配产品配置文件 **[!DNL Manage journeys]** 权限。 从此权限中，将产生低级权限，该权限将允许历程管理员写入、读取和删除历程。

## 历程功能 {#journey-capability}

### [!DNL Manage journeys] 许可 {#manage-journeys}

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

### [!DNL Publish journeys] 许可 {#publish-journeys}

的 **[!DNL Publish journeys]** 用户通过高级权限发布历程。

它包括以下低级权限：

* Journey Optimizer特定：
   * journeys.publish
   * journeys.read

### [!DNL View journeys] 许可 {#view-journeys}

的 **[!DNL View journeys]** 高级权限允许用户浏览和查看历程。

它包括以下低级权限：

* Journey Optimizer特定：
   * journeys.read

* Adobe Experience Platform特定：
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] 许可 {#manage-journeys-events}

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

### [!DNL View journeys events, data sources and actions] 许可 {#view-journeys-event}

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

### [!DNL View journeys report] 许可 {#view-journeys-report}

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

## 消息功能 {#message-capability}

### [!DNL Manage messages] 许可 {#manage-messages}

的 **[!DNL Manage messages]** 高级权限允许用户创建和编辑/删除消息。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Adobe Experience Platform特定：
   * segments.read
   * schemas.read

### [!DNL Manage messages preview and test] 许可 {#mange-messages-preview}

的 **[!DNL Manage messages preview and test]** 高级权限允许用户预览个性化消息。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages.publish
   * messages_preview_and_test.write
   * messages.publish

* Adobe Experience Platform特定：
   * profiles.read
   * profiles.write
   * schemas.read
   * datasets.write
   * datasets.read
   * identity_namespace.read
   * segments.read
   * queries.write
   * merge_policies.read

### [!DNL Publish messages] 许可 {#publish-messages}

的 **[!DNL Publish messages]** 高级权限允许用户发布消息。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages.publish

* Adobe Experience Platform特定：
   * profiles.read
   * schemas.read
   * datasets.read

### [!DNL View messages] 许可 {#view-messages}

的 **[!DNL View messages]** 高级权限允许用户只读消息。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages.read
   * messages_presets.read

* Adobe Experience Platform特定：
   * schemas.read
   * segments.read

### [!DNL View messages report] 许可 {#view-message-reports}

的 **[!DNL View messages report]** 高级权限允许用户使用只读电子邮件和推送报表。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## 决策管理能力 {#decisions-permissions}

### [!DNL Manage decisions] 许可 {#manage-decisioning}

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

### [!DNL View decisions] 许可 {#view-decisions}

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

### [!DNL Publish offers decisioning] 许可 {#publish-decisions}

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

### [!DNL Manage ranking strategies] 许可 {#manage-decisions}

的 **[!DNL Manage ranking strategies]** 高级权限允许用户读取、创建、编辑和删除自定义消息报表以及使用操作功能。

它包括以下低级权限：

* 具体决策管理：
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## 管理能力 {#administration-permissions}

### [!DNL Manage subdomains delegation] 许可 {#manage-subdomain}

的 **[!DNL Manage subdomains delegation]** 高级权限允许用户创建、编辑和删除子域委派（包括IP池）。

它包括以下低级权限：

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### [!DNL Manage PTR records] 许可 {#manage-ptr}

的 **[!DNL Manage PTR records]** 高级权限允许用户读取、创建、编辑和删除基于子域配置的PTR记录。

它包括以下低级权限：

* PTR_records.read
* PTR_records.write
* subdomains_delegation.read

### [!DNL View PTR records] 许可 {#view-ptr}

的 **[!DNL View PTR records]** 高级权限允许用户查看基于子域配置的PTR记录。

它包括以下低级权限：

* PTR_records.read
* subdomains_delegation.read

### [!DNL Manage IP pools] 许可 {#manage-ip-pools}

的 **[!DNL Manage IP pools]** 高级权限允许用户创建、编辑和删除亲和度定义。

它包括以下低级权限：

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### [!DNL Manage messages general settings] 许可 {#manage-message-settings}

的 **[!DNL Manage messages general settings]** 高级权限允许用户在沙盒级别创建、编辑和删除全局设置。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* Adobe Experience Platform特定：
   * schemas.read

### [!DNL View messages general settings] 许可 {#view-message-settings}

的 **[!DNL View messages general settings]** 高级权限允许用户查看消息的常规设置，如执行地址。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages_general_settings.read
* Adobe Experience Platform特定：
   * schemas.read

### [!DNL Manage messages presets] 许可 {#manage-message-presets}

的 **[!DNL Manage messages presets]** 高级权限允许用户在沙盒级别跨渠道创建、编辑和删除消息预设。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read(从Adobe Experience Platform Launch)

### [!DNL View messages presets] 许可 {#view-message-presets}

的 **[!DNL View messages presets]** 高级权限允许用户查看消息预设，以便了解在创建消息时要使用的消息预设。

它包括以下低级权限：

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read(从Adobe Experience Platform数据收集)

### [!DNL Manage suppression] 许可 {#manage-suppression}

的 **[!DNL Manage suppression]** 高级权限允许用户在将电子邮件地址添加到禁止列表之前定义退回次数，以及向禁止列表添加和删除条目。

它包括以下低级权限：

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### [!DNL View suppression list] 许可 {#view-suppression-list}

的 **[!DNL View suppression list]** 高级权限允许用户查看禁止列表内容和设置。

它包括以下低级权限：

* Journey Optimizer特定：
   * suppression_list.view

* Adobe Experience Platform特定：
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] 许可 {#export-suppression-list}

的 **[!DNL Export suppression list]** 高级权限允许用户将禁止列表下载为CSV文件。

它包括以下低级权限：

* Journey Optimizer特定：
   * suppression_list.export

* Adobe Experience Platform特定：
   * profiles.read
   * datasets.read
