---
solution: Journey Optimizer
product: journey optimizer
title: 使用高级表达式编辑器
description: 了解如何构建高级表达式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
hide: true
hidefromtoc: true
keywords: 表达式、条件、用例、事件
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
source-git-commit: dbb1a4d649f29b763121c7856cecca16dcd2864f
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 2%

---


# 高级表达式示例{#advanced-expression-examples}

高级表达式编辑器可用于创建条件，以允许您在历程中筛选用户。 利用这些条件，可按时间、日期、位置、持续时间定位用户，以便在历程中重新定位用户。

>[!CAUTION]
>
>不支持在历程表达式/条件中使用体验事件。 如果您的用例需要使用体验事件，请考虑替代方法。 [了解详情](../exp-event-lookup.md)


## 基于体验事件构建条件


>[!CAUTION]
>
>不支持在历程表达式/条件中使用体验事件。 如果您的用例需要使用体验事件，请考虑替代方法。 [了解详情](../exp-event-lookup.md)
>



高级表达式编辑器必须对时间序列执行查询，例如消息的购买或过去点击列表。 无法使用简单编辑器执行此类查询。

>[!NOTE]
>
>事件以@开头，数据源以#开头。

体验事件作为收藏集从Adobe Experience Platform中按反时间顺序进行检索，因此：

* 第一个函数将返回最近的事件
* last函数将返回最早的函数。

例如，假设您想定位过去7天内放弃购买购物车的客户，以便在客户接近商店时发送消息，提供有关他们想要的店内商品的优惠。

**您需要生成以下条件：**

首先，定位浏览在线商店但在过去7天内未完成订单的客户。

**此表达式在字符串值中查找指定的值：**

`In ("addToCart", #{field reference from experience event})`

**此表达式将查找过去7天内为该用户指定的所有事件：**

然后，它选择未转换为completePurchase的所有购物车事件。

>[!NOTE]
>
>要在表达式中快速插入字段，请双击编辑器左侧面板中的字段。

指定的时间戳将用作日期时间值，第二个时间戳是天数。

```json
        in( "addToCart", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction})
        and
        not(in( "completePurchase", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction}))
```

此表达式返回布尔值。

**现在，让我们构建一个表达式，检查产品是否已有库存**

* 在库存中，此表达式查找产品的数量字段，并指定它应大于0。

`#{Inventory.fieldgroup3.quantity} > 0`

* 在右边，指定必要的值，这里，我们需要检索存储的位置，该位置是从事件“EndaysLumaStudio”的位置映射的：

`#{ArriveLumaStudio._acpevangelists1.location.location}`

* 并使用函数`first`指定SKU以检索最新的“addToCart”交互：

  ```json
      #{ExperiencePlatformDataSource
                      .ExperienceEventFieldGroup
                      .experienceevent
                      .first(
                      currentDataPackField
                      .productData
                      .productInteraction == "addToCart"
                      )
                      .SKU}
  ```

从该位置，您可以在历程中添加其他路径（产品不在商店中）并发送包含参与选件的通知。 相应地配置消息并使用个性化数据增强消息目标。

## 使用高级表达式编辑器进行字符串处理的示例

**条件**

此条件仅检索在“Arlington”中触发的地理围栏事件：

```json
        @event{GeofenceEntry
                    .placeContext
                    .POIinteraction
                    .POIDetail
                    .name} == "Arlington"
```

解释：这是一个严格的字符串比较（区分大小写），相当于简单模式中的查询，该模式使用`equal to`并选中`Is sensitive`。

取消选中`Is sensitive`的相同查询将在高级模式下生成以下表达式：

```json
        equalIgnoreCase(@event{GeofenceEntry
                        .placeContext
                        .POIinteraction
                        .POIDetail
                        .name}, "Arlington")
```

**操作中**

以下表达式允许您在操作个性化字段中定义CRM ID：

```json
substr(
   @event{MobileAppLaunch
   ._myorganization
   .identification
   .crmid},
   1, 
   lastIndexOf(
     @event{MobileAppLaunch
     ._myorganization
     .identification
     .crmid},
     '}'
   )
)
```

解释：此示例使用`substr`和`lastIndexOf`函数删除包含通过移动设备应用程序启动事件传递的CRM ID的大括号。


有关如何使用高级表达式编辑器的详细信息，请观看[此视频](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/introduction-to-building-a-journey.html?lang=zh-Hans)。
