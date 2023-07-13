---
solution: Journey Optimizer
product: journey optimizer
title: 生成区段定义
description: 了解如何通过区段定义创建受众
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 5%

---

# 生成区段定义 {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="创建规则"
>abstract="构建规则创建方法允许您使用Adobe Experience Platform受众服务创建新的受众定义。"

在此示例中，我们将构建受众以定位居住在亚特兰大、旧金山或西雅图且出生于1980年之后的所有客户。 所有这些客户都应在过去7天内打开Luma应用程序，然后在打开应用程序后的2小时内购买了该应用程序。

➡️ [在此视频中了解如何创建受众](#video-segment)

1. 访问 **[!UICONTROL 受众]** 菜单，然后单击 **[!UICONTROL 创建受众]** 按钮。

   ![](assets/create-segment.png)

   利用区段定义屏幕，可配置定义受众所需的所有字段。 了解如何在 [分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target="_blank"}.

   ![](assets/segment-builder.png)

1. 在 **[!UICONTROL 受众属性]** 窗格，为受众提供名称和描述（可选）。

   ![](assets/segment-properties.png)

1. 将所需字段从左窗格拖放到中心工作区，然后根据需要进行配置。

   >[!NOTE]
   >
   >请注意，左窗格中可用的字段因 **XDM个人资料** 和 **XDM ExperienceEvent** 已为您的组织配置架构。  了解详情，请参阅 [Experience Data Model (XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}.

   ![](assets/drag-fields.png)

   在此示例中，我们需要依靠 **属性** 和 **事件** 用于构建受众的字段：

   * **属性**：居住在1980年后亚特兰大、旧金山或西雅图的用户档案

     ![](assets/add-attributes.png)

   * **事件**：过去7天内打开了Luma应用程序，然后在打开应用程序后2小时内购买的用户档案。

     ![](assets/add-events.png)

1. 当您在工作区中添加和配置新字段时， **[!UICONTROL 受众属性]** 窗格会自动更新属于受众的估计用户档案的信息。

   ![](assets/segment-estimate.png)

1. 受众准备就绪后，单击 **[!UICONTROL 保存]**. 它显示在Adobe Experience Platform受众列表中。 请注意，搜索栏可帮助您搜索列表中的特定受众。

受众现在可以在您的历程中使用。 有关详细信息，请参阅[此部分](../audience/about-audiences.md)。

## 操作方法视频{#video-segment}

了解如何创建受众。

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
