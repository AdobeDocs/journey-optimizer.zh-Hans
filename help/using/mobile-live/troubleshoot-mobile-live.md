---
solution: Journey Optimizer
product: journey optimizer
title: 实时活动故障诊断
description: 了解如何针对单一和广播用例（包括用户档案令牌问题、营销活动配置和投放失败）对Journey Optimizer中的实时活动进行故障排除
role: User
level: Intermediate
source-git-commit: b71dbb0e4987cfc879a7b153d5c1453d6c220bf9
workflow-type: tm+mt
source-wordcount: '4503'
ht-degree: 1%

---


# 实时活动故障诊断 {#troubleshoot-mobile-live}

Adobe Journey Optimizer中的实时活动支持在iOS锁屏界面和Dynamic Islands上进行实时、动态更新。 它们只能通过API触发的营销活动来触发和管理。

**用例类型：**

* **单一**：单独定位、事务性（API触发的事务性营销活动）
* **广播**：面向受众的大规模投放（API触发的营销活动）

实时活动的一个常见挑战是，用于触发或更新实时活动的API调用返回&#x200B;**成功响应(200 OK)**，但实时活动无法在用户的设备上显示或更新。 API确认与实际设备行为之间的这种断开可能会在投放管道中的多个点发生。 本指南提供了一种系统化的故障排除方法来识别投放失败的位置，通过设备渲染检查API请求验证中的每个阶段。

## 先决条件

在进行故障诊断之前，请确保您已：

