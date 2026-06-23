---
solution: Journey Optimizer
product: journey optimizer
title: 使用高级表达式编辑器
description: 了解如何构建高级表达式
feature: Journeys
role: Developer
level: Experienced
hide: true
keywords: 表达式、条件、用例、事件
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/UUeCcATC7MFHsLuI8TPoVHqwVe9GOXUq3U3RoAG-a1o
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1103
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

然后，它选择未转换为completePurchase的所有添加到购物车事件。

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

## 表达式中的时间戳筛选

在引用多个购物车活动事件时，请指定开始和结束时间戳窗口，以避免提取历史数据。 例如：

```json
toDateTimeOnly(currentDataPackField.timestamp) >= toDateTimeOnly(@event{poc_UDXCartAddSavedCheckOutEv.timestamp})
AND
toDateTimeOnly(currentDataPackField.timestamp) < toDateTimeOnly(nowWithDelta(4, "hours"))
```

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

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;本页提供了使用高级表达式编辑器构建旅程条件的实际示例，这些条件按购物车活动、库存状态、地理围栏事件、字符串操作和时间戳窗口过滤用户。

**意图：**

* 使用`in()`和`inLastDays()`构建购物车放弃条件，以定向添加商品但未在7天内完成购买的用户
* 按时间戳窗口筛选体验事件集合，以避免捕获历史数据
* 将区分大小写和不区分大小写的字符串比较应用于地理围栏事件字段
* 使用`substr`和`lastIndexOf`从移动设备应用程序启动事件中提取和处理CRM ID
* 通过将数量字段与阈值进行比较，检查产品库存可用性
* 在历程条件中使用`and` / `not`逻辑合并多个布尔表达式

**术语表：**

* **高级表达式编辑器**：用于使用函数、运算符和字段引用&#x200B;*（产品特定的）*&#x200B;编写复杂代码级表达式的Journey Optimizer接口
* **currentDataPackField**：在`all()`、`first()`或`last()`函数&#x200B;*（产品特定）*&#x200B;内迭代数据源集合时使用的循环变量
* **inLastDays(timestamp， N)**：如果给定的时间戳在最近N天内，则返回真&#x200B;*（产品特定）*&#x200B;的日期函数
* **体验事件**：存储在Adobe Experience Platform中的时间序列行为数据记录，按反向时间顺序&#x200B;*（产品特定）*&#x200B;检索

**护栏：**

* 不支持直接在历程表达式/条件中使用体验事件；应改用计算属性或受众区段等替代方法
* 对时间序列数据（如购买或点击的集合）的查询必须使用高级表达式编辑器（不是简单编辑器）
* 双击左侧面板中的字段可将其快速插入到表达式中；避免手动键入字段路径以减少错误
* 查询体验事件的表达式将返回一个布尔值；请确保下游逻辑需要一个布尔类型

**术语：**

* 规范名称：高级表达式编辑器 — 首字母缩略词：none — 变体：表达式编辑器，高级编辑器
* 同义词： &quot;addToCart&quot; = &quot;add to cart interaction&quot;； &quot;completePurchase&quot; = &quot;purchase completion event&quot;
* 请勿混淆：事件（以`@`为前缀）≠数据源（以`#`为前缀）

**常见问题解答：**

* **问：为什么必须使用高级编辑器而不是简单的编辑器来执行购物车放弃查询？**  — 简单编辑器无法对时间序列集合执行查询；`all()`、`first()`和`last()`集合函数需要高级编辑器。
* **问：如何在表达式中引用最新的“addToCart”事件？**  — 对按`productInteraction == "addToCart"`筛选的体验事件集合使用`first()`函数，因为事件是按反向时间顺序返回的。
* **问：如何在高级编辑器中使字符串比较不区分大小写？**  — 使用`equalIgnoreCase()`函数而不是`==`运算符。
* **问：在查询购物车事件时添加时间戳窗口有何用途？**  — 同时指定开始和结束时间戳，可防止拾取超出预定活动窗口的历史数据。
* **问：如何从事件中传递的CRM ID字符串中删除大括号？**  — 使用`substr()`和`lastIndexOf()`组合提取大括号之间的内容。

+++
