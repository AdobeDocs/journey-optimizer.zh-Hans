---
solution: Journey Optimizer
product: journey optimizer
title: 配置忠诚度计划
description: 了解如何在Adobe [!DNL Journey Optimizer]中为您的忠诚度计划配置奖励提供商、事件定义、产品清单、排除和组织级别的设置。
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="私人测试版" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: 9383220dd57f6a3ebfe67d0d1081b8834b524293
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 1%

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

## 概述 {#access-loyalty-admin}

忠诚度计划配置通过在营销人员提出挑战之前设置奖励履行、事件映射、产品库存和排除项，将[!DNL Journey Optimizer]连接到您的外部忠诚度系统。

>[!NOTE]
>
>除了忠诚度挑战所需的权限之外，忠诚度计划配置还需要对您的[!DNL Journey Optimizer]实例具有管理员访问权限。 要获取访问权限，请与Adobe管理员联系。

要打开配置界面，请导航到&#x200B;**[!UICONTROL 忠诚度]**&#x200B;并选择&#x200B;**[!UICONTROL 忠诚管理员]**。 该界面将组织为选项卡：

* **全局设置** — 为您的项目选择Experience Platform标识命名空间。 [了解如何配置全局设置](#global-settings)
* **奖励提供商** — 连接可在客户取得进展或完成挑战时提供奖励的API。 [了解如何配置奖励提供商](#reward-providers)
* **事件定义** — 将传入体验事件映射到&#x200B;**[!UICONTROL 自定义AEP事件]**&#x200B;任务中使用的活动。 [了解如何配置事件定义](#event-definitions)
* **产品库存** — 上传项目到组的映射，以供在任务资格规则中使用。 [了解如何配置产品清单](#product-inventory)
* **排除项** — 上传用于任务配置的组织范围项和组排除项。 [了解如何配置排除项](#exclusions)

## 全局设置 {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="全局设置"
>abstract="为您的忠诚度计划选择Adobe Experience Platform身份命名空间。"

打开&#x200B;**[!UICONTROL 全局设置]**&#x200B;选项卡，并在&#x200B;**[!UICONTROL 命名空间]**&#x200B;下拉列表中为您的忠诚度计划选择Adobe Experience Platform [身份命名空间](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/namespaces)。 此命名空间必须匹配在您的数据中标识成员配置文件的方式。

![](assets/admin-global-settings.png)

➡️ [了解如何使用身份命名空间](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/namespaces){target="_blank"}

## 奖励提供者 {#reward-providers}

**奖励提供商**&#x200B;告知[!DNL Journey Optimizer]在记录质询进度或完成质询时发送完成调用的位置。 例如，将会员积分或开始积分到会员帐户的API。

要创建奖励提供者，请执行以下步骤：

1. 打开&#x200B;**[!UICONTROL 奖励提供者]**&#x200B;选项卡并选择&#x200B;**[!UICONTROL 创建奖励提供者]**。

   ![](assets/admin-reward.png)

1. 输入&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

1. 在&#x200B;**[!UICONTROL URL]**&#x200B;字段中，输入接收履行请求的API终结点。

1. 根据需要为API添加&#x200B;**[!UICONTROL 标头]**（例如，API密钥或内容类型）。

1. 配置与奖励提供商关联的资源。 展开以下每个部分以获取字段详细信息：

   +++奖励定义

   为您的提供商支持的每种奖励类型（例如，计划积分、星级或货币信用）添加一个条目。 对于每个定义：

   * 输入&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。
   * 指定定义是否为&#x200B;**[!UICONTROL 已启用]**。
   * 切换&#x200B;**[!UICONTROL Default]**&#x200B;以将一个定义标记为此提供程序的默认值。
   * 定义随履行调用发送的&#x200B;**有效负载**。

   ![](assets/admin-reward-definition.png)

   +++

   +++奖励代理

   通过中间服务器路由完成调用，而不是将其直接发送到您的端点。 在奖励提供程序和&#x200B;**[!UICONTROL 创建代理]**&#x200B;屏幕上，使用&#x200B;**[!UICONTROL 凭据]**&#x200B;字段进行代理身份验证。

   * 输入&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。
   * 输入&#x200B;**[!UICONTROL 主机]**&#x200B;和&#x200B;**[!UICONTROL 端口]**。
   * 指定代理是否为&#x200B;**[!UICONTROL 已启用]**。
   * 在&#x200B;**[!UICONTROL 凭据]**&#x200B;中，以JSON格式输入代理用户名和密码。 凭据值通常如下所示：

     ```json
     { "userName": "test", "password": "xxxx" }
     ```

   ![](assets/admin-reward-proxies.png)

   +++

   +++身份验证令牌生成器

   当API需要持有者令牌或类似身份验证时使用。

   * 输入&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。
   * 在&#x200B;**[!UICONTROL 身份验证类型]**&#x200B;中，输入身份验证类型（例如，持有者）。
   * 选择HTTP方法（例如，POST）。
   * 输入响应中的令牌终结点URL和&#x200B;**[!UICONTROL 令牌键]**（例如，`access_token`）。
   * 指定身份验证令牌生成器是否为&#x200B;**[!UICONTROL 已启用]**。
   * 添加令牌端点所需的任何标头。

   [!DNL Journey Optimizer]使用此配置在每次调用奖励API之前获取新的令牌。

   ![](assets/admin-reward-auth.png)

   +++

1. 选择&#x200B;**[!UICONTROL 创建奖励提供程序]**。 提供程序与所有配置的资源一起保存。

保存后，该提供商将显示在奖励提供商列表中。 营销人员可以在配置挑战奖励时选择它。 [了解如何配置挑战奖励](create-challenges.md#rewards)

要编辑奖励提供者，请打开&#x200B;**[!UICONTROL 奖励提供者]**&#x200B;选项卡，选择提供者，并更新适当的字段。 对奖励定义、代理和身份验证令牌生成器的更改会在您更新时自动保存。

>[!NOTE]
>
>**[!UICONTROL 自带数据]**&#x200B;挑战可通过您自己的数据集成完成奖励。 此处配置的奖励提供商不适用于这些挑战。 [了解如何创建您自己的数据挑战](create-challenges.md#create-the-challenge)

## 事件定义 {#event-definitions}

**[!UICONTROL 事件定义]**&#x200B;告知[!DNL Journey Optimizer]要处理的传入Adobe Experience Platform体验事件。 例如，购买或入住酒店。 营销人员在创建&#x200B;**[!UICONTROL 自定义AEP事件]**&#x200B;任务时引用这些定义。 忽略不符合任何定义的事件。

当您的组织以自己的JSON格式发送事件时，**[!UICONTROL 架构]**&#x200B;和&#x200B;**[!UICONTROL 转换器]**&#x200B;帮助[!DNL Journey Optimizer]验证有效负载、解析有效负载并决定是否跟踪活动。

要创建事件定义，请执行以下步骤：

1. 打开&#x200B;**[!UICONTROL 事件定义]**&#x200B;选项卡并创建新定义。

   ![](assets/admin-event-definition.png)

1. 输入事件的&#x200B;**[!UICONTROL Name]**（例如，`Coffee purchase`）。 营销人员在配置&#x200B;**[!UICONTROL 自定义AEP事件]**&#x200B;任务时看到此名称。

1. 指定[!DNL Journey Optimizer]如何识别传入负载中的事件。 提供&#x200B;**[!UICONTROL 标识符路径]**&#x200B;和/或&#x200B;**[!UICONTROL XDM架构ID]**：

   * **[!UICONTROL 标识符路径]** — 有效负载中字段的路径（例如，`data.memberId`）。 当按有效负载中的值匹配事件时，请使用此项。
   * **[!UICONTROL 标识符值]** — 标识符路径上的值必须存在才能匹配此定义。
   * **[!UICONTROL XDM架构ID]** — 此事件类型的Experience Platform XDM架构的ID。 在根据已知架构捕获事件时，使用此选项。

1. 如果需要，请将字符串粘贴到&#x200B;**[!UICONTROL 架构]**&#x200B;和&#x200B;**[!UICONTROL 转换器]**&#x200B;中：

   * **[!UICONTROL 架构]** — 传入有效负载的验证字符串。
   * **[!UICONTROL Transformer]** — 将有效负载映射到忠诚度挑战预期格式的转换表达式（例如，JSONata）。

1. 保存事件定义。 它显示在&#x200B;**[!UICONTROL 事件定义]**&#x200B;列表中，并在营销人员创建&#x200B;**[!UICONTROL 自定义AEP事件]**&#x200B;任务时可用。 [了解如何创建任务](create-tasks.md#choose-activity)

## 产品库存 {#product-inventory}

**[!UICONTROL 产品库存]**&#x200B;选项卡将目录项分组，以便营销人员可以在任务中定位它们，而无需输入每个项ID。 上载将每个项目标识符映射到一个或多个&#x200B;**产品组**&#x200B;的&#x200B;**CSV文件**（同一项目可以属于多个组）。 配置任务资格时，导入的组可用。 [了解如何创建任务](create-tasks.md)

要上传产品清单文件，请执行以下步骤：

1. 准备一个CSV文件，以将每个项目标识符映射到一个或多个产品组。 展开以下部分以查看示例。

   +++产品库存CSV示例

   ![](assets/admin-inventory-csv.png)

   +++

1. 打开&#x200B;**[!UICONTROL 产品清单]**&#x200B;选项卡。

1. 选择&#x200B;**[!UICONTROL 上传]**&#x200B;并选择您的CSV文件。

   ![](assets/admin-inventory-upload.png)

1. 查看清单列表中的导入数据。 该列表每一项显示一行。 **列中包含的**&#x200B;组将该项目的每个产品组显示为Pillar，或者当该项目属于多个组时显示多个Pills。

   ![](assets/admin-inventory-imported.png)

1. 要查看产品组中的所有项目，请在任意行上的&#x200B;**列中包含的**&#x200B;组中选择该组的药丸。 组详细信息视图列出组中的每个项目。

   ![](assets/admin-inventory-group.png)

1. 打开&#x200B;**[!UICONTROL 上载历史记录]**&#x200B;以查看以前的CSV上载。

## 排除项 {#exclusions}

**[!UICONTROL 排除项]**&#x200B;选项卡定义在项目范围内排除的目录项和组，因此营销人员不必在每个任务上列出相同的排除项。 上载将每个项目标识符映射到一个或多个&#x200B;**排除组**&#x200B;的&#x200B;**CSV文件**（同一项目可以属于多个组）。

导入后，当营销人员配置&#x200B;**[!UICONTROL 符合条件的项目和排除项]**&#x200B;时，排除的项目和组将显示在任务生成器中。 [了解如何定义任务中的合格项目和排除项](create-tasks.md#eligible-items-exclusions)

要上传排除项，请执行以下步骤：

1. 准备一个CSV文件以将每个项目标识符映射到一个或多个排除组。 展开以下部分以查看示例。

   +++排除项CSV示例

   ![](assets/admin-exclusions-csv.png)

   +++

1. 打开&#x200B;**[!UICONTROL 排除项]**&#x200B;选项卡。

1. 选择&#x200B;**[!UICONTROL 上传]**&#x200B;并选择您的CSV文件。

   ![](assets/admin-exclusions-upload.png)

1. 查看排除项列表中的导入数据。 该列表每一项显示一行。 **列中包含的**&#x200B;组将该项目的每个排除组显示为Pillar，如果该项目属于多个组，则显示多个Pills。

<!-- SCREENSHOT: Exclusions list after CSV upload -->

1. 要查看排除组中的所有项目，请在任意行上的&#x200B;**列中包含的**&#x200B;组中选择该组的药丸。 组详细信息视图列出组中的每个项目。

<!-- SCREENSHOT: Exclusion group details -->

1. 打开&#x200B;**[!UICONTROL 上载历史记录]**&#x200B;以查看以前的CSV上载。
