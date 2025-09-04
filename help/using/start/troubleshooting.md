---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer疑难解答
description: Journey Optimizer疑难解答问题
feature: Get Started
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 3ab8957d0aec6f30853de5537e03f0e7bec2017c
workflow-type: tm+mt
source-wordcount: '1663'
ht-degree: 2%

---

# 故障排除 {#ajo-troubleshooting}


以下是Adobe Journey Optimizer的故障诊断文章列表。 每个故障排除部分都提供常见问题的解答和问题的解决方案。

另请参阅[Adobe Experience Platform常见问题解答和疑难解答文档](https://experienceleague.adobe.com/en/docs/experience-platform/landing/troubleshooting#service-troubleshooting-directory){target="_blank"}。

## 电子邮件渠道 {#ajo-troubleshooting-email}

### 电子邮件设计 {#ajo-troubleshooting-design}

+++ 如何防止在Adobe Journey Optimizer中使用主题时出现电子邮件格式问题？

在Adobe Journey Optimizer (AJO)中，修改电子邮件标头中的默认CSS块可能会导致意外的格式问题，尤其是在删除内容片段之后。 这些问题在移动设备上更加明显，并且可能会导致布局偏移或样式不一致。 要防止出现这种情况，请使用“主题”功能安全地应用自定义CSS，而无需更改系统生成的CSS样式。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"}，了解如何解决此问题。

在此页面[上了解有关电子邮件格式](../email/get-started-email-design.md)的更多信息。

+++


+++ 为什么具有可编辑字段的片段无法正常工作？

在Adobe Journey Optimizer中，包含可编辑字段的片段在添加到模板时可能无法正确加载或意外重复。 该问题通常会影响环境之间的特定片段。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"}，了解如何解决此问题。

在此页面[上了解有关可自定义片段](../content-management/customizable-fragments.md)的更多信息。

+++

+++ 为什么电子邮件模板和内容会从未发布的历程中消失？

在未发布的历程中编辑电子邮件模板时，某些电子邮件的内容和模板可能会意外消失。 这可能会导致返工和延迟。 为了降低此问题的风险，请避免同时进行编辑，限制打开选项卡的数量，并经常保存更改。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}，了解如何解决此问题。

在此页面[上了解有关模板](../email/use-email-templates.md)的更多信息。

+++

+++ 配置文件能否在Adobe Journey Optimizer中有多个推送令牌？

在Journey Optimizer中实施推送通知时，单个配置文件实际上可以具有多个与不同设备关联的推送令牌。 在推送通知营销活动期间，Journey Optimizer旨在管理这些令牌，并确保可以在所有关联设备上访问目标用户档案。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}，了解有关推送令牌管理的更多信息。

在此页面[上了解有关推送配置](../push/push-configuration.md)的更多信息。

+++

### 电子邮件跟踪和报告 {#ajo-troubleshooting-tracking}

+++ 如何防止报告中缺少电子邮件跟踪链接？

当电子邮件URL使用动态变量并且不以http开头时，或者当逻辑语句放置在URL字段中时，会出现Adobe Journey Optimizer中缺少链接跟踪的情况。 要解决此问题，请确保所有URL都以http开头，避免使用URL字段中的逻辑，并将复杂的个性化逻辑移动到HTML内容或预处理属性。


请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"}，了解如何解决此问题。

在此页面[上了解有关电子邮件跟踪](../email/message-tracking.md)的更多信息。

+++

### 电子邮件发送 {#ajo-troubleshooting-sending}

+++ 在设置API触发的事务性电子邮件营销活动时，如何解决邮件交换器错误？ 

如果您在Adobe Journey Optimizer中为API触发的事务性电子邮件促销活动创建渠道配置时遇到邮件交换器(MX)错误，可能是因为&#x200B;**DNS配置错误**&#x200B;或&#x200B;**DMARC策略限制**。 要解决此问题，请确保您的DNS配置正确，并验证您的域是否符合&#x200B;**基于域的消息身份验证、报告和符合性(DMARC)**&#x200B;要求。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26200){target="_blank"}，了解如何解决此问题。

在此页面[上了解有关电子邮件DMARC策略](../configuration/dmarc-record-update.md)的更多信息。

