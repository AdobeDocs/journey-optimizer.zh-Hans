---
solution: Journey Optimizer
product: journey optimizer
title: 历程进入与退出标准
description: 通过真实世界的示例和最佳实践，了解如何有效管理用户档案进入和退出历程的时间
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: 登入、退出、标准、历程、用户档案、重新进入、最佳实践
version: Journey Orchestration
exl-id: e879a0f6-b969-4de0-a733-f2880d58d59b
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '1550'
ht-degree: 0%

---

# 使用历程进入和退出条件 {#entry-exit-criteria-guide}

在客户体验编排中，在正确的时间提供正确的信息需要对客户何时进入和退出您的历程进行精确控制。 了解并正确配置登入和退出标准有助于区分成功且富有吸引力的营销活动，以及错过的机会或消息疲劳。

本指南提供了在[!DNL Adobe Journey Optimizer]中管理历程进入和退出标准的实用指南、真实示例和最佳实践。

## 什么是进入和退出标准？ {#what-are-criteria}

**进入条件**&#x200B;确定[客户配置文件](../audience/get-started-profiles.md)有资格进入特定历程的条件。 用户档案可以根据以下条件输入：

* **[客户行为](../event/about-events.md)** — 客户采取的操作会实时触发历程条目，例如进行购买、放弃购物车或打开移动应用程序。

* **[配置文件属性](../audience/get-started-profiles.md)** — 客户特征根据存储在其配置文件中的数据确定资格，如忠诚度级别、位置、年龄或通信偏好设置。

* **[外部事件](../event/about-creating-business.md)** — 同时影响多个客户的业务或环境触发器，例如低库存警报、天气条件或价格变化。

* **[受众成员资格](../audience/about-audiences.md)** — 属于特定受众区段可为高价值客户、非活动用户或新订阅者等组启用定向历程。

**退出条件**&#x200B;定义用户档案离开历程或从中移除的时间和方式：

* **历程完成** — 用户档案在到达所有历程路径的[结尾](end-journey.md)时自动退出，完成设计的体验。

* **成功量度成就** — 用户档案完成[历程目标](success-metrics.md)后退出，例如进行购买或下载应用程序，从而消除不必要的后续通信。

* **基于条件** — 当满足[特定条件](condition-activity.md)时（例如，在设置的期间内不活动或配置文件属性发生更改），配置文件退出。

* **基于事件** — 配置文件在[发生特定事件](../event/about-events.md)时退出，例如订阅取消或产品退货。

* **受众取消资格** — 当个人资料不再符合[目标受众条件](../audience/about-audiences.md)时，将退出，从而确保消息仍然相关。

## 为什么进入和退出标准很重要 {#why-they-matter}

恰当地定义进入和退出标准可以带来巨大的商业价值：

* **相关性**：只有合适的客户才能进入历程，通过在最佳时间定位最合适的受众来提高参与度和转化率。

* **效率**：防止客户停留在不相关的历程中，从而减少不必要的通信、运营成本和客户烦恼。

* **Personalization**：支持根据实时数据和行为动态定制体验，从而创建更有意义的客户交互。

* **合规性**：帮助管理频率封顶和避免过度通信，尊重客户偏好和法规要求，同时维护品牌声誉。

## 历程进入和退出的真实示例 {#real-world-examples}

以下是一些常见情景，它们演示了进入和退出标准在实践中的工作方式：

**新订阅者的欢迎营销活动**

通过自动引导新订阅者了解您的品牌、产品和服务，创建个性化的第一印象。

* **条目**：用户档案在订阅新闻稿时进入历程
* **退出**：用户档案在完成一系列欢迎电子邮件后退出，或者如果用户档案未参与，则在一定时间后退出
* **福利**：确保新订阅者及时上线，同时避免重复发送消息

**放弃的购物车恢复**

通过提醒客户他们遗留的商品并提供完成购买的激励措施，重新获取损失的收入。

* **登入**：如果客户将商品添加到购物车但未在24小时内完成结帐，则他们进入历程
* **退出**：用户档案在完成购买时退出，如果未购买，则在7天后退出
* **好处**：通过及时提醒促进转化，而不会向不感兴趣的客户发送垃圾邮件

**忠诚度计划参与度**

通过独家优势和个性化通信奖励您最有价值的客户，以增强品牌忠诚度并提高存留期价值。

* **登入**：客户在达到特定忠诚度积分阈值后加入历程
* **退出**：配置文件在兑换奖励后退出，或者处于非活动状态60天后退出
* **优惠**：让高价值客户参与个性化优惠并避免沟通疲劳

