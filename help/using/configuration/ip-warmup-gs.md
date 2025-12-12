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
source-git-commit: 5dd6ebadd7b8c7490cb10496282697ce32ff3693
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 43%

---

# 开始使用 IP 预热计划 {#ip-warmup-gs}

使用[!DNL Journey Optimizer]，您可以按照最佳可投放性最佳实践，以标准化且高效的方式直接从用户界面执行IP预热工作流。 使用新平台发送电子邮件时，互联网服务提供商 (ISP) 会怀疑无法识别的 IP 地址。如果突然发送大量电子邮件，ISP 通常会将其标记为垃圾邮件。

要避免被标记为垃圾邮件，您可以使用 IP 预热计划功能逐步增加发送量。使用&#x200B;**[!UICONTROL 管理]**&#x200B;菜单中的这个新选项，您可以自动执行卷管理并简化预热过程，而无需复杂的历程配置。

>[!NOTE]
>
>在实施IP预热计划之前，请在此[IP预热可投放性指南](ip-warmup-deliverability-guide.md)中了解可投放性基础知识、信誉构建和最佳实践。

➡️ [在此视频中了解如何创建和执行IP预热计划](#video)

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

>[!VIDEO](https://video.tv.adobe.com/v/3453850/?captions=chi_hans&learn=on)

>[!NOTE]
>
>在[可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=zh-Hans)中了解有关利用IP预热提高电子邮件信誉的更多信息。

## 其他资源 {#additional-resources}

浏览这些有用博客帖子，获取有关IP预热的更深入指导：

* [Adobe Journey Optimizer可投放性指南：从零信誉到收件箱英雄](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950) — 涵盖信誉基础知识、预热日历、监控和故障排除最佳实践的综合指南。

* [了解如何设置IP预热设置](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warmup-understanding-how-to-set-up-the-ip-warmup/ba-p/761949) — 了解设置IP预热计划的基础知识和成功实施的最佳实践。

* [IP预热计划中的高级功能](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/advanced-features-in-ajo-ip-warm-up-plans-granular-controls-for/ba-p/761958) — 探索用于优化IP预热策略的高级功能和精细控制。

* [IP预热故障排除](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warm-up-troubleshooting-audience-delays-and-smart-retry/ba-p/761952) — 查找受众延迟等常见问题的解决方案，并了解智能重试机制。
