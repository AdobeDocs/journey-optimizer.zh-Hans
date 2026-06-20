---
title: 开发人员入门
description: 作为开发人员，了解有关如何使用 Journey Optimizer 的更多信息
feature: Get Started
role: Developer
level: Intermediate
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
TQID: https://experienceleague.adobe.com/7fRI-CPkIeBAPjtXmDgFdyNKgB4WwEc01yKrGUXnc3U
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: e5e8545bef077219ff91428c9048c978184b57ec
workflow-type: tm+mt
source-wordcount: 3456
ht-degree: 54%

---

# 开发人员入门 {#get-started-developers}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;实施将您的应用程序连接到Adobe Journey Optimizer的SDK、事件流、自定义操作端点和API，以使您的旅程能够在实时数据上运行。

>[!ENDSHADEBOX]

作为&#x200B;**开发人员**，您负责将[!DNL Adobe Journey Optimizer]实施并集成到您的应用和系统中。 [系统管理员](administrator.md)和[数据工程师](data-engineer.md)为您授予访问权限并准备好环境后，您就可以开始使用 [!DNL Adobe Journey Optimizer]。

>[!NOTE]
>
>**实施顺序：** [管理员](administrator.md) → [数据工程师](data-engineer.md) →您位于此处： **开发人员** → [营销人员](marketer.md)
>
>在实施移动和Web集成之前，请确保已配置[数据架构和事件](data-engineer.md)。

## 您在 Journey Optimizer 生态系统中的角色

当其他团队成员通过用户界面配置 Journey Optimizer 时，您将专注于以下方面：

* 在移动端和 web 应用中&#x200B;**实现 SDK**
* 从您的应用程序&#x200B;**发送事件**&#x200B;以触发历程
* **构建 API 端点**&#x200B;供 Journey Optimizer 通过自定义操作调用
* **将** Journey Optimizer 与您现有的系统和基础设施集成
* **测试和调试**&#x200B;您的实现内容

您的[数据工程师](data-engineer.md)将处理数据架构、事件配置和数据源。 您的[管理员](administrator.md)将设置权限和渠道配置。 [营销人员](marketer.md)将设计使用您所实现的历程与内容。

本指南涵盖必要的技术实施步骤，助您开始使用 Journey Optimizer。 无论您是构建移动应用程序、web 体验还是 API 集成，请按照以下部分设置您的实施内容。

## 先决条件 {#prerequisites}

在开始实施之前，请确保您具备以下条件：

