---
solution: Journey Optimizer
product: journey optimizer
title: 使用“构建受众”活动
description: 了解如何在精心策划的市场活动中使用“构建受众”活动
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 45%

---

# 构建受众 {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="构建受众活动"
>abstract="**构建受众**&#x200B;活动允许您定义将进入精心策划的市场活动的受众。 在精心策划的市场活动上下文中发送消息时，消息受众不在渠道活动中定义，而是在&#x200B;**构建受众**&#x200B;活动中定义。"

**生成受众**&#x200B;活动是一个&#x200B;**定位**&#x200B;活动。此活动允许您定义将输入经过协调的市场活动的受众。 在精心策划的市场活动上下文中发送消息时，消息受众不在渠道活动中定义，而是在&#x200B;**构建受众**&#x200B;活动中定义。

要定义受众群体，您可以：

* 选择 Adobe Experience Platform 受众。
* 通过定义和组合筛选条件，使用查询建模器构建新的受众。

>[!NOTE]
>
>使用“构建访问群体”活动无法定位从文件加载的访问群体。 为此，您需要先使用&#x200B;**加载文件**&#x200B;活动，然后再使用&#x200B;**协调**&#x200B;活动。

<!--
The **Build audience** activity can be placed at the beginning of the workflow or after any other activity. Any activity can be placed after the **Build audience**.
-->

## 配置构建受众活动 {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="受众"
>abstract="选择您的受众，就像设计新投放时使用受众一样。"

请按照以下步骤配置&#x200B;**生成受众**&#x200B;活动：

![](../assets/workflow-audience.png)

1. 添加一个&#x200B;**生成受众**&#x200B;活动。
1. 定义一个标签。
1. 定义受众类型：**创建您自己的**&#x200B;或&#x200B;**读取受众**。
1. 按照以下选项卡中详述的步骤配置受众。

>[!BEGINTABS]

>[!TAB 创建您自己的（查询）]

要创建您自己的查询，请执行以下步骤：

1. 选择&#x200B;**创建您自己的（查询）**。
1. 选择&#x200B;**定位维度**。通过定位维度，可定义操作面向的群体：收件人、合同受益人、操作人员、订阅者等。默认情况下从收件人中选择目标。
1. 单击&#x200B;**继续**。
1. 使用查询建模器定义查询，方法与设计新电子邮件时创建受众的方式相同。

>[!TAB 读取受众]

要选择现有受众，请执行以下步骤：

1. 选择&#x200B;**读取受众**。
1. 单击&#x200B;**继续**。
1. 选择您的受众，就像设计新投放时使用受众一样。

>[!ENDTABS]

## 示例{#build-audience-examples}

以下是包含两个&#x200B;**构建受众**&#x200B;活动的精心策划的营销活动示例。 第一个示例针对扑克玩家受众，然后是电子邮件投放。第二个示例针对 VIP 客户受众，然后是短信投放。

![](../assets/workflow-audience-example.png)
