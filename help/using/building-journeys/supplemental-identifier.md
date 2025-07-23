---
title: 触发事件的历程中的补充标识符
description: 了解如何在事件触发的历程中使用补充标识符。
badge: label="限量发布版" type="Informative"
exl-id: f6ebd706-4402-448a-a538-e9a4c2cf0f8b
source-git-commit: 664f38b4ff56ce871599400f898e23a8d04f7816
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 8%

---

# 触发事件的历程中的补充标识符 {#supplemental-id}

>[!CONTEXTUALHELP]
>id="ajo_journey_parameters_supplemental_identifier"
>title="使用补充标识符"
>abstract="补充标识符是辅助标识符，可为历程的执行提供额外的背景信息。若要定义它，请选择要用作补充标识符的字段，并选择与其关联的命名空间。"

>[!AVAILABILITY]
>
>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。

默认情况下，事件触发的历程会在&#x200B;**配置文件ID**&#x200B;的上下文中执行。 这意味着，只要用户档案在给定历程中处于活动状态，它就无法重新进入另一个历程。 为防止出现这种情况，Journey Optimizer允许您在事件中捕获&#x200B;**补充标识符**，例如订单ID、订阅ID、处方ID以及配置文件ID。
在本例中，我们添加了预订ID作为补充标识符。

![](assets/event-supplemental-id.png){width=40% zoomable}

这样，由事件触发的历程将在与补充标识符关联的用户档案ID（此处为预订ID）的上下文中执行。 为补充标识符的每个迭代执行历程的一个实例。 如果访客进行了不同的预订，这将允许历程中出现多个相同用户档案ID的入口。

此外，Journey Optimizer允许您利用补充标识符的属性（例如，预订编号、处方续订日期、产品类型）进行消息自定义，从而确保高度相关的通信。<!--Example: A healthcare provider can send renewal reminders for each prescription in a patient's profile.-->

