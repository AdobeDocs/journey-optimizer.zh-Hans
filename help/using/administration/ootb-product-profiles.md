---
title: 内置产品配置文件
description: 了解内置的产品配置文件
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: f5627a23ceb0d00dd01db8766e72fed1b5d652a3
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 10%

---

# 内置产品配置文件 {#ootb-product-profiles}

## [!DNL Journey Administrator] {#journey-administrator}

的 **[!DNL Journey Administrator]** 产品配置文件允许管理菜单，其中可以管理和发布历程、消息和决策管理。

此产品用户档案包括以下权限：

|功能 |权限| |-|-| |历程| <ul><li> **[!DNL Manage journeys]**:读取、创建、编辑和删除历程。</li><li>**[!DNL Publish journeys]**:发布历程。</li><li>**[!DNL Manage journeys events, data sources and actions]**:读取、创建、编辑和删除事件、源或操作。</li><li>**[!DNL View journeys report]**:阅读和编辑历程报告。</li></ul>|
|消息|<ul><li> **[!DNL Manage messages]**:读取、创建、编辑消息预览并发送测试/校样。</li><li>**[!DNL Manage messages preview and test]**:发布消息。</li><li>**[!DNL Publish messages]**:读取、创建和编辑消息预览并发送测试/校样。</li><li>**[!DNL View messages report]**:阅读和编辑消息报表。</li></ul>|
|管理|<ul><li>**[!DNL Manage subdomains delegation]**:读取、创建、编辑和删除子域委派。</li><li>**[!DNL Manage IP pools]**:读取、创建、编辑和删除ip池。</li><li>**[!DNL Manage PTR records]**:读取和编辑PTR记录。</li><li>**[!DNL View PTR records]**:对PTR记录的只读访问。</li><li> **[!DNL Manage messages general settings]**:读取、创建、编辑和删除消息常规设置。</li><li>**[!DNL Manage messages presets]**:读取、创建、编辑和删除内容品牌。</li><li>**[!DNL Manage suppression rules]**:访问读取、创建、编辑和删除隐藏规则。</li><li>**[!DNL View suppression list]**:读取和导出本地抑制列表。</li><li>**[!DNL Manage alerts]**:启用/禁用旅程、消息和授权的警报。</li></ul>|
|决策管理|<ul><li>**[!DNL Manage decisions]**:读取、创建、编辑和删除决策。</li><li>**[!DNL Manage ranking strategies]**:读取、创建、编辑和删除排名策略。</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**:授予对沙箱的访问权限。</li><li>**[!DNL Manage segments]**:读取、创建、编辑和删除区段。</li><li>**[!DNL Manage profiles]**:读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**:对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**:对架构的只读访问。</li><li>**[!DNL Read Identity namespace]**:对身份命名空间的只读访问权限。</li><li>**[!DNL Manage merge policies]**:读取、创建、编辑和删除合并策略。</li></ul>| |Journey Optimizer库|<ul><li>**[!DNL Manage Library Items]**:添加和删除 [!DNL Journey Optimizer] 库。</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

的 **[!DNL Journey Approver]** 产品用户档案允许用户批准投放并发布它们。 他们稍后可以使用 **[!DNL Message]** 和 **[!DNL Journey]** 报表。

此产品用户档案包括以下权限：

|功能 |权限| |-|-| |历程| <ul><li>**[!DNL Manage journeys]**:读取、创建、编辑和删除历程。</li><li>**[!DNL Publish journey]**:发布历程。</li><li>**[!DNL View journeys events, data sources and actions]**:对历程事件、历程自定义操作和历程数据源的只读访问。</li><li>**[!DNL View journeys report]**:阅读、编辑历程报告。</li></ul>|
|消息| <ul><li>**[!DNL Manage messages]**:读取、创建、编辑和删除消息。</li><li>**[!DNL Publish messages]** 发布消息。</li><li>**[!DNL Manage messages preview and test]**:读取、创建和编辑消息预览并发送测试/校样。</li><li>**[!DNL View messages report]**:读取、创建、编辑和删除消息报表。</li></ul>|
|决策管理| <ul><li>**[!DNL Manage decisions]**:读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**:读取、创建、编辑和删除自定义消息报表以及使用操作功能。</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**:读取、创建、编辑和删除区段。</li><li>**[!DNL Manage profiles]**:读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**:对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**:对架构的只读访问。</li><li>**[!DNL Manage merge policies]**:读取、创建、编辑和删除合并策略。</li></ul>|
|管理| <ul><li>**[!DNL View messages presets]**:对消息预设的只读访问权限。</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

