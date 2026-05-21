---
solution: Journey Optimizer
product: journey optimizer
title: 配置忠诚度计划
description: 了解如何在Adobe Journey Optimizer中为您的忠诚度计划配置奖励提供商、事件定义和组织级别设置。
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="私人测试版" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: a4ad533e54f3692eb0483138a8cfd1cee0e77ba1
workflow-type: tm+mt
source-wordcount: '1128'
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
* **配置忠诚度计划** ◀}︎**您位于此处**
* [忠诚度挑战API参考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私人测试版**&#x200B;中。 有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](../rn/releases.md)。

在&#x200B;**[!UICONTROL 忠诚度管理员]**&#x200B;部分中，您可以配置Journey Optimizer如何连接到外部忠诚度系统。 营销人员使用&#x200B;**[!UICONTROL 忠诚度挑战(Beta)]**&#x200B;设计挑战、任务、内容和消息。 **[!UICONTROL 忠诚度管理员]**&#x200B;是一个单独的仅管理员区域，用于奖励履行、事件映射和产品库存。

当客户完成挑战或达到奖励里程碑时，Journey Optimizer会调用您配置为提供点数或其他奖励的奖励提供商。 **[!UICONTROL 忠诚度管理员]**&#x200B;中的配置不会影响挑战&#x200B;**[!UICONTROL 内容]**、**[!UICONTROL 消息]**&#x200B;或&#x200B;**[!UICONTROL 受众]**&#x200B;设置 — 这些设置仍受营销人员控制。

## 您在此处配置的内容与忠诚度挑战中的配置 {#scope}

| 面积 | 在忠诚度管理中配置 | 在忠诚度挑战中配置 |
|------|----------------------------|----------------------------------|
| 奖励履行API | 是 — 奖励提供者 | 否 — 仅选择提供者和金额 |
| 自定义活动的事件映射 | 是 — 事件定义 | 否 — 在自定义事件任务中选择事件名称 |
| 产品组映射 | 是 — 产品库存 | 否 — 在创作购买/支出任务时使用组 |
| 挑战结构、内容、受众 | 否 | 是 |

当客户获得奖励时，Adobe Journey Optimizer会向您的奖励提供商发送履行呼叫。 您的忠诚度平台负责将会员的账户贷记。

## 先决条件 {#prerequisites}

**[!UICONTROL 忠诚度管理员]**&#x200B;适用于每个组织的少量管理员。 除了[忠诚度挑战](get-started.md#prerequisites)所需的权限之外，您还需要Journey Optimizer实例的管理员级访问权限。 联系Adobe管理员以请求获取访问权限。

## 访问忠诚度管理员 {#access-loyalty-admin}

要打开&#x200B;**[!UICONTROL 忠诚度管理员]**，请从Journey Optimizer的左侧导航中选择它。

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

**[!UICONTROL 忠诚度管理员]**&#x200B;组织为选项卡：**[!UICONTROL 全局设置]**、**[!UICONTROL 奖励提供商]**、**[!UICONTROL 事件定义]**&#x200B;和&#x200B;**[!UICONTROL 产品清单]**。 您可用的选项卡取决于贵组织的权限和功能配置。

## 全局设置 {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="全局设置"
>abstract="为您的忠诚度计划选择Adobe Experience Platform身份命名空间，并复制您的配置ID。 必须先设置这些组织级别设置，然后奖励提供商才能正确履行奖励。"

使用&#x200B;**[!UICONTROL 全局设置]**&#x200B;为忠诚度挑战配置组织范围的选项。

1. 打开&#x200B;**[!UICONTROL 全局设置]**&#x200B;选项卡。

1. 在&#x200B;**[!UICONTROL 命名空间]**&#x200B;下拉列表中，选择忠诚度计划使用的[身份命名空间](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/namespaces)。

1. 选择&#x200B;**[!UICONTROL 保存]**&#x200B;以将命名空间应用于您的忠诚度挑战配置。

1. 在需要与实施团队或外部系统共享&#x200B;**[!UICONTROL 配置ID]**&#x200B;时（例如，配置入站事件投放时），请复制该ID。

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## 奖励提供者 {#reward-providers}

**奖励提供商**&#x200B;告知Journey Optimizer在记录挑战进度或完成挑战时发送完成调用的位置，例如，将会员积分或开始点数授予会员帐户的API。

奖励提供商配置包括：

* 基本连接详细信息（名称、描述、API URL、标头）
* **[!UICONTROL 奖励定义]** — 此提供商可以颁发的奖励类型（例如，星级或英里）
* **[!UICONTROL 奖励代理]**（可选） — 通过而非您的端点直接路由调用的中间代理
* **[!UICONTROL 身份验证令牌生成器]** — Journey Optimizer在调用API之前用于获取访问令牌的机制

### 创建奖励提供者 {#create-reward-provider}

1. 打开&#x200B;**[!UICONTROL 奖励提供者]**&#x200B;选项卡并选择&#x200B;**[!UICONTROL 创建奖励提供者]**。

1. 输入接收履行请求的&#x200B;**[!UICONTROL Name]**、**[!UICONTROL Description]**&#x200B;和&#x200B;**[!UICONTROL API URL]**。

1. 根据需要为API添加&#x200B;**[!UICONTROL 标头]**（例如，API密钥或内容类型）。

1. 配置&#x200B;**[!UICONTROL 奖励定义]** — 您的提供商支持的每个奖励类型有一个条目（例如，计划积分或星级）。 对于每个定义：

   * 指定随履行调用发送的&#x200B;**有效负荷**。
   * 可以选择将一个定义标记为此提供程序的&#x200B;**默认值**。

1. 可以选择配置&#x200B;**[!UICONTROL 奖励代理]**&#x200B;以通过中间服务器路由履行调用：

   * **[!UICONTROL Name]**、**[!UICONTROL Description]**&#x200B;以及代理是否已启用&#x200B;****
   * **[!UICONTROL 主机]**、**[!UICONTROL 端口]**&#x200B;和凭据

1. 如果API需要持有者令牌进行身份验证，请配置&#x200B;**[!UICONTROL 身份验证令牌生成器]**：

   * 令牌端点URL和HTTP方法（例如，OAuth样式流的&#x200B;**POST**）
   * 响应中的&#x200B;**[!UICONTROL 令牌键]**（例如，`access_token`）
   * 令牌端点所需的标头

   Journey Optimizer使用此配置在调用奖励API之前获取新的令牌。

1. 选择&#x200B;**[!UICONTROL 创建奖励提供程序]**。 提供程序与所有已配置的子资源一起保存。

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

保存后，该提供商将显示在奖励提供商列表中。 营销人员在[配置挑战奖励](create-challenges.md#rewards)时选择此提供商。

要编辑现有的奖励提供者，请打开&#x200B;**[!UICONTROL 奖励提供者]**&#x200B;选项卡，选择提供者，并更新适当的字段。 更新子资源（奖励定义、代理、身份验证令牌生成器）时，将保存对子资源的更改。

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>**[!UICONTROL 自带数据]**&#x200B;挑战可通过您自己的数据集成完成奖励。 此处配置的奖励提供商不适用于这些挑战。 [了解更多关于如何应对您自己的数据挑战](create-challenges.md#create-the-challenge)。

## 事件定义（可选） {#event-definitions}

**[!UICONTROL 事件定义]**&#x200B;将您系统中的体验事件（无论您的品牌使用什么JSON或XDM格式）映射到忠诚度挑战可以执行的活动，最显着的是&#x200B;**[!UICONTROL 自定义事件]**&#x200B;任务。 当事件到达时，Journey Optimizer会使用这些定义确定是否处理它们。 忽略不符合任何定义的事件。

### 创建事件定义 {#create-event-definition}

1. 打开&#x200B;**[!UICONTROL 事件定义]**&#x200B;选项卡并创建新定义。

1. 输入事件的&#x200B;**[!UICONTROL 名称]**（例如，`Coffee purchase`） — 这是营销人员在配置&#x200B;**[!UICONTROL 自定义事件]**&#x200B;任务时看到的名称。

1. 指定如何识别传入有效负载中的事件：

   * **[!UICONTROL 标识符路径]** — 标识事件或成员的字段的JSON路径（例如，`data.memberId`）
   * **[!UICONTROL 标识符值]** — 必须存在值才能匹配此定义

1. 如果您的事件负载符合Experience Platform架构，可以选择指定&#x200B;**[!UICONTROL XDM架构ID]**。

1. 可选地使用&#x200B;**[!UICONTROL 架构]**&#x200B;和&#x200B;**[!UICONTROL 转换器]**&#x200B;字段提供自定义架构和转换字符串，以分析和验证传入的JSON。

   您可以提供XDM架构ID和/或标识符路径，具体取决于事件的结构。

1. 保存事件定义。

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

大多数组织会创建多个事件定义 — 每个要跟踪的活动创建一个事件定义（例如，购买、登记或网站访问）。 [了解如何在挑战中使用自定义事件任务](create-tasks.md#choose-activity)。

## 产品库存（可选） {#product-inventory}

使用&#x200B;**[!UICONTROL 产品清单]**&#x200B;选项卡上传将产品或项目标识符（例如，MPG ID）映射到产品组的CSV文件。 接下来，营销人员可以在任务资格规则中引用这些组，而不是键入单个SKU。

1. 打开&#x200B;**[!UICONTROL 产品清单]**&#x200B;选项卡。

1. 上载映射文件。

1. 查看清单列表中的导入映射。 选择一个产品组以查看该组中的所有项目，或使用搜索按名称或ID查找项目。

1. 使用&#x200B;**[!UICONTROL 上载历史记录]**&#x200B;查看以前的上载。

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>产品清单的&#x200B;**[!UICONTROL 全局排除项]**&#x200B;计划用于未来版本，此处未记录此内容。
