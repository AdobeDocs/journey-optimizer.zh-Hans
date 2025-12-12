---
title: 开发人员入门
description: 作为开发人员，了解有关如何使用 Journey Optimizer 的更多信息
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: ed3246d0bd552fee9c4df01babe18a5c1acd3b5f
workflow-type: tm+mt
source-wordcount: '1886'
ht-degree: 2%

---

# 开发人员入门 {#get-started-developers}

作为&#x200B;**开发人员**，您负责实施[!DNL Adobe Journey Optimizer]并将其集成到您的应用程序和系统中。 一旦[!DNL Adobe Journey Optimizer]系统管理员[和](administrator.md)数据工程师[向您授予访问权限并准备好环境，您就可以开始使用](data-engineer.md)。

## 您在Journey Optimizer生态系统中的角色

其他团队成员通过用户界面配置Journey Optimizer时，您将专注于：

* 在移动和Web应用程序中&#x200B;**实施SDK**
* 从您的应用程序&#x200B;**发送事件**&#x200B;以触发历程
* **生成API端点**，Journey Optimizer可通过自定义操作调用该端点
* **集成** Journey Optimizer与您现有的系统和基础架构
* **测试和调试**&#x200B;您的实施

您的[数据工程师](data-engineer.md)将处理数据架构、事件配置和数据源。 您的[管理员](administrator.md)将设置权限和渠道配置。 [营销人员](marketer.md)将设计使用您实施的历程和内容。

本指南涵盖了开始使用Journey Optimizer的基本技术实施步骤。 无论您是构建移动应用程序、Web体验还是API集成，请按照以下部分设置您的实施。

## 先决条件 {#prerequisites}

在开始实施之前，请确保您已：

