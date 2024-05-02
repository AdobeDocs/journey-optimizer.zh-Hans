---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer内置角色
description: 了解内置角色
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: 权限、创作、消息
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '1172'
ht-degree: 6%

---

# 内置角色 {#ootb-product-profiles}

内置角色是一组统一的权限，允许用户访问界面中的特定功能或对象。 请参阅 [此页面](ootb-permissions.md) 以获取构建角色的可用权限列表。

## [!DNL Campaign Administrator] {#campaign-administrator}

此 **[!DNL Campaign Administrator]** 角色允许管理菜单管理和发布营销活动和决策管理。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| 营销活动 | <ul><li> **[!DNL Manage campaigns]**：读取、创建、编辑和删除营销活动。</li><li>**[!DNL Publish campaigns]**：发布营销活动。</li><li>**[!DNL View campaigns report]**：读取和编辑营销活动报告。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL Manage subdomains delegation]**：读取、创建、编辑和删除子域委派。</li><li>**[!DNL Manage IP pools]**：读取、创建、编辑和删除ip池。</li><li>**[!DNL Manage PTR records]**：读取和编辑PTR记录。</li><li>**[!DNL View PTR records]**：对PTR记录的只读访问权限。</li><li> **[!DNL Manage messages general settings]**：读取、创建、编辑和删除消息常规设置。</li><li>**[!DNL Manage messages presets]**：读取、创建、编辑和删除内容品牌策略。</li><li>**[!DNL Manage suppression rules]**：访问读取、创建、编辑和删除禁止显示规则。</li><li>**[!DNL Export suppression list]**：访问将禁止列表导出为CSV文件。</li><li>**[!DNL View suppression list]**：读取和导出本地禁止显示列表。</li><li>**[!DNL Manage alerts]**：为营销活动、消息和权利启用/禁用警报。</li><li>**[!DNL Manage landing page settings]**：读取、创建、编辑和删除登陆页面设置。</li><li>**[!DNL Manage SMS settings]**：读取、创建、编辑和删除短信设置。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除排名策略。</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**：授予对沙盒的访问权限。</li><li>**[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**：对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**：对架构的只读访问权限。</li><li>**[!DNL Read Identity namespace]**：对身份命名空间的只读访问。</li><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

此 **[!DNL Campaign Approver]** 角色允许用户批准投放并发布它们。 然后，他们可以使用检查其投放是否成功 **[!DNL Campaigns]** 报表。

| 资源 | 权限 |
|-|-|
| 营销活动 | <ul><li>**[!DNL Manage campaigns]**：读取、创建、编辑和删除营销活动。</li><li>**[!DNL Publish campaigns]**：发布营销活动。</li><li>**[!DNL View Campaigns report]**：读取，编辑历程报告。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义消息报表并使用操作功能。</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**：对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**：对架构的只读访问权限。</li><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL View messages presets]**：对消息预设的只读访问权限。</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

此 **[!DNL Campaign Manager]** 角色允许用户创建和编辑 **[!UICONTROL 营销活动]** 以及链接到的每个功能 **[!UICONTROL 营销活动]** 但是无法发布它们。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| 营销活动 | <ul><li>**[!DNL Manage campaigns]**：读取、创建、编辑和删除营销活动。</li><li>**[!DNL View campaigns report]**：读取，编辑历程报告。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义消息报表并使用操作功能。</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**：对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**：对架构的只读访问权限。</li><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL View messages presets]**：对消息预设的只读访问权限。</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

此 **[!DNL Campaign Viewer]** 角色允许对进行只读访问 **[!UICONTROL 营销活动]** 和 **[!UICONTROL 决策管理]** 功能。

分配到此角色的用户将无法编辑或发布。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| 营销活动 | <ul><li>**[!DNL View campaigns]**：对营销活动的只读访问权限。</li><li>**[!DNL View campaigns report]**：对营销活动报表的只读访问权限。</li></ul> |
| 决策管理 | <ul><li>**[!DNL View decisions]**：对决策实体的只读访问权限。</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

