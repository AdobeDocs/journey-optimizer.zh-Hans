---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
hide: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 3902d92e0306ea23fa877dca64165b14c4e3f9dd
workflow-type: tm+mt
source-wordcount: 1960
ht-degree: 10%

---


# 预发行说明 {#e-release-notes}

Adobe Journey Optimizer不断提供新功能、现有功能的增强以及错误修复。 所有更改会在每月末整合到[发行说明](release-notes.md)中。

## 2026年6月预发行说明 {#june-26-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。 一旦更改发布到生产环境，链接、屏幕和更新的文档就会发布。 虽然大多数更改将在发布日期交付，但其中一些更改可能会稍后推出 — 有关详细信息，请参阅为每个条目列出的可用性日期。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发行日期**： 2026年6月16日至17日


### 历程 {#june-26-journeys}

此版本中的历程将包括以下功能和改进。

<table>
<thead>
<tr>
<th><strong>历程路径优化 — 定位</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用新的<strong>优化节点</strong>来定位特定受众，以确定满足以业务为中心的KPI的最佳途径。</p>
<p>利用此工具，可制定更高效的营销活动，从而更可能在1:1级别引起共鸣，改进客户的营销个性化工作，并提高关键客户参与KPI（如转化率和收入）。</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14720">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程仲裁 — 公式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用<strong>公式</strong>根据客户个人资料属性和上下文因素自动提升<strong>历程优先级分数</strong>，确保客户进入最相关的历程。</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14719">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

* **增加了实时历程限制和新护栏** — 您现在最多可以有&#x200B;**200个活动历程**，比之前的100个限制有所增加。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14826">链接到DOCAC JIRA任务</a>

* **历程标题中的开始和结束日期** — 在实时历程中配置开始和/或结束日期时，它们现在显示在实时状态徽章旁边的&#x200B;**历程标题**中。显示的标签会根据每个日期即将到来还是已经过去进行调整。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14702">链接到DOCAC JIRA任务</a>

* **直接停止或关闭暂停的历程** — 您现在可以&#x200B;**直接从**&#x200B;暂停&#x200B;**状态停止历程或将其关闭到新入口**。以前，暂停的历程必须恢复为实时状态，然后才能停止或关闭。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14229">链接到DOCAC JIRA任务</a>

### 编排的营销活动 {#june-26-oc}

此版本中的编排营销活动即将推出以下功能和改进。

<table>
<thead>
<tr>
<th><strong>在编排的营销活动中加载文件活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，编排的营销活动支持直接将<strong>CSV或TXT文件</strong>加载到营销活动画布中作为定向受众，而无需先将文件摄取到Adobe Experience Platform。 文件数据在执行时消耗，并且不作为Adobe Experience Platform数据集保留。 在文件设置过程中，可以定义列映射、数据类型、NULL处理和每列错误策略。 这支持临时发送或合作伙伴列表营销活动，在这些活动中构建完整摄取管道不切实际。</p>
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14704">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>对精心安排的活动的无讯息工作时间支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将<strong>无讯息小时数</strong>应用于编排的营销活动。 无讯息小时允许您定义<strong>基于时间的排除</strong>，以防止在特定期间发送消息，从而帮助您跨活动编排用例尊重客户偏好和合规性要求。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14054">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

* **在编排的营销活动中基于循环的关系数据个性化** — 个性化编辑器现在支持&#x200B;**循环块**，该块可在关系收藏集（如订单、帐户或预订）上进行迭代，并在单个电子邮件或短信中为每个记录呈现一个内容块。收藏集是使用个性化令牌通过数据选取器配置的，无需编写表达式。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14703">链接到DOCAC JIRA任务</a>

* **为每个收件人和营销活动个性化电子邮件发件人详细信息** — 编排的营销活动现在支持使用配置文件属性或关系数据对&#x200B;**电子邮件标题字段**进行个性化，包括发件人姓名、发件人地址和回复。这允许发件人详细信息反映每个收件人的相关顾问、位置或分支，而不是通过单个公司地址路由所有发送。可以在渠道级别设置标题值，并使用上下文数据覆盖每个营销活动的标题值，以实现更精确的控制。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13761">链接到DOCAC JIRA任务</a>

* **协调营销活动中的目标维度简化** — 活动&#x200B;**目标维度**现在显示在工作流画布上，以便您查看渠道活动使用了哪个维度。多实体分段流程更简单，因为您不再需要单独的“更改维度”活动。此外，您现在可以明确选择是在用户档案级别还是在辅助维度级别发送消息。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13554">链接到DOCAC JIRA任务</a>

