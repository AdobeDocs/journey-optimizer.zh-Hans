---
solution: Journey Optimizer
product: journey optimizer
title: 权限级别
description: 了解允许用户访问不同功能的高级别和低级别权限。
topic: Administration
feature: Access Management
role: Admin, Architect, Developer
level: Experienced
keywords: 权限，高级，低级别，配置文件， admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: b4998f62d5cc5fa134271ec5ce8c177150472a30
workflow-type: tm+mt
source-wordcount: '1126'
ht-degree: 0%

---

# 权限级别 {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

每个角色均由允许用户访问不同功能的权限组成。
它们可以分为两种类型：

* **高级权限**：表示可以分配到的不同权限 **[!UICONTROL 角色]**，例如 **[!DNL Publish journeys]** 和 **[!DNL Manage subdomains delegation]**. 高级权限包括低级权限。 有关高级权限的详情，请参见 [此页面](ootb-permissions.md).

* **低级权限**：表示来自高级别权限的不同权限。

例如， **[!DNL Journey administrator]** 角色已分配给 **[!DNL Manage journeys]** 许可。 此权限会产生低级权限，这些权限将允许历程管理员写入、读取和删除旅程。

## 历程资源 {#journey-capability}

* **[!DNL Manage journeys]** 高级权限允许用户创建新的和编辑/删除现有历程，以及访问旅程画布中用于构建旅程流的对象。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：

      * journeys.read
      * journeys.write
      * journeys.delete
      * messages.read

   * 特定于Adobe Experience Platform：

      * segments.read
      * profiles.read
      * datasets.read
      * schemas.read

+++

* **[!DNL Publish journeys]** 高级权限允许用户发布历程。

+++ 它包括以下低级权限：
   * 特定于Journey Optimizer：
      * journeys.publish
      * journeys.read

+++

* **[!DNL View journeys]** 高级权限允许用户浏览和查看历程。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * journeys.read

   * 特定于Adobe Experience Platform：
      * segments.read
      * profiles.read

+++

* **[!DNL Manage journeys events, data sources and actions]** 高级权限允许用户配置事件和数据配置。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * journeys_events.read
      * journeys_events.write
      * journeys_events.delete
      * journeys_data_sources.read
      * journeys_data_sources.write
      * journeys_data_sources.delete
      * journeys_actions.read
      * journeys_actions.write
      * journeys_actions.delete

   * 特定于Adobe Experience Platform：
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* **[!DNL View journeys events, data sources and actions]** 高级权限允许用户在历程流中使用事件和数据。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * journeys_events.read
      * journeys_data_sources.read
      * journeys_actions.read

   * 特定于Adobe Experience Platform：
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* **[!DNL View journeys report]** 高级权限允许用户只读历程报告。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * journeys_report.read
      * message_report.read

   * 特定于Adobe Experience Platform：
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

+++

## Journey Optimizer规则资源 {#journey-rules-capability}

* **[!DNL Manage frequency rules]** 高级权限允许用户读取、创建、编辑、删除和激活/停用频率规则。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

+++

* **[!DNL View frequency rules]** 高级权限允许用户查看频率规则。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * frequency_rules.read

+++

## 营销活动资源 {#campaign-capability}

* **[!DNL Export suppression list]** 高级权限允许用户以CSV文件格式下载禁止列表。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * suppression_list.export

   * 特定于Adobe Experience Platform：
      * profiles.read
      * datasets.read

+++

* **[!DNL Manage campaigns]** 高级权限允许用户创建新的和编辑/删除营销活动

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

+++

* **[!DNL Publish campaigns]** 高级权限允许用户发布营销活动。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：

      * 营销活动读取
      * campaign-publish
        <!--* experiments.activate-->

+++

* **[!DNL View campaigns report]** 高级权限允许用户阅读和编辑营销活动报告。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

+++

## 决策管理资源 {#decisions-permissions}

* **[!DNL Manage decisions]** 高级权限允许用户创建新权限和编辑/删除现有权限 **[!DNL Activity entities]**，并管理在这些活动中用于制定决策的对象。

+++ 它包括以下低级权限：

   * 决策管理特定：
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

   * 特定于Adobe Experience Platform：
      * datasets.read
      * datasets.write
      * datasets.delete
      * schemas.read
      * profile.read
      * segments.read

+++

* **[!DNL View decisions]** 高级权限允许用户使用现有活动和相关业务对象做出决策。

