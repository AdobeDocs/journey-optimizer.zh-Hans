---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: bcbca3a179b2cb5c686f1afd04fa9e9e611c9720
workflow-type: tm+mt
source-wordcount: 2036
ht-degree: 15%

---


# 预发行说明 {#e-release-notes}

Adobe Journey Optimizer 不断地提供新功能、对现有功能的增强和错误修复。 所有更改会在每月末整合到[发行说明](release-notes.md)中。

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.




### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## 2026年7月预发行说明 {#july-26-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。 一旦更改发布到生产环境，链接、屏幕和更新的文档就会发布。 虽然大多数更改都在发布日期交付，但其中一些更改可能会稍后推出。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发行日期**： 2026年7月28日至29日

### 忠诚度 {#july-26-loyalty}

Journey Optimizer引入了忠诚度，这是此版本中的一项新功能。

<table>
<thead>
<tr>
<th><strong>忠诚度挑战</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>忠诚度挑战可将忠诚度计划转化为引人入胜的游戏化体验，从而激励客户采取有价值的行动，例如进行购买、撰写评论或任何期望的行为。</p>
<p>管理员可以使用“忠诚度管理员”菜单将Journey Optimizer与您的忠诚度生态系统关联，包括奖励履行API、事件定义、产品库存、排除和身份设置。 然后，营销人员可以设计标准、连续或顺序挑战，定义任务和奖励，提供品牌内容卡和消息，并使用AI支持的报告仪表板监控性能。 Journey Optimizer生成在后台编排每个挑战的历程，因此团队可以专注于客户体验和业务目标。</p>
<p>忠诚度还引入了同事技能，使团队能够更有效地执行关键挑战操作，包括创建挑战、设置挑战属性、管理受众和相关配置，以及查看见解以监控挑战参与情况和奖励表现。</p>
<p>此功能仅适用于获得Journey Optimizer忠诚度许可的组织。 要获得访问权限，请与 Adobe 代表联系。</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<!--

### Onboarding {#july-26-onboarding}

Journey Optimizer introduces the Onboarding Assistant, a new capability in this release.

<table>
<thead>
<tr>
<th><strong>Onboarding Assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

### 历程 {#july-26-journeys}

在此版本中，历程中添加了以下功能和改进。

<table>
<thead>
<tr>
<th><strong>渠道优化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将历程操作配置为包含多个出站渠道（电子邮件、推送、短信），并让Journey Optimizer通过最佳渠道为每个客户自动交付。 提供了三种优化模式：</p>
<ul>
<li>手动排名：指定您的首选渠道顺序。</li>
<li>客户偏好设置：使用客户个人资料中的偏好渠道（体验数据模型同意和偏好设置属性）。</li>
<li>基于人工智能模型的排名：使用机器学习倾向分数推断每位客户最有效的渠道。</li>
</ul>
<p>当排名最前的渠道不可用（未选择启用、频率限制或未配置）时，系统回退到下一个可用渠道。</p>
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* 历程模拟中的&#x200B;**外部受众** -历程模拟现在支持外部受众。 在模拟面向CSV或联合受众组合受众的历程时，您可以直接通过UI表单或JSON导入来模拟这些受众的扩充属性。 UI仅动态显示历程逻辑中使用的特定扩充属性，从而能够在决策分支和个性化规则上线之前进行精确验证。<!-- Documentation link: TBD -->

### 营销活动 {#july-26-campaigns}

此版本中的营销活动添加了以下功能和改进。

<table>
<thead>
<tr>
<th><strong>API触发的电子邮件中的个性化PDF附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在支持在API触发的营销活动中，每封电子邮件最多附加5个特定于收件人的PDF。 PDF文件是从Azure或AWS存储中安全获取的，并在发送时附加，每个文件的位置直接传递到API有效负载中。 这允许保留现有的上游文档生成系统，由Journey Optimizer处理投放。</p>
<p>受支持的用例包括发票、对帐单、票证、合同、运输标签和类似的文档，这些文档因收件人而异。 个性化PDF附件仅在API触发的营销活动中可用，在历程或其他营销活动类型（操作、编排）中不受支持。</p>
<p>PDF附件加载项支持更大的附件卷和大小；有关更多信息，请与Adobe代表联系。</p>
<p></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>活动中的入站体验模拟</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在上线之前在“操作”营销活动中模拟入站渠道操作。 使用模拟模式通过模拟用户测试您的配置并预览呈现的体验，包括生成的URL和二维码，因此您可以端到端地验证规则、决策和内容呈现。</p>
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

* **营销活动文件夹** — 您现在可以将营销活动组织到文件夹中，以改进界面中的导航和管理。<!-- Documentation link: TBD -->

* **覆盖营销活动中的默认执行字段** — 以前在历程级别可用，现在可覆盖在营销活动参数中为电子邮件、短信和WhatsApp投放设置的全局默认执行字段。<!-- Documentation link: TBD -->

* **营销活动仪表板中的品牌一致性分数** – 您现在可以直接在营销活动仪表板中评估品牌一致性分数，以确保内容符合品牌形象。 这使您无需打开内容设计器即可一目了然地验证准则。<!-- Documentation link: TBD -->

