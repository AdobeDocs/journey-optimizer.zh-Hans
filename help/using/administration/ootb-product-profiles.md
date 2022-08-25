---
title: 内置产品配置文件
description: 了解内置的产品配置文件
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 9%

---

# 内置产品配置文件 {#ootb-product-profiles}

Adobe Journey Optimizer将发布内联创作新功能，该功能允许您直接从历程创建和创作消息。 有关此新功能的更多信息，请参阅此页面。

>[!WARNING]
>
>如果您的用户已分配到 **[!DNL Message Manager]** 仅限产品配置文件，不包含 **[!DNL Journey manager]** 产品配置文件中，您需要为他们分配新的产品配置文件，以便能够继续编辑内容。

此功能将影响以下权限：

| 权限名称 | 将包含在 |
|:-:|:-:|
| **[!DNL View Messages]** | **[!DNL View Journeys]** |
| **[!DNL View Message reports]** | **[!DNL View Journeys Report]** |
| **[!DNL Manage Messages]** | **[!DNL Manage Journey]** |
| **[!DNL Publish Messages]** | **[!DNL Publish Journeys]** |
| **[!DNL Manage Messages Preview and Test]** | **[!DNL Manage Journeys]** |

**7月25日之后**，与消息相关的权限将仍然可用，因为仍然可以访问消息以启用过渡，并且您仍可以将它们另存为模板。

**截至9月6日**，与消息相关的权限将被删除，消息将不再可访问。

## [!DNL Campaign Administrator] {#campaign-administrator}

的 **[!DNL Campaign Administrator]** 产品配置文件允许管理菜单，其中可以管理和发布营销活动和决策管理。

此产品用户档案包括以下权限：

|功能 |权限| |-|-| |促销活动| <ul><li> **[!DNL Manage campaigns]**:读取、创建、编辑和删除营销活动。</li><li>**[!DNL Publish campaigns]**:发布营销活动。</li><li>**[!DNL View campaigns report]**:阅读和编辑营销活动报表。</li></ul>|
|管理|<ul><li>**[!DNL Manage subdomains delegation]**:读取、创建、编辑和删除子域委派。</li><li>**[!DNL Manage IP pools]**:读取、创建、编辑和删除ip池。</li><li>**[!DNL Manage PTR records]**:读取和编辑PTR记录。</li><li>**[!DNL View PTR records]**:对PTR记录的只读访问。</li><li> **[!DNL Manage messages general settings]**:读取、创建、编辑和删除消息常规设置。</li><li>**[!DNL Manage messages presets]**:读取、创建、编辑和删除内容品牌。</li><li>**[!DNL Manage suppression rules]**:访问读取、创建、编辑和删除隐藏规则。</li><li>**[!DNL Export suppression list]**:有权将禁止列表导出为CSV文件。</li><li>**[!DNL View suppression list]**:读取和导出本地抑制列表。</li><li>**[!DNL Manage alerts]**:启用/禁用营销活动、消息和授权的警报。</li><li>**[!DNL Manage landing page settings]**:读取、创建、编辑和删除登陆页面设置。</li><li>**[!DNL Manage SMS settings]**:读取、创建、编辑和删除短信设置。</li></ul>|
|决策管理|<ul><li>**[!DNL Manage decisions]**:读取、创建、编辑和删除决策。</li><li>**[!DNL Manage ranking strategies]**:读取、创建、编辑和删除排名策略。</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**:授予对沙箱的访问权限。</li><li>**[!DNL Manage segments]**:读取、创建、编辑和删除区段。</li><li>**[!DNL Manage profiles]**:读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**:对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**:对架构的只读访问。</li><li>**[!DNL Read Identity namespace]**:对身份命名空间的只读访问权限。</li><li>**[!DNL Manage merge policies]**:读取、创建、编辑和删除合并策略。</li></ul>|

## [!DNL Campaign Approver] {#campaign-approver}

的 **[!DNL Campaign Approver]** 产品用户档案允许用户批准投放并发布它们。 他们稍后可以使用 **[!DNL Campaigns]** 报表。

