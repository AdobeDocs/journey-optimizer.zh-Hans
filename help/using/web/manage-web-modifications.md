---
title: 管理 Web 修改
description: 了解如何管理Journey Optimizer网页内容中的修改
feature: Web Channel
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 213511b4-7556-4a25-aa23-b50acd11cd34
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 11%

---

# 管理 Web 修改 {#manage-web-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="轻松管理所有更改"
>abstract="使用此窗格，您可以浏览和管理您添加到网页的所有调整和样式。"

您可以轻松管理添加到网页的所有组件、调整和样式。 您还可以直接从专用窗格添加修改。

## 使用修改窗格 {#use-modifications-pane}

1. 选择 **[!UICONTROL 修改]** 图标，以在左侧显示相应的窗格。

   ![](assets/web-designer-modifications-pane.png)

1. 您可以查看对页面所做的每项更改。

1. 选择不需要的修改，然后单击 **[!UICONTROL 删除修改]** 选项来自 **[!UICONTROL 更多操作]** 按钮将其删除。

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >在删除操作时请务必谨慎，因为此操作可能影响后续操作。

1. 要同时删除多个修改，请单击 **[!UICONTROL 选择]** 按钮位于顶部 **[!UICONTROL 修改]** 窗格，检查您选择的修改内容，然后单击 **[!UICONTROL 删除]** 图标。

   ![](assets/web-designer-modifications-select-delete.png)

1. 使用 **[!UICONTROL 更多操作]** 按钮位于顶部 **[!UICONTROL 修改]** 窗格，以便一次删除所有修改。

   ![](assets/web-designer-delete-modifications.png)

1. 您还可以仅删除无效的修改，即由其他更改覆盖的更改。 例如，如果修改文本的颜色，然后删除该文本，则颜色修改将变得无效，因为该文本已不存在。

1. 您可以使用取消和重做操作 **[!UICONTROL 撤消/重做]** 按钮。

   ![](assets/web-designer-undo-redo.png)

   单击并按住按钮以在 **[!UICONTROL 还原]** 和 **[!UICONTROL 重做]** 选项。 然后，单击按钮本身以应用所需的操作。

## 从专用窗格中添加修改 {#add-modifications}

使用Web设计器编辑页面时，可以直接从 **[!UICONTROL 修改]** 窗格 — 无需从Web设计器界面中选择组件并进行编辑。 请按照以下步骤操作。

1. 从 **[!UICONTROL 修改]** 窗格，单击 **[!UICONTROL 更多操作]** 按钮。

1. 选择 **[!UICONTROL 添加修改]**.

   ![](assets/web-designer-add-modification.png)

