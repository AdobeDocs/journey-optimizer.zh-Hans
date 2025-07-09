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
source-git-commit: e20db7c39e751bf720cd0ae75b4e8f031de18eef
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 7%

---

# 内置角色 {#ootb-product-profiles}

内置角色是一组统一的权限，允许用户访问界面中的特定功能或对象。 有关生成角色的可用权限列表，请参阅[此页面](ootb-permissions.md)。

## [!DNL Content Library Manager] {#content-library-manager}

**[!DNL Content Library Manager]**&#x200B;角色仅允许访问&#x200B;**[!UICONTROL 内容模板]**&#x200B;菜单。 分配给此角色的用户只能访问模板库以创建内容，而无法访问历程或营销活动。

此权限包括以下权限：

| 功能 | 权限 |
|-|-|
| Journey Optimizer Library | <ul><li>**[!DNL Manage library items]**：读取、创建、编辑和删除Journey Optimizer库项目，包括内容模板和片段。</li><li>**[!DNL Manage simulate content]**：访问预览和验证的&#x200B;**[!UICONTROL 模拟内容]**&#x200B;选项。</li><li>**[!DNL Publish Fragment]**：发布内容片段。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义报告并使用操作功能。</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li><li> **[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL View datasets]**：对数据集的只读访问权限。</li><li>**[!DNL View schemas]**：对架构的只读访问权限。</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

**[!DNL Decisioning manager]**&#x200B;角色仅允许访问&#x200B;**[!UICONTROL 决策管理]**&#x200B;菜单。 分配至此角色的用户将只能管理、查看和发布决策。

此权限包括以下权限：

