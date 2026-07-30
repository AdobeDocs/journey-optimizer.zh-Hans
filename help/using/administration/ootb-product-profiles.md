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
TQID: https://experienceleague.adobe.com/LkOCFOSH-AzwWMoteNN-XI3R2yYkO5iBrVwMtobd4iI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
subfeature_v2: []
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: e1e0219c-f879-479f-8427-888ed2a6e9c2id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: c46ce04b47a3576e6373cbe788f2bbccf6ddbed0
workflow-type: tm+mt
source-wordcount: 2684
ht-degree: 5%

---

# 内置角色 {#ootb-product-profiles}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;浏览内置角色及其包含的权限，以便快速授予用户与其职责相匹配的现成级别访问权限。

>[!ENDSHADEBOX]

内置角色是一组统一的权限，允许用户访问界面中的特定功能或对象。 有关生成角色的可用权限列表，请参阅[此页面](ootb-permissions.md)。


## [!DNL Campaign Administrator] {#campaign-administrator}

**[!DNL Campaign Administrator]**&#x200B;角色允许管理菜单管理和发布营销活动和决策管理。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li> <li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li> <li>**[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li> <li>**[!DNL View datasets]**：对数据集的只读访问权限。</li> <li>**[!DNL Read Identity namespace]**：对标识命名空间的只读访问权限。</li> <li>**[!DNL View schemas]**：对架构的只读访问权限。</li> <li>**[!DNL Sandbox]**：授予对沙盒的访问权限。</li> </ul> |
| 营销活动 | <ul><li> **[!DNL Manage campaigns]**：读取、创建、编辑和删除营销活动。</li><li>**[!DNL Publish campaigns]**：发布营销活动。</li><li>**[!DNL View campaigns report]**：读取并编辑营销活动报告。</li></ul> |
| 渠道配置 | <ul> <li>**[!DNL Export suppression list]**：访问将禁止列表导出为CSV文件的权限。</li> <li>**[!DNL Manage alerts]**：为营销活动、消息和权利启用/禁用警报。</li> <li>**[!DNL Manage IP pools]**：读取、创建、编辑和删除ip池。</li> <li>**[!DNL Manage landing page settings]**：读取、创建、编辑和删除登陆页面设置。</li> <li>**[!DNL Manage messages general settings]**：读取、创建、编辑和删除邮件常规设置。</li> <li>**[!DNL Manage messages presets]**：读取、创建、编辑和删除内容品牌。</li> <li>**[!DNL Manage PTR records]**：读取和编辑PTR记录。</li> <li>**[!DNL Manage SMS settings]**：读取、创建、编辑和删除短信设置。</li> <li>**[!DNL Manage subdomains delegation]**：读取、创建、编辑和删除子域委派。</li> <li>**[!DNL Manage suppression rules]**：访问读取、创建、编辑和删除禁止显示规则。</li> <li>**[!DNL View PTR records]**：对PTR记录的只读访问权限。</li> <li>**[!DNL View suppression list]**：读取和导出本地禁止显示列表。</li> </ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除排名策略。</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

**[!DNL Campaign Approver]**&#x200B;角色允许用户批准投放并发布它们。 他们以后可以使用&#x200B;**[!DNL Campaigns]**&#x200B;报告检查其投放是否成功。

| 资源 | 权限 |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li><li>**[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li><li>**[!DNL View datasets]**：对数据集的只读访问权限。</li><li>**[!DNL View schemas]**：对架构的只读访问权限。</li></ul> |
| 营销活动 | <ul><li>**[!DNL Manage campaigns]**：读取、创建、编辑和删除营销活动。</li><li>**[!DNL Publish campaigns]**：发布营销活动。</li><li>**[!DNL View campaigns report]**：读取、编辑营销活动报告。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL View messages presets]**：对消息预设的只读访问权限。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义消息报告并使用操作功能。</li></ul> |


## [!DNL Campaign Manager] {#campaign-manager}

