---
solution: Journey Optimizer
product: journey optimizer
title: 创建您的第一个组合工作流程
description: 了解如何创建合成工作流以组合和排列现有受众。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
badge: label="Beta" type="Informative"
source-git-commit: 818c3ff2d159ec3a668c55224996b4736f950e5d
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 14%

---

# 创建您的第一个组合工作流程 {#create-compositions}

>[!BEGINSHADEBOX]

本文档包括以下内容：

* [受众组合入门](get-started-audience-orchestration.md)
* **[创建您的第一个组合工作流程](create-compositions.md)**
* [使用组合画布](composition-canvas.md)
* [访问和管理受众](access-audiences.md)

>[!ENDSHADEBOX]

## 创建合成工作流 {#create}

要创建合成工作流，请执行以下步骤：

1. 访问 **[!UICONTROL 区段]** 菜单并选择 **[!UICONTROL 创建受众]**.

1. 选择 **[!UICONTROL 组成受众]**.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL 生成规则]** 创建方法允许您使用以下对象创建新的区段定义： [分段服务](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

1. 组合画布显示有两个默认活动：

   * **[!UICONTROL Audience]**：构图的起点。 此活动允许您选择一个或多个受众作为工作流的基础，

   * **[!UICONTROL 保存]**：构成的最后一步。 利用此活动，可将工作流结果保存到新受众中。
   有关如何配置构成工作流画布中的活动的更多信息，请参阅 [使用合成画布](composition-canvas.md).

1. 打开合成属性以指定标题和描述。

   如果未在属性中定义标题，则组合的标签将设置为“组合”，其后跟有其创建日期和时间。

   ![](assets/audiences-properties.png)

1. 通过在页面之间添加所需数量的活动来配置合成 **[!UICONTROL Audience]** 和 **[!UICONTROL 保存]** 活动。 [了解如何使用合成画布](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. 准备好构成后，单击 **[!UICONTROL Publish]** 按钮以发布构成并将生成的受众保存到Adobe Experience Platform中。

   >[!IMPORTANT]
   >
   >在一个给定的沙盒中最多可发布75个合成。 如果您已达到此阈值，则需要删除合成以释放空间并发布新合成。

   如果在发布期间发生任何错误，将显示警报，其中包含有关如何解决该问题的信息。

   ![](assets/audiences-alerts.png)

1. 组合已发布。 生成的受众将保存到Adobe Experience Platform中，并准备好在Journey Optimizer营销活动中定位。 [了解如何使用营销活动](../campaigns/get-started-with-campaigns.md)

## 访问合成 {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="发布受众"
>abstract="发布您的组合以将生成的受众保存到 Adobe Experience Platform 中。"

所有创建的合成都可从以下位置访问： **[!UICONTROL 合成]** 选项卡。 它们可以具有多种状态：

* **[!UICONTROL 草稿]**：构成正在进行中，尚未发布。
* **[!UICONTROL 已发布]**：构成已发布，生成的受众已保存并可供使用。
* **[!UICONTROL 已存档]**：构成已存档。

![](assets/audiences-compositions.png)

>[!NOTE]
>
>您可以使用列表中的省略号按钮随时复制或删除现有合成。
