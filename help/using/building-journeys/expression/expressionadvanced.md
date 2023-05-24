---
solution: Journey Optimizer
product: journey optimizer
title: 关于高级表达式编辑器
description: 了解如何构建高级表达式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 運算式編輯器，資料，歷程
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 79%

---

# 关于高级表达式编辑器 {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="关于高级表达式编辑器"
>abstract="使用高级表达式编辑器可以在界面的各个屏幕中构建高级表达式。例如，您可以在配置和使用历程时以及在定义数据源条件时构建表达式。"

使用高级表达式编辑器可以在界面的各个屏幕中构建高级表达式。例如，您可以在配置和使用历程时以及在定义数据源条件时构建表达式。它还可在您每次需要定义需要特定数据操作的操作参数时使用。您可以利用来自事件的数据或从数据源检索的其他信息。在历程中，显示的事件字段列表是符合上下文的，并根据历程中添加的事件而有所不同。

高级表达式编辑器提供一组内置函数和运算符，让您处理值并定义一个专门满足您需求的表达式。高级表达式编辑器还允许您定义外部数据源参数的值、处理映射字段和集合，如体验事件。

![](../assets/journey65.png)

_高级表达式编辑器界面_

高级表达式编辑器可用于：

* 为数据源和事件信息创建[高级条件](../condition-activity.md#about_condition)
* 定义自定义[等待活动](../wait-activity.md#custom)
* 定义操作参数映射

如有可能，您可以使用 **[!UICONTROL 進階模式]** / **[!UICONTROL 簡單模式]** 按鈕。 [此处](../condition-activity.md#about_condition)介绍了简单模式。

>[!NOTE]
>
>条件可以在简单或高级表达式编辑器中定义。它们始终返回布尔类型。
>
>操作参数可以通过选择字段或通过高级表达式编辑器来定义。他们根据表达式返回特定数据类型。

## 访问高级表达式编辑器 {#accessing-the-advanced-expression-editor}

您可以通过不同方式访问高级表达式编辑器：

* 建立資料來源條件時，您可以按一下「 」以存取進階編輯器 **[!UICONTROL 進階模式]**.

   ![](../assets/journeyuc2_33.png)

* 创建自定义计时器时，系统将直接显示高级编辑器。
* 對應動作引數時，按一下 **[!UICONTROL 進階模式]**.

## 了解界面{#discovering-the-interface}

此屏幕允许您手动编写表达式。

![](../assets/journey70.png)

屏幕左侧显示了可用字段和函数：

* **[!UICONTROL 事件]**：選擇從傳入事件接收的其中一個欄位。 显示的事件字段列表是符合上下文的，并根据历程中添加的事件而有所不同。[了解详情](../../event/about-events.md)
* **[!UICONTROL 區段]**：如果您已卸除 **[!UICONTROL 區段資格]** 事件，選擇您要在運算式中使用的區段。 [了解详情](../condition-activity.md#using-a-segment)
* **[!UICONTROL 資料來源]**：從資料來源欄位群組中的可用欄位清單中選擇。 [了解详情](../../datasource/about-data-sources.md)
* **[!UICONTROL 歷程屬性]**：本節會對特定設定檔中與歷程相關的技術欄位進行重新分組。 [了解详情](journey-properties.md)
* **[!UICONTROL 函式]**：從可執行複雜篩選的內建函式清單中選擇。 函数按类别组织。[了解详情](functions.md)

![](../assets/journey65.png)

自动完成机制会显示上下文建议。

![](../assets/journey68.png)

语法验证机制检查代码的完整性。错误显示在编辑器顶部。

![](../assets/journey69.png)

**使用高级表达式编辑器构建条件时需要参数**

如果您从外部数据源选择字段，则需要调用参数（请参阅[此页面](../../datasource/external-data-sources.md)）。例如，在与天气相关的数据源中，常用的参数将为“city”。因此，必须选择要获取此城市参数的位置。还可以将函数应用于参数以执行格式更改或连接。

![](../assets/journeyuc2_19.png)

对于更复杂的用例，如果要在主表达式中包含数据源的参数，可以使用“params”关键字定义其值。请参阅[此页](../expression/field-references.md)。