|功能 |权限| |-|-| |促销活动| <ul><li>**[!DNL Manage campaigns]**:读取、创建、编辑和删除营销活动。</li><li>**[!DNL Publish campaigns]**:发布营销活动。</li><li>**[!DNL View Campaigns report]**:阅读、编辑历程报告。</li></ul>|
|决策管理| <ul><li>**[!DNL Manage decisions]**:读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**:读取、创建、编辑和删除自定义消息报表以及使用操作功能。</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**:读取、创建、编辑和删除区段。</li><li>**[!DNL Manage profiles]**:读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**:对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**:对架构的只读访问。</li><li>**[!DNL Manage merge policies]**:读取、创建、编辑和删除合并策略。</li></ul>|
|管理| <ul><li>**[!DNL View messages presets]**:对消息预设的只读访问权限。</li></ul>|

## [!DNL Campaign Manager] {#campaign-manager}

的 **[!DNL Campaign Manager]** 产品配置文件允许用户创建和编辑 **[!UICONTROL Campaigns]** 和链接到 **[!UICONTROL Campaigns]** 但无法发布它们。

此产品用户档案包括以下权限：

|功能 |权限| |-|-| |促销活动| <ul><li>**[!DNL Manage campaigns]**:读取、创建、编辑和删除营销活动。</li><li>**[!DNL View campaigns report]**:阅读，编辑历程报告。</li></ul>|
|决策管理| <ul><li>**[!DNL Manage decisions]**:读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**:读取、创建、编辑和删除自定义消息报表以及使用操作功能。</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**:读取、创建、编辑和删除区段。</li><li>**[!DNL Manage profiles]**:读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**:对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**:对架构的只读访问。</li><li>**[!DNL Manage merge policies]**:读取、创建、编辑和删除合并策略。</li></ul>|
|管理| <ul><li>**[!DNL View messages presets]**:对消息预设的只读访问权限。</li></ul>|

## [!DNL Campaign viewer] {#campaign-viewer}

的 **[!DNL Campaign viewer]** 产品配置文件允许对 **[!UICONTROL Campaigns]** 和 **[!UICONTROL Decision management]** 功能。

分配给此产品配置文件的用户将无法编辑或发布。

此产品用户档案包括以下权限：

|功能 |权限| |-|-| |促销活动| <ul><li>**[!DNL View campaigns]**:对营销活动的只读访问权限。</li><li>**[!DNL View campaigns report]**:对营销活动报表的只读访问权限。</li></ul>|
|决策管理| <ul><li>**[!DNL View decisions]**:对决策实体的只读访问权限。</li></ul>|

## [!DNL Journey Administrator] {#journey-administrator}

的 **[!DNL Journey Administrator]** 产品配置文件允许管理菜单，其中可以管理和发布历程和决策管理。

此产品用户档案包括以下权限：

|功能 |权限| |-|-| |历程| <ul><li> **[!DNL Manage journeys]**:读取、创建、编辑和删除历程。</li><li>**[!DNL Publish journeys]**:发布历程。</li><li>**[!DNL Manage journeys events, data sources and actions]**:读取、创建、编辑和删除事件、源或操作。</li><li>**[!DNL View journeys report]**:阅读和编辑历程报告。</li></ul>|
|管理|<ul><li>**[!DNL Manage subdomains delegation]**:读取、创建、编辑和删除子域委派。</li><li>**[!DNL Manage IP pools]**:读取、创建、编辑和删除ip池。</li><li>**[!DNL Manage PTR records]**:读取和编辑PTR记录。</li><li>**[!DNL View PTR records]**:对PTR记录的只读访问。</li><li>**[!DNL Manage channel surfaces]**:读取、创建、编辑和删除内容品牌。</li><li>**[!DNL Manage Landing page settings]**:创建、编辑和删除登陆页面子域和登陆页面预设。</li><li> **[!DNL Manage messages general settings]**:读取、创建、编辑和删除消息常规设置。</li><li>**[!DNL Manage SMS settings]**:创建、编辑和删除启用短信渠道所需的API凭据和短信渠道表面。</li><li>**[!DNL Manage suppression rules]**:访问读取、创建、编辑和删除隐藏规则。</li><li>**[!DNL View suppression list]**:读取和导出本地抑制列表。</li><li>**[!DNL Manage alerts]**:启用/禁用历程和授权警报。</li></ul>|
|决策管理|<ul><li>**[!DNL Manage decisions]**:读取、创建、编辑和删除决策。</li><li>**[!DNL Manage ranking strategies]**:读取、创建、编辑和删除排名策略。</li></ul>| |Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**:授予对沙箱的访问权限。</li><li>**[!DNL Manage segments]**:读取、创建、编辑和删除区段。</li><li>**[!DNL Manage profiles]**:读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**:对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**:对架构的只读访问。</li><li>**[!DNL Read Identity namespace]**:对身份命名空间的只读访问权限。</li><li>**[!DNL Manage merge policies]**:读取、创建、编辑和删除合并策略。</li></ul>| |Journey Optimizer库|<ul><li>**[!DNL Manage Library Items]**:添加和删除 [!DNL Journey Optimizer] 库。</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

