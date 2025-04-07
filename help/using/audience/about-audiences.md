---
solution: Journey Optimizer
product: journey optimizer
title: 关于 Adobe Experience Platform 受众
description: 了解如何使用 Adobe Experience Platform 受众
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 19%

---


# 受众入门 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="受众"
>abstract="通过利用 Real-Time Customer Profile 数据，Adobe Experience Platform 让您能够轻松地构建区段定义，从而创建目标受众，用于捕捉客户的独特行为和偏好。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="选择营销活动受众"
>abstract="此列表显示所有可用的 Adobe Experience Platform 受众。选择营销活动的目标受众。营销活动中配置的消息将发送到属于所选受众的所有个人。[了解有关受众的详细信息](../audience/about-audiences.md)"

受众是指具有相似行为和/或特征的人群。 它们使用Adobe Experience Platform Segmentation Service在Adobe Experience Platform上集中配置和维护，并可在Journey Optimizer中轻松访问，以便在您的旅程和营销活动中激活。

Adobe Journey Optimizer提供了强大的工具来创建、管理和丰富受众，从而加强营销工作。 在与Adobe Real-Time Customer Data Platform结合使用时，Journey Optimizer可让您栈叠受众以实现更复杂的分段，并与其他Adobe Experience Cloud解决方案双向共享受众。

实时数据流或批量上传时，数据集更新和Journey Optimizer会实时动态地将个人移入和移出受众和历程。

>[!BEGINSHADEBOX]

本文档提供了有关如何使用[!DNL Adobe Journey Optimizer]中的受众的信息。 有关Audience Portal和受众的详细信息，请参阅Adobe Experience Platform分段服务文档。 有关更多详细信息，请参阅以下部分：

* [分段服务UI指南](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/overview){target="_blank"}

* [分段服务 — 常见问题解答](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/faq){target="_blank"}

>[!ENDSHADEBOX]

## 浏览受众 {#browse}

可通过&#x200B;**[!UICONTROL 客户]** > **[!UICONTROL 受众]**&#x200B;菜单访问受众。

仪表板以可视化形式显示重要受众之间的重叠，并支持探索有价值的受众趋势，例如给定时间段内的受众规模变化或受众突然激增，可突出显示导致受众萎缩的事件或操作，以及导致受众增长的事件或操作，例如成功选件。

![](assets/audiences-overview.png)

从Audience Portal，您可以通过标准标签、治理控件、可搜索文件夹和标记轻松管理、查找和浏览受众。

有关如何在Audience Portal中使用受众的更多信息，请参阅[Adobe Experience Platform分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hans){target="_blank"}。

## 受众类型 {#types}

可以使用不同方法生成受众：

* **区段定义**：使用Adobe Experience Platform分段服务创建新的受众定义。 受众从区段定义生成，并根据其评估类型在不同的时间刷新。

   * 流式分段：随着新数据流入实时更新受众，确保基于用户活动的持续相关性。
   * 批量分段：受众每24小时刷新一次，以固定间隔捕获用户档案快照。
   * Edge分段：在边缘即时评估受众，以实现实时个性化。

[了解如何生成区段定义](creating-a-segment-definition.md)

* **自定义上传**：使用CSV文件导入受众。 [了解如何创建自定义上传受众](custom-upload.md)

* **受众组合**：创建组合工作流以将现有受众组合到可视画布中，并应用排名、拆分、加入等操作来创建新受众。 [了解如何使用受众组合](get-started-audience-orchestration.md)

* **联合受众构成**：直接从现有数据仓库联合数据集，以在一个系统中构建和扩充Adobe Experience Platform受众和属性。 [了解如何使用联合受众合成](federated-audience-composition.md)。

## 操作方法视频 {#video}

了解 Journey Optimizer 中统一的客户轮廓和受众。

>[!VIDEO](https://video.tv.adobe.com/v/3432671?quality=12)