| 功能 | 权限 |
|-|-|
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义报告并使用操作功能。</li><li>**[!DNL View decisions]**：对决策实体的只读访问权限。</li><li>**[!DNL Publish decisions]**：激活或停用决策活动。</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Campaign Administrator] {#campaign-administrator}

**[!DNL Campaign Administrator]**&#x200B;角色允许管理菜单管理和发布营销活动和决策管理。

此权限包括以下权限：

| 资源 | 权限 |
|-|-|
| 营销活动 | <ul><li> **[!DNL Manage campaigns]**：读取、创建、编辑和删除营销活动。</li><li>**[!DNL Publish campaigns]**：发布营销活动。</li><li>**[!DNL View campaigns report]**：读取并编辑营销活动报告。</li></ul> |
| 渠道配置 | <ul> <li>**[!DNL Export suppression list]**：访问将禁止列表导出为CSV文件的权限。</li> <li>**[!DNL Manage alerts]**：为营销活动、消息和权利启用/禁用警报。</li> <li>**[!DNL Manage IP pools]**：读取、创建、编辑和删除ip池。</li> <li>**[!DNL Manage landing page settings]**：读取、创建、编辑和删除登陆页面设置。</li> <li>**[!DNL Manage messages general settings]**：读取、创建、编辑和删除邮件常规设置。</li> <li>**[!DNL Manage messages presets]**：读取、创建、编辑和删除内容品牌。</li> <li>**[!DNL Manage PTR records]**：读取和编辑PTR记录。</li> <li>**[!DNL Manage SMS settings]**：读取、创建、编辑和删除短信设置。</li> <li>**[!DNL Manage subdomains delegation]**：读取、创建、编辑和删除子域委派。</li> <li>**[!DNL Manage suppression rules]**：访问读取、创建、编辑和删除禁止显示规则。</li> <li>**[!DNL View PTR records]**：对PTR记录的只读访问权限。</li> <li>**[!DNL View suppression list]**：读取和导出本地禁止显示列表。</li> </ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除排名策略。</li></ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li> <li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li> <li>**[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li> <li>**[!DNL View datasets]**：对数据集的只读访问权限。</li> <li>**[!DNL Read Identity namespace]**：对标识命名空间的只读访问权限。</li> <li>**[!DNL View schemas]**：对架构的只读访问权限。</li> <li>**[!DNL Sandbox]**：授予对沙盒的访问权限。</li> </ul> |

## [!DNL Campaign Approver] {#campaign-approver}

**[!DNL Campaign Approver]**&#x200B;角色允许用户批准投放并发布它们。 他们以后可以使用&#x200B;**[!DNL Campaigns]**&#x200B;报告检查其投放是否成功。

| 资源 | 权限 |
|-|-|
| 营销活动 | <ul><li>**[!DNL Manage campaigns]**：读取、创建、编辑和删除营销活动。</li><li>**[!DNL Publish campaigns]**：发布营销活动。</li><li>**[!DNL View campaigns report]**：读取、编辑营销活动报告。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义消息报告并使用操作功能。</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li><li>**[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li><li>**[!DNL View datasets]**：对数据集的只读访问权限。</li><li>**[!DNL View schemas]**：对架构的只读访问权限。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL View messages presets]**：对消息预设的只读访问权限。</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

**[!DNL Campaign Manager]**&#x200B;角色允许用户创建和编辑&#x200B;**[!UICONTROL 营销活动]**&#x200B;以及链接到&#x200B;**[!UICONTROL 营销活动]**&#x200B;的每个功能，但无法发布它们。

此权限包括以下权限：

| 资源 | 权限 |
|-|-|
| 营销活动 | <ul><li>**[!DNL Manage campaigns]**：读取、创建、编辑和删除营销活动。</li><li>**[!DNL View campaigns report]**：读取，编辑历程报告。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义消息报告并使用操作功能。</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li><li> **[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL View datasets]**：对数据集的只读访问权限。</li><li>**[!DNL View schemas]**：对架构的只读访问权限。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL View messages presets]**：对消息预设的只读访问权限。</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

**[!DNL Campaign Viewer]**&#x200B;角色允许对&#x200B;**[!UICONTROL 营销活动]**&#x200B;和&#x200B;**[!UICONTROL 决策管理]**&#x200B;功能的只读访问。

分配到此角色的用户将无法编辑或发布。

此权限包括以下权限：

| 资源 | 权限 |
|-|-|
| 营销活动 | <ul><li>**[!DNL View campaigns]**：对营销活动的只读访问权限。</li><li>**[!DNL View campaigns report]**：对营销活动报告的只读访问权限。</li></ul> |
| 决策管理 | <ul><li>**[!DNL View decisions]**：对决策实体的只读访问权限。</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

**[!DNL Journey Administrator]**&#x200B;角色允许管理菜单管理和发布历程和决策管理。

此权限包括以下权限：

| 资源 | 权限 |
|-|-|
| 历程 | <ul> <li>**[!DNL Manage journeys]**：读取、创建、编辑和删除历程。</li> <li>**[!DNL Manage journeys events, data sources and actions]**：读取、创建、编辑和删除事件、源或操作。</li> <li>**[!DNL Publish journeys]**：发布历程。</li> <li>**[!DNL View journeys report]**：读取并编辑历程报告。</li> </ul> |
| 渠道配置 | <ul> <li>**[!DNL Manage alerts]**：为历程和授权启用/禁用警报。</li> <li>**[!DNL Manage IP pools]**：读取、创建、编辑和删除ip池。</li> <li>**[!DNL Manage Landing page settings]**：创建、编辑和删除登陆页面子域和登陆页面预设。</li> <li>**[!DNL Manage messages general settings]**：读取、创建、编辑和删除邮件常规设置。</li> <li>**[!DNL Manage messages presets]**：读取、创建、编辑和删除内容品牌。</li> <li>**[!DNL Manage PTR records]**：读取和编辑PTR记录。</li> <li>**[!DNL Manage SMS settings]**：创建、编辑和删除启用SMS渠道所需的API凭据和SMS渠道配置。</li> <li>**[!DNL Manage subdomains delegation]**：读取、创建、编辑和删除子域委派。</li> <li>**[!DNL Manage suppression rules]**：访问读取、创建、编辑和删除禁止显示规则。</li> <li>**[!DNL View PTR records]**：对PTR记录的只读访问权限。</li> <li>**[!DNL View suppression list]**：读取和导出本地禁止显示列表。</li> </ul> |
| 决策管理 | <ul> <li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策。</li> <li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除排名策略。</li> </ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li> <li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li> <li>**[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li> <li>**[!DNL View datasets]**：对数据集的只读访问权限。</li> <li>**[!DNL Read Identity namespace]**：对标识命名空间的只读访问权限。</li> <li>**[!DNL View schemas]**：对架构的只读访问权限。</li> <li>**[!DNL Sandbox]**：授予对沙盒的访问权限。</li> </ul> |
| Journey Optimizer Library | <ul> <li>**[!DNL Manage Library Items]**：添加和删除[!DNL Journey Optimizer]库中保存的表达式。</li> </ul> |
| 数据治理 | <ul> <li>**[!DNL Manage data usage policies]**：读取、创建、编辑和删除数据使用策略。</li> <li>**[!DNL Manage usage label]**：读取、创建和删除使用标签。</li> <li>**[!DNL View data usage policies]**：对数据使用策略的只读访问权限。</li> <li>**[!DNL View user activity log]**：读取和导出审核日志。</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

**[!DNL Journey Approver]**&#x200B;角色允许用户批准投放并发布它们。 他们以后可以使用&#x200B;**[!DNL Journey]**&#x200B;报告检查其投放是否成功。

此权限包括以下权限：

| 资源 | 权限 |
|-|-|
| 历程 | <ul><li>**[!DNL Manage journeys]**：读取、创建、编辑和删除历程。</li><li>**[!DNL Publish journey]**：发布历程。</li><li>**[!DNL View journeys events, data sources and actions]**：对历程事件、历程自定义操作和历程数据源的只读访问权限。</li><li>**[!DNL View journeys report]**：读取，编辑历程报告。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义报告并使用操作功能。</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li><li>**[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL View datasets]**：对数据集的只读访问权限。</li><li>**[!DNL View schemas]**：对架构的只读访问权限。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL View channel configurations]**：对渠道配置的只读访问权限。</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

**[!DNL Journey Manager]**&#x200B;角色允许用户创建和编辑&#x200B;**[!UICONTROL 历程]**&#x200B;以及链接到&#x200B;**[!UICONTROL 历程]**&#x200B;的每个功能，但无法发布它们。

此权限包括以下权限：

| 资源 | 权限 |
|-|-|
| 历程 | <ul><li>**[!DNL Manage journeys]**：读取、创建、编辑和删除历程。</li><li>**[!DNL View journeys events]**：对历程事件、历程自定义操作和历程数据源的只读访问权限。</li><li>**[!DNL View journeys report]**：读取，编辑历程报告。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义报告并使用操作功能。</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li><li> **[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL View datasets]**：对数据集的只读访问权限。</li><li>**[!DNL View schemas]**：对架构的只读访问权限。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL View channel configurations]**：对渠道配置的只读访问权限。</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

