---
solution: Journey Optimizer
product: journey optimizer
title: IP预热可投放性指南
description: 了解IP预热的可投放性基础知识和最佳实践
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP 、可投放性、信誉、 ISP 、参与
exl-id: TBD
source-git-commit: b1b9b34aec305d6690d93e68238aed852ef689b7
workflow-type: tm+mt
source-wordcount: '1088'
ht-degree: 6%

---

# IP预热可投放性指南 {#ip-warmup-deliverability-guide}

在Adobe Journey Optimizer中启动具有新IP地址或域的电子邮件营销活动时，了解可投放性基础对于构建强大的发件人信誉至关重要。 本指南涵盖了关键概念、准备步骤和最佳实践，帮助您从零信誉成功放置收件箱。

➡️ [观看此视频以了解IP预热可投放性基础知识](#video)

>[!NOTE]
>
>有关在Adobe Journey Optimizer中实施IP预热计划的逐步说明，请参阅[开始使用IP预热计划](ip-warmup-gs.md)。

## 为什么IP和域信誉重要 {#reputation-matters}

邮箱提供商(Gmail、Yahoo、Microsoft、Apple Mail等)根据四个关键支柱评估每个发件人：

* **投诉**：收件人是否将您的邮件标记为垃圾邮件？
* **参与**：收件人是否打开、点击或回复电子邮件？
* **基础架构**：您的发送基础架构是否已验证、稳定且值得信赖？
* **内容**：您的邮件内容是否合法、有价值？

IP预热主要通过逐步向邮箱提供商证明您的新基础架构是合法的，而且您希望在扩展到完整发送量之前完成这一过程，从而解决前三大支柱。

## 预检核对清单 {#pre-flight-checklist}

在开始准备IP地址之前，请确保所有基本元素都已准备就绪。 下表概述了在开始IP预热计划之前需要完成的基本任务。

| 任务 | 为什么这很重要 | 如何完成 |
|------|----------------|-------------------|
| 在AJO中保留固定IP并委派子域 | 所有未来的信誉都附加到这些基础架构元素中 | 导航到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件设置]** > **[!UICONTROL 子域]**。 [了解详情](delegate-subdomain.md) |
| 配置SPF和DKIM | 确认您的发送服务器是合法的并且已授权 | 在子域委派和渠道配置创建后由Adobe自动处理。 [了解详情](delegate-subdomain.md) |
| 设置 DMARC 记录 | 启用电子邮件身份验证报告和未来实施策略 | 在子域委派和渠道配置创建后由Adobe自动处理。 [了解详情](dmarc-record.md) |
| 配置种子列表监测 | 在预热过程的早期检测到收件箱放置问题 | 在创建渠道配置时添加种子地址。 [了解详情](seed-lists.md) |
| 构建阶段1高参与受众 | 提升与最活跃收件人的早期参与量度 | 创建过去30天内打开或单击的受众少于5,000个联系人 |

>[!CAUTION]
>
>身份验证问题(SPF、DKIM、DMARC)无法通过卷斜坡解决。 在开始发送之前，请确保已正确配置这些服务器。

## 四周预热日历示例 {#warmup-calendar}

此示例日历提供了基于最终每日流量(UDV)百分比的渐进式流量增加。 调整这些数字以适合您的特定发送要求，并与您的可投放性顾问合作来创建自定义计划。

| Days | %的UDV | 目标受众 | 内容推荐 |
|------|----------|-----------------|------------------------|
| 1-3 | 0.5% | 您参与度最高的收件人 | 使用简短纯文本格式，在折上方加上一个清晰的call-to-action |
| 4-7 | 1% | 参与的用户以及最近的购买者 | 添加轻量级主页图像，将链接限制为3个或更少 |
| 8-14 | 5% | 更广泛的活动订阅者列表 | 引入您的标准电子邮件模板，但避免大量促销内容 |
| 15-21 | 25% | 活动订阅者和轻度不活动的订阅者 | 使用正常的营销内容，同时密切监控投诉率 |
| 22-28 | 50-100% | 完整列表（遵循禁止显示列表） | 过渡到稳态发送节奏 |

>[!NOTE]
>
>Adobe Journey Optimizer提供了一个专用的[IP预热计划功能](ip-warmup-gs.md)，它自动化了卷管理并简化了预热过程，而无需复杂的旅程配置。

## 使用AJO的IP预热计划功能 {#ajo-warmup-feature}

Adobe Journey Optimizer包括简化的IP预热计划功能，不再需要通过复杂的历程设置手动设置卷上限。 此功能可确保采用标准化方法来建立发件人信誉。

### 工作原理

1. **创建IP预热活动**：在启用&#x200B;**[!UICONTROL IP预热计划激活]**&#x200B;选项的情况下生成一个或多个活动。 [了解详情](ip-warmup-campaign.md)

