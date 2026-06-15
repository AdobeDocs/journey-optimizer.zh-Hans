---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 53618e9d511215ed90b7666fe161edf9fd72c42b
workflow-type: tm+mt
source-wordcount: 1951
ht-degree: 5%

---


# 预发行说明 {#e-release-notes}

Adobe Journey Optimizer不断提供新功能、现有功能的增强以及错误修复。 所有更改会在每月末整合到[发行说明](release-notes.md)中。

## 2026年6月预发行说明 {#june-26-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。 一旦更改发布到生产环境，链接、屏幕和更新的文档就会发布。 虽然大多数更改将在发布日期交付，但其中一些更改可能会稍后推出 — 有关详细信息，请参阅为每个条目列出的可用性日期。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发行日期**： 2026年6月16日至17日

### 历程 {#june-26-journeys}

此版本中的历程将包括以下功能和改进。

* **增加了实时历程限制和新护栏** — 您现在最多可以有&#x200B;**200个活动历程**，比之前的100个限制有所增加。

* **历程标题中的开始和结束日期** — 在实时历程中配置开始和/或结束日期时，它们现在显示在实时状态徽章旁边的&#x200B;**历程标题**&#x200B;中。 显示的标签会根据每个日期即将到来还是已经过去进行调整。

* **直接停止或关闭暂停的历程** — 您现在可以&#x200B;**直接从**&#x200B;暂停&#x200B;**状态停止历程或将其关闭到新入口**。 以前，暂停的历程必须恢复为实时状态，然后才能停止或关闭。

### 编排的营销活动 {#june-26-oc}

此版本中的编排营销活动即将推出以下功能和改进。

<table>
<thead>
<tr>
<th><strong>在编排的营销活动中基于文件的定位</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，编排的营销活动支持直接将<strong>CSV或TXT文件</strong>加载到营销活动画布中作为定向受众，而无需先将文件摄取到Adobe Experience Platform。 文件数据在执行时消耗，并且不作为Adobe Experience Platform数据集保留。 在文件设置过程中，可以定义列映射、数据类型、NULL处理和每列错误策略。 验证失败的行会被拒绝，并在营销活动运行之前进行记录，这样可保持受众干净，而无需手动预处理。 这尤其适用于临时发送或合作伙伴列表营销活动，这些活动构建完整摄取管道不现实。</p>
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
</td>
</tr>
</tbody>
</table>

* **在编排的营销活动中基于循环的关系数据个性化** — 个性化编辑器现在支持&#x200B;**循环块**，该块可在关系收藏集（如订单、帐户或预订）上进行迭代，并在单个电子邮件或短信中为每个记录呈现一个内容块。 收藏集是使用个性化令牌通过数据选取器配置的，无需编写表达式。 您可以在营销活动开始之前，预览循环块针对示例数据的呈现方式，包括处理空集合。

* **为每个收件人和营销活动个性化电子邮件发件人详细信息** — 编排的营销活动现在支持使用配置文件属性或关系数据对&#x200B;**电子邮件标题字段**&#x200B;进行个性化，包括发件人姓名、发件人地址和回复。 这允许发件人详细信息反映每个收件人的相关顾问、位置或分支，而不是通过单个公司地址路由所有发送。 可以在渠道级别设置标题值，并使用上下文数据覆盖每个营销活动的标题值，以实现更精确的控制。

<!--
* **Target dimension simplification in Orchestrated campaigns** - The active **targeting dimension** is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->

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
</td>
</tr>
</tbody>
</table>

* **动态项目属性** — 决策项目自定义属性现在可以在交付时使用配置文件、上下文和受众数据进行个性化。 这消除了维护次要内容变体的重复选件的需要，允许营销人员管理更少、更灵活的决策项目。

### 电子邮件 {#june-26-email}

