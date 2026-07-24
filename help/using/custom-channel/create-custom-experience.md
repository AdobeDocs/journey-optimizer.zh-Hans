---
title: 创建自定义渠道体验
description: 了解如何在Adobe Journey Optimizer中的历程、活动或编排的活动中使用自定义渠道。
feature: Channel Configuration
topic: Content Management
role: User
level: Experienced
badge: label="有限发布版" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 15%

---


# 创建自定义渠道体验 {#create-custom-channel}

>[!AVAILABILITY]
>
>此功能为限量发布版。 请联系 Adobe 代表获取访问权限。

在[!DNL Journey Optimizer]中，您可以使用营销活动、历程和编排营销活动中的自定义渠道投放消息。 请按照以下步骤设置您的自定义渠道体验。

>[!NOTE]
>
>在创建自定义渠道体验之前，请确保管理员已配置自定义渠道。 [了解详情](configure-custom-channel.md)

## 通过历程或营销活动添加一个自定义操作 {#create-custom-channel-experience}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_channel"
>title="自定义渠道操作"
>abstract="当轮廓到达历程中的这个步骤时，自定义渠道操作会向其发送消息。 标签标识了历程画布中的活动，操作会引用一个定义了用于传递消息的端点、负载和凭据的自定义渠道配置。 **优化**&#x200B;部分可以包含内容试验或目标选择规则，**超时或错误**&#x200B;部分可以定义操作失败情况下的替代路径。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/orchestrate-journeys/about-journey-building/journey-action#add-action" text="开始使用自定义渠道"



>[!BEGINTABS]

>[!TAB 向历程添加自定义渠道]

自定义渠道显示在历程画布调色板的&#x200B;**[!UICONTROL 操作]**&#x200B;部分中，按其显示名称和自定义图标列出，如渠道生成器中所定义。

要向历程添加自定义渠道操作，请执行以下操作：

1. [创建历程](../building-journeys/journey-gs.md)。

1. 通过[事件](../building-journeys/general-events.md)或[读取受众](../building-journeys/read-audience.md)活动开始您的历程。

1. 从调色板的&#x200B;**[!UICONTROL 操作]**&#x200B;部分拖放&#x200B;**[!UICONTROL 操作]**&#x200B;活动。 了解有关[操作活动](../building-journeys/journey-action.md)的详细信息。

1. 在&#x200B;**[!UICONTROL 操作]**&#x200B;下拉列表中，选择要使用的自定义渠道。 自定义渠道按渠道生成器中分配的名称和图标列出。

   ![](assets/custom_channel_journey_action.png){width="80%"}

1. 向操作添加标签，单击右侧面板中的&#x200B;**[!DNL Configure action]**，然后选择要使用的&#x200B;**[!UICONTROL 渠道配置]**。 [了解如何创建自定义渠道配置](custom-channel-configuration.md#create-channel-config)

1. 在&#x200B;**[!UICONTROL 消息]**&#x200B;部分中，单击&#x200B;**[!UICONTROL 编辑内容]**&#x200B;以打开有效负荷编辑器并创作消息。 [了解如何创作内容](#author-content)

1. 根据需要添加其他步骤以完成旅程流，然后发布旅程。 [了解详情](../building-journeys/journey-gs.md)

>[!TAB 创建自定义渠道营销活动]

要在营销活动中使用自定义渠道，请执行以下操作：

1. [创建营销活动](../campaigns/create-campaign.md)。

1. 选择营销活动类型：

   * **[!UICONTROL 已计划 — 营销]** — 立即执行或在指定日期执行。 为营销消息而设计，通过UI进行配置。
   * **[!UICONTROL API触发 — 营销/事务性]** — 通过API调用执行。 专为事件触发的消息传送（例如，订单确认或密码重置）而设计。 [了解详情](../campaigns/api-triggered-campaigns.md)