**[!DNL Campaign Manager]**&#x200B;角色允许用户创建和编辑&#x200B;**[!UICONTROL 营销活动]**&#x200B;以及链接到&#x200B;**[!UICONTROL 营销活动]**&#x200B;的每个功能，但无法发布它们。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li><li> **[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL View datasets]**：对数据集的只读访问权限。</li><li>**[!DNL View schemas]**：对架构的只读访问权限。</li></ul> |
| 营销活动 | <ul><li>**[!DNL Manage campaigns]**：读取、创建、编辑和删除营销活动。</li><li>**[!DNL View campaigns report]**：读取，编辑历程报告。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL View messages presets]**：对消息预设的只读访问权限。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义消息报告并使用操作功能。</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

**[!DNL Campaign Viewer]**&#x200B;角色允许对&#x200B;**[!UICONTROL 营销活动]**&#x200B;和&#x200B;**[!UICONTROL 决策管理]**&#x200B;功能的只读访问。

分配到此角色的用户将无法编辑或发布。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| 营销活动 | <ul><li>**[!DNL View campaigns]**：对营销活动的只读访问权限。</li><li>**[!DNL View campaigns report]**：对营销活动报告的只读访问权限。</li></ul> |
| 决策管理 | <ul><li>**[!DNL View decisions]**：对决策实体的只读访问权限。</li></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

**[!DNL Content Library Manager]**&#x200B;角色仅允许访问&#x200B;**[!UICONTROL 内容模板]**&#x200B;菜单。 分配给此角色的用户只能访问模板库以创建内容，而无法访问历程或营销活动。

此权限包括以下权限：

| 功能 | 权限 |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li><li> **[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL View datasets]**：对数据集的只读访问权限。</li><li>**[!DNL View schemas]**：对架构的只读访问权限。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义报告并使用操作功能。</li></ul> |
| Journey Optimizer Library | <ul><li>**[!DNL Manage library items]**：读取、创建、编辑和删除Journey Optimizer库项目，包括内容模板和片段。</li><li>**[!DNL Manage simulate content]**：访问预览和验证的&#x200B;**[!UICONTROL 模拟内容]**&#x200B;选项。</li><li>**[!DNL Publish Fragment]**：发布内容片段。</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

**[!DNL Decisioning manager]**&#x200B;角色仅允许访问&#x200B;**[!UICONTROL 决策管理]**&#x200B;菜单。 分配至此角色的用户将只能管理、查看和发布决策。

此权限包括以下权限：

| 功能 | 权限 |
|-|-|
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义报告并使用操作功能。</li><li>**[!DNL View decisions]**：对决策实体的只读访问权限。</li><li>**[!DNL Publish decisions]**：激活或停用决策活动。</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

**[!DNL Journey Administrator]**&#x200B;角色允许管理菜单管理和发布历程和决策管理。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li> <li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li> <li>**[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li> <li>**[!DNL View datasets]**：对数据集的只读访问权限。</li> <li>**[!DNL Read Identity namespace]**：对标识命名空间的只读访问权限。</li> <li>**[!DNL View schemas]**：对架构的只读访问权限。</li> <li>**[!DNL Sandbox]**：授予对沙盒的访问权限。</li> </ul> |
| 渠道配置 | <ul> <li>**[!DNL Manage alerts]**：为历程和授权启用/禁用警报。</li> <li>**[!DNL Manage IP pools]**：读取、创建、编辑和删除ip池。</li> <li>**[!DNL Manage Landing page settings]**：创建、编辑和删除登陆页面子域和登陆页面预设。</li> <li>**[!DNL Manage messages general settings]**：读取、创建、编辑和删除邮件常规设置。</li> <li>**[!DNL Manage messages presets]**：读取、创建、编辑和删除内容品牌。</li> <li>**[!DNL Manage PTR records]**：读取和编辑PTR记录。</li> <li>**[!DNL Manage SMS settings]**：创建、编辑和删除启用SMS渠道所需的API凭据和SMS渠道配置。</li> <li>**[!DNL Manage subdomains delegation]**：读取、创建、编辑和删除子域委派。</li> <li>**[!DNL Manage suppression rules]**：访问读取、创建、编辑和删除禁止显示规则。</li> <li>**[!DNL View PTR records]**：对PTR记录的只读访问权限。</li> <li>**[!DNL View suppression list]**：读取和导出本地禁止显示列表。</li> </ul> |
| 数据治理 | <ul> <li>**[!DNL Manage data usage policies]**：读取、创建、编辑和删除数据使用策略。</li> <li>**[!DNL Manage usage label]**：读取、创建和删除使用标签。</li> <li>**[!DNL View data usage policies]**：对数据使用策略的只读访问权限。</li> <li>**[!DNL View user activity log]**：只读访问权限，可查看Experience Platform活动记录的审核日志。</li> </ul> |
| 决策管理 | <ul> <li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策。</li> <li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除排名策略。</li> </ul> |
| 历程 | <ul> <li>**[!DNL Manage journeys]**：读取、创建、编辑、停止（实时、测试模式和试运行）和删除历程。 </li> <li>**[!DNL Manage journeys events, data sources and actions]**：读取、创建、编辑和删除事件、源或操作。</li> <li>**[!DNL Publish journeys]**：发布、启动测试模式、开始试运行、暂停和恢复历程。 </li> <li>**[!DNL View journeys report]**：读取并编辑历程报告。</li> </ul> |
| Journey Optimizer Library | <ul> <li>**[!DNL Manage Library Items]**：添加和删除[!DNL Journey Optimizer]库中保存的表达式。</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