**[!DNL Journey viewer]**&#x200B;角色允许对&#x200B;**[!UICONTROL 历程]**&#x200B;和&#x200B;**[!UICONTROL 决策管理]**&#x200B;功能的只读访问。

分配到此角色的用户将无法编辑或发布。

此权限包括以下权限：

| 资源 | 权限 |
|-|-|
| 历程 | <ul><li>**[!DNL View journeys]**：对历程的只读访问权限。</li><li>**[!DNL View journeys event, data sources, actions]**：对历程事件和数据源的只读访问权限。</li><li>**[!DNL View journeys report]**：对历程报告的只读访问权限。</li></ul> |
| 决策管理 | <ul><li>**[!DNL View decisions]**：对决策实体的只读访问权限。</li></ul> |

<!--
## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

The **[!DNL Orchestrated Campaign Administrator]** role allows the administration menus with the possibility to manage and publish Campaigns and Decision management. 

This permission includes the following permissions:

| Resources | Permissions|
|-|-|
|Campaigns| <ul><li> **[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete orchestrated campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish orchestrated campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read and edit orchestrated campaigns report.</li></ul>|
|Channel configurations|<ul><li>**[!DNL Export suppression list]**: access to export suppression list as a CSV file.</li> <li>**[!DNL Manage alerts]**: enable/disable alerts for campaigns, messages and entitlements.</li> <li>**[!DNL Manage custom dashboards]**: XX.</li><li>**[!DNL Manage IP pools]**: read, create, edit, and delete ip pool.</li> <li>**[!DNL Manage landing page settings]**: read, create, edit, and delete landing page settings.</li> <li>**[!DNL Manage messages general settings]**: read, create, edit, and delete message general settings.</li> <li>**[!DNL Manage messages presets]**: read, create, edit, and delete content branding.</li> <li>**[!DNL Manage orchestrated campaign administrator]**: XX.</li><li>**[!DNL Manage PTR records]**: read and edit PTR records.</li> <li>**[!DNL Manage SMS settings]**: read, create, edit, and delete SMS settings.</li> <li>**[!DNL Manage subdomains delegation]**: read, create, edit, and delete subdomain delegation.</li> <li>**[!DNL Manage suppression rules]**: access read, create, edit and delete suppression rules.</li> <li>**[!DNL View PTR records]**: read-only access to PTR records.</li> <li>**[!DNL View suppression list]**: read and export local suppression list.</li> </ul>|
|Decision management|<ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisions.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete ranking strategies.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL Read Identity namespace]**: read-only access to identity namespace.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL Sandbox]**: grant access to sandboxes.</li> </ul>|

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

The **[!DNL Orchestrated Campaign Approver]** role allows users to approve deliveries and publish them. They can later check the success of their deliveries with the **[!DNL Campaigns]** reports. 

| Resources | Permissions|
|-|-|
|Campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read, edit orchestrated campaign reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations|<ul><li>**[!DNL View orchestrated campaigns admin]**: XX.</li> <li>**[!DNL View messages presets]**: read-only access to messages presets.</li> <li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li></ul>|

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

The **[!DNL Orchestrated Campaign Manager]** role allows users to create and edit **[!UICONTROL Campaigns]** and every capability linked to **[!UICONTROL Campaigns]** but will not be able to publish them.

This permission includes the following permissions:

| Resources | Permissions|
|-|-|
|Campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read, edit journey report.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li><li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li><li> **[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li><li>**[!DNL View datasets]**: read-only access to datasets.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li><li>**[!DNL View orchestrated campaigns admin]**: XX.</li><li>**[!DNL View schemas]**: read-only access to schemas.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View messages presets]**: read-only access to messages presets.</li></ul>|

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

The **[!DNL Campaign Viewer]** role allows read-only access to the **[!UICONTROL Campaigns]** and **[!UICONTROL Decision management]** capabilities. 

Users assigned to this role will not be able to edit or publish. 

This permission includes the following permissions:

| Resources | Permissions|
|-|-|
|Campaigns| <ul><li>**[!DNL View orchestrated campaigns]**: read-only access to campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read-only access to campaigns reports.</li></ul>|
|Decision management| <ul><li>**[!DNL View decisions]**: read-only access to decisions entities.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View orchestrated campaigns admin]**: XX.</li></ul>|

-->