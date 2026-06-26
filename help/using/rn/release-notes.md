---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 2df5d9db31e03d4548b8ccc32c2d25293d829f1d
workflow-type: tm+mt
source-wordcount: 3714
ht-degree: 84%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、增强现有功能，并修复错误。 所有更改会在每月的最后一周整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 遵循持续交付模式，使 Adobe 能够持续不断地提供新功能、增强功能和修复。 此方法支持以可扩展的方式分阶段推出各种功能，以确保所有环境的性能和稳定性。 由于此模型，在每月发行版本之间会更新发行说明。 有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](releases.md)。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。 在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

>[!NOTE]
>
>这些发行说明中列出的功能包括&#x200B;**可用日期**，该日期指明每项变更在您的环境中何时可供使用。 **即将推出**&#x200B;折叠面板中的条目预计将在未来几天或几周内列出。 这些部分中的信息可能随时更改。

## 2026年6月发行说明 {#june-26-rn}

### 历程 {#june-26-journeys}

在此版本中，历程中添加了以下功能和改进。 预计未来几天或几周内还将进行其他更改。


<table>
<thead>
<tr>
<th><strong>历程模拟（正式发布版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将历程设置为“模拟”模式。 此模式允许您使用模拟用户验证逻辑。 这些是为了模拟而专门创建的临时轮廓，让您可以自由测试，而无需在 Adobe Experience Platform 中管理长期保留的测试轮廓。 </p>
<p>此功能之前为限量发布版，历程模拟现在可供所有环境使用。 在此正式发布版中，您现在可以使用 Journey 代理直接在模拟菜单中生成模拟用户和事件。</p>
<p><img src="assets/do-not-localize/journey-simulation.gif"></p>
<p>有关更多信息，请参阅<a href="../building-journeys/simulate-journey-gs.md">详细文档</a>。</p>
<p>发布日期：2026 年 6 月 9 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程片段（正式发布版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在 Adobe Journey Optimizer 中创建<strong>历程片段</strong>。 历程片段是可重用的历程节点集，您可以一次性生成此节点，然后将其放到沙盒的任意历程中。 无论是资格检查、首选渠道路由逻辑还是欢迎序列，片段都可以帮助团队提高效率并保持一致，无需每次都从头开始重新生成相同的逻辑。</p>
<p>创建后，片段会被存储在专用的<strong>片段清单</strong>中，并可使用<strong>历程片段</strong>活动将其插入任何历程。</p>
<p>此功能此前以“有限可用版”形式推出，现已对所有客户可用。 历程片段还支持<strong>沙盒工具</strong>，允许您跨沙盒打包和导出片段。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/journey-fragments.md">详细文档</a>。</p>
<p>发布日期：2026 年 6 月 9 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程路径优化 - 定位（正式发布版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>优化活动</strong>现在支持<strong>定向规则</strong>，利用这些规则，可根据受众区段或轮廓属性定义客户必须满足的特定条件，以符合特定历程路径的资格。</p>
<p>与试验性做法（将客户随机分配给路径）不同，定位使用确定性逻辑来确保将适当的受众或客户轮廓路由到预期路径。</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p><img src="assets/do-not-localize/optimize.gif"></p>
<p>有关更多信息，请参阅<a href="../building-journeys/path-targeting.md">详细文档</a>。</p>
<p>发布日期：2026 年 6 月 8 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程表达式的 AI 助手（公共 Beta 版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AI 助手现在在历程高级表达式编辑器中运行，以将自然语言提示转换为有效的表达式和条件逻辑。 描述您要生成的表达式，AI 助手便会生成可直接使用的代码。您可以立即应用这些代码，或通过后续提示对其进一步优化。</p>
<p>此功能目前为公开 Beta 版，向所有客户开放。</p>
<p><img src="assets/do-not-localize/expression-assistant.gif"></p>
<p>有关更多信息，请参阅<a href="../building-journeys/expression/expression-agent.md">详细文档</a>。</p>
<p>发布日期：2026 年 6 月 3 日</p> 
</td>
</tr>
</tbody>
</table>


* [!BADGE 弃用]{type=Negative} **受众资格节点中已弃用批次受众** — 从&#x200B;**2026年8月**&#x200B;开始，Journey Optimizer将阻止在&#x200B;**受众资格**&#x200B;节点中使用批次受众的任何历程的发布。 历程画布中已显示验证警告。 现有的实时历程不受影响。 包含此配置的新历程、草稿历程和重复历程必须在2026年8月之前更新。 在“受众资格”节点中使用流式受众，或切换到&#x200B;**读取受众**&#x200B;活动。 [了解如何迁移您的历程](../building-journeys/aq-batch-audiences-migration.md)

