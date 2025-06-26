---
solution: Journey Optimizer
product: journey optimizer
title: 定义历程的属性
description: 了解如何使用Adobe Journey Optimizer设置历程的属性
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: 历程，配置，属性
exl-id: 6c21371c-6cbc-4d39-8fe6-39f1b8b13280
source-git-commit: 7d5d27d9509dd80fece2e360d58437d26df7c4de
workflow-type: tm+mt
source-wordcount: '2392'
ht-degree: 15%

---

# 设置历程属性 {#jo-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="历程属性"
>abstract="此部分显示历程属性。默认情况下，只读参数是隐藏的。可用设置取决于历程的状态、您的权限和产品配置。"

## 访问历程的属性 {#access-properties}

历程的属性集中在右边栏中。 默认情况下，创建新历程时会显示此部分。 对于现有历程，单击历程名称旁边的铅笔图标以将其打开。

在此部分中，定义历程的名称、添加描述并设置历程全局属性。

您可以：

* 将Adobe Experience Platform统一标记分配给您的历程，以轻松对其进行分类并改进营销活动列表中的搜索。 [了解如何使用标记](../start/search-filter-categorize.md#tags)
* 选择您的历程量度。 [了解如何配置和跟踪您的历程量度](success-metrics.md)
* 管理[进入和重新进入](#entrance)。 用户档案入口管理取决于历程类型。 详细信息可在[此页面](entry-management.md)上找到
* 管理[对数据的访问](#manage-access)
* 选择历程和配置文件[时区](#timezone)
* 选择自定义[开始和结束日期](#dates)
* 在历程活动中定义[超时持续时间](#timeout)（仅适用于管理员用户）
* 使用[冲突管理工具](#conflict)监视冲突并设置历程优先级

![](assets/new-journey-properties.png){width="80%"}{zoomable="yes"}

>[!NOTE]
>
>对于实时历程，此屏幕仅显示发布日期和发布历程的用户名称。

使用&#x200B;**复制技术详细信息**&#x200B;选项，您可以复制有关历程的技术信息，供支持团队用于进行故障排除。 已复制以下信息：`JourneyVersion UID`、`OrgID`、`orgName`、`sandboxName`、`lastDeployedBy`、`lastDeployedAt`。

在此页面[&#128279;](expression/journey-properties.md)上进一步了解与给定用户档案的历程相关的技术字段以及如何使用它们。

## 入口和重入 {#entrance}

用户档案进入模式在历程级别的右配置窗格中定义。 下文介绍了相关设置。

用户档案入口管理取决于历程类型。 在[此页面](entry-management.md)上了解有关用户档案进入和重新进入管理的更多信息。

### 允许重入  {#allow-reentrance}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_entrance"
>title="允许重入"
>abstract="默认情况下，允许重入新的历程。例如，如果您想在有人进入商店时提供一次性的礼物，则您可以取消选中&#x200B;**允许重入**&#x200B;选项。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="轮廓入口管理"

默认情况下，允许重入新的历程。对于“一次性”历程，您可以取消选中&#x200B;**允许重新进入**&#x200B;选项，例如，如果要在人员进入商店时提供一次性礼品。

### 重入等待期  {#reentrance-wait}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_re-entrance_wait"
>title="重入等待期"
>abstract="设置允许用户档案在单一历程中再次进入历程之前的等待时间。 这可以防止用户在选定的持续时间内重新进入历程。最长持续时间：90 天。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="轮廓入口管理"

激活&#x200B;**允许重新进入**&#x200B;选项时，将显示&#x200B;**重新进入等待期**&#x200B;字段。 使用该字段，您可以定义允许轮廓再次进入单一历程（以事件或受众资格筛选开始）之前等待的时间。这可防止同一事件多次错误触发历程。默认情况下，字段设置为 5 分钟。最长持续时间为90天。

## 管理访问权限 {#manage-access}

您可以根据访问标签限制对历程的访问。

要为历程分配自定义数据使用标签，请单击&#x200B;**[!UICONTROL 管理访问标签]**&#x200B;图标并选择一个或多个标签。

[了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md)

## 历程和配置文件时区 {#timezone}

时区在历程级别定义。 您可以输入固定时区，或使用Adobe Experience Platform配置文件定义历程时区。 如果在Adobe Experience Platform配置文件中定义了时区，则可以在旅程中检索该时区。

[了解有关时区管理的更多信息](../building-journeys/timezone-management.md)

## 开始和结束日期 {#dates}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_start_date"
>title="开始日期"
>abstract="选择轮廓可以开始进入历程的日期。如果未设置开始日期，则它会默认为历程的发布日期。"

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_end_date"
>title="结束日期"
>abstract="设置历程结束的日期。在此日期，活动用户档案自动退出历程，不允许新进入。"

默认情况下，用户档案可在发布后立即进入您的历程，并可一直保留，直到达到[全局历程超时](#global_timeout)。 唯一的例外是循环读取受众历程，激活了&#x200B;**在重复时强制重入**，该历程在下一次发生事件的开始日期结束。

如果需要，您可以定义自定义&#x200B;**开始日期**&#x200B;和&#x200B;**结束日期**。 这允许用户档案在特定日期进入您的历程，并在到达结束日期时自动退出。

## 超时 {#timeout}

### 历程活动超时 {#timeout_and_error}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_timeout"
>title="超时或错误"
>abstract="指定历程可以尝试执行某个操作或评估某个条件多长时间，这个时间过去后即视为超时。建议值介于 1 至 30 秒之间。"

编辑操作或条件活动时，您可以定义替代路径以防出现错误或超时。 如果处理询问第三方系统的活动超过了历程属性的&#x200B;**[!UICONTROL 超时或错误]**&#x200B;字段中定义的超时持续时间，将选择第二个路径以执行潜在的回退操作。

建议值介于 1 至 30 秒之间。

如果历程对时间敏感（例如：对人员的实时位置做出反应），我们建议您定义一个非常短的&#x200B;**[!UICONTROL 超时或错误]**&#x200B;值，因为您的操作延迟的时间不能超过几秒。 如果您的旅程不太时效性，则可以使用较长的值，为调用的系统留出更多时间来发送有效响应。

历程还会使用全局超时，如下所述。

### 全局历程超时 {#global_timeout}

除了历程活动中使用的[超时](#timeout_and_error)之外，还应用了全局历程超时。 它不会显示在界面中，无法更改。

此全局超时在个人进入历程&#x200B;**91天**&#x200B;后停止个人进度。 这意味着个人的历程不能超过91天。 在此超时时段后，个人数据将被删除。 超时时间结束时仍在历程中流动的个人将被停止，并且不会在报表中考虑他们。 因此，您可能会看到进入历程的人员多于退出的人员。

由于91天的历程超时，当历程不允许重新进入时，我们无法确保重新进入阻止将工作超过91天。 事实上，当我们删除有关进入旅程91天后进入旅程的人员的所有信息时，我们无法知道该人员是超过91天前进入的。

仅当个人在历程中剩余的时间足以在91天历程超时之前完成等待持续时间时，他或她才能进入等待活动。 请参阅[此页](../building-journeys/wait-activity.md)。

#### 存留时间(TTL)和数据保留常见问题解答 {#timeout-faq}

从Adobe Journey Optimizer 2024年6月版本开始，历程全局超时已从30天移动到91天。 影响列于以下常见问题解答中：

单一历程的&#x200B;**&#x200B;**
<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>推出TTL扩展后发布的历程会发生什么情况？</p>
    </td>
    <td>
      <p>进入新历程的用户档案的TTL将自动为91天。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>进入在TTL扩展启动之前发布的历程的个人资料会发生什么情况？</p>
    </td>
    <td>
      <p>用户档案的TTL为30天（HIPAA为7天），与最初发布历程的时间一致。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>启动TTL扩展后，已进入历程的用户档案会发生什么情况？</p>
    </td>
    <td>
      <p>根据历程的原始发布时间，用户档案将保留30天（HIPAA为7天）的TTL。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>在TTL扩展启动后重新发布的先前历程版本中的配置文件会发生什么情况？</p>
    </td>
    <td>
      <p>用户档案的TTL将保持为30天（对于HIPAA为7天），与原始历程版本的发布时间一致。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>对于在TTL扩展启动后进入重新发布的历程版本的新用户档案，会发生什么情况？</p>
    </td>
    <td>
      <p>用户档案的TTL为91天，与新重新发布的历程版本的TTL匹配。</p>
    </td>
  </tr>
</table>

**区段触发器历程**

<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>在TTL扩展之后发布的新一次性历程会发生什么情况？</p>
    </td>
    <td>
      <p>进入新历程的用户档案的TTL自动为91天。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>在TTL扩展后发布的不强制重新进入的新定期历程会发生什么情况？</p>
    </td>
    <td>
      <p>进入新历程的用户档案的TTL自动为91天。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>在TTL扩展后发布的具有强制重新进入的新循环历程会发生什么情况？</p>
    </td>
    <td>
      <p>进入新历程的用户档案的TTL将等于重复周期。 例如，如果历程每天运行，则TTL将为1天。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>进入在TTL扩展启动之前发布的历程的个人资料会发生什么情况？</p>
    </td>
    <td>
      <p>该配置文件的TTL为30天（对于HIPAA，为7天），与原始发布时间一致。 对于强制重新进入的定期历程，TTL将与定期时段匹配。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>启动TTL扩展后，通过历程运行的用户档案会发生什么情况？</p>
    </td>
    <td>
      <p>根据历程的原始发布时间，用户档案将保留30天（HIPAA为7天）的TTL。 对于强制重新进入的定期历程，TTL将与定期时段匹配。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>在发布TTL扩展后重新发布的先前历程版本中，正在运行的配置文件会发生什么情况？</p>
    </td>
    <td>
      <p>用户档案的TTL将保持为30天（对于HIPPA为7天），与原始历程版本的发布时间一致。 对于强制重新进入的定期历程，TTL将与定期时段匹配。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>对于在TTL扩展启动后进入重新发布的历程版本的新用户档案，会发生什么情况？</p>
    </td>
    <td>
      <p>用户档案的TTL为91天，与新重新发布的历程版本的TTL匹配。 对于强制重新进入的定期历程，TTL将与定期时段匹配。</p>
    </td>
  </tr>
</table>

## 合并策略 {#merge-policies}

从Adobe Experience Platform检索配置文件数据时，Adobe Journey Optimizer使用合并策略。 根据历程类型，使用不同的合并策略：

* 在读取受众或受众资格历程中：使用受众的合并策略
* 在单一事件历程中：使用默认合并策略
* 在业务事件历程中：在以下读取受众活动中使用来自目标受众的合并策略

Adobe Journey Optimizer会应用在整个历程中使用的合并策略。 因此，如果在历程中使用多个受众（例如使用[`inAudience`函数](functions/functioninaudience.md)中的），这将导致与历程使用的合并策略不一致，从而引发错误并阻止发布。 但是，如果在消息个性化中使用不一致的受众，则不会触发警报，即使存在不一致也是如此。 因此，强烈建议在消息个性化中使用此受众时，检查与受众关联的合并策略。

要了解有关合并策略的更多信息，请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/merge-policies/overview){target="_blank"}。

>[!NOTE]
>
>更新受众合并策略时，必须重新发布（或复制）引用该受众的任何活动历程。 更改合并策略会有效地创建当前历程无法访问的“新”受众，从而确保数据一致性。

## 退出标准 {#exit-criteria}

>[!CONTEXTUALHELP]
>id="ajo_journey_exit_criterias"
>title="历程退出标准"
>abstract="此部分显示退出标准选项。您可以为历程创建一个或多个退出标准规则。"

### 描述 {#exit-criteria-desc}

通过添加退出条件，您可以在事件发生后（例如：购买）或符合受众的条件时，让用户档案立即退出历程。这将阻止用户从历程收到任何进一步的通信。

当配置文件不再满足历程的目的时，您可能希望将其从历程中删除。 这可以通过与目标管理密切相关的&#x200B;**全局退出标准**&#x200B;来实现。

**示例用例**

营销人员具有包含一系列通信的促销历程。 每一次通信都旨在促使客户进行购买。 一旦完成购买，客户就不应收到系列中的其余消息。 通过定义退出标准，将从历程中删除购买的所有用户档案。

### 配置和使用情况 {#exit-criteria-config}

退出标准在历程级别设置。 一个历程可以有多个退出条件。 如果您设置了多个退出条件，则使用`OR`逻辑从上到下进行评估。 因此，如果您具有退出标准A和退出标准B，则评估为&#x200B;**或** B。将在历程的每个步骤中评估标准。

要&#x200B;**创建**&#x200B;退出条件，请执行以下步骤：

1. 打开您的历程。

1. 单击位于历程画布右上角的![](assets/do-not-localize/Smock_UserCheckedOut_18_N.svg) **[!UICONTROL 显示退出标准]**&#x200B;图标。

1. 选择&#x200B;**[!UICONTROL 添加退出条件]**。

1. 输入&#x200B;**标签**&#x200B;并选择您的退出标准是基于&#x200B;**事件**&#x200B;还是&#x200B;**受众**。

   * 对于基于事件的退出条件（例如下载应用程序或向购物车添加产品），请仅选择单一事件。
   * 对于基于受众的退出标准，例如检查客户在过去24小时内是否购买的受众，请选择一个受众。 注意：使用受众的退出标准可能需要长达10分钟才能生效。

您可以添加多个退出条件。

![](assets/exitcriteria-sample.png){width="40%" align="left"}

### 护栏和限制 {#exit-criteria-guardrails}

以下护栏和限制适用于历程退出标准功能：

* 退出条件仅在草稿状态下定义
* 事件和基于事件的退出标准之间的历程命名空间一致性

## 历程计划 {#schedule}

**[!UICONTROL 计划]**&#x200B;部分仅在画布中放置&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动时可用。 它允许您定义历程应运行的特定日期/时间和频率。 [了解如何计划读取受众历程](../building-journeys/read-audience.md)

## 冲突管理 {#conflict}

历程属性中的&#x200B;**[!UICONTROL 冲突管理]**&#x200B;部分允许您监视冲突并区分历程的优先级。 您可以：

* 应用&#x200B;**规则集**&#x200B;以根据上限规则将此历程排除到部分受众。 [了解如何使用规则集](../conflict-prioritization/rule-sets.md)

* 为历程分配&#x200B;**优先级得分**，范围为0到100。 数字越大，表示优先级越高。此处插入的优先级值由此历程中包含的任何入站操作（例如应用程序内）继承。[了解如何使用优先级得分](../conflict-prioritization/priority-scores.md)

  对于在其他营销活动或历程中使用相同入站渠道配置的情况，系统会向收件人显示优先级分数最高的入站操作。如果多个历程或营销活动具有相同的分数，则会选择最近修改的元素。

* **查看与其他历程、营销活动或渠道配置的冲突**。 如果您希望识别受众、开始和结束日期、渠道配置、渠道或规则集上的重叠，则可以在此处查看潜在冲突。 [了解如何识别历程中的潜在冲突](../conflict-prioritization/conflicts.md)