此 **[!DNL Journey Administrator]** 角色允许管理菜单，并可以管理和发布历程和决策管理。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| 历程 | <ul><li> **[!DNL Manage journeys]**：读取、创建、编辑和删除历程。</li><li>**[!DNL Publish journeys]**：发布历程。</li><li>**[!DNL Manage journeys events, data sources and actions]**：读取、创建、编辑和删除事件、源或操作。</li><li>**[!DNL View journeys report]**：读取和编辑历程报告。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL Manage subdomains delegation]**：读取、创建、编辑和删除子域委派。</li><li>**[!DNL Manage IP pools]**：读取、创建、编辑和删除ip池。</li><li>**[!DNL Manage PTR records]**：读取和编辑PTR记录。</li><li>**[!DNL View PTR records]**：对PTR记录的只读访问权限。</li><li>**[!DNL Manage messages presets]**：读取、创建、编辑和删除内容品牌策略。</li><li>**[!DNL Manage Landing page settings]**：创建、编辑和删除登陆页面子域和登陆页面预设。</li><li> **[!DNL Manage messages general settings]**：读取、创建、编辑和删除消息常规设置。</li><li>**[!DNL Manage SMS settings]**：创建、编辑和删除启用SMS渠道所需的API凭据和SMS渠道表面。</li><li>**[!DNL Manage suppression rules]**：访问读取、创建、编辑和删除禁止显示规则。</li><li>**[!DNL View suppression list]**：读取和导出本地禁止显示列表。</li><li>**[!DNL Manage alerts]**：启用/禁用历程和授权警报。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除排名策略。</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**：授予对沙盒的访问权限。</li><li>**[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**：对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**：对架构的只读访问权限。</li><li>**[!DNL Read Identity namespace]**：对身份命名空间的只读访问。</li><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li></ul> |
| Journey Optimizer Library | <ul><li>**[!DNL Manage Library Items]**：添加和删除中保存的表达式 [!DNL Journey Optimizer] 库。</li></ul> |
| 数据治理 | <ul><li>**[!DNL Manage usage label]**：读取、创建和删除使用标签。</li><li>**[!DNL Manage data usage policies]**：读取、创建、编辑和删除数据使用策略。</li><li>**[!DNL View data usage policies]**：对数据使用策略的只读访问权限。</li><li>**[!DNL View user activity log]**：读取和导出审核日志。</li></ul> |

## [!DNL Journey Approver] {#journey-approver}

此 **[!DNL Journey Approver]** 角色允许用户批准投放并发布它们。 然后，他们可以使用检查其投放是否成功 **[!DNL Journey]** 报表。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| 历程 | <ul><li>**[!DNL Manage journeys]**：读取、创建、编辑和删除历程。</li><li>**[!DNL Publish journey]**：发布历程。</li><li>**[!DNL View journeys events, data sources and actions]**：对历程事件、历程自定义操作和历程数据源的只读访问权限。</li><li>**[!DNL View journeys report]**：读取，编辑历程报告。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义报表并使用操作功能。</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**：对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**：对架构的只读访问权限。</li><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL View channel surfaces]**：对渠道表面的只读访问权限。</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

此 **[!DNL Journey Manager]** 角色允许用户创建和编辑 **[!UICONTROL 历程]** 以及链接到的每个功能 **[!UICONTROL 历程]** 但是无法发布它们。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| 历程 | <ul><li>**[!DNL Manage journeys]**：读取、创建、编辑和删除历程。</li><li>**[!DNL View journeys events]**：对历程事件、历程自定义操作和历程数据源的只读访问权限。</li><li>**[!DNL View journeys report]**：读取，编辑历程报告。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义报表并使用操作功能。</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**：对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**：对架构的只读访问权限。</li><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL View channel surfaces]**：对渠道表面的只读访问权限。</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

此 **[!DNL Journey viewer]** 角色允许对进行只读访问 **[!UICONTROL 历程]** 和 **[!UICONTROL 决策管理]** 功能。

分配到此角色的用户将无法编辑或发布。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| 历程 | <ul><li>**[!DNL View journeys]**：对历程的只读访问权限。</li><li>**[!DNL View journeys event, data sources, actions]**：对历程事件和数据源的只读访问权限。</li><li>**[!DNL View journeys report]**：对历程报告的只读访问权限。</li></ul> |
| 决策管理 | <ul><li>**[!DNL View decisions]**：对决策实体的只读访问权限。</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

此 **[!DNL Decisioning manager]** 角色仅允许访问 **[!UICONTROL 决策管理]** 菜单。 分配至此角色的用户将只能管理、查看和发布决策。

此角色包括以下权限：

| 功能 | 权限 |
|-|-|
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL View decisions]**：对决策实体的只读访问权限。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义报表并使用操作功能。</li><li>**[!DNL Publish decisions]**：激活或取消激活决策活动。</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Experience decisioning entities.</li--></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

此 **[!DNL Content Library Manager]** 角色仅允许访问 **[!UICONTROL 内容模板]** 菜单。 分配给此角色的用户只能访问模板库以创建内容，而无法访问历程或营销活动。

此角色包括以下权限：

| 功能 | 权限 |
|-|-|
| Journey Optimizer Library | <ul><li>**[!DNL Manage library items]**：读取、创建、编辑和删除Journey Optimizer库项目，包括内容模板和片段。</li><li>**[!DNL Manage simulate content]**：访问 **[!UICONTROL 模拟内容]** 预览和验证选项。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义报表并使用操作功能。</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**：对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**：对架构的只读访问权限。</li><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li></ul> |