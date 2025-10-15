---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1a5f6be689c9e91ee0dc0b5f024dbe8020424337
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 29%

---

# 预发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。


## 2025年10月预发行说明 {#25-10-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。链接、屏幕和更新的文档会于发布日期在发行说明中发布。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发布日期**：2025 年 10 月 21-22 日

### 新功能 {#oct-25-10-features}

<table>
<thead>
<tr>
<th><strong>历程中的直邮渠道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>直邮渠道以前仅限于营销活动，现在可在历程画布中使用，使您能够将直邮合并到历程中。 现在，可以在批处理和1:1历程场景中使用直邮，并且支持文件提取配置和基于时间的频率设置。</p>
<p> 此功能之前为限量发布版，现在可供在所有环境中使用（正式发布）。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>用于检索操作营销活动的新API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现已提供新的Journey Optimizer API，可让您以编程方式检索和检查与活动相关的数据，如详细信息、版本和配置。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自定义操作监控和报告</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过此功能，可以更好地了解历程运行状况和执行情况，包括生命周期状态和性能警报。您现在可以快速了解自定义操作中何时何处发生异常以及发生异常的原因。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>RCS基本消息传递</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过新的RCS Basic附加产品，您现在可以在Journey Optimizer中提供基本的丰富通信服务(RCS)报文传送，从而根据提供商和地理位置支持，实现以下增强的报文传送功能：</p>
<ul>
<li><strong>品牌和经验证的发件人支持：</strong>使用具有品牌元素（徽标、发件人名称等）的经验证的业务配置文件发送邮件。</li>
<li><strong>邮件传递见解：</strong>接收包含邮件状态更新（例如，已发送、已传递、已读取）的详细传递报告。</li>
<li><strong>链接跟踪：</strong>在RCS消息中嵌入和跟踪URL以进行参与分析。</li>
<li><strong>回退到短信：</strong>当收件人的设备不支持RCS或暂时无法通过RCS访问时，自动回退到短信。</li>
<li><strong>基本邮件合成：</strong>发送基于文本的RCS基本邮件。</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>编排的营销活动中的直邮渠道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>直邮渠道现在可用于编排的营销活动。 直邮活动可在您的编排营销活动中以直邮方式发送消息，支持一次性发送和定期发送。它用于自动生成直邮服务商所需的提取文件，从而实现直邮流程的自动化。您可以在编排营销活动画布中组合各类渠道活动，构建跨渠道营销活动，以根据客户行为和数据触发相应操作。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>忠诚度应用程序的新源连接器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform现在为Talon.One、Capillary和Kobie忠诚度应用程序提供新的源连接器。 这些连接器让您可以无缝地将忠诚度数据流式传输到Adobe Experience Platform中，并在Journey Optimizer中利用这些数据。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件渠道中的决策支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将决策策略添加到电子邮件历程和营销活动中。决策策略是产品建议的容器，利用决策引擎动态返回将会为每个受众成员提供的最佳内容。</p>
<p> 此功能之前为限量发布版，现在可供在所有环境中使用（正式发布）。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API触发的电子邮件营销活动的高吞吐量模式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>API 触发的营销活动现在提供新的高吞吐量模式。此模式专为大规模实时消息传送而设计（每秒最多 5000 个事务），能够在提高可用性的同时降低延迟。</p>
<p>此功能仅适用于电子邮件渠道，以及已购买 Adobe 高吞吐量事务性消息附加组件的组织。请联系 Adobe 客户代表以获取更多详情。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>无讯息小时数/基于时间的排除</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>利用免打扰时间，您可以定义电子邮件、短信、推送和WhatsApp渠道的基于时间的排除项。 它们可确保在特定时间段内不发送任何消息，从而帮助您尊重客户偏好和合规性要求。</p>
<p>您可以通过规则集应用无提示小时数，这些规则集可以分配给营销活动或历程中的单个操作，以实现精确控制。 通过简化这些流程。</p>
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>新的执行元数据辅助函数</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>个性化编辑器中提供了新的executionMetadata辅助函数。 利用该功能，可将上下文信息附加到任何本机操作，并将其捕获到数据集中以导出到外部系统。</p>
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>发布日期： 2025年10月13日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>试验代理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experimentation Agent是一款AI支持的工具，可更新您跨网站、电子邮件、推送消息和应用程序运行和管理数字实验的方式。 Experimentation Agent构建于Adobe Experience Platform AI平台和实验工具之上，可帮助您更有效地运行实验、组织业务目标，并生成可操作的见解，其中会突出显示哪些有效、哪些无效以及下一步在何处实验。</p>
<p>作为新Experimentation Accelerator功能的一部分，代理提供：</p>
<ul>
<li><strong>性能：</strong>试验中所发生情况的清楚视图</li>
<li><strong>分析：</strong>结果出现原因的解释</li>
<li><strong>机会：</strong>后续操作指南</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>发布日期：2025年10月9日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>用于检索历程的公共API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>新的Journey Optimizer API现在可用于检索历程及其关联的对象，例如营销活动和表面。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>发布日期： 2025年9月25日</p>
</td>
</tr>
</tbody>
</table>