### 编排的营销活动 {#july-26-oc}

此版本中的编排活动添加了以下改进。

* **查看编排的营销活动过渡权限** — 添加了新的&#x200B;**查看编排的营销活动过渡**&#x200B;权限，以替换旧版&#x200B;**在编排的营销活动中查看文件**&#x200B;选项。 此更改允许您隐藏促销活动过渡中的预览结果，以支持个人身份信息合规性。

<!--
<table>
<thead>
<tr>
<th><strong>Quiet Hours support for orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now apply quiet hours to Orchestrated campaigns. Quiet hours let you define time-based exclusions to prevent messages from being sent during specific periods, helping you respect customer preferences and compliance requirements across campaign orchestration use cases.</p>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

* **Ability to Manage Profile Target Dimensions** - You can now delete a Profile Target Dimension or edit and swap its configured identity namespace, providing greater control and flexibility over your data setups.

* **Support for Line** - You can now add LINE actions directly into your Orchestrated campaigns. This new activity allows you to build and deliver highly personalized content, including text, stickers, images, videos, location data, and rich Flex Messages, to engage your customers seamlessly on the LINE platform. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.

* **New Orchestrated campaigns public APIs** - New API specifications are now available for Orchestrated campaigns. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines.

* **Personalize email sender details per recipient and campaign** - Orchestrated campaigns now support personalization of email header fields, including From name, From address, and Reply-To, using profile attributes or relational data. This allows sender details to reflect the relevant advisor, location, or branch for each recipient, rather than routing all sends through a single corporate address. Header values can be set at the channel level and overridden per campaign using contextual data for more precise control. Documentation link: TBD

* **Target dimension simplification in Orchestrated campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.

-->

### 决策 {#july-26-decisioning}

在此版本中，已向Decisioning添加了以下改进。

* **从自然语言表达式创建决策规则** — 您现在可以简单语言描述要创建的决策规则，并让AI为您生成它。 此功能面向有权访问Adobe AI功能的客户提供。

  此功能仅面向一部分组织（限量发布）。 要获取访问权限，请联系您的Adobe代表。<!-- Documentation link: TBD -->

* **决策规则和排名公式模拟** — 您现在可以直接从规则编辑器或公式编辑器模拟决策规则和排名公式。 添加手动测试变体或使用AI生成它们，然后对测试数据运行表达式以验证资格并查看排名结果，所有这些都是在部署到生产环境之前完成的。 具有访问Adobe AI功能的客户可以生成变体。

  此功能仅面向一部分组织（限量发布）。 要获取访问权限，请联系您的Adobe代表。<!-- Documentation link: TBD -->

* **优惠级别的Personalization** — 决策项自定义属性现在可以在交付时使用配置文件、上下文和受众数据进行个性化。 这消除了维护次要内容变体的重复选件的需要，允许营销人员管理更少、更灵活的决策项目。<!-- Documentation link: TBD -->

<!--
* **Placement-level frequency capping in Decisioning** - Frequency capping rules in Decisioning can now be scoped to individual placements, giving you finer control over how often an offer is shown in a given surface. Two modes are available: placement-specific capping (define a cap that applies only when the offer is displayed in a selected placement) and per-placement capping (apply a cap independently across every placement where the offer appears, so each placement maintains its own capping counter). Documentation link: TBD
-->

### 内容管理 {#july-26-content}

此版本中的内容管理添加了以下改进。

* **电子邮件模板**&#x200B;的`<head>`中支持表达式片段 — 现在可以在电子邮件模板的`<head>`中使用表达式片段。 这允许您在一个片段中集中设置样式或任何自定义代码，并在多个模板中重复使用。 更新并重新发布片段后，所有基于引用该片段的模板构建的电子邮件都会自动继承最新代码，而无需分别手动更新每封电子邮件。<!-- Documentation link: TBD -->

* 将&#x200B;**“AI助手”重命名为“生成内容”** - AI助手已重命名为“在整个Adobe Journey Optimizer中生成内容”。 此更新仅限于命名和术语；未引入任何功能更改。 内容生成、图像生成、个性化表达式和内容实验的导航标签、按钮、菜单和对话框已从“AI助手”重命名为“生成内容”。<!-- Documentation link: TBD -->

* **用于AI内容生成的灵活图像源** — 现在，在Journey Optimizer中生成内容时，将直接从Adobe Experience Manager Assets Essentials及更高版本中获取品牌批准的图像。 控制平衡的模式有三种：Assets（数字资产管理来源，默认）、Balanced（数字资产管理优先，AI填补空白）和Creative（AI优先）。 这可确保每个视觉对象都准确、符合品牌要求，并为历程和营销活动做好生产准备。<!-- Documentation link: TBD -->

* **多语言改进** — 语言设置现在可以从现有的活动设置复制，因此您不再需要完全重建配置以进行更改。 在创作语言设置时，您还可以将条件从一个区域设置复制到另一个区域设置，从而简化具有多种语言的网站的设置。

<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. [Documentation link: TBD]
-->

