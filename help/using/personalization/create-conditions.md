---
title: 创建条件
description: 了解如何创建条件
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
source-git-commit: 9593ea40853221e0eec45f30f7635d8a116b03c1
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 1%

---


# 使用条件规则 {#conditions}

条件规则是一组规则，用于定义消息中应显示的内容，具体取决于各种标准，如用户档案属性、区段成员资格或上下文事件。

条件规则是使用表达式编辑器创建的，如果要在内容中重复使用条件规则，可以对其进行存储。 [了解如何将条件规则保存到库](#save)

>[!NOTE]
>
>个人需要 [管理库项目](../administration/ootb-product-profiles.md) 保存或删除条件规则的权限。 保存的条件可供组织内的所有用户使用。

## 访问条件规则生成器 {#access}

条件规则是从 **[!UICONTROL 条件]** 表达式编辑器中的菜单，可访问该菜单的以下任一位置：

* 在Email Designer中为电子邮件正文中的组件启用动态内容时。 [了解如何将动态内容添加到电子邮件中](dynamic-content.md#emails)

   ![](assets/conditions-access-email.png)

* 在可以使用 [表达式编辑器](personalization-build-expressions.md).

   ![](assets/conditions-access-editor.png)

## 创建条件规则 {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions_create"
>title="创建条件"
>abstract="合并用户档案属性、上下文事件或受众，以构建规则来定义消息中应显示的内容。"

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions"
>title="创建条件"
>abstract="合并用户档案属性、上下文事件或受众，以构建规则来定义消息中应显示的内容。"

创建条件规则的步骤如下所示：

1. 访问 **[!UICONTROL 条件]** 菜单，然后单击 **[!UICONTROL 新建]**.

1. 根据需要构建条件规则。 要实现此目的，请将所需属性从左侧菜单拖放到画布中，并排列到画布中。

   将属性合并到画布中的步骤与区段生成体验类似。 有关如何使用规则生成器画布的更多信息，请参阅 [本文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#rule-builder-canvas).

   ![](assets/conditions-create.png)

   属性分为三个选项卡：

   * **[!UICONTROL 配置文件]**:
      * **[!UICONTROL 区段成员资格]** 列出所有区段属性（即状态、版本等） 表示 [Adobe Experience Platform分段服务](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html),
      * **[!UICONTROL XDM单个配置文件]** 列出与 [体验数据模型(XDM)架构](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans) 在Adobe Experience Platform中定义。
   * **[!UICONTROL 情境]**:在历程中使用消息时，上下文历程字段可通过此选项卡使用。
   * **[!UICONTROL 受众]**:列出从中创建的区段生成的所有受众 [Adobe Experience Platform分段服务](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

1. 条件规则准备就绪后，您可以将其添加到消息中以创建动态内容。 [了解如何添加动态内容](dynamic-content.md)

   您还可以保存规则以供进一步重复使用。 [了解如何保存条件](#save)

## 保存条件规则 {#save}

如果有条件规则需要经常重复使用，则可以将其保存到条件库。 所有保存的规则都是共享的，组织内的个人都可以访问并使用这些规则。

>[!NOTE]
>
>利用历程上下文属性的条件规则无法保存到库。

1. 在条件编辑屏幕中，单击 **[!UICONTROL 保存条件]** 按钮。

1. 为规则指定名称和描述（可选），然后单击 **[!UICONTROL 添加]**.

   ![](assets/conditions-name-description.png)

1. 条件规则将保存到库。 您现在可以使用它在消息中创建动态内容。 [了解如何添加动态内容](dynamic-content.md)

## 编辑和删除保存的条件规则 {#edit-delete}

您可以随时使用椭圆按钮删除条件规则。

![](assets/conditions-open.png)

无法修改保存到库的条件规则。 但是，您仍可以使用它们创建新规则。 为此，请打开条件规则，进行所需的更改，然后将其保存到库。 [了解如何将条件保存到库](#save)