1. **设置计划**：访问&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件设置]** > **[!UICONTROL IP预热计划]**，并上传与可投放性顾问一起准备的分阶段预热模板。 [了解详情](ip-warmup-plan.md)

1. **执行阶段**：为每个阶段选择一个营销活动并激活相应的运行。 系统会自动从以前的运行中排除用户档案，以防止过度联系。 [了解详情](ip-warmup-execution.md)

1. **监视和调整**：使用合并的报告仪表板跟踪进度、监视运行状态，并在出现问题时修改计划。 [了解详情](ip-warmup-execution.md#monitor-plan)

## 实时监控和关键量度 {#monitoring}

Adobe Journey Optimizer提供内置的报告功能以跟踪您的IP预热性能：

* **实时报告**：从&#x200B;**[!UICONTROL 最近24小时]**&#x200B;选项卡访问营销活动的实时测量和可视化图表。 [了解详情](../reports/live-report.md)

* **Customer Journey Analytics集成**：要获得更深入的见解，请利用Customer Journey Analytics分析来自Adobe Experience Platform的数据并创建自定义可视化图表。 [了解详情](../reports/report-gs-cja.md)

### 目标量度

在整个预热过程中监控以下关键绩效指标：

| 量度 | 目标阈值 | 超出时的操作 |
|--------|-----------------|-------------------|
| 投诉率 | ≤ 0.1% | 审核分段并抑制慢性投诉人 |
| 硬跳出率 | ≤ 2% | 审查列表质量和卫生习惯 |
| 打开率 | ≥ 10% | 验证您是否在定位参与的受众 |

>[!TIP]
>
>要获得全面的营销活动分析，请使用[营销活动实时报告](../reports/campaign-live-report.md#email-live)和[Customer Journey Analytics报告](../reports/campaign-global-report-cja-email.md)功能。

## 疑难解答行动手册 {#troubleshooting}

使用此决策矩阵解决预热期间的常见问题：

| 症状 | 可能的原因 | 建议的操作 |
|---------|--------------|-------------------|
| Yahoo临时失败（421错误） | 数量增长过快 | 暂停发送24小时，然后在上一层重新启动 |
| 种子帐户的打开率低于2% | IP 列入阻止列表 | 检查[Google Postmaster Tools](https://postmaster.google.com/)和[Microsoft SNDS](https://sendersupport.olc.protection.outlook.com/snds/)；如果需要，打开可投放性票证 |
| 投诉率超过0.3% | 受众定位错误或过时 | 审核区段定义并从[禁止显示列表](manage-suppression-list.md)中排除慢性投诉人 |

>[!IMPORTANT]
>
>最好是减慢热身速度，而不是稍后尝试修复损坏的发件人信誉。 始终优先考虑保持健康的量度，而不是大幅增加量。

## 预热后最佳实践 {#post-warmup}

完成预热计划并稳定指标后：

* **保持一致性**：将每日流量每周增加量保持在30%以下，以维护您的既有声誉

* **持续监控**：计划每季信誉运行状况检查，以主动识别和解决问题

* **遵守参与信号**：继续优先考虑参与的收件人，并为不活动的订阅者实施重新参与营销活动

* **保持身份验证最新**：定期验证您的SPF、DKIM和DMARC记录是否保持正确配置

## 主要要点 {#key-takeaways}

* **IP预热是必不可少的**：跳过预热过程比正确执行预热过程所需的工作花费更多的时间和声誉

* **数据驱动型决策**：每天跟踪投诉、跳出和参与率，并在ISP惩罚您之前调整您的策略

* **首先进行身份验证，其次是卷**：先解决所有SPF、DKIM和DMARC问题，然后再开始增加卷

* **一致性问题**：邮箱提供程序支持可预测的发送模式；避免突然的流量尖峰或不规则的发送计划

## 操作说明视频 {#video}

了解Adobe Journey Optimizer中的可投放性基础知识、信誉建立和IP预热最佳实践。

>[!VIDEO](https://video.tv.adobe.com/v/3463792/?captions=chi_hans&learn=on)

<!--
>[!NOTE]
>
>For more guidance, explore the [Adobe Journey Optimizer Deliverability Guide blog post](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950).-->

## 相关主题 {#related-topics}

* [开始使用 IP 预热计划](ip-warmup-gs.md)
* [创建 IP 预热营销活动](ip-warmup-campaign.md)
* [创建 IP 预热计划](ip-warmup-plan.md)
* [执行 IP 预热计划](ip-warmup-execution.md)
* [设置渠道配置](channel-surfaces.md)
* [委派子域](delegate-subdomain.md)
* [管理禁止列表](manage-suppression-list.md)
* [可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=zh-Hans)