### 改进

- **营销活动， Experience Decisioning，历程**
   - **在定位中选择可重复使用的规则** — 现在，在历程和营销活动中结合使用定位规则与消息优化功能时，您可以利用规则生成器。<!-- [Read more](../FILE.md) -->

- **渠道 — WhatsApp**
   - WhatsApp渠道的&#x200B;**执行字段** — 除了电子邮件和短信之外，现在还可以更新WhatsApp默认执行字段。 也可以覆盖在WhatsApp历程活动高级参数或WhatsApp渠道配置中全局设置的执行字段。<!-- [Read more](../FILE.md) -->

- **权限**
   - **历程/营销活动创建者不应能够批准** — 在创建或设置批准策略时添加了一个选项，以阻止历程/营销活动创建者批准自己的对象。<!-- [Read more](../FILE.md) -->

- **渠道 - 推送**
   - **移动设备实时活动 — 私人测试版** — 实时活动在移动设备应用程序中提供实时更新和交互式体验，使用户能够直接在设备屏幕上及时了解正在进行的事件或任务。 此功能通过提供实时信息（例如进度跟踪、事件更新或交互式内容）来增强参与度，而无需用户打开应用程序。<!-- [Read more](../FILE.md) -->

- **历程**
   - **新历程警报** — 可用日期：2025年10月14日
新的预配置警报可用于历程：超过的配置文件丢弃率（超过阈值的最后5分钟中配置文件丢弃与输入配置文件的比率）、超过的自定义操作错误率（超过阈值的最后5分钟中自定义操作错误与成功HTTP调用的比率）、超过的配置文件错误率（超过阈值的最后5分钟中配置文件出错与输入配置文件的比率）。<!-- [Read more](../FILE.md) -->

- **配置**
   - 一键取消订阅URL支持&#x200B;**自定义属性** — 可用日期： 2025年10月6日
借助Journey Optimizer，如果您在Adobe之外管理同意，则可以通过在电子邮件配置中定义您自己的一键式取消订阅链接来设置外部自定义端点。 当您的收件人单击取消订阅链接时，Journey Optimizer会向同意更新事件附加一些特定于用户档案的默认参数。 为进一步对取消订阅电子邮件地址进行个性化设置，您现在可以定义将会附加到同意事件的自定义属性。此功能自2025年8月起已为自定义一键取消订阅URL提供，现在为限量发布的Mailto（取消订阅）选项发布。 请联系您的Adobe代表以获取访问权限。<!-- [Read more](../FILE.md) -->

- **渠道 - 电子邮件**
   - **电子邮件的PDF附件** — 发布日期：2025年9月30日
您现在可以将静态PDF文件附加到使用Journey Optimizer发送的电子邮件中。 您每年最多可以为每个用户档案发送6封包含PDF附件的邮件。 每个附件允许的最大文件大小为5 MB。 对于任何其他大小或卷，您可以购买PDF附件加载项。 有关更多信息，请与 Adobe 代表联系。

  >[!AVAILABILITY]
  >
  >以前以“有限可用性”的形式发布，但现在所有环境都可以使用此改进（一般可用性）。

  <!-- [Read more](../FILE.md) -->

