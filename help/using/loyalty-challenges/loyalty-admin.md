---
solution: Journey Optimizer
product: journey optimizer
title: 配置忠诚度计划
description: 了解如何在Adobe [!DNL Journey Optimizer]中为您的忠诚度计划配置奖励提供商、事件定义和组织级别设置。
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="私人测试版" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: e4ee70a9c918bffb372ab7cee567ae7422c3720c
workflow-type: tm+mt
source-wordcount: '1456'
ht-degree: 0%

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
>此功能当前处于&#x200B;**私人测试版**&#x200B;中。 有关[!DNL Journey Optimizer]中发行周期和可用性阶段的完整详细信息，请参阅[发行周期](../rn/releases.md)。

使用[!DNL Journey Optimizer]中的忠诚度计划配置连接到外部忠诚度系统。 营销人员使用&#x200B;**[!UICONTROL 忠诚度挑战(Beta)]**&#x200B;设计挑战、任务、内容和消息。 忠诚度计划配置是一个单独的仅管理员区域，用于奖励履行、事件映射、产品库存和排除。

## 先决条件 {#prerequisites}

忠诚度计划配置适用于管理员。 除了忠诚度挑战所需的权限之外，您还需要管理员级别的[!DNL Journey Optimizer]实例访问权限。 联系Adobe管理员以请求获取访问权限。

## 访问忠诚度计划配置 {#access-loyalty-admin}

导航到&#x200B;**[!UICONTROL 忠诚度]**&#x200B;并选择&#x200B;**[!UICONTROL 忠诚度管理员]**&#x200B;以访问忠诚度计划配置界面。

该界面将组织为选项卡：

