---
solution: Journey Optimizer
product: journey optimizer
title: 配置忠诚度计划
description: 了解如何在Adobe Journey Optimizer中为您的忠诚度计划配置奖励提供商、事件定义和组织设置。
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="私人测试版" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: e66628ab1d9df497226ab625947aa18a2a3b6f48
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 2%

---

# 配置忠诚度计划 {#loyalty-admin}

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* [忠诚度挑战入门](get-started.md)
* [访问和管理挑战和任务](access-loyalty-challenges.md)
* [创建挑战](create-challenges.md)
* [创建任务](create-tasks.md)
* [监测忠诚度挑战表现](loyalty-reporting.md)
* **配置忠诚度计划** ◀&rbrace;︎**您位于此处**
* [忠诚度挑战API参考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私人测试版**&#x200B;中。 有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](../rn/releases.md)。

在&#x200B;**[!UICONTROL 忠诚度管理员]**&#x200B;部分，管理员可配置Journey Optimizer如何连接到忠诚度计划后端。 营销人员使用&#x200B;**[!UICONTROL 忠诚度挑战(Beta)]**&#x200B;来设计挑战、任务、内容和消息；忠诚度管理员是用于奖励履行和事件映射的单次设置。

当客户完成挑战（或达到奖励里程碑）时，Journey Optimizer会调用您在此处配置的奖励提供商，以提供点数或其他奖励。 挑战&#x200B;**[!UICONTROL 内容]**、**[!UICONTROL 消息]**&#x200B;和&#x200B;**[!UICONTROL 受众]**&#x200B;设置不受忠诚度管理员配置的影响。

## 访问忠诚度管理员 {#access-loyalty-admin}

要打开“忠诚度管理员”，请登录到Journey Optimizer，然后在左侧导航中选择&#x200B;**[!UICONTROL 忠诚度管理员]**。

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

管理界面分为几个选项卡。 根据您的组织，您可能会看到&#x200B;**[!UICONTROL 全局设置]**、**[!UICONTROL 奖励提供商]**、**[!UICONTROL 事件定义]**&#x200B;和&#x200B;**[!UICONTROL 产品清单]**。

## 全局设置 {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="全局设置"
>abstract="为您的忠诚度计划选择Adobe Experience Platform身份命名空间，并复制您的配置ID。 必须先设置这些组织级别设置，然后奖励提供商才能正确履行奖励。"

使用&#x200B;**[!UICONTROL 全局设置]**&#x200B;为忠诚度挑战配置组织范围的选项。

1. 打开&#x200B;**[!UICONTROL 全局设置]**&#x200B;选项卡。

1. 在&#x200B;**[!UICONTROL 命名空间]**&#x200B;下拉列表中，从Adobe Experience Platform中选择您的忠诚度计划使用的[身份命名空间](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/namespaces)。 选择&#x200B;**[!UICONTROL 保存]**&#x200B;以更新您组织的忠诚度挑战配置上的命名空间。

1. 如果需要与实施团队或外部系统共享&#x200B;**[!UICONTROL 配置ID]**，请复制它。

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## 奖励提供者 {#reward-providers}

**奖励提供商**&#x200B;告知Journey Optimizer在记录挑战进度或完成挑战时发送完成调用的位置，例如，将会员积分或开始点数授予会员帐户的API。

奖励提供者包括：

* 基本连接详细信息（名称、描述、API URL、标头）
* **[!UICONTROL 奖励定义]** — 此提供商可以颁发的奖励类型（例如，星级或英里）
* **[!UICONTROL 奖励代理]**（可选） — 通过代理路由调用，而不是直接路由到您的端点
* **[!UICONTROL 身份验证令牌生成器]** — Journey Optimizer如何在调用API之前获取访问令牌

### 创建奖励提供者 {#create-reward-provider}

按照以下步骤注册新的奖励提供商及其相关资源。

1. 打开&#x200B;**[!UICONTROL 奖励提供商]**&#x200B;选项卡并开始创建提供商。

1. 输入&#x200B;**[!UICONTROL Name]**&#x200B;和&#x200B;**[!UICONTROL Description]**，然后输入发送履行请求的&#x200B;**[!UICONTROL API URL]**。

1. 根据需要为API添加&#x200B;**[!UICONTROL 标头]**（例如，API密钥或内容类型）。 您可以在UI中添加或删除标题行。

1. 配置&#x200B;**[!UICONTROL 奖励定义]**：

   * 定义您的提供商支持的每种奖励类型（例如，计划积分或星级）。
   * 可以选择将一个定义标记为该提供程序的&#x200B;**默认值**。
   * 为每个定义指定随履行调用发送的&#x200B;**有效负载**。

1. 可选配置&#x200B;**[!UICONTROL 奖励代理]**：

   * **[!UICONTROL 主机]**、**[!UICONTROL 端口]**&#x200B;和凭据
   * **[!UICONTROL Name]**、**[!UICONTROL Description]**&#x200B;以及代理是否已启用&#x200B;**&#x200B;**

1. 如果在每次调用之前您的API需要令牌，请配置&#x200B;**[!UICONTROL 身份验证令牌生成器]**：

   * 令牌端点URL和HTTP方法（例如，OAuth样式流的&#x200B;**POST**）
   * 响应中的&#x200B;**[!UICONTROL 令牌键]**（例如，`access_token`）
   * 令牌端点所需的标头

   Journey Optimizer在调用奖励API之前从此配置请求令牌，因此调用使用当前凭据。

1. 选择&#x200B;**[!UICONTROL 创建奖励提供者]**。 提供程序及其子资源（定义、代理和令牌生成器）一起创建。

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

创建后，该提供商将显示在奖励提供商列表中。 营销人员在[配置挑战奖励](create-challenges.md#rewards)时选择此提供商。

### 编辑奖励提供者 {#edit-reward-provider}

1. 打开&#x200B;**[!UICONTROL 奖励提供商]**&#x200B;选项卡并选择提供商。

1. 根据需要更新提供商的名称、描述、URL或标头。

1. 要更改&#x200B;**[!UICONTROL 奖励定义]**、**[!UICONTROL 奖励代理]**&#x200B;或&#x200B;**[!UICONTROL 身份验证令牌生成器]**，请打开相应的部分并编辑字段。 对这些子资源所做的更改会在您就地更新时保存。

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>对于&#x200B;**[!UICONTROL 自带数据]**&#x200B;挑战（任务和奖励完全来自您的数据集成），此处配置的奖励提供商可能不适用。 [了解更多关于如何应对您自己的数据挑战](create-challenges.md#create-the-challenge)。

## 事件定义 {#event-definitions}

**[!UICONTROL 事件定义]**&#x200B;将品牌格式的传入体验事件映射到忠诚度挑战可以使用的活动，特别是&#x200B;**[!UICONTROL 自定义事件]**&#x200B;任务。 当数据从您的渠道到达时，Journey Optimizer会使用这些定义来确定某个事件是否相关以及如何解释它。 忽略不符合任何定义的事件。

### 创建事件定义 {#create-event-definition}

1. 打开&#x200B;**[!UICONTROL 事件定义]**&#x200B;选项卡并创建新定义。

1. 输入事件的&#x200B;**[!UICONTROL Name]**（例如，`Coffee purchase`）。 此名称是营销人员在配置&#x200B;**[!UICONTROL 自定义事件]**&#x200B;任务时选择的名称。

1. 指定如何识别传入有效负载中的事件：

   * **[!UICONTROL 标识符路径]** — 标识事件或成员的字段的JSON路径（例如，`data.memberId`）
   * **[!UICONTROL 标识符值]** — 必须存在值才能匹配此定义

1. （可选）指定&#x200B;**[!UICONTROL XDM架构ID]**&#x200B;和/或使用&#x200B;**[!UICONTROL 架构]**&#x200B;和&#x200B;**[!UICONTROL 转换器]**&#x200B;字段粘贴架构和转换字符串，以便您的团队在处理之前分析和验证传入JSON。

   您可以提供XDM架构ID和/或标识符路径，具体取决于事件的结构。

1. 保存事件定义。

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

大多数组织会创建多个事件定义 — 每个要跟踪的活动（例如，购买、登记或网站访问）都有一个事件定义。 [了解如何在挑战中使用自定义事件任务](create-tasks.md#choose-activity)。

## 产品库存 {#product-inventory}

**[!UICONTROL 产品清单]**&#x200B;选项卡允许您上传CSV文件，以将产品或项目标识符（例如，MPG ID）映射到任务资格中使用的产品组。 这支持任务引用分组产品而不是手动键入的单个SKU的情况。

1. 打开&#x200B;**[!UICONTROL 产品清单]**&#x200B;选项卡。

1. 通过将映射文件拖入上传区域或浏览以将其选中，上传该映射文件。

1. 查看清单列表中的导入映射。 选择一个产品组以查看该组中的所有项目。 使用搜索功能可按名称或ID查找项目。

1. 使用&#x200B;**[!UICONTROL 上载历史记录]**&#x200B;查看以前的上载。

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>产品清单的&#x200B;**[!UICONTROL 全局排除项]**&#x200B;计划用于未来版本，此处未记录此内容。

## 忠诚度管理员如何应对挑战 {#how-admin-relates-to-challenges}

| 面积 | 在忠诚度管理中配置 | 在忠诚度挑战中配置 |
|------|----------------------------|----------------------------------|
| 奖励履行API | 是 — 奖励提供者 | 否 — 仅选择提供者和金额 |
| 自定义活动的事件映射 | 是 — 事件定义 | 否 — 在自定义事件任务中选择事件名称 |
| 产品组映射 | 是 — 产品库存 | 否 — 在创作购买/支出任务时使用组 |
| 挑战结构、内容、受众 | 否 | 是 |

典型设置顺序：

1. 在忠诚度管理员中配置&#x200B;**[!UICONTROL 全局设置]**&#x200B;和至少一个&#x200B;**[!UICONTROL 奖励提供程序]**。
1. 如果您的程序使用自定义事件或基于CSV的产品组，可以选择添加&#x200B;**[!UICONTROL 事件定义]**&#x200B;和&#x200B;**[!UICONTROL 产品清单]**。
1. 在&#x200B;**[!UICONTROL 忠诚度挑战(Beta)]**&#x200B;中创建[任务](create-tasks.md)和[挑战](create-challenges.md)，选择您配置的奖励提供商和定义。

当客户获得奖励时，Adobe Journey Optimizer会向您的提供商发送履行呼叫；您的忠诚度平台拥有该会员的账户贷记。

## 先决条件 {#prerequisites}

忠诚度管理员适用于贵组织中的少数管理员。 除了[忠诚度挑战](get-started.md#prerequisites)所需的权限之外，您还需要配置组织级别的忠诚度设置的权限。

如果&#x200B;**[!UICONTROL 忠诚度管理员]**&#x200B;未出现在左侧导航中，或者您无法保存全局设置或奖励提供商，请联系您的管理员。