### 个性化 {#july-26-personalization}

此版本中的个性化设置添加了以下改进。

* **管理用于完整/基本URL个性化的域** — 您现在可以直接从Adobe Journey Optimizer中的“管理”设置创建和管理用于完整/基本URL个性化的已批准域，而无需联系Adobe支持部门。<!-- Documentation link: TBD -->

* **个性化表达式中的新辅助函数** — 个性化表达式中现在有新辅助函数：

  * `appendQueryParams`：将查询参数附加到URL，如果键已存在，则替换该参数。
  * `dateBetween`：检查日期是否在开始和结束日期范围内（包括）。
  * `equalsAnyIgnoreCase`：当字符串与任何提供的值匹配时返回true，忽略大小写。
  * `getUrlFragment`：提取URL的片段部分（#之后的部分）。
  * `join`：使用分隔符将数组元素串联为单个字符串。
  * `decode64`：对Base64编码的字符串进行解码。 如果输入无效Base64，则原始输入字符串将保持不变。
  * `parseJson`：将JSON字符串解析为可在模板中使用的结构化变量。
  * `valueAtPath`：将数据路径中的值分配给模板变量，并通过可选索引从数组或集合中提取特定元素。

  `concat`函数也得到了增强，现在支持两个或更多参数。

  此外，以下模板迁移函数现在可用于协助将现有模板迁移到Journey Optimizer：

  * `ampCompare`：使用指定的比较运算符比较两个值。
  * `ampSubstr`：返回指定开始索引和结束索引之间的字符串的一部分。
  * `compareTo`：按词典比较两个字符串。

<!-- Documentation link: TBD -->

### 电子邮件渠道 {#july-26-email}

以下功能已添加到此版本的电子邮件渠道中。

<table>
<thead>
<tr>
<th><strong>电子邮件设计器中的模块</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Email Designer 现在内置了一个现成的布局模块库——包括页眉、产品卡片、信息块和页脚等——您可以将这些模块直接拖放到电子邮件画布中。 每个模块都预先配置了可编辑的属性（图像、标题、文本、按钮、链接），并且可以通过 WYSIWYG 界面完全自定义，从而加快电子邮件创建速度，而无需您从头开始构建结构。</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 渠道 {#july-26-channels}

此版本中的渠道添加了以下功能和改进。

<table>
<thead>
<tr>
<th><strong>自定义出站频道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在引入了“自定义渠道”这一新功能，管理员可以通过无代码渠道生成器，将任何基于HTTP的出站消息渠道（如WeChat、Kakao Talk、Messenger或专有提供商）直接引入Journey Optimizer。 配置完毕后，即可跨营销活动、历程和编排的营销活动使用自定义渠道，并具有与本机渠道相同的完整功能集：使用表达式编辑器进行个性化、内容实验、预览和验证、现成的报告以及同意和治理实施。 这填补了之前由自定义操作填补的空白，这些操作仅适用于历程，缺少专用渠道功能。</p>
<p>自定义出站渠道当前以有限可用状态提供。 要获得访问权限，请与 Adobe 代表联系。</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **WhatsApp渠道：支持WhatsApp流量模板** — 您现在可以在Adobe Journey Optimizer中发送WhatsApp流量模板，以提供交互式多屏幕体验，如调查和商机捕获。 响应在提交时捕获，并作为原始JSON有效负载存储在新的Journey Optimizer渠道跟踪事件数据集中。<!-- Documentation link: TBD -->

* **吞吐量的性能加载项 — 推送** — 在API触发的营销活动中提供新的高吞吐量事务性消息传递模式。 此模式专为大规模实时事务型消息传递而设计，支持每秒最多 5,000 个事务并具有较高的可用性。 以前仅适用于电子邮件渠道，而现在此功能也可用于推送渠道，适用于已购买Adobe高吞吐量事务性消息传递附加产品的组织。 有关更多详细信息，请与Adobe代表联系。<!-- Documentation link: TBD -->

* **增强的自定义提供程序集成 — 移动设备** — 自定义提供程序集成现在通过关键消息传递和标头更新提供了扩展的灵活性：

  * 标头自定义：您现在可以编辑默认的Content-Type标头值并添加最多10个自定义标头参数。

  * SMS有效负载支持：在SMS有效负载中添加了对Adobe Journey Optimizer帮助程序函数的支持，包括编码64。

### 管理 {#july-26-administration}

此版本中的管理中添加了以下功能。

<table>
<thead>
<tr>
<th><strong>Web应用程序防火墙IP白名单</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer现在支持将登陆页列入Web应用程序防火墙IP白名单，从而使组织能够强制要求所有传入请求仅通过其配置的Web应用程序防火墙基础架构进行路由。 借助这项增强功能，客户可以将Journey Optimizer配置为拒绝任何绕过Web应用程序防火墙层的直接请求，从而确保始终如一地应用在Imperva等工具中定义的安全策略。</p>
<p>此功能增强了具有严格网络访问要求的企业的安全状况，使它们能够完全控制流向Journey Optimizer托管的登陆页面的流量。</p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>
