---
solution: Journey Optimizer
product: journey optimizer
title: 使用高级表达式编辑器
description: 了解如何构建高级表达式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 表达式编辑器，数据，历程
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
source-git-commit: b69023669b6ca59ea5980b1a671a90c41eb665fb
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 55%

---

# 使用高级表达式编辑器 {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="关于高级表达式编辑器"
>abstract="使用高级表达式编辑器可以在界面的各个屏幕中生成高级表达式。例如，您可以在配置和使用历程时以及在定义数据源条件时生成表达式。"

使用历程高级表达式编辑器在界面的各种屏幕中构建高级表达式。 例如，您可以在配置和使用历程时以及在定义数据源条件时生成表达式。

它还可在您每次需要定义需要特定数据操作的操作参数时使用。您可以利用来自事件的数据或从数据源检索的其他信息。在历程中，显示的事件字段列表是符合上下文的，并根据历程中添加的事件而有所不同。

![](../assets/journey65.png)


高级表达式编辑器提供一组内置函数和运算符，让您处理值并定义一个专门满足您需求的表达式。高级表达式编辑器还允许您定义外部数据源参数的值、处理映射字段和集合。

>[!NOTE]
>
>历程高级表达式编辑器中可用的功能和功能与[个性化编辑器](../../personalization/functions/functions.md)中可用的功能和功能不同。

## 访问高级表达式编辑器 {#accessing-the-advanced-expression-editor}

高级表达式编辑器可用于：

* 为数据源和事件信息创建[高级条件](../condition-activity.md#about_condition)
* 定义自定义[等待活动](../wait-activity.md#custom)
* 定义操作参数映射

如果可能，您可以使用&#x200B;**[!UICONTROL 高级模式]** / **[!UICONTROL 简单模式]**&#x200B;按钮在两种模式之间切换。 [此处](../condition-activity.md#about_condition)介绍了简单模式。

>[!NOTE]
>
>* 条件可以在简单或高级表达式编辑器中定义。它们始终返回布尔类型。
>
>* 操作参数可以通过选择字段或通过高级表达式编辑器来定义。他们根据表达式返回特定数据类型。

您可以通过不同方式访问高级表达式编辑器：

* 在创建数据源条件时，单击&#x200B;**[!UICONTROL 高级模式]**&#x200B;可访问高级编辑器。

  ![](../assets/journeyuc2_33.png)

* 创建自定义计时器时，系统将直接显示高级编辑器。
* 映射操作参数时，单击&#x200B;**[!UICONTROL 高级模式]**。

## 探索界面 {#discovering-the-interface}

此屏幕允许您手动编写表达式。

![](../assets/journey70.png)

屏幕左侧显示了可用字段和函数：

* **[!UICONTROL 事件]**：选择从入站事件接收的字段之一。 显示的事件字段列表是符合上下文的，并根据历程中添加的事件而有所不同。 [了解详情](../../event/about-events.md)

  >[!CAUTION]
  >
  >不支持使用体验事件创建表达式。 [此处](../../building-journeys/exp-event-lookup.md)引用了使用体验事件创建表达式/逻辑的替代方法和最佳实践

* **[!UICONTROL 受众]**：如果您已删除&#x200B;**[!UICONTROL 受众资格]**&#x200B;事件，请选择要在表达式中使用的受众。 [了解详情](../condition-activity.md#using-a-segment)
* **[!UICONTROL 数据源]**：从数据源的字段组提供的字段列表中进行选择。 [了解详情](../../datasource/about-data-sources.md)
* **[!UICONTROL 历程属性]**：此部分重新分组与给定用户档案的历程相关的技术字段。 [了解详情](journey-properties.md)
* **[!UICONTROL 函数]**：从允许执行复杂筛选的内置函数列表中进行选择。 函数按类别组织。 [了解详情](functions.md)

![](../assets/journey65.png)

自动完成机制会显示上下文建议。

![](../assets/journey68.png)

语法验证机制检查代码的完整性。错误显示在编辑器顶部。

![](../assets/journey69.png)


>[!TIP]
>
>在高级表达式编辑器中创建条件时，请确保表达式不包含隐藏或不可打印的字符。 此外，使用单行表达式以避免分析错误。


**使用高级表达式编辑器构建条件时需要参数**

如果您从外部数据源中选择需要调用参数的字段（请参阅[此页面](../../datasource/external-data-sources.md)），则右侧将显示一个新选项卡，允许您指定此参数。 参数值可能来自位于历程或Experience Platform数据源中的事件（而非其他外部数据源）。 例如，在与天气相关的数据源中，常用的参数将为“city”。因此，必须选择要获取此城市参数的位置。还可以将函数应用于参数以执行格式更改或连接。

![](../assets/journeyuc2_19.png)

对于更复杂的用例，如果要在主表达式中包含数据源的参数，可以使用“params”关键字定义其值。请参阅[此页](../expression/field-references.md)。
