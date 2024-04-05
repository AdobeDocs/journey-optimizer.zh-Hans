---
solution: Journey Optimizer
product: journey optimizer
title: 基于属性的访问控制
description: 通过基于属性的访问控制(ABAC)，可定义用于管理特定团队或用户组的数据访问的授权。
feature: Access Management
topic: Administration
role: Admin,Leader
level: Intermediate
keywords: abac，属性，授权，数据，访问，敏感，资产
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 0%

---

# 基于属性的访问控制 {#attribute-based-access}

通过基于属性的访问控制(ABAC)，可定义用于管理特定团队或用户组的数据访问的授权。 其目的是保护敏感的数字资产，使其免遭未经授权的用户的侵害，从而进一步保护个人数据。

在Adobe Journey Optimizer中，ABAC允许您保护数据并授予特定字段元素的特定访问权限，这些元素包括体验数据模型(XDM)架构、配置文件属性和受众。

有关与ABAC一起使用的术语的更详细列表，请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/overview.html?lang=zh-Hans).

在本例中，我们想要将一个标签添加到 **国籍** 模式字段，用于限制未经授权的用户使用该字段。 要使此功能正常工作，您需要执行以下步骤：

1. 新建  **[!UICONTROL 角色]** 并为其分配相应的  **[!UICONTROL 标签]** 以便用户能够访问和使用架构字段。

1. 分配  **[!UICONTROL 标签]** 到 **国籍** Adobe Experience Platform中的架构字段。

1. 使用  **[!UICONTROL 架构字段]** 在Adobe Journey Optimizer中。

请注意 **[!UICONTROL 角色]**， **[!UICONTROL 策略]** 和 **[!UICONTROL 产品]** 也可以使用基于属性的访问控制API进行访问。 有关详细信息，请参阅此 [文档](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/abac-api/overview.html).

## 创建角色并分配标签 {#assign-role}

>[!IMPORTANT]
>
>在管理角色的权限之前，您将首先需要创建策略。 有关详细信息，请参见 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/policies.html?lang=zh-Hans).

**[!UICONTROL 角色]** 是组织内共享相同权限、标签和沙盒的一组用户。 每个用户属于一个 **[!UICONTROL 角色]** 有权使用产品中包含的Adobe应用程序和服务。
您还可以创建自己的 **[!UICONTROL 角色]** 如果您想微调用户对于界面中特定功能或对象的访问权限。

现在，我们要向选定的用户授予对 **国籍** 字段，标记为C2。 为此，我们需要创建一个 **[!UICONTROL 角色]** ，并授予他们标签C2 ，让他们使用 **国籍** 中的详细信息 **[!UICONTROL 历程]**.

1. 从 [!DNL Permissions] 产品，选择 **[!UICONTROL 角色]** 从左窗格菜单中单击 **[!UICONTROL 创建角色]**. 请注意，您还可以添加 **[!UICONTROL 标签]** 到内置角色。

   ![](assets/role_1.png)

1. 添加 **[!UICONTROL 名称]** 和 **[!UICONTROL 描述]** 到您的新的 **[!UICONTROL 角色]**，此处：受限角色人口统计。

1. 从下拉列表中，选择您的 **[!UICONTROL 沙盒]**.

   ![](assets/role_2.png)

1. 从 **[!UICONTROL 资源]** 菜单，单击 **[!UICONTROL Adobe Experience Platform]** 以打开不同的功能。 在此，我们选择 **[!UICONTROL 历程]**.

   ![](assets/role_3.png)

1. 从下拉菜单中，选择 **[!UICONTROL 权限]** 链接到选定功能，例如 **[!UICONTROL 查看历程]** 或 **[!UICONTROL 发布历程]**.

   ![](assets/role_6.png)

1. 保存您新创建的后 **[!UICONTROL 角色]**，单击 **[!UICONTROL 属性]** 以进一步配置对角色的访问权限。

   ![](assets/role_7.png)

1. 从 **[!UICONTROL 用户]** 选项卡，单击 **[!UICONTROL 添加用户]**.

   ![](assets/role_8.png)

1. 从 **[!UICONTROL 标签]** 选项卡，选择 **[!UICONTROL 添加标签]**.

   ![](assets/role_9.png)

1. 选择 **[!UICONTROL 标签]** 添加到您的角色，然后单击 **[!UICONTROL 保存]**. 在本例中，我们为用户授予标签C2以访问以前受限的架构的字段。

   ![](assets/role_4.png)

