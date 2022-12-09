---
solution: Journey Optimizer
product: journey optimizer
title: 创建合成工作流
description: 了解如何创建合成工作流以合并和排列现有受众。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# 创建合成工作流 {#create-compositions}

利用合成工作流，可合并和排列现有受众以创建新受众。

## 创建合成工作流 {#create}

1. 访问 **[!UICONTROL Segments]** 菜单和选择 **[!UICONTROL Create Audience]**.

1. 选择 **[!UICONTROL Compose Audience]**.

   >[!NOTE]
   >
   >的 **[!UICONTROL Build rule]** 创建方法允许您使用 [Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

   ![](assets/audiences-create.png)

1. 此时将显示组合画布，其中包含两个默认活动：

   * **[!UICONTROL Audience]**:作品的起点。 此活动允许您选择一个或多个受众作为工作流的基础，

   * **[!UICONTROL Save]**:最后一步。 此活动用于将工作流的结果保存到新受众中。
   有关如何在合成工作流画布中配置活动的更多信息，请参阅 [使用合成画布](composition-canvas.md).

1. 打开合成属性以指定标题和描述。

   如果属性中未定义标题，则合成标签将作为开始 **[!UICONTROL Audience]** 活动。

   ![](assets/audiences-properties.png)

1. 通过在 **[!UICONTROL Audience]** 和 **[!UICONTROL Save]** 活动。 [了解如何使用合成画布](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. 准备好构图后，单击 **[!UICONTROL Publish]** 按钮来发布合成并将生成的受众保存到Adobe Experience Platform中。

   如果在发布过程中发生任何错误，则会显示警报，其中包含有关如何解决此问题的信息。

   ![](assets/audiences-alerts.png)

1. 合成已发布。 生成的受众会保存到Adobe Experience Platform中，并且可以在Journey Optimizer促销活动中进行定位。 [了解如何使用营销活动](../campaigns/get-started-with-campaigns.md)

## 接入组合物 {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="发布受众"
>abstract="发布您的构图，以将生成的受众保存到Adobe Experience Platform中。"

所有创建的合成都可以从 **[!UICONTROL Compositions]** 选项卡。 它们可以具有多种状态：

* **[!UICONTROL Draft]**:该组合正在进行中，尚未发布。
* **[!UICONTROL Published]**:合成已发布，生成的受众已保存并可供使用。
* **[!UICONTROL Archived]**:构图已存档。

![](assets/audiences-compositions.png)

>[!NOTE]
>
>您可以随时使用列表中的椭圆按钮复制或删除现有合成。

了解更多：

* [受众构成入门](get-started-audience-orchestration.md)
* [使用合成画布](composition-canvas.md)
* [访问和管理受众](access-audiences.md)
