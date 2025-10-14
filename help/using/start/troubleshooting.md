---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer疑难解答
description: Journey Optimizer疑难解答问题
feature: Get Started
role: User
level: Intermediate
exl-id: f8acb987-5c6e-4545-93b9-fdfc0d74db57
source-git-commit: f46cc01dce5ab0a30c1f0907b2a4684802b216be
workflow-type: tm+mt
source-wordcount: '2746'
ht-degree: 2%

---

# 故障排除 {#ajo-troubleshooting}

以下是Adobe Journey Optimizer的故障诊断文章列表。 每个故障排除部分都提供常见问题的解答和问题的解决方案。

另请参阅[Adobe Experience Platform常见问题解答和疑难解答文档](https://experienceleague.adobe.com/en/docs/experience-platform/landing/troubleshooting){target="_blank"}。

## 电子邮件渠道 {#ajo-troubleshooting-email}

+++ 如何防止在Adobe Journey Optimizer中使用主题时出现电子邮件格式问题？

在Adobe Journey Optimizer (AJO)中，修改电子邮件标头中的默认CSS块可能会导致意外的格式问题，尤其是在删除内容片段之后。 这些问题在移动设备上更加明显，并且可能会导致布局偏移或样式不一致。 要防止出现这种情况，请使用“主题”功能安全地应用自定义CSS，而无需更改系统生成的CSS样式。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"}，了解如何解决此问题。

在此页面[上了解有关电子邮件格式](../email/get-started-email-design.md)的更多信息。

+++


+++ 为什么具有可编辑字段的片段无法正常工作？

在Adobe Journey Optimizer中，包含可编辑字段的片段在添加到模板时可能无法正确加载或意外重复。 该问题通常会影响环境之间的特定片段。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"}，了解如何解决此问题。

在此页面[上了解有关可自定义片段](../content-management/customizable-fragments.md)的更多信息。

+++

+++ 为什么HTML片段没有在电子邮件中正确显示？

HTML片段在电子邮件中可能无法正确呈现，通常显示为&#x200B;**片段ID**&#x200B;而不是实际内容。 与可视化片段不同，HTML片段需要仔细配置。 要解决此问题，请遵循在电子邮件促销活动中同时使用&#x200B;**可视化和HTML表达式片段**&#x200B;的最佳实践。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-25441){target="_blank"}，了解如何解决此问题。

在此页面[上了解有关HTML片段](../content-management/fragments.md)的更多信息。

+++

+++ 为什么电子邮件模板和内容会从未发布的历程中消失？

在未发布的历程中编辑电子邮件模板时，某些电子邮件的内容和模板可能会意外消失。 这可能会导致返工和延迟。 为了降低此问题的风险，请避免同时进行编辑，限制打开选项卡的数量，并经常保存更改。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}，了解如何解决此问题。

在此页面[上了解有关模板](../email/use-email-templates.md)的更多信息。

+++

+++ 为什么电子邮件邮件引文字段未在“自行编码”模式下显示？ 

在&#x200B;**编辑电子邮件正文**&#x200B;功能下的&#x200B;**“自己编码”**&#x200B;模式中，未出现预编译标头输入字段。 要包含标头文本，用户必须在其自定义HTML内容中&#x200B;**手动编码标头**。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26174){target="_blank"}以了解如何解决此问题。

在此页面[上了解有关电子邮件邮件标头配置](../email/header-parameters.md)的更多信息。

+++

+++ 在电子邮件模板中使用HTML组件时，链接行为为何会出现差异？  

将&#x200B;**HTML组件**&#x200B;添加到电子邮件模板时，链接的行为可能会有所不同，具体取决于&#x200B;**电子邮件客户端**、**查看模式**&#x200B;或&#x200B;**设备/浏览器**。 例如，锚点链接在&#x200B;**Outlook的并排视图**&#x200B;中的功能与全屏视图中的功能有所不同。 在设计电子邮件模板并在多个客户端和设备中进行测试时，请注意这些变化。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26221){target="_blank"}以了解如何解决此问题。

另请参阅此页面[上的电子邮件设计最佳实践](../email/get-started-email-design.md)。

