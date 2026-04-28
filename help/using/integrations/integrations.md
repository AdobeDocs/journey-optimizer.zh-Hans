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
hide: true
exl-id: 104f283e-f6a5-431b-919a-d97b83d19632
source-git-commit: f40e030e7d14120cdbc118a8f93e2f752d713f6b
workflow-type: tm+mt
source-wordcount: '1227'
ht-degree: 7%

---

# 使用集成 {#external-sources}

>[!BEGINSHADEBOX]

目录：

* **[使用集成](integrations.md)**
* [快速入门](vendor-integration-gs.md)
* [可用的供应商](vendor-integration.md)
* [常见问题解答](vendor-integration-faq.md)

>[!ENDSHADEBOX]

## 概述

**集成**&#x200B;功能将Adobe Journey Optimizer链接到您已在其他位置管理其数据和可组合内容的第三方系统。 您可以在创作期间和发送时提供这些材料，从而为您在Journey Optimizer中使用的各个渠道提供响应更灵敏、个性化的体验。

您可以使用此功能访问外部数据，并从第三方工具中提取内容，例如：

* 来自忠诚度系统的&#x200B;**奖励积分**。
* 产品的&#x200B;**价格信息**。
* 来自推荐引擎的&#x200B;**产品推荐**。
* **物流更新**&#x200B;为交货状态。

要开始使用集成，需要向用户授予&#x200B;**[!UICONTROL 管理AJO集成配置]**&#x200B;和&#x200B;**[!UICONTROL 查看AJO集成]**&#x200B;权限。 [了解有关权限的更多信息](../administration/permissions.md)

+++ 了解如何分配集成相关权限

1. 在&#x200B;**[!UICONTROL 权限]**&#x200B;产品中，转到&#x200B;**[!UICONTROL 角色]**&#x200B;选项卡并选择所需的&#x200B;**[!UICONTROL 角色]**。

1. 单击&#x200B;**[!UICONTROL 编辑]**，修改权限。

1. 添加&#x200B;**[!UICONTROL AJO集成配置]**&#x200B;资源，然后从下拉菜单中选择相应的集成权限。

   ![](assets/external-integration-config-9.png)

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;以应用更改。

   任何已分配此角色的用户的权限都将自动更新。

1. 要将此角色分配给新用户，请导航到&#x200B;**[!UICONTROL 角色]**&#x200B;仪表板中的&#x200B;**[!UICONTROL 用户]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL 添加用户]**。

1. 输入用户名、电子邮件地址或从列表中选择，然后单击&#x200B;**[!UICONTROL 保存]**。

如果之前未创建用户，请参阅[此文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/abac/permissions-ui/users)。

+++

## 配置集成 {#configure}

>[!AVAILABILITY]
>
> 此集成功能仅限出站渠道（电子邮件、短信和推送），并提供JSON或HTML格式的数据。 请注意，API是只读的，仅支持检索操作。

作为管理员，您可以按照以下步骤设置外部集成：

1. 导航到左侧菜单中的&#x200B;**[!UICONTROL 配置]**&#x200B;部分，然后单击&#x200B;**[!UICONTROL 集成]**&#x200B;卡片中的&#x200B;**[!UICONTROL 管理]**。

   然后，单击&#x200B;**[!UICONTROL 创建集成]**&#x200B;以启动新配置。

   ![](assets/external-integration-config-1.png)

1. 或者，粘贴&#x200B;**cURL**&#x200B;命令以自动填充URL、HTTP方法、标头和查询参数。

1. 为您的集成提供&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

   >[!NOTE]
   >
   >这些字段不能包含空格。

1. 输入API终结点&#x200B;**[!UICONTROL URL]**，该终结点可能包含路径参数以及可使用标签和默认值定义的变量。

1. 使用&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 默认值]**&#x200B;配置&#x200B;**[!UICONTROL 路径模板]**。

   ![](assets/external-integration-config-2.png)

1. 选择GET与POST之间的&#x200B;**[!UICONTROL HTTP方法]**。

1. 根据集成需要，单击&#x200B;**[!UICONTROL 添加标头]**&#x200B;和/或&#x200B;**[!UICONTROL 添加查询参数]**。 对于每个参数，提供以下详细信息：

   * **[!UICONTROL 参数]**：：内部用于引用该参数的唯一标识符。

   * **[!UICONTROL 名称]**： API所预期的参数的实际名称。

   * **[!UICONTROL 类型]**：为固定值选择&#x200B;**常量**，为动态输入选择&#x200B;**变量**。

   * **[!UICONTROL 值]**：直接输入常量的值，或选择变量映射。

   * **[!UICONTROL 必需]**：指定此参数是否为必需。

   ![](assets/external-integration-config-3.png)

1. 选择&#x200B;**[!UICONTROL 身份验证类型]**：

   * **[!UICONTROL 无身份验证]**：适用于不需要任何凭据的开放API。

   * **[!UICONTROL API密钥]**：使用静态API密钥对请求进行身份验证。 输入您的&#x200B;**[!UICONTROL API密钥名称{1&#x200B;}、**&#x200B;[!UICONTROL &#x200B; API密钥值{3&#x200B;}并指定您的&#x200B;**[!UICONTROL 位置]**。]&#x200B;**]**

   * **[!UICONTROL 基本身份验证]**：使用标准HTTP基本身份验证。 输入&#x200B;**[!UICONTROL 用户名]**&#x200B;和&#x200B;**[!UICONTROL 密码]**。

   * **[!UICONTROL OAuth 2.0]**：使用OAuth 2.0协议进行身份验证。 单击![编辑](assets/do-not-localize/Smock_Edit_18_N.svg)图标以配置或更新&#x200B;**[!UICONTROL 有效负载]**。

   ![](assets/external-integration-config-4.png)