**[!DNL Journey Approver]**&#x200B;角色允许用户批准投放并发布它们。 他们以后可以使用&#x200B;**[!DNL Journey]**&#x200B;报告检查其投放是否成功。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li><li>**[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL View datasets]**：对数据集的只读访问权限。</li><li>**[!DNL View schemas]**：对架构的只读访问权限。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL View channel configurations]**：对渠道配置的只读访问权限。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义报告并使用操作功能。</li></ul> |
| 历程 | <ul><li>**[!DNL Manage journeys]**：读取、创建、编辑、停止（实时、测试模式和试运行）和删除历程。 </li><li>**[!DNL Publish journey]**：发布、启动测试模式、开始试运行、暂停和恢复历程。 </li><li>**[!DNL View journeys events, data sources and actions]**：对历程事件、历程自定义操作和历程数据源的只读访问权限。</li><li>**[!DNL View journeys report]**：读取，编辑历程报告。</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

**[!DNL Journey Manager]**&#x200B;角色允许用户创建和编辑&#x200B;**[!UICONTROL 历程]**&#x200B;以及链接到&#x200B;**[!UICONTROL 历程]**&#x200B;的每个功能，但无法发布它们。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li><li> **[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL View datasets]**：对数据集的只读访问权限。</li><li>**[!DNL View schemas]**：对架构的只读访问权限。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL View channel configurations]**：对渠道配置的只读访问权限。</li></ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义报告并使用操作功能。</li></ul> |
| 历程 | <ul><li>**[!DNL Manage journeys]**：读取、创建、编辑、停止（实时、测试模式和试运行）和删除历程。</li><li>**[!DNL View journeys events]**：对历程事件、历程自定义操作和历程数据源的只读访问权限。</li><li>**[!DNL View journeys report]**：读取，编辑历程报告。</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

**[!DNL Journey viewer]**&#x200B;角色允许对&#x200B;**[!UICONTROL 历程]**&#x200B;和&#x200B;**[!UICONTROL 决策管理]**&#x200B;功能的只读访问。

分配到此角色的用户将无法编辑或发布。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| 决策管理 | <ul><li>**[!DNL View decisions]**：对决策实体的只读访问权限。</li></ul> |
| 历程 | <ul><li>**[!DNL View journeys]**：对历程的只读访问权限。</li><li>**[!DNL View journeys event, data sources, actions]**：对历程事件和数据源的只读访问权限。</li><li>**[!DNL View journeys report]**：对历程报告的只读访问权限。</li></ul> |

## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

