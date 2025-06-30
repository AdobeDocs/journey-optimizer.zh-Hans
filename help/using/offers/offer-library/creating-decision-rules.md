---
title: 创建决策规则
description: 了解如何创建决策规则以定义可向谁显示优惠
badge: label="旧版" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 7%

---

# 创建决策规则 {#create-decision-rules}

## 关于决策规则 {#about}

您可以根据Adobe Experience Platform中的可用数据创建优惠决策规则。 决策规则确定可向谁显示优惠。

例如，您可以指定当（性别=“女性”）和（地区=“东北”）时仅显示“女士冬装选件”。

➡️ [通过观看视频了解此功能](#video)

以下是使用决策规则时要注意的限制列表：

* Edge决策使用的边缘配置文件不会存储事件，因此边缘决策中使用的任何规则都将无效。
* 创建决策规则时，不支持回顾以前的时间段。 例如，如果您将上个月之内发生的体验事件指定为规则的组件。 在规则创建期间任何包含回顾期的尝试将在保存时触发错误。
  <!--* Decision requests that use the hub profile will look at the last 100 experience events on the profile to evaluate rules that reference historical experience events.-->

## 创建决策规则 {#create}

可在&#x200B;**[!UICONTROL 组件]**&#x200B;菜单中访问已创建的决策规则列表。

![](../assets/decision_rules_list.png)

要创建决策规则，请执行以下步骤：

1. 转到&#x200B;**[!UICONTROL 规则]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL 创建规则]**。

   ![](../assets/offers_decision_rule_creation.png)

1. 命名规则并提供说明，然后根据需要配置规则。

   为此，可使用Adobe Experience Platform **区段生成器**&#x200B;帮助您生成规则的条件。 [了解如何生成区段定义](../../audience/creating-a-segment-definition.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >与&#x200B;**[!UICONTROL 分段]**&#x200B;服务中使用的区段生成器相比，为创建决策规则而提供的区段生成器存在一些特殊性。 但是，[区段生成器](../../audience/creating-a-segment-definition.md)文档中描述的全局进程对于生成优惠决策规则仍然有效。 请参阅 [Adobe Experience Platform 分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=zh-Hans)以了解详情。

1. 在工作区中添加和配置新字段时，**[!UICONTROL 受众属性]**&#x200B;窗格显示有关属于受众的估计配置文件的信息。 单击&#x200B;**[!UICONTROL 刷新估算]**&#x200B;以更新数据。

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >当规则参数包含不在配置文件中的数据（如上下文数据）时，配置文件估计不可用。 例如，资格规则要求当前天气为≥80度。

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;确认。

1. 创建规则后，该规则将显示在&#x200B;**[!UICONTROL 规则]**&#x200B;列表中。 您可以选择它以显示其属性，并对其进行编辑或删除。

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>[!DNL Journey Optimizer]当前不支持基于事件的优惠。 如果您创建基于[事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=zh-Hans#events){target="_blank"}的决策规则，则无法在优惠中利用它。

## 教程视频 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/341363?quality=12&captions=chi_hans)