1. 为API请求设置&#x200B;**[!UICONTROL 策略配置]**，如&#x200B;**[!UICONTROL 超时]**&#x200B;段，并选择启用限制、缓存和/或重试。

   启用限制时，支持的速率范围从&#x200B;**50** TPS （最小）到&#x200B;**5000** TPS （最大）。
启用重试后，其他失败将默认遵循&#x200B;**3**&#x200B;次重试，在连续尝试之间有&#x200B;**200毫秒**、**400毫秒**&#x200B;和&#x200B;**800毫秒**。

1. 使用&#x200B;**[!UICONTROL 响应有效负载]**&#x200B;字段，您可以决定示例输出的哪些字段需要用于消息个性化。

   单击![编辑](assets/do-not-localize/Smock_Edit_18_N.svg)图标并粘贴示例JSON响应有效负载以自动检测数据类型。

1. 选择要为个性化显示的字段并指定其相应的数据类型。

   ![](assets/external-integration-config-5.png)

   >[!NOTE]
   >
   >The **[!UICONTROL Response payload]** configuration defines the expected response for authoring including any schema applied in that step. Marketers may reference only exposed fields, tokens for other paths fail validation in the editor.

1. 使用&#x200B;**[!UICONTROL 发送测试连接]**&#x200B;来验证集成。

   验证后，单击&#x200B;**[!UICONTROL 激活]**。

### 发送时间限制和行为 {#configure-send-time}

在发送时，来自外部API的响应默认可能高达&#x200B;**4 MB**。 任何较大的都被视为集成错误，当失败是由响应大小引起时，不尝试&#x200B;**重试**。

调用遵循您配置的&#x200B;**限制**&#x200B;速率：即使外部系统关闭或返回错误，Journey Optimizer仍会计划尝试达到该限制。 如果启用了&#x200B;**缓存**，则只存储&#x200B;**成功的**&#x200B;响应并重复使用，直到您定义的缓存&#x200B;**TTL**&#x200B;过期；从不缓存失败的响应。

每个排队消息还带有有效窗口(TTL)。 如果处理延迟，并且消息位于该窗口之外，则系统&#x200B;**丢弃该窗口**&#x200B;并发出一个&#x200B;**`MessageValidityExclusion`**&#x200B;事件，以便从队列中清除旧工作并保持资源可用。


## 使用外部集成进行个性化 {#personalization}

Before you use external integrations for personalization, note that the scheduling and isolation of integration calls depend on execution context:

* **Batch execution** (batch campaigns, orchestrated campaigns, and API-triggered marketing campaigns): each batch run operates in a dedicated, isolated environment. Concurrent batch executions that call external systems therefore do not contend with or obstruct one another.

* **Unitary execution** (unitary journeys, batch journeys, and API-triggered transactional campaigns): integration traffic is isolated per brand sandbox, so a slow external API for one brand does not delay another. Within your sandbox, concurrent integrations can briefly delay other integration-backed messages; each message is attempted for up to 12 hours before expiration.

作为营销人员，您可以使用配置的集成来个性化您的内容。 执行以下步骤：

1. 访问您的营销活动内容，然后单击文本或HTML **[!UICONTROL 组件]**&#x200B;中的&#x200B;**[!UICONTROL 添加个性化]**。

   [了解有关组件的更多信息](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. 导航到&#x200B;**[!UICONTROL 集成]**&#x200B;部分，然后单击&#x200B;**[!UICONTROL 打开集成]**&#x200B;以查看所有活动的集成。

   请注意，内容片段在集成中可用，但仅支持出站渠道，入站发布将不会成功。 片段发布后，将禁用添加和保存新集成，以避免对现有历程和营销活动造成影响。

   ![](assets/external-integration-content-2.png)

1. 选择集成并单击&#x200B;**[!UICONTROL 保存]**。

   ![](assets/external-integration-content-3.png)

1. 启用&#x200B;**[!UICONTROL Pills]**&#x200B;模式以解锁高级集成菜单。

   ![](assets/external-integration-content-4.png)

1. 当您创作集成个性化时，集成帮助程序包含一个&#x200B;**`required`**&#x200B;字段，该字段定义失败或缺少数据与默认内容的交互方式：

   * **`required=true`** （默认）：该消息的渲染停止。 发送被排除在&#x200B;**`ExternalDataLookupExclusion`**&#x200B;之外，该排除记录在&#x200B;**消息反馈数据集**&#x200B;中。
   * **`required=false`**：结果变量设置为&#x200B;**`null`**，并继续渲染。 在模板中使用默认文本、回退或条件逻辑，以便在集成不返回数据时，配置文件不会接收空内容。

     ![](assets/external-integration-content-8.png)

1. 要完成集成设置，请定义集成属性，这些属性先前在[配置](#configure)期间指定。

   可以使用静态值（保持常量）或配置文件属性（动态地从用户配置文件中提取信息）为这些属性分配值。

   ![](assets/external-integration-content-5.png)

1. 定义集成属性后，您现在可以通过单击![添加](assets/do-not-localize/Smock_Add_18_N.svg)图标，将内容中的集成字段用于个性化消息传递。

   ![](assets/external-integration-content-6.png)

   >[!NOTE]
   >
   >模板中的令牌必须仅使用管理员在集成配置中公开的字段。 例如，`{{weatherResponse.temperature}}`在`temperature`公开时有效；如果`humidity`未公开，则`{{weatherResponse.humidity}}`在编辑器中被拒绝。

1. 单击&#x200B;**[!UICONTROL 保存]**。

您的集成个性化现在已成功应用于您的内容，确保每位收件人都能根据您配置的属性获得量身定制的相关体验。

![](assets/external-integration-content-7.png)