| 类别 | 要求 |
|----------|-------------|
| **技术技能** | * 具备 JavaScript（用于 Web SDK）或 Swift/Kotlin（用于 Mobile SDK）经验<br>* 了解 RESTful API 和 JSON<br>* 熟悉异步编程和事件驱动型架构<br>* 了解您所在组织的应用架构 |
| **访问权限与工具** | * 访问 [Adobe Developer Console](https://developer.adobe.com){target="_blank"} 以获取 API 凭据<br>* 可访问应用代码库的开发环境<br>* 用于 API 测试的工具（如 Postman）<br>* 浏览器开发者工具或移动端调试工具 |
| **来自其他团队成员** | *由[管理员](administrator.md)<br>授予的环境访问权限 * 来自[数据工程师](data-engineer.md)<br>的 XDM 架构与事件定义 * 来自[营销人员](marketer.md)的需求与用例 |

## 理解技术基础 {#technical-foundation}

在深入实施之前，请先熟悉以下核心技术概念：

1. **Adobe Experience Platform 集成**：Journey Optimizer 原生构建于 Adobe Experience Platform 之上。 理解其底层架构将帮助您构建更高效的实施方案。 进一步了解 [Journey Optimizer 的工作原理](../understanding-ajo.md)。

1. **XDM 数据模型**：Journey Optimizer 使用体验数据模型 (XDM) 来构建事件和轮廓数据的结构。 作为开发人员，您需要了解如何发送符合[数据工程师](data-engineer.md)配置的数据架构的数据。 了解 [XDM 架构](../../data/get-started-schemas.md)。

1. **身份验证和安全性**：所有实施都需要进行适当的认证。 了解如何为 SDK 和 API 设置身份验证。 了解 [API 身份验证](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}。

## 设置移动应用集成 {#mobile-integration}

### 配置 Adobe Experience Platform Mobile SDK

Mobile SDK是您直接在iOS或Android应用程序中嵌入的库集合。 它充当应用程序与Adobe Experience Platform之间的通信层：用于从Journey Optimizer中标识用户、收集行为事件并提供说明，包括推送通知、应用程序内消息和个性化内容。 如果没有这些信息，Journey Optimizer将无法看到您的应用程序用户在做什么，并且也无法联系他们。

1. **安装和配置 Mobile SDK**：按照[Adobe Experience Platform Mobile SDK 文档](https://developer.adobe.com/client-sdks/documentation/getting-started){target="_blank"}操作，开始进行 SDK 集成。

1. **创建移动属性**：在 [!DNL Adobe Experience Platform Data Collection] 中设置移动属性。 了解如何[创建和配置移动属性](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property){target="_blank"}。

1. **配置推送通知**：
   * 针对 **iOS 应用**：在 APN（Apple 推送通知服务）中注册您的应用。 请在 [Apple 文档](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}中了解详情。
   * 对于 **Android 应用程序**：为 Android 应用程序设置 Firebase Cloud Messaging。 请在 [Google 文档](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}中了解详情。

1. **测试您的移动端集成**：使用[移动端快速启动工作流](../../push/mobile-onboarding-wf.md)来高效配置和测试您的移动端设置。

[此页面](../../push/push-configuration.md)提供了配置推送通知的详细步骤。

### 实施基于代码的体验 (Mobile SDK)

通过基于代码的体验，您可以向本机移动设备应用程序中的任何表面交付个性化内容 — 从入门培训屏幕和产品详细信息页面，到应用程序内横幅和功能标记 — 而无需发布新的应用程序。 使用Mobile SDK在运行时获取和呈现个性化内容，让您的团队可以完全控制版面和演示：

* 请按照[本教程](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial){target="_blank"}进行移动 SDK 实施
* 查看 [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} 和 [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"} 的实施示例

## 实施 web 体验 {#web-implementation}

### 设置 Adobe Experience Platform Web SDK

Web SDK (`alloy.js`)是单个JavaScript库，它取代了您的网站可能需要的单独Adobe标记的补丁工作。 它会收集行为数据，通过您配置的数据流将其流式传输到Adobe Experience Platform，并接收返回的个性化指令 — 所有这些都在一个网络中来回传输。 设置完毕后，Journey Optimizer即可识别访客、从其操作触发旅程，并立即向您的页面交付定制的内容。

1. **安装 Web SDK**：按照 [Web SDK 实施指南](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"}在您的网站上设置 SDK。

1. **配置数据流**：在 [!DNL Adobe Experience Platform Data Collection] 中创建并配置启用了 Journey Optimizer 的数据流。 有关更多信息，请参阅[数据流文档](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hans){target="_blank"}。

1. **启用 Web 推送通知**（可选）： Web 推送通知现已正式发布。 在 Web SDK 配置中配置 [pushNotifications 属性](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"}，并使用 [sendPushSubscription 命令](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"}注册推送订阅。 [了解 Web 推送配置](../../push/push-configuration-web.md)。

### 实施基于代码的体验 (Web SDK)

与营销人员完全控制布局的可视化渠道不同，基于代码的体验可让您完全掌控页面上个性化内容的呈现方式。 Journey Optimizer会返回包含个性化数据的JSON有效负载；您的代码可决定要在何处以及如何显示该有效负载。 此模型适用于任何Web表面（主页横幅、推荐轮播、搜索结果排名、A/B测试变体），而无需可视化编辑器或页面发布工作流程。

1. **选择实施方法**：客户端、服务器端或混合模式。 查看每种方法的[实施示例](../../code-based/code-based-implementation-samples.md)。

1. **定义展示界面**：确定应用程序中您希望提供个性化内容的位置。 了解[展示界面配置](../../code-based/code-based-surface.md)。

1. **实施内容渲染**：使用 Web SDK 获取和应用个性化内容。 请参阅[基于代码的实施教程](../../code-based/code-based-decisioning-implementations.md)。

1. **发送展示与交互事件**：追踪内容的展示时机以及用户何时与内容交互以进行分析和优化。

浏览 [&#128279;](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}GitHub 上的实施示例，了解实际应用中的基于代码的体验。

进一步了解[基于代码的体验快速入门](../../code-based/get-started-code-based.md)。

## 实施事件流 {#event-streaming}

### 发送事件以触发历程

历程在事件上运行 — 用户登录，将项目添加到购物车，完成购买，放弃表单。 你的工作是适时地从你的应用程序中发出这些事件。 每个事件都是发送到Experience Platform流摄取API的XDM结构化JSON有效负载；Journey Optimizer在毫秒内选取它，并将配置文件路由到任何匹配的旅程。 事件架构和有效负载结构由您的[数据工程师](data-engineer.md)定义 — 在开始编码之前与它们协调。

1. **了解事件负载**：与您的数据工程师协作，获取事件架构及所需的负载结构。 负载必须符合其配置的 XDM 架构。 了解[事件架构要求](../../event/experience-event-schema.md)。

1. **实施事件流**：使用[流式数据摄取 API](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hans){target="_blank"} 将事件发送至 Adobe Experience Platform。 了解[发送事件的步骤](../../event/additional-steps-to-send-events-to-journey.md)。

1. **处理事件类型**：
   * **单一事件**：针对特定用户的操作（例如按钮点击、购买完成）实现事件发送
   * **业务事件**：发送业务相关事件（例如库存更新、价格变更）

1. **测试事件传递**：验证事件是否被正确接收并按预期触发客户历程。 了解[事件故障排除](../../building-journeys/troubleshooting-inbound.md)。

通过 API 发送事件的&#x200B;**实施示例**：

```javascript
POST https://{DATACOLLECTION_ENDPOINT}/collection/{DATASTREAM_ID}
Content-Type: application/json

{
  "header": {
    "datasetId": "{DATASET_ID}",
    "imsOrgId": "{ORG_ID}",
    "source": {
      "name": "Web SDK"
    }
  },
  "body": {
    "xdmMeta": {
      "schemaRef": {
        "id": "{SCHEMA_ID}"
      }
    },
    "xdmEntity": {
      "_id": "unique-event-id",
      "eventType": "purchase",
      "timestamp": "2024-01-01T12:00:00Z",
      // ... your event data
    }
  }
}
```

进一步了解[处理历程事件](../../event/about-events.md)。

## 开发自定义操作端点 {#custom-actions}

当历程达到自定义操作步骤时，Journey Optimizer会对您提供的URL（您的后端、CRM、忠诚度平台、任何REST端点）进行出站HTTP调用。 您的工作是构建和公开该端点：定义请求合同（有效负荷形状、身份验证方法、响应格式），实施其背后的业务逻辑，并确保它可以处理Journey Optimizer将生成的调用量。 然后，您的[管理员](administrator.md)会在Journey Optimizer中注册该端点，以便营销人员可以将其用作其历程中的步骤。

1. **构建您的 API 端点**：创建 RESTful API 端点，供 Journey Optimizer 在历程执行期间调用。 您的端点应：
   * 接受 JSON 负载
   * 身份验证请求（OAuth、API 密钥或 JWT）
   * 在适当的超时限制内处理请求
   * 以预期格式返回响应

1. **了解自定义操作功能**：自定义操作可以连接到第三方系统，如 Epsilon、Slack、Firebase 或您自己的服务。 详细了解[自定义操作](../../action/action.md)。

1. **使用操作配置**：您的[管理员](administrator.md)或[数据工程师](data-engineer.md)将在 Journey Optimizer 中配置自定义操作，定义 API 端点 URL、身份验证方法和参数。 您将向他们提供您的 API 规范。 了解[自定义操作配置](../../action/about-custom-action-configuration.md)。 您可以在超时/错误分支中定义可选的&#x200B;**错误响应负载**，以实现更丰富的回退逻辑。

1. **返回可操作数据**：设计您的 API 以返回可在后续历程步骤中使用的数据。 了解[操作响应](../../action/action-response.md)。

1. **监视自定义操作运行状况**：使用自定义操作监视仪表板跟踪成功的调用、错误、吞吐量、响应时间和队列等待时间。 了解[自定义操作报告](../../action/reporting.md)。

1. **实现速率限制**：确保您的端点能够处理预期的请求量。 Journey Optimizer 设有 5000 次/秒的调用限制，但您的系统应具备一定弹性。 了解[上限和限制](../../configuration/external-systems.md)。

**示例用例**：使用自定义操作[将历程事件写入 Experience Platform](../../building-journeys/custom-action-aep.md)。

## 使用 Journey Optimizer API {#apis}

并非所有事情都需要通过Journey Optimizer UI发生。 有时，您需要从自己的后端触发营销活动、在隐私请求后禁止显示电子邮件地址，或从外部CMS同步内容模板。 Journey Optimizer的REST API允许您以编程方式访问平台的核心功能。 所有调用都使用OAuth服务器到服务器身份验证 — 弃用旧的JWT方法。

1. **了解 API 功能**： Journey Optimizer API 允许您以编程方式创建、读取、更新和删除各种资源。 了解 [Journey Optimizer API](../../configuration/ajo-apis.md)。

1. **身份验证**：按照[本教程](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}，使用 Adobe Developer Console 设置 API 身份验证。

1. **浏览 API 参考文档**：浏览完整的 API 文档，并直接在 [Adobe Journey Optimizer API 参考](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}中尝试 API 调用。

1. **API 触发的营销活动**：通过 API 触发的营销活动构建交易型消息。 针对高流量场景（最高可达 5000 TPS），可探索使用[高吞吐量模式](../../campaigns/api-triggered-high-throughput.md)（需要附加许可证）。

1. **决策管理 API**：使用专门的 API 进行产品建议管理和决策。 在[决策管理 API 指南](../../offers/api-reference/getting-started.md)中了解更多信息。

1. **Decisioning 迁移 API**：以编程方式将决策管理实体迁移到 Decisioning，它具有灵活的迁移范围、自动验证和回滚支持。 在 [Decisioning 迁移 API 指南](../../experience-decisioning/decisioning-migration-api.md)中了解详情。

1. **短信 Webhook**：配置入站 Webhook 以捕获传入消息，并配置反馈 Webhook 以接收投放回执和状态更新。 [了解详情](../../mobile/mobile-webhook.md)。

## 测试与调试 {#testing}

在实施上线之前，您需要确信事件会在正确的时间触发，历程会按预期触发，自定义操作会在实际负载下运行，并且个性化内容会正确呈现。 本节介绍用于及早发现问题的工具和技术，从低级别的SDK日志记录到使用真实用户档案进行的端到端旅程测试运行。

1. **调试SDK实施**：使用Adobe Experience Platform Assurance检查SDK事件，验证数据收集，并在集成问题发生时对其进行故障诊断。 [进一步了解 Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=zh-Hans){target="_blank"}。

1. **测试事件传递**：验证您应用程序发出的事件是否被 Adobe Experience Platform 正确接收并按预期触发历程。 监控事件摄取过程并验证有效负载结构。

1. **验证 API 集成**：测试您的自定义操作端点，以确保其能正确处理 Journey Optimizer 请求、在超时限制内响应，并返回预期的数据格式。

1. **对测试轮廓使用测试模式**：与[数据工程师](data-engineer.md)协作获取对测试轮廓的访问权限，然后使用历程测试模式验证您的实施。 了解如何[测试历程](../../building-journeys/testing-the-journey.md)。

1. **监控 SDK 日志**：在您的 SDK 实现中启用调试日志记录，以便在开发期间排查问题：
   * **Mobile SDK**：启用日志记录以查看 SDK 事件和 API 调用
   * **Web SDK**：使用浏览器控制台监控 SDK 活动

1. **验证数据流配置**：确保您的数据流已正确配置，可将数据发送至 Journey Optimizer。 检查事件是否通过数据流传递至正确的目标位置。

1. **查询历程数据以供分析**：在数据湖上使用 SQL 查询来分析历程步骤事件、调试问题并监控自定义操作性能。 探索[用于历程分析的查询示例](../../reports/query-examples.md)，包括：
   * 轮廓进入/退出追踪和丢弃原因分析
   * 自定义操作性能指标（延迟、吞吐量、错误率）
   * 事件交付和错误模式
   * 历程实例状态

## 高级开发人员主题 {#advanced-topics}

一旦您的核心SDK、事件和API准备就绪，这些主题将帮助您走得更远：在运行时扩充历程数据而不扩充配置文件，处理同意信号以使选择退出在整个集成中传播，以及针对生产规模所需的吞吐量和可靠性调整您的实施。

### 处理上下文数据和扩充

历程通常需要的数据多于触发事件中提供的数据 — 产品名称、忠诚度等级和订单行项目列表。 上下文扩充允许您的旅程在运行时从AEP数据集查找它或从自定义操作响应中将其转发，而不是将所有这些预先加载到每个配置文件中。 然后，您的消息和分支条件可以引用该数据，而无需将其永久存储在用户档案中。

* **对数组进行迭代**：使用 Handlebars 语法在消息中展示来自事件、自定义操作响应及数据集查询的动态列表。 了解[迭代上下文数据](../../personalization/iterate-contextual-data.md)。
* **数据集查找**：实施数据集查找以扩充 Adobe Experience Platform 数据集的历程数据。 与您的数据工程师协作进行配置。 了解[数据集查找](../../building-journeys/dataset-lookup.md)。

### 处理同意与治理

Journey Optimizer在平台级别实施数据治理和同意策略，但您的集成也需要尊重它们。 当客户选择退出营销通信或数据使用标签限制字段的使用方式时，这些规则需要在自定义操作和数据集查找中传播 — 而不仅仅是UI中的阻止操作。

* **数据治理**：将数据使用策略应用于自定义操作。 进一步了解[数据治理](../../action/action-privacy.md)。
* **同意管理**：在您的实施中处理客户同意偏好设置。 了解[同意](../../action/consent.md)。

### 优化与最佳实践

生产Journey Optimizer实施每秒会定期处理数百万个事件和数千次旅程执行。 这些资源可帮助您针对该规模调整集成 — 在点击速率限制之前了解这些限制，避免静默丢弃用户档案的常见旅程设计隐患，以及构建可正常降低而不是不透明地失败的错误处理。

* **上限和限制**：了解速率限制并实施适当的节流机制。 了解[外部系统](../../configuration/external-systems.md)。
* **历程优化**：遵循[历程优化](../../building-journeys/optimize.md)的最佳实践。
* **错误处理**：实施稳健的错误处理机制。 查阅[错误代码](../../building-journeys/error-codes-reference.md)及[故障排除指南](../../building-journeys/troubleshooting.md)。

## 调用Journey Optimizer REST API {#rest-apis}

除了实施SDK和事件流之外，您还可以以编程方式从您自己的系统中驱动Journey Optimizer。 完整的API引用、OpenAPI规格和代码示例位于[Journey Optimizer开发人员门户](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}上。

>[!NOTE]
>
>所有集成都必须使用OAuth服务器到服务器身份验证 — JWT方法已被弃用。 [设置身份验证](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}

### 执行API触发的营销活动 {#api-triggered}

使用交互式消息执行REST API触发来自外部系统的事务性或营销消息。 在调用端点之前：

* 在终结点接受调用之前，营销活动必须是&#x200B;**激活的**。
* 调用的&#x200B;**超时为60秒**；内部重试处理意外超时。
* 如果配置了促销活动开始/结束日期，则超出这些日期的API调用将失败。
* 要构建有效负载，请在Journey Optimizer UI中从实时营销活动的&#x200B;**cURL请求**&#x200B;部分中检索生成的示例cURL请求 — 其中包括该营销活动的所有个性化变量。
* 标准和[高吞吐量营销活动](../../campaigns/api-triggered-high-throughput.md)使用不同的端点。

[API引用](https://developer.adobe.com/journey-optimizer-apis/references/messaging){target="_blank"} · [代码示例](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples){target="_blank"} · [使用API触发的营销活动](../../campaigns/api-triggered-campaigns.md)

### 外部端点的上限和限制 {#capping-throttling}

当历程通过自定义操作或数据源调用外部系统时，上限和限制API会保护这些系统免受过载。 设置上限可拒绝超出配置限制的调用；限制可使调用排队长达6小时（仅限生产沙盒、自定义操作）。

[上限API引用](https://developer.adobe.com/journey-optimizer-apis/references/journeys-throttling){target="_blank"} · [使用上限API](../../configuration/capping.md) · [使用限制API](../../configuration/throttling.md)

### 更多REST API {#more-rest-apis}

除了消息传递和封顶之外，Journey Optimizer还会公开REST端点，以用于禁止管理、内容模板、活动检索、验证和编排的活动执行。 当您需要自动执行操作时，请使用这些选项，否则UI中需要手动步骤，例如，拉取数据后批量隐藏地址，或从外部内容管道同步模板。

| 您需要执行的操作 | API 参考 |
| ------------------- | ------------- |
| 以编程方式从发送中排除电子邮件地址或域 | [隐藏API](https://developer.adobe.com/journey-optimizer-apis/references/suppression){target="_blank"} · [管理隐藏列表](../../configuration/manage-suppression-list.md) |
| 检索历程元数据以进行审核或外部同步 | [历程API](https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve){target="_blank"} |
| 从外部管道创建和管理内容模板和片段 | [内容API](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"} · [模板](../../content-management/content-templates.md) · [片段](../../content-management/fragments.md) |
| 检索和过滤操作营销活动 | [促销活动API](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"} |
| 预览营销活动并以编程方式发送验证 | [模拟API](https://developer.adobe.com/journey-optimizer-apis/references/simulations){target="_blank"} |
| 验证数据集并触发编排的活动执行 | [数据集验证](https://developer.adobe.com/journey-optimizer-apis/references/orchestrated-campaign-dataset){target="_blank"} · [触发器](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} · [启用数据集](../../orchestrated/manual-schema.md) |

## 其他资源 {#additional-resources}

* **Developer Console**：访问 [Adobe Developer Console](https://developer.adobe.com){target="_blank"} 以创建集成并管理 API 凭据。
* **示例代码**：浏览 [GitHub 上的实施示例](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}。
* **视频教程**：通过 [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=zh-Hans){target="_blank"} 上的实践教程进行学习。
* **开发人员社区**：与其他开发人员联系，并在 Adobe 社区论坛中获取支持。

## 跨角色协作 {#next-steps}

您的实施工作与其他团队成员相互关联：

>[!BEGINTABS]

>[!TAB 与数据工程师协作]

与[数据工程师](data-engineer.md)协作处理数据和事件配置。 对用户行为做出反应的每个历程都取决于您发送的事件 — 数据工程师定义架构，您实施生成这些架构的代码。

* 获取需要实施的[XDM架构](../../data/get-started-schemas.md)和事件结构
* 了解您需要发送哪些事件及其所需的有效负载格式 — 请参阅[处理历程事件](../../event/about-events.md)
* 确认每个事件有效负载中的哪些字段是必填字段还是可选字段，以及当预期字段缺失或格式错误时，旅程中会发生什么情况 — 请参阅[架构要求](../../event/experience-event-schema.md#schema-requirements)
* 使用[Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=zh-Hans){target="_blank"}一起测试事件投放和数据摄取

>[!TAB 与管理员协作]

与[管理员](administrator.md)在访问和渠道配置上进行协作。 历程只能通过管理员设置的渠道联系用户 — 尽早协调，以便您的SDK工作及其配置保持同步。

* 为将在Journey Optimizer中配置的[自定义操作](../../action/about-custom-action-configuration.md)提供API规范
* 通过[Adobe Developer Console](https://developer.adobe.com){target="_blank"}请求必要的权限和API凭据
* 协调渠道配置要求 — [iOS](../../push/push-configuration.md)和Android的推送证书、[Web推送](../../push/push-configuration-web.md)设置、[SMS webhook](../../mobile/mobile-webhook.md)端点
* 在运行[历程测试模式](../../building-journeys/testing-the-journey.md)之前，根据沙盒策略和测试环境进行调整

>[!TAB 与营销人员协作]

与[营销人员](marketer.md)协作进行历程设计和测试。 营销人员构建旅程和内容完全取决于您发送的事件和公开的外观 — 您对齐得越近，旅程上线的速度就越快。

* 一起查看[Journey Optimizer](../../building-journeys/journey.md)中的历程设计，了解哪些用户交互必须触发事件以及哪些表面需要个性化
* 实施跟踪，以便营销人员可以衡量[内容绩效和用户参与度](../../reports/report-gs-cja.md)
* 使用测试配置文件一起运行[历程测试模式](../../building-journeys/testing-the-journey.md)以端到端地验证完整流程
* 邮件传递、个性化呈现或[自定义操作](../../action/action.md)响应问题疑难解答

>[!ENDTABS]

## 开始实施

准备好开始构建了吗？ 从以上部分中选择您的首个实施领域：

1. **移动应用程序？** 从 [Mobile SDK 集成](#mobile-integration)开始
2. **网站？** 从 [Web SDK 设置](#web-implementation)开始
3. **API 集成？** 跳转到[使用 API](#apis)
4. **自定义系统？** 查看[自定义操作](#custom-actions)

每个部分都包含指向详细技术文档、代码示例和教程的链接，以指导您的实施工作。

## 其他角色指南 {#other-role-guides}

| 角色 | 指南 |
|------|-------|
| 管理员 | [管理员入门](administrator.md) |
| 数据工程师 | [数据工程师入门](data-engineer.md) |
| Developer | [开发人员入门](developer.md) |
| 营销人员 | [营销人员入门指南](marketer.md) |

返回[角色和职责概述](../quick-start.md) ·返回[开始](../../../rp_landing_pages/get-started-landing-page.md)