中的用户 **受限角色人口统计** 角色现在可以访问标记为C2的对象。

## 将标签分配给Adobe Experience Platform中的对象 {#assign-label}

>[!WARNING]
>
>不正确的标签使用可能会中断对人员的访问并触发策略违规。

**[!UICONTROL 标签]** 可以使用基于属性的访问控制来指定特定的功能区域。
在本例中，我们要限制对 **国籍** 字段。 此字段仅对具有相应 **[!UICONTROL 标签]** 敬他们的  **[!UICONTROL 角色]**.

请注意，您还可以添加  **[!UICONTROL 标签]** 到  **[!UICONTROL 架构]**，  **[!UICONTROL 数据集]** 和  **[!UICONTROL 受众]**.

1. 创建您的 **[!UICONTROL 架构]**. 有关详细信息，请参见 [本文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=zh-Hans).

   ![](assets/label_1.png)

1. 在新创建的 **[!UICONTROL 架构]**，我们首先添加 **[!UICONTROL 人口统计详细信息]** 包含 **国籍** 字段。

   ![](assets/label_2.png)

1. 从 **[!UICONTROL 标签]** 选项卡，在此处检查受限字段名称 **国籍**. 然后，从右窗格菜单中选择 **[!UICONTROL 编辑治理标签]**.

   ![](assets/label_3.png)

1. 选择相应的 **[!UICONTROL 标签]**&#x200B;在本例中，C2 — 数据无法导出到第三方。 有关可用标签的详细列表，请参阅 [此页面](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html#contract-labels).

   ![](assets/label_4.png)

1. 如果需要，进一步个性化您的架构，然后启用它。 有关如何启用架构的详细步骤，请参阅此 [页面](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#profile).

架构的字段现在将仅可见，并且现在只能由属于具有C2标签的角色集的用户使用。
通过应用 **[!UICONTROL 标签]** 敬您的 **[!UICONTROL 字段名称]**，请注意 **[!UICONTROL 标签]** 将自动应用于 **国籍** 每个创建的架构中的字段。

![](assets/label_5.png)

## 访问Adobe Journey Optimizer中带有标签的对象 {#attribute-access-ajo}

在标记我们的 **国籍** 字段名称以及我们的新角色，我们现在可以在Adobe Journey Optimizer中看到此限制的影响。
例如，第一个访问标记为C2的对象的历程X将创建一个用户，其条件以受限用户为目标 **[!UICONTROL 字段名称]**. 第二个用户Y无权访问标记为C2的对象，则需要发布该历程。

1. 在Adobe Journey Optimizer中，您首先需要配置 **[!UICONTROL 数据源]** 使用新架构。

   ![](assets/journey_1.png)

1. 添加新 **[!UICONTROL 字段组]** 您新创建的 **[!UICONTROL 架构]** 到内置 **[!UICONTROL 数据源]**. 您还可以创建新的外部 **[!UICONTROL 数据源]** 和关联的 **[!UICONTROL 字段组]**.

   ![](assets/journey_2.png)

1. 选择您之前创建的 **[!UICONTROL 架构]**，单击 **[!UICONTROL 编辑]** 从 **[!UICONTROL 字段]** 类别。

   ![](assets/journey_3.png)

1. 选择 **[!UICONTROL 字段名称]** 你想瞄准。 在此处，我们选择受限制的 **国籍** 字段。

   ![](assets/journey_4.png)

1. 然后，创建一个历程，向具有特定国籍的用户发送电子邮件。 添加 **[!UICONTROL 事件]** 然后 **[!UICONTROL 条件]**.

   ![](assets/journey_5.png)

1. 选择受限制的 **国籍** 用于开始构建表达式的字段。

   ![](assets/journey_6.png)

1. 编辑您的 **[!UICONTROL 条件]** 使用受限制的特定群体进行定位 **国籍** 字段。

   ![](assets/journey_7.png)

1. 根据需要个性化您的历程，我们在此添加一个 **[!UICONTROL 电子邮件]** 操作。

   ![](assets/journey_8.png)

如果无权访问标签C2对象的用户Y需要使用此受限字段访问此历程：

* 用户Y将无法使用受限字段名称，因为它将不可见。

* 在高级模式下，用户Y将无法编辑具有受限字段名称的表达式。 将出现以下错误 `The expression is invalid. Field is no longer available or you don't have enough permission to see it`.

* 用户Y可以删除表达式。

* 用户Y将无法测试历程。

* 用户Y将无法发布历程。