**产品反馈集合**

通过在投放后的最佳时刻请求反馈，收集有关客户满意度和产品性能的见解。

* **条目**：客户在收到产品交货确认事件后进入历程
* **退出**：用户档案在提交反馈后退出，如果没有响应，则在10天后退出
* **好处**：及时捕获有价值的反馈，而不会因持续请求而烦恼客户

## 如何配置历程进入标准 {#configure-entry}

>[!BEGINSHADEBOX]

**在此处了解您需要了解的有关参加标准的所有信息：**

* **[基于事件的触发器](../event/about-events.md)**：使用“创建配置文件”、“事务已完成”或自定义事件等事件启动历程。 [在](../event/about-creating.md)管理&#x200B;**[!UICONTROL >]**&#x200B;事件&#x200B;**[!UICONTROL 中配置事件]**&#x200B;并定义[事件架构和字段](../event/experience-event-schema.md)。 然后在&#x200B;**[!UICONTROL 历程设计器]**&#x200B;的[事件](using-the-journey-designer.md)调色板中添加该事件。

* **[基于受众的条目](read-audience.md)**： Target以一次性批次或定期计划的方式历程到属于特定受众的用户档案。 [在](../audience/creating-a-segment-definition.md)受众&#x200B;**[!UICONTROL 菜单中创建受众]**，然后添加&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动并[配置计划](journey-properties.md#schedule)。

* **[受众资格条目](audience-qualification-events.md)**：当配置文件符合或实时退出特定受众时触发历程。 定义[流式受众](../audience/about-audiences.md)，从&#x200B;**[!UICONTROL 事件]**&#x200B;调色板添加&#x200B;**[!UICONTROL 受众资格]**&#x200B;事件，然后选择触发器类型。

* **[属性筛选器](condition-activity.md)**：通过使用AND/OR逻辑将事件或受众与配置文件属性和上下文组合在一起，从而优化进入条件。 使用[条件](conditions.md)引用[配置文件属性](../audience/get-started-profiles.md)、事件或[外部数据](../datasource/about-data-sources.md)。

