---
title: 基于属性的访问控制
description: 了解基于属性的访问控制
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
source-git-commit: 630b8ef5a140709161b24256083b2104be5b6121
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 2%

---

# 基于属性的访问控制 {#attribute-based-access}

>[!IMPORTANT]
>
>基于属性的访问控制目前仅适用于一组组织（有限可用性）。 如果要利用此功能，请联系您的Adobe客户经理。

基于属性的访问控制(ABAC)允许您定义权限，以管理特定团队或用户组的数据访问。 其目的是保护敏感数字资产免受未经授权用户的侵害，从而进一步保护个人数据。

在Adobe Journey Optimizer中，ABAC允许您保护数据并授予对特定字段元素的特定访问权限，这些元素包括体验数据模型(XDM)架构、用户档案属性和区段。

<!--For a more detailed list of the terminology used with ABAC, refer to Adobe Experience Platform documentation.-->

在本例中，我们要向 **国籍** 架构字段，以限制未授权用户使用该架构。 要使此功能正常工作，您需要执行以下步骤：

1. 分配  **[!UICONTROL Label]** 到 **国籍** 架构字段。Adobe Experience Platform

2. 新建  **[!UICONTROL Role]** 并为其分配相应的  **[!UICONTROL Label]** 使用户能够访问和使用架构字段。

3. 使用  **[!UICONTROL Schema field]** 在Adobe Journey Optimizer。

## 为Adobe Experience Platform中的对象分配标签 {#assign-label}

>[!WARNING]
>
>错误的标签使用可能会中断对人员的访问并触发策略违规。

**[!UICONTROL Labels]** 可以使用基于属性的访问控制来分配特定的功能区域。
在本例中，我们要限制对 **国籍** 字段。 只有具有相应 **[!UICONTROL Label]** 到  **[!UICONTROL Role]**.

请注意，您还可以  **[!UICONTROL Label]** to  **[!UICONTROL Schema]**,  **[!UICONTROL Datasets]** 和  **[!UICONTROL Segments]**.

1. 创建 **[!UICONTROL Schema]**. 有关更多信息，请参阅 [本文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=zh-Hans).

   ![](assets/label_1.png)

1. 在新创建的 **[!UICONTROL Schema]**，我们会首先在 **[!UICONTROL Demographic details]** 包含的字段组 **国籍** 字段。

   ![](assets/label_2.png)

1. 从 **[!UICONTROL Labels]** ，请在此处查看受限字段名称 **国籍**. 然后，从右窗格菜单中，选择 **[!UICONTROL Edit governance labels]**.

   ![](assets/label_3.png)

