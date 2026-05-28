---
solution: Journey Optimizer
product: journey optimizer
title: 启用外部集成
description: 将外部集成集成集成到渠道创作流程中，以使用个性化和动态信息丰富内容
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: 集成
exl-id: 104f283e-f6a5-431b-919a-d97b83d19632
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
  - id: c08fcc42-2918-421a-a25e-e1bd9464c290
  - id: c6fdb8b1-45ee-460a-a859-9031c59118b7
  - id: d16f7424-4847-4b90-a37c-4b52cbdabee5
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1125
ht-degree: 8%

---

# 使用集成 {#external-sources}

## 概述

**集成**&#x200B;功能将Adobe Journey Optimizer链接到您已在其他位置管理其数据和可组合内容的第三方系统。 您可以在创作期间和发送时提供这些材料，从而为您在Journey Optimizer中使用的各个渠道提供响应更灵敏、个性化的体验。

您可以使用此功能访问外部数据，并从第三方工具中提取内容，例如：

* 来自忠诚度系统的&#x200B;**奖励积分**。
* 产品的&#x200B;**价格信息**。
* 来自推荐引擎的&#x200B;**产品推荐**。
* **物流更新**&#x200B;为交货状态。

要开始使用集成，需要向用户授予&#x200B;**[!UICONTROL 管理AJO集成配置]**&#x200B;和&#x200B;**[!UICONTROL 查看AJO集成配置]**&#x200B;权限。 [了解有关权限的更多信息](../administration/permissions.md)

+++ 了解如何分配集成相关权限

1. 在&#x200B;**[!UICONTROL 权限]**&#x200B;产品中，转到&#x200B;**[!UICONTROL 角色]**&#x200B;选项卡并选择所需的&#x200B;**[!UICONTROL 角色]**。

1. 单击&#x200B;**[!UICONTROL 编辑]**，修改权限。

1. 添加&#x200B;**[!UICONTROL AJO集成配置]**&#x200B;资源，然后从下拉菜单中选择相应的集成权限。

   ![](assets/external-integration-config-9.png)

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;以应用更改。

   任何已分配此角色的用户的权限都将自动更新。

1. 要将此角色分配给新用户，请导航到&#x200B;**[!UICONTROL 角色]**&#x200B;仪表板中的&#x200B;**[!UICONTROL 用户]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL 添加用户]**。

1. 输入用户名、电子邮件地址或从列表中选择，然后单击&#x200B;**[!UICONTROL 保存]**。

如果之前没有创建用户，请参阅[此文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/abac/permissions-ui/users)。

+++

## 配置集成 {#configure}

>[!AVAILABILITY]
>
> 此集成功能仅限出站渠道（电子邮件、短信和推送）并支持提取JSON或HTML。

作为管理员，您可以按照以下步骤设置外部集成：

1. 导航到左侧菜单中的&#x200B;**[!UICONTROL 配置]**&#x200B;部分，然后单击&#x200B;**[!UICONTROL 集成]**&#x200B;卡片中的&#x200B;**[!UICONTROL 管理]**。

   然后，单击&#x200B;**[!UICONTROL 创建集成]**&#x200B;以启动新配置。

   ![](assets/external-integration-config-1.png)

1. 或者，粘贴&#x200B;**cURL**&#x200B;命令以自动填充URL、HTTP方法、标头和查询参数。

1. 为您的集成提供&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

   >[!NOTE]
   >
   >**[!UICONTROL 名称]**&#x200B;字段不能包含空格。

1. 输入API终结点&#x200B;**[!UICONTROL URL]**。

   对于路径变量，在URL中用双大括号括起标签，例如`https://api.example.com/v1/products/{{productId}}`，然后在&#x200B;**[!UICONTROL 路径模板]**&#x200B;中设置每个占位符。

1. 为您在URL中添加的每个占位符配置&#x200B;**[!UICONTROL 路径模板]**&#x200B;的&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 默认值]**。

   请注意，**[!UICONTROL Name]**&#x200B;仅在编辑器中是面向营销人员的标签，不会通过API请求发送。

   ![](assets/external-integration-config-2.png)

1. 选择GET与POST之间的&#x200B;**[!UICONTROL HTTP方法]**。

1. 根据集成需要，单击&#x200B;**[!UICONTROL 添加标头]**&#x200B;和/或&#x200B;**[!UICONTROL 添加查询参数]**。 对于每个参数，提供以下详细信息：

   * **[!UICONTROL 参数]**： API所需的实际标头或查询参数名称。

   * **[!UICONTROL 名称]**：此参数的营销人员友好标签，作者在营销活动中映射值时选择它。

   * **[!UICONTROL 类型]**：为固定值选择&#x200B;**常量**，为动态输入选择&#x200B;**变量**。

   * **[!UICONTROL 值]**：直接输入常量的值，或选择变量映射。

   * **[!UICONTROL 必需]**：指定此参数是否为必需。 对于必需&#x200B;**[!UICONTROL 变量]**&#x200B;参数，如果未在运行时解析任何值并且未提供默认值，则生成请求将失败并出现错误，并且不会进行出站API调用。

   ![](assets/external-integration-config-3.png)