的 **[!DNL Journey Manager]** 产品配置文件允许用户创建和编辑 **[!UICONTROL Journeys]** 和链接到 **[!UICONTROL Journeys]** 但无法发布它们。

此产品用户档案包括以下权限：

|功能 |权限| |-|-| |历程| <ul><li>**[!DNL Manage journeys]**:读取、创建、编辑和删除历程。</li><li>**[!DNL View journeys events]**:对历程事件、历程自定义操作和历程数据源的只读访问。</li><li>**[!DNL View journeys report]**:阅读，编辑历程报告。</li></ul>|
|消息| <ul><li>**[!DNL Manage messages]**:读取、创建、编辑和删除消息。</li><li> **[!DNL Manage messages preview and test]**:读取、创建和编辑消息预览并发送测试/校样。</li><li>**[!DNL View messages report]**:读取、创建、编辑和删除消息报表。</li></ul>|
|决策管理| <ul><li>**[!DNL Manage decisions]**:读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**:读取、创建、编辑和删除自定义消息报表以及使用操作功能。</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**:读取、创建、编辑和删除区段。</li><li>**[!DNL Manage profiles]**:读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**:对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**:对架构的只读访问。</li><li>**[!DNL Manage merge policies]**:读取、创建、编辑和删除合并策略。</li></ul>|
|管理| <ul><li>**[!DNL View messages presets]**:对消息预设的只读访问权限。</li></ul>|

## [!DNL Journey viewer] {#journey-viewer}

的 **[!DNL Journey viewer]** 产品配置文件允许对 **[!UICONTROL Journeys]**, **[!UICONTROL Goals]**, **[!UICONTROL Messages]** 和 **[!UICONTROL Decision management]** 功能。

分配给此产品配置文件的用户将无法编辑或发布。

此产品用户档案包括以下权限：

|功能 |权限| |-|-| |历程| <ul><li>**[!DNL View journeys]**:对历程的只读访问权限。</li><li>**[!DNL View journeys event, data sources, actions]**:对历程事件和数据源的只读访问权限。</li><li>**[!DNL View journeys report]**:对历程报告的只读访问权限。</li></ul>|
|消息| <ul><li>**[!DNL View messages]**:对消息的只读访问权限。</li><li>**[!DNL View messages report]**:对消息报表的只读访问权限。</li></ul>|
|决策管理| <ul><li>**[!DNL View decisions]**:对决策实体的只读访问权限。</li></ul>|

## [!DNL Message Manager] {#message-manager}

的 **[!DNL Message Manager]** 产品配置文件允许用户创建和编辑 **[!UICONTROL Messages]** 和 **[!UICONTROL Decision management]** 但无法发布它们。

此产品用户档案包括以下权限：

|功能 |权限| |-|-| |历程| <ul><li>**[!DNL View journeys]**:对历程的只读访问权限。</li><li>**[!DNL View Journeys events, data sources and actions]**:对历程事件、历程自定义操作和历程数据源的只读访问。</li></ul>|
|消息| <ul><li>**[!DNL Manage messages]**:读取、创建、编辑和删除消息。</li><li>**[!DNL Manage messages preview and test]**:读取、创建和编辑消息预览并发送测试/校样。</li><li> **[!DNL View messages report]**:读取、创建、编辑和删除消息报表。</li></ul>|
|决策管理| <ul><li>**[!DNL Manage decisions]**:读取、创建、编辑和删除决策实体。</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Read profiles]**:对用于预览和测试的配置文件的只读访问权限。</li><li>**[!DNL Read datasets]**:对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**:对架构的只读访问。</li><li>**[!DNL Manage merge policies]**:读取、创建、编辑和删除合并策略。</li></ul>|
|管理| <ul><li>**[!DNL View messages presets]**:对消息预设的只读访问权限。</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

的 **[!DNL Decisioning manager]** 产品配置文件仅允许 **[!UICONTROL Decision management]** 菜单。 分配给此产品配置文件的用户将只能管理、查看和发布决策。

此产品用户档案包括以下权限：

|功能 |权限| |-|-| |决策管理| <ul><li>**[!DNL Manage decisions]**:读取、创建、编辑和删除决策实体。</li><li>**[!DNL View decisions]**:对决策实体的只读访问权限。</li><li>**[!DNL Manage ranking strategies]**:读取、创建、编辑和删除自定义消息报表以及使用操作功能。</li><li>**[!DNL Publish decisions]**:激活或停用决策活动。</li></ul>|