* &#x200B;
  +++ 设置Assurance会话

  设置&#x200B;**Assurance会话**&#x200B;以捕获SDK事件并检查投放管道。 Assurance提供以下可视性：

   * Edge Network请求和响应
   * 配置文件资格事件
   * 推送令牌注册
   * 实时活动生命周期事件

  请参阅[Assurance文档](https://experienceleague.adobe.com/zh-hans/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance)以了解如何设置Adobe Experience Platform Assurance。

  **注意**：对于iOS Live Activity，请确保您的应用程序在物理iOS设备(iOS 16.1或更高版本)或Xcode模拟器(iOS 16.1或更高版本)上运行。

  +++

* &#x200B;
  +++ 收集API触发的营销活动详细信息

  导航到Journey Optimizer中的API触发的营销活动，并检索：

   * 营销活动名称
   * 在URL或营销活动属性中找到的营销活动ID
   * Campaign版本（如果适用）
   * 表面配置，用于实时活动的iOS应用程序表面

  +++

* &#x200B;
  +++ 收集API请求信息

  在进行API调用以触发实时活动时，保存：

   * API请求负载，包括配置文件标识符和实时活动数据
   * api响应，包括状态代码、消息ID、请求ID
   * 调用API的时间戳
   * 使用的端点，例如`/campaign/{CAMPAIGN_ID}/execute`

  +++

* &#x200B;
  +++ 识别测试用户档案

  从您的API请求中检索：

   * 配置文件命名空间，例如ECID、电子邮件、客户ID
   * API调用中使用的配置文件ID

  确保您可以在Adobe Experience Platform中查找此配置文件。 在Experience Platform文档[中了解如何](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide.html)查找配置文件。

  +++

* &#x200B;
  +++ 设备和应用程序信息

  从测试设备收集以下信息：

   * 设备型号，例如iPhone 14 Pro
   * iOS版本
   * 应用程序包标识符
   * APN推送令牌
   * 测试时的网络连接状态

  +++

## 常见应用场景

### 配置文件或推送令牌问题 {#profile-issue}

[!BADGE 适用于单一和广播用例]{type=Positive}

API返回HTTP 200，但未显示实时活动。 常见原因：

* Adobe Experience Platform中不存在配置文件。
* 实时活动推送令牌尚未同步到配置文件。
* 实时活动推送详细信息已同步，但包含不正确的配置，例如错误的`appId`或`attributeType`。

**注意广播用例**：如果受众中的某些配置文件缺少令牌，则只有这些配置文件将无法接收实时活动。 从受众中取样多个配置文件以诊断令牌问题。 这仅适用于远程启动事件，不适用于更新或结束事件。

#### 预检查

* iOS应用程序要求：
   * iOS 16.1+
   * 在`NSSupportsLiveActivities`中将`YES`设置为`Info.plist`
   * `ActivityAttributes`已正确实施。
* 移动SDK集成：
   * Adobe Experience Platform Mobile SDK (消息传送SDK 5.11.0+)
   * 使用Live Activity推送令牌实施和调用了`Messaging.registerLiveActivities`。

#### 调试步骤

1. &#x200B;
   +++ 验证Adobe Experience Platform中存在配置文件

   1. 在Journey Optimizer中，导航到&#x200B;**客户** `>` **配置文件**。
   1. 使用API请求中的命名空间和身份值搜索。
   1. 如果找不到配置文件，则该配置文件不存在或摄取未完成。 在触发实时活动之前创建配置文件或等待摄取。
   1. 如果找到配置文件，请继续执行下面的步骤2以检查推送令牌是否已同步。

      +++

1. &#x200B;
   +++ 检查实时活动推送令牌是否已同步

   您可以使用Assurance验证令牌注册：

   1. 在Assurance中，从&#x200B;**事件**&#x200B;列表中，过滤或搜索事件`eventType = "liveActivity.pushToStart"`。
   1. 选择&#x200B;**事件**&#x200B;并检查有效负载。
   1. 检查是否存在令牌、appId和attributeType值。
   1. 确认事件是否已成功发送。

   您还可以签入Adobe Experience Platform配置文件。

   1. 在Adobe Experience Platform中，从您的&#x200B;**配置文件**&#x200B;访问&#x200B;**事件**&#x200B;选项卡。
   1. 搜索`liveActivity.pushToStart`事件。
   1. 检查偶数时间戳和有效负载。

   如果未找到任何事件，则表示您的移动应用无法正确调用`Messaging.registerLiveActivity`。 您需要修复SDK集成。

   +++

1. &#x200B;
   +++ 验证配置文件上的令牌详细信息

   1. 从您的&#x200B;**配置文件**，访问&#x200B;**属性**&#x200B;选项卡。
   1. 找到`liveActivityPushNotificationDetails`。
   1. 验证令牌配置：

      ```json
      {
        "liveActivityPushNotificationDetails": [
          {
            "appId": "com.example.myapp",
            "token": "abc123def456...",
            "platform": "apns",
            "denylisted": false,
            "attributeType": "OrderTrackingAttributes",
            "identity": {}
          }
        ]
      }
      ```

   **验证每个字段：**

   | 字段 | 要求 | 常见问题 |
   |-|-|-|
   | `appId` | 必须与iOS捆绑包标识符完全匹配 | 开发/生产捆绑包ID不匹配 |
   | `attributeType` | 必须完全匹配Swift `ActivityAttributes`结构名称（区分大小写） | 结构名称拼写错误或不正确 |
   | `platform` | 必须为`"apns"`或`"apnsSandbox"` | 平台值错误 |
   | `denylisted` | 必须为`false` | 令牌标记为无效或用户选择退出 |
   | `token` | 有效的APN推送令牌 | 令牌已过期或重新安装应用程序 |

   如果有任何字段不正确：更新移动应用程序，使用`Messaging.registerLiveActivities`重新注册，等待5-10分钟，然后重新检查。

   如果`liveActivityPushNotificationDetails`缺失：令牌尚未同步。 在Assurance中看到`liveActivity.pushToStart`事件后等待5-10分钟。

   +++

### Campaign配置和有效负载问题 {#payload-issues}

[!BADGE 适用于单一和广播用例]{type=Positive}

存在带有效令牌的配置文件，但未显示实时活动。 这可能是由于：

* 错误的表面或渠道配置。
* API有效负载结构不正确。
* `content-state`和`attributes`与iOS `ActivityAttributes`实现不匹配。
* `timestamp`过时（对于更新/结束至关重要）。

**广播用例的注意事项**：营销活动必须是&#x200B;**API触发的营销**（非事务性）。 有效负载使用`audience`，而不是单个`profile`。 有关广播特定的有效负荷结构，请参阅[此部分](#broadcast-config)；有关完整的API规范，请参阅[Adobe Developer文档](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMAudienceMessageExecution)。

#### 预检查

* Campaign是&#x200B;**API触发的事务性** （单一）或&#x200B;**API触发的营销** （广播），并且&#x200B;**高吞吐量**&#x200B;选项必须&#x200B;**不**&#x200B;启用，因为它与实时活动不兼容。
* 使用上述[方案](#profile-issue)，确保配置文件存在且令牌已正确同步。

#### 调试步骤

1. &#x200B;
   +++ 验证营销活动表面配置

   1. 在Journey Optimizer中，打开您的&#x200B;**营销活动**&#x200B;并导航到&#x200B;**操作**&#x200B;菜单。
   1. 检查您的&#x200B;**实时活动配置**。 必须为iOS应用配置表面，使其包标识符与您配置文件`appId`中的`liveActivityPushNotificationDetails`匹配。 例如，如果您的配置文件具有`"appId": "com.example.myapp"`，则表面必须针对同一应用程序。
   1. 检查营销活动配置中的&#x200B;**活动类型**&#x200B;是否与用户档案的`attributeType`中的`liveActivityPushNotificationDetails`完全匹配。 例如，如果您的配置文件具有`"attributeType": "FoodDeliveryLiveActivityAttributes"`，则营销活动必须指定此相同的活动类型。

      +++

1. &#x200B;
   +++验证API有效负荷结构

   通过API执行活动时，请确保有效负载遵循正确结构。

   **单一有效负载：**

   ```json
   {
     "campaignId": "your-campaign-id",
     "recipients": [{
       "type": "aep",
       "userId": "user@example.com",
       "namespace": "email",
       "context": {
         "requestPayload": {
           "aps": {
             "content-available": 1,
             "timestamp": 1756984054,
             "event": "start",
             "attributes-type": "FoodDeliveryLiveActivityAttributes",
             "content-state": { ... },
             "attributes": { ... }
           }
         }
       }
     }]
   }
   ```

   **常见有效负载问题：**

   | 字段 | 要求 | 常见问题 |
   |-|-|-|
   | `attributes-type` | 必须匹配促销活动类型和配置文件`attributeType` | 不匹配或拼写错误 |
   | `campaignId` | 必须匹配激活的营销活动ID | 营销活动ID错误或缺失 |
   | `content-available` | 必须为`1` | 值缺失或错误 |
   | `event` | 必须为`"start"`、`"update"`或`"end"` | 事件类型无效 |
   | `timestamp` | 必须始终为当前/最新Unix纪元时间（以秒为单位） | 使用旧/缓存的时间戳 |
   | `userId` / `namespace` | 必须匹配AEP中的现有配置文件 | 配置文件标识符不匹配 |

   **关键：始终使用最新的时间戳**

   * 在发出每个API调用时，`timestamp`字段必须&#x200B;**始终**&#x200B;为当前&#x200B;**Unix纪元时间**（秒）。
   * 这适用于&#x200B;**所有事件类型**： `start`、`update`和&#x200B;**，特别是`end`**。
   * **对更新/结束请求的影响**：使用过时的或旧的时间戳将导致更新和结束请求失败或被设备忽略。
   * 请&#x200B;**不**&#x200B;重复使用以前请求中的时间戳或使用缓存的值。
   * 为每个API调用生成新的时间戳。

   **可选字段（所有事件类型）：**

   * `requestId`：用于跟踪的唯一标识符（推荐）。
   * `alert`：通知对象为`title`和`body`（用于提醒注意更新）。

   **关于`dismissal-date`：**

   * 包含Unix纪元时间（秒）的可选字段。
   * **仅在`event: "end"`**&#x200B;时相关。
   * 指定何时应自动从设备中删除实时活动。
   * 如果未在最终事件中提供，实时活动将保持可见，直到用户将其消除。
   * 必须为未来的时间戳（晚于`timestamp`）。

     +++

1. &#x200B;
   +++ 将有效负载与iOS实施保持一致

   确保API有效负载与iOS应用程序的`ActivityAttributes`实施相匹配。 Adobe SDK的`LiveActivityAttributes`协议扩展了iOS `ActivityAttributes`，并且需要`liveActivityData`属性。

   **验证映射：**

   1. 您的`ActivityAttributes`必须实施Adobe的`LiveActivityAttributes`协议。 示例：

      ```swift
      struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
       public struct ContentState: Codable, Hashable {
           var orderStatus: String
           var estimatedDeliveryTime: String
       }
      
       // Adobe SDK requirement
       var liveActivityData: LiveActivityData
      
       // Your custom attributes
       var restaurantName: String
      }
      ```

      **请注意** `liveActivityData`字段是Adobe SDK的必需字段，必须包含在所有实现中。

   1. 您的API有效负载必须镜像iOS结构：

      ```json
      {
        "aps": {
           "event": "start",
           "timestamp": 1756984054,
           "attributes-type": "FoodDeliveryLiveActivityAttributes",
           "content-state": {
           "orderStatus": "Preparing",
           "estimatedDeliveryTime": "20 mins"
        },
        "attributes": {
          "liveActivityData": {
            "liveActivityID": "order-12345"
          },
          "restaurantName": "Pizza Palace"
        }
        }
      }
      ```

   **验证核对清单：**

   * 在`ContentState`中包含所有`content-state`字段（所有事件类型均需要该字段）。
   * 包括`LiveActivityAttributes`中的所有`attributes`字段（仅限开始事件），包括：
      * `liveActivityData` （必需；通常包含`liveActivityID`或类似的标识符）
      * 结构中的所有自定义字段
   * 完全匹配字段名称（区分大小写）。
   * 匹配数据类型（String、Int、Bool、嵌套对象）。
   * 保留嵌套的对象结构。

   **常见错误：**

   | 问题 | 影响 | 修复 |
   |-------|--------|-----|
   | 属性中缺少`liveActivityData` | 实时活动将不会启动 | 在开始事件中始终包含`liveActivityData`对象 |
   | 开始事件中缺少必填字段 | 实时活动将不会启动 | 从iOS结构添加所有字段 |
   | 字段名称错误（拼写错误/大小写） | 字段被忽略或分析错误 | 完全匹配iOS字段名称 |
   | 错误的数据类型 | 解析错误 | 匹配iOS数据类型 |
   | 缺少嵌套对象 | 不完整数据 | 包括所有嵌套结构 |
   | 更新/结束中包括`attributes` | 不需要，但通常被忽略 | 在开始事件中仅包括`attributes` |
   | 更新/结束时的过期时间戳 | 设备忽略更新/结束 | 始终生成新的时间戳 |

   有关更多示例，请参阅[创建实时活动页面](create-mobile-live.md)。

   +++

1. &#x200B;
   +++ 使用Assurance进行测试

   使用Assurance验证API执行和有效负载投放：

   1. 打开Assurance会话。
   1. 执行API调用以触发实时活动。
   1. 在&#x200B;**事件列表**&#x200B;中，检查：
      * 营销活动执行事件。
      * 实时活动交付活动。
      * 有效负载验证错误事件。
   1. 查看事件负载以验证：
      * 已正确处理有效负载。
      * 未发生验证错误。
      * 实时活动已发送到APN。

      +++

### 投放失败和错误分析

[!BADGE 适用于单一和广播用例]{type=Positive}

在此方案中，所有先前的检查均已通过：

* 存在具有[有效实时活动推送令牌的配置文件](#profile-issue)
* 营销活动已使用正确的负载[正确配置](#payload-issues)
* [更新令牌已同步](#token-not-synced)（仅用于更新/结束事件，单一用例）

但实时活动仍无法按预期显示、更新或结束。 问题可能出在Adobe交付系统级别，也可能出在推送通知服务提供商(APN)身上。

**广播用例的注意事项**：报表显示所有受众成员的量度。 某些配置文件可能会成功，而其他配置文件则会失败。

**预检查**

* **已验证的以前方案：**
   * 存在具有正确`liveActivityPushNotificationDetails`的配置文件
   * 营销活动平面和活动类型正确
   * API有效负载包含当前时间戳
   * 更新令牌已同步（对于更新/结束事件）

* **API调用已确认：**

   * API调用返回了HTTP 200（成功）
   * 活动ID和收件人详细信息正确

#### 调试步骤

1. &#x200B;
   +++ 检查营销活动报告

   1. 导航到您的&#x200B;**实时活动营销活动**。
   1. 单击&#x200B;**报表**&#x200B;按钮。
   1. 选择&#x200B;**查看所有时间报表**。
   1. 请查看以下部分：

      1. 检查&#x200B;**发送统计数据**&#x200B;量度以了解发送成功：

         | 量度 | 它的含义 | 要查找的内容 |
         |-|-|-|
         | 已定位 | 符合受众条件的配置文件数 | 应包含您的测试用户档案 |
         | 发送 | 尝试的推送通知总数 | 应与您的API调用匹配 |
         | 已送达 | 已成功交付到设备 | 比较发送以查看成功率 |
         | 发送错误 | 发送失败的推送通知 | 高数字 |
         | 发送排除项 | Adobe Journey Optimizer排除的用户档案 | 检查您的配置文件是否已被排除 |

      1. 如果发送错误> 0，请检查&#x200B;**错误原因**&#x200B;表以了解具体的错误代码和消息：

         | 常见错误 | 含义 | 解决方法 |
         |-|-|-|
         | 标记无效 | 推送令牌无效或已过期 | 从设备重新注册实时活动令牌 |
         | 未找到标记 | 没有与配置文件关联的有效令牌 | 验证`liveActivityPushNotificationDetails`是否存在 |
         | 已拒绝APN | Apple推送通知服务拒绝了推送 | 检查APNs证书、捆绑包ID、环境 |
         | 网络超时 | 无法访问APN | 暂时性问题；重试API调用 |

      1. 如果&#x200B;**发送排除项** > 0，请检查&#x200B;**排除的原因**&#x200B;表：

         | 常见排除项 | 含义 | 解决方法 |
         |-|-|-|
         | 配置文件已选择退出 | 用户已选择退出通知 | 检查配置文件同意状态 |
         | 列入阻止列表令牌 | 令牌标记为无效 | 重新注册令牌或检查阻止列表状态 |
         | 配置文件不符合条件 | 配置文件不符合营销活动标准 | 查看活动受众规则 |

   在[实时活动营销活动报告页面](../reports/campaign-global-report-cja-activity.md)中了解详情。

   +++

1. &#x200B;
   +++ 查看用户档案中的消息反馈事件

   1. 在Journey Optimizer中导航到&#x200B;**客户** > **配置文件**。
   1. 搜索并打开配置文件。
   1. 选择&#x200B;**事件**&#x200B;选项卡。
   1. 筛选或搜索具有`eventType = "message.feedback"`的事件。
   1. 查找与实时活动的`liveActivityID`和`event`类型匹配的反馈事件。
   1. 查看以下关键字段：

      | 字段 | 可能值 | 它的含义 |
      |-|-|-|
      | `feedbackStatus` | `sent`、`error`、`denylist` | 来自服务提供商的投放结果 |
      | `serviceProvider` | `apns/apnsSandbox` | 应为iOS Live活动的APN |
      | `errorCode` | 数字代码或`null` | APNs特定的错误代码（如果失败） |
      | `errorMessage` | 错误描述或`null` | 人工可读的错误消息 |

   1. **如果`feedbackStatus: "error"`：**
      * 检查`errorCode`和`errorMessage`中的特定APN错误
      * 常见的APN错误包括令牌过期、证书无效、捆绑包ID错误

   1. **如果未找到反馈事件：**
      * 可能尚未尝试推送通知
      * 检查营销活动报告中是否排除了用户档案（如上面的步骤1所述）。

      +++

1. &#x200B;
   +++ 在Assurance中验证将实时活动交付给APN

   1. 打开Assurance会话，它在API调用期间必须处于活动状态。
   1. 执行API调用（开始、更新或结束）。
   1. 在&#x200B;**事件列表**&#x200B;中，查找实时活动投放事件。
   1. 搜索与APNs推送投放相关的事件。
   1. 检查以下指示器：
      * **向APNs推送请求**：确认Adobe已向Apple的服务器发送推送请求
      * **APNs响应**：显示APNs是接受还是拒绝推送
      * **投放状态**：成功或失败指示
   1. 如果发现问题，请参阅以下常见的APN传送问题：

      | 问题 | Assurance中的症状 | 解决方法 |
      |-|-|-|
      | APNs证书已过期 | 身份验证错误 | 续订并上传新的APNs证书 |
      | 错误的环境（开发环境与生产环境） | 令牌不匹配错误 | 确保证书与应用程序生成类型匹配 |
      | 捆绑ID不匹配 | 捆绑包标识符无效 | 验证证书包ID是否与应用程序匹配 |
      | 令牌已过期 | 来自APN的InvalidToken错误 | 重新注册实时活动令牌 |
      | 限速 | 请求过多 | 降低API调用频率 |

      +++

1. &#x200B;
   +++ 继续其他诊断检查

   1. 查看营销活动报告中的实时活动生命周期量度。

      在营销活动报告中，查看&#x200B;**实时活动生命周期**&#x200B;部分：

      | 量度 | 检查内容 |
      |-|-|
      | 远程启动 | 应显示API触发的开始计数 |
      | 更新 | 应显示更新事件计数 |
      | 结束 | 应显示结束事件计数 |
      | 总计计数 | 整个实时活动活动量 |

      如果这些指标为零或与您的API调用不匹配，则Adobe与APN之间存在交付问题。

   1. 如果Adobe显示已成功交付，但设备未显示实时活动：

      * 查看iOS设备日志以了解实时活动错误。
      * 验证应用程序是否处于前台或后台（未终止）。
      * 确认设备具有网络连接。
      * 在多个设备上测试以排除特定于设备的问题。
      * 验证iOS的版本是否为16.1或更高版本。

      +++

1. &#x200B;
   +++ 上报至Adobe支持

   如果您已完成所有步骤，但问题仍未解决，请通过以下方式联系Adobe客户关怀团队：

   **必需的信息：**

   * 营销活动 ID 和名称
   * 配置文件命名空间和ID
      * API有效负载中的`liveActivityID`
   * API调用时间戳
   * 屏幕截图：
      * 营销活动报告（发送统计数据、错误原因、排除的原因）
      * 配置文件事件(`liveActivity.updateToken`， `message.feedback`)
      * 显示投放事件的Assurance会话
   * 完成API请求负载
   * APNs证书详细信息（到期、环境、捆绑包ID）

     +++

## 单一特定方案

### 实时活动更新令牌未同步{#token-not-synced}

实时活动在设备上成功启动，但后续`update`或`end` API调用（返回HTTP 200）无法更新或取消实时活动。 当&#x200B;**Live Activity更新令牌**&#x200B;未正确同步到Adobe的系统时，会发生这种情况。

**了解更新令牌**

当活动在设备上启动时，iOS会为该特定活动实例生成一个唯一的更新令牌。 以下项需要此令牌：

* 向实时活动发送更新
* 远程结束实时活动

每个实时活动实例都有自己的唯一更新令牌。 Adobe需要此令牌来提供更新和结束事件。

**预期行为**

要使更新和结束事件正常工作，必须发生以下情况：

1. 在设备上成功启动实时活动。
1. 设备为该Live Activity实例生成更新令牌。
1. Mobile SDK可捕获更新令牌并将其发送到Adobe。
1. 更新令牌已同步并存储在Adobe的系统中。
1. 后续的更新/结束API调用使用此令牌进行交付。

**预检查：**

* **用户权限**：首次在设备上启动实时活动时，iOS会显示系统提示：“允许[应用程序名称]提供实时活动更新？” 用户&#x200B;**必须点按“允许”**&#x200B;才能生成并同步更新令牌。 如果用户点按“不允许”，则不会创建任何更新令牌，并且更新/结束请求将失败。 这是每个应用程序的一次性权限。
* **个人资料和营销活动验证**：完成[方案1](#profile-issue)和[方案2](#payload-issues)检查，以确保个人资料、令牌和营销活动配置正确。

#### 调试步骤

1. &#x200B;
   +++ 验证Assurance中的更新令牌同步

   1. 打开Assurance会话。
   1. 确保当活动在设备上启动时，会话处于活动状态。
   1. 筛选或搜索具有`eventType = "liveActivity.updateToken"`的事件。
   1. 选择事件并检查有效负载：

      * 验证`token`字段是否包含有效的更新令牌字符串。
      * 检查`liveActivityID`是否与您的实时活动实例匹配。
      * 确认`activityType`与您的`attributes-type`匹配。

   1. 如果找不到事件：

      * SDK未生成或捕获更新令牌。
      * 检查用户是否被授予实时活动权限。
      * 验证是否已在设备上成功启动实时活动。
      * 确认移动设备SDK已正确集成以捕获更新令牌。

   1. 如果找到事件，请继续执行步骤2。

      +++

2. &#x200B;
   +++ 验证配置文件事件中的更新令牌

   1. 在Journey Optimizer中导航到&#x200B;**客户** > **配置文件**。
   1. 搜索并打开配置文件。
   1. 选择&#x200B;**事件**&#x200B;选项卡。
   1. 查找`liveActivity.updateToken`事件。
   1. 检查事件详细信息：

      * 验证时间戳是否为最新（与实时活动开始的时间匹配）。
      * 确认`token`和`liveActivityID`存在。
      * 确保`activityType`正确。

   1. 如果在配置文件中未找到事件：

      * 可能尚未将更新令牌事件引入配置文件。
      * 等待5-10分钟，然后重新检查。
      * 如果15分钟后仍然缺失，则可能存在事件摄取问题。

   1. 如果找到事件，则表示更新令牌已同步。 您可以继续执行步骤3。

      +++

3. &#x200B;
   +++ 在Assurance中查看实时活动交付事件

   1. 在Assurance会话中，执行更新或结束API调用。
   1. 在&#x200B;**事件列表**&#x200B;中，查找实时活动投放事件（APNs推送事件）。
   1. 检查事件以指示：
      * 推送通知已发送到APN。
      * 来自APN的响应（成功或错误）。
      * 投放确认。
   1. 如果存在APNs投放事件：已发送推送通知。 如果设备仍未更新，则问题可能出在设备端（应用程序无法处理推送、网络问题等）。
   1. 如果缺少APNs投放事件：更新令牌可能未正确存储，或者未与Adobe系统中的用户档案关联。
   1. 如果存在错误事件：检查错误详细信息中的特定失败原因（无效令牌、APN被拒绝等）。

      +++

## 广播特定的场景

### 广播营销活动配置和有效负荷问题{#broadcast-config}

此部分介绍了特定于广播实时活动的故障排除方案，这些方案需要与单一营销活动不同的调试方法。

当配置文件具有有效令牌，但受众成员的实时活动未按预期显示、更新或运行时，问题通常源于以下原因之一：

* 营销活动未配置为API触发的营销。
* API有效负载使用不正确的广播结构（缺少`audience`或`input-push-channel`）。
* `content-state`和`attributes`字段与iOS `ActivityAttributes`实现不匹配。
* 未在Apple开发人员门户上正确创建`input-push-channel`。

此疑难解答方案适用于广播营销活动中的所有实时活动事件： `start`、`update`和`end`。

**预检查：**

* **促销活动类型**：
   * 验证是否将营销活动创建为API触发的营销（基于广播/受众的营销活动需要）。
   * 确认已在Campaign配置中定义了受众。
* **配置文件和令牌验证**：从受众中采样多个配置文件以验证它们是否具有有效的`liveActivityPushNotificationDetails`。 有关详细的验证步骤，请按照[方案1](#profile-issue)操作。

#### 调试步骤

1. &#x200B;
   +++ 验证Campaign受众配置

   1. 在Journey Optimizer中打开&#x200B;**API触发的营销活动**。
   1. 导航到&#x200B;**受众**&#x200B;部分并验证：
      * 为营销活动选择受众。
      * 受众ID与您的API有效负载中使用的受众ID匹配。
      * 受众包含预期的用户档案。
   1. 导航到&#x200B;**操作**&#x200B;部分。
   1. 检查&#x200B;**实时活动配置**：
      * 必须使用正确的捆绑标识符为iOS应用程序设置配置。
      * 活动类型必须与API有效负载中的`attributes-type`匹配。 例如，如果您的有效负载包含`"attributes-type": "AirplaneTrackingAttributes"`，则营销活动必须指定此相同的活动类型。

      +++

1. &#x200B;
   +++ 验证广播API有效负载结构

   广播有效负载结构不同于单一营销活动。 验证有效负载是否遵循正确的广播格式。

   **广播的必填字段：**

   ```json
   {
     "campaignId": "878a11d4-b519-47bd-8313-fecfee19857b",
     "audience": {
       "id": "8c3dbdea-2957-401f-acf0-3966fba1601e"
     },
     "context": {
       "requestPayload": {
         "aps": {
           "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
           "content-available": 1,
           "timestamp": 1771829292,
           "event": "update",
           "attributes-type": "AirplaneTrackingAttributes",
           "content-state": { ... },
           "attributes": { ... }
         }
       }
     }
   }
   ```

   **常见有效负载问题：**

   | 字段 | 要求 | 常见问题 |
   |-|-|-|
   | `campaignId` | 必须与激活的营销活动ID匹配 | 营销活动ID错误或使用事务性营销活动 |
   | `audience.id` | 必须匹配AEP中的现有受众 | 错误的受众ID或受众不存在 |
   | `input-push-channel` | 广播必需 — 此广播实例的唯一标识符 | `channelID`中缺少或不匹配`liveActivityData` |
   | `timestamp` | 必须始终为当前/最新Unix纪元时间（以秒为单位） | 使用旧/缓存的时间戳 |
   | `event` | 必须为`"start"`、`"update"`或`"end"` | 事件类型无效 |
   | `attributes-type` | 必须匹配促销活动类型 | 不匹配或拼写错误 |
   | `content-available` | 必须为`1` | 值缺失或错误 |

   **关键广播特定字段：**

   * **`input-push-channel`**：
      * 所有直播活动均需要此参数。
      * 用作此特定广播实例的唯一标识符。
      * 受众中的所有用户档案都会收到与此渠道关联的实时活动。
      * 必须匹配`channelID`中的`liveActivityData.channelID`（请参阅步骤3）。
      * 必须由客户端在Apple开发人员门户上为`appID`创建。
      * 只有为特定`appID`创建的频道才能用于广播该应用程序上的实时活动。

   * **`audience.id`**：
      * 必须引用在Adobe Experience Platform中创建的有效受众区段。
      * 此受众中的所有用户档案均定位为实时活动。
      * 必须激活受众并包含具有有效`liveActivityPushNotificationDetails`的用户档案。

   **始终使用最新的时间戳：**

   * `timestamp`字段必须始终是每个API调用的当前Unix纪元时间（以秒为单位）。
   * 此要求适用于所有事件类型： `start`、`update`和`end`。
   * **更新/结束的关键**：使用过时的时间戳会导致更新和结束请求失败。
   * 为每个广播API调用生成新的时间戳。

   **可选字段：**

   * `dismissal-date`：自动删除的Unix纪元时间（仅与`end`事件相关）
   * `alert`：通知对象为`title`和`body`

   有关完整的API规范，请参阅[Adobe Journey Optimizer消息传送API文档](https://developer.adobe.com/journey-optimizer-apis/references/messaging)。

   +++

1. &#x200B;
   +++ 使content-state、attributes和input-push-channel与iOS实施保持一致

   请确保有效负载字段与iOS应用程序的`ActivityAttributes`实现匹配，并且`input-push-channel`与`channelID`中的`liveActivityData`匹配。

   1. 查看iOS ActivityAttributes定义。

   您的自定义`ActivityAttributes`结构必须实施Adobe的`LiveActivityAttributes`协议：

   ```swift
   struct AirplaneTrackingAttributes: LiveActivityAttributes {
    public struct ContentState: Codable, Hashable {
        var journeyProgress: Int
    }
   
    // Adobe SDK requirement
    var liveActivityData: LiveActivityData
   
    // Your custom attributes
    var arrivalAirport: String
    var departureAirport: String
    var arrivalTerminal: String
   }
   ```

   1. 将iOS字段映射到广播API有效负载。

   对于所有事件，包括`attributes`和`content-state`：

   ```json
         {
         "aps": {
          "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
          "event": "start",
          "timestamp": 1771829292,
          "attributes-type": "AirplaneTrackingAttributes",
          "content-state": {
            "journeyProgress": 0
          },
          "attributes": {
            "arrivalAirport": "DEL",
            "departureAirport": "MUM",
            "arrivalTerminal": "T1",
            "liveActivityData": {
              "channelID": "FEt0NgvLEfEAAOqA6AXdIQ=="
            }
          }
         }
         }
   ```

   **关键： `input-push-channel`必须匹配`channelID`**

   * `input-push-channel`根目录中的`aps`值必须与`channelID`中的`liveActivityData`完全匹配。
   * 在上述示例中，两个值均为`"FEt0NgvLEfEAAOqA6AXdIQ=="`。
   * 此匹配将广播实例链接到实时活动数据。
   * 不匹配会导致投放失败。

   **关键验证点：**

   * 包含所有事件类型在`ContentState`中的所有`content-state`字段。
   * 仅包括开始事件的`LiveActivityAttributes`中的所有自定义`attributes`字段。
   * 对于开始事件，`liveActivityData.channelID`必须匹配`input-push-channel`。
   * 字段名称区分大小写，且必须完全匹配。
   * 数据类型必须匹配（String、Int、Bool、嵌套对象等）。
   * 对于更新/结束事件，请使用与原始开始事件相同的`input-push-channel`。

   **常见错误：**

   | 问题 | 影响 | 修复 |
   |-|-|-|
   | 缺少`input-push-channel` | 广播不起作用 | 为每个广播添加唯一的频道ID |
   | `input-push-channel`与`channelID`不匹配 | 实时活动将不会启动 | 确保两个值相同 |
   | 更新/结束的不同`input-push-channel` | 更新/结束将不会到达实时活动 | 在整个生命周期中使用相同的渠道ID |
   | 缺少`liveActivityData.channelID` | 实时活动将不会链接到广播 | 在开始事件的属性中包含`channelID` |
   | 开始事件中缺少必填字段 | 实时活动将不会启动 | 从iOS结构添加所有字段 |
   | 字段名称错误（拼写错误/大小写） | 字段被忽略或分析错误 | 完全匹配iOS字段名称 |
   | 更新/结束时的过期时间戳 | 设备忽略更新/结束 | 始终生成新的时间戳 |

   +++

1. &#x200B;
   +++ 使用Assurance进行测试

   使用Assurance验证API执行和有效负载投放：

   1. 在作为受众的一部分的测试设备上打开Assurance会话。
   1. 执行广播API调用。
   1. 在&#x200B;**事件列表**&#x200B;中，查找：
      * 营销活动执行事件。
      * 实时活动交付活动。
      * 指示有效负载验证失败的错误事件。
   1. 检查事件负载以确认：
      * 已正确处理有效负载。
      * `input-push-channel`存在。
      * 未发生验证错误。
      * 已将实时活动发送给受众成员的APN。

      +++

### 配置文件不在受众或过时的受众快照中

在此方案中，营销策划和有效负载已正确配置，但特定用户档案不会接收实时活动。 这通常发生在以下情况中：

* 用户档案不是链接到营销活动的受众的成员。
* 受众是批处理受众，包含配置文件数据的过期快照。
* 最近添加了该用户档案的实时活动令牌，但尚未反映在受众快照中。

此疑难解答场景专门适用于使用基于受众的定位的广播营销活动。

**了解受众评估**

Adobe Experience Platform使用不同的受众评估方法来确定何时在受众中反映配置文件更新：

| 方法 | 评估频率 | 数据新鲜度 | 最适合 |
|-|-|-|--|
| 批次 | 每天一次（已计划） | 可能长达24小时已失效 | 大型受众，对时间不敏感 |
| 流传输 | 实时（用户档案更改） | 已更新配置文件的近乎实时 | 时效性，需要更新配置文件 |

**预检查：**

* **营销活动和有效负载验证**：
   * 完成[此方案](#broadcast-config)中的检查，以确保营销活动和有效负载正确。
   * 验证API有效负载中的`audience.id`是否与营销活动配置匹配。
* **配置文件存在**：确认AEP中存在具有有效`liveActivityPushNotificationDetails`的配置文件。

#### 调试步骤

1. &#x200B;
   +++ 验证配置文件是否在受众中

   首先，确认应接收实时活动的配置文件是否实际属于受众。

   1. 导航到Adobe Experience Platform中的&#x200B;**受众**。
   1. 使用营销活动中的`audience.id`搜索并打开受众。
   1. 单击&#x200B;**浏览**&#x200B;或&#x200B;**示例配置文件**&#x200B;查看受众成员。
   1. 使用命名空间和身份值搜索测试配置文件。
   1. **如果在受众中未找到配置文件：**
      * 配置文件不符合受众标准或区段规则。
      * 查看受众定义以了解成员资格要求。
      * 更新用户档案数据或受众定义以包含用户档案。
      * 等待受众评估完成（请参阅步骤2）。
   1. **如果在受众中找到配置文件：**&#x200B;请继续执行步骤2以检查数据新鲜度。

      +++

2. &#x200B;
   +++ 检查受众评估类型和计划

   确定受众使用批量评估还是流式评估，因为这决定了数据新鲜度。

   1. 在&#x200B;**受众详细信息**&#x200B;页面上，检查&#x200B;**评估方法**：
      * **批次**：按计划每天评估一次。
      * **流**：在发生配置文件更新时实时评估。
      * **Edge**：在边缘位置实时评估。

   根据评估方法执行相应的故障诊断步骤：

   **如果受众使用批次评估：**

   1. **了解批次受众限制：**
      * 每天评估一次批量受众（通常在一夜之间）。
      * 受众快照可能长达24小时。
      * 如果配置文件最近注册了实时活动令牌，则这些令牌可能不在当前快照中。
      * 直到下一次批量评估才会反映用户档案的更新。

   1. **检查上次评估的时间：**
      * 在受众详细信息中，查找&#x200B;**上次评估**&#x200B;时间戳。
      * 如果个人资料的`liveActivityPushNotificationDetails`在此时间戳之后更新，则受众具有过时数据。

   1. **解决陈旧数据：**
      1. **选项1：等待计划的批次评估**
         * 下一次批量评估将包括更新的用户档案数据。
         * 每天自动发生一次。
         * 最适合非紧急情况。

      1. **选项2：触发按需受众评估**
         1. 导航到AEP中的&#x200B;**受众**。
         1. 选择受众。
         1. 单击&#x200B;**立即评估**&#x200B;或&#x200B;**按需激活**。
         1. 等待评估完成（这可能需要几分钟到几小时，具体取决于受众规模）。
         1. 验证配置文件现在是否更新了受众快照中的数据。
         1. 重试广播API调用。

   **如果受众使用流式评估：**

   1. **了解流受众行为：**
      * 发生配置文件更新时，流式受众会实时评估。
      * **新用户档案**：如果符合区段标准，则在创建后不久即获得资格。
      * **已更新配置文件**：更新后不久即获得资格或取消资格。
      * **现有未更改的用户档案**：除非进行更新，否则不会重新评估。

   1. **识别问题：**
      * 如果某个用户档案已存在并符合区段标准，但该用户档案未发生更新，则可能无法将其添加到新创建的流受众。
      * 配置文件必须接收更新（任何属性更改）才能触发重新评估。

   1. **解决问题：**
      * **对于新用户档案**：如果满足条件，则这些用户档案会自动获得资格。 无需执行任何操作。
      * **对于没有最近更新的现有配置文件：**
         * 对配置文件进行细微更新（例如，更新时间戳字段）。
         * 这会触发流式评估并将配置文件添加到受众。
         * 替代方法：为现有用户档案使用批量受众或边缘受众。

      +++