1. 选择&#x200B;**[!UICONTROL 身份验证类型]**：

   * **[!UICONTROL 无身份验证]**：适用于不需要任何凭据的开放API。

   * **[!UICONTROL API密钥]**：使用静态API密钥对请求进行身份验证。 输入您的&#x200B;**[!UICONTROL API密钥名称{1&#x200B;}、**&#x200B;[!UICONTROL &#x200B; API密钥值{3&#x200B;}并指定您的&#x200B;**[!UICONTROL 位置]**。]&#x200B;**]**

   * **[!UICONTROL 基本身份验证]**：使用标准HTTP基本身份验证。 输入&#x200B;**[!UICONTROL 用户名]**&#x200B;和&#x200B;**[!UICONTROL 密码]**。

   * **[!UICONTROL OAuth 2.0]**：使用OAuth 2.0协议进行身份验证。 单击![编辑](assets/do-not-localize/Smock_Edit_18_N.svg)图标以配置或更新&#x200B;**[!UICONTROL 有效负载]**。

   ![](assets/external-integration-config-4.png)

1. 为API请求设置&#x200B;**[!UICONTROL 策略配置]**，如&#x200B;**[!UICONTROL 超时]**&#x200B;段，并选择启用限制、缓存和/或重试。

   >[!NOTE]
   >
   >启用限制后，支持的速率为50到5000 TPS。 限制适用于&#x200B;**集成**，而不适用于每个API终结点。
   >
   >启用重试后，默认情况下其他失败将重试&#x200B;**3**&#x200B;次，每次尝试之间有&#x200B;**200毫秒**、**400毫秒**&#x200B;和&#x200B;**800毫秒**。

1. 使用&#x200B;**[!UICONTROL 响应有效负载]**&#x200B;字段，您可以决定示例输出的哪些字段需要用于消息个性化。

   单击![编辑](assets/do-not-localize/Smock_Edit_18_N.svg)图标并粘贴示例JSON响应有效负载以自动检测数据类型。

1. 选择要为个性化显示的字段并指定其相应的数据类型。

   ![](assets/external-integration-config-5.png)

   >[!NOTE]
   >
   >**[!UICONTROL 响应有效负载]**&#x200B;配置定义了用于创作的预期响应，包括在该步骤中应用的任何架构。 营销人员只能引用公开的字段，其他路径的令牌无法在编辑器中验证。

1. 使用&#x200B;**[!UICONTROL 发送测试连接]**&#x200B;来验证集成。 [了解有关如何测试连接的更多信息](#connection)

   验证后，单击&#x200B;**[!UICONTROL 激活]**。

1. 访问新创建的集成，以：

   * **更新**：仅更改&#x200B;**身份验证**&#x200B;详细信息和&#x200B;**策略配置**。 更新适用于实时历程和营销活动。 在保存更改之前，请使用&#x200B;**[!UICONTROL 浏览引用]**&#x200B;菜单确认集成的使用位置。
   * **存档**：存档集成配置。

   ![](assets/external-integration-config-7.png)

激活后，单击![高级菜单](assets/do-not-localize/Smock_More_18_N.svg)图标以访问&#x200B;**[!UICONTROL 浏览引用]**&#x200B;菜单，并查看此配置的使用情况，包括依赖此配置的历程和营销活动。

![](assets/external-integration-config-6.png)

### 发送时间限制和行为 {#configure-send-time}

在发送时，来自外部API的响应默认可能高达&#x200B;**4 MB**。 任何较大的都被视为集成错误，当失败是由响应大小引起时，不尝试&#x200B;**重试**。

调用遵循您配置的&#x200B;**限制**&#x200B;速率：即使外部系统关闭或返回错误，Journey Optimizer仍会计划尝试达到该限制。 如果启用了&#x200B;**缓存**，则只存储&#x200B;**成功的**&#x200B;响应并重复使用，直到您定义的缓存&#x200B;**TTL**&#x200B;过期；从不缓存失败的响应。

每个排队消息还带有有效窗口(TTL)。 如果处理延迟，并且消息位于该窗口之外，则系统&#x200B;**丢弃该窗口**&#x200B;并发出一个&#x200B;**`MessageValidityExclusion`**&#x200B;事件，以便从队列中清除旧工作并保持资源可用。

## 测试您的连接 {#connection}

**[!UICONTROL 发送测试连接]**&#x200B;在激活之前针对目标API验证端点URL、身份验证和请求结构，这降低了消息处理期间运行时失败的风险。

1. 定义URL、HTTP方法、标头和查询参数后，单击&#x200B;**[!UICONTROL 发送测试连接]**&#x200B;以运行连接测试并确认配置。

1. 在&#x200B;**[!UICONTROL 发送测试连接]**&#x200B;对话框中，为URL路径、标头和查询参数中的任意&#x200B;**[!UICONTROL 变量]**&#x200B;占位符输入默认值。

   这些值包含在测试请求中。 Journey Optimizer会调用端点并报告连接是成功还是失败。

   ![](assets/external-integration-config-11.png)

1. 如果测试返回了成功的响应，请选择&#x200B;**[!UICONTROL 用作响应有效负载]**&#x200B;以将响应正文复制到&#x200B;**[!UICONTROL 响应有效负载]**&#x200B;字段中，请参阅[配置集成](#configure)中的步骤10，其中可检测到数据类型并可选择字段进行个性化。

   ![](assets/external-integration-config-10.png)

1. 如果测试未成功，请展开&#x200B;**[!UICONTROL 错误]**&#x200B;下拉列表以查看失败详细信息，根据需要更新集成配置，然后再次运行&#x200B;**[!UICONTROL 发送测试连接]**。

   ![](assets/external-integration-content-12.png)

测试成功后，在集成配置中选择&#x200B;**[!UICONTROL 激活]**。 请参阅[配置集成](#configure)。

