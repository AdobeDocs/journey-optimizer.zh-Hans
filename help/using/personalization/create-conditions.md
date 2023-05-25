---
solution: Journey Optimizer
product: journey optimizer
title: 创建条件
description: 了解如何创建条件
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表达式，编辑器，条件，规则
exl-id: 246a4a55-059e-462c-ac1e-43b90f4abda4
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 8%

---

# 使用条件规则 {#conditions}

条件规则是一组规则，用于定义应在消息中显示哪些内容，具体取决于用户档案属性、区段成员资格或上下文事件等各种条件。

条件规则是使用表达式编辑器创建的，如果要跨内容重用这些规则，可以存储这些规则。 [了解如何将条件规则保存到库](#save)

>[!NOTE]
>
>个人将需要 [管理库项目](../administration/ootb-product-profiles.md) 保存或删除条件规则的权限。 保存后的条件可供组织内的所有用户使用。

## 访问条件规则生成器 {#access}

条件规则是从以下位置创建的 **[!UICONTROL 条件]** 表达式编辑器中的菜单，可通过以下任一方式访问：

* 在Email Designer中为电子邮件正文中的组件启用动态内容时。 [了解如何将动态内容添加到电子邮件中](dynamic-content.md#emails)

   ![](assets/conditions-access-email.png)

* 在任何您可以使用添加个性化的字段中 [表达式编辑器](personalization-build-expressions.md).

   ![](assets/conditions-access-editor.png)

## 创建条件规则 {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions_create"
>title="创建条件"
>abstract="结合配置文件属性、上下文事件或受众来构建规则，以定义应在消息中显示哪些内容。"

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions"
>title="创建条件"
>abstract="结合配置文件属性、上下文事件或受众来构建规则，以定义应在消息中显示哪些内容。"

创建条件规则的步骤如下：

1. 访问 **[!UICONTROL 条件]** 表达式编辑器或电子邮件设计器中的菜单，然后单击 **[!UICONTROL 新建]**.

1. 根据需要构建条件规则。 为此，请将所需属性从左侧菜单拖放并排列到画布中。

   将属性组合到画布中的步骤与区段构建体验类似。 有关如何使用规则生成器画布的更多信息，请参阅 [本文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#rule-builder-canvas).

   ![](assets/conditions-create.png)

   属性分为三个选项卡：

   * **[!UICONTROL 配置文件]**:
      * **[!UICONTROL 区段成员资格]** 列出所有区段属性（即状态、版本等） 对象 [Adobe Experience Platform Segmentation service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)，
      * **[!UICONTROL XDM个人资料]** 列出与关联的所有配置文件属性 [Experience Data Model (XDM)架构](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans) 在Adobe Experience Platform中定义。
   * **[!UICONTROL 上下文]**：当您的消息在历程中使用时，上下文历程字段可通过此选项卡使用。
   * **[!UICONTROL 受众]**：列出从在中创建的区段生成的所有受众 [Adobe Experience Platform Segmentation service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

1. 条件规则准备就绪后，您可以将其添加到消息以创建动态内容。 [了解如何添加动态内容](dynamic-content.md)

   您还可以保存规则以进一步重复使用。 [了解如何保存条件](#save)

## 保存条件规则 {#save}

如果存在将经常重用的条件规则，则可以将其保存到条件库。 所有保存的规则都将共享，并可由组织内的个人访问和使用。

>[!NOTE]
>
>无法将利用历程上下文属性的条件规则保存到库。

1. 在条件版本屏幕中，单击 **[!UICONTROL 保存条件]** 按钮。

1. 为规则指定名称和描述（可选），然后单击 **[!UICONTROL 添加]**.

   ![](assets/conditions-name-description.png)

1. 条件规则将保存到库。 您现在可以使用它在消息中创建动态内容。 [了解如何添加动态内容](dynamic-content.md)

## 编辑和删除已保存的条件规则 {#edit-delete}

您可以使用省略号按钮随时删除条件规则。

![](assets/conditions-open.png)

无法修改保存到库的条件规则。 但是，您仍可以使用它们创建新规则。 为此，请打开条件规则，进行所需的更改，然后将其保存到库。 [了解如何将条件保存到库](#save)
