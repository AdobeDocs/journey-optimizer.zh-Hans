---
title: 向优惠添加约束
description: 了解如何定义优惠的显示条件
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '2357'
ht-degree: 17%

---

# 向优惠添加约束 {#add-constraints}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="关于优惠约束"
>abstract="通过约束，您可以指定与其他优惠相比，该优惠如何确定优先级并呈现给用户。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_constraints"
>title="关于优惠约束"
>abstract="通过约束，您可以指定与其他优惠相比，该优惠如何确定优先级并呈现给用户。"

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="关于优惠优先级"
>abstract="在此字段中，您可以指定优惠的优先级设置。优先级是一个数字，用于对满足所有约束（例如资格、日期和上限）的优惠进行排名。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_priority"
>title="设置优先级"
>abstract="如果用户有资格获得多个优惠，则优先级有助于定义该优惠相对于其他优惠的优先级。优惠的优先级越高，与其他优惠相比其优先级就越高。"

利用约束，可定义显示优惠的条件。

1. 配置 **[!UICONTROL 优惠资格]**. [了解详情](#eligibility)

   ![](../assets/offer-eligibility.png)

1. 定义 **[!UICONTROL 优先级]** 与其他选件相比，如果用户符合多个选件的条件，则该选件具有相同的权限。 优惠的优先级越高，与其他优惠相比其优先级就越高。

   ![](../assets/offer-priority.png)

1. 指定优惠的 **[!UICONTROL 上限]**，表示优惠的展示次数。 [了解详情](#capping)

   ![](../assets/offer-capping.png)

1. 单击 **[!UICONTROL 下一个]** 以确认您定义的所有约束。

例如，如果设置了以下约束：

![](../assets/offer-constraints-example.png)

* 只有符合“金会员客户”决策规则的用户，才会考虑提供该优惠。
* 优惠的优先级设置为“50”，这意味着优惠将在优先级为1到49的优惠之前呈现，并且优先级至少为51的优惠之后呈现。
* 每个用户每月仅在所有投放位置中显示一次选件。

## 资格 {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_eligibility"
>title="定义资格"
>abstract="默认情况下，任何配置文件都有资格获得优惠，但您可以使用区段或决策规则将优惠限制为特定的配置文件。"

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="关于优惠资格"
>abstract="在此部分中，您可以使用决策规则来确定哪些用户有资格享受优惠。"
>additional-url="https://video.tv.adobe.com/v/329373" text="观看演示视频"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_total_profile_estimate"
>title="对配置文件的总体估计"
>abstract="当您选择区段或决策规则时，可以看到有关估计符合资格的配置文件的信息。"

此 **[!UICONTROL 优惠资格]** 部分允许您将优惠限制为您使用区段或决策规则定义的特定用户档案。

>[!NOTE]
>
>了解关于使用的更多信息 **区段** 对比 **决策规则** 在 [本节](#segments-vs-decision-rules).

* 默认情况下， **[!UICONTROL 所有访客]** 选项，这意味着任何用户档案都符合呈现优惠的条件。

   ![](../assets/offer-eligibility-default.png)

* 您还可以将优惠的呈现方式限制为一个或多个成员 [Adobe Experience Platform区段](../../segment/about-segments.md).

   为此，请激活 **[!UICONTROL 属于一个或多个区段的访客]** 选项，然后从左窗格添加一个或多个区段并使用 **[!UICONTROL 和]** / **[!UICONTROL 或]** 逻辑运算符。

   ![](../assets/offer-eligibility-segment.png)

* 如果要关联特定 [决策规则](../offer-library/creating-decision-rules.md) 对于选件，选择 **[!UICONTROL 按定义的决策规则]**，然后将所需规则从左窗格拖入 **[!UICONTROL 决策规则]** 区域。

   ![](../assets/offer_rule.png)

   >[!CAUTION]
   >
   >中当前不支持基于事件的优惠 [!DNL Journey Optimizer]. 如果您根据以下规则创建决策规则： [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target="_blank"}，您将无法在选件中利用它。

当您选择区段或决策规则时，可以看到有关估计符合资格的配置文件的信息。单击 **[!UICONTROL 刷新]** 以更新数据。

![](../assets/offer-eligibility-segment-estimate.png)

>[!NOTE]
>
>当规则参数包含不在配置文件中的数据（如上下文数据）时，配置文件估计不可用。 例如，一个资格规则，要求当前天气为≥80度。

### 使用区段与决策规则 {#segments-vs-decision-rules}

要应用约束，您可以将选件的选择限制为一个或多个选件的成员 **Adobe Experience Platform区段**，或者您可以使用 **决策规则**，这两种解决方案分别对应于不同的用法。

基本上，区段的输出是用户档案的列表，而决策规则是在决策过程中根据单个用户档案按需执行的功能。 这两种使用方式的区别详见下文。

* **区段**

   一方面，区段是一组Adobe Experience Platform配置文件，它们根据配置文件属性和体验事件匹配特定逻辑。 但是，选件管理不会重新计算区段，因为此区段在展示选件时可能不是最新的。

   了解中有关区段的更多信息 [本节](../../segment/about-segments.md).

* **决策规则**

   另一方面，决策规则基于Adobe Experience Platform中可用的数据，并决定可以向谁显示优惠。 在给定投放位置的优惠或决策中选择优惠后，每次做出决策时都会执行规则，从而确保每个用户档案都获得最新和最佳优惠。

   在中了解有关决策规则的更多信息 [本节](creating-decision-rules.md).

## 上限 {#capping}

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="关于优惠上限"
>abstract="在此字段中，可指定可呈现优惠的次数。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="使用上限"
>abstract="为避免过度招揽客户，请使用上限定义可呈现优惠的最大次数。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints.html#capping-change-date" text="更改日期可能会影响上限"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping"
>title="设置上限频率"
>abstract="您可以选择每天、每周或每月重置优惠上限计数器。请注意，保存优惠后，您将无法更改所选频率。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping_impression"
>title="印象"
>abstract="仅入站频道可将印象用作上限事件。"

上限用作约束，以定义可显示优惠的最大次数。

通过限制用户获得特定优惠的次数，您可以避免过度向客户提供报价，从而使用最佳优惠优化每个接触点。

要设置上限，请执行以下主要步骤。

1. 确保 **[!UICONTROL 包括上限]** 切换按钮处于选中状态。 默认情况下包含上限。

   >[!CAUTION]
   >
   >无法为之前创建的选件启用或禁用频率上限。 为此，您需要复制选件或创建新选件。

1. 定义哪些 **[!UICONTROL 设置事件上限]** 将被考虑以增加计数器。 [了解详情](#capping-event)

1. 设置可显示优惠的次数。 [了解详情](#capping-count)

1. 选择是将上限应用于所有用户，还是只应用于一个配置文件。 [了解详情](#capping-type)

1. 设置 **[!UICONTROL 频率]** 以定义重置上限计数的频率。 [了解详情](#frequency-capping)

1. 如果已定义多个 [呈现](add-representations.md) 对于选件，指定是否要应用上限 **[!UICONTROL 在所有投放位置中]** 或 **[!UICONTROL 对于每个投放位置]**. [了解详情](#placements)

1. 保存并批准优惠后，如果根据您定义的标准和时间范围，已按照您在此字段中指定的次数向其显示优惠，则投放将停止。

在准备电子邮件时会计算建议使用选件的次数。 例如，如果您准备发送一封包含大量选件的电子邮件，则无论是否发送了这封电子邮件，这些数量都将计入您的最大上限。

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>当优惠到期时或优惠开始日期后2年后（以先到者为准），上限计数器将重置。 了解如何在中定义优惠的日期 [本节](creating-personalized-offers.md#create-offer).

### 设置事件上限 {#capping-event}

此 **[!UICONTROL 设置事件上限]** 字段允许您定义 **[!UICONTROL 设置事件上限]** 将考虑以增加计数器：

![](../assets/offer-capping-event.png)

* **[!UICONTROL 决策事件]** （默认值）：可显示选件的最大次数。
* **[!UICONTROL 展示]**：选件可向用户显示的最大次数。

   >[!NOTE]
   >
   >可将展示次数用作上限事件 **入站渠道** 仅此而已。

* **[!UICONTROL 点击次数]**：用户可单击选件的最大次数。
* **[!UICONTROL 自定义事件]**：您可以定义一个自定义事件，用于限制发送的优惠数量。 例如，您可以限制赎回次数，直到它们等于10000次，或者直到给定用户档案赎回了1次。 要执行此操作，请使用 [ADOBE EXPERIENCE PLATFORM XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"} 用于构建自定义事件规则的架构。

   <!--For example, you can cap on the number of redemptions so that the offer can be shown until redemptions equal 10000. You can only select XDM ExperienceEvents. -->

   在下面的示例中，您希望限制结账的数量。

   1. 选择 **[!UICONTROL 自定义事件]** ，并使用 **[!UICONTROL 添加自定义事件]** 按钮。

      ![](../assets/offer-capping-custom-event-add.png)

   1. 使用 **[!UICONTROL 创建自定义事件规则]** 生成器以选择相关事件。 您可以选择您希望限制选件的任何用户操作。

      在此选择 **[!UICONTROL 商务]** > **[!UICONTROL 结账]** > **[!UICONTROL 值]** 并选择 **[!UICONTROL 存在]** 下拉列表中。

      ![](../assets/offer-capping-custom-event.png)

   1. 创建规则后，该规则将显示在 **[!UICONTROL 自定义事件查询]** 字段。

      ![](../assets/offer-capping-custom-event-query.png)

>[!CAUTION]
>
>对于除决策事件之外的所有上限事件，决策管理反馈可能无法自动收集，这可能导致上限计数器无法正确递增。 [了解详情](../data-collection/data-collection.md)
>
>要确保在上限计数器中对每个上限事件进行跟踪和计数，请确保用于收集体验事件的架构包含该事件的正确字段组。 [了解详情](../data-collection/schema-requirement.md)

### 上限计数 {#capping-count}

此 **[!UICONTROL 上限计数]** 字段，用于指定可显示选件的次数。

![](../assets/offer-capping-times.png)

>[!NOTE]
>
>数字必须是大于0的整数。

例如，您定义了一个自定义上限事件，例如将结账数量考虑在内。 如果您在 **[!UICONTROL 上限计数]** 字段，10次结账后将不再发送任何优惠。

### 上限类型 {#capping-type}

您还可以指定要将上限应用于所有用户还是某个特定用户档案：

![](../assets/offer-capping-total.png)

* 选择 **[!UICONTROL 总计]** 定义可在组合目标受众中建议多少次选件，即在所有用户中均如此。

   例如，如果您是一家具有“TV doorbuster deal”的电子零售商，则希望在所有配置文件中仅返回200次选件。

* 选择 **[!UICONTROL 每个配置文件]** 定义可向同一用户建议多少次选件。

   例如，如果您是一家提供“白金信用卡”优惠的银行，您不希望每个用户档案显示此优惠超过5次。 实际上，您相信，如果用户查看了5次报价，但未对其执行操作，则他们更有可能对下一个最佳报价执行操作。

### 频次上限 {#frequency-capping}

此 **[!UICONTROL 频率]** 部分允许您定义重置上限计数的频率。 要执行此操作，请定义盘点期间（每天、每周或每月），并输入您选择的天数/周数/月数。

![](../assets/offer-capping-frequency.png)

>[!NOTE]
>
>重置发生在UTC凌晨12点（您定义的日期）或周/月的第一天（如果适用）。 工作开始日期是星期日。 您选择的任何持续时间不得超过2年（即相应的月数、周数或天数）。

例如，如果希望每2周重置一次上限计数，请选择 **[!UICONTROL 每周]** 从 **[!UICONTROL 重复]** 下拉列表和类型 **2** 在另一个栏位中。 重置将在每隔一个星期日的中午12点(UTC)发生。

>[!CAUTION]
>
>保存优惠后，您将无法更改为该频率选择的时间段（每月、每周或每日）。

### 上限和投放 {#placements}

如果已定义多个 [呈现](add-representations.md) 对于选件，指定是否要应用上限 **[!UICONTROL 在所有投放位置中]** 或 **[!UICONTROL 对于每个投放位置]**.

![](../assets/offer-capping-placement.png)

* **[!UICONTROL 在所有投放位置中]**：上限计数将总计与优惠关联的投放位置中的所有决策。

   例如，如果选件具有 **电子邮件** 投放位置和 **Web** 放置，并将上限设置为 **所有投放位置中每个配置文件2个**，则无论版面组合如何，每个用户档案最多可以接收总共2次选件。

* **[!UICONTROL 对于每个投放位置]**：上限计数将分别应用每个投放位置的决策计数。

   例如，如果选件具有 **电子邮件** 投放位置和 **Web** 放置，并将上限设置为 **每次投放每个用户档案2个**，则每个用户档案最多可收到选件2次（用于电子邮件投放），以及额外的2次（用于网站投放）。

### 更改日期对上限设置的影响 {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="更改日期可能会影响上限"
>abstract="如果此优惠具有上限，则在更改开始或结束日期时可能会影响该上限。"

更改优惠日期时必须小心操作，因为如果满足以下条件，这可能会影响上限：

* 选件为 [已批准](#review).
* [上限](#capping) 已应用于选件。
* 根据配置文件定义上限。

>[!NOTE]
>
>了解如何在中定义优惠的日期 [本节](creating-personalized-offers.md#create-offer).

每个配置文件设置上限会存储每个配置文件上的上限计数。 当您更改已批准优惠的开始日期和结束日期时，某些用户档案的上限计数可能会根据下面描述的不同情况受到影响。

![](../assets/offer-capping-change-date.png)

以下是以下情形的可能方案： **更改优惠开始日期**：

| 方案：<br>如果…… | 发生什么情况：<br>然后…… | 对上限计数的可能影响 |
|--- |--- |--- |
| ...优惠开始日期在原始优惠开始日期之前更新， | ...上限计数将从新的开始日期开始。 | 否 |
| ...新的开始日期早于当前结束日期， | ...上限将继续计为一个新的开始日期，每个用户档案的上一个上限计数将结转。 | 否 |
| ...新的开始日期在当前的结束日期之后， | ...当前上限将过期，新的上限计数将从新开始日期的所有配置文件的0重新开始。 | 是 |

以下是以下情形的可能方案： **延长优惠结束日期**：

| 方案：<br>如果…… | 发生什么情况：<br>然后…… | 对上限计数的可能影响 |
|--- |--- |--- |
| ...决策请求发生在原始优惠结束日期之前， | ...将更新上限计数，并将结转每个用户档案的上一个上限计数。 | 否 |
| ...在原始结束日期之前不会发生任何决策请求， | ...上限计数将在每个配置文件的原始结束日期重置。 对于在原始结束日期之后发生的任何新决策请求，新的上限计数将从0重新开始。 | 是 |

**示例**

假设您有一个优惠，其原始开始日期设置为 **1月1日**，到期日期 **1月，31日**.

1. 配置文件X、Y和Z将显示选件。
1. 日期 **1月10日**，则优惠的结束日期将更改为 **2,15**.
1. **一月十一日至一月三十一日**，则只有配置文件Z呈现选件。

   * 因为决策请求发生在原始结束日期之前 **配置文件Z**，优惠的结束日期可以延长到 **2,15**.
   * 但是，由于以下项的原始结束日期之前未发生任何活动： **配置文件X和Y**，其计数器将过期，其上限计数将重置为0于 **1月，31日**.

![](../assets/offer-capping-change-date-ex.png)
