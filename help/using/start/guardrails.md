---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer护栏和限制
description: 详细了解Journey Optimizer护栏
feature: Guardrails
role: User
level: Intermediate
mini-toc-levels: 1
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
TQID: https://experienceleague.adobe.com/k4DqGogrTZ9QrnqyFGwdgDeUI9ivpOd1iSI0c5comuU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: a6c67b0d-bd3e-4d5d-95a8-882e3709d632
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c3f67a94-f1ff-4f5e-bf6f-bc22405930a3
  - id: cce82f05-fc3c-4af7-85ff-8bba603861a7
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: e240d5e8-8393-4b76-8a3d-9e53a2f7306c
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
  - id: e57d1da4-32c2-4cc6-945c-9feb219156ff
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: c5ecc28ec44a9c608f4fe5011e061cad62d92e2b
workflow-type: tm+mt
source-wordcount: 4226
ht-degree: 0%

---

# 护栏和限制 {#limitations}

在下方，您将找到使用[!DNL Adobe Journey Optimizer]时的护栏和限制。

[Adobe Journey Optimizer产品说明页面](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}列出了授权、产品限制和性能护栏。

>[!CAUTION]
>
>* 实时客户配置文件数据和分段的[护栏](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/guardrails){target="_blank"}也适用于Adobe Journey Optimizer。
>
>* 另请参阅[实时客户资料中的数据摄取护栏](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ingestion/guardrails){target="_blank"}

## 系统和平台 {#system-platform}

### 支持的浏览器 {#browsers}

Adobe [!DNL Journey Optimizer]界面设计为可在最新版本的Google Chrome中以最佳方式工作。 在旧版本或其他浏览器上使用某些功能时可能会遇到问题。

### 数据集护栏 {#datasets-guardrails}

自2025年2月起，在&#x200B;**新沙盒和新组织**&#x200B;中的Journey Optimizer系统生成的数据集中推出生存时间(TTL)护栏，如下所示：

* 90天配置文件存储中的数据，
* 对于数据湖中的数据，为13个月。

此更改将在后续阶段中转出到&#x200B;**现有客户沙盒**。 [了解有关数据集生存时间(TTL)护栏的更多信息](../data/datasets-ttl.md)

## 渠道和消息传递 {#channel-guardrails}

此部分涵盖所有通信渠道(包括电子邮件、短信、入站渠道（Web、应用程序内、基于代码、内容卡）和事务性消息)的护栏。

