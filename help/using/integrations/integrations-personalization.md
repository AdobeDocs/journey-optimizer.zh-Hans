---
solution: Journey Optimizer
product: journey optimizer
title: 使用外部集成
description: 将外部集成集成集成到渠道创作流程中，以使用个性化和动态信息丰富内容
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: 集成
source-git-commit: c5defc4940043753ff6c4e27d2ebafc807f8c9ba
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---


# 使用外部集成进行个性化 {#integrations-personalization}

在内容中使用外部集成之前，请确认管理员已&#x200B;**配置和激活**&#x200B;每个集成（端点、身份验证、策略、响应有效负载和激活），如[使用集成](integrations.md)中所述。

您最多可以为消息中的每个&#x200B;**[!UICONTROL 片段]**&#x200B;添加&#x200B;**3**&#x200B;个集成，最多添加&#x200B;**5**&#x200B;个集成。 仅来自片段的集成不计入&#x200B;**5**。

## 将集成个性化应用于您的内容 {#apply-integration-personalization}

作为营销人员，您可以使用配置的集成来个性化您的内容。 执行以下步骤：

1. 访问您的营销活动内容，然后单击文本或HTML **[!UICONTROL 组件]**&#x200B;中的&#x200B;**[!UICONTROL 添加个性化]**。

   [了解有关组件的更多信息](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. 导航到&#x200B;**[!UICONTROL 集成]**&#x200B;部分，然后单击&#x200B;**[!UICONTROL 打开集成]**&#x200B;以查看所有活动的集成。

   请注意，**Journey Optimizer片段**&#x200B;可与集成一起使用，但仅支持出站渠道。 片段发布后，将禁用添加和保存新集成，以避免对现有历程和营销活动造成影响。

   ![](assets/external-integration-content-2.png)

1. 选择集成并单击&#x200B;**[!UICONTROL 保存]**。

   ![](assets/external-integration-content-3.png)

1. 启用&#x200B;**[!UICONTROL Pills]**&#x200B;模式以解锁高级集成菜单。

   ![](assets/external-integration-content-4.png)

1. 当您创作集成个性化时，集成帮助程序包含一个&#x200B;**`required`**&#x200B;字段，该字段定义失败或缺少数据与默认内容的交互方式：

   * **`required=true`** （默认）：该消息的渲染停止。 发送被排除在&#x200B;**`ExternalDataLookupExclusion`**&#x200B;之外，该排除记录在&#x200B;**消息反馈数据集**&#x200B;中。
   * **`required=false`**：结果变量设置为&#x200B;**`null`**，并继续渲染。 在模板中使用默认文本、回退或条件逻辑，以便在集成不返回数据时，配置文件不会接收空内容。

     ![](assets/external-integration-content-8.png)

1. 要完成集成设置，请定义集成属性，这些属性先前在[配置](integrations.md#configure)期间指定。

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

## 将一个API调用映射到另一个调用 {#map-integration-chain}

您可以链接集成，以便一个调用的结果馈送下一个调用，例如路径区段、标题或查询参数。 这些调用在同一消息中按顺序运行，这支持更丰富的个性化，而无需自定义代码。

在开始之前，请确保：

* 管理员已配置并激活您所需的每个集成。 请参阅[配置集成](integrations.md)。
* 变量路径占位符、标头和查询参数是在集成配置中设置的，带有面向营销人员的标签。
* 管理员在每个集成的&#x200B;**[!UICONTROL 响应有效负载]**&#x200B;中显示了所需的响应字段，以便在创作时显示。

以下示例使用从用户档案的预订中返回航班号的预订集成，然后使用该号码作为实时状态（延迟、目的地）的航班信息集成。 将第二个集成的输入映射到第一个调用的响应。

1. 打开您的消息或片段，然后打开个性化编辑器。

   ![](assets/uc-integrations-1.png)

1. 在&#x200B;**[!UICONTROL 集成]**&#x200B;中，单击&#x200B;**[!UICONTROL 打开集成]**。

   ![](assets/uc-integrations-2.png)

1. 添加其响应将馈送下次调用的集成，例如，包含航班标识符的预订或预订数据。

   ![](assets/uc-integrations-3.png)

1. （可选）如果要将命名变量绑定到保留响应，请打开&#x200B;**[!UICONTROL 帮助程序函数]**&#x200B;菜单并添加一个帮助程序，例如`Let`函数。

   >[!NOTE]
   >
   > 仅管理员定义的&#x200B;**[!UICONTROL 响应有效负载]**&#x200B;中公开的字段可用。 您无法引用配置中未公开的属性。

1. 如果使用辅助变量，请将该变量映射到预订集成返回以供下游使用的字段，例如，乘客或预订有效负荷中的航班号。

   ![](assets/uc-integrations-4.png)

1. 从&#x200B;**[!UICONTROL 打开集成]**&#x200B;菜单中，添加第二个集成，例如航班状态。

   ![](assets/uc-integrations-5.png)

1. 在第二个集成中，打开&#x200B;**[!UICONTROL 集成属性]**。 对于必须重复使用来自第一次调用的数据的每个输入（如路径变量、标题或查询参数），请从第一次集成响应中选择映射源。

   在&#x200B;**[!UICONTROL Pills]**&#x200B;体验中，您可以将第一次调用输出直接映射到第二次调用输入，而无需使用`Let`语句。 如果您使用`Let`，则可以通过该变量进行映射。

   ![](assets/uc-integrations-6.png)

1. 使用![添加](assets/do-not-localize/Smock_Add_18_N.svg)控件将第二次集成的令牌插入到您的内容中，例如从航班信息响应插入目标。

   ![](assets/uc-integrations-8.png)

1. 保存您的内容。

在&#x200B;**[!UICONTROL 模拟]**&#x200B;或发送上，Journey Optimizer按顺序运行集成：第一次调用使用您配置的配置文件上下文，其结果构建第二个请求。 给定的集成是在模拟时运行还是在发送时运行，取决于您的设置和渠道。

![](assets/uc-integrations-7.png)

## 操作方法视频 {#video}

此视频展示了&#x200B;**集成**&#x200B;如何将Adobe Journey Optimizer连接到外部API，以便您可以将实时数据和内容提取到&#x200B;**出站**&#x200B;渠道、电子邮件、短信和推送，以进行更相关的个性化。

>[!VIDEO](https://video.tv.adobe.com/v/3484118/?learn=on)