* **覆盖营销活动中的默认执行字段** — 以前在历程级别可用，现在可覆盖在营销活动参数中为电子邮件、短信和WhatsApp投放全局设置的默认&#x200B;**执行字段**。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14718">链接到DOCAC JIRA任务</a>

### 决策 {#june-26-decisioning}

在此版本中，Decisioning即将提供以下功能。

<table>
<thead>
<tr>
<th><strong>在Decisioning中使用Adobe Experience Manager内容片段</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在Decisioning中将<strong>Adobe Experience Manager内容片段</strong>映射到<strong>决策项</strong>，并在决策策略中利用它们以在正确的时间将正确的片段提供给正确的客户。</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14885">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

### 电子邮件渠道 {#june-26-email}

此版本中的电子邮件渠道即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>高级组件 — 布局（超级组件）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Email Designer现在包括现成的布局组件</strong>的<strong>库，例如页眉、产品卡（1、2或3列）、信息块和页脚，您可以将这些组件直接拖放到电子邮件画布中。 每个组件都预先配置了可编辑的属性（图像、标题、文本、按钮、链接），并且可以通过WYSIWYG界面完全自定义，从而加快电子邮件创建速度，而无需您从头开始构建结构。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14877">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件Designer中的内容签入</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在允许用户直接在Email Designer界面中验证其<strong>电子邮件内容质量</strong>，包括可读性、有效性和内容一致性。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14870">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>启用电子邮件大小缩减</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>这个新选项允许<strong>在电子邮件中去除不必要的空格、注释和冗余代码，从而缩小HTML</strong>的大小，而无需更改电子邮件的外观。 这有助于提高可投放性（某些电子邮件提供商拒绝或标记超大电子邮件），并可加快收件人的加载时间。</p>
<p>发布日期：2026年6月10日</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14777">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

* 片段中的&#x200B;**文本模式支持** — 为了支持基于文本的电子邮件工作流，您现在可以创建和管理&#x200B;**文本版本**的可视化片段，以便在包含该片段的纯文本版本的电子邮件中实现最佳使用。使用在当前版本之前创建的片段时，片段文本版本可能会错误地呈现 — 在电子邮件Designer中以及在发送给收件人的最终电子邮件中。为了对较旧的片段获得最佳结果，请编辑、保存并重新发布每个片段。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14204">链接到DOCAC JIRA任务</a>

* **更新了面向客户的方案中的批量发送吞吐量基准** - Adobe Journey Optimizer的&#x200B;**批量发送吞吐量基准**已更新，以反映多个个性化方案中的生产级性能 — 从基本发送到带条件逻辑的复杂动态内容。产品文档中现在提供了更新的指标，以帮助客户准确规划其报文传送量。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14816">链接到DOCAC JIRA任务</a>

* **自定义子域的反馈循环OTP流程** — 反馈循环(FBL)自定义子域配置流程已得到改进，直接在产品UI中显示Yahoo发件人中心&#x200B;**一次性密码(OTP)**。用户现在可以自动检索和显示Yahoo发件人中心域所有权验证期间生成的OTP。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14815">链接到DOCAC JIRA任务</a>

### 移动消息（短信、彩信、RCS和LINE） {#june-26-mobile}

此版本中的移动消息传送功能即将实现以下改进。

* 短信报告的&#x200B;**唯一点击次数** — 为短信报告引入了一个新的&#x200B;**唯一点击次数**模块，为当前可用于电子邮件报告的短信引入了相同级别的粒度性能跟踪。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14895">链接到DOCAC JIRA任务</a>

* **LINE频道 — 创作更改** - LINE频道UI已升级，具有高级消息创作功能。此版本引入了对&#x200B;**多种消息格式**的支持，包括文本、图像、图像映射、轮播和Flex （JSON编辑器），以及实时设备预览。用户现在可以管理最多五条已排序消息的分组消息（具有添加、删除和重新排序控件），并利用集成的个性化编辑器进行验证的动态消息传送。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14869">链接到DOCAC JIRA任务</a>

* **Journey Optimizer转售 — 显示使用情况量度** — 对于直接通过Adobe Journey Optimizer购买短信的客户，引入了新的&#x200B;**短信使用情况仪表板**。您现在可以查看和跟踪最近90天的消息发送指标，并按发起的移动设备(MO)和终止的移动设备(MT)消息进行分类。此数据也可以通过CSV下载，从而更好地显示和控制短信支出。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14345">链接到DOCAC JIRA任务</a>

### 内容和集成 {#june-26-content}

