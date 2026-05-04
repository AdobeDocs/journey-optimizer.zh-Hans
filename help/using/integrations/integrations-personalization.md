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
source-git-commit: 4cc3c959fe08c1d574a5d041bf7721441bc96f97
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 1%

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

<!--

## Map one API call to another {#map-integration-chain}

You can **chain** integrations so that values returned by one active integration drive the inputs (path, headers, or query parameters) of another. That lets you build a real-time data flow in a single message without custom code.

Before you start, make sure that:

* An administrator has configured and activated every integration you need. See [Configure your Integration](integrations.md).
* Variable path placeholders, headers, and query parameters are set up in the integration configuration with marketer-facing labels.
* The administrator exposed the response fields you need in each integration's **[!UICONTROL Response payload]** so they appear when authoring.

In the below example, a reservation system integration returns a flight booking reference from the profile context. A separate flight-information integration expects that reference as a **path variable**. In the personalization editor, you map the second integration's variable to a field from the first integration's response, instead of a static value or profile attribute alone.

1. Open your message or fragment and place the cursor where you want personalized content (for example, a **[!UICONTROL Text]** field).

1. Open the personalization editor and go to **[!UICONTROL Integrations]** → **[!UICONTROL Open integrations]**.

1. Select the integration whose output will supply the downstream input (in the example, the reservation or profile API that returns the flight identifier).

1. Define that integration's inputs as usual—static values, profile attributes, or other allowed mappings—then save so its response is available for chaining.

    >[!NOTE]
    >
    > Fields must appear in the administrator-defined response payload for each integration. You cannot reference response properties that were not exposed in configuration.

1. Select the **second** integration (for example, the API that needs the flight number or booking reference on the URL path).

1. For each input that must come from the first call—often a **path variable** or **variable** header/query parameter—choose the mapping source that references the **first integration's response** (for example, the flight booking reference field from the reservation payload). Do not use a static test value if you need live, profile-specific data.

1. Insert the response tokens you need in the content (for example, destination name from the flight API, loyalty balance from a loyalty integration) using the ![add](assets/do-not-localize/Smock_Add_18_N.svg) control.

1. Save the personalization.

When you **simulate** or send, Journey Optimizer resolves integrations in order: the first call runs with the profile context you configured; its output is used to build the second request. Different integrations may run at simulation time and at send time according to your setup and channel behavior.

-->

## 操作方法视频 {#video}

此视频展示了&#x200B;**集成**&#x200B;如何将Adobe Journey Optimizer连接到外部API，以便您可以将实时数据和内容提取到&#x200B;**出站**&#x200B;渠道、电子邮件、短信和推送，以进行更相关的个性化。

>[!VIDEO](https://video.tv.adobe.com/v/3484128/?captions=chi_hans&learn=on)
