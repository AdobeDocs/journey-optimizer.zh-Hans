---
title: 开发人员入门
description: 作为开发人员，了解有关如何使用 Journey Optimizer 的更多信息
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: fd10a600cb54b8c35e2d195be7379b0dd120b6a7
workflow-type: tm+mt
source-wordcount: '1918'
ht-degree: 93%

---

# 开发人员入门 {#get-started-developers}

作为&#x200B;**开发人员**，您负责将[!DNL Adobe Journey Optimizer]实施并集成到您的应用和系统中。[系统管理员](administrator.md)和[数据工程师](data-engineer.md)为您授予访问权限并准备好环境后，您就可以开始使用 [!DNL Adobe Journey Optimizer]。

## 您在 Journey Optimizer 生态系统中的角色

当其他团队成员通过用户界面配置 Journey Optimizer 时，您将专注于以下方面：

* 在移动端和 web 应用中&#x200B;**实现 SDK**
* 从您的应用程序&#x200B;**发送事件**&#x200B;以触发历程
* **构建 API 端点**&#x200B;供 Journey Optimizer 通过自定义操作调用
* **将** Journey Optimizer 与您现有的系统和基础设施集成
* **测试和调试**&#x200B;您的实现内容

您的[数据工程师](data-engineer.md)将处理数据架构、事件配置和数据源。您的[管理员](administrator.md)将设置权限和渠道配置。[营销人员](marketer.md)将设计使用您所实现的历程与内容。

本指南涵盖必要的技术实施步骤，助您开始使用 Journey Optimizer。无论您是构建移动应用程序、web 体验还是 API 集成，请按照以下部分设置您的实施内容。

## 先决条件 {#prerequisites}

在开始实施之前，请确保您具备以下条件：