**[!DNL Orchestrated Campaign Administrator]**&#x200B;角色允许管理菜单管理和发布编排的营销活动。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Enable AI Assistant]**：启用或访问AI支持的营销活动和受众功能。</li> <li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li> <li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li> <li>**[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li> <li>**[!DNL View datasets]**：对数据集的只读访问权限。</li> <li>**[!DNL Read Identity namespace]**：对标识命名空间的只读访问权限。</li> <li>**[!DNL View schemas]**：对架构的只读访问权限。</li> <li>**[!DNL Sandbox]**：授予对沙盒的访问权限。</li> <li>**[!DNL View operational insights]**：对系统级洞察和监控仪表板的只读访问权限。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL Export suppression list]**：访问将禁止列表导出为CSV文件的权限。</li> <li>**[!DNL Manage alerts]**：为营销活动、消息和权利启用/禁用警报。</li> <li>**[!DNL Manage custom dashboards]**：读取、创建、编辑和删除自定义仪表板。</li><li>**[!DNL Manage IP pools]**：读取、创建、编辑和删除ip池。</li> <li>**[!DNL Manage landing page settings]**：读取、创建、编辑和删除登陆页面设置。</li> <li>**[!DNL Manage messages general settings]**：读取、创建、编辑和删除邮件常规设置。</li> <li>**[!DNL Manage messages presets]**：读取、创建、编辑和删除内容品牌。</li><li>**[!DNL Manage PTR records]**：读取和编辑PTR记录。</li> <li>**[!DNL Manage SMS settings]**：读取、创建、编辑和删除短信设置。</li> <li>**[!DNL Manage subdomains delegation]**：读取、创建、编辑和删除子域委派。</li> <li>**[!DNL Manage suppression rules]**：访问读取、创建、编辑和删除禁止显示规则。</li> <li>**[!DNL View PTR records]**：对PTR记录的只读访问权限。</li> <li>**[!DNL View suppression list]**：读取和导出本地禁止显示列表。</li> </ul> |
| 功能板 | <ul> <li>**[!DNL Manage standard dashboard]**：通过构件库读取、创建、编辑和删除自定义构件和构件架构。</li> </ul> |
| 数据治理 | <ul> <li>**[!DNL View user activity log]**：只读访问权限，可查看Experience Platform活动记录的审核日志。 </li> </ul> |
| 数据摄取 | <ul> <li>**[!DNL Manage sources]**：读取、创建、编辑和禁用源。</li> </ul> |
| 数据管理 | <ul> <li>**[!DNL Manage datasets]**：读取、创建、编辑和删除数据集。</li> </ul> |
| 数据建模 | <ul> <li>**[!DNL Manage schemas]**：读取、创建、编辑和删除架构和相关资源。</li> </ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除排名策略。</li></ul> |
| Journey Optimizer规则 | <ul> <li>**[!DNL View frequency rules]**：对频率规则的只读访问权限。</li><li>**[!DNL Manage frequency rules]**：读取、创建、编辑或删除频率规则。</li> </ul> |
| 消息 | <ul><li> **[!DNL Manage Messages]**：读取、创建、编辑和删除消息。 </li> **[!DNL Manage Messages Preview and Test]**：在应用策略时批准和发布消息。</li><li>**[!DNL Publish Messages]**：发布消息。 </li><li>**[!DNL View Messages Report]**：读取和编辑邮件报告。 <li></ul> |
| 编排的营销活动 | <ul><li> **[!DNL Manage orchestrated campaigns]**：读取、创建、编辑和删除编排的营销活动。</li> <li>**[!DNL Manage orchestrated campaigns admin]**：读取、创建、编辑和删除Adobe Experience Platform配置文件与关系存储实体之间的链接和协调。</li><li>**[!DNL Publish orchestrated campaigns]**：发布编排的营销活动。</li><li>**[!DNL View orchestrated campaigns report]**：读取并编辑编排的营销活动报告。</li></ul> |

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

**[!DNL Orchestrated Campaign Approver]**&#x200B;角色允许用户发布编排的营销活动。

