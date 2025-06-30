---
title: 在Decisioning中使用上下文数据
description: 了解如何在Decisioning中使用上下文数据
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: ddc4b681-020b-4433-b4b3-3791c41907c9
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# 在Decisioning中使用上下文数据 {#context}

使用Decisioning，您可以利用Adobe Experience Platform中提供的任何信息来执行各种操作，例如创建[决策规则](rules.md)或[排名公式](ranking/ranking.md)。

例如，您可以设计一个决策规则，要求在发出决策请求时当前天气为≥80度。

>[!NOTE]
>
>上下文数据是在Adobe Experience Platform中定义的，在发出决策请求时发送。 它不包括历史数据。

要使用上下文数据，您首先需要定义要在Decisioning中可用的数据。 完成后，此数据将无缝集成到创建决策规则时可用的&#x200B;**[!UICONTROL 上下文数据]**&#x200B;选项卡中的决策。 您还可以在编辑排名公式时利用数据。

![](assets/decision-rules-context.png)

使用Adobe Experience Platform数据为Decisioning提供信息的步骤如下：

1. 在Adobe Experience Platform及其关联的&#x200B;**数据集**&#x200B;中创建一个&#x200B;**体验事件架构**。 [了解如何创建架构](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. 创建新的Adobe Experience Platform数据流：

   1. 导航到&#x200B;**[!UICONTROL 数据流]**&#x200B;菜单并选择&#x200B;**[!UICONTROL 新建数据流]**。

   1. 在&#x200B;**[!UICONTROL 事件架构]**&#x200B;下拉列表中，选择之前创建的Experience Event架构，然后单击&#x200B;**[!UICONTROL 保存]**。

      ![](assets/decision-rule-context-datastream.png)

   1. 单击&#x200B;**[!UICONTROL 添加服务]**&#x200B;并选择“Adobe Experience Platform”作为服务。 在&#x200B;**[!UICONTROL 事件数据集]**&#x200B;下拉列表中，选择之前创建的事件数据集并启用&#x200B;**[!UICONTROL Adobe Journey Optimizer]**&#x200B;选项。

      ![](assets/decision-rules-context-datastream-service.png)

数据流保存后，所选数据集的信息将自动获取并集成到Decisioning中，通常在大约24小时内变为可用。

有关如何使用Adobe Experience Platform的进一步指导，请探索以下资源：

* [体验数据模型(XDM)架构](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [数据集](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [数据流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview){target="_blank"}
