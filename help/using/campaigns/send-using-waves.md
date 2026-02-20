---
solution: Journey Optimizer
product: journey optimizer
title: 按波次发送
description: 计划在一段时间内以受控批次投放的出站营销活动消息。 波次发送支持可投放性并帮助维护发件人信誉。
feature: Campaigns
topic: Campaign scheduling
role: User
level: Intermediate
keywords: 批次，批次，计划，促销活动，历程，可投放性
source-git-commit: 6c509ef134c4240b243d255fd1ab7ec6bb062bf0
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 1%

---

# 使用营销活动中的批次发送 {#send-using-waves}

您可以将出站营销活动消息的投放分为多个批次（批次），并计划它们随时间的变化。 Wave发送有助于平衡负载，避免压倒性的下游系统（如呼叫中心或登陆页面），并支持可投放性和发件人信誉 — 尤其是对于高容量发送。

<!--
>[!CAUTION]
>
>Wave sending applies to **outbound** actions only (Email, SMS, Push, Direct mail).-->

Journey Optimizer允许您定义批次的数量、大小（以受众百分比或绝对数字表示）以及每个批次的运行时间。

## 限制和防护 {#limitations-guardrails}

* 波动发送仅适用于&#x200B;**出站**&#x200B;操作（电子邮件、短信、推送、直邮）。
* 您必须至少定义&#x200B;**2波**，并且最多可添加&#x200B;**10波**。
* 两个批次开始的最小间隔为&#x200B;**30分钟**。
* 波次开始不能早于营销活动开始或过去。

## 配置波次发送 {#configure-wave-sending}

要配置在营销策划中发送批次的方式和时间，请执行以下步骤。

1. 创建或打开包含出站操作（例如，电子邮件、短信、推送）的[操作营销活动](create-campaign.md)。

1. 在营销活动的&#x200B;**[!UICONTROL 计划]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL 分批次投放营销活动操作]**。

   ![](assets/campaign-wave-option.png){width="100%"}

   >[!NOTE]
   >
   >只有在营销活动的&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡中选择了叫客操作时，才会显示&#x200B;**[!UICONTROL 以批次交付营销活动操作]**&#x200B;选项。 [了解详情](campaign-action.md)

1. 设置要发送的批次数（例如，4）。

   >[!NOTE]
   >
   >您必须至少定义2个波段，并且最多可添加10个波段。

1. 选择如何定义波次大小和时间，如下所述。

### 相等波段 {#equal-waves}

默认情况下，受众会拆分为大小相等的批次。 安排第一波次的时间，并设置每个波次开始之间的固定间隔（例如，2小时）。

![](assets/campaign-equal-waves.png){width="80%"}

>[!NOTE]
>
>两个批次开始的最小间隔为&#x200B;**30分钟**。

然后，系统自动安排后续波次（例如，第一个波次在早上9:00，第二个波次在晚上11:00，第三个波次在晚上1:00，第四个波次在晚上3:00）。

### 自定义分发 {#custom-distribution}

选择&#x200B;**[!UICONTROL 自定义分布]**&#x200B;选项，将每个波次的大小定义为总受众的百分比（例如，15%、20%、25%、40%）。

![](assets/campaign-wave-percentage.png){width="80%"}

>[!NOTE]
>
>所有批次的总和必须等于100%。 如果不是这种情况，则会显示警告消息。<!--are the waves actually sent or does the system prevent user from saving the campaign?-->

选择&#x200B;**[!UICONTROL 数字]**&#x200B;可将每个波次的大小定义为配置文件的绝对数（例如，10,000；50,000）。

![](assets/campaign-wave-numbers.png){width="80%"}

>[!NOTE]
>
>在使用数字时，系统不会验证总和是否覆盖整个受众，您必须确保波次大小涵盖要发送到的受众。 请参阅[常见问题解答](#faq)以了解详情。

### 自定义计划 {#custom-schedule}

选择&#x200B;**[!UICONTROL 计划每个波次]**&#x200B;以定义每个波次的特定开始日期和时间。 批次不需要均匀隔开（例如，上午9:00，上午11:00，下午5:00，晚上8:30）。

![](assets/campaign-wave-custom-schedule.png){width="80%"}

>[!NOTE]
>
>两个批次开始的最小间隔为&#x200B;**30分钟**。

## 用例 {#use-cases}

Wave发送可帮助您控制发送消息的时间和数量，这可以提高可投放性，保护发件人信誉，并使发送与您的运营容量相匹配。 考虑在以下情况下使用波段：

* **呼叫中心或响应管理：**&#x200B;限制每天或每小时传出多少条消息，以便下游团队（例如，客户关怀团队）可以处理响应。 例如，每天发送20条消息以匹配呼叫中心容量。

  ![](assets/campaign-waves-ex-call-center.png){width="75%"}

* **高容量和可投放性：**&#x200B;避免一次发送一个非常大的营销活动。 随时间分散投放，以帮助维护发件人的信誉并降低被标记为垃圾邮件的风险。

  ![](assets/campaign-waves-ex-high-volume.png){width="75%"}

* **提升：**&#x200B;使用新平台或IP时，逐步增加容量（例如，第一波为10%，然后为15%、20%，以此类推）以逐步建立声誉。

  ![](assets/campaign-waves-ex-ramp-up.png){width="75%"}

## 常见问题 {#faq}

+++ 如果波浪大小的总和不等于总受众会发生什么？

* 如果您的波次大小之和&#x200B;**超过**&#x200B;个受众（例如，您计划在第一波次为100,000个受众发送100,000个受众），则第一波次将发送给所有受众，而其余波次将没有任何人可发送至 — 这些波次将不会执行。
* 如果总和&#x200B;**小于受众**（例如，您为100,000的受众定义了四个批次共40,000个配置文件），则只有这些批次中包含的用户档案将收到消息。 其他受众将不会收到该通信，并且以后将不会重试。

+++

+++ 我是否可以为各个批次分配不同的区段或标准？

您只能定义波的大小和时间。 整个营销活动的收件人选择是相同的；您不能向单个批次分配不同的区段或标准。

+++

## 后续步骤 {#next}

* [计划活动操作](campaign-schedule.md) — 设置开始日期、结束日期、频率和速率控制。
* [查看并激活营销活动](review-activate-campaign.md) — 检查该营销活动并上线。
