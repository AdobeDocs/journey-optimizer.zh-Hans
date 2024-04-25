---
solution: Journey Optimizer
product: journey optimizer
title: 创建您的第一个组合工作流程
description: 了解如何创建组合工作流以组合和排列现有受众。
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: 01c14590fe55d8f11c1ff2b18141933b0b3dd5ca
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 15%

---

# 创建您的第一个组合工作流程 {#create-compositions}

>[!BEGINSHADEBOX]

此文档提供了有关如何在 Adobe Journey Optimizer 中使用受众组合的详细信息。如果您没有使用Adobe Journey Optimizer， [单击此处](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=zh-Hans){target="_blank"}.

>[!ENDSHADEBOX]

## 创建合成工作流 {#create}

要创建合成工作流，请执行以下步骤：

1. 访问 **[!UICONTROL 受众]** 菜单并选择 **[!UICONTROL 创建受众]**.

1. 选择 **[!UICONTROL 组成受众]**.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL 生成规则]** 创建方法允许您使用以下对象创建新的区段定义： [分段服务](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=zh-Hans).

1. 组合画布显示有两个默认活动：

   * **[!UICONTROL 受众]**：构图的起点。 此活动允许您选择一个或多个受众作为工作流的基础，

   * **[!UICONTROL 保存]**：构成的最后一步。 此活动用于将工作流结果保存到新受众中。

   有关如何配置构成工作流画布中的活动的更多信息，请参阅 [使用合成画布](composition-canvas.md).

1. 打开合成属性以指定标题和描述。

   如果未在属性中定义标题，则排版标签将设置为“排版”，其后跟其创建日期和时间。

   ![](assets/audiences-properties.png)

1. 通过添加所需数量的活动来配置合成，具体方法是 **[!UICONTROL 受众]** 和 **[!UICONTROL 保存]** 活动。 [了解如何使用合成画布](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. 合成准备就绪后，单击 **[!UICONTROL Publish]** 按钮以发布构成并将生成的受众保存到Adobe Experience Platform中。

   >[!IMPORTANT]
   >
   >您最多可以在给定沙盒中发布10个合成。 如果您已达到此阈值，则需要删除组合以释放空间，然后才能发布新组合。

   如果在发布期间发生任何错误，将显示警报，其中包含有关如何解决该问题的信息。

   ![](assets/audiences-alerts.png)

1. 组合已发布。 生成的受众将保存到Adobe Experience Platform中，并准备好在Journey Optimizer中定位。 [了解如何在Journey Optimizer中定位受众](../audience/about-audiences.md#segments-in-journey-optimizer)

## 访问组合 {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="发布受众"
>abstract="发布您的组合以将生成的受众保存到 Adobe Experience Platform 中。"

所有创建的合成都可以从 **[!UICONTROL 合成]** 选项卡。 您可以使用列表中的省略号按钮随时复制或删除现有合成。

合成可以具有多种状态：

* **[!UICONTROL 草稿]**：构成正在进行中，尚未发布。
* **[!UICONTROL 已发布]**：构成已发布，生成的受众已保存并可供使用。

![](assets/audiences-compositions.png)

>[!NOTE]
>
>受众合成当前未与沙盒重置功能集成。 在启动沙盒重置之前，您需要手动删除合成，以确保正确清理关联的受众数据。 Adobe Experience Platform中提供了详细信息 [沙盒文档](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html#delete-audience-compositions)
