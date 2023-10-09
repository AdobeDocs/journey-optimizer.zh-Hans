---
solution: Journey Optimizer
product: journey optimizer
title: 开始使用 IP 预热计划
description: 了解如何实施 IP 预热计划
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP，可投放性
hide: true
hidefromtoc: true
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 100%

---

# 开始使用 IP 预热计划 {#ip-warmup-gs}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* **[开始使用 IP 预热](ip-warmup-gs.md)**
* [创建 IP 预热营销活动](ip-warmup-campaign.md)
* [创建 IP 预热计划](ip-warmup-plan.md)
* [执行 IP 预热计划](ip-warmup-execution.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>IP 预热功能目前仅作为 Beta 版供部分用户使用。要加入 Beta 版计划，请联系 Adobe 客户关怀团队。

借助 [!DNL Journey Optimizer]，您可以直接在用户界面中以标准化的高效方式轻松执行 IP 预热工作流程，并遵循最佳实践以实现卓越的可投放性。

>[!CAUTION]
>
>此功能仅适用于电子邮件渠道。

使用新平台发送电子邮件时，互联网服务提供商 (ISP) 会怀疑无法识别的 IP 地址。如果突然发送大量电子邮件，ISP 通常会将其标记为垃圾邮件。

要避免被标记为垃圾邮件，您可以使用 IP 预热计划功能逐步增加发送量。此新选项位于&#x200B;**[!UICONTROL 管理]**&#x200B;菜单，允许您以统一的方式更轻松地执行此操作，而不是创建复杂的每日历程。这应该可以确保启动阶段的顺利进行，并帮助您降低无效地址的总体占比。

>[!NOTE]
>
>在[可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=zh-Hans)中了解更多有关利用 IP 预热提高电子邮件声誉的信息。

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

实施 IP 预热计划的关键步骤如下：

1. 您首先需要在启用 IP 预热选项的情况下创建一个或多个营销活动。[了解详情](ip-warmup-campaign.md)

1. 在 [!DNL Journey Optimizer] 中创建 IP 预热计划，并上传在可投放性顾问的帮助下准备的 Excel 工作表。[了解详情](ip-warmup-plan.md)

1. 为计划的每个阶段选择一个营销活动并相应地激活运行。[了解详情](ip-warmup-execution.md)