此版本中的电子邮件渠道即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>电子邮件Designer中的内容质量检查</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在包括直接在Email Designer中进行的自动技术验证，可帮助您在发送之前捕获HTML和CSS问题。</p>
<p>检查涵盖不支持的元素，例如<code>&lt;script&gt;</code>和<code>&lt;base&gt;</code>标记、可中断Microsoft Outlook中的布局的空div、HTML Meta Refresh标记，以及触发Gmail渲染失败的CSS或HTML大小阈值。</p>
<p>结果直接在创作面板中显示为错误、警告或信息性声明，其中包含上下文详细信息和一键式修复（如果可用），因此无需离开编辑器即可解决问题。</p>
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
<p>Journey Optimizer现在包含一个选项，该选项通过去除不必要的空格、注释和冗余代码来减小电子邮件的HTML的大小，而不会影响电子邮件的呈现方式。</p>
<p>这可避免某些电子邮件提供商用于标记或拒绝邮件的大小阈值，从而提高可投放性，并可能缩短收件人的加载时间。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>片段可编辑字段中的富文本</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将富文本添加到电子邮件内容中使用的可自定义片段。</p>
<p>例如，在将文本组件用作电子邮件Designer中的可编辑字段时，您可以直接设置内容格式（例如，粗体和斜体）并插入超链接。</p>
</td>
</tr>
</tbody>
</table>

* **增强的图像到HTML转换器** — 现已提供新版本的图像到HTML转换器功能，从而提高生成HTML的准确性。 此更新利用更高层的LLM模型，从图像输入提供更精确、更可靠的HTML输出。

+++ 即将推出 — **下面的信息可能会发生更改**

<table>
<thead>
<tr>
<th><strong>电子邮件Designer中的模块</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>电子邮件Designer现在包括现成的布局模块库（例如页眉、产品卡、信息块和页脚），您可以将这些模块直接拖放到电子邮件画布中。</p>
<p>每个模块都预先配置了可编辑的属性（图像、标题、文本、按钮、链接），并且可以通过WYSIWYG界面完全自定义，从而加快电子邮件创建速度，而无需您从头开始构建结构。</p>
<p>发布日期：2026年6月22日</p>
</td>
</tr>
</tbody>
</table>

+++

### 移动消息（短信、彩信、RCS和LINE） {#june-26-mobile}

此版本中的移动消息传送功能即将实现以下改进。

* 短信报告的&#x200B;**唯一点击次数** — 为短信报告引入了一个新的&#x200B;**唯一点击次数**&#x200B;模块，为当前可用于电子邮件报告的短信引入了相同级别的粒度性能跟踪。

* **LINE频道 — 创作更改** - LINE频道UI已升级，具有高级消息创作功能。 此版本引入了对&#x200B;**多种消息格式**&#x200B;的支持，包括文本、图像、图像映射、轮播和Flex （JSON编辑器），以及实时设备预览。 用户现在可以管理最多五条已排序消息的分组消息（具有添加、删除和重新排序控件），并利用集成的个性化编辑器进行验证的动态消息传送。

* **短信 — 显示使用情况量度** — 对于直接通过Adobe Journey Optimizer购买短信的客户，引入了新的&#x200B;**短信使用情况仪表板**。 您现在可以查看和跟踪最近90天的消息发送指标，并按发起的移动设备(MO)和终止的移动设备(MT)消息进行分类。 此数据也可以通过CSV下载，从而更好地显示和控制短信支出。

### 内容和集成 {#june-26-content}