| 资源 | 权限 |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li> <li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li> <li>**[!DNL View datasets]**：对数据集的只读访问权限。</li> <li>**[!DNL View schemas]**：对架构的只读访问权限。</li> <li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li> <li>**[!DNL Enable AI Assistant]**：启用或访问AI支持的营销活动和受众功能。</li>  <li>**[!DNL View operational insights]**：对系统级洞察和监控仪表板的只读访问权限。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL View messages presets]**：对消息预设的只读访问权限。</li> <li>**[!DNL Manage custom dashboards]**：创建、编辑和删除自定义仪表板。</li></ul> |
| 功能板 | <ul> <li>**[!DNL Manage standard dashboard]**：通过构件库读取、创建、编辑和删除自定义构件和构件架构。</li> </ul> |
| 数据治理 | <ul> <li>**[!DNL View user activity log]**：只读访问权限，可查看Experience Platform活动记录的审核日志。</li> </ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义消息报告并使用操作功能。</li></ul> |
| Journey Optimizer规则 | <ul> <li>**[!DNL View frequency rules]**：对频率规则的只读访问权限。</li></ul> |
| 消息 | <ul><li> **[!DNL Manage Messages]**：读取、创建、编辑和删除消息。 </li> **[!DNL Manage Messages Preview and Test]**：在应用策略时批准和发布消息。</li><li>**[!DNL Publish Messages]**：发布消息。 </li><li>**[!DNL View Messages Report]**：读取和编辑邮件报告。 <li></ul> |
| 编排的营销活动 | <ul><li>**[!DNL Manage orchestrated campaigns]**：读取、创建、编辑和删除编排的营销活动。</li><li>**[!DNL Publish orchestrated campaigns]**：发布编排的营销活动。</li><li>**[!DNL View orchestrated campaigns admin]**：对Adobe Experience Platform配置文件与关系存储实体之间的链接和协调的只读访问权限。</li><li>**[!DNL View orchestrated campaigns report]**：读取、编辑编排的营销活动报告。</li></ul> |

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

**[!DNL Orchestrated Campaign Manager]**&#x200B;角色允许用户创建和编辑&#x200B;**[!UICONTROL 协调的营销活动]**&#x200B;以及链接到&#x200B;**[!UICONTROL 协调的营销活动]**&#x200B;的每个功能，但无法发布它们。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Enable AI Assistant]**：启用或访问AI支持的营销活动和受众功能。</li> <li>**[!DNL Manage merge policies]**：读取、创建、编辑和删除合并策略。</li><li>**[!DNL Manage profiles]**：读取、创建、编辑和删除配置文件。</li><li> **[!DNL Manage segments]**：读取、创建、编辑和删除区段定义。</li><li>**[!DNL View datasets]**：对数据集的只读访问权限。</li>  <li>**[!DNL View operational insights]**：对系统级洞察和监控仪表板的只读访问权限。</li><li>**[!DNL View schemas]**：对架构的只读访问权限。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL Manage custom dashboards]**：创建、编辑和删除自定义仪表板。</li><li>**[!DNL View messages presets]**：对消息预设的只读访问权限。</li></ul> |
| 功能板 | <ul> <li>**[!DNL Manage standard dashboard]**：通过构件库读取、创建、编辑和删除自定义构件和构件架构。</li> </ul> |
| 数据治理 | <ul> <li>**[!DNL View user activity log]**：只读访问权限，可查看Experience Platform活动记录的审核日志。</li> </ul> |
| 决策管理 | <ul><li>**[!DNL Manage decisions]**：读取、创建、编辑和删除决策实体。</li><li>**[!DNL Manage ranking strategies]**：读取、创建、编辑和删除自定义消息报告并使用操作功能。</li></ul> |
| Journey Optimizer规则 | <ul> <li>**[!DNL View frequency rules]**：对频率规则的只读访问权限。 </li></ul> |
| 消息 | <ul><li> **[!DNL Manage Messages]**：读取、创建、编辑和删除消息。 </li> **[!DNL Manage Messages Preview and Test]**：在应用策略时批准和发布消息。</li><li>**[!DNL View Messages Report]**：读取和编辑邮件报告。 </li></ul> |
| 编排的营销活动 | <ul><li>**[!DNL Manage orchestrated campaigns]**：读取、创建、编辑和删除编排的营销活动。</li><li>**[!DNL View orchestrated campaigns report]**：读取、编辑编排的营销活动。</li><li>**[!DNL View orchestrated campaigns admin]**：对Adobe Experience Platform配置文件与关系存储实体之间的链接和协调的只读访问权限。</li></ul> |

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

**[!DNL Campaign Viewer]**&#x200B;角色允许对&#x200B;**[!UICONTROL 协调的营销活动]**&#x200B;功能进行只读访问。

分配到此角色的用户将无法编辑或发布。

此角色包括以下权限：