另请参阅[API触发的营销活动文档](../campaigns/api-triggered-campaigns.md)。
+++

## 推送渠道 {#ajo-troubleshooting-push}

+++ 配置文件能否在Adobe Journey Optimizer中有多个推送令牌？

在Journey Optimizer中实施推送通知时，单个配置文件实际上可以具有多个与不同设备关联的推送令牌。 在推送通知营销活动期间，Journey Optimizer旨在管理这些令牌，并确保可以在所有关联设备上访问目标用户档案。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}，了解有关推送令牌管理的更多信息。

在此页面[上了解有关推送配置](../push/push-configuration.md)的更多信息。

+++

+++ 为何单击推送消息不会将我重定向到配置的Web URL？  

如果推送消息未重定向到预期的Web URL，可能是由于点击操作配置不正确或禁用了推送通知设置所致。 请确保正确设置了推送消息的&#x200B;**点击操作**，并且启用了推送通知的&#x200B;**自动显示和跟踪**&#x200B;以解决此问题。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26226){target="_blank"}，了解有关此问题的更多信息。

在此页面[上了解有关推送配置](../push/push-configuration.md)的更多信息。

+++


## 短信渠道 {#ajo-troubleshooting-sms}

+++ 即使同意设置为`marketing.sms.value=y`，为什么我的事务性短信仍未投放？

如果收件人对SMS响应&#x200B;**STOP**，则将阻止来自该短号码的所有未来消息，包括事务性消息。 为确保事务性短信的投放不会中断，请配置并通过之前未选择退出的&#x200B;**单独短号码**&#x200B;发送事务性短信。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26258){target="_blank"}，了解有关此问题的更多信息。

在此页面[上了解有关短信选择退出配置](../sms/sms-opt-out.md)的更多信息。

+++


## 数据管理 {#ajo-troubleshooting-data-management}

+++ 当您创建新的沙盒时，生存时间(TTL)设置如何应用于配置文件和数据湖数据集？

在Adobe Journey Optimizer中配置新沙盒的组织提出了生存时间(TTL)设置如何应用于配置文件和数据湖数据集的疑问。 本文阐明TTL设置不会影响现有沙盒，并且仅自动应用于新配置的沙盒。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"}，了解如何处理TTL。

在此页面[上了解有关数据集生存时间](../data/datasets-ttl.md)的更多信息。

+++


## 用户档案和受众管理 {#ajo-troubleshooting-audiences}

+++ 如何解决受众计数差异？

Adobe Journey Optimizer的&#x200B;**读取受众**&#x200B;功能中已处理的条目数可能低于预期的受众数。 此问题通常因命名空间配置不正确而出现，从而导致配置文件被排除在历程之外。 解决办法包括检查和更正命名空间配置、审查相关文档以及调整优先级以确保Adobe Journey Optimizer中的操作更顺畅。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"}，了解如何解决此问题。

另请参阅[这篇关于过时的受众计数的文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26166){target="_blank"}。

在此页面&#x200B;**上了解历程**&#x200B;中的[读取受众](../building-journeys/read-audience.md)活动的更多信息。

+++

+++ 为何配置文件更新失败？

在Adobe Journey Optimizer中，通过历程中的&#x200B;**更新配置文件**&#x200B;活动运行后，某些字段值可能无法正确更新。 在某些情况下，更新的字段可能会消失或恢复到其以前的状态。 要解决此问题，请检查冲突规则或条件，审查权限设置，为&#x200B;**更新配置文件**&#x200B;活动使用唯一的数据集，并确保没有其他摄取进程同时写入同一配置文件。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"}，了解解决此问题的步骤。

在此页面&#x200B;**上了解历程**&#x200B;中[更新配置文件](../building-journeys/update-profiles.md)活动的详细信息。

另请参阅有关数据摄取[的](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/tutorials/ingest-batch-data?lang=en#dataset-activity){target="_blank"}Adobe Experience Platform文档。

+++

+++ 为什么进入历程的配置文件计数与相关受众中的配置文件计数不匹配？

如果在执行历程时当天快照不可用，则当历程使用前一天的配置文件快照时，可能会出现差异。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26253){target="_blank"}，了解解决此问题的步骤。