此版本中的内容管理和集成即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager的内容片段</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此版本引入了多项增强功能，使<strong>Adobe Experience Manager内容片段</strong>在Journey Optimizer创作工作流中更可用、更可管理，并且更易于生产：</p>
<ul>
<li>Journey Optimizer现在支持从多个Adobe Experience Manager配置中提取内容片段，包括创作层、发布层和经过身份验证的发布层。</li>
<li>选择片段后，其上下文会在整个消息中保留，从而使作者能够跨内容块重用片段字段而无需重新选择。</li>
<li>Journey Optimizer中引入了新的专用内容片段列表页面，以改进生命周期管理；用户可以识别不同步的片段并触发手动同步以保持最新。</li>
<li>区域设置和变体支持现在允许营销人员更刻意地使用同一内容片段的替代版本。</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14686">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager存储库配置</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以灵活地了解Adobe Journey Optimizer如何访问Adobe Experience Manager内容。 此版本引入了为历程和营销活动中使用的内容片段<strong>切换源存储库</strong>的功能。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14684">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

* **本机Adobe Experience Manager内容片段(Managed Services)集成** — 现在与&#x200B;**Managed Services**兼容，您可以直接在Journey Optimizer中查看、访问和使用Adobe Experience Manager内容片段进行个性化。只需在配置设置中添加Adobe Experience Manager Managed Services存储库URL作为一次性设置即可。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14821">链接到DOCAC JIRA任务</a>

* **AI助手与Adobe Experience Manager Asset Essentials集成** - AI助手现在在生成电子邮件、网页和推送通知时，直接从您的Adobe Experience Manager Assets中自动提取&#x200B;**品牌批准的图像**。这消除了手动搜索Assets或依赖通用AI回退的需要，确保每个视觉效果都非常准确且符合品牌规范。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14761">链接到DOCAC JIRA任务</a>

### 自定义渠道 {#june-26-channels}

此版本中的渠道即将提供以下功能。

<table>
<thead>
<tr>
<th><strong>自定义出站频道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在引入了<strong>自定义渠道</strong>，这是一项新功能，可让管理员通过<strong>无代码渠道生成器</strong>，将任何基于HTTP的出站消息渠道（如WeChat、Kakao Talk、Messenger或专有提供商）直接引入AJO。 配置完毕后，即可跨营销活动、历程和编排的营销活动使用自定义渠道，并具有与本机渠道相同的完整功能集：使用表达式编辑器进行个性化、内容实验、预览和验证、现成的报告以及同意和治理实施。 这填补了以前由自定义操作填补的空白，这些操作仅限于历程且缺乏专门的内容创作。</p>
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11381">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

### 报表 {#june-26-reporting}

此版本中的报表即将进行以下改进。

* **排除电子邮件和短信报告的机器人点击次数** — 为了更准确地查看实际客户参与情况，现在提供了跨历程、营销活动和渠道报告的新估计指标。 这些量度有助于从报表数据中过滤掉非人工交互(NHI)和机器人点击：
   * 预计点击次数：删除识别的机器人和非人类流量后计算的总点击次数。
   * 预计CTR：相对于投放总数的预计点击次数。
   * 仅电子邮件的预计CTOR：相对于预计打开次数的预计点击次数。

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14354">链接到DOCAC JIRA任务</a>

### 配置 {#june-26-configuration}

此版本中的配置和管理功能将进行以下改进。

* AJO登陆页面的&#x200B;**Web应用程序防火墙(WAF) IP白名单** - Adobe Journey Optimizer现在支持登陆页面的&#x200B;**Web应用程序防火墙(WAF) IP白名单**，使组织能够强制要求所有传入请求仅通过其配置的WAF基础架构进行路由。借助这项增强功能，客户可以将AJO配置为拒绝任何绕过WAF层的直接请求，从而确保Imperva等工具中定义的安全策略得到一致应用。此功能增强了具有严格网络访问要求的企业的安全状况，使它们能够完全控制流向AJO托管的登陆页面的流量。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14814">链接到DOCAC JIRA任务</a>

* **数据集从流模式移动到批处理模式** - AJO消息反馈事件数据集正在从流模式过渡到&#x200B;**批处理摄取模式**。此更改可确保数据摄取不超过流摄取限制。如果您在Customer Journey Analytics报表中使用此数据集或对其运行查询，预计今后数据延迟最多将增加2小时。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14771">链接到DOCAC JIRA任务</a>

### 可用性改进 {#june-26-usability}

此版本中将提供以下可用性改进。

* **历程和营销活动文件夹** — 您现在可以将历程和营销活动整理到&#x200B;**文件夹**中，以改进界面中的导航和管理。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14038">链接到DOCAC JIRA任务</a>