1. 选择相应的 **[!UICONTROL Label]**，在这种情况下， C2 — 数据无法导出到第三方。 有关可用标签的详细列表，请参阅 [本页](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html#contract-labels).

   ![](assets/label_4.png)

1. 根据需要进一步个性化您的架构，然后启用它。 有关如何启用架构的详细步骤，请参阅此 [页面](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#profile).

您架构的字段现在将只可见，并且现在只能由使用C2标签的角色集的一部分的用户使用。
通过应用 **[!UICONTROL Label]** 至 **[!UICONTROL Field name]**，请注意 **[!UICONTROL Label]** 将自动应用于 **国籍** 字段。

![](assets/label_5.png)

## 创建角色并分配标签 {#assign-role}

**[!UICONTROL Roles]** 是您组织内共享相同权限、标签和沙箱的一组用户。 每个用户属于 **[!UICONTROL Role]** 有权使用产品中包含的Adobe应用程序和服务。
您还可以创建自己的 **[!UICONTROL Roles]** 如果您想要优化用户对界面中特定功能或对象的访问权限。

我们现在要向选定用户授予 **国籍** 字段，标记为C2。 为此，我们需要创建一个 **[!UICONTROL Role]** 并为他们授予标签C2，以便他们使用 **国籍** 详细信息 **[!UICONTROL Message]** 或 **[!UICONTROL Journey]**.

1. 从 [!DNL Permissions] 产品，选择 **[!UICONTROL Role]** 从左窗格菜单中，单击 **[!UICONTROL Create role]**. 请注意，您还可以 **[!UICONTROL Label]** 内置角色。

   ![](assets/role_1.png)

1. 添加 **[!UICONTROL Name]** 和 **[!UICONTROL Description]** 新 **[!UICONTROL Role]**，此处：角色人口限制。

1. 从下拉菜单中，选择 **[!UICONTROL Sandbox]**.

   ![](assets/role_2.png)

1. 从 **[!UICONTROL Resources]** 菜单，单击 **[!UICONTROL Adobe Experience Platform]** 以打开不同的功能。 在此，我们选择 **[!UICONTROL Messages]**.

   ![](assets/role_3.png)

1. 从下拉菜单中，选择 **[!UICONTROL Permissions]** 链接到所选功能，例如 **[!UICONTROL View messages]** 或 **[!UICONTROL Publish journeys]**.

   ![](assets/role_6.png)

1. 保存新创建的 **[!UICONTROL Role]**，单击 **[!UICONTROL Properties]** 以进一步配置对您角色的访问权限。

   ![](assets/role_7.png)

1. 在选项卡 **[!UICONTROL Users]** 中，单击 **[!UICONTROL Add users]**。

   ![](assets/role_8.png)

1. 在 **[!UICONTROL Labels]** 选项卡中，选择 **[!UICONTROL Add label]**。

   ![](assets/role_9.png)

1. 选择 **[!UICONTROL Labels]** 要添加到您的角色并单击 **[!UICONTROL Save]**. 在本例中，我们将为用户授予标签C2，以便其有权访问以前受限架构的字段。

   ![](assets/role_4.png)

中的用户 **受限角色人口统计** 角色现在可以访问C2标记的对象。

## 访问Adobe Journey Optimizer中的标记对象 {#attribute-access-ajo}

在标记 **国籍** 字段名称（在新架构和新角色中），我们现在可以在Adobe Journey Optimizer中查看此限制的影响。
例如，对标有C2的对象具有访问权限的第一个用户X将创建一个历程，该用户的条件是定位受限制的 **[!UICONTROL Field name]**. 如果第二个用户Y无权访问标有C2的对象，则需要发布该历程。

1. 在Adobe Journey Optimizer中，您首先需要配置 **[!UICONTROL Data source]** 使用新模式。

   ![](assets/journey_1.png)

1. 添加新 **[!UICONTROL Field group]** 新建 **[!UICONTROL Schema]** 内置 **[!UICONTROL Data source]**. 您还可以创建新的外部 **[!UICONTROLD数据源]** 关联 **[!UICONTROL Field groups]**.

   ![](assets/journey_2.png)

1. 选择您之前创建的 **[!UICONTROL Schema]**，单击 **[!UICONTROL Edit]** 从 **[!UICONTROL Fields]** 类别。

   ![](assets/journey_3.png)

1. 选择 **[!UICONTROL Field name]** 要定位。 在此，我们选择受限 **国籍** 字段。

   ![](assets/journey_4.png)

1. 然后，创建历程，以向具有特定国籍的用户发送消息。 添加 **[!UICONTROL Event]** 那么 **[!UICONTROL Condition]**.

   ![](assets/journey_5.png)

1. 选择受限制的 **国籍** 字段来开始构建表达式。

   ![](assets/journey_6.png)

1. 编辑 **[!UICONTROL Condition]** 以限制 **国籍** 字段。

   ![](assets/journey_7.png)

1. 根据需要将您的历程个性化，在此我们添加 **[!UICONTROL Message]** 操作。

   ![](assets/journey_8.png)

如果无权访问标签C2对象的用户Y需要访问此历程或具有此限制字段的任何消息：

* 用户Y将无法使用受限的字段名称，因为它不可见。

* 在高级模式下，用户Y将无法编辑具有受限字段名称的表达式。 将显示以下错误 `The expression is invalid. Field is no longer available or you don't have enough permission to see it`.

* 用户Y可以删除表达式。

* 用户Y将无法测试历程或消息。

* 用户Y将无法发布历程或消息。