1. 选择修改类型：

   * **[!UICONTROL CSS选择器]** - [了解详情](#css-selector)
   * **[!UICONTROL 页面`<Head>`]** - [了解详情](#page-head)

1. 输入您的内容并 **[!UICONTROL 保存]** 您所做的更改。

1. 单击 **[!UICONTROL 更多操作]** 按钮进行修改，然后选择 **[!UICONTROL 信息]** 以显示其详细信息。

   ![](assets/web-designer-add-modification-info.png)

### CSS选择器 {#css-selector}

添加 **CSS选择器** 键入modification ，请按照以下步骤操作。

1. 选择 **[!UICONTROL CSS选择器]** 作为修改类型。

1. 此 **[!UICONTROL CSS元素选择器]** 字段可以帮助您查找和选择要应用更改的HTML元素（或DOM树中的节点）。 <!--specify the desired CSS element that you want to modify.-->

   ![](assets/web-designer-add-modification-css.png)

1. 选择操作类型(**[!UICONTROL 设置内容]** 或 **[!UICONTROL 设置属性]**)并填写所需的信息/内容。

   * **[!UICONTROL 设置内容]**：指定进入由标识的元素中的内容 **[!UICONTROL CSS元素选择器]** 字段。

   * **[!UICONTROL 设置属性]**：指定要与当前CSS选择器关联的属性，以便该选择器能够也由此属性进行标识。 要执行此操作，请在 **[!UICONTROL 属性名称]** 字段和中的值 **[!UICONTROL 内容]** 字段。 如果属性已存在，则更新值；否则，将添加具有指定名称和值的新属性。

     ![](assets/web-designer-add-modification-css-attribute.png)

### 页面 `<head>` {#page-head}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_head"
>title="添加自定义代码"
>abstract="HEAD 元素是元数据的容器，置于 HTML 标记与 BODY 标记之间。请仅添加 SCRIPT 和 STYLE 元素。添加 DIV 标记和其他元素可能会导致其余的 HEAD 元素出现在 BODY 中。"

您可以使用添加自定义代码 **[!UICONTROL 页面`<head>`]** 修改类型。

此 `<head>` 元素是元数据（有关数据的数据）的容器，它放置在 `<html>` 标记和 `<body>` 标记之前。 在这种情况下，代码不会等待主体或页面加载事件，而是在页面加载开始时执行。

此 `<head>` 元素通常用于将JavaScript或CSS代码添加到页面顶部。 适用于后续可视化操作的选择器取决于此选项卡中添加的 HTML 元素。

添加 **页面`<head>`** 键入modification ，请按照以下步骤操作。

1. 选择 **[!UICONTROL 页面`<head>`]** 作为修改类型。

   ![](assets/web-designer-add-modification-head-type.png)

1. 将您的自定义代码添加到 **[!UICONTROL 内容]** 盒子。

   >[!CAUTION]
   >
   >您只能添加 `<script>` 和 `<style>` 元素到 `<head>` 部分。 正在添加 `<div>` 标记和其他元素可能会导致剩余 `<head>` 要跳入 `<body>`.

1. 单击 **[!UICONTROL 高级编辑选项]** 按钮。 表达式编辑器将打开。

   ![](assets/web-designer-add-modification-head-advanced.png)

   您可以利用 [!DNL Journey Optimizer] 具有所有个性化和创作功能的表达式编辑器。 [了解详情](../personalization/personalization-build-expressions.md)

#### 自定义代码示例 {#custom-code-examples}

您可以使用 **[!UICONTROL 页面`<head>`]** 修改类型：

* 使用JavaScript内联或链接到外部JavaScript文件。

  例如，要更改元素的颜色，请执行以下操作：

  ```
  <script type="text/javascript">
  document.getElementById("element_id").style.color = "blue";
  </script>
  ```

* 配置指向外部样式表的内联样式或链接。

  例如，要为overlay元素定义类：

  ```
  <style>
  .overlay
  { position: absolute; top:0; left: 0; right: 0; bottom: 0; background: red; }
  </style>
  ```

#### 自定义代码最佳实践 {#custom-code-best-practices}

+++ **始终将自定义代码包装在一个元素中。**

例如：

```
<script>
// Code goes here
</script>
```

如果需要进行任何修改，请在此容器中进行更改。

如果您不再需要自定义代码，只需将此容器留空，但不要将其删除。 这可以确保其他体验修改不受影响。

+++

+++ **请勿在自定义代码脚本中执行document.write操作。**

脚本是异步执行的。这通常会导致document.write操作出现在页面上错误的位置。 不建议在自定义代码内创建的脚本中使用document.write。

+++

+++ **如果创建一个元素然后对其进行修改，请不要删除原始元素。**

每次更改都会在 **[!UICONTROL 修改]** 面板。 因为第2个操作修改了Element 1，如果删除Element 1，则该操作将没有任何可修改的内容，因此更改不再有效。

+++

+++ **使用时要小心**[!UICONTROL &#x200B;页面 `<head>`]**影响同一URL的两个营销活动的修改类型。**

如果您使用 **[!UICONTROL 页面`<head>`]** 修改类型对于影响同一URL的两个营销活动，JavaScript会从这两个营销活动注入页面。 [!DNL Journey Optimizer] 自动确定已交付内容的顺序。 确保代码与放置无关。 由您来确保代码中没有冲突。

+++