| 类别 | 要求 |
|----------|-------------|
| **技术技能** | * 具备 JavaScript（用于 Web SDK）或 Swift/Kotlin（用于 Mobile SDK）经验<br>* 了解 RESTful API 和 JSON<br>* 熟悉异步编程和事件驱动型架构<br>* 了解您所在组织的应用架构 |
| **访问权限与工具** | * 访问 [Adobe Developer Console](https://developer.adobe.com){target="_blank"} 以获取 API 凭据<br>* 可访问应用代码库的开发环境<br>* 用于 API 测试的工具（如 Postman）<br>* 浏览器开发者工具或移动端调试工具 |
| **来自其他团队成员** | *由[管理员](administrator.md)<br>授予的环境访问权限 * 来自[数据工程师](data-engineer.md)<br>的 XDM 架构与事件定义 * 来自[营销人员](marketer.md)的需求与用例 |

## 理解技术基础 {#technical-foundation}

在深入实施之前，请先熟悉以下核心技术概念：

1. **Adobe Experience Platform 集成**：Journey Optimizer 原生构建于 Adobe Experience Platform 之上。理解其底层架构将帮助您构建更高效的实施方案。进一步了解 [Journey Optimizer 的工作原理](../understanding-ajo.md)。

1. **XDM 数据模型**：Journey Optimizer 使用体验数据模型 (XDM) 来构建事件和轮廓数据的结构。作为开发人员，您需要了解如何发送符合[数据工程师](data-engineer.md)配置的数据架构的数据。了解 [XDM 架构](../../data/get-started-schemas.md)。

1. **身份验证和安全性**：所有实施都需要进行适当的认证。了解如何为 SDK 和 API 设置身份验证。了解 [API 身份验证](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}。

## 设置移动应用集成 {#mobile-integration}

### 配置 Adobe Experience Platform Mobile SDK

要启用推送通知、应用程序内消息和其他移动端功能，请将 Adobe Experience Platform Mobile SDK 集成到您的移动应用程序中。

1. **安装和配置 Mobile SDK**：按照[Adobe Experience Platform Mobile SDK 文档](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"}操作，开始进行 SDK 集成。

1. **创建移动属性**：在 [!DNL Adobe Experience Platform Data Collection] 中设置移动属性。了解如何[创建和配置移动属性](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}。

1. **配置推送通知**：
   * 针对 **iOS 应用**：在 APN（Apple 推送通知服务）中注册您的应用。请在 [Apple 文档](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}中了解详情。
   * 对于 **Android 应用程序**：为 Android 应用程序设置 Firebase Cloud Messaging。请在 [Google 文档](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}中了解详情。

1. **测试您的移动端集成**：使用[移动端快速启动工作流](../../push/mobile-onboarding-wf.md)来高效配置和测试您的移动端设置。

[此页面](../../push/push-configuration.md)提供了配置推送通知的详细步骤。

### 实施基于代码的体验 (Mobile SDK)

若要通过基于代码的体验实现原生移动应用个性化：

* 请按照[本教程](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"}进行移动 SDK 实施
* 查看 [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} 和 [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"} 的实施示例

## 实施 web 体验 {#web-implementation}

### 设置 Adobe Experience Platform Web SDK

对于基于 web 的实施，Web SDK 是您的主要集成点：

1. **安装 Web SDK**：按照 [Web SDK 实施指南](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"}在您的网站上设置 SDK。

1. **配置数据流**：在 [!DNL Adobe Experience Platform Data Collection] 中创建并配置启用了 Journey Optimizer 的数据流。有关更多信息，请参阅[数据流文档](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hans){target="_blank"}。

1. **启用Web推送通知**（可选）： Web推送通知现在通常可用。 在Web SDK配置中配置[pushNotifications属性](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"}，并使用[sendPushSubscription命令](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"}注册推送订阅。 [了解Web推送配置](../../push/push-configuration-web.md)。

### 实施基于代码的体验 (Web SDK)

基于代码的体验允许您个性化任何数字接触点：

1. **选择实施方法**：客户端、服务器端或混合模式。查看每种方法的[实施示例](../../code-based/code-based-implementation-samples.md)。

1. **定义展示界面**：确定应用程序中您希望提供个性化内容的位置。了解[展示界面配置](../../code-based/code-based-surface.md)。

1. **实施内容渲染**：使用 Web SDK 获取和应用个性化内容。请参阅[基于代码的实施教程](../../code-based/code-based-decisioning-implementations.md)。

1. **发送展示与交互事件**：追踪内容的展示时机以及用户何时与内容交互以进行分析和优化。

浏览 ](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}GitHub 上的实施示例[，了解实际应用中的基于代码的体验。

进一步了解[基于代码的体验快速入门](../../code-based/get-started-code-based.md)。

## 实施事件流 {#event-streaming}

### 发送事件以触发历程

作为开发人员，您需要编写代码以发送触发历程的事件。您的[数据工程师](data-engineer.md)将在 Journey Optimizer 中配置事件架构和定义。

1. **了解事件负载**：与您的数据工程师协作，获取事件架构及所需的负载结构。负载必须符合其配置的 XDM 架构。了解[事件架构要求](../../event/experience-event-schema.md)。

1. **实施事件流**：使用[流式数据摄取 API](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hans){target="_blank"} 将事件发送至 Adobe Experience Platform。了解[发送事件的步骤](../../event/additional-steps-to-send-events-to-journey.md)。

1. **处理事件类型**：
   * **单一事件**：针对特定用户的操作（例如按钮点击、购买完成）实现事件发送
   * **业务事件**：发送业务相关事件（例如库存更新、价格变更）

1. **测试事件传递**：验证事件是否被正确接收并按预期触发客户历程。了解[事件故障排除](../../building-journeys/troubleshooting-inbound.md)。

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

自定义操作允许历程调用您的 API。作为开发人员，您将构建供自定义操作调用的 API 端点：

1. **构建您的 API 端点**：创建 RESTful API 端点，供 Journey Optimizer 在历程执行期间调用。您的端点应：
   * 接受 JSON 负载
   * 身份验证请求（OAuth、API 密钥或 JWT）
   * 在适当的超时限制内处理请求
   * 以预期格式返回响应

1. **了解自定义操作功能**：自定义操作可以连接到第三方系统，如 Epsilon、Slack、Firebase 或您自己的服务。详细了解[自定义操作](../../action/action.md)。

1. **使用操作配置**：您的[管理员](administrator.md)或[数据工程师](data-engineer.md)将在 Journey Optimizer 中配置自定义操作，定义 API 端点 URL、身份验证方法和参数。您将向他们提供您的 API 规范。了解[自定义操作配置](../../action/about-custom-action-configuration.md)。 您可以在超时/错误分支中为更丰富的回退逻辑定义可选的&#x200B;**错误响应有效负载**。

1. **返回可操作数据**：设计您的 API 以返回可在后续历程步骤中使用的数据。了解[操作响应](../../action/action-response.md)。

1. **监视自定义操作运行状况**：使用自定义操作监视仪表板跟踪成功的调用、错误、吞吐量、响应时间和队列等待时间。 了解[自定义操作报告](../../action/reporting.md)。

1. **实现速率限制**：确保您的端点能够处理预期的请求量。Journey Optimizer 设有 5000 次/秒的调用限制，但您的系统应具备一定弹性。了解[上限和限制](../../configuration/external-systems.md)。

**示例用例**：使用自定义操作[将历程事件写入 Experience Platform](../../building-journeys/custom-action-aep.md)。

## 使用 Journey Optimizer API {#apis}

Journey Optimizer 提供了全面的 REST API，支持通过编程方式访问：

1. **了解 API 功能**： Journey Optimizer API 允许您以编程方式创建、读取、更新和删除各种资源。了解 [Journey Optimizer API](../../configuration/ajo-apis.md)。

1. **身份验证**：按照[本教程](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}，使用 Adobe Developer Console 设置 API 身份验证。

1. **浏览 API 参考文档**：浏览完整的 API 文档，并直接在 [Adobe Journey Optimizer API 参考](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}中尝试 API 调用。

1. **API 触发的营销活动**：通过 API 触发的营销活动构建交易型消息。针对高流量场景（最高可达 5000 TPS），可探索使用[高吞吐量模式](../../campaigns/api-triggered-high-throughput.md)（需要附加许可证）。

1. **决策管理 API**：使用专门的 API 进行产品建议管理和决策。在[决策管理 API 指南](../../offers/api-reference/getting-started.md)中了解更多信息。

1. **Decisioning迁移API**：以编程方式将Decisioning Management实体迁移到Decisioning，它具有灵活的范围、自动验证和回滚支持。 请参阅[Decisioning迁移API指南](../../experience-decisioning/decisioning-migration-api.md)以了解详情。

1. **SMS Webhook**：配置入站Webhook以捕获传入消息和反馈Webhook，从而接收投放接收和状态更新。 [了解详情](../../sms/sms-webhook.md)。

## 测试与调试 {#testing}

1. **调试 SDK 实施**：使用 Adobe Experience Platform Assurance 检查 SDK 事件、验证数据收集并实时排查集成问题。[进一步了解 Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=zh-Hans){target="_blank"}。

1. **测试事件传递**：验证您应用程序发出的事件是否被 Adobe Experience Platform 正确接收并按预期触发历程。监控事件摄取过程并验证有效负载结构。

1. **验证 API 集成**：测试您的自定义操作端点，以确保其能正确处理 Journey Optimizer 请求、在超时限制内响应，并返回预期的数据格式。

1. **对测试轮廓使用测试模式**：与[数据工程师](data-engineer.md)协作获取对测试轮廓的访问权限，然后使用历程测试模式验证您的实施。了解如何[测试历程](../../building-journeys/testing-the-journey.md)。

1. **监控 SDK 日志**：在您的 SDK 实现中启用调试日志记录，以便在开发期间排查问题：
   * **Mobile SDK**：启用日志记录以查看 SDK 事件和 API 调用
   * **Web SDK**：使用浏览器控制台监控 SDK 活动

1. **验证数据流配置**：确保您的数据流已正确配置，可将数据发送至 Journey Optimizer。检查事件是否通过数据流传递至正确的目标位置。

1. **查询历程数据以供分析**：在数据湖上使用 SQL 查询来分析历程步骤事件、调试问题并监控自定义操作性能。探索[用于历程分析的查询示例](../../reports/query-examples.md)，包括：
   * 轮廓进入/退出追踪和丢弃原因分析
   * 自定义操作性能指标（延迟、吞吐量、错误率）
   * 事件交付和错误模式
   * 历程实例状态

## 高级开发人员主题 {#advanced-topics}

### 处理上下文数据和扩充

* **对数组进行迭代**：使用 Handlebars 语法在消息中展示来自事件、自定义操作响应及数据集查询的动态列表。了解[迭代上下文数据](../../personalization/iterate-contextual-data.md)。
* **数据集查找**：实施数据集查找以扩充 Adobe Experience Platform 数据集的历程数据。与您的数据工程师协作进行配置。了解[数据集查找](../../building-journeys/dataset-lookup.md)。

### 处理同意与治理

在集成中实施数据治理和同意策略：

* **数据治理**：将数据使用策略应用于自定义操作。进一步了解[数据治理](../../action/action-privacy.md)。
* **同意管理**：在您的实施中处理客户同意偏好设置。了解[同意](../../action/consent.md)。

### 优化与最佳实践

* **上限和限制**：了解速率限制并实施适当的节流机制。了解[外部系统](../../configuration/external-systems.md)。
* **历程优化**：遵循[历程优化](../../building-journeys/optimize.md)的最佳实践。
* **错误处理**：实施稳健的错误处理机制。查阅[错误代码](../../building-journeys/error-codes-reference.md)及[故障排除指南](../../building-journeys/troubleshooting.md)。

## 其他资源 {#additional-resources}

* **Developer Console**：访问 [Adobe Developer Console](https://developer.adobe.com){target="_blank"} 以创建集成并管理 API 凭据。
* **示例代码**：浏览 [GitHub 上的实施示例](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}。
* **视频教程**：通过 [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=zh-Hans){target="_blank"} 上的实践教程进行学习。
* **开发人员社区**：与其他开发人员联系，并在 Adobe 社区论坛中获取支持。

## 跨角色协作 {#next-steps}

您的实施工作与其他团队成员相互关联：

>[!BEGINTABS]

>[!TAB 与数据工程师协作]

与[数据工程师](data-engineer.md)协作处理数据和事件配置：

* 获取需要实施的 XDM 架构和事件结构
* 了解您需要发送哪些事件及其所需的负载格式
* 就数据收集要求与数据质量标准达成一致
* 共同测试事件传递与数据摄取过程

>[!TAB 与管理员协作]

与[管理员](administrator.md)就访问权限与配置进行协作：

* 为他们将要配置的自定义操作提供 API 规范
* 申请必要的权限和 API 凭据
* 协调渠道配置需求（例如推送证书）
* 就测试环境与沙盒策略达成一致

>[!TAB 与营销人员协作]

与[营销人员](marketer.md)就历程要求和测试进行协作：

* 了解哪些用户交互应该触发事件
* 为内容表现与用户参与实施跟踪机制
* 支持对您已实现功能的历程进行测试
* 排查消息投放或个性化相关的问题

>[!ENDTABS]

## 开始实施

准备好开始构建了吗？从以上部分中选择您的首个实施领域：

1. **移动应用程序？**&#x200B;从 [Mobile SDK 集成](#mobile-integration)开始
2. **网站？**&#x200B;从 [Web SDK 设置](#web-implementation)开始
3. **API 集成？**&#x200B;跳转到[使用 API](#apis) 部分
4. **自定义系统？**&#x200B;查看[自定义操作](#custom-actions)

每个部分都包含指向详细技术文档、代码示例和教程的链接，以指导您的实施工作。