此版本中的内容管理和集成即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>对Journey Optimizer中的Adobe Experience Manager内容片段的改进</strong><br/></th>
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
<li>现在，您可以灵活地了解Adobe Journey Optimizer如何访问Adobe Experience Manager内容。 此版本引入了为历程和营销活动中使用的内容片段<strong>切换源存储库</strong>的功能。</li>
<li>现在与<b>Managed Services</b>兼容，您可以直接在Journey Optimizer中查看、访问和使用Adobe Experience Manager内容片段以进行个性化。 只需在配置设置中添加Adobe Experience Manager Managed Services存储库URL作为一次性设置即可。</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI Assistant与Adobe Experience Manager Asset Essentials集成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在生成电子邮件、网页和推送通知时，AI助手现在会直接从您的Adobe Experience Manager Assets中自动提取<b>品牌批准的图像</b>。 这消除了手动搜索Assets或依赖通用AI回退的需要，确保每个视觉效果都非常准确且符合品牌规范。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>用于内容生成增强功能的AI助手</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此版本通过更强大的图像编辑、更可靠的品牌提取以及图像流中的内容真实性支持，改进了<strong>AI助手</strong>内容生成体验：</p>
<ul>
<li><strong>AI图像编辑</strong>现在可在图像生成流程中使用，包括Firefly第三方模型支持，因此无需离开助手即可优化源图像。</li>
<li><strong>品牌信号提取</strong>可提供更高质量的结果。 当所选页面信号不足时，改进的回退现在会填充颜色、排版规则、编写准则和其他品牌属性。</li>
<li><strong>基于Web的品牌提取</strong>更加可靠。 改进了超时处理功能，有助于防止慢页面、弹出窗口和Cookie横幅阻止提取。</li>
<li>图像流中现在支持<strong>内容真实性(CAI)</strong>。 此版本还修复了引用图像上传问题，并改进了对没有现有C2PA清单的图像的处理。</li>
</ul>
</td>
</tr>
</tbody>
</table>

<!--
### Campaigns {#june-26-campaigns}

The following improvement is coming to campaigns in this release.

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default **execution field** set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.
-->

### 报表 {#june-26-reporting}

此版本中的报表即将进行以下改进。

* **电子邮件和短信报告的预计点击次数** —历程、营销活动和渠道报告中现在为电子邮件和短信提供了一个新的&#x200B;**预计点击次数**&#x200B;指标。 此量度不包括已识别的机器人和非人工交互(NHI)流量，以便更清楚地了解真实的客户参与。 现有的点击量量度仍然可用，并且会继续报告总点击量。

+++ 即将推出 — **下面的信息可能会发生更改**

* **电子邮件和短信报告的新估计点击量度** — 为了更准确地查看实际客户参与情况，现在提供了跨历程、营销活动和渠道报告的新估计量度。 这些量度有助于从报表数据中过滤掉非人工交互(NHI)和机器人点击：

   * 预计CTR：相对于投放总数的预计点击次数。
   * 仅电子邮件的预计CTOR：相对于预计打开次数的预计点击次数。

  发布日期：2026年6月下旬

+++

### 配置 {#june-26-configuration}

此版本中的配置和管理功能将进行以下改进。

* **数据集从流模式移动到批处理模式** - AJO消息反馈事件数据集正在从流模式过渡到&#x200B;**批处理摄取模式**。 此更改可确保数据摄取不超过流摄取限制。 如果您在Customer Journey Analytics报表中使用此数据集或对其运行查询，预计今后数据延迟最多将增加2小时。

+++ 即将推出 — **下面的信息可能会发生更改**

* **Web应用程序防火墙(WAF) IP白名单** - Adobe Journey Optimizer现在支持将登陆页列入Web应用程序防火墙(WAF) IP白名单，从而使组织能够强制要求所有传入请求都专门通过其配置的WAF基础架构进行路由。 借助这项增强功能，客户可以将Journey Optimizer配置为拒绝任何绕过WAF层的直接请求，从而确保Imperva等工具中定义的安全策略得到一致应用。 此功能增强了具有严格网络访问要求的企业的安全状况，使它们能够完全控制流向AJO托管的登陆页面的流量。

  发布日期：2026年6月下旬

+++

### 可用性改进 {#june-26-usability}

此版本中将提供以下可用性改进。

* **历程和营销活动文件夹** — 您现在可以将历程和营销活动整理到&#x200B;**文件夹**&#x200B;中，以改进界面中的导航和管理。