+++ 它包括以下低级权限：

   * 决策管理特定：
      * activities.read
      * offers.read
      * placements.read
      * ranking_strategy.read

   * 特定于Adobe Experience Platform：
      * schemas.read
      * segment.read
      * datasets.read
      * datasets.write
      * datasets.delete

+++

* **[!DNL Manage offers]** 高级权限允许用户创建、编辑和删除所有优惠、组件、读取决策和收藏集。

+++ 它包括以下低级权限：

   * 决策管理特定：
      * offers_activity.read
      * offers.read
      * offers.Write
      * offers.Delete
      * placements.Read
      * placements.Write
      * placements.Delete
      * ranking_strategy.read

   * 特定于Adobe Experience Platform：
      * schemas.read
      * segment.read
      * datasets.read
      * profiles.read

+++

* **[!DNL Manage ranking strategies]** 高级权限允许用户读取、创建、编辑和删除排名策略。

+++ 它包括以下低级权限：

   * 决策管理特定：
      * ranking_strategy.read
      * ranking_strategy.write
      * ranking_strategy.delete
      * activities.read
      * offers.read
      * placements.read

+++

## 渠道配置资源 {#administration-permissions}

* **[!DNL Manage file routing]** 高级权限允许用户创建、编辑和删除文件路由配置。

+++ 它包括以下低级权限：
   * 特定于Journey Optimizer：

      * file_routing.read
      * file_routing.write
      * file_routing.delete

+++

* **[!DNL Manage IP pools]** 高级权限允许用户创建、编辑和删除关联定义。

+++ 它包括以下低级权限：
   * 特定于Journey Optimizer：
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

+++

* **[!DNL Manage landing page settings]** 高级权限允许用户读取、创建和编辑登陆页面子域和预设设置。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

+++

* **[!DNL Manage messages general settings]** 高级权限允许用户在沙盒级别创建、编辑和删除全局设置。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * 特定于Adobe Experience Platform：
      * schemas.read

+++

* **[!DNL Manage messages presets]** 高级权限允许用户在沙盒级别跨渠道读取、创建、编辑和删除渠道表面。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read

   * 数据收集特定：
      * Mobile_setting.read <!--(from Adobe Experience Platform Launch)-->

+++

* **[!DNL Manage PTR records]** 高级权限允许用户读取和编辑已根据子域配置的PTR记录。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

+++

* **[!DNL Manage Seedlist]** 高级权限允许用户读取、创建、编辑和删除种子列表。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * seedlist.read
      * seedlist.write
      * seedlist.delete

+++

* **[!DNL Manage SMS subdomains]** 高级权限允许用户读取、创建、编辑和删除短信子域。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete

+++

* **[!DNL Manage subdomains delegations]** 高级权限允许用户创建、编辑和删除子域委派（包括IP池）。

+++ 它包括以下低级权限：
   * 特定于Journey Optimizer：

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

+++

* **[!DNL Manage suppression]** 高级权限允许用户定义在将电子邮件地址添加到禁止列表之前的退回次数，以及在禁止列表中添加和删除条目。

+++ 它包括以下低级权限：
   * 特定于Journey Optimizer：
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

+++

* **[!DNL View file routing]** 高级权限允许用户查看文件路由配置。

+++ 它包括以下低级权限：
   * 特定于Journey Optimizer：

      * file_routing.read

+++

* **[!DNL View messages general settings]** 高级权限允许用户查看消息的一般设置，如执行地址。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * messages_general_settings.read

   * 特定于Adobe Experience Platform：
      * schemas.read

+++

* **[!DNL View messages presets]** 高级权限允许用户查看消息预设。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * messages_presets.read
      * subdomains_delegation.read
      * IP_pools.read

   * 数据收集特定：
      * Mobile_setting.read

+++

* **[!DNL View PTR records]** 高级权限允许用户查看已根据子域配置的PTR记录。

+++ 它包括以下低级权限：
   * 特定于Journey Optimizer：

      * PTR_records.read
      * subdomains_delegation.read

+++

<!--
### [!DNL View channel surface] permission {#view-channel-surface}

The **[!DNL View channel surface]** high-level permission allows users to view channel surfaces in order to know which channel surfaces to use. 
  +++ It includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->


* **[!DNL View suppression list]** 高级权限允许用户查看禁止列表内容和设置。

+++ 它包括以下低级权限：

   * 特定于Journey Optimizer：
      * suppression_list.view

   * 特定于Adobe Experience Platform：
      * profiles.read
      * datasets.read

+++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ It includes the following low-level permissions: 
-->