* **直接停止暂停的历程** — 您现在可以直接从&#x200B;**已暂停**&#x200B;状态停止历程。 以前，暂停的历程必须先恢复到&#x200B;**实时**，然后才能停止。 [了解更多信息](../building-journeys/journey-pause.md#stop-close-paused)

  发布日期：2026年6月18日至22日

* **外部受众的补充标识符支持** – 历程中的补充标识符现在支持外部受众，包括从 CSV 文件导入的受众和通过联合受众构成创建的受众。 您可以将受众中的任何非身份属性或非人员身份属性指定为补充 ID，无需进行模式标记。 [了解更多信息](../building-journeys/supplemental-identifier.md)

  发布日期：2026 年 6 月 11 日

* **非重复性读取受众历程的自动停止** – 现在，非重复性&#x200B;**读取受众**&#x200B;历程会在最后一个活跃轮廓退出后自动转换为&#x200B;**已停止**&#x200B;状态。 以前，这些历程会保持&#x200B;**活跃**&#x200B;状态，直到 91 天的全局超时期限结束，即使此时已没有轮廓在历程中流转。 经过此改进后，历程状态会在完成时反映实际的执行状态，从而无需手动干预即可保持历程清单的准确性。

  请注意，此行为不适用于包含导致等待期的节点的历程，例如等待节点、反应节点或事件触发的过渡。 这些历程仍受标准 91 天全局超时限制。 [了解详情](../building-journeys/end-journey.md#auto-stop-non-recurring)

  发布日期：2026 年 6 月 9 日

* **自定义操作中基于证书的自定义身份验证** — 自定义操作现在支持基于证书的自定义身份验证。 通过将 `subType: "certificateCredential"` 添加到自定义授权配置，Journey Optimizer 使用 Adobe 的受管证书对 JWT 客户端断言进行签名，并将其交换为访问令牌，无需客户端密钥。 专为实施基于证书的身份验证的企业 API（如 Microsoft Entra ID）而设计。 [了解详情](../datasource/external-data-sources.md#certificate-credential)

  发布日期：2026 年 6 月 4 日

* **增加了实时历程限制和新护栏** — 您现在最多可以有 **200 个活动历程**，比之前的 100 个限制有所增加。 [了解更多信息](../start/guardrails.md#journeys-guardrails-journeys)

  发布日期：2026年6月18日。 此功能将在未来几天内逐步推广到所有地区。


+++ 即将推出 — **下面的信息可能会发生更改。**

* **历程标题中的开始和结束日期** — 在实时历程中配置开始和/或结束日期时，它们现在显示在活跃状态徽章旁边的&#x200B;**历程标题**&#x200B;中。 显示的标签会根据每个日期即将到来还是已经过去进行调整。

+++

### 编排的营销活动 {#june-26-oc}

在此版本中，编排的营销活动中即将提供以下功能和改进。

* **关系数据的基于循环的个性化** — 个性化编辑器现在支持循环块，该循环块遍历关系集合（如订单、帐户或预订），并在单个电子邮件或短信中为每个记录呈现一个内容块。 收藏集是使用个性化令牌通过数据选取器配置的，无需编写表达式。 [了解更多信息](../orchestrated/add-personalization.md#enrichment-collections)

  发布日期：2026年6月26日

+++ 即将推出 — **下面的信息可能会发生更改。**

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
<p> 发布日期：2026年6月30日</p>
</td>
</tr>
</tbody>
</table>

+++

### 决策 {#june-26-decisioning}

在此版本中，Decisioning 中添加了以下功能和改进。

<table>
<thead>
<tr>
<th><strong>直邮渠道中的决策支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将决策策略添加到直邮历程和营销活动中。 决策策略是产品建议的容器，利用决策引擎为每个受众动态返回最佳内容。 直邮决策还支持批量决策用例，使您能够导出给定 Adobe Experience Platform 受众中每个配置文件的相应产品建议项目。 </p>
<p><img src="assets/do-not-localize/exd-dm.gif"></p>
<p>有关更多信息，请参阅<a href="../experience-decisioning/use-decision-policy.md">详细文档</a>。</p>
<p>发布日期：2026 年 6 月 3 日</p>
</td>
</tr>
</tbody>
</table>

* **在Decisioning中利用Adobe Experience Manager内容片段** — 您现在可以将Adobe Experience Manager内容片段映射到Decisioning中的决策项，并在决策策略中利用它们，以便在适当的时间将适当的片段提供给适当的客户。 此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。 [了解更多信息](../experience-decisioning/fragments-decision-policies.md)

  发布日期：2026年6月18日

+++ 即将推出 — **下面的信息可能会发生更改。**

* **动态项目属性** — 决策项目自定义属性现在可以在交付时使用轮廓、上下文和受众数据进行个性化。 这消除了维护次要内容变体的重复选件的需要，使营销人员管理更少、更灵活的决策项。

  发布日期：2026 年 6 月下旬

+++

### 内容管理 {#june-26-content}

此版本中的内容管理添加了以下功能和改进。

<table>
<thead>
<tr>
<th><strong>模拟内容变体 — 更新的体验和 AI 变体生成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>模拟内容</strong>工作流现在有两个更新可用：</p>
<ul>
<li><strong>新的默认路径</strong> — 单击<strong>模拟内容</strong>将默认打开<strong>模拟内容变体</strong>体验。 在单个屏幕中，您可以手动添加或从 CSV/JSON 文件添加样本输入、重复使用模拟的用户、预览渲染和发送校样。 若要使用 Adobe Experience Platform 测试轮廓进行预览、发送包含测试轮廓数据的校样，或检查电子邮件收件箱渲染和垃圾邮件报告，请单击<strong>模拟内容</strong>，然后从下拉列表中选择<strong>模拟内容（AEP 轮廓）</strong>。</li>
<li><strong>AI 生成的内容变体</strong> — 在<strong>模拟内容变体</strong>体验中，单击<strong>生成</strong>以使用 AI 自动创建内容变体。 系统将分析您的消息，检测个性化字段和条件分支，并填充实际值，以便您无需手动构建每个变体即可验证渲染。</li>
</ul>
<p>有关更多信息，请参阅<a href="../test-approve/simulate-sample-input.md">详细文档</a>。</p>
<p>发布日期：2026 年 6 月 9 日</p>
</td>
</tr>
</tbody>
</table>


+++ 即将推出 — **下面的信息可能会发生更改。**

<table>
<thead>
<tr>
<th><strong>模拟内容变体 — 更新的体验和 AI 变体生成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>模拟内容</strong>工作流现在有两个更新可用：</p>
<ul>
<li><strong>新的默认路径</strong> — 单击<strong>模拟内容</strong>将默认打开<strong>模拟内容变体</strong>体验。 在单个屏幕中，您可以手动添加或从 CSV/JSON 文件添加样本输入、重复使用模拟的用户、预览渲染和发送校样。 若要使用 Adobe Experience Platform 测试轮廓进行预览、发送包含测试轮廓数据的校样，或检查电子邮件收件箱渲染和垃圾邮件报告，请单击<strong>模拟内容</strong>，然后从下拉列表中选择<strong>模拟内容（AEP 轮廓）</strong>。</li>
<li><strong>AI 生成的内容变体</strong> — 在<strong>模拟内容变体</strong>体验中，单击<strong>生成</strong>以使用 AI 自动创建内容变体。 系统将分析您的消息，检测个性化字段和条件分支，并填充实际值，以便您无需手动构建每个变体即可验证渲染。</li>
</ul>
<p>有关更多信息，请参阅<a href="../test-approve/simulate-sample-input.md">详细文档</a>。</p>
<p>发布日期：2026 年 6 月下旬</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Optimizer 中 Adobe Experience Manager 内容片段的改进</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此版本带来了多项增强功能，使<strong>Adobe Experience Manager 内容片段</strong>在 Journey Optimizer 创作工作流中更具可用性、更易于治理，且更适合投入生产环境：</p>
<ul>
<li>Journey Optimizer 现在支持从多个 Adobe Experience Manager 配置中获取内容片段，包括创作层、发布层和经过身份验证的发布层。</li>
<li>选择片段后，其上下文将在整条消息中保留，使创作者能够跨内容块重复使用片段字段，无需重新选择。</li>
<li>Journey Optimizer 中新增了专用的内容片段列表页面，可改进生命周期管理；用户可以识别不同步的片段，并触发手动同步以保持最新状态。</li>
<li>区域设置和变体支持功能现在让营销人员能够更有针对性地使用同一内容片段的不同版本。</li>
<li>现在，您可以灵活控制 Adobe Journey Optimizer 访问 Adobe Experience Manager 内容的方式。 此版本带来了为历程和营销活动中使用的内容片段<strong>切换源存储库</strong>的功能。</li>
<li>现已兼容<b>Managed Services</b>，您可以直接在 Journey Optimizer 中查看、访问和使用 Adobe Experience Manager 内容片段以进行个性化。 只需在配置设置中添加您的 Adobe Experience Manager Managed Services 存储库 URL 即可完成一次性设置。</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI Assistant 与 Adobe Experience Manager Asset Essentials 集成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在生成电子邮件、网页和推送通知时，AI Assistant 现在会直接从您的 Adobe Experience Manager Assets 中自动获取<b>品牌批准的图像</b>。 这样一来，您无需手动搜索 Assets 或依赖通用 AI 回退方案，即可确保每个视觉元素都精准无误且符合品牌规范。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI Assistant 内容生成功能的增强</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此版本通过更强大的图像编辑、更可靠的品牌提取，以及图像流中的内容真实性支持，改进了<strong>AI Assistant</strong>内容生成体验：</p>
<ul>
<li><strong>AI 图像编辑</strong>现在可在图像生成流程中使用，包括 Firefly 第三方模型支持，因此无需离开 Assistant 即可优化源图像。</li>
<li><strong>品牌信号提取</strong>可提供更高质量的结果。 当所选页面信号不足时，改进后的回退机制会自动填充颜色、字体排版、文案规范和其他品牌属性。</li>
<li><strong>基于 Web 的品牌提取</strong>更加可靠。 改进了超时处理功能，有助于防止加载缓慢的页面、弹出窗口和 Cookie 横幅阻止提取。</li>
<li>图像流中现在支持<strong>内容真实性 (CAI)</strong>。 此版本还修复了参考图像上传问题，并优化了对未包含现有 C2PA 清单图像的处理。</li>
</ul>
</td>
</tr>
</tbody>
</table>

+++


### 电子邮件渠道 {#june-26-email}

此版本中的电子邮件渠道添加了以下改进。

* **URL 参数加密** — 您现在可以加密添加到电子邮件消息中的跟踪和登陆页链接中的 URL 参数。 这为敏感参数数据提供了额外的安全层。 此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。 [了解更多信息](../personalization/url-parameter-encryption.md)

  可用日期：2026 年 6 月 1 日

* **密钥注册表的新权限** – 现在需要具有两项新权限才能访问和管理 URL 参数加密所需的密钥：**管理密钥注册表**&#x200B;和&#x200B;**查看密钥注册表**。 [了解更多信息](../administration/high-low-permissions.md#administration-permissions)

  可用日期：2026 年 6 月 1 日

<table>
<thead>
<tr>
<th><strong>启用电子邮件大小缩减</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 现在包含一个选项，该选项通过去除不必要的空格、注释和冗余代码来减小电子邮件的 HTML 大小，而不会影响电子邮件的渲染方式。</p>
<p>这可避免某些电子邮件提供商用于标记或拒绝邮件的大小阈值，从而提高可投放性，并可能缩短收件人的加载时间。</p>
<p><img src="assets/do-not-localize/email-size-optimization.gif"></p>
<p>有关更多信息，请参阅<a href="../email/create-email.md#optimize-html-size">详细文档</a>。</p>
<p>发布日期：2026年6月26日</p>
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
<p>例如，在将文本组件用作电子邮件设计器中的可编辑字段时，您可以直接设置内容格式（例如，粗体和斜体）并插入超链接。</p>
<p><img src="assets/do-not-localize/rich-text-editable-fields.gif"></p>
<p>有关更多信息，请参阅<a href="../content-management/customizable-fragments.md#rich-text-visual">详细文档</a>。</p>
<p>发布日期：2026年6月19日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件设计器中的内容检查</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 现在包括直接在电子邮件设计器中进行的自动技术验证，可帮助您在发送之前捕获 HTML 和 CSS 问题。</p>
<p>检查涵盖不支持的元素，例如 <code>&lt;script&gt;</code> 和 <code>&lt;base&gt;</code> 标记、可中断 Microsoft Outlook 中布局的空 div、HTML Meta Refresh 标记，以及触发 Gmail 渲染失败的 CSS 或 HTML 大小阈值。</p>
<p>结果直接在创作面板中显示为错误、警告或信息性声明，其中包含上下文详细信息和一键式修复（如果可用），因此无需离开编辑器即可解决问题。</p>
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p><img src="assets/do-not-localize/content-check.gif"></p>
<p>有关更多信息，请参阅<a href="../email/content-check.md">详细文档</a>。</p>
<p>发布日期：2026年6月18日</p>
</td>
</tr>
</tbody>
</table>

* **增强的图像转 HTML 转换器** — 现已提供新版本的图像转 HTML 转换器功能，从而提高生成 HTML 的准确性。 此更新利用更高层的 LLM 模型，从图像输入提供更精确、更可靠的 HTML 输出。

  发布日期：2026年6月18日

+++ 即将推出 — **下面的信息可能会发生更改。**

<table>
<thead>
<tr>
<th><strong>电子邮件设计器中的模块</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Email Designer 现在内置了一个现成的布局模块库——包括页眉、产品卡片、信息块和页脚等——您可以将这些模块直接拖放到电子邮件画布中。</p>
<p>每个模块都预先配置了可编辑的属性（图像、标题、文本、按钮、链接），并且可以通过 WYSIWYG 界面完全自定义，从而加快电子邮件创建速度，而无需您从头开始构建结构。</p>
<p>发布日期：2026 年 6 月下旬</p>
</td>
</tr>
</tbody>
</table>

+++

### 内容 &amp; 集成 {#june-26-integration}

此版本将为内容管理和集成带来以下功能和改进。

<table>
<thead>
<tr>
<th><strong>Journey Optimizer 中 Adobe Experience Manager 内容片段的改进</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此版本带来了多项增强功能，使<strong>Adobe Experience Manager 内容片段</strong>在 Journey Optimizer 创作工作流中更具可用性、更易于治理，且更适合投入生产环境：</p>
<ul>
<li>Journey Optimizer 现在支持从多个 Adobe Experience Manager 配置中获取内容片段，包括创作层、发布层和经过身份验证的发布层。</li>
<li>选择片段后，其上下文将在整条消息中保留，使创作者能够跨内容块重复使用片段字段，无需重新选择。</li>
<li>Journey Optimizer 中新增了专用的内容片段列表页面，可改进生命周期管理；用户可以识别不同步的片段，并触发手动同步以保持最新状态。</li>
<li>区域设置和变体支持功能现在让营销人员能够更有针对性地使用同一内容片段的不同版本。</li>
<li>现在，您可以灵活控制 Adobe Journey Optimizer 访问 Adobe Experience Manager 内容的方式。 此版本带来了为历程和营销活动中使用的内容片段<strong>切换源存储库</strong>的功能。</li>
<li>现已兼容<b>Managed Services</b>，您可以直接在 Journey Optimizer 中查看、访问和使用 Adobe Experience Manager 内容片段以进行个性化。 只需在配置设置中添加您的 Adobe Experience Manager Managed Services 存储库 URL 即可完成一次性设置。</li>
</ul>
<p>有关更多信息，请参阅<a href="../integrations/aem-fragments-gs.md">详细文档</a>。</p>
<p>发布日期：2026年6月18日</p>
</td>
</tr>
</tbody>
</table>

+++ 即将推出 — **下面的信息可能会发生更改。**

<table>
<thead>
<tr>
<th><strong>AI Assistant 与 Adobe Experience Manager Asset Essentials 集成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在生成电子邮件、网页和推送通知时，AI Assistant 现在会直接从您的 Adobe Experience Manager Assets 中自动获取<b>品牌批准的图像</b>。 这样一来，您无需手动搜索 Assets 或依赖通用 AI 回退方案，即可确保每个视觉元素都精准无误且符合品牌规范。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI Assistant 内容生成功能的增强</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此版本通过更强大的图像编辑、更可靠的品牌提取，以及图像流中的内容真实性支持，改进了<strong>AI Assistant</strong>内容生成体验：</p>
<ul>
<li><strong>AI 图像编辑</strong>现在可在图像生成流程中使用，包括 Firefly 第三方模型支持，因此无需离开 Assistant 即可优化源图像。</li>
<li><strong>品牌信号提取</strong>可提供更高质量的结果。 当所选页面信号不足时，改进后的回退机制会自动填充颜色、字体排版、文案规范和其他品牌属性。</li>
<li><strong>基于 Web 的品牌提取</strong>更加可靠。 改进了超时处理功能，有助于防止加载缓慢的页面、弹出窗口和 Cookie 横幅阻止提取。</li>
<li>图像流中现在支持<strong>内容真实性 (CAI)</strong>。 此版本还修复了参考图像上传问题，并优化了对未包含现有 C2PA 清单图像的处理。</li>
</ul>
</td>
</tr>
</tbody>
</table>

+++

### 报表 {#june-26-reporting}

此版本中的报表添加了以下改进。

* **电子邮件报表的新估计点击量度** — 为了更准确地查看实际客户参与情况，现在提供了跨历程、营销活动和渠道报表的新估计量度。

   * **预计的CTR**（点进率）：计算为相对于已投放邮件总数的预计点击。

   * **预计的CTOR**（点击打开率）：计算为预计点击次数与预计打开总数的比率。

  发布日期：2026年6月25日

### 管理 {#june-26-administration}

此版本中的管理和数据管理添加了以下改进。

* [!BADGE 重要]{type=Informative}**AJO 消息反馈事件数据集正在迁移至批量摄取** — **AJO 消息反馈事件数据集**&#x200B;正在从流式摄取模式迁移至批量摄取模式。 因此，预计此数据集的数据延迟最长为 2 小时。 如果您在 Customer Journey Analytics 中构建报告或使用此数据集运行查询，请在未来将这种增加的延迟考虑在内。 [了解更多信息](../data/datasets-query-examples.md#message-feedback-event-dataset)

  发布日期：2026 年 6 月 10 日

* **营销活动生命周期事件的客户警报** — 新的系统警报现在会通知您有关操作和 API 触发的营销活动的关键生命周期事件。 在沙盒级别进行订阅。 [了解更多信息](../reports/alerts.md)

  可用日期：2026 年 6 月 1 日


+++ 即将推出：**以下信息可能会有所变更**

* **Web 应用程序防火墙 (WAF) IP 允许列表**：Adobe Journey Optimizer 现在支持为着陆页启用 Web 应用程序防火墙 (WAF) IP 允许列表功能，使组织能够强制要求所有传入请求仅通过其配置的 WAF 基础架构进行路由。 借助这项增强功能，客户可以将 Journey Optimizer 配置为拒绝任何绕过 WAF 层的直接请求，从而确保 Imperva 等工具中定义的安全策略得到一致应用。 此功能增强了对网络访问要求严格的企业的安全防护能力，使其能够完全掌控流向 AJO 托管着陆页的流量

  发布日期：2026 年 6 月下旬

+++


### Mobile 消息（短信、彩信、RCS &amp; LINE） {#june-26-mobile}

此版本将为 Mobile 消息传递带来以下改进。

* **短信报告的唯一点击次数**：短信报告新增了&#x200B;**唯一点击次数**&#x200B;模块，将电子邮件报告现有的细粒度效果跟踪能力，同样带到了短信。

* **短信：显示使用情况指标**：对于直接通过 Adobe Journey Optimizer 购买短信的客户，新增了&#x200B;**短信使用情况仪表板**。 您现在可以查看和跟踪最近 90 天的消息发送指标，并按移动始发 (MO) 和移动终止 (MT) 消息进行分类。 此数据也支持通过 CSV 下载，让您更全面地掌握和控制短信支出。 [了解详情](../mobile/sms-usage-report.md)

* **短信的预计点击量报表** — 现在，历程、营销活动和渠道报表中针对电子邮件和短信提供了新的预计点击量量量度。 此指标不包括已识别的机器人和非人工交互 (NHI) 流量，以便更清楚地了解真实的客户参与情况。 现有的&quot;点击量&quot;指标仍然可用，并将继续报告总点击量。

+++ 即将推出 — **下面的信息可能会发生更改。**

* **LINE 频道：创作功能更改**：LINE 频道 UI 已升级，具有高级消息创作功能。 此版本引入了对&#x200B;**多种消息格式**&#x200B;的支持，包括文本、图像、图像映射、轮播和 Flex（JSON 编辑器），以及实时设备预览。 用户现在可以管理由最多五条有序消息组成的分组消息（提供添加、删除和重新排序控件），并使用集成的个性化编辑器实现经过验证的动态消息传送。

+++

### 可用性改进 {#june-26-usability}

+++ 即将推出 — **下面的信息可能会发生更改。**

* **历程和营销活动文件夹**：您现在可以将历程和营销活动整理到 **文件夹** 中，以改善界面中的导航和管理功能。

+++

<!--
+++ Coming soon — **Information below is subject to change.**

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default execution field set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.

  Availability date: Early June, 2026

+++
-->
