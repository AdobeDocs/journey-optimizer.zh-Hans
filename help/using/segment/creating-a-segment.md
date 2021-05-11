---
title: 构建细分
description: 了解如何构建细分
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 5%

---

# 生成区段 {#build-segments}

![](../assets/do-not-localize/badge.png)

在此示例中，我们将构建一个细分，以目标居住在亚特兰大、旧金山或西雅图的1980年后出生的所有客户。 所有这些客户应在过去7天内打开Luma应用程序，然后在打开应用程序后2小时内进行购买。

1. 访问&#x200B;**[!UICONTROL Segments]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL Create segment]**&#x200B;按钮。

   ![](../assets/create-segment.png)

   区段定义屏幕允许您配置所有必填字段以定义区段。 了解如何在[分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html)中配置区段。

   ![](../assets/segment-builder.png)

1. 在&#x200B;**[!UICONTROL Segment properties]**&#x200B;窗格中，为区段提供名称和说明（可选）。

   ![](../assets/segment-properties.png)

1. 将所需字段从左侧窗格拖放到中心工作区，然后根据需要配置这些字段。

   >[!NOTE]
   >
   >请注意，左窗格中的可用字段会因组织的&#x200B;**XDM单个用户档案**&#x200B;和&#x200B;**XDM ExperienceEvent**&#x200B;模式的配置方式而异。  请阅读[体验数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans)了解更多信息。

   ![](../assets/drag-fields.png)

   在此示例中，我们需要依赖&#x200B;**Attributes**&#x200B;和&#x200B;**事件**&#x200B;字段来构建区段：

   * **属性**:住在亚特兰大，旧金山或西雅图的用户档案,1980年后出生，
   * **事件**:在过去7天内打开Luma应用程序的用户档案，在打开应用程序后2小时内完成购买。

      ![](../assets/add-attributes.png)

      ![](../assets/add-events.png)

1. 当您在工作区中添加和配置新字段时，**[!UICONTROL Segment Properties]**&#x200B;窗格会自动更新，显示属于该区段的估计用户档案的相关信息。

   ![](../assets/segment-estimate.png)

1. 区段准备就绪后，单击&#x200B;**[!UICONTROL Save]**。 它以Adobe Experience Platform区段的列表显示。 请注意，搜索栏可帮助您在列表中搜索特定区段。

现在，该区段可用于您的旅程。 如需详细信息，请参阅[此部分](../segment/about-segments.md)。