1. 完成活动设置：活动属性、[受众](../audience/about-audiences.md)和[计划](../campaigns/create-campaign.md#schedule)。

1. 在&#x200B;**[!UICONTROL 操作]**&#x200B;部分中，从渠道选择器中选择自定义渠道。 在您的沙盒上配置的所有自定义渠道均与本机渠道一起显示。

   ![](assets/custom_channel_campaign_action.png){width="80%"}

1. 选择或创建要使用的&#x200B;**[!UICONTROL 渠道配置]**。 [了解如何创建渠道配置](custom-channel-configuration.md#create-channel-config)

1. （可选）启用&#x200B;**[!UICONTROL 操作跟踪]**&#x200B;以自动跟踪消息有效负载中包含的链接（需要为自定义渠道配置子域）。 [了解如何委派自定义渠道的子域](custom-channel-subdomains.md#subdomain-delegation)

1. 在&#x200B;**[!UICONTROL 优化]**&#x200B;部分中，您可以：

   * **[!UICONTROL 创建定位规则]**&#x200B;以将不同的消息发送到受众的不同区段。 [了解详情](../campaigns/create-campaign.md#targeting)
   * 单击&#x200B;**[!UICONTROL 创建试验]**&#x200B;对自定义渠道消息运行A/B测试。 [了解详情](../campaigns/create-campaign.md#content-experiment)

1. 单击&#x200B;**[!UICONTROL 编辑内容]**&#x200B;以打开有效负荷编辑器并创作消息。 [了解如何创作内容](#author-content)

1. 查看并激活营销活动。 [了解详情](../campaigns/create-campaign.md)

<!--
>[!TAB Add a custom channel to an orchestrated campaign]

Custom channels appear in the channel selection list in the orchestrated Campaigns canvas, below the native channels, with their custom icon and display name.

To add a custom channel in an orchestrated campaign:

1. Open or create an orchestrated campaign.

1. In the canvas, add a channel action node and select your custom channel from the list.

1. Select the **[!UICONTROL Channel configuration]** to use. Ensure the configuration includes the **[!UICONTROL Execution details]** section required for orchestrated campaigns.

1. Click **[!UICONTROL Edit content]** to open the payload editor and author your message. [Learn how to author content](#author-content)
-->

>[!ENDTABS]

## 创作自定义渠道内容 {#author-content}

内容编辑器可反映您在配置自定义渠道时定义的有效负载结构。 单击&#x200B;**[!UICONTROL 编辑代码]**&#x200B;以打开有效负载编辑器并输入消息内容。

![](assets/custom_channel_payload_editor.png){width="80%"}

此时会显示可创作和个性化的字段。 您可以利用[!DNL Journey Optimizer]个性化编辑器及其所有个性化和创作功能。 [了解详情](../personalization/personalization-build-expressions.md)

>[!NOTE]
>
>仅支持JSON负载。 如果您的自定义渠道有效负载不是JSON，则可以使用JSON包装器来封装内容。 例如，如果您的有效负载为XML，则可以将其包装在JSON对象中，如下所示：
>
>```json
>{
>   "payload": "<xml>...</xml>"
>}
>```

### 将有效负载个性化 {#personalize}

[!DNL Journey Optimizer]的完整个性化功能在有效负载编辑器中可用：

* **配置文件属性** — 插入任何XDM配置文件属性，如`{{profile.person.name.firstName}}`或自定义标识，如存储在自定义命名空间中的消息传送平台用户ID。
* **上下文属性** — 使用在发送时解析的历程事件属性或营销活动上下文数据。
* **辅助函数** — 使用内置字符串、日期或算术函数设置值的格式。 [了解详情](../personalization/functions/helpers.md)
* **表达式片段** — 跨多个渠道和营销活动重用共享的个性化逻辑。 [了解详情](../content-management/customizable-fragments.md)

>[!CAUTION]
>
>当前，创作时不会对有效负载进行验证。 您可以使用&#x200B;**[!UICONTROL 模拟内容]**&#x200B;功能来验证您的有效负载是否为格式正确的JSON，以及所有个性化表达式是否都能正确解析您的测试配置文件。 [了解详情](test-custom-channel.md#simulate-content)

### 有效负载示例 {#example-payload}

以下示例显示自定义消息渠道<!--(to be replaced with a meaningful realistic example)-->的具有配置文件个性化的JSON有效负载：

```json
{
  "recipient_id": "{{profile.mobilePhone.number}}",
  "message_text": "Hello {{profile.person.name.firstName}}, your order {{context.journey.events.0.commerce.order.purchaseID}} has been confirmed.",
  "channel": "my-custom-channel",
  "image": {
    "id": "{{profile.preferences.imageId | default('default-image-001')}}"
  }
}
```

### 跟踪有效负载中的链接 {#track-links}

要在自定义渠道有效载荷中包含跟踪链接，以便自动在渠道的报表功能板中跟踪和显示点击，请使用以下手柄栏语法来换行URL：

```
{{url trackedUrl='' originalUrl='https://example.com/' type='TRACKED'}}
```

* `originalUrl` — 要将收件人重定向到的目标URL。
* `trackedUrl` — 将此留空；[!DNL Journey Optimizer]在发送时自动使用启用跟踪的重定向URL填充它。
* `type` — 必须设置为`TRACKED`。

>[!NOTE]
>
>链接跟踪需要为自定义渠道配置子域。 [了解如何委派自定义渠道的子域](custom-channel-subdomains.md#subdomain-delegation)

**示例 — LINE有效负载中的跟踪链接：**

```json
{
  "to": "{{profile.mobilePhone.number}}",
  "messages": [
    {
      "type": "text",
      "text": "Hello! Check out our latest offer: {{url trackedUrl='' originalUrl='https://example.com/' type='TRACKED'}}"
    }
  ]
}
```

<!--
### Strict JSON mode {#strict-json}

The editor supports a **[!UICONTROL Strict JSON]** toggle:

* **Strict JSON: Off (default)** – The editor accepts any payload content, including personalization helpers and functions that may temporarily produce non-JSON syntax. A warning is displayed at the **Review to Activate** step if the payload is not well-formed JSON, prompting you to simulate and proof before publishing.
* **Strict JSON: On** – The editor validates that the payload is well-formed JSON as you type. At the **Review to Activate** step, [!DNL Journey Optimizer] validates the payload against the channel schema and flags missing required fields or type mismatches as errors that must be resolved before activation.
-->

## 激活您的自定义渠道体验 {#activate}

>[!IMPORTANT]
>
>在激活之前，预览和测试自定义渠道有效负载。 [了解如何操作](test-custom-channel.md)
>
>如果您的营销活动或历程受批准政策的约束，则必须在激活之前请求批准。 [了解详情](../test-approve/gs-approval.md)

* **从历程** — 单击右上角区域中的&#x200B;**[!UICONTROL 发布]**。 历程将上线并开始调用您的外部端点来获取符合条件的用户档案。
* **从营销活动** — 单击&#x200B;**[!UICONTROL 查看以激活]**，查看您的设置，然后单击&#x200B;**[!UICONTROL 激活]**。 营销活动采用&#x200B;**[!UICONTROL 实时]**&#x200B;状态（或者&#x200B;**[!UICONTROL 已计划]**，如果已定义未来开始日期）。
