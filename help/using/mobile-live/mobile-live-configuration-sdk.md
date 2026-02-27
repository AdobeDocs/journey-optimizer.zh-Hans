---
solution: Journey Optimizer
product: journey optimizer
title: 配置实时活动渠道
description: 了解如何配置Adobe Experience Platform Mobile SDK集成
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 02ca7c8e-105a-4e77-9aad-2381904255d0
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---

# 实时活动与Adobe Experience Platform Mobile SDK集成 {#mobile-live-config-sdk}


Adobe Experience Platform Mobile SDK为Apple的实时活动提供内置支持。 这样，您的应用程序就可以直接在锁屏界面和Dynamic Island上显示实时的动态更新，而无需打开应用程序。

1. [导入所需的模块](#import)

   导入以下模块： **[!DNL AEPMessaging]**、**[!DNL AEPMessagingLiveActivity]**、**[!DNL ActivityKit]**。

1. [定义属性](#attributes)

   符合`LiveActivityAttributes`，包括`LiveActivityData`和`ContentState`属性。

1. [注册实时活动](#register)

   在SDK初始化后使用`Messaging.registerLiveActivity()`。

1. [创建构件配置](#widget)

   对Lock Screen和Dynamic Island接口实施`ActivityConfiguration`。

1. [在本地启动实时活动（可选）](#local)

   可以通过Journey Optimizer远程启动实时活动，也可以在应用程序代码中本地启动实时活动。

1. [添加调试支持（可选）](#debug)

   为Assurance实施`LiveActivityAssuranceDebuggable`。

验证是否安装了以下最低版本，以确保配置和兼容性正确。

>[!BEGINSHADEBOX]

**先决条件：**

* **iOS：**
   * **iOS16.1或更高版本**：基本实时活动功能
   * **iOS 17.2+**：即按即用支持
   * **iOS 18+**：广播频道支持
* **Xcode：** 14.0或更高版本
* **Swift：** 5.7或更高版本
* **依赖项：** AEPCore、AEPMessaging、AEPMessagingLiveActivity、ActivityKit
* **AEP Mobile SDK版本**： iOS消息5.11.0或更高版本

>[!ENDSHADEBOX]

## 步骤1：导入所需的模块 {#import}

若要开始，您首先需要导入以下模块： **[!DNL AEPMessaging]**、**[!DNL AEPMessagingLiveActivity]**、**[!DNL ActivityKit]**。

```swift
import AEPMessaging
import AEPMessagingLiveActivity
import ActivityKit
```

## 第2步：定义您的实时活动属性 {#attributes}

创建符合`LiveActivityAttributes`协议的结构。 这会定义实时活动的静态数据和动态内容状态。

关键组件包括：

* **`liveActivityData`** （必需），其中包含特定于Adobe Experience Platform的数据。
   * 对于个人用户：使用`LiveActivityData(liveActivityID: "unique-id")`
   * 用于广播：使用`LiveActivityData(channelID: "channel-id")`

* 静态属性，特定于您的用例的自定义属性，如`restaurantName`。

* **`ContentState`**&#x200B;定义可在实时活动生命周期中更新的动态数据。 它必须符合`Codable`和`Hashable`。

* `LiveActivityOrigin`枚举指定活动是在应用程序内本地启动，还是通过iOS 17.2及更高版本中支持的即点即用通知远程启动。 此值允许SDK在数据收集期间区分本地启动和远程触发的实时活动。

**示例**

```swift
@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
    // Mandatory: AEP Integration Data
    var liveActivityData: LiveActivityData
    
    // Static Attributes: Custom properties that do not change
    var restaurantName: String
    
    // Dynamic Content State: Data that can be updated
    struct ContentState: Codable, Hashable {
        var orderStatus: String
    }
}
```

```swift
@available(iOS 16.1, *)
public struct LiveActivityData: Codable {
    /// Unique identifier for broadcast Live activity channels
    public let channelID: String?
     
    /// Unique identifier for individual Live activity
    public let liveActivityID: String?
     
    /// Indicates local vs remote creation
    public let origin: LiveActivityOrigin?
     
    // Initializers
    public init(channelID: String)        // For broadcast Live activity
    public init(liveActivityID: String)   // For individual Live activity
}
```

您还可以为应用程序注册多种实时活动类型：

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(AirplaneTrackingAttributes.self)
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
    Messaging.registerLiveActivity(GameScoreLiveActivityAttributes.self)
}
```

## 步骤3：注册实时活动 {#register}

在SDK初始化后，在`AppDelegate`中注册您的实时活动类型，这允许您：

* 启用自动推送启动令牌收集(iOS 17.2+)
* 自动收集实时活动更新令牌
* 支持生命周期管理和事件跟踪

**食品配送实时活动示例：**

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
}
```

## 步骤4：创建实时活动构件 {#widgets}

实时活动通过构件显示，您需要创建构件捆绑包和配置：

**食品配送实时活动示例：**

```swift
@main
struct FoodDeliveryWidgetBundle: WidgetBundle {
    var body: some Widget {
        FoodDeliveryLiveActivityWidget()
    }
}

@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityWidget: Widget {
    var body: some WidgetConfiguration {
        ActivityConfiguration(for: FoodDeliveryLiveActivityAttributes.self) { context in
            // Lock Screen UI
            VStack {
                Text("Order from \(context.attributes.restaurantName)")
                Text("Status: \(context.state.orderStatus)") // possible status may include "Ordered", "Order accepted", "Preparing", "On the Way","Delivered"
            }
        } dynamicIsland: { context in
            // Dynamic Island UI
            DynamicIsland {
                // Expanded UI
            } compactLeading: {
                // Compact leading UI
            } compactTrailing: {
                // Compact trailing UI
            } minimal: {
                // Minimal UI
            }
        }
    }
}
```

## 步骤5：在本地启动实时活动（可选） {#local}

虽然Journey Optimizer可以远程启动实时活动，但您也可以本地启动它：

**食品配送实时活动示例：**

```swift
let attributes = FoodDeliveryLiveActivityAttributes(
    liveActivityData: LiveActivityData(liveActivityID: "order123"),
    restaurantName: "Pizza Palace"
)

let contentState = FoodDeliveryLiveActivityAttributes.ContentState(
    orderStatus: "Ordered"
)

let activity = try Activity<FoodDeliveryLiveActivityAttributes>.request(
    attributes: attributes,
    contentState: contentState,
    pushType: .token
)
```

## 步骤6：添加调试支持（可选） {#debug}

如果需要，您可以在Adobe Assurance中调试Live活动架构：

**食品配送实时活动示例：**

```swift
@available(iOS 16.1, *)
extension FoodDeliveryLiveActivityAttributes: LiveActivityAssuranceDebuggable {
    static func getDebugInfo() -> (attributes: FoodDeliveryLiveActivityAttributes, state: ContentState) {
        return (
            FoodDeliveryLiveActivityAttributes(
                liveActivityData: LiveActivityData(liveActivityID: "debug-order-123"),
                restaurantName: "Debug Restaurant"
            ),
            ContentState(orderStatus: "Ordered")
        )
    }
}
```