| 资源 | 权限 |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Enable AI Assistant]**：启用或访问AI支持的营销活动和受众功能。</li> <li>**[!DNL View operational insights]**：对系统级洞察和监控仪表板的只读访问权限。</li></ul> |
| 渠道配置 | <ul><li>**[!DNL Manage custom dashboards]**：创建、编辑和删除自定义仪表板。</li></ul> |
| 功能板 | <ul> <li>**[!DNL Manage standard dashboard]**：通过构件库读取、创建、编辑和删除自定义构件和构件架构。</li> </ul> |
| 数据治理 | <ul> <li>**[!DNL View user activity log]**：只读访问权限，可查看Experience Platform活动记录的审核日志。</li> </ul> |
| 决策管理 | <ul><li>**[!DNL View decisions]**：对决策实体的只读访问权限。</li></ul> |
| Journey Optimizer规则 | <ul> <li>**[!DNL View frequency rules]**：对频率规则的只读访问权限。</li></ul> |
| 编排的营销活动 | <ul><li>**[!DNL View orchestrated campaigns]**：对编排的营销活动的只读访问权限。</li><li>**[!DNL View orchestrated campaigns report]**：对编排的营销活动报告的只读访问权限。</li></ul> |

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：** Journey Optimizer随附内置角色（从Campaign管理员到编排的Campaign查看器），每个角色都捆绑着一个现成的权限集，因此管理员可以快速授予用户与其职责相匹配的访问级别，而无需从头开始构建角色。

**意图：**

* 确定最适合用户工作责任的内置角色
* 了解每个内置角色可以执行哪些操作，无法执行哪些操作（包括发布权限）
* 比较历程、营销活动和编排的营销活动域中的角色
* 分配现成的角色，而不是创建自定义角色
* 了解哪些角色包括AI助手访问权限

**术语表：**

* **内置角色**：预定义的权限和资源权限集已准备好分配给没有自定义配置的用户&#x200B;*（产品特定）*
* **历程管理员**：内置角色，用于管理和发布历程和决策管理，包括渠道配置和数据管理权限&#x200B;*（特定于产品）*
* **Campaign管理员**：启用营销活动和决策管理（包括渠道配置）的管理和发布的内置角色&#x200B;*（特定于产品）*
* **决策管理器**：内置角色，提供对决策管理菜单的独占访问权限；可以管理、查看和发布决策&#x200B;*（特定于产品）*
* **内容库管理器**：内置角色，仅提供对内容模板菜单的访问权限；无法访问历程或营销活动&#x200B;*（产品特定）*
* **测试模式**：“管理历程”和“发布历程”权限中引用的历程执行模式（历程管理员可以在测试模式下停止历程；“发布历程”权限包括启动测试模式）*（产品特定）*
* **试运行**：在测试模式&#x200B;*（产品特定）*&#x200B;旁边的“管理历程和发布历程”权限中引用的历程执行模式

**术语：**

* 规范名称：内置角色 — 变体：即装即用角色、OOTB角色、产品配置文件
* 请勿混淆：“营销活动审批者”（可以审批和发布营销活动）≠“营销活动管理员”（可以创建和编辑营销活动，但不能发布它们）
* 请勿混淆：“历程审批者”（可以审批和发布旅程）≠“历程管理员”（可以创建和编辑旅程，但不能发布它们）
* 请勿混淆：“历程查看器”（对历程和决策管理的只读访问权限）≠“营销活动查看器”（对营销活动和决策管理的只读访问权限）
* 请勿混淆：“编排的活动管理员”（管理编排的活动，包括AI助手和数据摄取/管理）≠“活动管理员”（管理标准活动；不包括编排的活动权限）
* 请勿混淆：“测试模式”（称为可通过管理历程/发布历程停止或启动的历程执行状态）≠“练习”（这些相同权限中还引用了单独的历程执行模式）

**常见问题解答：**

* **问：哪些内置角色可以发布历程？** —历程管理员和历程审批者可以发布旅程。
* **问：历程管理员能否发布历程？**  — 否；历程管理员可以创建并编辑历程，但发布历程权限不包括在该角色中。
* **问：哪个角色仅授予对决策管理菜单的访问权限？**  — 决策管理器。
* **问：哪个角色仅提供对内容模板的访问权限？**  — 内容库管理器。
* **问：哪些内置角色包含“启用AI助手”权限？**  — 编排的活动管理员、编排的活动审批者、编排的活动经理和编排的活动查看者。

+++
<!-- ai-accordion-version: 1 | source-hash: b9740765 -->




