---
solution: Journey Optimizer
product: journey optimizer
title: 对上下文数据进行迭代
description: 了解如何使用Handlebars语法从各种上下文源对数组进行迭代
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
hide: true
hidefromtoc: true
keywords: 表达式，编辑器， handlebars，迭代，数组，上下文，个性化
source-git-commit: d3a06e15440dc58267528444f90431c3b32b49f2
workflow-type: tm+mt
source-wordcount: '2704'
ht-degree: 0%

---

# 对上下文数据进行迭代 {#personalization-contexts}

了解如何使用Handlebars迭代语法在消息中显示来自各种源的数据的动态列表，包括事件、自定义操作响应和其他上下文数据。

## 概述 {#overview}

在[消息个性化](personalize.md)期间，Journey Optimizer允许从多个来源访问上下文数据。 您可以使用本机渠道（[电子邮件](../email/get-started-email-design.md)、[推送](../push/create-push.md)、[短信](../sms/create-sms.md)）中的Handlebars语法对这些源中的数组进行迭代，以显示动态内容，如产品列表、推荐或其他重复元素。

**可用的上下文源：**

* **[事件](#event-data)**：历程事件（业务事件、单一事件）中的数据
* **[自定义操作响应](#custom-action-responses)**：通过自定义操作从外部API调用返回的数据
* **[数据集查找](#dataset-lookup)**：从Adobe Experience Platform数据集检索的扩充数据
* **[技术属性](#technical-properties)**：历程元数据，例如历程ID和补充标识符
* **[历程上下文](#other-contexts)**：执行期间可访问的其他历程相关数据

本指南向您展示了如何在消息中从每个来源对阵列进行迭代，以及在配置历程活动时如何使用阵列。 从[Handlebars迭代语法](#syntax)开始，了解消息个性化基本知识，或跳转到[使用历程表达式中的数组](#arrays-in-journeys)，了解如何将数组数据传递给自定义操作和数据集查找。

## Handlebars迭代语法 {#syntax}

Handlebars提供`{{#each}}` [帮助程序](functions/helpers.md)以通过数组进行迭代。 基本语法为：

```handlebars
{{#each arrayPath as |item|}}
  <!-- Access item properties here -->
  {{item.property}}
{{/each}}
```

**关键点：**

* 将`arrayPath`替换为数组数据的路径
* 将`item`替换为您喜欢的任何变量名称（例如，`product`、`response`、`element`）
* 使用`{{item.propertyName}}`访问每个项目的属性
* 您可以为多级数组嵌套多个`{{#each}}`块

## 对事件数据进行迭代 {#event-data}

当您的历程由[事件](../event/about-events.md)触发时，事件数据可用。 这有助于显示历程开始时捕获的数据，例如购物车内容、订单项目或表单提交。

>[!TIP]
>
>您可以将事件数据与其他源相结合。 有关示例，请参阅[合并多个上下文源](#combine-sources)。

### 事件的上下文路径

```handlebars
context.journey.events.<event_ID>.<fieldPath>
```

* `<event_ID>`：历程中配置的事件唯一ID
* `<fieldPath>`：事件架构中字段或数组的路径

### 示例：事件中的购物车项目

如果您的[事件架构](../event/experience-event-schema.md)包含`productListItems`数组（标准[XDM格式](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html){target="_blank"}），您可以显示购物车内容，如下面的示例中详述。

+++ 查看示例代码

```handlebars
{{#each context.journey.events.event_ID.productListItems as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}
```

+++

### 示例：事件中的嵌套数组

对于嵌套结构，使用嵌套的`{{#each}}`块。

+++ 查看示例代码

```handlebars
{{#each context.journey.events.event_ID.categories as |category|}}
  <h2>{{category.name}}</h2>
  <ul>
    {{#each category.items as |item|}}
      <li>{{item.title}}</li>
    {{/each}}
  </ul>
{{/each}}
```

+++

在[最佳实践](#best-practices)中了解有关嵌套的更多信息。

## 迭代自定义操作响应 {#custom-action-responses}

[自定义操作](../action/about-custom-action-configuration.md)响应包含从外部API调用返回的数据。 这对于显示系统中的实时信息非常有用，例如忠诚度点数、产品推荐、库存状态或个性化优惠。

>[!NOTE]
>
>必须为自定义操作配置响应有效负载才能使用此功能。 在[本节](../action/action-response.md#config-response)中了解详情。 您还可以将自定义操作响应与事件数据或数据集查找相结合 — 请参阅[合并多个上下文源](#combine-sources)以获取示例。

### 自定义操作的上下文路径

```handlebars
context.journey.actions.<actionName>.<fieldPath>
```

* `<actionName>`：历程中配置的[自定义操作](../action/about-custom-action-configuration.md)的名称
* `<fieldPath>`：响应有效负载中字段或数组的路径

### 示例：来自API的产品推荐

要迭代从自定义操作返回的一系列产品推荐，并在消息中将它们显示为单个卡片，请参阅以下示例。

+++ 查看示例代码

**API响应：**

```json
{
  "recommendations": [
    {
      "productId": "12345",
      "productName": "Summer Jacket",
      "price": 89.99,
      "imageUrl": "https://example.com/jacket.jpg"
    },
    {
      "productId": "67890",
      "productName": "Running Shoes",
      "price": 129.99,
      "imageUrl": "https://example.com/shoes.jpg"
    }
  ]
}
```

**消息个性化：**

```handlebars
<h2>Recommended for You</h2>
<div class="recommendations">
  {{#each context.journey.actions.GetRecommendations.recommendations as |item|}}
    <div class="product-card">
      <img src="{{item.imageUrl}}" alt="{{item.productName}}" />
      <h3>{{item.productName}}</h3>
      <p class="price">${{item.price}}</p>
    </div>
  {{/each}}
</div>
```

+++

### 示例：自定义操作中的嵌套数组

要迭代包含嵌套数组（一个对象数组，其中每个对象都包含另一个数组）的自定义操作响应，请参阅以下示例。 此演示使用嵌套的`{{#each}}`循环访问多个级别的数据。

+++ 查看示例代码

**API响应：**

```json
{    
  "id": "84632848268632",    
  "responses": [
    { "productIDs": [1111, 2222, 3333] },
    { "productIDs": [4444, 5555, 6666] },
    { "productIDs": [7777, 8888, 9999] }
  ]
}
```

**消息个性化：**

```handlebars
<h2>Product Groups</h2>
{{#each context.journey.actions.GetProducts.responses as |response|}}
  <div class="product-group">
    <ul>
      {{#each response.productIDs as |productID|}}
        <li>Product ID: {{productID}}</li>
      {{/each}}
    </ul>
  </div>
{{/each}}
```

+++

有关更复杂的嵌套模式，请参阅[最佳实践](#best-practices)。

### 示例：忠诚度层级优势

要根据忠诚度状态显示动态福利，请参阅以下示例。

+++ 查看示例代码

**API响应：**

```json
{
  "loyaltyTier": "gold",
  "benefits": [
    { "name": "Free shipping", "icon": "truck" },
    { "name": "20% discount", "icon": "percent" },
    { "name": "Priority support", "icon": "headset" }
  ]
}
```

**消息个性化：**

```handlebars
<h2>Your {{context.journey.actions.GetLoyaltyInfo.loyaltyTier}} Member Benefits</h2>
<ul class="benefits">
  {{#each context.journey.actions.GetLoyaltyInfo.benefits as |benefit|}}
    <li>
      <span class="icon-{{benefit.icon}}"></span>
      {{benefit.name}}
    </li>
  {{/each}}
</ul>
```

+++

## 对数据集查找结果进行迭代 {#dataset-lookup}

[数据集查找活动](../building-journeys/dataset-lookup.md)允许您在历程运行时从[Adobe Experience Platform数据集](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh-Hans){target="_blank"}中检索数据。 扩充的数据将作为数组存储，并可在消息中迭代。

>[!AVAILABILITY]
>
>数据集查找活动仅适用于有限的一组组织。 要获得访问权限，请与 Adobe 代表联系。

在[此部分](../building-journeys/dataset-lookup.md)中了解有关配置数据集查找活动的更多信息。 与事件数据结合使用时，数据集查找功能尤为强大 — 请参阅[示例：通过数据集查找扩充了事件数据](#combine-sources)以了解实际用例。

### 数据集查找的上下文路径

```handlebars
context.journey.datasetLookup.<activityID>.entities
```

* `<activityID>`：数据集查找活动的唯一ID
* `entities`：从数据集中检索的扩充数据数组

### 示例：数据集中的产品详细信息

如果您使用数据集查找活动根据SKU检索产品信息，请参阅以下示例。

+++ 查看示例代码

**数据集查找配置：**

* 查找键： `list(@event{purchase_event.products.sku})`
* 要返回的字段： `["SKU", "category", "price", "name"]`

**消息个性化：**

```handlebars
<h2>Product Details</h2>
<table>
  <thead>
    <tr>
      <th>Product Name</th>
      <th>Category</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    {{#each context.journey.datasetLookup.3709000.entities as |product|}}
      <tr>
        <td>{{product.name}}</td>
        <td>{{product.category}}</td>
        <td>${{product.price}}</td>
      </tr>
    {{/each}}
  </tbody>
</table>
```

+++

### 示例：使用数据集数据过滤的迭代

要在迭代期间筛选数据集查找结果并仅显示符合特定条件的项（例如，特定类别中的产品），请在`{{#if}}`循环中使用条件`{{#each}}`语句。 请参阅以下示例。

+++ 查看示例代码

```handlebars
<h2>Household Products</h2>
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {{#if product.category = "household"}}
    <div class="product">
      <h3>{{product.name}}</h3>
      <p>Price: ${{product.price}}</p>
    </div>
  {{/if}}
{{/each}}
```

+++

在[最佳实践](#best-practices)中了解有关条件筛选的更多信息。

### 示例：通过数据集查找计算总数

要在迭代数据集查找结果时计算并显示总计，请参阅以下示例。

+++ 查看示例代码

```handlebars
{% let householdTotal = 0 %}
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {%#if product.category = "household"%}
    {% let householdTotal = householdTotal + product.price %}
  {%/if%}
{{/each}}

<p>Your household products total: ${{householdTotal}}</p>
```

+++

## 使用历程技术属性 {#technical-properties}

历程技术属性提供对旅程执行相关元数据的访问权限，例如旅程ID和补充标识符。 在与迭代模式结合使用时，这些规则可能很有用，尤其是对于根据特定历程实例筛选数组。

### 可用的技术属性

```handlebars
context.journey.technicalProperties.journeyUID
context.journey.technicalProperties.supplementalId
```

### 示例：使用补充标识符筛选数组项

在具有数组的事件触发的历程中使用补充标识符时，您可以进行筛选以仅显示当前历程实例的相关项目。 在[本指南](../building-journeys/supplemental-identifier.md)中了解有关补充标识符的更多信息。

**场景**：历程通过多个预订触发，但您只想显示触发此历程实例的特定预订（由补充ID标识）的信息。

+++ 查看示例代码

```handlebars
{{#each context.journey.events.event_ID.bookingList as |booking|}}
  {%#if booking.bookingInfo.bookingNum = context.journey.technicalProperties.supplementalId%}
    <div class="booking-details">
      <h3>Your Booking: {{booking.bookingInfo.bookingNum}}</h3>
      <p>Destination: {{booking.bookingInfo.bookingCountry}}</p>
      <p>Date: {{booking.bookingInfo.bookingDate}}</p>
    </div>
  {%/if%}
{{/each}}
```

+++

### 示例：包含用于跟踪的历程ID

要在消息中包含历程ID以进行跟踪，请参阅以下示例。

+++ 查看示例代码

```handlebars
<footer>
  <p>Journey Reference: {{context.journey.technicalProperties.journeyUID}}</p>
</footer>
```

+++

## 合并多个上下文源 {#combine-sources}

您可以将来自不同来源的数据合并到同一消息中，以创建丰富且个性化的体验。 本节显示了将多个上下文源结合使用的实际示例。

**可以合并的上下文源：**

* [事件数据](#event-data) + [自定义操作响应](#custom-action-responses)
* [事件数据](#event-data) + [数据集查找](#dataset-lookup)
* [多个源](#combine-sources) + [技术属性](#technical-properties)

### 示例：具有实时库存的购物车项目

要将事件数据（购物车内容）与自定义操作数据（库存状态）相结合，请查看以下示例。

+++ 查看示例代码

```handlebars
<h2>Your Cart</h2>
{{#each context.journey.events.cartEvent.productListItems as |product|}}
  <div class="cart-item">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}

<h2>We Also Recommend</h2>
{{#each context.journey.actions.GetRecommendations.items as |recommendation|}}
  <div class="recommendation">
    <h4>{{recommendation.name}}</h4>
    <p>${{recommendation.price}}</p>
    {{#if recommendation.inStock}}
      <span class="badge">In Stock</span>
    {{else}}
      <span class="badge out-of-stock">Out of Stock</span>
    {{/if}}
  </div>
{{/each}}
```

+++

### 示例：通过数据集查找扩充了事件数据

要将[事件SKU](#event-data)与[数据集查找](#dataset-lookup)中的详细产品信息相结合，请查看以下示例。

+++ 查看示例代码

```handlebars
<h2>Your Order Details</h2>
{{#each context.journey.events.orderEvent.productListItems as |item|}}
  <div class="order-item">
    <p><strong>SKU:</strong> {{item.SKU}}</p>
    <p><strong>Quantity:</strong> {{item.quantity}}</p>
    
    <!-- Enrich with dataset lookup data -->
    {{#each context.journey.datasetLookup.1234567.entities as |enrichedProduct|}}
      {{#if enrichedProduct.SKU = item.SKU}}
        <p><strong>Product Name:</strong> {{enrichedProduct.name}}</p>
        <p><strong>Category:</strong> {{enrichedProduct.category}}</p>
        <img src="{{enrichedProduct.imageUrl}}" alt="{{enrichedProduct.name}}" />
      {{/if}}
    {{/each}}
  </div>
{{/each}}
```

+++

### 示例：将多个源与技术属性相结合

要将多个上下文源（用户档案数据、事件数据、自定义操作和技术属性）合并到一封邮件中，请查看以下示例。

+++ 查看示例代码

```handlebars
<div class="personalized-content">
  <!-- Profile data -->
  <h1>Hello {{profile.person.name.firstName}},</h1>
  
  <!-- Event data iteration -->
  <h2>Your Recent Purchases</h2>
  {{#each context.journey.events.purchaseEvent.items as |purchase|}}
    <div class="purchase">
      <p>{{purchase.productName}} - ${{purchase.price}}</p>
    </div>
  {{/each}}
  
  <!-- Custom action response iteration -->
  <h2>Recommended for You</h2>
  {{#each context.journey.actions.GetPersonalizedRecs.recommendations as |rec|}}
    <div class="recommendation">
      <h3>{{rec.title}}</h3>
      <p>{{rec.description}}</p>
    </div>
  {{/each}}
  
  <!-- Technical properties -->
  <footer>
    <p class="fine-print">Journey ID: {{context.journey.technicalProperties.journeyUID}}</p>
  </footer>
</div>
```

+++

## 其他上下文类型 {#other-contexts}

虽然本指南侧重于数组上的迭代，但其他上下文类型可用于个性化，通常不需要迭代。 这些组件直接访问，而不是循环访问：

* **[配置文件属性](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}** (`profile.*`)： Adobe Experience Platform中的各个配置文件字段
* **[受众](../audience/about-audiences.md)** (`inAudience()`)：受众成员资格检查
* **[优惠决策](../offers/get-started/starting-offer-decisioning.md)**：决策管理优惠
* **[Target属性](../orchestrated/activities/channels.md#add-personalization)**（仅限编排的营销活动）：在营销活动画布中计算的属性
* **令牌** (`context.token`)：会话或身份验证令牌

有关使用这些源的完整个性化语法和示例，请参阅：

* [添加个性化](personalization-build-expressions.md)
* [个性化语法](personalization-syntax.md)

## 在历程表达式中使用数组 {#arrays-in-journeys}

虽然上一节侧重于使用Handlebars在消息个性化中迭代使用数组，但在配置历程活动时也可以使用数组。 本节介绍如何在历程表达式中使用来自事件的数组数据，尤其是将数据传递给自定义操作或使用具有数据集查找的数组时。

>[!IMPORTANT]
>
>历程表达式使用与Handlebars个性化不同的语法。 在历程配置（如自定义操作参数或条件）中，您将[历程表达式编辑器](../building-journeys/expression/expressionadvanced.md)与诸如`first`、`all`和`serializeList`之类的函数一起使用。 在消息内容中，您将Handlebars语法与`{{#each}}`循环一起使用。

### 将数组值传递到自定义操作参数 {#arrays-to-custom-actions}

在配置[自定义操作](../action/about-custom-action-configuration.md)时，您通常需要从事件数组中提取值，并将其作为参数传递。 本节介绍常见模式。

了解有关在[中将集合传递到自定义操作参数](../building-journeys/collections.md#passing-collection)中的详细信息。

#### 从数组中提取单个值

**用例**：从事件数组中获取特定字段，以作为查询参数传递到GET请求中。

+++ 查看示例代码

**示例场景**：从产品列表中提取价格大于0的第一个SKU。

**事件架构示例**：

```json
{
  "commerce": {
    "productListItems": [
      { "SKU": "SKU-1", "priceTotal": 10.0 },
      { "SKU": "SKU-2", "priceTotal": 0.0 },
      { "SKU": "SKU-3", "priceTotal": 20.0 }
    ]
  }
}
```

**自定义操作配置**：

1. 在自定义操作中，使用类型`sku`配置查询参数（例如`string`）
2. 将其标记为`Variable`以允许动态值

操作参数&#x200B;**中的**&#x200B;表达式历程：

```javascript
@event{YourEventName.commerce.productListItems.first(currentEventField.priceTotal > 0).SKU}
```

**说明**：

* `@event{YourEventName}`：引用您的历程事件
* `.first(currentEventField.condition)`：返回与条件匹配的第一个数组项
* `currentEventField`：代表事件数组中的每个项，因为您循环遍历它
* `.SKU`：从匹配项提取SKU字段
* 结果： `"SKU-1"` （适用于操作参数的字符串）

了解有关`first`集合管理函数[中的](../building-journeys/expression/collection-management-functions.md)函数的更多信息。

+++

#### 从数组构建值列表

**用例**：创建以逗号分隔的ID列表以作为查询参数传递（例如，`/products?ids=sku1,sku2,sku3`）。

+++ 查看示例代码

**自定义操作配置**：

1. 使用类型`ids`配置查询参数（例如`string`）
2. 将其标记为`Variable`

**历程表达式**：

```javascript
serializeList(
  @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0).SKU},
  ",",
  true
)
```

**说明**：

* `.all(currentEventField.condition)`：返回与条件匹配的所有数组项（返回列表）
* `currentEventField`：代表事件数组中的每个项，因为您循环遍历它
* `.SKU`：对列表进行项目以仅包含SKU值
* `serializeList(list, delimiter, addQuotes)`：将列表加入字符串
   * `","`：使用逗号作为分隔符
   * `true`：在每个字符串元素周围添加引号
* 结果： `"SKU-1,SKU-3"` （适用于查询参数）

详细了解：

* [&#39;全部&#39;](../building-journeys/expression/collection-management-functions.md)
* [&#39;serializeList&#39;](../building-journeys/functions/list-functions.md#serializeList)

[将集合传递到自定义操作参数](../building-journeys/collections.md#passing-collection)中涵盖了自定义操作的集合处理。

+++

#### 将对象数组传递给自定义操作

**用例**：发送请求正文中的对象的完整数组(用于POST或带有正文的GET)。

+++ 查看示例代码

**请求正文示例**：

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "Product A",
        "price": 20.1,
        "color": "blue"
      }
    ]
  }
}
```

**自定义操作配置**：

1. 在请求正文中，将`products`定义为类型`listObject`
2. 将其标记为`Variable`
3. 定义对象字段： `id`、`name`、`price`、`color`（每个字段都变为可映射）

**历程画布配置**：

1. 在高级模式下，设置集合表达式：

   ```javascript
   @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0)}
   ```

1. 在收藏集映射UI中：
   * 将`id`映射→`productListItems.SKU`
   * 将`name`映射→`productListItems.name`
   * 将`price`映射→`productListItems.priceTotal`
   * 将`color`映射→`productListItems.color`

Journey Optimizer会构建与操作有效负载结构匹配的对象数组。

>[!NOTE]
>
>使用事件数组时，使用`currentEventField`引用每个项。 对于数据源集合(Adobe Experience Platform)，请使用`currentDataPackField`。 对于自定义操作响应集合，请使用`currentActionField`。

请参阅[将集合传递到自定义操作参数](../building-journeys/collections.md#passing-collection)以了解详情。

+++

### 使用数组进行数据集查找 {#arrays-with-dataset-lookup}

使用[数据集查找活动](../building-journeys/dataset-lookup.md)时，您可以将一组值作为查找键传递以检索扩充数据。

**示例**：查找事件数组中所有SKU的产品详细信息。

+++ 查看示例代码

**数据集查找配置**：

在查找键字段中，使用`list()`将数组路径转换为列表：

```javascript
list(@event{purchaseEvent.productListItems.SKU})
```

这将创建一个列表，其中包含要在数据集中查找的所有SKU值。 结果在`context.journey.datasetLookup.<activityID>.entities`处可用作数组，您可以在消息中对其进行迭代（请参阅[对数据集查找结果进行迭代](#dataset-lookup)）。

+++

### 限制和模式 {#array-limitations}

在历程中使用数组时，请注意以下限制：

#### 在历程流中无需对阵列进行动态循环

历程无法创建动态循环，其中数组中的每个项会多次执行一个操作节点。 这是为了防止出现性能失控问题。

**您无法执行的操作**：

* 为每个数组项动态执行一次自定义操作
* 根据数组长度创建多个历程分支

**推荐的模式**：

1. **一次发送所有项**：将整个数组或序列化列表传递到单个处理所有项的自定义操作。 请参阅[从数组](#arrays-to-custom-actions)生成值列表。

2. **使用外部聚合**：让外部API接受多个ID并在单个调用中返回组合结果。

3. **在AEP中预计算**：使用[计算属性](../audience/computed-attributes.md)在配置文件级别预计算数组中的值。

4. **单值提取**：如果只需要一个值，请使用`first`或`head`提取它。 请参阅[从数组](#arrays-to-custom-actions)中提取单个值。

在[护栏和限制](../start/guardrails.md)中了解详情。

#### 阵列大小注意事项

大型阵列可能会影响历程性能：

* **事件数组**：将事件有效负载保持在50 KB以下
* **自定义操作响应**：响应负载应小于100KB
* **数据集查找结果**：限制查找键和返回实体的数量

### 完整示例：从事件数组到自定义操作 {#complete-example}

以下是一个完整的工作流，其中显示了如何将事件数组与自定义操作结合使用。

**方案**：当用户放弃购物车时，将购物车数据发送到外部推荐API以获取个性化建议，然后在电子邮件中显示这些建议。

+++ 查看示例代码

**步骤1：配置自定义操作**

创建自定义操作“GetCartRecommendations”：

* **方法**： POST
* **URL**： `https://api.example.com/recommendations`
* **请求正文**：

```json
{
  "cartItems": [
    {
      "sku": "string",
      "price": 0,
      "quantity": 0
    }
  ]
}
```

* 将`cartItems`标记为类型`listObject`和`Variable`
* 定义字段： `sku` （字符串）、`price` （数字）、`quantity` （整数）

请参阅[配置自定义操作](../action/about-custom-action-configuration.md)以了解详情。

**步骤2：配置响应有效负载**

在自定义操作中，配置响应：

```json
{
  "recommendations": [
    {
      "productId": "string",
      "productName": "string",
      "price": 0,
      "imageUrl": "string"
    }
  ]
}
```

在[使用API调用响应](../action/action-response.md)中了解更多信息。

**步骤3：在历程中引导操作**

1. 发生购物车放弃事件后，添加自定义操作
1. 在`cartItems`集合的高级模式下：

   ```javascript
   @event{cartAbandonment.commerce.productListItems.all(currentEventField.quantity > 0)}
   ```

1. 映射收藏集字段：
   * `sku` → `productListItems.SKU`
   * `price` → `productListItems.priceTotal`
   * `quantity` → `productListItems.quantity`

**步骤4：在电子邮件中使用响应**

在电子邮件内容中，对推荐进行迭代：

```handlebars
<h2>We noticed you left these items in your cart</h2>
{{#each context.journey.events.cartAbandonment.productListItems as |item|}}
  <div class="cart-item">
    <p>{{item.name}} - Quantity: {{item.quantity}}</p>
  </div>
{{/each}}

<h2>You might also like</h2>
{{#each context.journey.actions.GetCartRecommendations.recommendations as |rec|}}
  <div class="recommendation">
    <img src="{{rec.imageUrl}}" alt="{{rec.productName}}" />
    <h3>{{rec.productName}}</h3>
    <p>${{rec.price}}</p>
  </div>
{{/each}}
```

**步骤5：测试您的配置**

运行实时历程之前，使用操作配置中的“发送测试请求”功能测试自定义操作，以验证构建的请求和值。

1. 使用[历程测试模式](../building-journeys/testing-the-journey.md)
2. 使用包含`productListItems`数组的示例事件数据触发
3. 验证自定义操作是否收到正确的数组结构
4. 检查[操作测试日志](../action/action-response.md#test-mode-logs)
5. 预览电子邮件以确认两个数组均正确显示

请参阅[自定义操作疑难解答](../action/troubleshoot-custom-action.md)以了解详情。

+++

## 最佳实践 {#best-practices}

在对上下文数据进行迭代以创建可维护、高性能个性化时，请遵循这些最佳实践。

### 使用描述性变量名称

选择明确指示您正在迭代的内容的变量名称。 这使得您的代码更易读取和维护。 详细了解[个性化语法](personalization-syntax.md)：

+++ 查看示例代码

```handlebars
<!-- Good -->
{{#each products as |product|}}
{{#each users as |user|}}
{{#each recommendations as |recommendation|}}

<!-- Less clear -->
{{#each items as |item|}}
{{#each array as |element|}}
```

+++

### 处理空数组

当数组为空时，使用`{{else}}`子句提供回退内容。 了解有关[辅助函数的更多信息](functions/helpers.md)：

+++ 查看示例代码

```handlebars
{{#each context.journey.actions.GetRecommendations.items as |item|}}
  <div>{{item.name}}</div>
{{else}}
  <p>No recommendations available at this time.</p>
{{/each}}
```

+++

### 与条件帮助程序组合

在条件内容的循环中使用`{{#if}}`。 详细了解[条件规则](create-conditions.md)，并查看[自定义操作响应](#custom-action-responses)和[数据集查找](#dataset-lookup)部分中的示例。

+++ 查看示例代码

```handlebars
{{#each context.journey.actions.GetProducts.items as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    {{#if product.onSale}}
      <span class="badge">On Sale!</span>
    {{/if}}
    {{#if product.newArrival}}
      <span class="badge">New</span>
    {{/if}}
  </div>
{{/each}}
```

+++

### 限制性能迭代

对于大型数组，请考虑限制迭代次数：

+++ 查看示例代码

```handlebars
<!-- Display only first 5 items -->
{{#each context.journey.actions.GetProducts.items as |product|}}
  {{#if @index < 5}}
    <div>{{product.name}}</div>
  {{/if}}
{{/each}}
```

+++

### 访问阵列元数据

Handlebars在循环中提供特殊变量，帮助处理高级迭代模式：

* `@index`：当前迭代索引（基于0）
* `@first`：第一个迭代为True
* `@last`：最后一个迭代为True

+++ 查看示例代码

```handlebars
{{#each products as |product|}}
  <div class="product {{#if @first}}featured{{/if}}">
    {{@index}}. {{product.name}}
  </div>
{{/each}}
```

+++

>[!NOTE]
>
>这些Handlebars变量(`@index`、`@first`、`@last`)仅在消息个性化的`{{#each}}`循环中可用。 若要在历程表达式中使用数组（例如，在传递到自定义操作之前从数组获取第一项），请使用数组函数，如[`head`](../personalization/functions/arrays-list.md#head)、[`first`](../building-journeys/expression/collection-management-functions.md)或[`all`](../building-journeys/expression/collection-management-functions.md)。 有关详细信息，请参阅[在历程表达式中使用数组](#arrays-in-journeys)。

## 故障排除 {#troubleshooting}

存在迭代问题？ 本节介绍常见问题和解决方案。

### 数组未显示

**问题**：您的数组迭代未显示任何内容。

+++ 查看可能的原因和解决方案

**可能的原因和解决方案**：

1. **不正确的路径**：根据上下文源验证数组的确切路径：
   * 对于[事件](#event-data)： `context.journey.events.<event_ID>.<fieldPath>`
   * 对于[自定义操作](#custom-action-responses)： `context.journey.actions.<actionName>.<fieldPath>`
   * 对于[数据集查找](#dataset-lookup)： `context.journey.datasetLookup.<activityID>.entities`

2. **数组为空**：添加`{{else}}`子句以检查数组是否没有数据。 有关示例，请参阅[最佳实践](#best-practices)。

3. **数据尚不可用**：请确保在历程流中的消息活动之前已执行自定义操作、事件或数据集查找活动。

+++

### 语法错误

**问题**：表达式验证失败或未呈现消息。

+++ 查看常见错误

**常见错误**：

* 缺少结束标记：每个`{{#each}}`都必须有一个`{{/each}}`。 请查看[Handlebars迭代语法](#syntax)以了解正确结构。
* 变量名称不正确：请确保在整个块中一致使用变量名称。 有关命名惯例，请参阅[最佳实践](#best-practices)。
* 路径分隔符不正确：使用点(`.`)而不使用斜线或其他字符

+++

### 测试迭代

使用[历程测试模式](../building-journeys/testing-the-journey.md)验证您的迭代。 在使用[自定义操作](#custom-action-responses)或[数据集查找](#dataset-lookup)时，这一点尤其重要：

+++ 查看测试步骤

1. 在[测试模式下开始您的历程](../building-journeys/testing-the-journey.md)
2. 使用示例数据触发事件或自定义操作
3. 检查[消息预览](../content-management/preview.md)以验证迭代是否正确显示
4. 查看测试模式日志中是否有任何错误（请参阅[自定义操作测试模式日志](../action/action-response.md#test-mode-logs)）

+++

## 相关主题 {#related-topics}

**Personalization基础知识：** [个性化入门](personalize.md) | [添加个性化](personalization-build-expressions.md) | [Personalization语法](personalization-syntax.md) | [辅助函数](functions/helpers.md) | [创建条件规则](create-conditions.md)

**历程配置：** [关于事件](../event/about-events.md) | [配置自定义操作](../action/about-custom-action-configuration.md) | [将集合传递到自定义操作参数](../building-journeys/collections.md#passing-collection) | [在自定义操作中使用API调用响应](../action/action-response.md) | [自定义操作疑难解答](../action/troubleshoot-custom-action.md) | [在历程中使用Adobe Experience Platform数据](../building-journeys/dataset-lookup.md) | [在历程中使用补充标识符](../building-journeys/supplemental-identifier.md) | [护栏和限制](../start/guardrails.md) | [测试您的历程](../building-journeys/testing-the-journey.md)

**表达式函数历程：** [高级表达式编辑器](../building-journeys/expression/expressionadvanced.md) | [集合管理函数](../building-journeys/expression/collection-management-functions.md) （第一个、全部、最后一个） | [列出函数](../building-journeys/functions/list-functions.md) （serializeList、筛选器、排序） | [数组函数](../personalization/functions/arrays-list.md) （头、尾）

**Personalization使用案例：** [购物车放弃电子邮件](personalization-use-case-helper-functions.md) | [订单状态通知](personalization-use-case.md)

**邮件设计：**[电子邮件设计入门](../email/get-started-email-design.md) | [创建推送通知](../push/create-push.md) | [创建短信消息](../sms/create-sms.md) | [预览和测试您的内容](../content-management/preview-test.md)

