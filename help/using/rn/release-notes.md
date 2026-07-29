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
source-git-commit: 2411f0ba2371933c3af101603c28032e9cdcc7d2
workflow-type: tm+mt
source-wordcount: 1474
ht-degree: 28%

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

## 2026年7月发行说明 {#july-26-updates}

### 忠诚度挑战 {#july-26-loyalty}

Journey Optimizer引入了忠诚度挑战，这是此版本中的一项新功能。

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
<p>有关更多信息，请参阅<a href="../loyalty-challenges/get-started.md">详细文档</a>。</p>
<p> 发布日期： 2026年7月28日</p>
</td>
</tr>
</tbody>
</table>

### 出站渠道 {#july-26-outbound-channels}

此版本中引入了以下功能。

<table>
<thead>
<tr>
<th><strong>渠道优化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将历程或营销活动操作配置为包含多个出站渠道（电子邮件、推送、短信），并让Journey Optimizer通过最佳渠道为每个客户自动投放。 提供了三种优化模式：</p>
<ul>
<li>手动排名：指定您的首选渠道顺序。</li>
<li>客户偏好设置：使用客户个人资料中的偏好渠道（体验数据模型同意和偏好设置属性）。</li>
<li>基于人工智能模型的排名：使用机器学习倾向分数推断每位客户最有效的渠道。</li>
</ul>
<p>当排名最前的渠道不可用（未选择启用、频率限制或未配置）时，系统回退到下一个可用渠道。</p>
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p><img src="assets/do-not-localize/channel-optimization.gif"></p>
<p>有关更多信息，请参阅<a href="../building-journeys/channel-optimization.md">详细文档</a>。</p>
<p>发布日期： 2026年7月22日</p>
</td>
</tr>
</tbody>
</table>

### 历程 {#july-26-journeys}

在此版本中，历程中添加了以下功能和改进。
<table>
<thead>
<tr>
<th><strong>新用户界面</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>为历程画布引入了<b>新用户界面</b>，提高了大型历程的性能、提供了自动布局以提高可读性，并提供了引导式创作体验。</p>
<p><img src="../building-journeys/assets/journey-new-canvas.png"></p>
<p>要切换到新UI，请单击<b>新体验</b>按钮。 此设置会在历程级别保存，因此默认情况下，历程会在新体验中重新打开。 要还原，请单击<b>旧体验</b>。 <a href="../building-journeys/using-the-journey-designer.md#canvas-capabilities">了解详情</a>。</p>
<p><img src="../building-journeys/assets/journey-new-experience-switch.png"></p>
<p> 发布日期： 2026年7月16日</p>
</td>
</tr>
</tbody>
</table>

* 
  * [!BADGE 弃用]{type=Negative} **受众资格节点和退出标准不再支持批量受众** — 从2026年9月开始，Journey Optimizer将阻止在“受众资格”节点或退出标准中使用批量受众的任何历程的发布。 历程画布中已显示验证警告。  现有的实时历程不受影响。 包含此配置的新历程、草稿历程和重复历程必须在2026年9月之前更新。 在“受众资格”节点中使用流式受众，或切换到“读取受众”活动。 对于退出标准，请使用流式受众。 [了解如何迁移您的历程](../building-journeys/aq-batch-audiences-migration.md)

### 电子邮件设计器 {#july-26-email}

此版本中的电子邮件渠道添加了以下功能。

<table>
<thead>
<tr>
<th><strong>电子邮件Designer中的内容检查（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 现在包括直接在电子邮件设计器中进行的自动技术验证，可帮助您在发送之前捕获 HTML 和 CSS 问题。</p>
<p>检查涵盖不支持的元素，例如 <code>&lt;script&gt;</code> 和 <code>&lt;base&gt;</code> 标记、可中断 Microsoft Outlook 中布局的空 div、HTML Meta Refresh 标记，以及触发 Gmail 渲染失败的 CSS 或 HTML 大小阈值。</p>
<p>结果直接在创作面板中显示为错误、警告或信息性声明，其中包含上下文详细信息和一键式修复（如果可用），因此无需离开编辑器即可解决问题。</p>
<p>此功能此前以“有限可用版”形式推出，现已对所有客户可用。</p>
<p><img src="assets/do-not-localize/content-check.gif"></p>
<p>有关更多信息，请参阅<a href="../email/content-check.md">详细文档</a>。</p>
<p>发布日期： 2026年7月16日</p>
</td>
</tr>
</tbody>
</table>

