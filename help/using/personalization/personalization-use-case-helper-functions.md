---
solution: Journey Optimizer
product: journey optimizer
title: 个性化使用案例&colon；购物车放弃电子邮件
description: 了解如何通过用例个性化电子邮件正文。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表达式，编辑器，帮助程序，用例，个性化
exl-id: 9c9598c0-6fb1-4e2f-b610-ccd1a80e516e
source-git-commit: 02fc8825f61bd365b02788bbcd3e0647f5842bfa
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 2%

---

# 个性化使用案例：购物车放弃电子邮件 {#personalization-use-case-helper-functions}

在此示例中，您将个性化电子邮件正文。 此消息面向在购物车中遗留商品，但尚未完成购买的客户。

您将使用以下类型的辅助函数：

* 此 `upperCase` 字符串函数，以大写字母插入客户的名字。 [了解详情](functions/string.md#upper)。
* 此 `each` 帮助程序，用于列出购物车中的商品。 [了解详情](functions/helpers.md#each)。
* 此 `if` 帮助程序，在购物车中包含相关产品时插入特定于产品的注释。 [了解详情](functions/helpers.md#if-function)。
<!-- **Context**: personalization based on contextual data from the journey -->

➡️ [在此视频中了解如何使用辅助函数](#video)

在开始之前，请确保您知道如何配置这些元素：

* 单一事件。 [了解详情](../event/about-events.md)。
* 以事件开始的历程。 [了解详情](../building-journeys/using-the-journey-designer.md)。
* 历程中的电子邮件。 [了解详情](../email/create-email.md)
* 电子邮件的正文。 [了解详情](../email/content-from-scratch.md)。

执行以下步骤：

1. [创建初始事件和历程](#create-context).
1. [创建电子邮件](#configure-email).
1. [用大写字母插入客户的名字](#uppercase-function).
1. [将购物车内容添加到电子邮件](#each-helper).
1. [插入特定于产品的注释](#if-helper).
1. [测试并发布历程](#test-and-publish).

## 步骤1：创建初始事件和相关历程 {#create-context}

购物车内容是历程中的上下文信息。 因此，您必须先将初始事件和电子邮件添加到历程，然后才能将购物车特定的信息添加到电子邮件。

1. 创建其架构包含 `productListItems` 数组。
1. 将此数组中的所有字段定义为此事件的有效负荷字段。

   了解有关产品列表项数据类型的更多信息 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html){target="_blank"}.

1. 创建从此事件开始的历程。
1. 添加 **电子邮件** 历程的活动。

   ![](assets/personalization-uc-helpers-8.png)

## 第2步：创建电子邮件{#configure-email}

1. 在 **电子邮件** 活动，单击 **[!UICONTROL 编辑内容]**，然后单击 **[!UICONTROL 电子邮件设计工具]**.

   ![](assets/personalization-uc-helpers-1.png)

1. 从Email Designer主页的左侧面板中，将三个结构组件拖放到消息正文上。

1. 将HTML内容组件拖放到每个新结构组件上。

   ![](assets/personalization-uc-helpers-2.png)

## 步骤3：将客户的名字插入大写字母 {#uppercase-function}

1. 在Email Designer主页上，单击要添加客户名字的HTML组件。
1. 在上下文工具栏上，单击 **[!UICONTROL 显示源代码]**.

   ![](assets/personalization-uc-helpers-3.png)

1. 在 **[!UICONTROL 编辑HTML]** 窗口，添加 `upperCase` 字符串函数：
   1. 在左侧菜单中，选择 **[!UICONTROL 辅助函数]**.
   1. 使用搜索字段查找“大写”。
   1. 从搜索结果中，添加 `upperCase` 函数。 为此，请单击旁边的加号(+) `{%= upperCase(string) %}: string`.

      表达式编辑器显示此表达式：

      ```handlebars
      {%= upperCase(string) %}
      ```

      ![](assets/personalization-uc-helpers-4.png)

1. 从表达式中删除“string”占位符。
1. 添加名字令牌：
   1. 在左侧菜单中，选择 **[!UICONTROL 配置文件属性]**.
   1. 选择 **[!UICONTROL 人员]** > **[!UICONTROL 全名]**.
   1. 添加 **[!UICONTROL 名字]** 表达式的令牌。

      表达式编辑器显示此表达式：

      ```handlebars
      {%= upperCase(profile.person.name.firstName) %}
      ```

      ![](assets/personalization-uc-helpers-5.png)

      在中了解有关人员姓名数据类型的更多信息 [AdobeExperience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/person-name.html){target="_blank"}.

1. 单击 **[!UICONTROL 验证]**，然后单击 **[!UICONTROL 保存]**.

   ![](assets/personalization-uc-helpers-6.png)

1. 保存消息。

## 第4步：插入购物车中的项目列表 {#each-helper}

1. 重新打开消息内容。

1. 在Email Designer主页上，单击要在其中列出购物车HTML的内容组件。
1. 在上下文工具栏上，单击 **[!UICONTROL 显示源代码]**.

   ![](assets/personalization-uc-helpers-3.png)

1. 在 **[!UICONTROL 编辑HTML]** 窗口，添加 `each` 辅助函数：
   1. 在左侧菜单中，选择 **[!UICONTROL 辅助函数]**.
   1. 使用搜索字段查找“each”。
   1. 从搜索结果中，添加 `each` 助手。

      表达式编辑器显示此表达式：

      ```handlebars
      {{#each someArray as |variable|}} {{/each}}
      ```

      ![](assets/personalization-uc-helpers-9.png)

1. 添加 `productListItems` 数组的表达式：

   1. 从表达式中删除“someArray”占位符。
   1. 在左侧菜单中，选择 **[!UICONTROL 上下文属性]**.

      **[!UICONTROL 上下文属性]** 仅在历程上下文已传递到消息后可用。

   1. 选择 **[!UICONTROL Journey Optimizer]** > **[!UICONTROL 活动]** > ***[!UICONTROL event_name]***，然后展开 **[!UICONTROL productListItems]** 节点。

      在此示例中， *event_name* 表示事件的名称。

   1. 添加 **[!UICONTROL 产品]** 表达式的令牌。

      表达式编辑器显示此表达式：

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems.product as |variable|}} {{/each}}
      ```

      在此示例中， *event_ID* 表示事件的ID。

      ![](assets/personalization-uc-helpers-10.png)

   1. 修改表达式：
      1. 删除“.product”字符串。
      1. 将“variable”占位符替换为“product”。

      此示例显示了修改后的表达式：

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems as |product|}}
      ```

1. 将此代码粘贴到开始 `{{#each}}` 标记和结束 `{/each}}` 标记：

   ```html
   <table>
      <tbody>
         <tr>
            <td><b>#name</b></td>
            <td><b>#quantity</b></td>
            <td><b>$#priceTotal</b></td>
         </tr>
      </tbody>
   </table>
   ```

1. 为项目名称、数量和价格添加个性化令牌：

   1. 从HTML表中删除占位符“#name”。
   1. 从以前的搜索结果中，添加 **[!UICONTROL 名称]** 表达式的令牌。

   重复这些步骤两次：

   * 将占位符“#quantity”替换为 **[!UICONTROL 数量]** 令牌。
   * 将占位符“#priceTotal”替换为 **[!UICONTROL 总价]** 令牌。

   此示例显示了修改后的表达式：

   ```handlebars
   {{#each context.journey.events.event_ID.productListItems as |product|}}
      <table>
         <tbody>
            <tr>
               <td><b>{{context.journey.events.event_ID.productListItems.name}}</b></td>
               <td><b>{{context.journey.events.event_ID.productListItems.quantity}}</b></td>
               <td><b>${{context.journey.events.event_ID.productListItems.priceTotal}}</b></td>
            </tr>
         </tbody>
      </table>
   {{/each}}
   ```

1. 单击 **[!UICONTROL 验证]**，然后单击 **[!UICONTROL 保存]**.

   ![](assets/personalization-uc-helpers-11.png)

## 步骤5：插入特定于产品的说明 {#if-helper}

1. 在Email Designer主页上，单击要插入注释的HTML组件。
1. 在上下文工具栏上，单击 **[!UICONTROL 显示源代码]**.

   ![](assets/personalization-uc-helpers-3.png)

1. 在 **[!UICONTROL 编辑HTML]** 窗口，添加 `if` 辅助函数：
   1. 在左侧菜单中，选择 **[!UICONTROL 辅助函数]**.
   1. 使用搜索字段查找“if”。
   1. 从搜索结果中，添加 `if` 助手。

      表达式编辑器显示此表达式：

      ```handlebars
      {%#if condition1%} render_1
         {%else if condition2%} render_2
         {%else%} default_render
      {%/if%}
      ```

      ![](assets/personalization-uc-helpers-12.png)

1. 从表达式中删除此条件：

   ```handlebars
   {%else if condition2%} render_2
   ```

   此示例显示了修改后的表达式：

   ```handlebars
   {%#if condition1%} render_1
      {%else%} default_render
   {%/if%}
   ```

1. 将产品名称令牌添加到条件：
   1. 从表达式中删除“condition1”占位符。
   1. 在左侧菜单中，选择 **[!UICONTROL 上下文属性]**.
   1. 选择 **[!UICONTROL Journey Orchestration]** > **[!UICONTROL 活动]** > ***[!UICONTROL event_name]***，然后展开 **[!UICONTROL productListItems]** 节点。

      在此示例中， *event_name* 表示事件的名称。

   1. 添加 **[!UICONTROL 名称]** 表达式的令牌。

      表达式编辑器显示此表达式：

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name%}
         render_1
         {%else%} default_render
      {%/if%}
      ```

      ![](assets/personalization-uc-helpers-13.png)

1. 修改表达式：
   1. 在表达式编辑器中，在 `name` 令牌。

      请使用此语法，其中 *product_name* 表示产品的名称：

      ```javascript
      = "product_name"
      ```

      在此示例中，产品名称为“Juno Jacket”：

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         render_1
         {%else%} default_render
      {%/if%}
      ```

   1. 将“render_1”占位符替换为注释文本。

      示例：

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         Due to longer than usual lead times on the Juno Jacket, please expect item to ship two weeks after purchase.
         {%else%} default_render
      {%/if%}
      ```

   1. 从表达式中删除“default_render”占位符。
1. 单击 **[!UICONTROL 验证]**，然后单击 **[!UICONTROL 保存]**.

   ![](assets/personalization-uc-helpers-14.png)

1. 保存消息。

## 步骤6：测试并发布旅程 {#test-and-publish}

1. 打开 **[!UICONTROL 测试]** 切换，然后单击 **[!UICONTROL 触发事件]**.

   ![](assets/personalization-uc-helpers-15.png)

1. 在 **[!UICONTROL 事件配置]** 窗口中，输入输入值，然后单击 **[!UICONTROL 发送]**.

   测试模式仅适用于测试用户档案。

   ![](assets/personalization-uc-helpers-16.png)

   电子邮件将发送到测试用户档案的地址。

   在此示例中，电子邮件包含有关Juno Jacket的注释，因为该产品位于购物车中：

   ![](assets/personalization-uc-helpers-17.png)

1. 验证没有错误，然后发布历程。


## 相关主题 {#related-topics}

### Handlebars函数 {#handlebars}

* [辅助程序](functions/helpers.md)

* [字符串函数](functions/string.md)

### 用例 {#use-case}

* [使用用户档案信息、上下文和选件进行个性化](personalization-use-case.md)

* [通过基于决策的优惠进行个性化](../offers/offers-e2e.md)

## 操作方法视频{#video}

了解如何使用辅助函数。

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
