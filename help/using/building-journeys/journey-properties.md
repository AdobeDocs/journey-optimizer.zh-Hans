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
source-git-commit: e5b32629dac368855df09313edaad55e3bc143dc
workflow-type: tm+mt
source-wordcount: '1724'
ht-degree: 17%

---

# 设置历程属性 {#jo-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="历程属性"
>abstract="此部分显示历程属性。默认情况下，只读参数是隐藏的。可用设置取决于历程的状态、您的权限和产品配置。"

>[!CONTEXTUALHELP]
>id="ajo_journey_exit_criterias"
>title="历程退出标准"
>abstract="此部分显示退出标准选项。您可以为历程创建一个或多个退出标准规则。"


## 访问历程的属性 {#access-properties}

历程的属性集中在右边栏中。 默认情况下，创建新历程时会显示此部分。 对于现有历程，单击历程名称旁边的铅笔图标以将其打开。

在此部分中，您可以定义旅程的名称、添加描述以及：

* 管理 [进入和重入](#entrance)，
* 选择开始和结束 [日期](#dates)，
* 管理 [访问数据](#manage-access)，
* 定义 [超时持续时间](#timeout) 在历程活动中（仅适用于管理员用户），
* 选择历程和配置文件 [时区](#timezone)
* 将Adobe Experience Platform统一标记分配给您的历程，以轻松对其进行分类并改进营销活动列表中的搜索。 [了解如何使用标记](../start/search-filter-categorize.md#tags)

![](assets/journey32.png)

>[!NOTE]
>
>对于实时历程，此屏幕仅显示发布日期和发布历程的用户名称。

此 **复制技术详细信息** 允许您复制有关历程的技术信息，供支持团队用于进行故障排除。 将复制以下信息： `JourneyVersion UID`， `OrgID`， `orgName`， `sandboxName`， `lastDeployedBy`， `lastDeployedAt`.

详细了解与给定用户档案的历程相关的技术字段及其使用方法 [本页内容](expression/journey-properties.md).


## 进入和重新进入 {#entrance}

用户档案进入模式在历程级别的右配置窗格中定义。 下文介绍了相关设置。

用户档案入口管理取决于历程类型。 在中了解有关用户档案进入和重入管理的更多信息 [此页面](entry-management.md).

### 允许重新进入  {#allow-re-entrance}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_entrance"
>title="允许重新进入"
>abstract="默认情况下，允许重入新的历程。例如，如果您想在有人进入商店时提供一次性的礼物，则您可以取消选中&#x200B;**允许重入**&#x200B;选项。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="用户档案入口管理"

默认情况下，允许重入新的历程。您可以取消选中 **允许重新进入** “一次性”旅程选项，例如，如果您想在某人进入商店时提供一次性礼物。

### 重入等待期  {#re-entrance-wait}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_re-entrance_wait"
>title="重入等待期"
>abstract=" 设置在允许配置文件再次进入单一历程之前的等待时间。这可以防止用户在选定的持续时间内重新进入历程。最长持续时间：90 天。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="用户档案入口管理"

当 **允许重新进入** 选项已激活， **重新进入等待期** 字段。 使用该字段，您可以定义允许用户档案再次进入单一历程（以事件或受众鉴别开始）之前等待的时间。这可防止同一事件多次错误触发历程。默认情况下，字段设置为 5 分钟。最长持续时间为90天。


## 管理访问权限 {#manage-access}

要将自定义或核心数据使用标签分配给历程，请单击 **[!UICONTROL 管理访问权限]** 按钮。 [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

## 历程和配置文件时区 {#timezone}

时区在历程级别定义。 您可以输入固定时区，或使用Adobe Experience Platform配置文件定义历程时区。 如果在Adobe Experience Platform配置文件中定义了时区，则可以在旅程中检索该时区。

有关时区管理的更多信息，请参阅 [此页面](../building-journeys/timezone-management.md).

## 开始和结束日期 {#dates}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_start_date"
>title="开始日期"
>abstract="选择历程开始的日期。如果没有指定开始日期，则会自动设置为发布时间。"


>[!CONTEXTUALHELP]
>id="ajo_journey_properties_end_date"
>title="结束日期"
>abstract="选择历程的结束日期。达到该日期后，该历程中的配置文件会自动将其退出，并且新的无法再次进入。"

您可以定义 **开始日期**. 如果您尚未指定名称，则将在发布时自动定义它。

您还可以添加 **结束日期**. 这允许用户档案在到期时自动退出。如果未指定结束日期，则配置文件可以保留到 [全局历程超时](#global_timeout) （通常为91天）。 唯一的例外是具有以下特征的定期读取受众历程 **在重复时强制重新进入** 激活，在下一次事件的开始日期结束。

## 超时 {#timeout}

### 历程活动超时或错误 {#timeout_and_error}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_timeout"
>title="超时"
>abstract="定义历程在将其视为超时之前尝试执行操作或验证条件的时间量。"


编辑操作或条件活动时，您可以定义替代路径以防出现错误或超时。 如果处理询问第三方系统的活动超出了中定义的超时持续时间 **[!UICONTROL 超时或错误]** 在历程属性的字段中，将选择第二个路径来执行潜在的回退操作。

授权值介于1和30秒之间。

我们建议您定义一个非常短的 **[!UICONTROL 超时或错误]** 值(如果您的旅程对时间敏感（例如：对人员的实时位置做出反应），因为您的操作不能延迟超过几秒钟。 如果您的旅程不太时效性，则可以使用较长的值，为调用的系统留出更多时间来发送有效响应。

历程还会使用全局超时，如下所述。

### 全局历程超时 {#global_timeout}

除了 [timeout](#timeout_and_error) 在历程活动中使用，将应用全局历程超时。 它不会显示在界面中，无法更改。

此全局超时可停止历程中个人的进度 **91天** 他们进去之后。 这意味着个人的历程不能超过91天。 在此超时时段后，个人数据将被删除。 超时时间结束时仍在历程中流动的个人将被停止，并且不会在报表中考虑他们。 因此，您可能会看到进入历程的人员多于退出的人员。

由于91天的历程超时，当历程不允许重新进入时，我们无法确保重新进入阻止将工作超过91天。 事实上，当我们删除有关进入旅程91天后进入旅程的人员的所有信息时，我们无法知道该人员是超过91天前进入的。

仅当个人在历程中剩余的时间足以在91天历程超时之前完成等待持续时间时，他或她才能进入等待活动。 请参阅[此页](../building-journeys/wait-activity.md)。


#### 存留时间(TTL)和数据保留常见问题解答 {#timeout-faq}

从Adobe Journey Optimizer 2024年6月版本开始，历程全局超时已从30天移动到91天。 影响列于以下常见问题解答中：

**对于单一历程**
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

**对于区段触发历程**

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

从Adobe Experience Platform检索配置文件数据时，历程使用合并策略。 根据历程类型，使用不同的合并策略：

* 在读取受众或受众资格历程中：使用受众的合并策略
* 在单一事件历程中：使用默认合并策略
* 在业务事件历程中：在以下读取受众活动中使用来自目标受众的合并策略

历程将遵循在整个历程中使用的合并策略。 因此，如果旅程中使用多个受众（例如：在“inAudience”函数中），导致旅程使用的合并策略不一致，则会引发错误并阻止发布。 但是，如果在消息个性化中使用不一致的受众，则不会触发警报，即使存在不一致也是如此。 因此，强烈建议在消息个性化中使用此受众时，检查与受众关联的合并策略。

要了解有关合并策略的更多信息，请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/overview){target="_blank"}.
