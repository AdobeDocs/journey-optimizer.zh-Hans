---
solution: Journey Optimizer
product: journey optimizer
title: 开始使用 IP 预热计划
description: 了解如何实施 IP 预热计划
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP，可投放性
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
source-git-commit: 5e0d683bf52df4992773c6147b9e418241777e5d
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 73%

---

# 开始使用 IP 预热计划 {#ip-warmup-gs}

使用[!DNL Journey Optimizer]，您可以按照最佳可投放性最佳实践，以标准化且高效的方式直接从用户界面执行IP预热工作流。 使用新平台发送电子邮件时，互联网服务提供商 (ISP) 会怀疑无法识别的 IP 地址。如果突然发送大量电子邮件，ISP 通常会将其标记为垃圾邮件。

要避免被标记为垃圾邮件，您可以使用 IP 预热计划功能逐步增加发送量。此新选项位于&#x200B;**[!UICONTROL 管理]**&#x200B;菜单，允许您以统一的方式更轻松地执行此操作，而不是创建复杂的每日历程。

➡️[在此视频中了解如何创建和执行IP预热计划](#video)

>[!AVAILABILITY]
>
>只能在生产类型的沙盒上启用此功能。

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

## 操作方法视频 {#video}

了解如何创建和执行 IP 预热计划。

>[!VIDEO](https://video.tv.adobe.com/v/3432637/?learn=on)

>[!NOTE]
>
>在[可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=zh-Hans)中了解有关利用IP预热提高电子邮件信誉的更多信息。