+++


+++ 如何防止报告中缺少电子邮件跟踪链接？

当电子邮件URL使用动态变量并且不以http开头时，或者当逻辑语句放置在URL字段中时，会出现Adobe Journey Optimizer中缺少链接跟踪的情况。 要解决此问题，请确保所有URL都以http开头，避免使用URL字段中的逻辑，并将复杂的个性化逻辑移动到HTML内容或预处理属性。


请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"}，了解如何解决此问题。

在此页面[上了解有关电子邮件跟踪](../email/message-tracking.md)的更多信息。

+++

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

## 应用程序内渠道

+++ 为什么在Customer Journey Analytics中无法报告应用程序内渠道？

在Adobe Customer Journey Analytics中报告&#x200B;**应用程序内渠道**&#x200B;的困难通常是由错误配置的&#x200B;**数据视图**、**数据集**&#x200B;或&#x200B;**架构更新**&#x200B;造成的。 确保正确应用这些配置来解决问题。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26206){target="_blank"}，了解有关此问题的更多信息。

在此页面[上了解如何在Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/integrations/ajo?lang=en#automatically-configure-journey-optimizer-integration){target="_blank"}中集成Journey Optimizer分析数据。

另请参阅[Journey Optimizer所有时间报表文档](../reports/report-gs-cja.md)

+++


## 数据管理 {#ajo-troubleshooting-data-management}

+++ 当您创建新的沙盒时，生存时间(TTL)设置如何应用于配置文件和数据湖数据集？

在Adobe Journey Optimizer中配置新沙盒的组织提出了生存时间(TTL)设置如何应用于配置文件和数据湖数据集的疑问。 本文阐明TTL设置不会影响现有沙盒，并且仅自动应用于新配置的沙盒。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"}，了解如何处理TTL。

在此页面[上了解有关数据集生存时间](../data/datasets-ttl.md)的更多信息。

+++


## 用户档案和受众管理 {#ajo-troubleshooting-audiences}

+++ 如何解决受众计数差异？

Adobe Journey Optimizer的&#x200B;**读取受众**&#x200B;功能中已处理的条目数可能低于预期的受众数。 此问题通常因命名空间配置不正确而出现，从而导致配置文件被排除在历程之外。 解决办法包括检查和更正命名空间配置、审查相关文档以及调整优先级以确保Adobe Journey Optimizer中的操作更顺畅。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"}，了解如何解决此问题。

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

+++ 为什么可参与用户档案计数在短时间内会显着增加？ 

**可参与的用户档案**&#x200B;量度反映过去12个月内历程或营销活动参与的独特用户档案数。 突然增加的原因可能是大量受众成为目标或数据集发生变化。 要管理此操作，请检查&#x200B;**配置文件计数逻辑**，调查针对大型受众的历程，**在历程级别过滤受众**，减少&#x200B;**可寻址受众大小**，并监控&#x200B;**数据集更改**。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26161){target="_blank"}，了解解决此问题的步骤。

使用[许可证使用情况仪表板](../audience/license-usage.md)监视您组织的许可证使用情况和可参与配置文件

另请参阅[Adobe Experience Platform查询服务概述](https://experienceleague.adobe.com/en/docs/experience-platform/query/home?lang=en){target="_blank"}。

+++

+++ 为什么电子邮件会根据日期函数发送给目标受众之外的个人？

电子邮件可能会发送给不符合指定受众条件&#x200B;**的收件人**。 例如，赎回日期在2025年7月4日&#x200B;**之前的成员**&#x200B;可能会收到仅针对该日期之后的成员的电子邮件。 此行为可能是由于&#x200B;**受众区段配置错误**&#x200B;或&#x200B;**配置文件资格逻辑**&#x200B;中的意外更改所致。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26173){target="_blank"}，了解解决此问题的步骤。

在此页面[上了解有关日期函数](../../rp_landing_pages/date-landing-page.md)的详细信息。

+++

+++ 如何在保存历程时解决受众选择问题和Chrome错误？

将受众添加到历程条件有时可能会导致&#x200B;**应用程序崩溃**&#x200B;或在Chrome中显示&#x200B;**Aw Snap错误**，包括保存历程时出错。 这些问题通常与&#x200B;**Chromium服务**&#x200B;有关。 要解决这些问题，请应用&#x200B;**浏览器更新**&#x200B;或使用适当的&#x200B;**解决方法**。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26145){target="_blank"}，了解解决此问题的步骤。

+++

## 历程 {#ajo-troubleshooting-journeys}

有关历程，请参阅以下疑难解答部分：

* [测试历程之前排查错误](../building-journeys/troubleshooting.md)
* [历程中的入站操作故障排除](../building-journeys/troubleshooting-inbound.md)
* [实时历程执行疑难解答](../building-journeys/troubleshooting-execution.md)
* [对自定义操作进行故障排除](../action/troubleshoot-custom-action.md)


+++ 为什么在创建新历程版本时表达式会丢失？  

创建历程的新版本时，特定步骤&#x200B;**中的**&#x200B;表达式可能会丢失，从而导致错误并需要手动重新输入。 要解决此问题，**复制历程**，测试可重现性，**避免浏览器重新加载**，并对较旧的历程使用&#x200B;**更新的画布**。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26152){target="_blank"}，了解解决此问题的步骤。

在此页面[上了解如何复制历程](../building-journeys/journey-ui.md#duplicate-a-journey)。

+++

+++ 为什么用户档案过早退出历程？ 

如果发送消息的&#x200B;**条件检查反馈状态**&#x200B;配置错误，则用户档案可能会意外退出历程，而无需通过指定的节点。 要解决此问题，请查看&#x200B;**条件逻辑**，实施&#x200B;**替代逻辑**，或咨询您的&#x200B;**实施团队**。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26127){target="_blank"}，了解解决此问题的步骤。

另请参阅[历程设计准则](../building-journeys/using-the-journey-designer.md)。

+++


+++ 为什么配置文件意外退出历程？

当发生&#x200B;**事件上限**&#x200B;时，配置文件可能会意外退出历程，如果处理的事件数超过系统容量，会导致某些配置文件被丢弃。 若要减少配置文件退出，请了解&#x200B;**系统限制**，监视&#x200B;**事件峰值**，并优化&#x200B;**数据流**&#x200B;以防止超过阈值。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26018){target="_blank"}，了解解决此问题的步骤。

另请参阅[历程护栏](../start/guardrails.md#journey-guardrails)。

+++


+++ 为什么我的事件没有触发预期历程？  

事件可能无法触发历程，即使符合通过查询服务&#x200B;**创建的**&#x200B;所有条件，而不是流式传输到&#x200B;**数据收集核心服务(DCCS)**&#x200B;时。 要解决此问题，请查看事件配置，确保事件直接流式传输到DCCS **，并使用**&#x200B;测试模式&#x200B;**验证功能。**

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"}，了解解决此问题的步骤。

在此页面[上了解有关事件](../event/about-events.md)的更多信息。

另请参阅[历程事件护栏](../start/guardrails.md#events)。

+++


+++ 如何解决Adobe Journey Optimizer中受众发生更改后的旅程触发问题？ 

如果旅程在修改其关联受众（例如更改合并策略）后停止触发，则流可能会中断。 要解决此问题，请&#x200B;**使用更新的受众设置复制并重新发布历程**，以确保触发器正常工作。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"}，了解解决此问题的步骤。

在此页面[上了解如何复制历程](../building-journeys/journey-ui.md#duplicate-a-journey)。

+++

+++ 为何调用外部第三方端点的自定义操作会超时？

当&#x200B;**自定义操作**&#x200B;调用外部第三方终结点时，可能会发生超时错误。 若要解决此问题，请验证&#x200B;**终结点是否可访问**，检查&#x200B;**服务器日志**，确保&#x200B;**没有来自Adobe的阻止**，根据需要更新终结点配置，并&#x200B;**在更新后进行测试**。 此外，请注意&#x200B;**API调用超时规范**。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26156){target="_blank"}，了解解决此问题的步骤。

在此页面[上了解有关历程限制API &#x200B;](../configuration/throttling.md)的更多信息。

另请参阅[与外部系统集成的文档](../configuration/external-systems.md)。

+++

+++ 如果您遇到403错误消息为&#x200B;**invalid_access**&#x200B;或&#x200B;**从箭头发布受众时未授予对此dataId=XX的访问权限**，您应该采取什么步骤？

要解决此错误，请让管理员验证您的用户配置文件是否有权访问受众发布所需的数据视图，然后再次尝试发布受众。

请参阅[权限文档](../administration/permissions.md){target="_blank"}以了解解决此问题的步骤。

+++

## 规则 {#ajo-troubleshooting-rules}

+++ 为什么上限规则下拉列表不起作用？

当规则集&#x200B;**配置错误**&#x200B;或&#x200B;**无法访问**&#x200B;时，**上限规则下拉列表**&#x200B;经常出现问题。 确保所有规则集均已正确配置并可用于解决问题。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26204){target="_blank"}以了解详情。

在本节[中了解如何应用上限规则](../conflict-prioritization/rule-sets.md)。

+++

## 决策 {#ajo-troubleshooting-decisioning}

+++ 如何解决创建优惠收藏集时出现的问题？

如果没有为您的组织配置&#x200B;**目录**，则创建优惠收藏集通常会遇到困难。 要解决此问题，请在尝试创建优惠收藏集之前，验证所有必需的目录是否已正确配置。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"}，了解解决此问题的步骤。

在此页面[上了解有关优惠收藏集](../offers/offer-library/creating-collections.md)的更多信息。

+++

+++ 为何无法访问Offer Decisioning？  

在使用Adobe Journey Optimizer将Adobe Target集成到应用程序时，在数据流配置中可能无法访问&#x200B;**Offer Decisioning**&#x200B;选项。 这通常是由于&#x200B;**权限设置**&#x200B;或&#x200B;**设置约束**&#x200B;所致。 要解决此问题，请验证用户权限并确保已进行必要的配置。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26175){target="_blank"}，了解解决此问题的步骤。

在此页面[上进一步了解Offer Decisioning &#x200B;](../offers/get-started/starting-offer-decisioning.md#granting-acess-to-decision-management)所需的权限。

+++



## 多语言 {#ajo-troubleshooting-multilingual}

+++ 如何解决此问题`Message validation error (CJMMAS - 1069-500)`？

在Adobe Journey Optimizer中，链接到多语言功能的消息验证错误(CJMMAS - 1069-500)阻止将历程设置为测试模式或发布。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"}，了解解决此问题的步骤。

在此页面[上了解有关多语言内容](../content-management/multilingual-gs.md)的更多信息。

+++


## 配置 {#ajo-troubleshooting-config}

+++ 如何为自定义操作启用TLS v1.3？  

要在连接到第三方系统时维护&#x200B;**数据完整性和安全性**，请确保为自定义操作启用了传输层安全性(**TLS**) v1.3。 这有助于保护通信并防止潜在的安全漏洞。


请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"}以了解详情。

在此页面[上了解有关多语言内容](../action/about-custom-action-configuration.md)的更多信息。

+++

+++ 为什么我无法直接从Adobe Journey Optimizer中的查询创建功能板？ 

在Adobe Journey Optimizer中，无法直接从查询创建功能板。 要构建仪表板，请使用Adobe Experience Platform中可用的&#x200B;**仪表板创建功能**，此功能允许您有效地可视化和分析查询数据。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"}以了解详情。

+++

## API {#ajo-troubleshooting-apis}

+++ 如何解决查询服务API的访问问题？  

通过Postman或类似工具使用&#x200B;**查询服务API**&#x200B;时的访问错误通常是由于&#x200B;**权限不足**&#x200B;导致的。 要解决此问题，请验证用户权限，检查API凭据，并在需要时提供支持的详细信息。

请参阅[本疑难解答文章](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26196){target="_blank"}以了解详情。

另请参阅[管理API凭据文档](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions?lang=en#manage-api-credentials-for-role){target="_blank"}。

+++