请参阅[此Journey Optimizer社区帖子](https://experienceleaguecommunities.adobe.com/t5/real-time-customer-data-platform/profile-snapshot-and-segment-qualification-troubleshooting/ba-p/698998){target="_blank"}以了解详情。

另请参阅[Adobe Experience Platform计划API文档](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/api/schedules?lang=en){target="_blank"}以检查每日作业的计划时间。

+++


+++ 如何解决受众群体问题？

如果组件或资源缺失（通常是由于授权、配置或权限配置错误所致），可能会出现受众填充问题。 要解决这些问题，首先要验证权限，确保正确配置，然后检查权限。 如果问题仍然存在，请升级案例并与支持团队协调以获得完整的解决方案。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26333){target="_blank"}，了解解决此问题的步骤。

在此页面&#x200B;**上了解历程**&#x200B;中[更新配置文件](../building-journeys/update-profiles.md)活动的详细信息。

另请参阅[Adobe Real-Time CDP配置文件文档](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide?lang=en#profile-detail){target="_blank"}。

+++

+++ 如何解决Adobe Journey Optimizer中受众发生更改后的旅程触发问题？ 

如果旅程在修改其关联受众（例如更改合并策略）后停止触发，则可能会遇到营销活动流中断的情况。 要解决此问题，请&#x200B;**使用更新的受众设置复制并重新发布历程**，以确保触发器正常工作。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"}，了解解决此问题的步骤。

在此页面[上了解如何复制历程](../building-journeys/journey-ui.md#duplicate-a-journey)。

+++


## 历程

### 活动

+++ 为什么我的事件没有触发预期历程？  

事件可能无法触发历程，即使符合通过查询服务&#x200B;**创建的**&#x200B;所有条件，而不是流式传输到&#x200B;**数据收集核心服务(DCCS)**&#x200B;时。 要解决此问题，请查看事件配置，确保事件直接流式传输到DCCS **，并使用**&#x200B;测试模式&#x200B;**验证功能。**

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"}，了解解决此问题的步骤。

在此页面[上了解有关事件](../event/about-events.md)的更多信息。

另请参阅[历程事件护栏](../start/guardrails.md#events)。

+++

## 决策 {#ajo-troubleshooting-decisioning}

+++ 如何解决创建优惠收藏集时出现的问题？

如果没有为您的组织配置&#x200B;**目录**，则创建优惠收藏集通常会遇到困难。 要解决此问题，请在尝试创建优惠收藏集之前，验证所有必需的目录是否已正确配置。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"}，了解解决此问题的步骤。

在此页面[上了解有关优惠收藏集](../offers/offer-library/creating-collections.md)的更多信息。

+++


## 多语言 {#ajo-troubleshooting-multilingual}

+++ 如何解决此问题`Message validation error (CJMMAS - 1069-500)`？

在Adobe Journey Optimizer中，链接到多语言功能的消息验证错误(CJMMAS - 1069-500)阻止将历程设置为测试模式或发布。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"}，了解解决此问题的步骤。

在此页面[上了解有关多语言内容](../content-management/multilingual-gs.md)的更多信息。

++


## 配置 {#ajo-troubleshooting-config}

### 安全性 {#ajo-troubleshooting-security}

+++ 如何为自定义操作启用TLS v1.3？  

要在连接到第三方系统时维护&#x200B;**数据完整性和安全性**，请确保为自定义操作启用了传输层安全性(**TLS**) v1.3。 这有助于保护通信并防止潜在的安全漏洞。


请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"}以了解详情。

在此页面[上了解有关多语言内容](../action/about-custom-action-configuration.md)的更多信息。

+++

### 仪表板 {#ajo-troubleshooting-dashboards}

+++ 为什么我无法直接从Adobe Journey Optimizer中的查询创建功能板？ 

在Adobe Journey Optimizer中，无法直接从查询创建功能板。 要构建仪表板，请使用Adobe Experience Platform中可用的&#x200B;**仪表板创建功能**，此功能允许您有效地可视化和分析查询数据。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"}以了解详情。

++