的 **[!DNL Journey Approver]** 产品用户档案允许用户批准投放并发布它们。 他们稍后可以使用 **[!DNL Journey]** 报表。

此产品用户档案包括以下权限：

|功能 |权限| |-|-| |历程| <ul><li>**[!DNL Manage journeys]**:读取、创建、编辑和删除历程。</li><li>**[!DNL Publish journey]**:发布历程。</li><li>**[!DNL View journeys events, data sources and actions]**:对历程事件、历程自定义操作和历程数据源的只读访问。</li><li>**[!DNL View journeys report]**:阅读、编辑历程报告。</li></ul>|
|决策管理| <ul><li>**[!DNL Manage decisions]**:读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**:读取、创建、编辑和删除自定义报表以及使用操作功能。</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**:读取、创建、编辑和删除区段。</li><li>**[!DNL Manage profiles]**:读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**:对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**:对架构的只读访问。</li><li>**[!DNL Manage merge policies]**:读取、创建、编辑和删除合并策略。</li></ul>|
|管理| <ul><li>**[!DNL View channel surfaces]**:对通道曲面的只读访问。</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

的 **[!DNL Journey Manager]** 产品配置文件允许用户创建和编辑 **[!UICONTROL Journeys]** 和链接到 **[!UICONTROL Journeys]** 但无法发布它们。

此产品用户档案包括以下权限：

|功能 |权限| |-|-| |历程| <ul><li>**[!DNL Manage journeys]**:读取、创建、编辑和删除历程。</li><li>**[!DNL View journeys events]**:对历程事件、历程自定义操作和历程数据源的只读访问。</li><li>**[!DNL View journeys report]**:阅读，编辑历程报告。</li></ul>|
|决策管理| <ul><li>**[!DNL Manage decisions]**:读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**:读取、创建、编辑和删除自定义报表以及使用操作功能。</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**:读取、创建、编辑和删除区段。</li><li>**[!DNL Manage profiles]**:读取、创建、编辑和删除用户档案。</li><li>**[!DNL Read datasets]**:对数据集的只读访问权限。</li><li>**[!DNL Read schemas]**:对架构的只读访问。</li><li>**[!DNL Manage merge policies]**:读取、创建、编辑和删除合并策略。</li></ul>|
|管理| <ul><li>**[!DNL View channel surfaces]**:对通道曲面的只读访问。</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

的 **[!DNL Journey viewer]** 产品配置文件允许对 **[!UICONTROL Journeys]** 和 **[!UICONTROL Decision management]** 功能。

分配给此产品配置文件的用户将无法编辑或发布。

此产品用户档案包括以下权限：

|功能 |权限| |-|-| |历程| <ul><li>**[!DNL View journeys]**:对历程的只读访问权限。</li><li>**[!DNL View journeys event, data sources, actions]**:对历程事件和数据源的只读访问权限。</li><li>**[!DNL View journeys report]**:对历程报告的只读访问权限。</li></ul>|
|决策管理| <ul><li>**[!DNL View decisions]**:对决策实体的只读访问权限。</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

的 **[!DNL Decisioning manager]** 产品配置文件仅允许 **[!UICONTROL Decision management]** 菜单。 分配给此产品配置文件的用户将只能管理、查看和发布决策。

此产品用户档案包括以下权限：

|功能 |权限| |-|-| |决策管理| <ul><li>**[!DNL Manage decisions]**:读取、创建、编辑和删除决策实体。</li><li>**[!DNL View decisions]**:对决策实体的只读访问权限。</li><li>**[!DNL Manage ranking strategies]**:读取、创建、编辑和删除自定义报表以及使用操作功能。</li><li>**[!DNL Publish decisions]**:激活或停用决策活动。</li></ul>|