>[!NOTE]
>
>在极少数情况下，特定区域的临时中断可能会导致从历程中排除有效用户档案，或导致错误标记为退回的邮件。 恢复服务后，重新检查历程日志，验证同意配置文件字段，并根据需要重新发布历程。 在ISP中断的情况下，请参阅[本节](../configuration/manage-suppression-list.md#remove-from-suppression-list)以了解如何从禁止显示列表中删除配置文件。

### 电子邮件护栏 {#message-guardrails}

<!--The following guardrails apply to the [email channel](../../rp_landing_pages/email-landing-page.md):-->

以下护栏适用于[电子邮件渠道](../email/get-started-email.md)：

* 无法使用相同的发送域从[!DNL Adobe Journey Optimizer]和其他产品（例如[!DNL Adobe Campaign]或[!DNL Adobe Marketo Engage]）发送电子邮件。

在设计电子邮件时，系统会检查关键设置并显示警告（建议和最佳实践）和错误（阻止阻止测试或激活的问题）警报。 在[本节](../email/create-email.md#check-email-alerts)中了解有关电子邮件警报和验证要求的更多信息。

#### 历程发布的消息内容大小 {#message-content-size}

发布包含电子邮件的历程时，后端处理后的邮件内容总大小不得超过&#x200B;**2MB**。 在发布期间，系统会通过修补链接、图像并应用转换来自动处理消息内容，这会增加有效负载大小，使其超过创作的内容大小。

>[!CAUTION]
>
>如果最终处理的消息内容超过2MB，则历程发布将失败。 为避免发布失败，请将您的创作消息内容保持在2MB以下（最好在&#x200B;**1MB**&#x200B;以下），以便允许缓冲区300-400KB用于后端处理开销。

**防止发布失败的最佳实践：**

* 将创作的电子邮件内容保持在1MB以下
* 最大程度地减少内容变量的数量
* 在将图像添加到消息之前优化和压缩图像
* 删除未使用的资源和不必要的HTML元素
* 在将历程发布到生产环境之前测试消息大小

如果旅程发布因内容大小而失败，请减少消息内容并重新发布旅程。

### 短信护栏 {#sms-guardrails}

以下护栏适用于[短信渠道](../sms/get-started-sms.md)：

* 可以通过支持的URL包含MMS的媒体文件。 请确保单独上传媒体文件。
* 消息反馈同步当前不适用于MMS。
* 同意管理在MMS的短信渠道级别运行。

### 入站渠道护栏 {#inbound-guardrails}

* 要在[!DNL Journey Optimizer]中使用[基于代码的体验](../code-based/get-started-code-based.md)操作，并交付应用程序可以使用的代码内容有效负载，请按照[此页面](../code-based/code-based-prerequisites.md)上详述的先决条件操作。

* 若要在[!DNL Journey Optimizer]用户界面中访问和创作[网页](../web/get-started-web.md)，请遵循[此页面](../web/web-prerequisites.md)上列出的先决条件。

* 要在使用[!DNL Journey Optimizer]的历程和营销活动中发送应用程序内消息，请遵循[此页面](../in-app/inapp-configuration.md)上列出的投放先决条件。

* 要让Adobe Journey Optimizer正确显示内容卡片，您必须配置[此页面](../content-card/content-card-configuration-prereq.md)上列出的Adobe Experience Platform设置。

* Journey Optimizer支持每秒5,000个入站请求的峰值。 此护栏适用于所有入站请求，这些请求可以来自Journey Optimizer支持的入站渠道（[Web](../web/get-started-web.md)、[应用程序内](../in-app/get-started-in-app.md)、[基于代码的体验](../code-based/get-started-code-based.md)、[内容卡](../../rp_landing_pages/content-card-landing-page.md)）。

  Journey Optimizer入站渠道针对其他渠道中以前可能未参与的新用户档案。 这会增加您的[可参与用户档案](../audience/license-usage.md)总数，如果超出您购买的可参与用户档案的合同数量，则可能会影响成本。

  [Journey Optimizer产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}页面上列出了每个包的许可证指标。 您可以在[许可证使用情况仪表板](../audience/license-usage.md)中检查可参与的配置文件数。

* Journey Optimizer在任何时刻最多支持500个活动入站操作。 如果这些入站操作属于实时营销活动，或者属于实时历程中使用的节点，则会计入这些入站操作。 达到此数量后，您需要停用使用入站操作的旧营销活动或历程，然后才能启动新营销活动。

#### 使用入站渠道管理用户档案 {#profile-management-inbound}

[!DNL Journey Optimizer]入站渠道可以定位假名配置文件，即未经身份验证或尚未知道的配置文件，因为它们以前未在其他渠道上参与。 例如，当基于临时ID（如ECID）定位所有访客或受众时，就是这种情况。

这会增加您的可参与用户档案总数，如果超出您购买的可参与用户档案的合同数量，则可能会带来成本影响。 [Journey Optimizer产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}页面上列出了每个包的许可证指标。 您可以在[许可证使用情况仪表板](../audience/license-usage.md)中检查可参与的配置文件数。

要将可参与的用户档案保持在合理范围内，Adobe建议设置生存时间(TTL)，以便在特定时间范围内未看到或未参与匿名用户档案时，自动从实时客户档案中删除这些用户档案。

>[!NOTE]
>
>请参阅[Experience Platform文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}以了解如何为假名配置文件配置数据过期时间。

Adobe建议将TTL值设置为14天，以匹配当前的Edge配置文件TTL。

### 事务性消息护栏 {#transactional-message-guardrails}

Journey Optimizer在营销活动中支持每秒500条事务性消息的峰值量。

## 内容和Assets {#content-assets}

本节介绍内容创建和管理防护，包括登陆页面、子域和片段。

### 登陆页面护栏 {#lp-guardrails}

以下护栏适用于[登陆页面](../landing-pages/get-started-lp.md)：

* 在单个主页面中只能使用一个&#x200B;**表单**&#x200B;组件。
* 无法在子页面中使用&#x200B;**表单**&#x200B;组件。
* 您无法将预编译标头添加到登陆页面。
* 在设计主登录页面时，您无法选择&#x200B;**自己编写代码**&#x200B;选项。

### 子域护栏 {#subdomain-guardrails}

[此页面](../configuration/delegate-subdomain.md#guardrails)详细介绍了适用于Journey Optimizer中子域委派的护栏和限制。

### 片段护栏 {#fragments-guardrails}

以下护栏适用于[片段](../content-management/fragments.md)：

* 要创建、编辑、存档和发布片段，您需要具有&#x200B;**[!DNL Content Library Manager]**&#x200B;产品配置文件中包含的&#x200B;**[!DNL Manage library items]**&#x200B;和&#x200B;**[发布片段]**&#x200B;权限。 [了解详情](../administration/ootb-product-profiles.md#content-library-manager)
* 可视化片段仅适用于电子邮件渠道。
* 表达式片段不适用于应用程序内渠道。
* 可视片段不能超过100KB。 表达式片段不能超过200KB。
* 要在历程或营销策划中使用片段，该片段必须处于&#x200B;**实时**&#x200B;状态。
* 片段中不支持[上下文属性](../personalization/personalization-build-expressions.md)。
* 可视片段在使用主题和手动样式设置模式之间不交叉兼容。 要在要在要应用主题的内容中使用片段，必须在使用主题模式下创建此片段。 [了解有关主题的更多信息](../email/apply-email-themes.md)
* 在历程或营销活动中启用跟踪时，如果您向片段添加链接，并且在消息中使用此片段，则会跟踪这些链接，例如消息中包含的所有其他链接。 [了解有关链接和跟踪的更多信息](../email/message-tracking.md)

## Audiences &amp; Profiles {#audiences-profiles}

本节介绍用于受众管理、配置文件处理和可参与配置文件注意事项的护栏。

### 受众和配置文件护栏 {#audience}

* 您最多可以在给定沙盒中发布10个受众合成。 如果您已达到此阈值，则需要删除合成以释放空间并发布新合成。

  在[此页面](../audience/get-started-audience-orchestration.md)上了解有关受众构图的更多信息。

* 摄取数据时，电子邮件区分大小写。 这意味着可以创建重复的用户档案（例如，John.Greene@luma.com的一个用户档案，john.greene@luma.com的另一个用户档案），并在您的[!DNL Journey Optimizer]历程和营销活动中定位相应的收件人时使用。

* 将假名用户档案（未经身份验证的访客）与入站渠道进行定位时，请考虑设置自动删除用户档案的生存时间(TTL)，以管理可参与的用户档案计数和相关成本。 [了解详情](#profile-management-inbound)

## 决策管理 {#decision-management}

### 决策和决策管理护栏 {#decisioning-guardrails}

有关使用决策或决策管理时要牢记的护栏和限制，请参阅以下决策和决策管理部分：

* [决策护栏和限制](../experience-decisioning/decisioning-guardrails.md)
* [决策管理护栏和限制](../offers/decision-management-guardrails.md)

## 历程 {#journeys-guardrails}

本节介绍历程的护栏和限制，包括常规历程限制、历程组件（操作、事件、数据源）、历程活动以及自定义操作和表达式编辑器等特定功能。

### 常规历程护栏 {#journeys-guardrails-journeys}

* 历程中的活动数限制为50个。 活动数显示在历程画布的左上部。 这有助于提高可读性、QA和疑难解答。
* 默认情况下，同一时间的实时/暂停/练习历程数限制为100。  当前历程数显示在历程画布上方。
* 当您发布历程时，我们会自动进行扩展和调整，以确保最大吞吐量和稳定性。 当您一次接近100个实时历程的里程碑时，您将在UI中看到有关此成就的通知。 如果您看到此通知，并且需要将您的历程一次扩展到100个实时历程之外，请为客户关怀创建票证，我们将帮助您实现目标。
* 在历程中使用受众资格时，该受众资格活动可能最多需要10分钟才能激活，并侦听进入或退出受众的用户档案。
* 用户档案的历程实例的最大大小为1MB。 在历程执行过程中收集的所有数据都存储在该历程实例中。 因此，来自传入事件的数据、从Adobe Experience Platform检索的用户档案信息、自定义操作响应等将存储在历程实例中，并影响历程大小。 当历程以事件开始时，建议限制该事件有效负载的最大大小（例如：小于800 KB）以避免在历程执行中的一些活动后达到该限制。 当达到该限制时，用户档案处于错误状态并将从历程中排除。
* 对于每个用户档案和历程版本，历程运行时在处理一个挂起事件时保持内部队列最多10个。 如果达到此限制，则会以`maxInstanceStackEventsReached`原因丢弃其他事件，直到栈栈耗尽为止。 查看由于受阻的历程实例[&#128279;](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached)而丢弃的个事件。
* 除了历程活动中使用的超时之外，还有全局历程超时，此超时未显示在界面中，无法更改。 此全局超时在个人进入历程91天后停止个人进度。 [阅读更多](../building-journeys/journey-properties.md#global_timeout)


#### 有效负载大小验证历程 {#journey-payload-size}

在保存或发布旅程时，Journey Optimizer会验证旅程有效负载的总大小，以保持稳定性和性能。

**默认配置**

* **默认最大请求大小**： 2 MB （2,000,000字节）。 某些组织可能具有Adobe配置的自定义限制。
* **警告阈值**：最大限制的90%。
* **错误阈值**：最大限制的100%。 保存或发布被阻止，请求返回&#x200B;**HTTP 413请求实体太大**。

**用户体验方案**

* **有效负载&lt;限制的90%**：历程保存并发布成功。 不显示警告或错误。
* **有效负载为限制的90-99%**：历程保存并发布成功，并警告要优化。 警告消息： **警告**：历程有效负载大小接近限制。 最大节点：“[NodeName]”（类型：“[NodeType]”，大小： [N]字节）。
* **有效负载>=限制的100%**：历程保存或发布被阻止并出现错误。 错误消息： **错误**：历程的负载大小超出限制。 最大节点：“[NodeName]”（类型：“[NodeType]”，大小： [N]字节）。

**错误响应详细信息**

如果请求超出了允许的最大大小，则响应将包含&#x200B;**请求实体太大**。 历程有效负载超过了允许的大小上限。 查看错误详细信息并优化您的历程。

**故障排除和建议**

* 查看警告或错误中突出显示的最大节点。
* 简化条件，减少数据映射，并删除不必要的步骤或参数。
* 如果需要，请考虑将历程拆分为较小的历程。
* 如果您认为贵组织需要更高的限制，请联系您的Adobe代表。

要在发布之前监视历程的当前有效负载大小，请使用历程属性面板中的&#x200B;**[!UICONTROL 当前历程有效负载大小]**&#x200B;指示器。 [了解如何检查历程有效负载的大小](../building-journeys/journey-properties.md#journey-payload-size)

### 选择单一历程的包限制 {#select-package-limitations}

>[!NOTE]
>
>这些限制不适用于具有&#x200B;**Select**&#x200B;包的读取受众或业务事件历程。 如果您需要具有多个操作、条件或等待活动的更复杂的历程逻辑，请考虑升级您的许可证包或在适用的情况下使用读取受众历程。

对于使用&#x200B;**Select**&#x200B;许可证包的客户，以下附加限制尤其适用于单一历程、以事件或受众资格开始的历程：

* **SELECT包：单一历程(ERR_PKG_SELECT_8)**&#x200B;中只允许一个操作：单一历程只能包含一个操作活动。 您无法在同一历程中添加多个电子邮件、推送、短信或其他操作活动。

* **SELECT包：单一历程(ERR_PKG_SELECT_7)中不允许条件**：单一历程中不能使用条件活动。 历程必须遵循单个线性路径，且不含分支逻辑。

* **SELECT包：单一历程(ERR_PKG_SELECT_6)中不允许等待**：无法将等待活动添加到单一历程。 操作必须立即执行且无延迟。

* **SELECT包：从节点过渡超时/错误必须仅指向结束节点(ERR_PKG_SELECT_2)**：如果为操作（如电子邮件操作）配置超时或错误过渡，这些路径必须直接指向结束节点。 他们无法连接到历程中的其他活动或操作。


### 常规操作 {#general-actions-g}

以下护栏适用于历程中的[操作](../building-journeys/about-journey-activities.md)：

* 如果出现错误，将系统地执行三次重试。 您无法根据收到的错误消息调整重试次数。 对HTTP 401、403和404以外的所有HTTP错误执行重试。
* 内置&#x200B;**反应**&#x200B;事件允许您对开箱即用的操作做出反应。 在[此页面](../building-journeys/reaction-events.md)上了解详情。 如果要对通过自定义操作发送的消息做出反应，则必须配置专用事件。
* 不能同时设置两个操作，必须逐一添加。
* 对于历程[&#128279;](../building-journeys/publish-journey.md#journey-create-new-version)的所有活动版本，同一历程中不能同时存在多个配置文件。 如果启用了重新进入，则用户档案可以重新进入历程，但只有在完全退出该历程的上一个实例后才能重新进入历程。 [阅读更多](../building-journeys/end-journey.md)

### 历程版本 {#journey-versions-g}

以下护栏适用于[历程版本](../start/user-interface.md)：

* v1中以事件活动开始的历程，在后续版本中无法以事件之外的其他内容开始。 您无法通过&#x200B;**受众资格**&#x200B;事件开始历程。
* v1中以&#x200B;**受众资格**&#x200B;活动开始的历程在后续版本中必须始终以&#x200B;**受众资格**&#x200B;开始。
* 无法在新版本中更改在&#x200B;**受众资格** （第一个节点）中选择的受众和命名空间。
* 在所有历程版本中，重新进入规则必须相同。
* 以&#x200B;**读取受众**&#x200B;开始的历程在后续版本中无法以其他事件开始。
* 您无法创建具有增量读取的读取受众历程的新版本。 您必须复制历程。

### 自定义操作 {#custom-actions-g}

以下护栏适用于历程中的[自定义操作](../action/action.md)：

* 为所有自定义操作、每个主机和每个沙盒定义了1分钟内300,000次调用的上限。 “每台主机”限制适用于域级别（例如，example.com）。 对于响应时间小于0.75秒的端点，此上限强制作为每个沙盒和每个端点的滑动窗口。 对于响应时间大于0.75秒的端点，每30秒150,000次调用的单独限制（也是滑动窗口）适用。 请参阅[此页面](../action/about-custom-action-configuration.md)。 此限制是根据客户使用情况设置的，用于保护自定义操作所定位的外部端点。 如果需要，您可以通过我们的上限/限制API定义更大的上限或限制来覆盖此设置。 查看[此页面](../configuration/external-systems.md)。
* 自定义操作URL不支持动态参数。
* 支持POST、PUT和GET调用方法
* 查询参数或标头的名称不得以“。”开头 或“$”
* 不允许使用IP地址
* 不允许在URL和API中使用内部Adobe地址(`.adobe.*`)。
* 无法删除内置自定义操作。
* 仅当使用请求或响应负载时，自定义操作才支持JSON格式。 查看[此页面](../action/about-custom-action-configuration.md#custom-actions-limitations)。
* 在使用自定义操作选择要定位的端点时，请确保：

   * 此端点可以使用[限制API](../configuration/throttling.md)或[限制API](../configuration/capping.md)的配置来支持历程的吞吐量。 请注意，限制配置不能低于200 TPS。 任何目标端点必须支持至少200个TPS。
   * 此端点需要尽可能短的响应时间。 根据预期吞吐量，高响应时间可能会影响实际吞吐量。

### 活动 {#events-g}

以下护栏适用于您的历程中的[事件](../event/about-events.md)：

* Journey Optimizer支持所有沙盒的峰值速度为每秒5000个入站旅程事件。 在此页面[&#128279;](../event/about-events.md#event-thoughput)上了解有关此限制的更多信息。
* 事件触发的历程可能最多需要5分钟来处理历程中的第一个操作。
* 对于系统生成的事件，必须先在Journey Optimizer中配置用于启动客户历程的流数据，才能获取唯一的编排ID。 此编排ID必须附加到传入Adobe Experience Platform的流有效负载中。 此限制不适用于基于规则的事件。
* 业务事件不能与单一事件或受众资格活动结合使用。
* 单一历程（从事件或受众资格开始）包含护栏，可防止同一事件多次错误触发历程。 默认情况下，重新进入用户档案会被暂时阻止5分钟。 例如，如果某个事件在12:01触发特定用户档案的历程，而另一个事件在12:03到达（无论是同一事件还是其他事件触发同一历程），则此用户档案的历程将不会再次开始。
* Journey Optimizer要求将事件流式传输到数据收集核心服务(DCCS)才能触发旅程。 批量摄取的事件、通过&#x200B;**查询服务**&#x200B;插入的事件，或来自Journey Optimizer内部数据集（消息反馈、电子邮件跟踪等）的事件 无法用于触发历程。 对于无法获取流式传输的事件的用例，必须基于这些事件构建受众，然后改用&#x200B;**读取受众**&#x200B;活动。 从技术上讲，可以使用受众资格，但不建议使用，因为它可能会根据所使用的操作导致下游挑战。

### 数据源 {#data-sources-g}

以下护栏适用于历程中的[数据源](../datasource/about-data-sources.md)：

* 可在客户历程中利用外部数据源实时查找外部数据。 这些源必须可通过REST API使用，支持JSON，并能够处理大量请求。
* 不允许在URL和API中使用内部Adobe地址(`.adobe.*`)。

>[!NOTE]
>
>由于现在支持响应，因此您应该对外部数据源用例使用自定义操作而不是数据源。

### 历程和配置文件创建 {#journeys-limitation-profile-creation}

在Adobe Experience Platform中创建/更新基于API的配置文件存在延迟。 在每秒请求量(RPS)为20K的情况下，延迟方面的服务级别目标(SLT)从摄取到统一配置文件的第95%的请求的延迟小于1分钟。

如果在创建用户档案的同时触发了历程，并立即检查/检索用户档案服务中的信息，则该历程可能无法正常工作。

您可以从以下两种解决方案中选择一种：

* 在第一个事件后添加等待活动，以便给Adobe Experience Platform提供向配置文件服务执行摄取所需的时间。

* 设置不会立即利用用户档案的历程。 例如，如果历程旨在确认帐户创建，则体验事件可能包含发送第一条确认消息（名字、姓氏、电子邮件地址等）所需的信息。


### 补充标识符 {#supplemental}

特定护栏适用于在历程中使用补充标识符。 它们列在[此页面](../building-journeys/supplemental-identifier.md#guardrails)中。

### 表达式编辑器 {#expression-editor}

以下护栏适用于[历程表达式编辑器](../building-journeys/expression/expressionadvanced.md)：

* 以读取受众、受众资格或业务事件活动开始的历程中，无法使用体验事件字段组。 您必须创建一个新受众，并在历程中使用`inaudience`条件。
* 不能在表达式编辑器中使用`timeSeriesEvents`特性。 要在配置文件级别访问体验事件，请基于`XDM ExperienceEvent`架构创建新的字段组。
  <!--* A single condition expression cannot contain more than **200 values** in an `in` list (e.g. `field in ["val1","val2",...]`). Expressions exceeding this limit will fail validation. To work around this limit, split the values across multiple conditions combined with `or`.-->

### 历程活动 {#activities}

#### 受众资格活动 {#audience-qualif-g}

以下护栏适用于[受众资格](../building-journeys/audience-qualification-events.md)历程活动：

* 受众资格活动不能用于Adobe Campaign活动。
* 受众资格历程不支持补充标识符。

在[本节](../building-journeys/entry-management.md#journey-processing-rate)中了解有关历程处理速率和吞吐量限制的更多信息。

#### 营销活动 {#ac-g}

以下护栏适用于&#x200B;**[!UICONTROL Campaign v7/v8]**&#x200B;和&#x200B;**[!UICONTROL Campaign Standard]**&#x200B;活动：

* Adobe Campaign活动不能与读取受众或受众资格活动一起使用。
* **[!UICONTROL Campaign Standard]**&#x200B;活动不能与其他渠道活动一起使用：卡片、基于代码的体验、电子邮件、推送、短信、应用程序内消息、Web。
* **[!UICONTROL Campaign v7/v8]**&#x200B;活动可与同一历程中的本机渠道活动一起使用。

#### 应用程序内活动 {#in-app-activity-limitations}

以下护栏适用于&#x200B;**[!UICONTROL 应用程序内消息]**&#x200B;操作。 在[此页面](../in-app/create-in-app.md)上了解有关应用程序内消息的更多信息。

* 此功能目前不适用于医疗保健客户。

* Personalization只能包含配置文件属性。

* 应用程序内活动不能与&#x200B;**[!UICONTROL Campaign Standard]**&#x200B;活动一起使用。

* 应用程序内显示绑定到历程生命周期，这意味着当历程为用户档案结束时，该历程中的所有应用程序内消息将不再显示该用户档案。  因此，无法直接从历程活动停止应用程序内消息。 相反，您必须结束整个历程以停止向用户档案显示应用程序内消息。

* 在测试模式下，应用程序内显示取决于历程的有效期。 为避免历程在测试期间过早结束，请调整&#x200B;**[!UICONTROL 等待]**&#x200B;活动的&#x200B;**[!UICONTROL 等待时间]**&#x200B;值。

* **[!UICONTROL 反应]**&#x200B;活动无法用于响应应用程序内打开或点击。

* 从用户配置文件到达画布中的应用程序内活动到他们开始看到应用程序内消息之间，可能会发生激活延迟。

* 应用程序内消息的内容大小限制为2Mb。 包含大图像可能会妨碍发布流程。

#### 跳转活动 {#jump-g}

特定护栏适用于&#x200B;**[!UICONTROL 跳转]**&#x200B;活动。 它们列在[此页面](../building-journeys/jump.md#jump-limitations)上。

#### 读取受众活动 {#read-segment-g}

以下护栏适用于[读取受众](../building-journeys/read-audience.md)历程活动：

* 流式处理受众始终是最新的，但在检索时不会计算批量受众。 它们每天仅在每日批量评估时间中进行评估。
* 在历程条目中，配置文件使用批量受众快照中的属性值。 但是，当配置文件达到&#x200B;**等待**&#x200B;活动时，历程将通过从统一配置文件服务(UPS)获取最新数据来自动刷新配置文件属性。 这意味着在历程执行期间，配置文件属性可能会发生更改。
* **读取受众**&#x200B;活动不能与Adobe Campaign活动一起使用。
* **读取受众**&#x200B;活动只能用作历程中的第一个活动，或用作业务活动活动之后。
* 历程只能有一个&#x200B;**读取受众**&#x200B;活动。
* **读取受众**&#x200B;活动只能针对每个历程的一个受众。 如果需要多个受众，请先将它们合并到单个受众中。 [了解如何使用组合工作流组合受众](../audience/get-started-audience-orchestration.md)。
* 每个组织最多可以跨所有沙盒和历程同时运行五个&#x200B;**读取受众**&#x200B;实例（计划或业务事件触发）。 避免同时启动超过5个包含&#x200B;**读取受众**&#x200B;的历程；将其相隔5到10分钟。 在[本节](../building-journeys/entry-management.md#journey-processing-rate)中了解有关历程处理率的更多信息。
* 沙盒吞吐量：系统管理每个沙盒的处理，在所有&#x200B;**读取受众**&#x200B;活动中每秒最多共享20,000个配置文件。 单个活动可配置为每秒有500到20,000个配置文件。 如果达到沙盒限制，作业可能会排入队列。
* 作业处理超时： **无法在12小时内处理的读取受众**&#x200B;作业将被自动清理并且不会执行。
* 默认情况下，在检索导出作业时对受众触发的历程（从&#x200B;**读取受众**&#x200B;或&#x200B;**业务事件**&#x200B;开始）应用重试。 如果在创建导出作业期间发生错误，将每10mn重试一次，最长为1小时。 之后，我们将它视为失败。 因此，这些类型的历程可以在计划时间后最多1小时执行。
* 对于使用补充ID的历程，每个历程实例的读取受众活动的读取率限制为每秒500个配置文件上限。

另请参阅读取受众活动的[推荐和配置](../building-journeys/read-audience.md#must-read)。

#### 更新用户档案活动 {#update-profile-g}

特定护栏适用于&#x200B;**[!UICONTROL 更新配置文件]**&#x200B;活动。 它们列在[此页面](../building-journeys/update-profiles.md)上。

## 活动编排 {#campaign-orchestration}

### Campaign编排护栏 {#orchestration-guardrails}

有关使用Campaign Orchestration时要牢记的护栏和限制，请参阅此部分： [护栏和限制](../orchestrated/guardrails.md)。
