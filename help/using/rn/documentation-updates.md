---
solution: Journey Optimizer
product: journey optimizer
title: 文档更新
description: 了解最新文档更新
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: 3adcd750089d81e6216316dc3d39f6a7982033f4
workflow-type: tm+mt
source-wordcount: '2246'
ht-degree: 0%

---

# 文档更新 {#latest-updates}

本页列出了 [!DNL Journey Optimizer].

## 2022年12月 {#december-2022}

* 邮件指南已重组并拆分为每个渠道的专用指南：

   * [电子邮件渠道](../email/get-started-email.md)
   * [推送通知渠道](../push/get-started-push.md)
   * [短信渠道](../sms/get-started-sms.md)

* 配置指南已重新组织，以提高可读性。 [了解更多](../configuration/get-started-configuration.md)

## 2022年11月 {#november-2022}

* 添加了有关Journey Optimizer集成的新页面。 [了解更多](../start/ajo-integrations.md)
* 添加了关于镜像页面URL长度的推荐。 [了解更多](../email/message-tracking.md)
* 在电子邮件设置配置的回复电子邮件地址中添加了新子部分，包括确保正确回复管理的建议。 [了解更多](../email/email-settings.md#reply-to-email)
* 添加了有关如何修改实时历程中消息内容的章节。 [了解更多](../building-journeys/journeys-message.md#update-live-content)

## 2022年10月 {#october-2022}

* 添加了有关如何使用外部数据源和自定义操作限制吞吐量的历程用例。 [了解更多](../building-journeys/limit-throughput.md)
* 历程用例部分已重组为两个类别： [业务用例](../building-journeys/journeys-uc.md) 和 [技术用例](../building-journeys/collections.md).
* 的 **实体数据集** 章节已更新，其中包含更多详细信息。 [了解更多](../data/datasets-query-examples.md#entity-dataset)
* 选择退出管理和同意策略部分已重组。 [了解更多](../privacy/opt-out.md)
* 对历程消息中高级参数的部分进行了阐明，现在指定电子邮件地址覆盖仅应用于特定用例。 在大多数情况下，定义为 **执行字段** 是应该使用的。
* 在 **配置登陆页面子域** 部分，以指定登陆页面子域中不允许使用大写字母。 [了解更多](../landing-pages/lp-subdomains.md)

## 2022年9月 {#september-2022}

* 随附的所有新增功能和改进功能 [!DNL Journey Optimizer] 文档详细介绍了’22年9月的发布。 [了解更多](release-notes.md)
* 添加了与在定期读取区段历程中使用等待活动相关的最佳实践。 [了解更多](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* 添加了新的步骤事件查询示例以及有关id、instanceid和profileid之间差异的信息。 [了解更多](../reports/query-examples.md).
* 更新了与 [toDateOnly](../building-journeys/functions/functiontodateonly.md) 和 [toString](../building-journeys/functions/functiontostring.md) 函数。
* 添加了有关时间条件参数的详细信息。 [了解更多](../building-journeys/condition-activity.md#time_condition)
* 添加了有关内置数据集的信息。 [了解更多](../data/get-started-datasets.md#access-datasets)
* 改进并重组了“全局报告”和“实时报告”章节。 [了解更多](../reports/global-report.md)
* 添加了Adobe Journey Optimizer中可用的每个报表量度的列表。
   [了解更多](../reports/global-report.md#email-and-sms-metrics)
* “密件抄送电子邮件”部分已移至新的“支持存档”页面。 [了解更多](../configuration/archiving-support.md)

## 2022年8月 {#august-2022}

* 随附的所有新增功能和改进功能 [!DNL Journey Optimizer] 文档详细介绍了’22年8月的发行情况。 [了解更多](release-notes.md)
* “频度规则”部分已更新，以反映新的在线消息传递流程。 [了解更多](../configuration/frequency-rules.md#apply-frequency-rule)
* 现在，有关如何配置订阅和创建登陆页面的视频，请参阅登陆页面快速入门一节。 [了解更多](../landing-pages/get-started-lp.md#video)
* 添加了对使用读取区段活动的历程的限制。 [了解更多](../building-journeys/read-segment.md)
* 表达式编辑器运算符页面已得到改进。 [了解更多](../building-journeys/expression/operators.md)
* 添加了有关如何计划营销活动的章节。 [了解更多](../campaigns/create-campaign.md)
* 表达式编辑器的“常规语法规则”部分已更新，以考虑有关文本函数中反斜杠符号转义的新规则。 此更改不会影响现有已发布的消息。 只能更新新消息或草稿消息。 [了解更多](../personalization/personalization-syntax.md#general-rules)

## 2022年7月 {#july-2022}

* 随附的所有新增功能和改进功能 [!DNL Journey Optimizer] 文档详细介绍了’22年7月的发行版本。 [了解更多](release-notes.md)
* 的 **设置通道曲面** 阐明并更新了章节，其中包含描述如何配置短信渠道的页面链接。 [了解更多](../configuration/channel-surfaces.md#create-channel-surface)
* 在历程属性中， **配置文件时区** 选项现在默认处于禁用状态。 [了解更多](../building-journeys/timezone-management.md#timezone-from-profiles)
* 在 **等待** 活动， **固定日期** 选项不再可用。 [了解更多](../building-journeys/wait-activity.md)
* 添加了有关 **增量读取** 选项 **读取区段** 活动。 [了解更多](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* 在 **配置文件上限** 条件类型。 [了解更多](../building-journeys/condition-activity.md#profile_cap)
* 添加了对业务事件的限制。 [了解更多](../start/guardrails.md#events-g)

## 2022年6月 {#june-2022}

* 随附的所有新增功能和改进功能 [!DNL Journey Optimizer] 文档详细介绍了’22年6月的发行情况。 [了解更多](release-notes.md)
* 文档中新增了有关隐私请求的章节。 [了解更多](../privacy/requests.md)
* 文档中新增了有关资源审核日志的章节。 [了解更多](../privacy/audit-logs.md)
* 文档中新增了有关如何将来自Adobe Experience Cloud资产库的HTML或JSON内容添加到选件表示的章节。 [了解更多](../offers/offer-library/add-representations.md#html-json)
* 在历程生命周期中添加了新页面。 [了解更多](../building-journeys/journey.md#journey-versions)
* 更新了“等待”活动页面。 [了解更多](../building-journeys/wait-activity.md)
* 添加了包含查询示例的Adobe Journey Optimizer数据集列表。 [了解更多](../data/datasets-query-examples.md)
* 允许列表页面已移至配置部分。 [了解更多](../configuration/allow-list.md)
* 更新了“抑制”列表页面以阐明某些信息，包括在抑制字段中允许包含32到126之间的所有ASCII字符。 [了解更多](../configuration/manage-suppression-list.md)
* 添加了用于决策管理的护栏和静态限制的链接。 [了解更多](../start/guardrails.md)
* 发送时间优化功能现已适用于所有客户。 测试版提及已删除。 [了解更多](../building-journeys/journeys-message.md#send-time-optimization)
* Batch Decisioning API已添加到可用API列表中，以交付个性化优惠。 [了解更多](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## 2022年5月 {#may-2022}

* 随附的所有新增功能和改进功能 [!DNL Journey Optimizer] 文档中对’22年5月版进行了详细介绍。 [了解更多](release-notes.md)
* 与 [区段鉴别](../reports/query-examples.md#segment-qualification-queries) 和 [事件](../reports/query-examples.md#event-based-queries) 已添加。
* 电子邮件设计部分现在提及了新的内置模板，可用于开始内容。 相关屏幕截图已更新。 [了解更多](../email/get-started-email-design.md)
* Journey Optimizer文档主页中更新了指向关键资源的链接。
* 登陆页面和订阅报告的屏幕截图已更新。 [了解更多](../reports/live-report.md)
* 添加了注释，说明自定义操作不支持Delete方法。 [了解更多](../action/about-custom-action-configuration.md)
* 操作方法视频的链接已更新。
* 的 [电子邮件配置](../configuration/about-subdomain-delegation.md), [消息预设](../configuration/channel-surfaces.md) 和 [配置登陆页面](../landing-pages/lp-subdomains.md) 已重组各部分，以提高可读性。
* URL跟踪部分已更新并改进以提供示例。 [了解更多](../email/email-settings.md#url-tracking)
* 添加了关于设置转发电子邮件地址的新子部分。 请注意，您无法通过用户界面执行此操作。 [了解更多](../email/email-settings.md#forward-email)

## 2022年4月 {#april-2022}

* 随附的所有新增功能和改进功能 [!DNL Journey Optimizer] 文档详细介绍了’22年4月的发行情况。 [了解更多](release-notes.md)
* 的 **反应** 事件文档页面已更新。 [了解更多](../building-journeys/reaction-events.md)
* 更新了有关决策管理功能的视频，以反映Journey Optimizer用户界面。 [了解更多](../offers/get-started/starting-offer-decisioning.md)
* 的 **数据集入门** 部分已得到改进，以详细说明如何访问和创建数据集。 [了解更多](../data/get-started-datasets.md)
* 在 **Adobe Journey Optimizer文档** 主页。 [了解更多](https://experienceleague.adobe.com/docs/journey-optimizer.html)
* 的 **创建消息预设** 部分现在指定当选定的IP池在版本(**[!UICONTROL Processing]** 状态)且从未与选定的子域关联。 [了解更多](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* 消息预设 **URL跟踪** 更新了部分，以反映用户界面中的细微更改。 [了解更多](../configuration/channel-surfaces.md#url-tracking)

## 2022年3月 {#march-2022}

* 随附的所有新增功能和改进功能 [!DNL Journey Optimizer] 文档中对’22年3月版进行了详细介绍。 [了解更多](release-notes.md)
* 在 **Offer Decisioning** 部分，包括对 [自动优化模型](../offers/ranking/auto-optimization-model.md)、使用的算法以及更多技术详细信息。 [了解更多](../offers/ranking/ai-models.md)
* 测试用户档案创建页面已移至  **区段、用户档案和身份** 中。 [了解更多](../segment/creating-test-profiles.md)
* 添加了一个示例，说明如何在表达式编辑器中将表达式添加为默认值。 [了解更多](../building-journeys/expression/field-references.md#default-value)
* 的 **创建个性化优惠** 重组了章节，以提高可读性。 [了解更多](../offers/offer-library/creating-personalized-offers.md)
* 添加了新部分，以描述更改选件的开始和/或结束日期可能对此选件频率上限产生的影响。 [了解更多](../offers/offer-library/add-constraints.md#capping-change-date)
* 的 **更改主电子邮件地址** 更新了部分以反映用户界面的更改。 [了解更多](../configuration/primary-email-addresses.md)

## 2022年2月 {#feb-2022}

* 随附的所有新增功能和改进功能 [!DNL Journey Optimizer] 文档详细介绍了’22年2月的版本。 [了解更多](release-notes.md)
* 的 [替换](../building-journeys/functions/functionreplace.md#example_2) 和 [replaceAll](../building-journeys/functions/functionreplaceall.md#example) 函数文档页面已更新，其中包含有关target参数的其他信息和示例。
* 最佳实践已添加到 [运算符](../building-journeys/expression/operators.md#important-notes) 页面。

## 2022年1月 {#january-2022}

* 随附的所有新增功能和改进功能 [!DNL Journey Optimizer] 文档中对’22年1月版进行了详细介绍。 [了解更多](release-notes.md)
* 的 **Offer决策AI排名** 更新了章节，提供了自动优化模型的更详细描述。 [了解更多](../offers/ranking/auto-optimization-model.md)
* 添加了关于在使用排名策略时需要能够发送事件类型的架构要求的新部分。 [了解更多](../offers/ranking/schema-requirement.md)
* 与 [!DNL Journey Optimizer] 个性化功能已重新组织，以便更好地阅读。 [了解更多](../personalization/personalize.md)
* 的 **创建消息预设** 为提高清晰度，已将部分分为多个部分。 [了解更多](../configuration/channel-surfaces.md#create-channel-surface)
* 的 **选择退出管理** 对部分进行了澄清和轻微重组。 [了解更多](../privacy/opt-out.md#opt-out-management)
* 的 **插入链接** 章节已更新，以反映最近对用户界面所做的更改。 [了解更多](../email/message-tracking.md#insert-links)

## 2021年11月 {#november-2021}

* 对 **高级表达式编辑器** 在历程中使用现已可用。 [了解更多](../building-journeys/expression/expressionadvanced.md)
* 新增了关于 **CNAME子域委派方法** 已添加。 [了解更多](../configuration/delegate-subdomain.md#cname-subdomain-delegation)


## 2021年10月 {#october-2021}

* 随附的所有新增功能和改进功能 [!DNL Journey Optimizer] 文档中对’21年10月版进行了详细介绍。 [了解更多](release-notes.md)
* 添加了 **日期时间函数** 列表。 [了解更多](../personalization/functions/dates.md)
* 新建 **每个用户角色的快速入门部分**. 走自己的路，更快地实现目标！ [了解更多](../start/quick-start.md)
* 新建 **编辑消息预设** 中。 [了解更多](../configuration/channel-surfaces.md#edit-channel-surface)
* 新建 **编辑PTR记录** 中。 [了解更多](../configuration/ptr-records.md#edit-ptr-record)
* 新建 **停用消息预设** 中。 [了解更多](../configuration/channel-surfaces.md#edit-channel-surface#deactivate-a-surface)
* 向 **决策管理API开发人员指南** 受移动设备不支持的选件限制 [!DNL Experience Edge] 工作流。 [了解更多](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* 新建 **创建模拟** 中。 [了解更多](../offers/offer-activities/simulation.md)
* 已更新 **添加决策作用域** 中。 [了解更多](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* 已更新 **定义表示的内容** 部分，包括新 [子章](../offers/offer-library/creating-personalized-offers.md#custom-text) 了解如何定义和个性化自定义文本。 [了解更多](../offers/offer-library/creating-personalized-offers.md#content)

## 2021年9月 {#september-2021}

* 以下函数页面已更新： [sethours](../building-journeys/functions/functionsethours.md), [getListItem](../building-journeys/functions/functiongetlistitem.md), [inSegment](../building-journeys/functions/functioninsegment.md)

* 添加了以下函数： [过滤器](../building-journeys/functions/functionfilter.md), [相交](../building-journeys/functions/functionintersect.md), [toDateOnly](../building-journeys/functions/functiontodateonly.md)

* 在表达式编辑器文档中添加了dateOnly日期类型。 [了解更多](../building-journeys/expression/data-types.md)

* 添加了有关自定义操作缓存持续时间的详细信息。 [了解更多](../datasource/external-data-sources.md#custom-authentication-mode)

* 添加了有关自定义操作默认端口的信息。 [了解更多](../action/about-custom-action-configuration.md#url-configuration)

* 添加了有关多个业务事件用例的信息。 [了解更多](../event/about-creating-business.md#multiple-business-events)

* 添加了在数据湖中查询历程步骤事件的常用示例。 [了解更多](../reports/query-examples.md)

* 添加了 **限制** 页面。 [了解更多](../start/guardrails.md)

* 改进了 **快速入门** 页面，其中包含不同角色的步骤。 [了解更多](../start/quick-start.md)

* 现在，专用部分中描述的所有决策管理功能也适用于使用Offer Decisioning应用程序服务的Adobe Experience Platform用户。 [了解更多](../offers/get-started/starting-offer-decisioning.md)

* 添加了子部分，以阐明在应用约束限制为给定版面选择选件时，使用区段与使用决策规则之间的差异。 [了解更多](../offers/offer-activities/create-offer-activities.md#segments-vs-decision-rules)

* 添加了特定的排名公式示例，以说明一些实际用例。 [了解更多](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* 添加了关于如何编辑IP池的子部分。 [了解更多](../configuration/ip-pools.md#edit-ip-pool)


## 2021年8月 {#august-2021}

* 随附的所有新增功能和改进功能 [!DNL Journey Optimizer] 文档详细介绍了’21年8月的发行情况。 [了解更多](release-notes.md)
* 更新了决策管理权限。 [了解更多](../administration/ootb-product-profiles.md)
* 使用最新UI更新了Email designer屏幕截图。
* 更新了使用动态URL路径和动态标头进行自定义操作的配置过程。 [了解更多](../action/about-custom-action-configuration.md#url-configuration)
* 添加了有关辅助功能和快捷键的章节。 [了解更多](../start/user-interface.md#accessibility)
* 添加了有关区段评估方法的章节。 [了解更多](../segment/about-segments.md#evaluation-method-in-journey-optimizer)
* 在“禁止列表”、“允许列表”和“电子邮件全局/实时报表”部分添加了注释，以指定“电子邮件报表发送”量度中排除状态为“禁止显示”和“不允许显示”的用户档案。 [了解更多](../reports/global-report.md)
* 添加了新章节，介绍如何检索因电子邮件地址或域未列在允许列表中而从发送中排除的域。 [了解更多](../configuration/allow-list.md#reporting)
* 更新了启用允许列表章节。 [了解更多](../configuration/allow-list.md#enable-allow-list)
* 更新了“监视器”消息预设部分，其中包含可能的预设创建失败原因以及有关此类错误的详细信息。 [了解更多](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* 更新并重命名了“重试”时间段部分，以反映您现在可以调整消息预设中的电子邮件重试设置这一事实。 [了解更多](../configuration/retries.md#retry-duration)
* 添加了新章节，介绍如何在电子邮件内容中插入一键单击选择退出链接。 [了解更多](../privacy/opt-out.md#one-click-opt-out-link)
* 更新了委派子域部分，其中包含有关Adobe执行验证过程的更多详细信息。 [了解更多](../configuration/delegate-subdomain.md#subdomain-validation)
* 添加了描述如何手动将电子邮件地址和域添加到禁止列表的部分。 [了解更多](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* 更新了 [访问禁止列表](../configuration/manage-suppression-list.md#access-suppression-list) 部分和 [重试](../configuration/retries.md) 部分来反映新的用户界面。
* 记录了在创建选件时用于添加和配置表示法的新流程。 [了解更多](../offers/offer-library/creating-personalized-offers.md#representations)


## 2021年7月 {#july-2021}

* 随附的所有新增功能和改进功能 [!DNL Journey Optimizer] 文档详细介绍了’21年7月的发行版本。 [了解更多](release-notes.md)
* 在 [!DNL Journey Optimizer] 主页和目录
* Experience Platform服务的新登陆页面可在 [!DNL Journey Optimizer]
* 添加了 [!DNL Journey Optimizer] 主页中的产品描述
* 在多个页面中添加了教程视频
* 优化了主页图像
* 将“消息跟踪”部分移动、改进并重命名为“添加链接和跟踪消息”。 [了解更多](../email/message-tracking.md)
* 在镜像页面上添加了子部分。 [了解更多](../email/message-tracking.md#mirror-page)
* 在文档和屏幕中，将“选件活动”重命名为“决策”，将“决策”重命名为“决策范围”。 [了解更多](../offers/get-started/starting-offer-decisioning.md)
* 新用例： [使用帮助程序函数对消息进行个性化](../personalization/personalization-use-case-helper-functions.md)
* 更新了读取区段文档，以反映实体化区段的影响。 [了解更多](../building-journeys/read-segment.md)
* 更新了历程限制。 [了解更多](../start/guardrails.md)
* 更新了决策中的配置选件选择部分。 [了解更多](../offers/offer-activities/configure-offer-selection.md)
* 添加了警告，以说明当前不支持基于事件的选件。 [了解更多](../offers/offer-library/creating-personalized-offers.md#eligibility)
* 记录了新的“决策管理” **[!UICONTROL Overview]** 选项卡。 [了解更多](../offers/get-started/user-interface.md#overview)
* 添加了新章节，以描述选件和决策列表中可用的操作： [选件列表](../offers/offer-library/creating-personalized-offers.md#offer-list) 和 [决策列表](../offers/offer-activities/create-offer-activities.md#decision-list).

