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
source-git-commit: da885bd5e29ff3454fef1c6b362f0e646fe8c39a
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 0%

---

# 权限级别 {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

每个产品配置文件都包含允许用户访问不同功能的权限。
分为两种类型：

* **高级权限**:表示可分配给的不同权限 **[!UICONTROL Product profile]** 在 [!DNL Admin console]，例如 **[!UICONTROL Publish journeys]** 和 **[!UICONTROL Manage subdomains delegation]**. 高级权限包含低级权限。

* **低级别权限**:表示来自高级权限的不同权限。

例如， **[!UICONTROL Journey administrator]** 已分配产品配置文件 **[!UICONTROL Manage journeys]** 权限。 从此权限中，将产生低级权限，该权限将允许历程管理员写入、读取和删除历程。

## 历程功能 {#journey-capability}

### 管理历程权限 {#manage-journeys}

的 **[!UICONTROL Manage journeys]** 高级权限允许用户创建新历程和编辑/删除现有访客，以及访问历程画布中用于构建历程流的对象。

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

### 发布历程权限 {#publish-journeys}

的 **[!UICONTROL Publish journeys]** 用户通过高级权限发布历程。

它包括以下低级权限：

* Journey Optimizer特定：
   * journeys.publish
   * journeys.read

### 查看历程权限 {#view-journeys}

的 **[!UICONTROL View journeys]** 高级权限允许用户浏览和查看历程。

它包括以下低级权限：

* Journey Optimizer特定：
   * journeys.read

* Adobe Experience Platform特定：
   * segments.read
   * profiles.read

### 管理历程事件、数据源和操作权限 {#manage-journeys-events}

的 **[!UICONTROL Manage journeys events, data sources and actions]** 高级权限允许用户配置事件和数据配置。

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

### 查看历程事件、数据源和操作权限 {#view-journeys-event}

的 **[!UICONTROL View journeys events, data sources and actions]** 高级权限允许用户在历程流中使用事件和数据。

它包括以下低级权限：

* Journey Optimizer特定：
   * journeys_events.read
   * journeys_data_sources.read
   * journeys_actions.read

* Adobe Experience Platform特定：
   * schemas.read
   * datasets.read
   * identity_namespace.read

### 查看历程报表权限 {#view-journeys-report}

的 **[!UICONTROL View journeys report]** 高级权限允许用户报告只读历程。

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

### 管理消息权限 {#manage-messages}

的 **[!UICONTROL Manage messages]** 高级权限允许用户创建和编辑/删除消息。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Adobe Experience Platform特定：
   * segments.read
   * schemas.read

### 管理消息预览和测试权限 {#mange-messages-preview}

的 **[!UICONTROL Manage messages preview and test]** 高级权限允许用户预览个性化消息。

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

### 发布消息权限 {#publish-messages}

的 **[!UICONTROL Publish messages]** 高级权限允许用户发布消息。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages.publish

* Adobe Experience Platform特定：
   * profiles.read
   * schemas.read
   * datasets.read

### 查看消息权限 {#view-messages}

的 **[!UICONTROL View messages]** 高级权限允许用户只读消息。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages.read
   * messages_presets.read

* Adobe Experience Platform特定：
   * schemas.read
   * segments.read

### 查看消息报表权限 {#view-message-reports}

的 **[!UICONTROL View messages report]** 高级权限允许用户使用只读电子邮件和推送报表。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## 决策管理能力 {#decisions-permissions}

### 管理决策权限 {#manage-decisioning}

的 **[!UICONTROL Manage decisions]** 高级权限允许用户创建新页面，以及编辑/删除现有页面 **[!UICONTROL Activity entities]**，以及管理这些活动中用于做出决策的对象。

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

### 查看决策权限 {#view-decisions}

的 **[!UICONTROL View decisions]** 高级权限允许用户使用现有活动和相关业务对象做出决策。

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

### 发布选件决策权限 {#publish-decisions}

的 **[!UICONTROL Publish offers decisioning]** 高级权限允许用户访问批准/取消批准选件活动。

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

### 管理排名策略权限 {#manage-decisions}

的 **[!UICONTROL Manage ranking strategies]** 高级权限允许用户读取、创建、编辑和删除自定义消息报表以及使用操作功能。

它包括以下低级权限：

* 具体决策管理：
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## 管理能力 {#administration-permissions}

### 管理子域委派权限 {#manage-subdomain}

的 **[!UICONTROL Manage subdomains delegation]** 高级权限允许用户创建、编辑和删除子域委派（包括IP池）。

它包括以下低级权限：

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### 查看PTR记录权限 {#view-ptr}

的 **[!UICONTROL View PTR records]** 高级权限允许用户查看基于子域配置的PTR记录。

它包括以下低级权限：

* PTR_records.read
* subdomains_delegation.read

### 管理IP池权限 {#manage-ip-pools}

的 **[!UICONTROL Manage IP pools]** 高级权限允许用户创建、编辑和删除亲和度定义。

它包括以下低级权限：

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### 管理消息常规设置权限 {#manage-message-settings}

的 **[!UICONTROL Manage messages general settings]** 高级权限允许用户在沙盒级别创建、编辑和删除全局设置。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* Adobe Experience Platform特定：
   * schemas.read

### 查看消息常规设置权限 {#view-message-settings}

的 **[!UICONTROL View messages general settings]** 高级权限允许用户查看消息的常规设置，如执行地址。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages_general_settings.read
* Adobe Experience Platform特定：
   * schemas.read

### 管理消息预设权限 {#manage-message-presets}

的 **[!UICONTROL Manage messages presets]** 高级权限允许用户在沙盒级别跨渠道创建、编辑和删除消息预设。

它包括以下低级权限：

* Journey Optimizer特定：
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read(从Adobe Experience Platform Launch)

### 查看消息预设权限 {#view-message-presets}

的 **[!UICONTROL View messages presets]** 高级权限允许用户查看消息预设，以便了解在创建消息时要使用的消息预设。

它包括以下低级权限：

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read(从Adobe Experience Platform Launch)

### 管理抑制权限 {#manage-suppression}

的 **[!UICONTROL Manage suppression]** 高级权限允许用户在将电子邮件地址添加到禁止列表之前定义退回次数，以及向禁止列表添加和删除条目。

它包括以下低级权限：

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### 查看禁止列表权限 {#view-suppresion-list}

的 **[!UICONTROL View suppression list]** 高级权限允许用户查看禁止列表内容和设置。

它包括以下低级权限：

* Journey Optimizer特定：
   * suppression_list.view
* Adobe Experience Platform特定：
   * profiles.read
   * datasets.read

### 导出抑制列表权限 {#export-suppression-list}

的 **[!UICONTROL Export suppression list]** 高级权限允许用户将禁止列表下载为CSV文件。

它包括以下低级权限：

* Journey Optimizer特定：
   * suppression_list.export
* Adobe Experience Platform特定：
   * profiles.read
   * datasets.read
