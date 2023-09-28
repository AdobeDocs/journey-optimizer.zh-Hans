---
product: Journey Optimizer
audience: end-user
user-guide-title: Journey Optimizer 指南
user-guide-description: 使用 Journey Optimizer 为您的客户构建并提供互联、情境式和个性化的体验
type: Documentation
solution: Journey Optimizer
source-git-commit: c5c7d4d050958fac9b91e2a2a4c4a7a6640d1f06
workflow-type: tm+mt
source-wordcount: '1521'
ht-degree: 93%

---

# Adobe Journey Optimizer 帮助 {#using}

+ [Journey Optimizer 文档](ajo-home.md)
+ 新增功能{#whats-new}
   + [早期发行说明](using/rn/e-release-notes.md)
   + [最新发行说明](using/rn/release-notes.md)
   + 过往发行说明 {#previous-rn-new}
      + [2022 年发行说明](using/rn/release-notes-2022.md)
      + [2021 年发行说明](using/rn/release-notes-2021.md)
   + [文档更新](using/rn/documentation-updates.md)
+ 入门{#get-started}
   + [什么是 Journey Optimizer](using/start/get-started.md)
   + 快速入门指南{#quick-start}
      + [概述](using/start/quick-start.md)
      + [营销人员入门](using/start/path/marketer.md)
      + [数据工程师入门](using/start/path/data-engineer.md)
      + [管理员入门](using/start/path/administrator.md)
      + [开发人员入门](using/start/path/developer.md)
   + [用户界面](using/start/user-interface.md)
   + [搜索、筛选、分类](using/start/search-filter-categorize.md)
   + [辅助功能](using/start/accessibility.md)
   + [集成](using/start/ajo-integrations.md)
   + [护栏](using/start/guardrails.md)
   + [最佳实践](using/start/best-practices.md)
+ 历程 {#orchestrate-journeys}
   + [历程入门](using/building-journeys/journey.md)
   + 创建历程{#create-journey}
      + [创建您的第一个历程](using/building-journeys/journey-gs.md)
      + [设计您的历程](using/building-journeys/using-the-journey-designer.md)
      + [测试您的历程](using/building-journeys/testing-the-journey.md)
      + [发布您的历程](using/building-journeys/publishing-the-journey.md)
   + 管理您的历程{#manage-journey}
      + [结束您的历程](using/building-journeys/end-journey.md)
      + [时区管理](using/building-journeys/timezone-management.md)
      + [用户档案入口管理](using/building-journeys/entry-management.md)
      + [将历程复制到另一个沙盒](using/building-journeys/copy-to-sandbox.md)
      + [对历程进行故障排除](using/building-journeys/troubleshooting.md)
      + [与智能服务集成](using/building-journeys/ai-services-overview.md)
   + 活动 {#about-journey-building}
      + [历程活动入门](using/building-journeys/about-journey-activities.md)
      + [一般事件](using/building-journeys/general-events.md)
      + [反应](using/building-journeys/reaction-events.md)
      + [受众鉴别](using/building-journeys/audience-qualification-events.md)
      + [条件](using/building-journeys/condition-activity.md)
      + [等待](using/building-journeys/wait-activity.md)
      + [读取受众](using/building-journeys/read-audience.md)
      + [电子邮件、应用程序内消息、推送、短信](using/building-journeys/journeys-message.md)
      + [自定义操作](using/building-journeys/using-custom-actions.md)
      + [Adobe Campaign Standard 操作](using/building-journeys/using-adobe-campaign-standard.md)
      + [Adobe Campaign v7/v8 操作](using/building-journeys/using-adobe-campaign-classic.md)
      + [跳转](using/building-journeys/jump.md)
      + [更新用户档案](using/building-journeys/update-profiles.md)
   + 构建表达式 {#building-advanced-conditions-journeys}
      + [概述](using/building-journeys/expression/expressionadvanced.md)
      + 语法 {#syntax}
         + [概述](using/building-journeys/expression/generalities.md)
         + [条件指令](using/building-journeys/expression/conditional-instruction.md)
         + [数据类型](using/building-journeys/expression/data-types.md)
         + [字段引用](using/building-journeys/expression/field-references.md)
         + [收藏集管理函数](using/building-journeys/expression/collection-management-functions.md)
         + [操作员](using/building-journeys/expression/operators.md)
         + [历程属性](using/building-journeys/expression/journey-properties.md)
         + [示例](using/building-journeys/expression/advanced-editor-use-cases.md)
      + 函数 {#main-functions-journey}
         + [主要函数](using/building-journeys/expression/functions.md)
         + Adobe Experience Platform {#adobe-experience-platform}
            + [inSegment](using/building-journeys/functions/functioninsegment.md)
         + 聚合 {#aggregation}
            + [avg](using/building-journeys/functions/functionavg.md)
            + [count](using/building-journeys/functions/functioncount.md)
            + [countOnlyNull](using/building-journeys/functions/functioncountonlynull.md)
            + [countWithNull](using/building-journeys/functions/functioncountwithnull.md)
            + [distinctCount](using/building-journeys/functions/functiondistinctcount.md)
            + [distinctCountWithNull](using/building-journeys/functions/functiondistinctcountwithnull.md)
            + [max](using/building-journeys/functions/functionmax.md)
            + [min](using/building-journeys/functions/functionmin.md)
            + [sum](using/building-journeys/functions/functionsum.md)
         + 转化 {#conversion}
            + [toBool](using/building-journeys/functions/functiontobool.md)
            + [toDateOnly](using/building-journeys/functions/functiontodateonly.md)
            + [toDateTime](using/building-journeys/functions/functiontodatetime.md)
            + [toDateTimeOnly](using/building-journeys/functions/functiontodatetimeonly.md)
            + [toDecimal](using/building-journeys/functions/functiontodecimal.md)
            + [toDuration](using/building-journeys/functions/functiontoduration.md)
            + [toInteger](using/building-journeys/functions/functiontointeger.md)
            + [toString](using/building-journeys/functions/functiontostring.md)
         + 日期 {#date}
            + [currentTimeInMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
            + [inLastDays](using/building-journeys/functions/functioninlastdays.md)
            + [inLastHours](using/building-journeys/functions/functioninlasthours.md)
            + [inLastMonths](using/building-journeys/functions/functioninlastmonths.md)
            + [inLastYears](using/building-journeys/functions/functioninlastyears.md)
            + [inNextDays](using/building-journeys/functions/functioninnextdays.md)
            + [inNextHours](using/building-journeys/functions/functioninnexthours.md)
            + [inNextMonths](using/building-journeys/functions/functioninnextmonths.md)
            + [inNextYears](using/building-journeys/functions/functioninnextyears.md)
            + [now](using/building-journeys/functions/functionnow.md)
            + [nowWithDelta](using/building-journeys/functions/functionnowwithdelta.md)
            + [setHours](using/building-journeys/functions/functionsethours.md)
            + [setDays](using/building-journeys/functions/functionsetdays.md)
            + [updateTimeZone](using/building-journeys/functions/functionupdatetimezone.md)
         + 列表 {#list}
            + [distinct](using/building-journeys/functions/functiondistinct.md)
            + [distinctWithNull](using/building-journeys/functions/functiondistinctwithnull.md)
            + [filter](using/building-journeys/functions/functionfilter.md)
            + [getListItem](using/building-journeys/functions/functiongetlistitem.md)
            + [in](using/building-journeys/functions/functionin.md)
            + [intersect](using/building-journeys/functions/functionintersect.md)
            + [limit](using/building-journeys/functions/functionlimit.md)
            + [listSize](using/building-journeys/functions/functionlistsize.md)
            + [serializeList](using/building-journeys/functions/functionserializelist.md)
            + [sort](using/building-journeys/functions/functionsort.md)
         + 数学 {#math}
            + [random](using/building-journeys/functions/functionrandom.md)
            + [round](using/building-journeys/functions/functionround.md)
         + 字符串 {#string}
            + [concat](using/building-journeys/functions/functionconcat.md)
            + [contain](using/building-journeys/functions/functioncontain.md)
            + [containIgnoreCase](using/building-journeys/functions/functioncontainwithignorecase.md)
            + [endWith](using/building-journeys/functions/functionendwith.md)
            + [endWithIgnorecase](using/building-journeys/functions/functionendwithignorecase.md)
            + [equalIgnoreCase](using/building-journeys/functions/functionequalignorecase.md)
            + [indexOf](using/building-journeys/functions/functionindexof.md)
            + [isEmpty](using/building-journeys/functions/functionisempty.md)
            + [isNotEmpty](using/building-journeys/functions/functionisnotempty.md)
            + [lastIndexOf](using/building-journeys/functions/functionlastindexof.md)
            + [长度](using/building-journeys/functions/functionlength.md)
            + [lower](using/building-journeys/functions/functionlower.md)
            + [matchRegExp](using/building-journeys/functions/functionmatchregexp.md)
            + [notequalIgnoreCase](using/building-journeys/functions/functionnotequalignorecase.md)
            + [replace](using/building-journeys/functions/functionreplace.md)
            + [replaceAll](using/building-journeys/functions/functionreplaceall.md)
            + [split](using/building-journeys/functions/functionsplit.md)
            + [startWith](using/building-journeys/functions/functionstartwith.md)
            + [startWithIgnoreCase](using/building-journeys/functions/functionstartwithignorecase.md)
            + [substr](using/building-journeys/functions/functionsubstr.md)
            + [trim](using/building-journeys/functions/functiontrim.md)
            + [upper](using/building-journeys/functions/functionupper.md)
            + [uuid](using/building-journeys/functions/functionuuid.md)
   + 用例 {#journey-use-cases}
      + 商业用例 {#business-use-cases}
         + [发送多渠道消息](using/building-journeys/journeys-uc.md)
         + [使用 Campaign v7/v8 发送消息](using/building-journeys/ajo-ac.md)
         + [向订阅者发送消息](using/building-journeys/message-to-subscribers-uc.md)
      + 技术用例 {#technical-use-cases}
         + [使用自定义操作动态传递集合](using/building-journeys/collections.md)
         + [增加投放数量](using/building-journeys/ramp-up-deliveries-uc.md)
         + [使用外部数据源和自定义操作限制吞吐量](using/building-journeys/limit-throughput.md)
+ 营销活动{#campaigns}
   + [营销活动入门](using/campaigns/get-started-with-campaigns.md)
   + [创建营销活动](using/campaigns/create-campaign.md)
   + [查看和激活营销活动](using/campaigns/review-activate-campaign.md)
   + [管理活动](using/campaigns/modify-stop-campaign.md)
   + 内容体验{#content-experiment}
      + [内容体验入门](using/campaigns/get-started-experiment.md)
      + [创建内容体验](using/campaigns/content-experiment.md)
      + [配置实验报告](using/campaigns/reporting-configuration.md)
      + 技术说明 {#technotes}
         + [了解统计计算](using/campaigns/experiment-calculations.md)
         + [了解试验报告中的统计计算](using/campaigns/experiment-report-calculations.md)
   + [使用 API 触发活动](using/campaigns/api-triggered-campaigns.md)
+ 电子邮件渠道 {#email}
   + [电子邮件入门](using/email/get-started-email.md)
   + [创建电子邮件](using/email/create-email.md)
   + 设计电子邮件内容 {#design-email}
      + [电子邮件设计入门](using/email/get-started-email-design.md)
      + 开始创建内容 {#start-creating-content}
         + [从头开始设计内容](using/email/content-from-scratch.md)
         + [导入内容](using/email/existing-content.md)
         + [对您自己的内容进行编码](using/email/code-content.md)
         + [使用模板](using/email/email-templates.md)
      + 设计内容 {#add-content}
         + [使用内容组件](using/email/content-components.md)
         + [添加链接和跟踪消息](using/email/message-tracking.md)
         + [插入个性化优惠](using/email/add-offers-email.md)
         + [生成文本版本](using/email/text-version-email.md)
         + [添加预编译标头](using/email/preheader.md)
      + 编辑样式 {#edit-style}
         + [电子邮件样式入门](using/email/get-started-email-style.md)
         + [编辑背景设置](using/email/backgrounds.md)
         + [调整垂直对齐和填充](using/email/alignment-and-padding.md)
         + [添加内联样式属性](using/email/inline-styling.md)
   + [预览和测试电子邮件](using/email/preview.md)
   + [创建内容模板](using/email/content-templates.md)
   + [使用 Experience Manager 模板](using/email/aem-templates.md)
   + [使用片段](using/email/fragments.md)
   + [管理电子邮件选择退出](using/email/email-opt-out.md)
   + 配置电子邮件渠道 {#configure-email}
      + [电子邮件配置入门](using/email/get-started-email-config.md)
      + [配置电子邮件设置](using/email/email-settings.md)
+ 应用程序内渠道{#in-app}
   + [应用程序内渠道入门](using/in-app/get-started-in-app.md)
   + [创建应用程序内消息](using/in-app/create-in-app.md)
   + [设计应用程序内内容](using/in-app/design-in-app.md)
   + [测试并发送应用程序内通知](using/in-app/send-in-app.md)
   + [配置应用程序内渠道](using/in-app/inapp-configuration.md)
+ 推送通知渠道{#push}
   + [推送通知入门](using/push/get-started-push.md)
   + [创建推送通知](using/push/create-push.md)
   + [设计推送通知](using/push/design-push.md)
   + [发送推送通知](using/push/send-push.md)
   + 配置推送通知{#push-config}
      + [推送通知数据流](using/push/push-gs.md)
      + [配置推送通知渠道](using/push/push-configuration.md)
      + [移动端加入快速入门工作流程](using/push/mobile-onboarding-wf.md)
+ 短信渠道{#sms}
   + [短信入门](using/sms/get-started-sms.md)
   + [创建短信消息](using/sms/create-sms.md)
   + [预览和测试短信](using/sms/send-sms.md)
   + [管理短信选择禁用](using/sms/sms-opt-out.md)
   + [配置短信渠道](using/sms/sms-configuration.md)
   + [设置短信子域](using/sms/sms-subdomains.md)
+ 直邮 {#direct-mail}
   + [直邮入门](using/direct-mail/get-started-direct-mail.md)
   + [创建直邮](using/direct-mail/create-direct-mail.md)
   + [测试并发送直邮消息](using/direct-mail/test-send-direct-mail.md)
   + [配置直邮](using/direct-mail/direct-mail-configuration.md)
+ Web 渠道 {#web}
   + [Web 渠道入门](using/web/get-started-web.md)
   + [Web 渠道先决条件](using/web/web-prerequisites.md)
   + [创建 Web 体验](using/web/create-web.md)
   + 创建 Web 页面 {#author-web-pages}
      + [编辑网页内容](using/web/edit-web-content.md)
      + [管理修改](using/web/manage-web-modifications.md)
      + [监测您的Web活动](using/web/monitor-web-campaigns.md)
      + [创作单页应用程序](using/web/web-spa.md)
   + [配置 Web 子域](using/web/web-delegated-subdomains.md)
+ 基于代码的体验 {#code-based-experience}
   + [基于代码的渠道入门](using/code-based/get-started-code-based.md)
   + [基于代码的先决条件](using/code-based/code-based-prerequisites.md)
   + [基于代码的实施示例](using/code-based/code-based-implementation-samples.md)
   + [创建基于代码的体验](using/code-based/create-code-based.md)
+ 登陆页面{#landing-pages}
   + [登陆页面入门](using/landing-pages/get-started-lp.md)
   + [创建登陆页面](using/landing-pages/create-lp.md)
   + 设计内容 {#landing-pages-design}
      + [关于登陆页面设计](using/landing-pages/design-lp.md)
      + [创建登陆页面内容](using/landing-pages/lp-content.md)
      + [创建模板](using/landing-pages/lp-templates.md)
      + [添加自定义 JavaScript](using/landing-pages/lp-custom-js.md)
   + [创建订阅列表](using/landing-pages/subscription-list.md)
   + [通过用例学习](using/landing-pages/lp-use-cases.md)
   + 配置登陆页面 {#lp-configuration}
      + [配置登陆页面子域](using/landing-pages/lp-subdomains.md)
      + [定义登陆页面预设](using/landing-pages/lp-presets.md)
+ 内容管理 {#content-management}
   + [使用 Assets Essentials](using/content-management/assets-essentials.md)
   + [使用 Adobe Stock](using/content-management/stock.md)
   + 使用内容助手{#content-assistant}
      + [内容助手入门](using/content-management/gs-generative.md)
      + [内容生成](using/content-management/generative-content.md)
      + [图像生成](using/content-management/generative-image.md)
   + 个性化 {#personalization}
      + [个性化入门](using/personalization/personalize.md)
      + [个性化上下文](using/personalization/personalization-contexts.md)
      + [个性化语法](using/personalization/personalization-syntax.md)
      + 使用表达式编辑器 {#expression-editor}
         + [关于表达式编辑器](using/personalization/personalization-build-expressions.md)
         + [将属性添加到收藏夹](using/personalization/personalization-favorites.md)
         + [使用已保存的表达式](using/personalization/personalization-library.md)
         + [个性化验证](using/personalization/personalization-validation.md)
      + 辅助函数{#functions}
         + [辅助函数入门](using/personalization/functions/functions.md)
         + [聚合函数](using/personalization/functions/aggregation.md)
         + [算术函数](using/personalization/functions/arithmetic-functions.md)
         + [数组和列表函数](using/personalization/functions/arrays-list.md)
         + [日期函数](using/personalization/functions/dates.md)
         + [布尔和比较函数](using/personalization/functions/operators.md)
         + [辅助程序](using/personalization/functions/helpers.md)
         + [映射函数](using/personalization/functions/maps.md)
         + [数学函数](using/personalization/functions/math.md)
         + [目标函数](using/personalization/functions/objects.md)
         + [字符串函数](using/personalization/functions/string.md)
      + 个性化用例{#personalization-use-cases}
         + [订单状态通知](using/personalization/personalization-use-case.md)
         + [购物车放弃电子邮件](using/personalization/personalization-use-case-helper-functions.md)
   + 动态内容 {#dynamic}
      + [动态内容入门](using/personalization/get-started-dynamic-content.md)
      + [创建条件规则](using/personalization/create-conditions.md)
      + [创建动态内容](using/personalization/dynamic-content.md)
+ 受众、用户档案和身份{#audiences-profiles-identities}
   + 受众 {#audiences}
      + [受众入门](using/audience/about-audiences.md)
      + [生成区段定义](using/audience/creating-a-segment-definition.md)
      + 组合受众{#audience-orchestration}
         + [受众组合入门](using/audience/get-started-audience-orchestration.md)
         + [创建组合工作流](using/audience/create-compositions.md)
         + [使用组合画布](using/audience/composition-canvas.md)
         + [访问和管理受众](using/audience/access-audiences.md)
   + 用户档案{#profiles}
      + [开始使用用户档案](using/audience/get-started-profiles.md)
      + [创建测试用户档案](using/audience/creating-test-profiles.md)
      + [使用计算属性](using/audience/computed-attributes.md)
   + [标识](using/audience/get-started-identity.md)
   + [许可证使用](using/audience/license-usage.md)
+ 跟踪和监测 {#reporting}
   + 实时报告 {#live-report}
      + [实时报告入门](using/reports/live-report.md)
      + [组件列表](using/reports/live-report-components.md)
      + [历程实时报告](using/reports/journey-live-report.md)
      + [营销活动实时报告](using/reports/campaign-live-report.md)
      + [登陆页面实时报告](using/reports/lp-report-live.md)
      + [订阅列表实时报告](using/reports/subscription-report-live.md)
   + 全局报告 {#global-report}
      + [全局报告入门](using/reports/global-report.md)
      + [组件列表](using/reports/global-report-components.md)
      + [历程全局报告](using/reports/journey-global-report.md)
      + [营销活动全局报告](using/reports/campaign-global-report.md)
      + [目标报告](using/reports/objective-report.md)
      + [登陆页面全局报告](using/reports/lp-report-global.md)
      + [订阅列表全局报告](using/reports/subscription-report-global.md)
   + 渠道报表 {#channel-report}
      + [渠道报告入门](using/reports/channel-report-gs.md)
      + [渠道报表](using/reports/channel-report.md)
   + 历程报告 {#reports}
      + [创建历程报告](using/reports/sharing-overview.md)
      + [步骤事件字段列表](using/reports/sharing-field-list.md)
      + 旧版步骤事件字段{#legacy-step-event-fields}
         + [关于旧版字段](using/reports/sharing-legacy-fields.md)
         + [历程字段](using/reports/sharing-journey-fields.md)
         + [常用字段](using/reports/sharing-common-fields.md)
         + [操作执行字段](using/reports/sharing-execution-fields.md)
         + [数据提取字段](using/reports/sharing-fetch-fields.md)
         + [标识字段](using/reports/sharing-identity-fields.md)
      + [查询示例](using/reports/query-examples.md)
   + 可投放性{#deliverability}
      + [可投放性入门](using/reports/deliverability.md)
      + [了解禁止列表](using/reports/suppression-list.md)
   + [警报](using/reports/alerts.md)
   + [使用 Customer Journey Analytics](using/reports/cja-ajo.md)
+ 决策管理{#offer-decisioning}
   + 决策管理入门 {#get-started-decision}
      + [关于决策管理](using/offers/get-started/starting-offer-decisioning.md)
      + [用户界面](using/offers/get-started/user-interface.md)
      + [创建和管理优惠的关键步骤](using/offers/offer-library/key-steps.md)
      + [用例：在电子邮件中插入优惠](using/offers/offers-e2e.md)
   + 创建组件{#create-components}
      + [创建投放位置](using/offers/offer-library/creating-placements.md)
      + [创建决策规则](using/offers/offer-library/creating-decision-rules.md)
      + [创建收藏集限定符](using/offers/offer-library/creating-tags.md)
   + 创建排名 {#rankings}
      + [排名入门](using/offers/ranking/get-started-rankings.md)
      + [排名公式](using/offers/ranking/create-ranking-formulas.md)
      + AI 模型 {#ai-models}
         + [关于 AI 模型](using/offers/ranking/ai-models.md)
         + AI 模型类型 {#ai-model-types}
            + [自动优化模型](using/offers/ranking/auto-optimization-model.md)
            + [个性化优化模型](using/offers/ranking/personalized-optimization-model.md)
         + [创建 AI 模型](using/offers/ranking/create-ranking-strategies.md)
   + 创建和管理优惠 {#managing-offers-in-the-offer-library}
      + 配置优惠 {#configure-offers}
         + [创建个性化优惠](using/offers/offer-library/creating-personalized-offers.md)
         + [添加呈现](using/offers/offer-library/add-representations.md)
         + [添加约束](using/offers/offer-library/add-constraints.md)
      + [创建后备优惠](using/offers/offer-library/creating-fallback-offers.md)
      + [创建收藏集](using/offers/offer-library/creating-collections.md)
   + 创建和管理决策 {#create-manage-activities}
      + [创建决策](using/offers/offer-activities/create-offer-activities.md)
      + [在决策中配置优惠选择](using/offers/offer-activities/configure-offer-selection.md)
      + [创建模拟](using/offers/offer-activities/simulation.md)
   + [使用批量决策](using/offers/batch-delivery.md)
   + 收集事件数据{#collect-event-data}
      + [数据收集入门](using/offers/data-collection/data-collection.md)
      + [创建数据集以收集事件](using/offers/data-collection/create-dataset.md)
      + [配置事件捕获](using/offers/data-collection/schema-requirement.md)
   + 创建决策管理报表 {#create-reports}
      + [使用决策管理事件](using/offers/reports/get-started-events.md)
      + [访问事件 XDM 字段](using/offers/reports/xdm-fields.md)
   + 导出优惠目录{#export-catalog}
      + [导出优惠目录入门](using/offers/export-catalog/get-started-export.md)
      + [访问导出的优惠目录](using/offers/export-catalog/access-dataset.md)
      + [个性化优惠数据集](using/offers/export-catalog/export-offers.md)
      + [决策数据集](using/offers/export-catalog/export-decisions.md)
      + [投放位置数据集](using/offers/export-catalog/export-placements.md)
      + [备用数据集](using/offers/export-catalog/export-fallback.md)
   + API 参考 {#api-reference}
      + [快速入门](using/offers/api-reference/getting-started.md)
      + 使用 API 创建和管理优惠 {#offers-api}
         + 投放位置{#placements}
            + [列出投放位置](using/offers/api-reference/offers-api/placements/placements-list.md)
            + [查找投放位置](using/offers/api-reference/offers-api/placements/lookup.md)
            + [创建投放位置](using/offers/api-reference/offers-api/placements/create.md)
            + [更新投放位置](using/offers/api-reference/offers-api/placements/update.md)
            + [删除投放位置](using/offers/api-reference/offers-api/placements/delete.md)
         + 决策规则 {#decision-rules}
            + [列出决策规则](using/offers/api-reference/offers-api/decision-rules/rules-list.md)
            + [查找决策规则](using/offers/api-reference/offers-api/decision-rules/lookup.md)
            + [创建决策规则](using/offers/api-reference/offers-api/decision-rules/create.md)
            + [更新决策规则](using/offers/api-reference/offers-api/decision-rules/update.md)
            + [删除决策规则](using/offers/api-reference/offers-api/decision-rules/delete.md)
         + 收藏集限定符{#tags}
            + [列出收藏集限定符](using/offers/api-reference/offers-api/tags/tags-list.md)
            + [查找收藏集限定符](using/offers/api-reference/offers-api/tags/lookup.md)
            + [创建收藏集限定符](using/offers/api-reference/offers-api/tags/create.md)
            + [更新收藏集限定符](using/offers/api-reference/offers-api/tags/update.md)
            + [删除收藏集限定符](using/offers/api-reference/offers-api/tags/delete.md)
         + 个性化优惠 {#personalized-offers}
            + [列出个性化优惠](using/offers/api-reference/offers-api/personalized-offers/offers-list.md)
            + [查找个性化优惠](using/offers/api-reference/offers-api/personalized-offers/lookup.md)
            + [创建个性化优惠](using/offers/api-reference/offers-api/personalized-offers/create.md)
            + [更新个性化优惠](using/offers/api-reference/offers-api/personalized-offers/update.md)
            + [删除个性化优惠](using/offers/api-reference/offers-api/personalized-offers/delete.md)
         + 收藏集 {#collections}
            + [列出收藏集](using/offers/api-reference/offers-api/collections/collections-list.md)
            + [查找收藏集](using/offers/api-reference/offers-api/collections/lookup.md)
            + [创建收藏集](using/offers/api-reference/offers-api/collections/create.md)
            + [更新收藏集](using/offers/api-reference/offers-api/collections/update.md)
            + [删除收藏集](using/offers/api-reference/offers-api/collections/delete.md)
         + 后备优惠 {#fallback-offers}
            + [列出后备优惠](using/offers/api-reference/offers-api/fallback-offers/fallback-list.md)
            + [查找后备优惠](using/offers/api-reference/offers-api/fallback-offers/lookup.md)
            + [创建后备优惠](using/offers/api-reference/offers-api/fallback-offers/create.md)
            + [更新后备优惠](using/offers/api-reference/offers-api/fallback-offers/update.md)
            + [删除后备优惠](using/offers/api-reference/offers-api/fallback-offers/delete.md)
      + 使用 API 创建和管理决策 {#activities-api}
         + [列出决策](using/offers/api-reference/activities-api/activities/activities-list.md)
         + [查找决策](using/offers/api-reference/activities-api/activities/lookup.md)
         + [创建决策](using/offers/api-reference/activities-api/activities/create.md)
         + [更新决策](using/offers/api-reference/activities-api/activities/update.md)
         + [删除决策](using/offers/api-reference/activities-api/activities/delete.md)
      + 使用 API 投放优惠 {#offer-delivery-api}
         + [优惠投放 API 入门](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
         + [Decisioning API](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
         + [Edge Decisioning API](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
         + [Batch Decisioning API](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ Experience Decisioning {#experience-decisioning}
   + [Experience Decisioning入门](using/experience-decisioning/gs-experience-decisioning.md)
   + 管理您的决策项目 {#decision-items}
      + [配置物料目录](using/experience-decisioning/catalogs.md)
      + [创建决策项目](using/experience-decisioning/items.md)
      + [管理物料集合](using/experience-decisioning/collections.md)
   + 配置项目的选择 {#selection}
      + [创建决策规则](using/experience-decisioning/rules.md)
      + [创建排名方法](using/experience-decisioning/ranking.md)
   + [创建选择策略](using/experience-decisioning/selection-strategies.md)
   + [创建决策策略](using/experience-decisioning/create-decision.md)
+ 数据管理 {#data-management}
   + [数据管理入门](using/data/gs-data.md)
   + [使用模式](using/data/get-started-schemas.md)
   + Journey Optimizer 数据集 {#datasets}
      + [数据集入门](using/data/get-started-datasets.md)
      + [导出 Journey Optimizer 数据集](using/data/export-datasets.md)
      + [查询示例](using/data/datasets-query-examples.md)
      + [内置架构 >](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=zh_Hans)
   + [查询](using/data/get-started-queries.md)
+ 配置 {#configuration}
   + [Journey Optimizer 配置入门](using/configuration/get-started-configuration.md)
   + [设置渠道表面](using/configuration/channel-surfaces.md)
   + 委派电子邮件子域 {#delegate-subdomains}
      + [子域委派入门](using/configuration/about-subdomain-delegation.md)
      + [委派子域](using/configuration/delegate-subdomain.md)
      + [添加 Google TXT 记录](using/configuration/google-txt.md)
      + [访问和编辑 PTR 记录](using/configuration/ptr-records.md)
      + [创建 IP 池](using/configuration/ip-pools.md)
   + 实施IP预热计划 {#implement-ip-warmup-plan}
      + [IP预热计划入门](using/configuration/ip-warmup-gs.md)
      + [创建IP预热活动](using/configuration/ip-warmup-campaign.md)
      + [创建IP预热计划](using/configuration/ip-warmup-plan.md)
      + [运行IP预热计划](using/configuration/ip-warmup-execution.md)
   + 监测电子邮件地址 {#monitor-reputation}
      + [禁止列表](using/configuration/manage-suppression-list.md)
      + [重试](using/configuration/retries.md)
      + [允许列表](using/configuration/allow-list.md)
   + [使用种子列表](using/configuration/seed-lists.md)
   + [存档支持](using/configuration/archiving-support.md)
   + [更改执行地址](using/configuration/primary-email-addresses.md)
   + [配置频率规则](using/configuration/frequency-rules.md)
   + [实施单页应用程序](using/web/web-spa-implementation.md)
   + 配置历程{#configure-journeys}
      + [关于数据源、事件和操作](using/configuration/about-data-sources-events-actions.md)
      + 与外部系统集成 {#external-systems}
         + [历程与外部系统的集成](using/configuration/external-systems.md)
         + [API 上限](using/configuration/capping.md)
         + [API 限制](using/configuration/throttling.md)
      + 事件配置{#events-journeys}
         + [一般原则](using/event/about-events.md)
         + 配置统一事件{#unitary-events}
            + [统一事件入门](using/event/about-creating.md)
            + [关于 ExperienceEvent Schemas](using/event/experience-event-schema.md)
            + [使用 Adobe Analytics](using/event/about-analytics.md)
         + [配置业务事件](using/event/about-creating-business.md)
         + [用于发送事件的其他步骤](using/event/additional-steps-to-send-events-to-journey.md)
      + 数据源配置{#data-source-journeys}
         + [关于数据源](using/datasource/about-data-sources.md)
         + [配置数据源](using/datasource/configure-data-sources.md)
         + [Adobe Experience Platform 数据源](using/datasource/adobe-experience-platform-data-source.md)
         + [外部数据源](using/datasource/external-data-sources.md)
      + 操作配置{#action-journeys}
         + [关于操作](using/action/action.md)
         + [配置操作](using/action/about-custom-action-configuration.md)
         + [与 Adobe Campaign Standard 集成](using/action/acs-action.md)
         + [与 Adobe Campaign v7/v8 集成](using/action/acc-action.md)
         + [在自定义操作中使用 API 调用响应](using/action/action-response.md)
   + [源](using/start/get-started-sources.md)
+ 访问控制 {#access-control}
   + 访问控制概述 {#privacy}
      + [用户管理入门](using/administration/permissions-overview.md)
      + [内置角色](using/administration/ootb-product-profiles.md)
      + [内置权限](using/administration/ootb-permissions.md)
      + [权限级别](using/administration/high-low-permissions.md)
   + [管理用户和角色](using/administration/permissions.md)
   + [基于属性的访问控制](using/administration/attribute-based-access.md)
   + [对象级访问控制](using/administration/object-based-access.md)
   + [沙盒管理](using/administration/sandboxes.md)
+ 隐私权 {#privacy}
   + [隐私入门](using/privacy/get-started-privacy.md)
   + [隐私请求](using/privacy/requests.md)
   + [对资源的审核操作](using/privacy/audit-logs.md)
   + [执行数据卫生操作](using/privacy/data-hygiene.md)
   + 管理同意 {#consent}
      + [管理选择退出机制](using/privacy/opt-out.md)
      + [使用同意策略](using/action/consent.md)
   + [数据管理](using/action/action-privacy.md)
   + [设置和管理客户托管密钥](using/privacy/cmk.md)