* **全局设置** — 设置Experience Platform标识命名空间。 [了解如何配置全局设置](#global-settings)
* **奖励提供者** — 连接完成奖励的外部API，包括奖励类型、代理和身份验证。 [了解如何配置奖励提供商](#reward-providers)
* **事件定义** — 将传入体验事件映射到可在&#x200B;**[!UICONTROL 自定义事件]**&#x200B;任务中使用的活动。 [了解如何配置事件定义](#event-definitions)
* **产品库存** — 上传项目到组的映射，以便在任务资格规则中使用产品组。 [了解如何配置产品清单](#product-inventory)
* **排除项** — 上传营销人员配置任务时适用的组织范围项目和组排除项。 [了解如何配置排除项](#exclusions)

## 全局设置 {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="全局设置"
>abstract="为您的忠诚度计划选择Adobe Experience Platform身份命名空间。"

打开&#x200B;**[!UICONTROL 全局设置]**&#x200B;选项卡。 目前，此选项卡中可用的主要配置是从&#x200B;**[!UICONTROL 命名空间]**&#x200B;下拉列表中选择忠诚度计划使用的Adobe Experience Platform身份命名空间。

![](assets/admin-global-settings.png)

➡️ [了解如何使用身份命名空间](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/namespaces){target="_blank"}

## 奖励提供者 {#reward-providers}

**奖励提供商**&#x200B;告知[!DNL Journey Optimizer]在记录挑战进度或完成挑战时发送完成呼叫的位置，例如，将会员积分或开始积分到会员帐户的API。

奖励提供商配置包括：

![](assets/admin-reward.png)

* 基本连接详细信息（名称、描述、URL、标头）。
* **[!UICONTROL 奖励定义]** — 此提供商可以颁发的奖励类型（例如，星级或英里）。
* **[!UICONTROL 奖励代理]** — 一个中间代理，通过它来路由调用，而不是直接路由您的端点。
* **[!UICONTROL 身份验证令牌生成器]** — [!DNL Journey Optimizer]在调用API之前用于获取访问令牌的机制。

要创建奖励提供者，请执行以下步骤：

1. 打开&#x200B;**[!UICONTROL 奖励提供者]**&#x200B;选项卡并选择&#x200B;**[!UICONTROL 创建奖励提供者]**。

1. 输入&#x200B;**[!UICONTROL Name]**&#x200B;和&#x200B;**[!UICONTROL Description]**。

1. 在&#x200B;**[!UICONTROL URL]**&#x200B;字段中，输入接收履行请求的API URL。

1. 根据需要为API添加&#x200B;**[!UICONTROL 标头]**（例如，API密钥或内容类型）。

1. 配置以下与您的奖励提供商关联的资源。 展开每个部分以了解更多信息：

   +++奖励定义 — 您的提供商支持的每个奖励一个条目（例如，计划积分或星级、货币信用）

   对于每个定义：

   * 提供名称和描述。
   * 指定定义是否为&#x200B;**[!UICONTROL 已启用]**。
   * 切换&#x200B;**![!UICONTROL Default]**&#x200B;选项以将一个定义标记为此提供程序的默认值。
   * 指定随履行调用发送的&#x200B;**有效负荷**。

   ![](assets/admin-reward-definition.png)

   +++

   +++奖励代理 — 将履行调用路由到中间服务器，而不是直接路由到端点

   * 提供名称和描述。
   * 输入&#x200B;**[!UICONTROL 主机]**，**[!UICONTROL 端口]**&#x200B;信息。
   * 指定代理是否为&#x200B;**[!UICONTROL 已启用]**。
   * 添加代理&#x200B;**[!UICONTROL 凭据]**。

   ![](assets/admin-reward-proxies.png)

   +++

   +++身份验证令牌生成器 — 如果您的API需要持有者令牌才能进行身份验证

   * 输入名称和说明。
   * 在Auth type字段中，输入身份验证类型（例如Bearer）。
   * 选择要使用的HTTP方法（例如POST）。
   * 输入令牌端点URL。 并在响应中添加&#x200B;**[!UICONTROL 令牌键]**（例如，`access_token`）。
   * 指定身份验证令牌生成器是否为&#x200B;**[!UICONTROL 已启用]**。
   * 如果需要，添加令牌端点所需的标头。

   [!DNL Journey Optimizer]使用此配置在调用奖励API之前获取新的令牌。

   ![](assets/admin-reward-auth.png)

   +++

1. 选择&#x200B;**[!UICONTROL 创建奖励提供程序]**。 提供程序与所有配置的资源一起保存。

保存后，该提供商将显示在奖励提供商列表中。 营销人员在配置质询奖励时可以选择此提供商。 [了解如何配置挑战奖励](create-challenges.md#rewards)

要编辑现有的奖励提供者，请打开&#x200B;**[!UICONTROL 奖励提供者]**&#x200B;选项卡，选择提供者，并更新适当的字段。 更新子资源（奖励定义、代理、身份验证令牌生成器）时，将保存对子资源的更改。

>[!NOTE]
>
>**[!UICONTROL 自带数据]**&#x200B;挑战可通过您自己的数据集成完成奖励。 此处配置的奖励提供商不适用于这些挑战。 [了解如何创建您自己的数据挑战](create-challenges.md#create-the-challenge)

## 事件定义（可选） {#event-definitions}

**[!UICONTROL 事件定义]**&#x200B;将您系统中的体验事件（例如，购买、酒店签到）映射到忠诚度挑战可以执行的活动，最明显的是&#x200B;**[!UICONTROL 自定义事件]**&#x200B;任务。 当事件到达时，[!DNL Journey Optimizer]使用这些定义来决定是否处理它们。 忽略不符合任何定义的事件。

### 创建事件定义 {#create-event-definition}

1. 打开&#x200B;**[!UICONTROL 事件定义]**&#x200B;选项卡并创建新定义。

   ![](assets/admin-event-definition.png)

1. 输入事件的&#x200B;**[!UICONTROL 名称]**（例如，`Coffee purchase`） — 这是营销人员在配置&#x200B;**[!UICONTROL 自定义事件]**&#x200B;任务时看到的名称。

1. 指定[!DNL Journey Optimizer]如何识别传入负载中的事件。 提供&#x200B;**[!UICONTROL 标识符路径]**&#x200B;和/或&#x200B;**[!UICONTROL XDM架构ID]**：

   * **[!UICONTROL 标识符路径]** — 标识事件或成员的字段的路径（例如，`data.memberId`）。 当按有效负载中的值匹配事件时，请使用此项。
   * **[!UICONTROL 标识符值]** — 标识符路径上的值必须存在才能匹配此定义。
   * **[!UICONTROL XDM架构ID]** — 此事件类型的Experience Platform XDM架构的ID。 在根据已知架构捕获事件时，使用此选项。

1. 当品牌以自己的JSON格式发送事件时，请将字符串粘贴到&#x200B;**[!UICONTROL 架构]**&#x200B;和&#x200B;**[!UICONTROL 转换器]**&#x200B;中，这样[!DNL Journey Optimizer]就可以识别数据、解析数据并决定是否跟踪它。

   * **[!UICONTROL 架构]** — 传入有效负载的验证字符串。
   * **[!UICONTROL Transformer]** — 将有效负载映射到忠诚度挑战预期格式的转换表达式（例如，JSONata）。

1. 保存事件定义。 它出现在&#x200B;**[!UICONTROL 事件定义]**&#x200B;列表中。 您现在可以在挑战中使用它。 [了解如何创建挑战](create-challenges.md)

## 产品库存 {#product-inventory}

**[!UICONTROL 产品库存]**&#x200B;选项卡允许您对目录项进行分组，这样您便可以在任务中定位目录项，而无需列出每个项ID。 您上载了一个将每个项目标识符映射到一个或多个&#x200B;**产品组**&#x200B;的&#x200B;**CSV文件**（同一项目可以出现在多个组中）。 导入后，在配置任务资格时，这些组将可用。 [了解如何创建任务](create-tasks.md)

1. 准备一个CSV文件，以将每个项目标识符映射到一个或多个产品组。 展开以下部分以查看示例。

   +++产品库存CSV示例

   ![](assets/admin-inventory-csv.png)

   +++

1. 打开&#x200B;**[!UICONTROL 产品清单]**&#x200B;选项卡。

1. 单击&#x200B;**[!UICONTROL 上传]**&#x200B;按钮并选择您的CSV文件。

   ![](assets/admin-inventory-upload.png)

1. 在清单列表中查看导入的文件。 该列表每一项显示一行。 在&#x200B;**列中包含的**&#x200B;组中，您会看到该项所属的每个产品组。 每一组都显示为一种药丸（如果物品属于几组，则为数片）。

   ![](assets/admin-inventory-imported.png)

1. 要查看产品组中的每个项目，请在任意行上的&#x200B;**列中包含的**&#x200B;组中选择该组的药丸。 组详细信息视图会列出组中的所有项目，而不仅仅是选定行中的项目。

   ![](assets/admin-inventory-group.png)

1. 使用&#x200B;**[!UICONTROL 上载历史记录]**&#x200B;查看以前上载的CSV文件。

## 排除项 {#exclusions}

通过&#x200B;**[!UICONTROL 排除项]**&#x200B;选项卡，可定义在忠诚度计划中排除的目录项和组，而无需在每个任务中列出每个项ID。 您上载了一个将每个项目标识符映射到一个或多个&#x200B;**排除组**&#x200B;的&#x200B;**CSV文件**（同一项目可以出现在多个组中）。 导入后，这些项目和组在任务生成器中可用：排除的项目会自动标记，不能包含在任务中；只能将排除组添加到任务的排除列表，不能添加到包含列表。 [了解如何定义任务中的合格项目和排除项](create-tasks.md#eligible-items-exclusions)

1. 准备一个CSV文件以将每个项目标识符映射到一个或多个排除组。 展开以下部分以查看示例。

   +++排除项CSV示例

   ![](assets/admin-exclusions-csv.png)

   +++

1. 打开&#x200B;**[!UICONTROL 排除项]**&#x200B;选项卡。

1. 单击&#x200B;**[!UICONTROL 上传]**&#x200B;按钮并选择您的CSV文件。

   ![](assets/admin-exclusions-upload.png)

1. 查看排除项列表中的导入文件。 该列表每一项显示一行。 在&#x200B;**列中包含的**&#x200B;组中，您会看到项目所属的每个排除组。 每一组都显示为一种药丸（如果物品属于几组，则为数片）。

1. 要查看排除组中的每个项目，请在任意行上的&#x200B;**列中包含的**&#x200B;组中选择该组的药丸。 组详细信息视图会列出组中的所有项目，而不仅仅是选定行中的项目。

1. 使用&#x200B;**[!UICONTROL 上载历史记录]**&#x200B;查看以前上载的CSV文件。