| 类别 | 要求 |
|----------|-------------|
| **技术技能** | *使用JavaScript(适用于Web SDK)或Swift/Kotlin(适用于Mobile SDK)<br>*了解RESTful API和JSON<br>*熟悉异步编程和事件驱动型架构<br>*了解贵组织的应用程序架构 |
| **访问和工具** | *访问[Adobe Developer Console](https://developer.adobe.com){target="_blank"}以获取API凭据<br>*开发环境以访问应用程序的代码库<br>*测试工具，如Postman以获取API测试<br>*浏览器开发人员工具或移动调试工具 |
| **来自其他团队成员** | *您的[管理员](administrator.md)<br>* XDM架构和事件定义授予的环境访问权限来自[数据工程师](data-engineer.md)<br>*来自[营销人员](marketer.md)的要求和用例 |

## 了解技术基础 {#technical-foundation}

在开始实施之前，请熟悉核心技术概念：

1. **Adobe Experience Platform集成**： Journey Optimizer本机构建于Adobe Experience Platform上。 了解底层架构将帮助您构建更有效的实施。 详细了解[Journey Optimizer的工作方式](../understanding-ajo.md)。

1. **XDM数据模型**： Journey Optimizer使用Experience Data Model (XDM)来构造事件和配置文件数据。 作为开发人员，您需要了解如何发送符合[数据工程师](data-engineer.md)配置的架构的数据。 了解[XDM架构](../../data/get-started-schemas.md)。

1. **身份验证和安全性**：所有实施都需要正确的身份验证。 了解如何设置SDK和API的身份验证。 了解[API身份验证](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}。

## 设置移动应用程序集成 {#mobile-integration}

### 配置Adobe Experience Platform Mobile SDK

要启用推送通知、应用程序内消息和其他移动功能，请将Adobe Experience Platform Mobile SDK集成到您的移动应用程序中。

1. **安装和配置Mobile SDK**：按照[Adobe Experience Platform Mobile SDK文档](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"}操作，开始使用SDK集成。

1. **创建移动属性**：在[!DNL Adobe Experience Platform Data Collection]中设置移动属性。 了解如何[创建和配置移动属性](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}。

1. **配置推送通知**：
   * 对于&#x200B;**iOS应用程序**：向APN注册应用程序(Apple推送通知服务)。 请参阅[Apple的文档](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}以了解详情。
   * 对于&#x200B;**Android应用程序**：为Android应用程序设置Firebase Cloud Messaging。 请参阅[Google的文档](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}以了解详情。

1. **测试您的移动集成**：使用[移动入门快速启动工作流](../../push/mobile-onboarding-wf.md)快速配置和测试您的移动设置。

在[此页面](../../push/push-configuration.md)上提供了配置推送通知的详细步骤。

### 实施基于代码的体验(Mobile SDK)

对于使用基于代码的体验的本机移动设备应用程序个性化：

* 有关Mobile SDK实施的信息，请按照[本教程](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"}操作
* 查看[iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"}和[Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}的实施示例

## 实施Web体验 {#web-implementation}

### 设置Adobe Experience Platform Web SDK

对于基于Web的实施，Web SDK是您的主要集成点：

1. **安装Web SDK**：按照[Web SDK实施指南](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"}在您的网站上设置SDK。

1. **配置数据流**：在[!DNL Adobe Experience Platform Data Collection]中创建并配置启用了Journey Optimizer的数据流。 请参阅[数据流文档](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hans){target="_blank"}以了解详情。

1. **启用Web推送通知**（可选）：在Web SDK配置中配置[pushNotifications属性](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"}，并使用[sendPushSubscription命令](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"}注册推送订阅。

### 实施基于代码的体验(Web SDK)

基于代码的体验允许您个性化任何数字接触点：

1. **选择实施方法**：客户端、服务器端或混合。 查看每种方法的[实施示例](../../code-based/code-based-implementation-samples.md)。

1. **定义表面**：识别应用程序中要交付个性化内容的位置。 了解[表面配置](../../code-based/code-based-surface.md)。

1. **实施内容渲染**：使用Web SDK获取和应用个性化内容。 请参阅[基于代码的实现教程](../../code-based/code-based-decisioning-implementations.md)。

1. **发送显示和交互事件**：跟踪内容显示时间以及用户与内容交互以进行分析和优化的时间。

浏览GitHub [上的](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}示例实施，以查看基于代码的体验的实际操作情况。

了解有关[基于代码的体验快速入门](../../code-based/get-started-code-based.md)的更多信息。

## 实施事件流 {#event-streaming}

### 发送事件以触发历程

作为开发人员，您将实施代码以发送触发历程的事件。 您的[数据工程师](data-engineer.md)将在Journey Optimizer中配置事件架构和定义。

1. **了解事件有效负载**：与数据工程师合作，获取事件架构和所需的有效负载结构。 有效负载必须符合其配置的XDM架构。 了解[事件架构要求](../../event/experience-event-schema.md)。

1. **实施事件流式传输**：使用[流式引入API](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hans){target="_blank"}将事件发送到Adobe Experience Platform。 了解发送事件的[步骤](../../event/additional-steps-to-send-events-to-journey.md)。

1. **处理事件类型**：
   * **单一事件**：为特定于人员的操作（例如，按钮点击、购买完成）实施事件发送
   * **业务活动**：发送与业务相关的活动（例如，库存更新、价格变动）

1. **测试事件交付**：验证是否正确接收了事件并按预期触发历程。 了解[事件疑难解答](../../building-journeys/troubleshooting-inbound.md)。

通过API发送事件的&#x200B;**示例实施**：

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

了解有关[处理历程事件](../../event/about-events.md)的更多信息。

## 开发自定义操作端点 {#custom-actions}

自定义操作允许历程调用您的API。 作为开发人员，您将构建自定义操作调用的API端点：

1. **构建您的API端点**：创建Journey Optimizer将在历程执行期间调用的RESTful API端点。 您的端点应：
   * 接受JSON负载
   * 身份验证请求（OAuth、API密钥或JWT）
   * 在适当的超时限制内处理请求
   * 以预期格式返回响应

1. **了解自定义操作功能**：自定义操作可以连接到第三方系统，如Epsilon、Slack、Firebase或您自己的服务。 详细了解[自定义操作](../../action/action.md)。

1. **使用操作配置**：您的[管理员](administrator.md)或[数据工程师](data-engineer.md)将在Journey Optimizer中配置自定义操作，定义API终结点URL、身份验证方法和参数。 您将向他们提供您的API规范。 了解[自定义操作配置](../../action/about-custom-action-configuration.md)。

1. **返回可操作数据**：设计您的API以返回可在后续历程步骤中使用的数据。 了解[操作响应](../../action/action-response.md)。

1. **实施速率限制**：确保您的端点可以处理预期的卷。 Journey Optimizer应用5000次呼叫/秒限制，但您的系统应具有弹性。 了解[上限和限制](../../configuration/external-systems.md)。

**示例用例**：[使用自定义操作将历程事件写入Experience Platform](../../building-journeys/custom-action-aep.md)。

## 使用 Journey Optimizer API {#apis}

Journey Optimizer为程序化访问提供了全面的REST API：

1. **了解API功能**： Journey Optimizer API允许您以编程方式创建、读取、更新和删除各种资源。 了解[Journey Optimizer API](../../configuration/ajo-apis.md)。

1. **身份验证**：按照[本教程](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}中的说明，使用Adobe Developer Console设置API身份验证。

1. **浏览API引用**：浏览完整的API文档，并直接在[Adobe Journey Optimizer API引用](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}中尝试API。

1. **API触发的营销活动**：使用API触发的营销活动生成事务型消息传递。 对于大容量方案（最多5000 TPS），请探索[高吞吐量模式](../../campaigns/api-triggered-high-throughput.md) （需要附加许可证）。

1. **决策管理API**：使用专门的API进行优惠管理和决策。 请参阅[决策管理API指南](../../offers/api-reference/getting-started.md)以了解详情。

## 测试和调试 {#testing}

1. **调试SDK实施**：使用Adobe Experience Platform Assurance实时检查SDK事件、验证数据收集并排查集成问题。 [进一步了解Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html){target="_blank"}。

1. **测试事件投放**：验证Adobe Experience Platform是否正确接收来自您应用程序的事件，并正常触发历程。 监测事件摄取并验证有效负载结构。

1. **验证API集成**：测试您的自定义操作端点，以确保它们正确处理Journey Optimizer请求，在超时限制内响应，并返回预期的数据格式。

1. **对测试配置文件使用测试模式**：与您的[数据工程师](data-engineer.md)合作，获取对测试配置文件的访问权限，然后使用历程测试模式验证您的实施。 了解如何[测试历程](../../building-journeys/testing-the-journey.md)。

1. **监视SDK日志**：在SDK实现中启用调试日志记录以解决开发过程中的问题：
   * **Mobile SDK**：启用日志记录以查看SDK事件和API调用
   * **Web SDK**：使用浏览器控制台监视SDK活动

1. **验证数据流配置**：确保您的数据流已正确配置为将数据发送到Journey Optimizer。 检查事件是否通过数据流流向正确的目标。

1. **查询历程数据以供分析**：对数据湖使用SQL查询来分析历程步骤事件、调试问题和监视自定义操作性能。 探索历程分析的[查询示例](../../reports/query-examples.md)，包括：
   * 配置文件进入/退出跟踪和放弃原因
   * 自定义操作性能指标（延迟、吞吐量、错误）
   * 事件交付和错误模式
   * 历程实例状态

## 高级开发人员主题 {#advanced-topics}

### 使用上下文数据和扩充

* **通过数组进行迭代**：使用Handlebars语法在消息中显示来自事件、自定义操作响应和数据集查找的动态列表。 了解[迭代上下文数据](../../personalization/iterate-contextual-data.md)。
* **数据集查找**：实施数据集查找以扩充Adobe Experience Platform数据集的历程数据。 与您的数据工程师合作进行配置。 了解[数据集查找](../../building-journeys/dataset-lookup.md)。

### 在同意和治理下工作

在集成中实施数据治理和同意策略：

* **数据管理**：将数据使用策略应用于自定义操作。 了解有关[数据管理](../../action/action-privacy.md)的更多信息。
* **同意管理**：在您的实施中处理客户同意首选项。 了解[同意](../../action/consent.md)。

### 优化和最佳实践

* **上限和限制**：了解速率限制并实施适当的限制。 了解[外部系统](../../configuration/external-systems.md)。
* **历程优化**：遵循[历程优化](../../building-journeys/optimize.md)的最佳实践。
* **错误处理**：实现可靠的错误处理。 查看[错误代码](../../building-journeys/error-codes-reference.md)和[疑难解答指南](../../building-journeys/troubleshooting.md)。

## 其他资源 {#additional-resources}

* **Developer Console**：访问[Adobe Developer Console](https://developer.adobe.com){target="_blank"}以创建集成并管理API凭据。
* **示例代码**：浏览GitHub上的[示例实施](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}。
* **教程视频**：学习有关[Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=zh-Hans){target="_blank"}的动手教程。
* **开发人员社区**：与其他开发人员联系，并在Adobe社区论坛中获取支持。

## 跨角色协作 {#next-steps}

您的实施工作与其他团队成员相交：

>[!BEGINTABS]

>[!TAB 与数据工程师合作]

与[数据工程师](data-engineer.md)协作处理数据和事件配置：

* 获取需要实施的XDM架构和事件结构
* 了解您需要发送哪些事件及其所需的有效负载格式
* 符合数据收集要求和数据质量标准
* 同时测试事件交付和数据摄取

>[!TAB 与管理员合作]

与[管理员](administrator.md)协作访问和配置：

* 为要配置的自定义操作提供API规范
* 请求必要的权限和API凭据
* 协调渠道配置要求（如推送证书）
* 根据测试环境和沙盒策略进行调整

>[!TAB 与营销人员合作]

与[营销人员](marketer.md)就历程要求和测试进行协作：

* 了解哪些用户交互应该触发事件
* 实施内容性能和用户参与跟踪
* 支持使用您实施的功能测试历程
* 消息投放或个性化问题的故障诊断

>[!ENDTABS]

## 保持最新

跟上最新的Journey Optimizer功能和技术变化：

* **[发行说明](../../rn/release-notes.md)**：查看每月发布的新功能、API更改、SDK更新和错误修复
* **[文档更新](../../rn/documentation-updates.md)**：跟踪技术文档的最新更改，包括新的实施指南和代码示例
* **[产品通知](../../rn/releases.md#staying-informed)**：了解如何订阅有关Journey Optimizer更新的电子邮件和产品内通知，包括新的SDK版本、API更改、重大更改和关键安全更新

## 开始实施

准备好开始构建了吗？ 从以上部分中选择您的第一个实施区域：

1. **移动应用？**&#x200B;从[Mobile SDK集成](#mobile-integration)开始
2. **网站？**&#x200B;以[Web SDK安装程序](#web-implementation)开始
3. **API集成？**&#x200B;跳转到[使用API](#apis)
4. **自定义系统？**&#x200B;签出[自定义操作](#custom-actions)

每个部分都包含指向详细技术文档、代码示例和教程的链接，以指导您的实施。