* **[时间窗口和计划](journey-properties.md#schedule)**：设置时间约束以保持历程的及时性和相关性。 在读取受众活动[上配置](read-audience.md)计划，使用[等待活动](wait-activity.md)，并添加[基于时间的条件](conditions.md)以控制计时。

>[!ENDSHADEBOX]

## 如何设置历程退出标准 {#configure-exit}

>[!BEGINSHADEBOX]

**在此处了解关于退出标准需要了解的所有信息：**

* **[历程完成](end-journey.md)**：用户档案在到达最终旅程步骤后自动退出。 设计结束于&#x200B;**[!UICONTROL 结束]**&#x200B;活动的历程路径。

* **[成功量度成就](journey-properties.md#exit-criteria)**：定义成功量度（如购买或订阅）并在完成时退出配置文件。 单击&#x200B;**[!UICONTROL 显示退出条件]**&#x200B;图标，选择&#x200B;**[!UICONTROL 添加退出条件]**，然后选择[事件](../event/about-events.md)或[受众](../audience/about-audiences.md)作为退出触发器。

* **[非活动超时](wait-activity.md)**：如果在设定的时间范围内没有发生参与，则退出用户档案。 对检查上次参与日期的受众使用[退出标准](journey-properties.md#exit-criteria)，对定义的持续时间设置[等待活动](wait-activity.md)，并使用[条件](condition-activity.md)检查活动。

* **[重新进入规则](entry-management.md)**：根据您的营销活动策略，决定用户档案是否可以多次重新进入历程，还是只能再次进入历程一次。 配置历程&#x200B;**[!UICONTROL 属性]**&#x200B;中的&#x200B;**[!UICONTROL 重新进入]**&#x200B;设置以设置等待期，启用强制重新进入，或使用[补充标识符](supplemental-identifier.md)进行特定于上下文的重新进入。

>[!ENDSHADEBOX]

## 详细历程示例 {#journey-examples}

有关包含完整技术细节的分步实施指南，请探索这些文档化的用例：

* **[客户入门历程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)** — 通过受众资格、事件超时和基于目标的退出构建个性化的欢迎体验

* **[放弃的购物车恢复](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)** — 使用事件触发的历程、行动手册和渠道路由恢复损失的销售

* **[重新参与营销活动](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)** — 通过行为定位和付费媒体激活赢回不活动的客户

* **[向订阅者发送消息](message-to-subscribers-uc.md)** — 具有读取受众和个性化内容的目标订阅列表

* **[发送多渠道消息](journeys-uc.md)** — 将电子邮件和推送与反应事件和多路径逻辑相结合

* **[仅在工作日发送电子邮件](weekday-email-uc.md)** — 使用基于时间的条件和等待公式安排通信

>[!TIP]
>
>浏览[历程用例库](jo-use-cases.md)中的所有可用用例，以了解更多模式和实现。 示例包括[增加投放](ramp-up-deliveries-uc.md)、[体验事件模式](exp-event-lookup.md)和[从实时历程中删除配置文件](journey-pause.md#apply-an-exit-criteria-in-a-paused-journey)。

## 管理登入和退出的最佳实践 {#best-practices}

**清除定义**

建立明确的文档和命名惯例，确保您的团队了解用户档案如何在历程中移动：

* 在构建历程以调整营销和分析团队之前，请记录您的进入和退出逻辑
* 创建显示入口点、历程路径和退出条件的流程图
* 清楚地定义业务规则：“用户档案在X发生时或Y天后退出”
* 使用描述性标签：“Exit - Purchase Completed”而不是“Exit 1”
* [标记历程](../start/search-filter-categorize.md#tags)以一致的方式进行报告和筛选

**避免历程重叠**

通过协调跨营销活动的历程策略防止客户混淆和消息冲突：

* [在启动类似历程之前审核活动历程](journey-ui.md)以防止冲突
* 利用[冲突管理](../conflict-prioritization/conflicts.md)和[优先级分数](../conflict-prioritization/priority-scores.md)解决重叠问题并优先处理历程
* 相互补充而不是竞争的设计历程

>[!NOTE]
>
>对于高级方案（例如在用户档案符合较高优先级历程条件时自动删除用户档案），请使用[历程上限和仲裁](../conflict-prioritization/journey-capping.md)，而不是退出标准。

**监视和优化**

持续评估历程表现并根据真实客户行为优化进入和退出标准：

* 使用[历程报告](../reports/journey-global-report-cja.md)跟踪每个历程的进入率、退出率和完成率
* 监视[成功量度](success-metrics.md)：通过成功量度完成而退出与超时的百分比
* 在启动之前，使用各种配置文件方案测试[进入和退出条件](testing-the-journey.md)
* 根据数据进行调整：如果早期退出次数较多，则审查参加标准相关性；如果成功量度完成率较低，则分析内容和时间
* 每季度查看所有活动历程

**遵守频率上限**

通过控制所有历程通信中的消息频率来维护客户信任和参与：

* 设置适当的[重新进入等待期](entry-management.md)或禁用一次性历程的重新进入
* 使用[频率上限规则](../conflict-prioritization/rule-sets.md)防止过度通信
* 监测报告中的频率量度以确保法规遵从性

>[!NOTE]
>
>要管理多个历程中的频率限制和历程进入次数上限，请使用[历程上限和仲裁](../conflict-prioritization/journey-capping.md)和[按渠道进行频率上限](../conflict-prioritization/channel-capping.md)。

## 结论 {#conclusion}

历程进入和退出标准是通过[!DNL Adobe Journey Optimizer]提供个性化、及时和有效的客户体验的基础。 通过精心设计这些条件，营销人员可以提高参与度、减少摩擦并建立更牢固的客户关系。

首先明确映射客户触发器和退出点，彻底测试并监控结果，以不断优化历程编排。

## 相关资源 {#related-resources}

**技术文档**

[用户档案入口管理](entry-management.md) | [历程属性和退出条件](journey-properties.md) | [历程结束方式](end-journey.md) | [补充标识符](supplemental-identifier.md) | [历程设计器](using-the-journey-designer.md)

**教程和示例**

[历程用例](jo-use-cases.md) | [客户入门视频](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding) | [放弃的购物车视频](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart) | [社区博客：登录和退出标准](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/mastering-journey-entry-and-exit-criteria-in-adobe-journey/ba-p/760958)

**相关功能**

[受众资格事件](audience-qualification-events.md) | [成功量度和目标](success-metrics.md) | [冲突管理](../conflict-prioritization/conflicts.md) | [频率封顶](../conflict-prioritization/rule-sets.md) | [测试历程](testing-the-journey.md) | [条件活动](condition-activity.md) | [反应事件](reaction-events.md) | [等待活动](wait-activity.md)