### 编排的营销活动 {#july-26-oc}

在此版本中，编排的营销活动中即将提供以下功能和改进。

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
<p>有关更多信息，请参阅<a href="../orchestrated/activities/load-file.md">详细文档</a>。</p>
<p> 发布日期：2026年7月6日</p>
</td>
</tr>
</tbody>
</table>

### 内容管理 {#july-26-content}

此版本中的内容管理添加了以下功能和改进。

* **片段清单中的快速启动快捷方式** — 您现在可以使用&#x200B;**[!UICONTROL 更多操作]**&#x200B;按钮从片段列表中快速访问常用操作。 可用的快捷方式包括编辑片段、打开其详细信息以及放弃草稿版本。 [了解详情](../content-management/manage-fragments.md#quick-launch-fragments)

  ![](../content-management/assets/fragment-quick-launch.png)

* 模板清单中的&#x200B;**快速启动快捷方式** — “内容模板”列表中的&#x200B;**[!UICONTROL 更多操作]**&#x200B;按钮现在提供对常用操作的快速访问：编辑模板详细信息、模拟内容和删除模板。 对于电子邮件模板，使用其他快捷方式可以编辑主题行和电子邮件正文、查看或发送验证、运行垃圾邮件报告以及呈现电子邮件。 [了解详情](../content-management/access-content-templates.md#quick-launch-templates)

  ![](../content-management/assets/content-template-quick-launch.png)

### 内容 &amp; 集成 {#july-26-integration}

此版本将为内容管理和集成带来以下功能和改进。

* **决策项目的动态自定义属性** — 决策项目自定义属性现在可以在交付时使用配置文件、上下文和受众数据进行个性化。 这消除了维护次要内容变体的重复选件的需要，使营销人员管理更少、更灵活的决策项。 [了解更多信息](../experience-decisioning/items.md#attributes)

  发布日期： 2026年7月27日

* **AJO MCP服务器新工具** - [!DNL Adobe Journey Optimizer] MCP服务器现在公开五个额外的只读&#x200B;**渠道配置工具**，使您可直接从AI助手查询渠道配置、支持资源和营销操作。 您现在可以使用&#x200B;**列表渠道配置**（跨所有AJO渠道）、**获取渠道配置**、**列表配置资源**、**获取配置资源**&#x200B;和&#x200B;**列表营销操作**。 [了解更多信息](../integrations/ajo-mcp.md#mcp-tools)

  发布日期： 2026年7月9日

* **个性化表达式中的新辅助函数** — 个性化表达式中现在有新辅助函数：

  * `appendQueryParams`：将查询参数附加到URL，如果键已存在，则替换该参数。
  * `dateBetween`：检查日期是否在开始和结束日期范围内（包括）。
  * `equalsAnyIgnoreCase`：当字符串与任何提供的值匹配时返回true，忽略大小写。
  * `getUrlFragment`：提取URL的片段部分（#之后的部分）。
  * `join`：使用分隔符将数组元素串联为单个字符串。
  * `decode64`：对Base64编码的字符串进行解码。 如果输入无效Base64，则原始输入字符串将保持不变。
  * `parseJson`：将JSON字符串解析为可在模板中使用的结构化变量。
  * `valueAtPath`：将数据路径中的值分配给模板变量，并通过可选索引从数组或集合中提取特定元素。
  * `abort`：在呈现期间到达时停止消息投放。

  `concat`函数也得到了增强，现在支持两个或更多参数。

  此外，以下模板迁移函数现在可用于协助将现有模板迁移到Journey Optimizer：

  * `ampCompare`：使用指定的比较运算符比较两个值。
  * `ampSubstr`：返回指定开始索引和结束索引之间的字符串的一部分。
  * `compareTo`：按词典比较两个字符串。

  [了解有关辅助函数的更多信息](../personalization/functions/functions.md)

  发布日期： 2026年7月28日

### 管理 {#july-26-administration}

此版本中的管理和数据管理添加了以下改进。

* **数据集生存时间(TTL)护栏 — 现有沙盒** — 从&#x200B;**2026年10月1日**&#x200B;开始，将在&#x200B;**现有客户沙盒和组织**&#x200B;上强制实施Journey Optimizer系统生成的数据集的生存时间(TTL)护栏（配置文件存储区为90天，数据湖为13个月）。 [了解详情](../data/datasets-ttl.md#ttl-guardrail)