➡️ [通过观看视频了解此功能](#video)

## 保护和限制 {#guardrails}

* **并发实例限制**：配置文件不能包含超过10个并发历程实例。

<!--* **Array depth**: Supplemental identifier objects can have a maximum depth of 3 levels (2 levels of nesting).

    +++Example

    ```
    [
    (level 1) "Atorvastatin" : {
    "description" : "used to lower cholesterol",
    "renewal_date" : "11/20/25",
    "dosage" : "10mg"
    (level 2) "ingredients" : [
    (level 3) "Atorvastatin calcium",
    "lactose monohydrate",
    "microcrystalline cellulose",
    "other" ]
    }
    ]
    ```

    +++
-->
* **退出标准**：如果触发退出标准，则将退出当前历程中实时接收的用户档案的所有实例。 它与配置文件ID +补充标识符组合无关。

* **频率规则**：根据补充标识符使用率创建的每个历程实例都计入频率上限，即使单个事件导致多个历程实例也是如此。

* **数据类型和架构结构**：补充标识符的类型必须为`string`。 它可以是独立的字符串属性，也可以是对象数组中的字符串属性。 独立的字符串属性将生成单个历程实例，而对象数组中的字符串属性将生成每个对象数组的迭代的唯一历程实例。 不支持字符串数组和映射。

* **历程重新进入**

  补充标识符的历程重入行为遵循现有的重入策略：

   * 如果历程是非可重新进入的，则相同的配置文件ID +补充ID组合无法重新进入历程。
   * 如果历程通过时间窗口重新进入，则可以在定义的时间窗口后重新输入相同的配置文件ID +补充ID组合。

* **下游事件配置**

  如果您在历程的下游使用另一个事件，则必须使用相同的补充ID并具有相同的ID命名空间。

## 添加补充标识符并在历程中利用它 {#add}

要在历程中使用补充标识符，请执行以下步骤：

1. **在事件架构中将属性标记为标识符**

   1. 访问事件架构，找到要用作补充标识符的属性（例如，预订ID、订阅ID），并将其标记为ID。 [了解如何使用架构](../data/get-started-schemas.md)

   1. 将标识符标记为&#x200B;**[!UICONTROL 标识]**。

      ![](assets/supplemental-ID-schema.png)

      >[!IMPORTANT]
      >
      >确保不将属性标记为&#x200B;**主标识**。

   1. 选择要与补充ID关联的命名空间。 这必须是非人员标识符命名空间。

1. **将补充ID添加到事件**

   1. 创建或编辑所需的事件。 [了解如何配置单一事件](../event/about-creating.md)

   1. 在事件配置屏幕中，选中&#x200B;**[!UICONTROL Use supplemental identifier]**&#x200B;选项。

      ![](assets/supplemental-ID-event.png)

   1. 使用表达式编辑器选择标记为补充ID的属性。

      >[!NOTE]
      >
      >确保在&#x200B;**[!UICONTROL 高级模式]**&#x200B;中使用表达式编辑器来选择属性。

   1. 选择补充ID后，关联的命名空间在事件配置屏幕中显示为只读。

1. **将事件添加到历程**

   将已配置事件拖到历程画布上。 它会根据用户档案ID和补充ID触发历程条目。

   ![](assets/supplemental-ID-journey.png)

1. **利用补充ID属性**

   使用表达式编辑器和个性化编辑器为个性化或条件逻辑引用补充标识符的属性。 可从&#x200B;**[!UICONTROL 上下文属性]**&#x200B;菜单访问属性。

   ![](assets/supplemental-ID-perso.png)

   >[!NOTE]
   >
   >如果您使用数组（例如，多个处方或策略），请使用公式来提取特定元素。

+++ 查看示例

   在补充ID为`bookingNum`且属性位于同一级别`bookingCountry`的对象数组中，历程将根据bookingNum遍历数组对象，并为每个对象创建历程实例。

   * 条件活动中的以下表达式将遍历对象数组，并检查`bookingCountry`的值是否等于“FR”：

     ```
     @event{<event_name>.<object_path>.<object_array_name>.all(currentEventField.<attribute_path>.bookingNum==${supplementalId}).at(0).<attribute_path>.bookingCountry}=="FR"
     ```

   * 电子邮件个性化编辑器中的以下表达式将遍历对象数组，提取适用于当前历程实例的`bookingCountry`，并将其显示在内容中：

     ```
     {{#each context.journey.events.<event_ID>.<object_path>.<object_array_name> as |l|}} 
     
     {%#if l.<attribute_path>.bookingNum = context.journey.technicalProperties.supplementalId%} {{l.<attribute_path>.bookingCountry}}  {%/if%}
     
     {{/each}}
     ```

   * 用于触发历程的事件示例：

     ```
     "bookingList": [
           {
               "bookingInfo": {
                   "bookingNum": "x1",
                         "bookingCountry": "US"
               }
           },
           {
               "bookingInfo": {
                   "bookingNum": "x2",
                   "bookingCountry": "FR"
               }
           }
       ]
     ```

+++

1. **发布历程**

   配置完毕后，发布历程以开始使用基于补充标识符的多个并发条目。

## 示例用例

### **策略续订通知**

* **方案**：保险公司向客户持有的每个有效保单发送续订提醒。
* **执行**：
   * 个人资料： “John”。
   * 补充ID： `"AutoPolicy123", "HomePolicy456"`。
   * 历程针对每个策略单独执行，并提供个性化的续订日期、服务范围详细信息和高级信息。

### **订阅管理**

* **方案**：当触发订阅的事件时，订阅服务会为每个订阅发送定制的消息。
* **执行**：
   * 个人资料： “Jane”。
   * 补充ID： `"Luma Yoga Program ", "Luma Fitness Program"`。
   * 每个事件都包含订阅ID以及有关该订阅的详细信息。 历程针对每个事件/订阅单独执行，从而允许每个订阅提供个性化的续订优惠。

### **产品推荐**

* **情景**：电子商务平台根据客户购买的特定产品发送推荐。
* **执行**：
   * 个人资料：“Alex”。
   * 补充ID： `"productID1234", "productID5678"`。
   * 历程针对每个产品单独执行，并提供个性化的追加销售机会。

## 操作说明视频 {#video}

了解如何在[!DNL Adobe Journey Optimizer]中启用并应用补充标识符。

>[!VIDEO](https://video.tv.adobe.com/v/3464792?quality=12)
